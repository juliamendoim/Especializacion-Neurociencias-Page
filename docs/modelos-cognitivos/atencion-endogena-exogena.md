# Atención endógena vs. exógena (y las redes frontoparietales)

En psicología cognitiva, la distinción **endógeno / exógeno** es canónica. Aparece en De Vega ("Introducción a la psicología cognitiva", 1984) y se mantiene central en la neurociencia cognitiva contemporánea, con un sustrato neural disociable: dos redes frontoparietales descriptas por **Corbetta & Shulman (2002)**.

## La distinción cognitiva base

| | Endógeno | Exógeno |
|---|---|---|
| **Origen** | Interno (objetivos, intenciones, expectativas) | Externo (estímulo saliente) |
| **Carácter** | Voluntario, controlado | Automático, capturado |
| **Estilo** | *Top-down* | *Bottom-up* |
| **Velocidad** | Lento (~300 ms) | Rápido (~100 ms) |
| **Modulable por instrucción** | Sí | No (o muy poco) |
| **Esfuerzo cognitivo** | Alto | Bajo |

El **mecanismo endógeno** es la manera operacional con la que De Vega — y la psicología cognitiva clásica — habla de **voluntad, intención, control deliberado** sin caer en vocabulario filosófico cargado (la "voluntad" cartesiana, el "yo" husserliano). Es el mismo movimiento que hace con [el término "conciencia"](../neurobiologia/tinbergen-niveles-analisis.md): operacionalizar lo que la tradición fenomenológica trataba como categoría primaria.

## El paradigma experimental: Posner cueing (1980)

La distinción se vuelve medible con el **Posner cueing task**:

- **Pista endógena**: una flecha central (← o →) indica dónde aparecerá el target. El sujeto **interpreta** el símbolo y orienta su atención voluntariamente.
- **Pista exógena**: un flash periférico (un cuadrado parpadea) en la posición donde aparecerá el target. La atención se va sola, automáticamente, aunque la pista sea no informativa.

**Métrica de TR**: en ambas condiciones, los TRs son **más rápidos** cuando la pista es válida y **más lentos** cuando es inválida (cost-benefit). Pero el **timing y la flexibilidad** difieren entre los dos tipos.

## El nivel neural: dos redes frontoparietales disociables

**Corbetta & Shulman (2002)** "Control of goal-directed and stimulus-driven attention in the brain" *Nature Reviews Neuroscience* propusieron — sobre la base de fMRI + datos de neuropsicología — un modelo de **dos sistemas atencionales separados**, anatómica y funcionalmente:

### Red dorsal frontoparietal (atención endógena)

| Componente | Localización |
|---|---|
| **FEF** (frontal eye fields) | Surco precentral, área 8 de Brodmann |
| **IPS / SPL** | Sulcus intraparietal y lóbulo parietal superior |

**Función**: control voluntario, mantenimiento del *set* atencional, sostenimiento del objetivo en el tiempo, generación de **mapas espaciales** de prioridad. **Bilateral**.

### Red ventral frontoparietal (atención exógena)

| Componente | Localización |
|---|---|
| **TPJ** (temporoparietal junction) | Unión temporoparietal |
| **VFC** (ventral frontal cortex) | Incluye IFG (giro frontal inferior) y MFG (giro frontal medio) |

**Función**: detección de estímulos **salientes inesperados** (un cambio brusco, un sonido fuerte, un nombre propio). Actúa como **"circuit breaker"** — interrumpe a la red dorsal para re-orientar hacia lo nuevo. **Lateralizada a la derecha**.

### La interacción entre ambas

El modelo de Corbetta & Shulman es **dinámico**: las dos redes no operan en paralelo independiente. La red **ventral interrumpe a la dorsal** cuando aparece algo saliente; después la red dorsal **suprime a la ventral** mientras se mantiene el foco. La atención cotidiana es un **balance** entre ambas — sostener foco vs. estar receptivo a lo nuevo.

## Evidencia clínica que disocia ambos sistemas

- **Lesiones de la red dorsal** (parietal superior, FEF): déficits en atención **voluntaria sostenida**, dificultad para mantener un foco contra distractores; pero la captura por estímulos salientes se conserva.
- **Lesiones de la red ventral derecha** (TPJ, especialmente lado derecho): **negligencia espacial unilateral** (heminegligencia) — el paciente "no se da cuenta" del lado izquierdo del espacio, falla en re-orientar la atención hacia estímulos nuevos del lado contralesional. Es el sello clínico clásico del lóbulo parietal derecho.

Esta **doble disociación** es la evidencia más fuerte de que son dos sistemas neurales separables, no una sola "atención".

## El modelo paralelo de Posner: tres redes atencionales

**Posner & Petersen (1990)**, actualizado en **Petersen & Posner (2012)** *Annual Review of Neuroscience*, propone tres redes atencionales en lugar de dos:

| Red | Función | Sustrato neural |
|---|---|---|
| **Alerting** (alerta) | Mantener estado de vigilancia, prepararse para responder | Locus coeruleus, sistema noradrenérgico |
| **Orienting** (orientación) | Seleccionar info del input (≈ endógeno + exógeno de Corbetta-Shulman) | Sistemas frontoparietales (dorsal + ventral) |
| **Executive** (control ejecutivo) | Resolver conflicto, monitorear errores, control top-down | Corteza cingulada anterior (ACC), PFC dorsolateral |

El modelo de Posner-Petersen y el de Corbetta-Shulman **no compiten** — el "orienting" de Posner se descompone en los dos sistemas (dorsal endógeno + ventral exógeno) de Corbetta. Son niveles complementarios de descripción.

## ¿Por qué importa esta distinción para el cruce humanos / LLMs?

Una de las **asimetrías más limpias** entre la atención humana y la atención en transformers es justamente la **disociación endógeno/exógeno**:

- En humanos hay **dos sistemas neurales disociables** (dorsal vs. ventral), con timing distinto, vulnerabilidades clínicas distintas, y dinámica de interacción específica.
- En transformers hay **un solo mecanismo** de atención (query-key-value + softmax) que no distingue arquitecturalmente entre "atención dirigida por objetivos" y "captura por salience". Toda la atención emerge del mismo cálculo.

Algunos modelos recientes de visión computacional (**Anderson et al. 2018** "Bottom-Up and Top-Down Attention") intentan introducir explícitamente esa disociación, pero es la excepción, no la regla. La arquitectura transformer estándar es **monolítica** desde el punto de vista atencional — un punto importante para cualquier comparación seria entre atención humana y atención artificial.

## Conexiones en este sitio

- [Bottom-up vs. top-down](../neurobiologia/bottom-up-top-down.md) — el eje conceptual del que viene la distinción endógeno/exógeno.
- [Tareas de tiempo de reacción (TR)](../metodologia/tiempo-reaccion.md) — el Posner cueing task es una tarea de TR estándar.
- [Garden paths](garden-paths.md) — en parsing, el re-análisis sintáctico involucra una forma de control endógeno.
- [Surprisal](surprisal.md) — predice efectos de captura por estímulo inesperado (exógenos en sentido amplio).

## Lecturas

### Fundacionales
- **Posner, M. I. (1980)** "Orienting of attention". *Quarterly Journal of Experimental Psychology* 32:3-25. El paradigma cueing y la distinción endógeno/exógeno.
- **Posner, M. I. & Petersen, S. E. (1990)** "The attention system of the human brain". *Annual Review of Neuroscience* 13:25-42. Las tres redes (alerting/orienting/executive).
- **De Vega, M. (1984)** *Introducción a la psicología cognitiva*. Alianza. Cap. de atención — el contexto del libro donde aparece la distinción operacionalizada.

### Neurociencia cognitiva
- **Corbetta, M. & Shulman, G. L. (2002)** "Control of goal-directed and stimulus-driven attention in the brain". *Nature Reviews Neuroscience* 3:201-215. **El modelo dorsal/ventral.**
- **Petersen, S. E. & Posner, M. I. (2012)** "The attention system of the human brain: 20 years after". *Annual Review of Neuroscience* 35:73-89. Actualización del modelo de tres redes.
- **Corbetta, M., Patel, G. & Shulman, G. L. (2008)** "The reorienting system of the human brain: From environment to theory of mind". *Neuron* 58:306-324. Profundización del rol de la red ventral.

### Conexión con atención artificial
- **Anderson, P. et al. (2018)** "Bottom-Up and Top-Down Attention for Image Captioning and Visual Question Answering". *CVPR*. Uno de los pocos modelos que introduce la disociación explícitamente en arquitectura artificial.
- **Lindsay, G. W. (2020)** "Attention in Psychology, Neuroscience, and Machine Learning". *Frontiers in Computational Neuroscience* 14:29. Revisión canónica del paralelo entre atención psicológica, neural y artificial.
