# N400 y P600: los potenciales del lenguaje

Los **potenciales relacionados con eventos** (ERP) son la señal de EEG promediada a lo largo de muchos ensayos, alineada temporalmente con un estímulo. El promediado cancela la actividad no relacionada y deja una onda con picos característicos, identificados por su **polaridad** y su **latencia**: N400 es una deflexión negativa que llega a su máximo alrededor de los 400 ms; P600, una positiva alrededor de los 600 ms.

Su virtud es la **resolución temporal en el orden de milisegundos**, que permite ver el curso del procesamiento en vez de solo su resultado. Su límite es la resolución espacial: el ERP dice *cuándo*, no *dónde*.

---

## El N400

### Qué lo dispara

El hallazgo fundacional es de Kutas y Hillyard (1980): leer una oración que termina de manera semánticamente inapropiada —*"Untó el pan tibio con medias"*— produce una negatividad centro-parietal marcada alrededor de los 400 ms respecto de un final esperable.

La interpretación inicial fue "detector de anomalías semánticas". Es incorrecta, y la corrección importa.

### No es todo o nada: es graduado

El N400 aparece ante **cualquier** palabra de contenido, no solo ante las anómalas. Lo que varía es su **amplitud**, y varía de manera continua con la predictibilidad: cuanto más esperable es la palabra en su contexto, **menor** el N400.

Eso lo convierte en algo mucho más útil que un detector de errores: es un **índice graduado del costo de acceder o integrar significado**. La relación con la probabilidad cloze es monótona.

Y por eso conecta con [surprisal](../modelos-cognitivos/surprisal.md): si la amplitud escala con la improbabilidad de la palabra dado el contexto, el N400 es un correlato neural plausible de la surprisal. Hay trabajos que muestran que la surprisal de modelos de lenguaje explica múltiples efectos N400.

Lo modula:

- **Predictibilidad contextual** (el factor dominante)
- Relación semántica con el contexto previo
- **Frecuencia léxica** — las palabras infrecuentes dan N400 mayor
- **Repetición** — la segunda presentación lo reduce
- Concreción e imaginabilidad

### El resultado que más dice sobre comprensión

**Hagoort, Hald, Bastiaansen y Petersson (2004)**, en *Science*, contrastaron dos tipos de violación en la misma estructura:

| Oración | Tipo |
|---|---|
| *"Los trenes holandeses son **amarillos** y van muy llenos"* | correcta |
| *"Los trenes holandeses son **blancos** y van muy llenos"* | violación de **conocimiento de mundo** (en Holanda son amarillos) |
| *"Los trenes holandeses son **agrios** y van muy llenos"* | violación **semántica** |

Las dos violaciones produjeron **N400 de amplitud y latencia similares**. En fMRI, ambas activaron el **giro frontal inferior izquierdo**.

La conclusión es fuerte: **el cerebro no trata el significado de las palabras y el conocimiento del mundo como dos bases de datos consultadas en serie.** Los integra en paralelo y en la misma ventana temporal. No hay un momento "lingüístico" previo a un momento "enciclopédico".

Para el estudio de la [comprensión de texto](../lectura/cohesion-coherencia-modelo-situacion.md) esto es decisivo: las violaciones de coherencia basadas en conocimiento de mundo son detectables en línea **con los mismos instrumentos** que las semánticas.

### El debate abierto: ¿acceso o integración?

Dos lecturas conviven:

**Acceso léxico-semántico**
: El N400 refleja la facilidad con que se activa la información semántica asociada a la palabra. El contexto preactiva rasgos, y una palabra preactivada se accede más barato.

**Integración**
: El N400 refleja el costo de **incorporar** el significado de la palabra a la representación del mensaje que se viene construyendo.

La distinción no es escolástica: la primera ubica el efecto antes del compromiso con una interpretación y la segunda después. Los datos no la resuelven del todo, y hay posiciones intermedias.

---

## El P600

Positividad posterior alrededor de los 600 ms, clásicamente asociada a **violaciones sintácticas** y a procesos de **reanálisis** — las oraciones de [garden path](../modelos-cognitivos/garden-paths.md) lo producen.

La lectura tradicional era una división de trabajo limpia: N400 para lo semántico, P600 para lo sintáctico. **No se sostiene.**

El problema es el llamado **P600 semántico**: ciertas oraciones con anomalías de rol temático —del tipo *"el pescado que comió al hombre"*— producen P600 y **no** N400, cuando la división clásica predice lo contrario. Hay varias explicaciones en competencia (conflicto entre rutas de procesamiento, monitoreo, reanálisis semántico) y ninguna cerró el caso.

La moraleja metodológica: **los componentes ERP no son módulos.** Son patrones de actividad que correlacionan con familias de manipulaciones, no etiquetas de procesos.

---

## Qué hay que saber para leer un paper con ERP

- **Promediado**: cada condición necesita decenas de ensayos limpios por participante. Los ERP no se miden en un ítem.
- **Línea de base y ventana**: los resultados dependen de qué intervalo previo se usa como referencia y en qué ventana se cuantifica la amplitud. Deben estar declarados.
- **Artefactos**: parpadeos y movimientos oculares contaminan; se corrigen o se descartan ensayos. Cuántos se descartaron es un dato relevante.
- **Co-registro con movimientos oculares**: técnicamente difícil pero permite lectura natural en vez de presentación palabra por palabra. Es la dirección en la que va el campo.

---

## Cómo se conecta con otros conceptos

- **[Surprisal](../modelos-cognitivos/surprisal.md)** — la amplitud del N400 escala con la improbabilidad contextual; es el puente entre modelos de lenguaje y electrofisiología.
- **[Cohesión, coherencia y modelo de situación](../lectura/cohesion-coherencia-modelo-situacion.md)** — el resultado de Hagoort es lo que vuelve medible la coherencia basada en conocimiento de mundo.
- **[Modelos predictivos](../modelos-cognitivos/modelos-predictivos.md)** — el N400 como error de predicción léxico-semántico.
- **[Garden paths](../modelos-cognitivos/garden-paths.md)** — el terreno clásico del P600.
- **[Efecto de canonicidad](../modelos-cognitivos/efecto-canonicidad.md)** — las estructuras no canónicas y su firma electrofisiológica.
- **[Frecuencia](../modelos-cognitivos/frecuencia.md)** — la frecuencia léxica modula el N400, otro nivel donde la frecuencia deja huella.

---

## Referencias de entrada

- Kutas, M. & Hillyard, S. (1980). Reading senseless sentences: brain potentials reflect semantic incongruity. *Science*, 207(4427), 203-205.
- Kutas, M. & Federmeier, K. (2011). Thirty years and counting: finding meaning in the N400 component of the event-related brain potential. *Annual Review of Psychology*, 62, 621-647.
- Hagoort, P., Hald, L., Bastiaansen, M. & Petersson, K. M. (2004). Integration of word meaning and world knowledge in language comprehension. *Science*, 304(5669), 438-441.
- Lau, E., Phillips, C. & Poeppel, D. (2008). A cortical network for semantics: (de)constructing the N400. *Nature Reviews Neuroscience*, 9(12), 920-933.
- Osterhout, L. & Holcomb, P. (1992). Event-related brain potentials elicited by syntactic anomaly. *Journal of Memory and Language*, 31(6), 785-806.
- Kuperberg, G. (2007). Neural mechanisms of language comprehension: challenges to syntax. *Brain Research*, 1146, 23-49.
- Michaelov, J. et al. (2024). Strong prediction: language model surprisal explains multiple N400 effects. *Neurobiology of Language*.
