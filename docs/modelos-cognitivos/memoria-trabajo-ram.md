# RAM ≠ memoria de trabajo: hasta dónde llega la analogía

La memoria RAM de la computadora es una de las analogías más usadas para explicar qué es la memoria de trabajo. **Funciona a un nivel y se rompe en los demás.** Esta entrada mapea con honestidad dónde sirve, dónde miente, y por qué la diferencia más interesante — los **chunks** — disuelve directamente la idea de "capacidad" tomada de la informática.

## Donde la analogía funciona

A nivel **funcional abstracto** — el nivel computacional de Marr ("¿qué problema resuelve el sistema?") — RAM y memoria de trabajo (MT) hacen lo mismo:

- **Almacén temporario** activo durante el procesamiento.
- **Capacidad limitada** (RAM en GB; MT en ~4 chunks según Cowan, 7±2 según Miller).
- **Acceso rápido** comparado con un "disco" (memoria a largo plazo).
- **Decae si se pierde la "alimentación"** (corte de luz / pérdida de atención).
- **Workspace** para la computación en curso — ni RAM ni MT son donde "vive" la información a la larga.

Hasta acá la analogía es útil. Y se queda corta acá.

## Donde la analogía se rompe

### 1. Direccionamiento

- **RAM**: direccionable por **dirección** ("dame el byte en 0x4F2A" → te lo da). Bit-exacto.
- **MT**: direccionable por **contenido / clave** ("algo que empezaba con M y era de la facu" → te trae aproximaciones).

No hay "dirección" de un recuerdo. Es el mismo contraste que aparece en [recuperación de memoria](recuperacion-memoria.md) — pattern completion en vez de random access.

### 2. Fidelidad

- **RAM**: read/write perfecto (asumiendo hardware OK).
- **MT**: lossy. Items decaen, se distorsionan, interfieren. El efecto de similitud fonológica (recordar B-C-V-G es más difícil que B-K-R-M) no tiene equivalente en RAM.

### 3. Capacidad — y por qué la diferencia más interesante es plástica

(Esta es la sección de chunks, que extiendo abajo en detalle.)

- **RAM**: capacidad en bytes, **discreta y definida por el hardware**.
- **MT**: capacidad en **chunks**, y el chunk es **plástico**. Depende de qué tenés en memoria a largo plazo.

### 4. Substrato

- **RAM**: módulo físico **separado** (chip distinto del CPU, conectado por bus).
- **MT**: **no es una región** del cerebro. Emerge de **actividad persistente** en córtex prefrontal y áreas asociadas, en **las mismas neuronas** que hacen otro procesamiento. No hay "stick de MT".

Hay un consenso creciente (Cowan, D'Esposito) de que **MT es la porción activada de la memoria a largo plazo** — el foco atencional sobre representaciones que ya viven en LP. RAM no es "la porción activada del disco".

### 5. Decaimiento e interferencia

- **RAM**: decae sólo con pérdida de power. Una posición no afecta a otra.
- **MT**: decae **pasivamente** en ~15-30 seg (paradigma Brown-Peterson) Y por **interferencia** entre items similares.

### 6. Multi-componente

- **RAM**: homogénea. No le importa si guardás texto, imágenes o números.
- **MT** (Baddeley): bucle fonológico, sketchpad visuoespacial, buffer episódico, ejecutivo central. Mantener verbal + espacial al mismo tiempo es **más fácil** que verbal + verbal — los subsistemas no compiten entre sí.

### 7. Almacenamiento ≠ manipulación

- **RAM**: **sólo almacena**. La CPU manipula y vuelve a escribir.
- **MT**: el "working" es justamente la **manipulación**. Mantener "342 + 178" en mente mientras lo sumás no es "leer de RAM → computar en CPU → escribir a RAM": es la misma operación neural haciendo las dos cosas a la vez. **El cerebro no es Von Neumann**: no hay separación arquitectónica entre storage y processing.

### 8. Mantenimiento activo

- **RAM**: no requiere "atención" para conservar contenido. Está ahí.
- **MT**: requiere **rehearsal o atención activa**. Sin eso decae. Por eso la MT está tan acoplada al control atencional.

### 9. Interacción con la memoria a largo plazo

- **RAM**: lo que pasa por RAM no modifica el disco.
- **MT**: lo que se mantiene en MT tiene **más chance de consolidarse** en LP. Relación bidireccional, no buffer pasivo.

## Chunks — la diferencia más interesante (y la que la analogía oculta)

Esta es la parte que más complica el paralelo, y la que más vale la pena entender.

### Qué es un chunk

Un **chunk** es **una unidad significativa de información tratada como una sola pieza por la MT**, independientemente de cuántos elementos "básicos" la compongan.

Ejemplo clásico: tratá de retener esta secuencia de letras:

> FBI – CIA – KGB – NSA – MIT

Son 15 letras (15 unidades a nivel bit) pero retenerlas es trivial porque las agrupás en **5 chunks** (5 siglas conocidas). Si las letras fueran al azar — `QXRPL – ZVMTC – BWGRD` — serían también 15 letras pero **15 chunks**, e inalcanzables sin estrategia.

**Lo que define un chunk no es el material, sino lo que ya sabés**.

### Miller (1956) — el origen

George A. Miller, en *"The Magical Number Seven, Plus or Minus Two"* (Psychological Review), propuso que la MT mantiene **7 ± 2 chunks**. Era una observación empírica robusta a través de tareas (dígitos, palabras, posiciones), y fue el paper fundacional del estudio cognitivo de la MT.

Lo importante del paper no es el número sino la idea: **la capacidad es en chunks, no en bits**. Miller ya notaba que "expandimos artificialmente nuestra capacidad" al recodificar la información en unidades más significativas.

### Chase & Simon (1973) — la prueba con ajedrez

Estudio canónico. Tomaron **maestros de ajedrez** y **jugadores principiantes**, les mostraron una posición de tablero por 5 segundos, y luego les pidieron reconstruirla. Dos condiciones:

| Condición | Principiante | Maestro |
|---|---|---|
| **Posición de una partida real** | Recuerda ~4-5 piezas | Recuerda ~25 piezas |
| **Posición aleatoria** (piezas tiradas al azar) | Recuerda ~4-5 piezas | **Recuerda ~4-5 piezas** |

La conclusión: el maestro **no tiene mejor MT** que el principiante. Tiene una **memoria a largo plazo enorme de patrones de juego** que le permite **chunkear** la posición en pocas unidades ("ataque indio de rey + estructura de peones tipo erizo + alfiles desarrollados"). En la posición aleatoria no puede chunkear → vuelve a la capacidad base.

Es la demostración más limpia de que **la "capacidad" depende del conocimiento previo**.

### Cowan (2001) — la corrección del número de Miller

Nelson Cowan, en *"The magical number 4 in short-term memory: a reconsideration of mental storage capacity"* (Behavioral and Brain Sciences), revisó cuidadosamente los experimentos posteriores a Miller y argumentó que la **verdadera capacidad del foco atencional es ~4 chunks**, no 7.

¿Por qué Miller veía 7? Porque sus tareas permitían **rehearsal** (repaso subvocálico) que infla artificialmente el conteo. Cuando se bloquea el rehearsal (con tareas de supresión articulatoria), la capacidad cae a **4 ± 1**.

Hoy el consenso es **4 chunks como capacidad pura de foco atencional**, expandible con rehearsal y estrategias.

### Ericsson & Kintsch (1995) — long-term working memory

Anders Ericsson y Walter Kintsch propusieron que **expertos en un dominio usan la memoria a largo plazo como extensión virtual de la MT**. Los chunks complejos del experto no están "en MT" en el sentido tradicional — están en LP, pero las **claves de recuperación** están en MT, y los chunks se traen tan rápido que funcionalmente actúan como MT extendida.

Esto es lo que les permite a memoristas, ajedrecistas, médicos, traductores y otros expertos manejar volúmenes de información que romperían cualquier modelo de MT clásica.

**Implicación clave**: la MT efectiva en un dominio depende casi totalmente de cuánto LP estructurado tenés en ese dominio. Esto desarma definitivamente la analogía con RAM, donde el espacio está fijado por el hardware.

### Chunks y lenguaje

Aplicaciones específicas del chunking al procesamiento del lenguaje:

- **Lectura**: los lectores expertos chunkean palabras en sintagmas; los principiantes chunkean letras en palabras. Por eso el span lector (Daneman & Carpenter, 1980) crece con la habilidad lectora.
- **Procesamiento sintáctico**: los **garden paths** ([entrada aparte](garden-paths.md)) son fallos de chunking — el parser cierra un chunk en un punto y tiene que reabrirlo. La dependency locality theory de Gibson (DLT, 2000) modela la dificultad de oraciones como costo de mantener referentes abiertos en MT.
- **Adquisición**: los niños van armando chunks lingüísticos progresivamente (fonemas → sílabas → palabras → frases hechas → patrones sintácticos abstractos). Tomasello (2003) construyó toda una teoría de adquisición del lenguaje sobre esto.
- **TDL y dislexia**: niños con TDL muestran **chunks fonológicos más débiles** (Gathercole et al.). La repetición de pseudopalabras los expone porque no hay LP para chunkear.
- **LLMs**: los modelos de lenguaje también "chunkean" — pero con tokens (BPE, byte-pair encoding). La compresión es estructuralmente análoga a la chunking humana en lectura, aunque la implementación es muy distinta. Conecta con [surprisal](surprisal.md).

### Por qué importa para la analogía RAM

Decir "tenés 4-7 espacios de MT" como si fueran slots de RAM **es engañoso**. La capacidad efectiva en cualquier dominio es:

> capacidad efectiva = N_chunks × tamaño_promedio_de_chunk

El primer factor (N_chunks) es relativamente constante por individuo. El segundo (tamaño del chunk) es **infinitamente expansible** con experticia. Lo que parece "memoria limitada" desde el lado de la informática es en realidad **memoria estructurada por aprendizaje** desde el lado de la cognición.

## Una analogía mejor (pero también imperfecta)

Más fiel sería comparar la MT con **registros de CPU + caché L1**, no con RAM:

- Capacidad mucho más chica.
- Acoplada físicamente al procesador (no es un módulo aparte).
- Acceso rapidísimo.
- Contenido desaparece rápido cuando deja de usarse.

Pero también se rompe — los registros se direccionan por nombre, y el caché reemplaza con LRU sin equivalente cognitivo claro.

## La lectura desde Marr

Es el mismo patrón que aparece en muchas comparaciones cerebro-máquina:

| Nivel de Marr | ¿RAM ≈ MT? |
|---|---|
| **Computacional** (qué problema resuelve) | ✅ Sirve. Ambos resuelven "mantener info brevemente durante el procesamiento". |
| **Algorítmico** (con qué procedimiento) | ❌ Direccionamiento, capacidad y interferencia distintos. |
| **Implementacional** (en qué hardware) | ❌ Chip separado vs. actividad persistente en córtex; Von Neumann vs. no-Von Neumann. |

**Regla general**: las analogías cerebro-computadora suelen funcionar en el nivel 1 y romperse en los niveles 2 y 3. Útil saberlo para no llevar la analogía a conclusiones que no sostiene — por ejemplo "podemos hacer upgrade de MT como agregamos RAM" (falso) o "la MT tiene una capacidad fija como la RAM" (falso, depende del LP).

## Conexión con el resto del sitio

- **[Memoria de trabajo y corto plazo](memoria-trabajo.md)** — el modelo de Baddeley en detalle.
- **[Recuperación de memoria](recuperacion-memoria.md)** — direccionamiento por contenido en vez de por dirección, pattern completion.
- **[Marr — modelo computacional](../neurobiologia/marr-vision-computacional.md)** — los tres niveles que ordenan dónde funciona y dónde no la analogía.
- **[Garden paths](garden-paths.md)** — los chunks lingüísticos en acción (y fallando).
- **[Surprisal](surprisal.md)** — la conexión con chunking en modelos de lenguaje.

## Lecturas

### Para entrar al tema de chunks — los tres papers que te bastan

1. **Miller, G. A. (1956)** "The magical number seven, plus or minus two: some limits on our capacity for processing information". *Psychological Review* 63:81-97. — **El paper fundacional.** Corto, escrito con humor, todavía vigente.
2. **Chase, W. G. & Simon, H. A. (1973)** "Perception in chess". *Cognitive Psychology* 4:55-81. — **La demostración empírica más limpia.** El estudio del ajedrez con la condición de tableros aleatorios.
3. **Cowan, N. (2001)** "The magical number 4 in short-term memory: a reconsideration of mental storage capacity". *Behavioral and Brain Sciences* 24:87-185. — **La revisión moderna** que recalibra el número de Miller. Largo pero el target article son ~30 páginas y vale la pena.

### Para extender

- **Ericsson, K. A. & Kintsch, W. (1995)** "Long-term working memory". *Psychological Review* 102:211-245. — el marco que explica cómo los expertos rompen los límites aparentes.
- **Gobet, F. & Simon, H. A. (1996)** "Templates in chess memory: a mechanism for recalling several boards". *Cognitive Psychology* 31:1-40. — extensión de Chase & Simon con el concepto de "template" (chunk de chunks).
- **Gobet, F. et al. (2001)** "Chunking mechanisms in human learning". *Trends in Cognitive Sciences* 5:236-243. — revisión accesible.

### Sobre MT y substrato neural

- **Cowan, N. (2008)** "What are the differences between long-term, short-term, and working memory?" *Progress in Brain Research* 169:323-338. — modelo embedded-processes.
- **D'Esposito, M. & Postle, B. R. (2015)** "The cognitive neuroscience of working memory". *Annual Review of Psychology* 66:115-142. — revisión del substrato neural; deja claro que no hay "región de MT".
- **Baddeley, A. (2003)** "Working memory: looking back and looking forward". *Nature Reviews Neuroscience* 4:829-839. — el modelo multi-componente del autor.

### Conexión con lenguaje específicamente

- **Daneman, M. & Carpenter, P. A. (1980)** "Individual differences in working memory and reading". *Journal of Verbal Learning and Verbal Behavior* 19:450-466. — la *reading span task* que enlaza chunks con habilidad lectora.
- **Gibson, E. (2000)** "The dependency locality theory: a distance-based theory of linguistic complexity". En *Image, Language, Brain* (Marantz et al., eds.), MIT Press. — DLT y chunks en parsing.
