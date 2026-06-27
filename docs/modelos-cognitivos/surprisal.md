# Surprisal en LLMs y procesamiento del lenguaje

## El concepto raíz

**Surprisal** es un concepto de la **teoría de la información** (Shannon, 1948). Mide *cuán sorprendente* es un evento dado un contexto, en términos cuantitativos:

```
surprisal(palabra) = −log P(palabra | contexto)
```

Traducido:

- Si una palabra tiene **probabilidad alta** dado el contexto (predecible) → surprisal **baja** (poca sorpresa).
- Si tiene **probabilidad baja** (inesperada) → surprisal **alta**.
- El logaritmo es lo que la convierte en una escala "psicológicamente lineal" — lo desarrollo en la sección **¿Por qué logaritmo?** más abajo.

La unidad son **bits** (con log base 2) o **nats** (con log natural). En psicolingüística se reporta usualmente en bits.

Ejemplo intuitivo. Después de *"El gato persigue al…"*:

- *"…ratón"* → probabilidad alta → surprisal baja
- *"…tractor"* → probabilidad baja → surprisal alta

<figure markdown>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 380" role="img" aria-label="Surprisal en función de la probabilidad del token: curva del logaritmo negativo">
  <defs>
    <pattern id="grid-surp" width="49" height="35.7" patternUnits="userSpaceOnUse">
      <path d="M 49 0 L 0 0 0 35.7" fill="none" stroke="#e8e8f5" stroke-width="0.7"/>
    </pattern>
  </defs>
  <rect x="70" y="40" width="490" height="250" fill="url(#grid-surp)"/>
  <line x1="70" y1="290" x2="560" y2="290" stroke="#222" stroke-width="1.5"/>
  <line x1="70" y1="290" x2="70" y2="40" stroke="#222" stroke-width="1.5"/>
  <g font-family="system-ui, -apple-system, sans-serif" font-size="11" fill="#444" text-anchor="middle">
    <text x="70" y="307">0</text>
    <text x="168" y="307">0.2</text>
    <text x="266" y="307">0.4</text>
    <text x="364" y="307">0.6</text>
    <text x="462" y="307">0.8</text>
    <text x="560" y="307">1.0</text>
  </g>
  <g font-family="system-ui, -apple-system, sans-serif" font-size="11" fill="#444" text-anchor="end">
    <text x="63" y="294">0</text>
    <text x="63" y="258">1</text>
    <text x="63" y="222">2</text>
    <text x="63" y="187">3</text>
    <text x="63" y="151">4</text>
    <text x="63" y="115">5</text>
    <text x="63" y="79">6</text>
    <text x="63" y="44">7</text>
  </g>
  <text x="315" y="332" font-family="system-ui, -apple-system, sans-serif" font-size="13" fill="#222" text-anchor="middle">P(palabra | contexto)</text>
  <text x="22" y="165" font-family="system-ui, -apple-system, sans-serif" font-size="13" fill="#222" text-anchor="middle" transform="rotate(-90 22 165)">surprisal = −log₂ P  (bits)</text>
  <text x="315" y="24" font-family="system-ui, -apple-system, sans-serif" font-size="14" fill="#1a1a1a" text-anchor="middle" font-weight="600">La curva del logaritmo negativo</text>
  <polyline points="74.9,52.7 79.8,88.4 84.7,109.3 94.5,135.6 104.3,153.0 119.0,171.4 143.5,192.3 168.0,207.1 217.0,228.0 266.0,242.8 315.0,254.3 364.0,263.7 413.0,271.6 462.0,278.5 511.0,284.6 560.0,290.0" fill="none" stroke="#3F51B5" stroke-width="2.8" stroke-linejoin="round" stroke-linecap="round"/>
  <circle cx="511" cy="284.6" r="5" fill="#43A047" stroke="white" stroke-width="1.5"/>
  <text x="503" y="270" font-family="system-ui, -apple-system, sans-serif" font-size="11" fill="#2E7D32" text-anchor="end" font-weight="500">esperable (P≈0.9, S≈0.15)</text>
  <circle cx="217" cy="228" r="5" fill="#FB8C00" stroke="white" stroke-width="1.5"/>
  <text x="227" y="223" font-family="system-ui, -apple-system, sans-serif" font-size="11" fill="#E65100" font-weight="500">poco esperada (P≈0.3, S≈1.7)</text>
  <circle cx="94.5" cy="135.6" r="5" fill="#E53935" stroke="white" stroke-width="1.5"/>
  <text x="105" y="131" font-family="system-ui, -apple-system, sans-serif" font-size="11" fill="#B71C1C" font-weight="500">inesperada (P≈0.05, S≈4.3)</text>
</svg>
<figcaption markdown>**Surprisal en función de la probabilidad del token**. Cuando la palabra es esperable (P alta), la surprisal es casi cero — el sistema "ya la tenía". Cuando es inesperada (P baja), la surprisal crece rápido y sin cota cuando P → 0. La curva es **cóncava**: el costo no escala lineal con la rareza, sino logarítmicamente, lo que coincide con lo que se observa en tiempos de lectura humanos (Smith & Levy, 2013).</figcaption>
</figure>

## Un ejemplo numérico

Supongamos que después del contexto *"El gato persigue al…"* un modelo de lenguaje (un LLM, o un humano hipotético) asigna las siguientes probabilidades a posibles continuaciones:

| Palabra | P(palabra \| contexto) | Surprisal (bits) | Cálculo |
|---|---|---|---|
| ratón | 0.40 | **1.32** | $-\log_2 0.40 = 1.32$ |
| pájaro | 0.20 | **2.32** | $-\log_2 0.20 = 2.32$ |
| niño | 0.10 | **3.32** | $-\log_2 0.10 = 3.32$ |
| ladrón | 0.02 | **5.64** | $-\log_2 0.02 = 5.64$ |
| tractor | 0.0001 | **13.29** | $-\log_2 0.0001 = 13.29$ |

Si la teoría surprisal de Levy es correcta (ver abajo), el tiempo de lectura para *"tractor"* debería ser ~10× más alto que para *"ratón"* (sumando un baseline constante para procesos comunes a todos los tokens: acceso visual, articulación, etc.).

Lo notable, y lo que motiva el uso del logaritmo: la diferencia entre P=0.40 y P=0.20 (factor 2 en probabilidad) suma **1 bit** de surprisal. La diferencia entre P=0.0001 y P=0.00005 (también factor 2) suma **1 bit** también. Lo que importa **no es la diferencia absoluta de probabilidades, sino el factor multiplicativo entre ellas**. Sobre este punto vuelvo en la sección de abajo.

## Por qué importa: la teoría surprisal de Levy (2008)

**Roger Levy** propuso en *"Expectation-based syntactic comprehension"* (Cognition, 2008) una hipótesis fuerte: **el tiempo de procesamiento de una palabra es proporcional a su surprisal**.

```
RT(palabra) ≈ k × surprisal(palabra)
```

Cuanto más sorprendente la palabra dado el contexto, más tarda el cerebro en procesarla. Esa hipótesis unifica un montón de fenómenos psicolingüísticos:

- **Efectos de frecuencia**: palabras frecuentes son más probables a priori → menor surprisal → menor RT.
- **Efectos de predictibilidad contextual**: palabras esperadas por el contexto se procesan más rápido (lo que se medía con tareas de cloze).
- **[Garden paths](garden-paths.md)**: el disambiguador tiene baja probabilidad bajo la interpretación inicial → surprisal alta → RT alta. Eso explica el "spike" de tiempo de lectura.
- **Sintaxis sin parser explícito**: cualquier estructura sintáctica que afecte la distribución de probabilidades de la siguiente palabra se refleja en surprisal.

## ¿Por qué logaritmo? La escala "psicológicamente lineal"

La forma logarítmica de la fórmula no es arbitraria. Tiene **tres justificaciones convergentes** que vale la pena tener separadas:

### 1. Justificación teórica (información de Shannon)

Shannon (1948) demostró que si querés que la información de eventos independientes **se sume** (en lugar de multiplicarse), la única función que cumple eso es el logaritmo de la probabilidad. Para dos eventos independientes A y B:

$$S(A \cap B) = -\log P(A)P(B) = -\log P(A) - \log P(B) = S(A) + S(B)$$

Sin el logaritmo no podrías sumar contribuciones independientes — tendrías que multiplicarlas, lo cual es contraintuitivo como medida de "esfuerzo acumulado". El logaritmo convierte productos de probabilidades (la regla matemática para eventos independientes) en sumas de surprisal (lo que se siente como costo aditivo).

### 2. Justificación empírica (Smith & Levy 2013)

Smith & Levy (2013) hicieron el test crítico: ¿el RT humano escala lineal o logarítmicamente con la probabilidad? Usaron una variedad de modelos de lenguaje con distintos niveles de calidad, calcularon probabilidades para palabras en corpus de eye-tracking, y testearon ambos modelos contra datos humanos.

**Resultado**: el efecto es **logarítmico, no lineal**. La diferencia entre P=0.5 y P=0.25 (factor 2) produce el mismo aumento de RT que la diferencia entre P=0.001 y P=0.0005 (también factor 2). Validación empírica directa de la forma matemática.

### 3. Conexión con la ley de Weber-Fechner

En psicofísica clásica (Fechner 1860), la **magnitud subjetiva percibida** (intensidad de un sonido, brillo de una luz, peso) escala **logarítmicamente** con la magnitud física. Pasar el volumen de 60 a 70 dB se percibe como un aumento similar al de 80 a 90 dB — el mismo factor multiplicativo, no el mismo incremento aditivo.

La surprisal y el RT comparten esta forma: lo "psicológicamente lineal" es el **logaritmo de la probabilidad**, no la probabilidad bruta. El sistema cognitivo opera en escala logarítmica de probabilidad, **igual que opera en escala logarítmica de intensidad sensorial**. Esto es lo que se quiere decir cuando se afirma que el logaritmo convierte la sorpresa probabilística en una escala psicológicamente lineal.

## Cómo se mide surprisal con un LLM

Los LLMs son **modelos probabilísticos del lenguaje**: dada una secuencia, asignan a cada posible siguiente token una probabilidad. Esa es exactamente la distribución que necesitás para calcular surprisal.

Procedimiento típico:

1. Tomás una oración de prueba: *"The horse raced past the barn fell."*
2. Pasás los tokens uno por uno al LLM.
3. Para cada token, mirás la **log-probabilidad** que el modelo le asignó dado el contexto previo.
4. El **negativo** de esa log-probabilidad es la surprisal de ese token.
5. Comparás surprisals entre condiciones (garden path vs. control, frecuente vs. infrecuente, etc.).

Las APIs de OpenAI, Anthropic y los modelos open-weight (Llama, Mistral, etc.) **te devuelven log-probs directamente** — no hace falta entrenar nada. Es lo que vuelve a los LLMs una mina de oro para psicolingüistas: te dan un **modelo expectativo gratis** sobre el cual se computan predicciones.

## Por qué los LLMs cambiaron el campo

Antes de los LLMs, calcular surprisal requería:

- Entrenar un modelo de lenguaje propio (n-gramas, gramáticas probabilísticas).
- Lidiar con problemas de cobertura: si la oración tenía palabras raras o construcciones complejas, el modelo se rompía.
- Decidir manualmente qué contexto considerar.

Con un LLM moderno todo eso desaparece. Tenés un modelo que cubre prácticamente cualquier texto en el idioma, ya pre-entrenado, y devuelve probabilidades para cualquier secuencia. Por eso desde 2018 explotó la literatura usando LLMs como **psycholinguistic subjects**: se les hace pasar por experimentos diseñados para humanos y se mide surprisal en lugar de RT.

## Lo que predice bien y lo que no

**Predice bien:**

- Efectos de frecuencia léxica.
- Efectos de predictibilidad contextual (cloze probability).
- [Garden paths](garden-paths.md) — el disambiguador tiene surprisal alta.
- Efectos de complejidad sintáctica (oraciones con dependencias largas tienen surprisal acumulada mayor).
- Concordancia sujeto-verbo a distancia.

**No predice tan bien:**

- **Magnitud absoluta del costo de reanalysis**: van Schijndel & Linzen (2021) mostraron que el surprisal de los LLMs **subestima** el RT humano en garden paths. La gente sufre más de lo que un cálculo limpio de surprisal predeciría — sugiere que hay procesos extra (re-estructuración representacional) que el surprisal no captura.
- **Asimetrías de orden de procesamiento**: a veces lo que cuesta más en humanos no se refleja en la surprisal de la palabra esperada.
- **Diferencias individuales**: surprisal es un cálculo a nivel modelo; los humanos varían entre sí en función de memoria de trabajo, vocabulario, etc.

## El "sweet spot" de tamaño de modelo

Un hallazgo interesante: **modelos más grandes no necesariamente predicen mejor el RT humano**. Oh & Schuler (2023) mostraron que hay un punto óptimo: modelos medianos (~125M-1B parámetros) predicen RT humano *mejor* que modelos enormes (GPT-3, GPT-4).

Razón intuitiva: los modelos enormes tienen tan buena memoria distribucional que **no se sorprenden** con cosas que sí sorprenden a humanos. Su surprisal es más uniforme. Los modelos medianos, con menos capacidad, tienen surprisal más "humana".

Esto conecta con el debate de Yedetore et al. (2023): cuando reducís el modelo a un tamaño comparable al input infantil, **se vuelve más humano** — pero también más limitado.

## Más allá del costo: UID — uniform information density (Jaeger & Tily)

Hasta acá vimos surprisal como **medida descriptiva** del costo de procesamiento del oyente. Pero también tiene un uso **normativo** importante: la hipótesis de **uniform information density (UID)**, propuesta por Levy & Jaeger (2007) y desarrollada principalmente por **T. Florian Jaeger** y **Harry Tily**.

**La hipótesis central**: los hablantes estructuran sus enunciados para que la información (medida en surprisal) se distribuya de manera **aproximadamente uniforme** a lo largo del enunciado. Picos de surprisal son costosos para el oyente; un buen hablante los evita redistribuyendo la información.

Esto invierte la mirada: surprisal no es solo lo que **sufre el oyente al procesar**, también es lo que **el hablante optimiza al producir**.

**Predicciones empíricas que se han confirmado**:

- **Palabras opcionales** (el "*that*" del inglés en *"the fact that…"*, los pronombres en lenguas pro-drop como el español) tienden a usarse cuando lo que viene después es de alta surprisal — para "amortiguar" el pico. Cuando lo que viene es predecible, se omiten — porque no hace falta amortiguar.
- **Reducciones fonológicas** (vocales reducidas, contracciones) ocurren preferentemente en palabras de baja surprisal, donde el riesgo de pérdida de información es menor.
- En lenguas con **orden de palabras flexible**, los hablantes prefieren órdenes que distribuyen la información de manera más uniforme.
- **Velocidad del habla**: las palabras de baja surprisal se pronuncian más rápido; las de alta surprisal, más lento. Esto está documentado en corpus de habla espontánea (Aylett & Turk 2004; Jaeger 2010).

**El paper canónico** es **Jaeger (2010)** "Redundancy and reduction: Speakers manage syntactic information density" (*Cognitive Psychology* 61:23-62), que muestra evidencia empírica fuerte de que la omisión opcional del *that* complementizador en inglés se predice bien por surprisal local.

**Para el debate IA / cerebro**: UID predice algo que los LLMs no necesariamente hacen — los LLMs se entrenan para **minimizar surprisal promedio**, no para producir surprisal **uniforme** a lo largo del output. Eso da un test interesante: ¿el output de un LLM tiene picos de surprisal que un hablante humano evitaría? Si sí, esa es una asimetría productiva-cognitiva entre humanos y máquinas que vale la pena estudiar — y que conecta con el debate sobre por qué el texto generado por LLMs a veces "suena raro" aun cuando es gramaticalmente impecable.

## Conexión con el resto del campo

**Hale (2001)** introdujo formalmente la idea de surprisal aplicada al parsing en *"A probabilistic Earley parser as a psycholinguistic model"*. **Levy (2008)** la generalizó y le dio soporte empírico fuerte. Desde entonces es **la** medida estándar para vincular modelos computacionales del lenguaje con datos de procesamiento humano.

Hay competencia teórica: modelos basados en **memoria** (Lewis & Vasishth 2005, modelos de activación tipo ACT-R) en lugar de **expectativa** (Levy). El consenso actual es que ambos contribuyen — no es expectativa o memoria, es ambas. Pero surprisal es la métrica más limpia y más fácil de calcular, así que domina la literatura empírica.

## Lecturas recomendadas

- **Hale, J. (2001)** "A probabilistic Earley parser as a psycholinguistic model". El paper-bisagra.
- **Levy, R. (2008)** "Expectation-based syntactic comprehension". *Cognition* 106(3):1126-1177. **El paper a leer si vas a leer uno solo.**
- **Smith, N. J. & Levy, R. (2013)** "The effect of word predictability on reading time is logarithmic". *Cognition* 128(3):302-319.
- **Goodkind & Bicknell (2018)** "Predictive power of word surprisal for reading times is a linear function of language model quality".
- **Wilcox et al. (2020)** "On the predictive power of neural language models for human real-time comprehension behavior".
- **Oh & Schuler (2023)** "Why does surprisal from larger transformer-based language models provide a poorer fit to human reading times?".
- **van Schijndel & Linzen (2021)** "Single-stage prediction models do not explain the magnitude of syntactic disambiguation difficulty".
- **Levy, R. & Jaeger, T. F. (2007)** "Speakers optimize information density through syntactic reduction" *NeurIPS*. **El paper fundacional de UID.**
- **Jaeger, T. F. (2010)** "Redundancy and reduction: Speakers manage syntactic information density" *Cognitive Psychology* 61(1):23-62.
- **Jaeger, T. F. & Tily, H. (2011)** "On language 'utility': Processing complexity and communicative efficiency" *Wiley Interdisciplinary Reviews: Cognitive Science* 2(3):323-335. **Revisión accesible de UID y procesamiento.**
- **Aylett, M. & Turk, A. (2004)** "The smooth signal redundancy hypothesis" *Language and Speech* 47:31-56. Precursor empírico de UID en fonética.
- **Fechner, G. T. (1860)** *Elemente der Psychophysik*. La ley logarítmica de la percepción — antecedente conceptual del logaritmo en surprisal.
