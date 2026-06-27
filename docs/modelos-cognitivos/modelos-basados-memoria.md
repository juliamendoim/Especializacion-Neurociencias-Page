# Modelos de procesamiento basados en memoria

La otra alternativa moderna al modelo generativo clásico: en vez de plantear que el procesamiento del lenguaje es **construcción de estructura sintáctica desde cero**, esta familia de modelos sostiene que es **una operación de recuperación desde una memoria de trabajo direccionable por contenido**. El parser no construye desde cero; **rastrilla y reune**. Es la contraparte de los [modelos predictivos](modelos-predictivos.md) — donde aquellos enfatizan anticipación top-down, estos enfatizan retrieval retrospectivo.

## Qué tiene de "moderno" frente al modelo generativo clásico

El modelo clásico (Frazier, Forster) plantea:

- Un **parser dedicado** que construye estructura sintáctica usando heurísticas (minimal attachment, late closure).
- **Encapsulamiento modular**: el parser opera sin recurrir a la memoria de trabajo general.
- **Costo de procesamiento = complejidad estructural** (profundidad de árbol, distancia de dependencia).
- **Errores = violaciones gramaticales** detectadas por el parser.

Los modelos basados en memoria desplazan estas tesis:

- **No hay un parser dedicado** — la comprensión es operaciones sobre WM general.
- **Costo de procesamiento = costo de retrieval** (interferencia, decaimiento de activación).
- **Errores = fallos de recuperación** (recupero el antecedente equivocado, "atraído" por similitud).
- **Las predicciones experimentales se calculan con principios de memoria**, no con principios estructurales abstractos.

Es un cambio de teoría central: pasamos de "sintaxis como cómputo especializado" a "sintaxis como caso de memoria".

## El modelo de Lewis & Vasishth (2005)

El modelo computacional más influyente de esta familia. Es una implementación dentro de **ACT-R** (la arquitectura cognitiva de John Anderson) aplicada a parsing.

**Principio central**: cada palabra que entra debe **integrarse con elementos previos**. Esa integración es una operación de recuperación desde memoria: el parser busca en WM el ítem que satisface los requerimientos (sujeto del verbo, antecedente del pronombre, etc.) usando **claves de retrieval**.

**Cómo funciona**:

1. Cada elemento parseado se almacena en memoria como un *chunk* con rasgos (categoría, número, género, animacidad, etc.).
2. Cuando aparece una palabra que demanda integración (un verbo, un pronombre), se generan **claves de retrieval** específicas. Por ejemplo, para un verbo: *busca un sujeto que sea +N, +3pers, +sg*.
3. El sistema activa los chunks que matchean las claves, ponderados por activación residual.
4. Se recupera el chunk con mayor activación.

**El costo de procesamiento** tiene dos fuentes:

- **Decaimiento**: la activación de chunks disminuye con el tiempo desde su último uso.
- **Interferencia basada en similitud (similarity-based interference)**: si hay múltiples chunks que matchean parcialmente las claves, compiten entre sí, bajando la activación del target correcto.

## Lo que predice — y por qué es distinto del modelo generativo

### Cláusulas relativas con interferencia

Comparar dos versiones de una oración con cláusula relativa de objeto:

- *"The senator who the **lawyer** attacked admitted the error"* — un solo distractor humano (lawyer).
- *"The senator who the **lawyer** that the **journalist** interviewed attacked admitted the error"* — múltiples distractores humanos similares al sujeto.

El modelo generativo clásico predice **dificultad por profundidad de embedding**. Lewis & Vasishth predicen dificultad por **interferencia entre chunks similares** — los tres sustantivos humanos compiten por las claves del verbo. Empíricamente, el patrón observado en eye-tracking favorece la predicción de Lewis & Vasishth: la dificultad escala con el número de distractores similares, no solo con la profundidad estructural.

### Agreement attraction (atracción de concordancia)

*"The key to the cabinets **are** rusty"* — error de concordancia que los humanos cometen sistemáticamente. El verbo *are* concuerda con *cabinets* (plural cercano) en vez de con *key* (singular, sujeto real).

El modelo generativo clásico no tiene un mecanismo natural para este efecto. Lewis & Vasishth lo predicen directamente: la clave de retrieval para sujeto (*+N, +sg*) matchea parcialmente a *cabinets* (*+N*), y por similitud parcial puede ganar la competición sobre *key* si la activación residual de *key* está baja.

**Wagers, Lau & Phillips (2009)** dieron evidencia experimental fuerte de que la attraction es un efecto de retrieval, no de codificación inicial.

Ver la entrada dedicada [Agreement attraction y la lectura distributiva](agreement-attraction-distributividad.md) para el tratamiento extendido del fenómeno, el rol de la distributividad/número nocional, el modelo *marking and morphing*, y la comparación con modelos lexicalistas y con LLMs.

## McElree y la atención focal

**McElree (2000, 2006)** propone una versión más extrema: la comprensión opera sobre una **memoria direccionable por contenido**, donde el retrieval es esencialmente **plano en el tiempo**. No hay decaimiento gradual — solo hay una distinción entre lo que está **en foco** (un solo ítem, capacidad ~1) y lo que está **fuera de foco** (todo lo demás).

Datos clave: tareas *speed-accuracy tradeoff* (SAT) muestran que el tiempo de retrieval **no aumenta con la distancia** al referente cuando se controla por interferencia. Eso es incompatible con la idea de búsqueda serial; favorece retrieval por contenido (content-addressable memory).

## Las dos familias internas

Dentro del paradigma memory-based hay dos posiciones que tensionan el campo:

| | **Capacidad activa limitada** | **Memoria por contenido** |
|---|---|---|
| Cuello de botella | Cuántos ítems se mantienen activos | Cuán similares son los distractores |
| Costo escala con | Distancia + carga total | Interferencia |
| Modelo prototípico | Caplan & Waters (1999) | Lewis & Vasishth (2005), McElree |

La evidencia empírica de las últimas dos décadas favorece bastante a la posición de retrieval por contenido (interferencia como cuello de botella central), aunque siguen apareciendo escenarios donde la capacidad activa también juega un papel.

## Diferencia con los modelos predictivos

Importante no confundir las dos alternativas modernas al modelo clásico:

| | **Modelos predictivos** | **Modelos basados en memoria** |
|---|---|---|
| Operación central | Anticipación top-down | Recuperación desde WM |
| Costo de procesamiento | Magnitud del error de predicción (surprisal) | Interferencia + decaimiento en retrieval |
| Dirección temporal | Pre-input (anticipación) | Post-input (integración) |
| Datos centrales | Anticipatorios (N400, eye-tracking visual world) | Retrospectivos (interferencia en cláusulas relativas, attraction) |
| Modelo formal | Modelos bayesianos / surprisal | ACT-R / Lewis & Vasishth |

Las dos familias **no son incompatibles** — varios trabajos contemporáneos las combinan (Hofmeister & Vasishth 2013; Vasishth, Nicenboim et al. 2019). La predicción genera expectativas, el retrieval las completa cuando llega el input.

## Conexión con TDL

Los modelos basados en memoria ofrecen una **explicación procesual** de por qué los chicos con TDL fallan en sintaxis compleja sin tener déficits estructurales abstractos: si su WM es más débil (memoria fonológica deficiente, mayor interferencia), entonces la dificultad en relativas de objeto, concordancia a distancia y comprensión de oraciones largas se sigue como **consecuencia del cuello de botella en retrieval**, no de un déficit gramatical específico.

Esto se conecta con la **hipótesis del déficit de procesamiento** (Ullman & Pierpont 2005; Joanisse & Seidenberg 1998) y compite con la **hipótesis modular** (van der Lely, Wexler). Ver entrada [markers psicolingüísticos del TDL](../tdl/markers-psicolinguisticos.md).

## Conexión con LLMs

Hay un paralelo intrigante: la operación de **self-attention** en transformers es matemáticamente una **operación de retrieval desde una memoria direccionable por contenido**. Cada token genera un *query* que busca en la memoria de *keys* (todos los tokens previos) y recupera información ponderada de los *values*.

Esto es estructuralmente parecido a Lewis & Vasishth — un sistema de recuperación por contenido — y bastante diferente del modelo generativo clásico (que construye estructura sintáctica serial). Pero las diferencias importan:

- En transformers no hay decaimiento temporal natural. La atención puede atender a cualquier token con igual facilidad dentro de la ventana de contexto.
- No hay interferencia basada en similitud humana. No aparecen errores tipo *attraction* de forma sistemática en LLMs.
- La memoria del modelo es **ventana de contexto pasiva**, no WM activa con foco.

Aun así, los modelos basados en memoria son el marco cognitivo más cercano arquitecturalmente a la operación interna del transformer — más que el modelo generativo clásico.

## Conexiones en este sitio

- [Memoria de trabajo](memoria-trabajo.md) — la entrada general sobre WM como **capacidad cognitiva** (Baddeley, span de dígitos, bucle fonológico). Esta entrada es la **versión procesual** — cómo la WM opera durante el parsing.
- [Modelos predictivos](modelos-predictivos.md) — primera alternativa moderna al modelo generativo clásico (anticipación top-down).
- [Modelos lexicalistas / constraint satisfaction (conexionistas)](modelos-lexicalistas.md) — tercera alternativa moderna (activación en paralelo de restricciones léxicas; línea directa de los LLMs).
- [Garden paths](garden-paths.md) — reinterpretados como fallos de retrieval bajo interferencia, no como fallos del parser dedicado.
- [Activación](activacion.md) — el sustrato común a ACT-R y otros modelos basados en memoria.
- [Markers psicolingüísticos del TDL](../tdl/markers-psicolinguisticos.md) — la repetición de no-palabras como marker fonológico de WM débil.

## Referencias clave

- **Lewis, R. L. & Vasishth, S. (2005)** "An activation-based model of sentence processing as skilled memory retrieval" *Cognitive Science* 29:375-419. **El paper central** del paradigma.
- **Lewis, R. L., Vasishth, S. & Van Dyke, J. A. (2006)** "Computational principles of working memory in sentence comprehension" *Trends in Cognitive Sciences* 10(10):447-454. Revisión accesible.
- **McElree, B. (2000)** "Sentence comprehension is mediated by content-addressable memory structures" *Journal of Psycholinguistic Research* 29:111-123.
- **McElree, B. (2006)** "Accessing recent events" *Psychology of Learning and Motivation* 46:155-200.
- **Wagers, M. W., Lau, E. F. & Phillips, C. (2009)** "Agreement attraction in comprehension: Representations and processes" *Journal of Memory and Language* 61:206-237.
- **Van Dyke, J. A. & McElree, B. (2006)** "Retrieval interference in sentence comprehension" *Journal of Memory and Language* 55:157-166.
- **Vasishth, S., Nicenboim, B., Engelmann, F. & Burchert, F. (2019)** "Computational models of retrieval processes in sentence processing" *Trends in Cognitive Sciences* 23(11):968-982. **Revisión moderna.**
- **Hofmeister, P. & Vasishth, S. (2013)** "Distinguishing distance-based and similarity-based interference effects" *Frontiers in Psychology* 4:799.
- **Anderson, J. R. et al. (2004)** "An integrated theory of the mind" *Psychological Review* 111:1036-1060. **El marco ACT-R** subyacente.
- **Caplan, D. & Waters, G. S. (1999)** "Verbal working memory and sentence comprehension" *Behavioral and Brain Sciences* 22(1):77-94. La versión "capacidad activa" alternativa.
