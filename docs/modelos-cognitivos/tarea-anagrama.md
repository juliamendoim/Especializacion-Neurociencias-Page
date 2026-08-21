# Tarea de anagrama

La **tarea de anagrama** es una tarea psicolingüística clásica donde se presentan **letras desordenadas** (típicamente 4-7) y el participante tiene que **reordenarlas para formar una palabra real** de la lengua. Es una herramienta versátil que se usa en investigación cognitiva sobre resolución de problemas y acceso léxico, en neuropsicología para disociar componentes del sistema de lectura y escritura, en evaluación cognitiva del envejecimiento y de las demencias, y en terapia de afasia y disgrafia.

## Estructura de la tarea

- **Input**: conjunto de letras presentadas como estímulo visual (o auditivo, aunque menos común).
- **Output**: la palabra correcta formada por reordenamiento de esas mismas letras.
- **Restricciones habituales**: usar todas las letras; la palabra resultante debe existir en el diccionario mental del participante.

Ejemplos en español:

- *SOMAR* → **RAMOS** o **AMORS** (nombre) o **MORAS**
- *EMSA* → **MESA** (única palabra estándar)
- *NOMAR* → **NORMA** o **RAMÓN**
- *TORAC* → **CORTA**, **RATOC** (no), **TARCO** (no) — **CORTA** es la solución típica
- *TALIRE* → **ALERTI** (no), **LITERA**, **RETALI** (no)

En diseños experimentales controlados se elige cuidadosamente:
- **Longitud** (más letras = más difícil, más permutaciones)
- **Frecuencia** de la palabra target
- **Número de soluciones posibles** (idealmente única para no ambigüedad)
- **Similitud ortográfica entre input y solución** (más "diferentes" = más difícil)

## Qué operaciones cognitivas requiere

Resolver un anagrama demanda varios procesos en paralelo:

1. **Codificación visual** de las letras y sus identidades.
2. **Mantenimiento en memoria de trabajo** de todas las letras mientras se prueban permutaciones (bucle fonológico + agenda visuoespacial, en términos de [Baddeley](memoria-trabajo.md)).
3. **Generación de permutaciones candidatas** — combinaciones a probar.
4. **Búsqueda en el léxico** — comparar cada candidato con las representaciones ortográficas almacenadas.
5. **Reconocimiento** cuando una permutación matchea una entrada léxica existente.

Estas operaciones son "cascada" — no puramente seriales, no puramente paralelas.

## Aplicaciones en cognición general

### 1. Estudios de insight vs. no-insight

**Metcalfe & Wiebe (1987)** "Intuition in insight and noninsight problem solving" (*Memory & Cognition* 15:238-246) usaron anagramas como caso prototípico de **problema sin insight**. Su metodología clave: pedirle al participante que reporte cada 10 segundos qué tan cerca cree estar de la solución (*warmth judgments*).

**Resultado**: en anagramas, los participantes muestran un **incremento gradual** en warmth mientras se acercan a la solución. En cambio, en problemas de insight ("problemas de intuición") los participantes reportan estar "fríos" hasta que de golpe encuentran la solución.

Esto convirtió a los anagramas en un **paradigma canónico** para estudiar procesos de resolución de problemas incrementales vs. de repente. Anagramas = **búsqueda serial informada por retroalimentación léxica**, no reestructuración conceptual súbita.

### 2. Efectos de frecuencia y otras variables léxicas

Los tiempos de resolución de anagramas son sensibles a las mismas variables que gobiernan el acceso léxico:

- **Frecuencia** de la palabra target → anagramas de palabras frecuentes se resuelven **mucho más rápido**.
- **Imaginabilidad** → palabras concretas más fáciles que abstractas.
- **Edad de adquisición** → palabras aprendidas temprano son más accesibles.
- **Longitud** → más letras = más difícil, pero no linealmente (interacción con frecuencia).
- **Similitud entre estímulo y solución** — cuanto más "revueltas" están las letras respecto a la palabra correcta, más difícil (Mayzner & Tresselt 1958; Novick & Sherman 2003).

Esto conecta con las cuatro mecánicas de la [frecuencia](frecuencia.md) — resolver anagramas activa representaciones léxicas cuya facilidad de acceso depende de historial de uso.

### 3. Investigación de acceso léxico

La tarea de anagrama es útil porque **evita** algunos confounds de otras tareas léxicas:
- No requiere pronunciación (a diferencia de lectura en voz alta).
- No es de decisión sí/no (a diferencia de decisión léxica).
- Requiere producción genuina de la palabra, pero desde estímulo visual (letras revueltas).

Modelos de acceso léxico predicen que anagramas de palabras vecinas ortográficamente son especialmente difíciles (ambigüedad de solución), mientras que anagramas con solución ortográfica única son más rápidos.

## Aplicaciones en neuropsicología cognitiva de la afasia y la disgrafia

**Éste es el uso central en el contexto del seminario de afasia.**

### Disociar ruta ortográfica y ruta fonológica

En el marco del [modelo dual-ruta](dual-ruta-lectura.md), un paciente puede tener preservada una ruta y afectada la otra. La tarea de anagrama permite testear esto:

- Paciente que **falla en escritura al dictado** (fonología → ortografía) pero **resuelve anagramas correctamente** → tiene **léxico ortográfico intacto**; el problema es la ruta de acceso fonológico-a-ortográfico.
- Paciente que **puede leer en voz alta y comprende** pero **no resuelve anagramas** → probablemente déficit específico de manipulación en WM o de acceso al léxico ortográfico como *output*.
- Paciente que **no puede resolver anagramas ni siquiera de palabras simples y frecuentes** → posible déficit central en representaciones ortográficas (disgrafia profunda).

### Terapia con anagramas en afasia

**Bruce & Howard (1987)** describieron protocolos donde se usan anagramas y otras claves ortográficas para facilitar recuperación en pacientes con anomia. La lógica: cuando el paciente "no puede sacar la palabra", presentar las letras activa la representación ortográfica y desde ahí se recupera la fonología. Es más efectivo que dar la primera letra sola o la definición.

En **afasia crónica con anomia persistente**, los anagramas son una de las estrategias del arsenal terapéutico. Se combinan con:
- Claves fonológicas (primer sonido)
- Claves semánticas (definición)
- Claves visuales (dibujo)

### Diagnóstico diferencial de disgrafias

Distintos tipos de disgrafia se comportan distinto en anagramas:

| Tipo de disgrafia | Rendimiento en anagramas |
|---|---|
| **Disgrafia fonológica** (afectada la ruta indirecta) | Bien, si palabra tiene representación léxica |
| **Disgrafia superficial** (afectada la ruta directa) | Mal para palabras irregulares; mejor con las regulares (puede reconstruir por fonología) |
| **Disgrafia profunda** (afectadas ambas rutas + errores semánticos) | Muy mal, con errores semánticos ocasionales |
| **Disgrafia por afectación del buffer grafémico** | Mal para palabras largas independiente de frecuencia |

La combinación de tareas de anagrama con escritura al dictado, denominación escrita y lectura permite caracterizar el perfil específico.

## Aplicaciones en evaluación cognitiva

- **Envejecimiento normal**: el rendimiento en anagramas decae con la edad (Bowles & Poon 1988), correlacionado con enlentecimiento cognitivo general.
- **Alzheimer y otras demencias**: severamente afectados por deterioro semántico y de WM. Se usa como parte de baterías cognitivas.
- **Población infantil**: correlaciona con vocabulario, comprensión lectora y desarrollo léxico. Se usa en investigación educativa.

## Conexión con LLMs — una asimetría reveladora

Esta parte es interesante para tu TP de homonimias IA / cognición humana.

**Los LLMs son notoriamente malos con anagramas**. Ejemplo viral: si le pedís a un LLM que cuente cuántas "r" hay en la palabra *"strawberry"* o que reordene las letras de una palabra, con frecuencia falla o dice cosas absurdas.

**La razón**: los LLMs no ven letras individuales — ven **tokens**. La tokenización BPE (Byte-Pair Encoding) que usan modelos como GPT y Claude convierte *"strawberry"* en algo así como `[straw][berry]` o `[str][aw][berry]` — dos o tres tokens, no ocho letras. La palabra *"MESA"* es un token único, no *M-E-S-A*.

Esto tiene consecuencias importantes:
- Los LLMs **no pueden operar naturalmente al nivel de letra**.
- Tareas triviales para humanos (contar letras, hacer anagramas, deletrear) son sorprendentemente difíciles para LLMs.
- Con **chain-of-thought** y prompting explícito, los LLMs pueden hacer estas tareas mejor — pero de manera indirecta, "razonando" sobre las letras que asumen que la palabra tiene.

**Por qué es interesante para tu TP**:

- Es una **homonimia engañosa** poderosa. "Procesar palabras" en un humano incluye trivialmente acceso a letras. "Procesar palabras" en un LLM opera sobre unidades distintas (tokens) que no coinciden con letras.
- Los humanos que aprenden a leer aprenden **explícitamente** que las palabras están compuestas de letras — hay una intuición desarrollada de la unidad. Los LLMs no tienen esa intuición porque su arquitectura no lo requiere.
- Esta asimetría revela que **capacidades funcionalmente similares** (uso de lenguaje escrito) pueden operar sobre **representaciones internas radicalmente distintas**.
- Es un buen argumento contra la lectura ingenua de que "los LLMs procesan el lenguaje como los humanos".

## Conexiones en este sitio

- [Dual-ruta de lectura](dual-ruta-lectura.md) — el marco teórico para entender qué componente evalúan los anagramas.
- [Memoria de trabajo](memoria-trabajo.md) — la tarea depende del bucle fonológico y del ejecutivo central.
- [Frecuencia](frecuencia.md) — los efectos clásicos de frecuencia se replican en anagramas.
- [Modelos lexicalistas](modelos-lexicalistas.md) — el marco moderno donde el léxico es central.
- [Áreas de Broca y Wernicke](../afasia/areas-broca-wernicke.md) — las afasias donde la tarea es diagnósticamente útil.
- [Evaluación de comprensión: Boston y AAT](../afasia/comprension-boston-aat.md) — cómo se ubica la tarea de anagrama respecto a las baterías estandarizadas.
- [Perseveración](../afasia/perseveracion.md) — las perseveraciones también aparecen en tareas de anagrama seriadas.

## Referencias clave

- **Metcalfe, J. & Wiebe, D. (1987)** "Intuition in insight and noninsight problem solving" *Memory & Cognition* 15:238-246. **El paradigma clásico** de warmth judgments con anagramas.
- **Mayzner, M. S. & Tresselt, M. E. (1958)** "Anagram solution times: A function of letter order and word frequency" *Journal of Experimental Psychology* 56:376-379. Efectos clásicos de orden y frecuencia.
- **Novick, L. R. & Sherman, S. J. (2003)** "On the nature of insight solutions: Evidence from skill differences in anagram solution" *Quarterly Journal of Experimental Psychology* 56A:351-382. Análisis moderno.
- **Bowles, N. L. & Poon, L. W. (1988)** "Age and context effects in lexical decision: An age-related slowing of retrieval" *Experimental Aging Research* 14:201-205. Envejecimiento y acceso léxico.
- **Bruce, C. & Howard, D. (1987)** "Computer-generated phonemic cues: An effective aid for naming in aphasia" *British Journal of Disorders of Communication* 22:191-201. Uso terapéutico en afasia.
- **Coltheart, M., Rastle, K., Perry, C., Langdon, R. & Ziegler, J. (2001)** "DRC: A dual route cascaded model of visual word recognition and reading aloud" *Psychological Review* 108:204-256. El modelo dual-ruta que fundamenta el análisis clínico.
- **Ellis, A. W. & Young, A. W. (1988/1996)** *Human Cognitive Neuropsychology*. Hove: Lawrence Erlbaum. Marco general para interpretar disociaciones en tareas de anagrama y otras tareas de lectura/escritura.
