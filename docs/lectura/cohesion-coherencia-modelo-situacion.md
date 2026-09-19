# Cohesión, coherencia y modelo de situación

Dos términos que se usan casi como sinónimos y nombran cosas de distinto tipo. La diferencia no es terminológica: define **dónde** hay que buscar el fenómeno y **con qué** se lo mide.

> **Cohesión** está en el texto. **Coherencia** está en el lector.

---

## 1. La distinción

**Cohesión**
: Las marcas lingüísticas explícitas que enlazan partes del texto: referencia pronominal, elipsis, sustitución, conectores, repetición léxica. Son propiedades **del objeto**. Se pueden contar.

**Coherencia**
: Que el texto represente una situación posible y comprensible. Es una propiedad de la **representación mental** que construye quien lee, y depende de su conocimiento del mundo.

Las dos se disocian en ambas direcciones:

| | Ejemplo |
|---|---|
| **Cohesivo pero incoherente** | *"Fueron a lo de su hermana a ver una peli. Compraron las entradas y entraron a la sala."* Los enlaces están todos bien; la situación no cierra |
| **Coherente pero poco cohesivo** | *"Se cortó la luz. Velas."* Sin conectores ni referencia explícita, y sin embargo se entiende perfectamente |

El primer caso es el interesante: **"compraron las entradas" no tiene nada raro lingüísticamente.** Lo raro es situacional — comprar entradas no forma parte del guion de visitar a alguien. La incoherencia no está en ninguna palabra ni en ningún enlace: está en la relación entre lo que el texto dice y lo que se sabe del mundo.

---

## 2. Los tres niveles de Kintsch

El marco que ordena esto es el de van Dijk y Kintsch, que distingue tres representaciones simultáneas de un mismo texto:

| Nivel | Qué contiene | Cuánto dura |
|---|---|---|
| **Superficie** | Las palabras exactas y su forma sintáctica | Se pierde rápido |
| **Texto base** | La red de proposiciones que el texto enuncia explícitamente. Acá vive la **cohesión** | Intermedio |
| **Modelo de situación** | El estado de cosas representado, integrando el texto **con el conocimiento de mundo y las inferencias**. Acá vive la **coherencia** | Es lo que perdura |

Que sean tres niveles y no uno tiene consecuencia medible: al cabo de un rato la gente **no recuerda las palabras exactas pero sí la situación**, y acepta como "lo que decía el texto" paráfrasis que nunca leyó — siempre que respeten la situación. Rechaza, en cambio, cambios que alteren el estado de cosas aunque conserven las palabras.

Esa disociación entre memoria verbatim y memoria situacional es la evidencia de que el modelo de situación existe como nivel propio.

### Las cinco dimensiones del modelo de situación

Zwaan y Radvansky proponen que un modelo de situación se rastrea a lo largo de cinco ejes, y que una ruptura en cualquiera de ellos genera un costo de procesamiento:

**causación · intencionalidad (metas) · tiempo · espacio · personas**

El ejemplo del cine viola la **intencionalidad**: comprar entradas no pertenece a la estructura de metas de "ir a casa de alguien". Es una violación de guion, en el sentido de Schank y Abelson.

---

## 3. Las inferencias son el mecanismo

El modelo de situación se construye completando lo que el texto no dice. Dos tipos conviene distinguir:

**Inferencias puente**
: Necesarias para mantener la coherencia. *"Fueron al picnic. La cerveza estaba caliente."* — el artículo definido obliga a inferir que había cerveza en el picnic. Sin esa inferencia el texto no se conecta. Se hacen en línea, casi obligatoriamente.

**Inferencias elaborativas**
: Enriquecen pero no son necesarias. *"Golpeó el clavo"* invita a inferir un martillo. Son opcionales y dependen de recursos y de objetivos de lectura.

La distinción importa porque **solo las primeras son diagnósticas de coherencia**. Un texto que exige muchas inferencias puente difíciles es costoso pero coherente; uno que exige una inferencia imposible es incoherente.

---

## 4. Que el conocimiento de mundo entre no es una metáfora

El dato que ancla todo esto: **Hagoort y colegas (2004)** compararon una violación **semántica** (*"los trenes holandeses son agrios"*) con una de **conocimiento de mundo** (*"los trenes holandeses son blancos"* — en Holanda son amarillos).

Las dos produjeron [N400](../metodologia/n400-p600-potenciales.md) de amplitud y latencia **similares**, y activaron las mismas regiones.

El cerebro no consulta primero un diccionario y después una enciclopedia: integra las dos fuentes **en paralelo y en la misma ventana temporal**. Para el estudio de la comprensión eso significa que las rupturas de coherencia basadas en conocimiento de mundo son detectables en línea con los instrumentos habituales.

---

## 5. Cómo se mide

### En línea, durante la lectura

- **Tiempos en la región crítica**: lectura autoadministrada o registro de movimientos oculares. Conviene mirar también *spillover* y, sobre todo, **regresiones**: la coherencia rota suele mandar la mirada hacia atrás, a buscar de dónde salió el problema.
- **Potenciales evocados**: N400 si el costo es de integración semántica; P600 si hay reanálisis.

### Fuera de línea, para el modelo de situación

- **Reconocimiento de paráfrasis vs. verbatim** — la prueba clásica. Si se acepta la paráfrasis correcta y se rechaza el cambio de situación, se construyó un modelo y no solo se leyeron palabras.
- **Verificación de inferencias**: preguntar por algo que el texto no dijo pero se sigue de él.
- **Recuerdo libre y su estructura**: qué se conserva y qué se reordena.

### Computacionalmente

**Coh-Metrix** (Graesser y McNamara) es la herramienta canónica, construida sobre el marco multinivel. Entrega alrededor de cien índices: solapamiento referencial entre oraciones, similitud semántica, y **conectores clasificados por tipo** — causales, aditivos, temporales, lógicos y adversativos.

Con una advertencia que sus propios autores hacen: **Coh-Metrix mide cohesión, no coherencia.** Mide lo que está en el texto, que es todo lo que un programa puede ver sin un lector.

Otras vías: **grillas de entidades**, que representan la coherencia como patrones de transición de entidades entre oraciones, y medidas de probabilidad a nivel de oración.

---

## 6. Por qué la surprisal no alcanza (todavía)

La [surprisal](../modelos-cognitivos/surprisal.md) es la improbabilidad de una palabra dado el contexto previo. Es una medida excelente de dificultad de procesamiento, pero **no es una medida de coherencia**, y confundirlas es un error frecuente.

Se separan en las dos direcciones:

- **Alta surprisal, coherente**: la cerveza del picnic. Cuesta procesarla porque exige una inferencia puente, no porque el texto falle.
- **Baja surprisal, incoherente**: se pueden encadenar frases altamente probables que no describan ninguna situación posible.

El problema de fondo es que la surprisal es **un escalar**: informa *cuánto* sorprendió, nunca *por qué*. No distingue una violación sintáctica de una semántica, de una de conocimiento de mundo, ni de una inferencia legítima pero costosa.

### La propuesta que apunta a resolverlo

Venhuizen, Crocker y Brouwer proponen una **surprisal centrada en la comprensión**: definida no sobre la probabilidad de la palabra sino sobre la del **significado que se va construyendo**, integrando experiencia lingüística y conocimiento de mundo en una sola métrica.

Su hallazgo más revelador: con un modelo de situación que lo sostenga, oraciones que **violan la animacidad** resultan **más fáciles** que las que no la violan. El modelo de situación puede **sobrescribir** la expectativa puramente lingüística — que es justamente la prueba de que son niveles distintos.

### Y el límite de los modelos actuales

Los modelos de lenguaje distinguen razonablemente bien **lo imposible** de lo posible, pero les cuesta **lo improbable-pero-posible**, y fallan cuando un conector debería revertir la plausibilidad de un escenario.

El ejemplo del cine cae justo en esa zona: comprar entradas en casa de alguien no es imposible, es **raro**. Es el tipo de incoherencia más difícil de detectar automáticamente, y probablemente el más frecuente en textos reales.

---

## Cómo se conecta con otros conceptos

- **[N400 y P600](../metodologia/n400-p600-potenciales.md)** — los instrumentos que vuelven medible la integración de conocimiento de mundo.
- **[Surprisal](../modelos-cognitivos/surprisal.md)** — por qué no es lo mismo que coherencia, y qué haría falta para que lo fuera.
- **[Modelos predictivos](../modelos-cognitivos/modelos-predictivos.md)** — la comprensión como anticipación y error de predicción.
- **[Modelo dual-ruta](../modelos-cognitivos/dual-ruta-lectura.md)** — decodificar es condición necesaria y no suficiente: se puede leer cada palabra y no construir ningún modelo de situación.
- **[Memoria de trabajo](../modelos-cognitivos/memoria-trabajo.md)** — el espacio donde se sostienen las proposiciones mientras se integran.
- **[ECENI](../evaluacion/eceni.md)** — evaluación de comprensión de textos narrativos e inferencias.

---

## Referencias de entrada

- Halliday, M. A. K. & Hasan, R. (1976). *Cohesion in English*. Longman.
- van Dijk, T. & Kintsch, W. (1983). *Strategies of Discourse Comprehension*. Academic Press.
- Kintsch, W. (1988). The role of knowledge in discourse comprehension: a construction-integration model. *Psychological Review*, 95(2), 163-182.
- Kintsch, W. (1998). *Comprehension: A Paradigm for Cognition*. Cambridge University Press.
- Zwaan, R. & Radvansky, G. (1998). Situation models in language comprehension and memory. *Psychological Bulletin*, 123(2), 162-185.
- Schank, R. & Abelson, R. (1977). *Scripts, Plans, Goals and Understanding*. Lawrence Erlbaum.
- Graesser, A., McNamara, D. & Kulikowich, J. (2011). Coh-Metrix: providing multilevel analyses of text characteristics. *Educational Researcher*, 40(5), 223-234.
- Hagoort, P. et al. (2004). Integration of word meaning and world knowledge in language comprehension. *Science*, 304(5669), 438-441.
- Venhuizen, N., Crocker, M. & Brouwer, H. (2019). Expectation-based comprehension: modeling the interaction of world knowledge and linguistic experience. *Discourse Processes*, 56(3), 229-255.
- Barreyro, J. P., Fumagalli, J. et al. (2023). El vocabulario y la generación de inferencias en la comprensión de narraciones en niños preescolares. *RECIE*, 7(1), 205-222.
