# Surprisal en LLMs y procesamiento del lenguaje

## El concepto raíz

**Surprisal** es un concepto de la **teoría de la información** (Shannon, 1948). Mide *cuán sorprendente* es un evento dado un contexto, en términos cuantitativos:

```
surprisal(palabra) = −log P(palabra | contexto)
```

Traducido:

- Si una palabra tiene **probabilidad alta** dado el contexto (predecible) → surprisal **baja** (poca sorpresa).
- Si tiene **probabilidad baja** (inesperada) → surprisal **alta**.
- El logaritmo es lo que la convierte en una escala "psicológicamente lineal" (volveré a esto).

La unidad son **bits** (con log base 2) o **nats** (con log natural). En psicolingüística se reporta usualmente en bits.

Ejemplo intuitivo. Después de *"El gato persigue al…"*:

- *"…ratón"* → probabilidad alta → surprisal baja
- *"…tractor"* → probabilidad baja → surprisal alta

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

**El logaritmo es crucial**. Smith & Levy (2013) mostraron empíricamente que el efecto de la probabilidad sobre el tiempo de lectura es **logarítmico, no lineal**. Eso valida la fórmula matemática y le da soporte empírico a la teoría.

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
