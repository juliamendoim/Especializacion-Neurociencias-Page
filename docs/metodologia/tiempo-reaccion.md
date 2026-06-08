# Tareas de tiempo de reacción (TR)

**TR = tiempo de reacción**: el intervalo entre la presentación de un estímulo y la respuesta del sujeto, medido en milisegundos. **De Vega** ("Introducción a la psicología cognitiva", 1984) lo usa en el sentido clásico de la psicología cognitiva: una **medida indirecta de procesos mentales no observables**.

La lógica es heredada de **Donders (1868)** y revivida por **Sternberg (1969)**: si un proceso mental existe, *ocupa tiempo*. Comparando condiciones que difieren en un solo proceso, se puede aislar la duración de ese proceso. En la era pre-neuroimagen, el TR era la principal ventana al "mecanismo interno".

## El supuesto fuerte: *pure insertion* de Donders

Si la condición A y la condición B difieren **solo** en un proceso X, entonces:

$$TR(B) - TR(A) = \text{duración de } X$$

Esta asunción — llamada **pure insertion** — sostiene casi todos los experimentos clásicos del libro de De Vega. Es controversial: implica que agregar un proceso no modifica los otros, algo que no siempre se cumple.

## Tipos de tareas de TR

### TR simple
Un solo estímulo, una sola respuesta. Mide tiempo basal de detección + ejecución motora. Útil como línea de base.

### TR de elección (*choice RT*)
Varios estímulos posibles, cada uno con su respuesta. La **ley de Hick (1952)**:

$$TR = a + b \cdot \log_2(n)$$

donde $n$ es el número de alternativas. El TR crece logarítmicamente con la cantidad de opciones — evidencia de que la decisión escala con la incertidumbre (en bits).

### TR de discriminación / *go-no go*
Responder solo a algunos estímulos, inhibir la respuesta a otros. Aísla **decisión** y **control inhibitorio**.

### Tarea de Sternberg (*memory scanning*)
Se presenta un set de ítems (ej.: 2, 4 o 6 dígitos), después un ítem de prueba; el sujeto decide si estaba o no. La **pendiente** del TR en función del tamaño del set revela si la búsqueda es:

- **Serial exhaustiva**: pendiente igual en sí/no → revisa todos los ítems aun cuando ya encontró.
- **Serial autoterminada**: pendiente menor para "sí" que para "no".
- **Paralela**: pendiente plana.

Sternberg encontró pendientes paralelas en sí/no (~38 ms por ítem) → **búsqueda serial exhaustiva en memoria de corto plazo**.

### Decisión léxica
¿Es palabra o no? (ej.: *casa* sí / *terc* no). Mide **acceso al léxico**. Es la tarea workhorse de la psicolingüística experimental.

### *Priming* (semántico, repetido, ortográfico, etc.)
Si un estímulo previo (prime) facilita el siguiente (target), el TR baja → evidencia de **activación propagada** en la red de representaciones. Ej.: "pan" → "manteca" se responde más rápido que "pan" → "guitarra".

### Stroop
Leer "ROJO" escrito en tinta azul. El TR como índice de **interferencia** entre lectura automática y nombrado de color → ventana al **control ejecutivo**.

### *Posner cueing*
Una pista predice (o no) dónde aparecerá el target. TR menor cuando la pista es válida → mide **orientación de la atención**.

## TR vs. precisión: el *speed-accuracy tradeoff*

De Vega es prolijo en distinguir TR (que mide procesos cognitivos) de **precisión / tasa de error** (que mide otra cosa). El sujeto puede *negociar* uno por el otro: si lo apurás, va más rápido pero comete más errores; si le pedís precisión, tarda más. Hay que reportar **ambas variables** y hacer análisis condicionales (TR solo de los ensayos correctos, por ejemplo).

## Críticas y matices

- **Pure insertion falla**: agregar un proceso *modifica* los anteriores (efecto cascada, no aditivo).
- **Variabilidad inter-sujeto** alta: hay que comparar dentro del sujeto, no entre.
- **Estrategias del sujeto**: el TR no es "puro", está moldeado por motivación, expectativa, fatiga.
- **El TR es un agregado**: incluye percepción + decisión + selección de respuesta + ejecución motora. Aislar el componente cognitivo requiere diseños sustractivos cuidadosos.
- **Modelos modernos** (drift-diffusion, LATER, race models) ya no asumen etapas discretas: modelan el TR como un proceso continuo de **acumulación de evidencia** hasta un umbral. Estos modelos descomponen el TR en parámetros (tasa de drift, umbral, tiempo no-decisional) y son la herencia técnica del programa de Sternberg.

## Lo que De Vega quería que te llevaras

Que el TR no es "cuánto tarda alguien en apretar un botón" sino **una herramienta para descomponer la cognición en etapas medibles**. En los 80, cuando él escribe, esa era la principal evidencia empírica de la **arquitectura modular de la mente** — antes de que la neuroimagen tomara el relevo.

El TR sigue siendo central hoy en psicolingüística (decisión léxica, lectura auto-administrada, *eye tracking* con métricas de fijación), pero ahora se combina con EEG/MEG (que dan resolución temporal todavía mayor) y modelos computacionales que predicen TR a partir de variables como [surprisal](../modelos-cognitivos/surprisal.md).

## Conexiones en este sitio

- [Surprisal](../modelos-cognitivos/surprisal.md) — usa TR de lectura (auto-administrada o *eye tracking*) como variable dependiente predicha por modelos de lenguaje.
- [Garden paths](../modelos-cognitivos/garden-paths.md) — el TR aumenta cuando el parser tiene que reanalizar; ventana al procesamiento sintáctico en tiempo real.
- [Activación](../modelos-cognitivos/activacion.md) — el priming (medido con TR) es la evidencia conductual más directa de propagación de activación.

## Lecturas

- **De Vega, M. (1984).** *Introducción a la psicología cognitiva*. Alianza. — Cap. introductorio sobre métodos: dónde encaja TR en el programa cognitivo.
- **Donders, F. C. (1868).** *On the speed of mental processes*. Reimpreso en *Acta Psychologica* 30, 412-431 (1969). El origen del método sustractivo.
- **Sternberg, S. (1969).** "The discovery of processing stages: Extensions of Donders' method". *Acta Psychologica*, 30, 276-315. El paper fundacional del *additive factors method*.
- **Posner, M. I. (1978).** *Chronometric explorations of mind*. — Tratado clásico sobre cronometría mental.
- **Ratcliff, R. & McKoon, G. (2008).** "The diffusion decision model: theory and data for two-choice decision tasks". *Neural Computation*, 20, 873-922. — La actualización moderna: modelar el TR como acumulación de evidencia, no como suma de etapas.
