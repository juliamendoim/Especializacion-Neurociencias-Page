# Modelos lexicalistas y de satisfacción de restricciones (la tradición conexionista)

La tercera gran alternativa moderna al modelo generativo clásico — junto con los [modelos predictivos](modelos-predictivos.md) y los [modelos basados en memoria](modelos-basados-memoria.md). Esta familia se conoce con varios nombres que apuntan a la misma red de compromisos teóricos:

- **Lexicalista**: la mayoría del trabajo se hace en el léxico, no en módulos sintácticos autónomos. Cada palabra trae información probabilística detallada sobre los contextos en que aparece.
- **De satisfacción de restricciones (constraint satisfaction)**: la ambigüedad se resuelve combinando en paralelo múltiples fuentes débiles de evidencia (léxica, semántica, contextual, frecuencial) — no aplicando una heurística sintáctica autónoma.
- **Conexionista**: la implementación computacional típica es vía redes neuronales con activación distribuida en paralelo (PDP — *parallel distributed processing*).

Las tres etiquetas no son sinónimas pero están **profundamente entrelazadas** — todo modelo serio de la familia es lexicalista en sus compromisos teóricos, *constraint-satisfaction* en su mecánica, y conexionista en su implementación.

## Qué deja atrás del modelo generativo clásico

El modelo dominante hasta los años 90 (Frazier, Forster, Fodor) sostenía:

- **Modularidad sintáctica**: un parser autónomo construye estructura sin acceder a información léxica detallada ni semántica ni contextual.
- **Síntesis serial**: dos etapas — primero estructura mínima por heurística, después integración con otros niveles si es necesario.
- **Léxico como catálogo pasivo**: las palabras son entradas que el parser consulta para categoría sintáctica y poco más.

Los modelos lexicalistas/conexionistas desplazan radicalmente esos compromisos:

- **No hay parser autónomo**: la sintaxis emerge de la interacción de restricciones léxicas, semánticas y contextuales.
- **Procesamiento en paralelo**: todas las alternativas se activan simultáneamente con grado variable; la más apoyada por las restricciones "gana".
- **Léxico como repositorio rico**: cada palabra carga información probabilística sobre frecuencias estructurales (por ejemplo, *send* aparece más como transitivo simple que como ditransitivo; *give* al revés). Esa información es **la materia del parsing**, no un dato secundario.

## El giro lexicalista — MacDonald, Pearlmutter & Seidenberg (1994)

El paper canónico es **MacDonald, Pearlmutter & Seidenberg (1994)** "The lexical nature of syntactic ambiguity resolution" (*Psychological Review* 101:676-703). Argumentan que la resolución de ambigüedad sintáctica **no requiere mecanismos sintácticos específicos** — basta con información léxica probabilística operando en paralelo con otras restricciones.

Ejemplo canónico: *"The horse raced past the barn fell"* (garden path clásico). El modelo de Frazier dice que el parser comete error por *minimal attachment*. MacDonald et al. responden: el problema es que *raced* tiene una frecuencia abrumadora como verbo principal en past simple y bajísima como past participle. Si en el léxico, *raced* tuviera frecuencias parejas, el garden path se debilita. La ambigüedad se resuelve con **información léxica probabilística**, no con heurísticas sintácticas abstractas.

Esto cambia el centro de gravedad teórico: el léxico **no es periferia**, es **el corazón del sistema de comprensión**.

## Constraint satisfaction — Spivey-Knowlton, Trueswell, Tanenhaus

Trueswell & Tanenhaus (1994), Spivey-Knowlton (1996) y Tanenhaus et al. (1995) implementan el paradigma vía modelos de **satisfacción de restricciones**: cada palabra activa múltiples interpretaciones posibles, ponderadas por:

- Frecuencia léxica del uso (*raced* como V principal vs. participio).
- Plausibilidad semántica (¿es coherente que un caballo corra? ¿es coherente que algo corra a un caballo?).
- Contexto previo (qué se mencionó antes).
- Información visual (en el *visual world paradigm*).

Las interpretaciones compiten por activación en paralelo. La "más apoyada por las restricciones" gana. Cuando llega información tardía que cambia el balance, hay *reanalysis* — pero no es desbaratar una estructura ya construida, es **redistribuir activación** entre alternativas que estaban presentes desde el principio.

**Tanenhaus, Spivey-Knowlton, Eberhard & Sedivy (1995)** "Integration of visual and linguistic information in spoken language comprehension" (*Science*) estableció el **visual world paradigm** y mostró que el contexto visual influye sobre el parsing **en tiempo real** — incompatible con la modularidad clásica.

## La implementación conexionista — Elman y la SRN

**Elman (1990, 1991, 1993)** propuso la **Simple Recurrent Network (SRN)** — una red neuronal recurrente entrenada para predecir la próxima palabra. Sin gramática explícita, sin reglas, la red aprende a:

- Representar categorías sintácticas como patrones de activación en la capa oculta.
- Capturar dependencias a distancia (concordancia sujeto-verbo a través de relativas).
- Generalizar a oraciones novedosas que respetan la estructura aprendida.

**Elman (1991)** "Distributed representations, simple recurrent networks, and grammatical structure" mostró que una SRN aprende, sin supervisión sintáctica explícita, la estructura de oraciones inglesas — incluyendo concordancia, subcategorización verbal, cláusulas relativas. Es el **antecedente directo** de los LLMs modernos.

Otros modelos canónicos de la tradición:

- **McClelland & Elman (1986)** TRACE: modelo conexionista de percepción del habla. Activación en paralelo, interacción top-down/bottom-up, restricciones compitiendo. Es el prototipo de cómo se modela cualquier nivel del procesamiento del lenguaje en la tradición conexionista.
- **Seidenberg & McClelland (1989)** modelo conexionista de lectura. Una sola red aprende lectura regular e irregular sin la división dual-ruta de Coltheart. Es la **alternativa conexionista** al dual-ruta clásico (ver [dual-ruta de lectura](dual-ruta-lectura.md)) y argumenta que con una sola red distribuida se puede modelar todo el espectro de la lectura sin postular dos rutas separadas.
- **Rumelhart & McClelland (1986)** modelo conexionista del past tense, que disparó el **past tense debate** (1986-2000) — la pelea histórica entre dual-route simbólica y red única conexionista.

## Casos canónicos donde la familia se diferencia del modelo clásico

| Fenómeno | Modelo clásico (Frazier) | Lexicalista / constraint satisfaction |
|---|---|---|
| Garden paths | Falla del parser por aplicar *minimal attachment* | Sesgo léxico fuerte que se viola; la interpretación correcta tenía activación inicial baja |
| Diferencias entre verbos | No predichas (la sintaxis es la misma) | Predichas exactamente — diferencias de frecuencia subcategorial |
| Influencia del contexto | Tardía (post-parsing) | Inmediata (en paralelo con info léxica) |
| Plausibilidad semántica | No afecta el primer parsing | Afecta desde la primera palabra |
| Reanalysis | Costo estructural de desbaratar y reconstruir | Redistribución de activación entre alternativas |
| Adquisición | Implícita en el modelo | Explícita: aprendizaje de distribuciones |

Trueswell, Tanenhaus & Garnsey (1994) mostraron que la **plausibilidad semántica** influye sobre la resolución de ambigüedad **en tiempo real** (con eye-tracking), lo cual es difícil de acomodar para el modelo clásico modular pero natural para *constraint satisfaction*.

## Diferencia con los otros dos modelos modernos

Las tres familias modernas comparten su rechazo al modelo generativo clásico, pero difieren en qué consideran la operación central:

| | **Predictivos** | **Basados en memoria** | **Lexicalistas / constraint-satisfaction** |
|---|---|---|---|
| Operación central | Anticipación top-down | Retrieval desde WM | Activación en paralelo de restricciones léxicas |
| Foco | Lo que viene | Lo que ya pasó (integrar) | Toda la info disponible al mismo tiempo |
| Implementación típica | Modelos bayesianos / surprisal | ACT-R / Lewis & Vasishth | Redes recurrentes / PDP |
| Léxico | Importante pero no central | Importante (chunks de retrieval) | **El corazón del sistema** |
| Modelo prototípico | Kuperberg & Jaeger, Levy | Lewis & Vasishth 2005 | MacDonald, Pearlmutter & Seidenberg 1994 |

En la práctica, **los modelos contemporáneos combinan elementos de las tres familias**. La distinción es histórica y conceptual; la investigación reciente tiende a integrar — surprisal puede leerse como instancia de constraint satisfaction, retrieval como complemento de predicción, etc.

## Conexión con LLMs — la herencia directa

Esta familia es **la línea genealógica directa de los LLMs actuales**. Los LLMs son redes neuronales (conexionistas), entrenadas en predicción de próxima palabra (línea de Elman), que aprenden información probabilística sobre cómo cada palabra se combina en contextos (lexicalismo), y resuelven ambigüedad por activación distribuida sobre múltiples fuentes simultáneas de evidencia (*constraint satisfaction*).

Los conceptos clave de los LLMs tienen antecedentes directos en esta tradición:

- **Embeddings** (representaciones vectoriales de palabras) → *distributed representations* de Elman, Hinton.
- **Self-attention** sobre representaciones distribuidas → activación interactiva del TRACE de McClelland & Elman.
- **Next-token prediction como objetivo de entrenamiento** → la SRN de Elman estaba entrenada exactamente con ese objetivo.
- **Aprendizaje sin estructura sintáctica explícita** → el resultado de Elman (1991): la sintaxis emerge sin ser pre-programada.

Esto cambia algo importante en la lectura de LLMs: **no son una "tecnología nueva" sin antecedentes psicolingüísticos**. Son la escala industrial de un programa de investigación cognitiva que arrancó en los 80s. La pelea Pinker vs. Rumelhart de 1986-2000 (past tense debate) anticipa exactamente las preguntas que se hacen hoy sobre LLMs.

## Críticas y matices

- **Pinker & Prince (1988)** y la línea dual-route critican que los modelos conexionistas sobre-generalizan, fallan en casos clave, y no explican la diferencia entre regulares e irregulares de manera principada. El *past tense debate* (1986-2000) es la versión más extensa de esta crítica.
- **Marcus (2018, 2020)** critica que las redes neuronales — y por extensión los LLMs — son débiles cuando el material es **distribucionalmente novedoso**: memorizan distribuciones, no abstraen como humanos. Compatible con la posición simbólica.
- **Yang (2002, 2016)** ofrece una posición intermedia: hay reglas pero se aprenden probabilísticamente, con un umbral de productividad (*tolerance principle*). Reconcilia "hay reglas" con "se aprenden del input".
- **Yedetore, Linzen et al. (2023)** muestran que las redes entrenadas con cantidades de input comparables al humano (~10⁷ palabras) **fallan en generalizaciones jerárquicas** que los niños hacen sin esfuerzo. Argumento moderno contra el conexionismo puro y a favor de sesgos inductivos específicos del humano.

## Conexiones en este sitio

- [Modelos predictivos](modelos-predictivos.md) — la primera alternativa moderna al modelo generativo clásico (anticipación top-down).
- [Modelos basados en memoria](modelos-basados-memoria.md) — la segunda (retrieval desde WM).
- [Dual-ruta de lectura](dual-ruta-lectura.md) — el modelo de Seidenberg & McClelland (1989) es la alternativa conexionista al dual-ruta clásico.
- [Activación](activacion.md) — el sustrato común a todos los modelos conexionistas.
- [Surprisal](surprisal.md) — la métrica que conecta esta tradición con la psicolingüística contemporánea.
- [Aprendizajes generales](../aprendizajes-generales.md) — la sección sobre autoorganización vs. big data discute el debate Elman/Pinker en clave actual.

## Referencias clave

- **MacDonald, M. C., Pearlmutter, N. J. & Seidenberg, M. S. (1994)** "The lexical nature of syntactic ambiguity resolution" *Psychological Review* 101:676-703. **Paper canónico del lexicalismo.**
- **Trueswell, J. C., Tanenhaus, M. K. & Garnsey, S. M. (1994)** "Semantic influences on parsing: Use of thematic role information in syntactic ambiguity resolution" *Journal of Memory and Language* 33:285-318.
- **Tanenhaus, M. K., Spivey-Knowlton, M. J., Eberhard, K. M. & Sedivy, J. C. (1995)** "Integration of visual and linguistic information in spoken language comprehension" *Science* 268:1632-1634. **El visual world paradigm.**
- **Spivey-Knowlton, M. J. (1996)** "Integration of visual and linguistic information: Human data and model simulations" PhD diss., University of Rochester.
- **Elman, J. L. (1990)** "Finding structure in time" *Cognitive Science* 14:179-211. **El paper fundacional de las SRN.**
- **Elman, J. L. (1991)** "Distributed representations, simple recurrent networks, and grammatical structure" *Machine Learning* 7:195-225.
- **Elman, J. L. (1993)** "Learning and development in neural networks: The importance of starting small" *Cognition* 48:71-99.
- **McClelland, J. L. & Elman, J. L. (1986)** "The TRACE model of speech perception" *Cognitive Psychology* 18:1-86.
- **Rumelhart, D. E. & McClelland, J. L. (1986)** "On learning the past tenses of English verbs" en *Parallel Distributed Processing*. MIT Press. **Inicio del past tense debate.**
- **Seidenberg, M. S. & McClelland, J. L. (1989)** "A distributed, developmental model of word recognition and naming" *Psychological Review* 96:523-568.
- **McClelland, J. L. & Rumelhart, D. E. (1986)** *Parallel Distributed Processing: Explorations in the Microstructure of Cognition* (2 vols.). MIT Press. **Los dos volúmenes fundacionales del conexionismo moderno.**
- **Pinker, S. & Prince, A. (1988)** "On language and connectionism: Analysis of a parallel distributed processing model of language acquisition" *Cognition* 28:73-193. **La crítica simbólica clásica.**
- **Marcus, G. (2018)** "Deep learning: A critical appraisal" arXiv:1801.00631.
- **Yedetore, A., Linzen, T. et al. (2023)** "How poor is the stimulus? Evaluating hierarchical generalization in neural networks trained on child-directed speech" *ACL*.
