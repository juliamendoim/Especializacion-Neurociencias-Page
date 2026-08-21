# CHILDES — Child Language Data Exchange System

**CHILDES** es la **base de datos internacional de adquisición del lenguaje** más importante del mundo. Contiene transcripciones de habla infantil y de interacciones niño-adulto en más de 50 lenguas, recolectadas durante cuatro décadas por equipos de investigación de todo el mundo y puestas a disposición pública. Es la infraestructura empírica sobre la que descansa buena parte de la psicolingüística contemporánea del desarrollo.

## Origen y propósito

Fundada en **1984** por **Brian MacWhinney** (Carnegie Mellon University) y **Catherine Snow** (Harvard), CHILDES surgió de una necesidad concreta: hasta los años 80, cada grupo de investigación recolectaba y transcribía sus propios datos de niños hablando, con sus propios formatos y criterios, y los resultados eran difíciles de comparar o replicar. Lo que MacWhinney y Snow propusieron fue **un estándar común** de transcripción y un **repositorio compartido** donde todos pudieran depositar sus datos para reutilización.

Es parte del proyecto más amplio **TalkBank** (https://talkbank.org), que extiende la misma idea a otras poblaciones (afasia, lectura, segunda lengua, conversación adulta, etc.).

Dirección oficial: **https://childes.talkbank.org**.

## Qué contiene

Lo central son las **transcripciones de niños interactuando con adultos** (típicamente padres, en contextos naturalistas: en casa, jugando, durante comidas) y de niños interactuando entre sí. Cada transcripción está acompañada, idealmente, de:

- Audio o video del registro original.
- Metadatos: edad del niño, contexto, lengua, situación.
- Anotaciones lingüísticas (morfología, sintaxis, errores).

Algunos de los **corpora más famosos** dentro de CHILDES:

| Corpus | Lengua | Aporte |
|---|---|---|
| **Brown** (Adam, Eve, Sarah) | Inglés | Los datos seminales de **Roger Brown (1973)** que fundaron el estudio sistemático de adquisición. Fueron de los primeros incorporados a CHILDES. |
| **Manchester** | Inglés británico | Recolección sistemática de 12 niños desde los 2 a los 3 años. Base de muchísimos análisis de Theakston, Lieven, Tomasello. |
| **MacWhinney** | Inglés | Datos longitudinales de los hijos del propio MacWhinney. |
| **Linaza, Vila, López-Ornat** | Español peninsular | Corpora pioneros para el estudio del español en adquisición. |
| **Aguirre** | Español | Datos de niños monolingües y bilingües en España. |
| **Sachs, Bates, Bloom** | Inglés | Otros clásicos longitudinales de niños individuales. |

Hoy CHILDES contiene cientos de corpora en lenguas tan distintas como mandarín, japonés, hebreo, francés, italiano, alemán, ruso, quechua, ASL y muchas más. **Cualquier investigador puede descargar los datos libremente y publicarlos sin permiso adicional** (con la única condición de citar el corpus original).

## Las herramientas: CHAT y CLAN

CHILDES no es solo una base de datos; es un **ecosistema metodológico**.

### CHAT — Codes for the Human Analysis of Transcripts

Es el **formato estándar** de transcripción. Define cómo se escriben las palabras del niño, las del adulto, los gestos, las pausas, las repeticiones, los errores, los morfemas. Una transcripción CHAT mínima tiene un aspecto como:

```
@Begin
@Participants:	CHI Sarah Target_Child, MOT Mother
@Age of CHI:	2;3.15
*MOT:	what's that?
*CHI:	doggy bow-wow.
%mor:	n|doggy n|bow-wow.
*MOT:	yes, the doggy says bow-wow.
@End
```

Lo que estandariza CHAT es que todos los datos en CHILDES tienen este formato, lo que hace posible escribir software de análisis que funcione sobre **cualquier corpus de la base**.

### CLAN — Computerized Language ANalysis

Es el **conjunto de herramientas de análisis** que permite procesar archivos CHAT: contar palabras, calcular MLU (longitud media de enunciado), identificar morfemas, hacer búsquedas, generar concordancias. Es gratuito y se descarga del sitio.

Con CLAN podés, por ejemplo:

- Calcular el MLU de un niño en un punto del desarrollo y comparar con normas.
- Buscar todas las ocurrencias de un morfema (por ejemplo, el -ndo del gerundio) y ver cuándo aparece por primera vez.
- Comparar la frecuencia de cierta estructura en el habla de la madre vs. la del niño.
- Extraer estadísticas para entrenar modelos computacionales.

## Por qué importa

### Para la psicolingüística del desarrollo

CHILDES hizo posible que la psicolingüística pase de hipótesis basadas en casos individuales (los hijos de los investigadores, observados anecdóticamente) a **investigación cuantitativa a gran escala**. Cualquier afirmación sobre adquisición del lenguaje hoy se puede contrastar con datos de CHILDES.

Ejemplo concreto: la pelea **Tomasello vs. innatistas** sobre si el niño aprende por construcciones (*usage-based*) o aplica reglas innatas (Pinker) **se libra en buena medida sobre datos de CHILDES**. Cuando Tomasello argumenta que el niño aprende patrones específicos de verbos antes de generalizar, lo que está haciendo es analizar corpora de Manchester o Brown. Cuando los innatistas responden, también suelen apoyarse en CHILDES.

### Para el debate sobre IA y lenguaje

Esto es lo que vuelve a CHILDES central para el cruce IA / neurociencia: **CHILDES proporciona los corpora con los que se entrenan los BabyLMs**.

Un *BabyLM* es un modelo de lenguaje entrenado con cantidades de input **comparables a las que recibe un niño** en sus primeros años (~10⁷-10⁸ palabras), en lugar de los ~10¹¹-10¹³ tokens que recibe un LLM comercial. El **BabyLM Challenge** (Warstadt et al. 2023) construyó su corpus de entrenamiento explícitamente usando texto extraído de CHILDES + otras fuentes orientadas al niño (libros infantiles, transcripciones de programas, etc.).

Resultados de esa línea de investigación:

- **Yedetore, Linzen et al. (2023)** "How poor is the stimulus?": entrenan redes con cantidades CHILDES-equivalentes y muestran que **no logran las generalizaciones jerárquicas que los niños hacen sin esfuerzo**. Argumento moderno y poderoso a favor de sesgos inductivos específicos del humano.
- **Hosseini et al. (2024)**: redes neuronales entrenadas con corpus realistas (similares a los datos infantiles) siguen prediciendo bien la actividad cerebral humana. Sugiere que la asimetría humano-LLM no es solo cantidad de datos, sino algo más profundo.
- **Warstadt et al. (2023)** "Findings of the BabyLM Challenge": resultados de cientos de equipos que entrenaron modelos con corpus reducidos. Conclusión preliminar: con escala humana de datos, las redes hacen bastante pero no lo suficiente como para igualar al niño.

Sin CHILDES, esta línea de investigación no existiría. Es la única forma de tener una **base de comparación rigurosa** entre humanos y modelos en términos de input cuantitativo realista.

### Para la clínica y la evaluación

CHILDES también es referencia para construir **normas de adquisición**: a qué edad aparece típicamente cierto morfema, cierta estructura, cierto vocabulario. Eso permite diagnosticar **retrasos** del desarrollo lingüístico (TDL, por ejemplo) por comparación con la trayectoria esperada.

Para el español específicamente, los corpora de **Linaza, Vila y López-Ornat** son referencia obligada en estudios sobre adquisición del español peninsular, y han influido en investigaciones argentinas sobre adquisición y TDL.

## Limitaciones y críticas

- **Sesgo de muestra**: muchos corpora son de niños de clase media-alta, en contextos urbanos, con padres educados. La diversidad sociocultural está representada pero no de manera proporcional.
- **Naturaleza de los datos**: son transcripciones de interacciones grabadas, lo que implica que los padres saben que están siendo grabados — el habla puede estar ligeramente artificializada. El "habla casera real" es difícil de capturar.
- **Cobertura cuantitativa por niño**: aunque CHILDES es enorme en agregado, **cada niño individual tiene relativamente pocas horas registradas** (cientos de horas en los mejores casos). Estimar el input total de un niño hasta los 3 años (que es del orden de millones de palabras) requiere extrapolación.
- **Sesgo hacia el inglés**: aunque hay más de 50 lenguas, el inglés está sobrerrepresentado, lo que sesga las conclusiones teóricas hacia patrones del inglés.

## Cómo accederla

1. Ir a https://childes.talkbank.org.
2. Navegar por lengua, por tipo de población, por edad.
3. Descargar los archivos `.cha` (formato CHAT).
4. Bajar CLAN desde el mismo sitio si querés analizarlos.
5. Citar el corpus original siempre que uses datos.

El manual completo, el libro de MacWhinney *The CHILDES Project*, está disponible gratis en PDF en el sitio. Es **lectura recomendada** para cualquier estudio empírico sobre adquisición.

## Referencias

- **MacWhinney, B. (2000)** *The CHILDES Project: Tools for Analyzing Talk* (3ª ed.). Mahwah, NJ: Lawrence Erlbaum. **El manual de referencia.** Descargable en https://talkbank.org/manuals/CHAT.pdf
- **MacWhinney, B. y Snow, C. (1985)** "The Child Language Data Exchange System". *Journal of Child Language*, 12, 271-296. El paper fundacional.
- **Brown, R. (1973)** *A First Language: The Early Stages*. Cambridge, MA: Harvard UP. **El libro fundacional** del estudio sistemático de la adquisición en inglés. Los corpora de Adam, Eve y Sarah provienen de este trabajo.
- **Warstadt, A. et al. (2023)** "Findings of the BabyLM Challenge: Sample-efficient pretraining on developmentally plausible corpora". *CoNLL*. La iniciativa contemporánea de entrenar modelos con cantidades realistas de input.

## Conexiones en este sitio

- [Garden paths](../modelos-cognitivos/garden-paths.md) — los corpora CHILDES también se usan para estudiar el procesamiento sintáctico temprano.
- [Surprisal](../modelos-cognitivos/surprisal.md) — los modelos entrenados en CHILDES sirven para calcular surprisal "realista" comparable con datos humanos.
- [Aprendizajes generales](../aprendizajes-generales.md) — la sección sobre autoorganización cerebral vs. big data discute los resultados de los modelos entrenados con corpus tipo CHILDES.
