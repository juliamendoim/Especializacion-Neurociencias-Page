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

## Cuán establecido está todo esto

Conviene graduar la confianza, porque no todo lo anterior tiene el mismo respaldo.

### Consenso: el efecto

El N400 es de lo más replicado que hay en neurociencia cognitiva. Es de 1980, o sea que **precede a la [crisis de replicación](crisis-replicacion.md) y la atravesó sin problemas**: está en la categoría de los efectos básicos muy robustos, junto con Stroop o el efecto de frecuencia.

El argumento más fuerte no es la cantidad de estudios sino **la variedad de estímulos que lo producen**: palabras escritas, habladas y signadas, pseudopalabras, dibujos, fotos, videos de caras, objetos y acciones, sonidos y símbolos matemáticos. Un efecto que aparece en tantos paradigmas no puede ser artefacto de ninguno.

La modulación **graduada** por predictibilidad también es consenso.

### Abierto: qué significa

Qué proceso indexa el N400 —acceso, integración o error de predicción— **no está resuelto**, y siguen publicándose estudios diseñados específicamente para separar esas cuentas. Los **generadores neurales** tampoco están cerrados: la corteza temporal izquierda es el candidato principal, pero el ERP tiene mala resolución espacial y la evidencia apunta a una red distribuida.

El **P600 está bastante menos asentado que el N400**: hay varias cuentas en competencia sobre el P600 semántico y ninguna cerró el caso.

### Problema real: la calidad de los estudios

Šoškić y colegas (2021) revisaron **132 papers de N400** publicados entre 1980 y 2018, evaluando 73 propiedades de diseño, procesamiento, medición, estadística y reporte. Encontraron que **cada estudio tenía un enfoque único** y que **a todos les faltaba al menos algún detalle**.

La causa es estructural: decenas de electrodos por cientos de puntos temporales dan una cantidad casi ilimitada de análisis posibles. Luck y Gaspelin (2017) mostraron que eligiendo ventana y electrodos **mirando los datos**, más ANOVAs multifactoriales, la probabilidad de al menos un efecto significativo espurio **supera el 50 %** en muchos experimentos.

**La distinción que hay que hacer:** eso afecta mucho más a los hallazgos **nuevos y específicos** que al efecto central. El contraste congruente/incongruente es enorme y aparece en cualquier análisis razonable; un efecto que solo emerge en una ventana estrecha y en electrodos elegidos después de ver los datos, no.

Lo mismo vale para el resultado de Hagoort sobre conocimiento de mundo: es un antecedente sólido y muy citado, pero es **un estudio**. La afirmación general —que el conocimiento de mundo modula el N400— está replicada; la versión fuerte de que ambas violaciones cuestan exactamente lo mismo descansa sobre ese trabajo.

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
- **[La crisis de replicación](crisis-replicacion.md)** — por qué el efecto central es sólido pero conviene mirar con lupa los hallazgos específicos.

---

## Referencias de entrada

- Kutas, M. & Hillyard, S. (1980). Reading senseless sentences: brain potentials reflect semantic incongruity. *Science*, 207(4427), 203-205.
- Kutas, M. & Federmeier, K. (2011). Thirty years and counting: finding meaning in the N400 component of the event-related brain potential. *Annual Review of Psychology*, 62, 621-647.
- Hagoort, P., Hald, L., Bastiaansen, M. & Petersson, K. M. (2004). Integration of word meaning and world knowledge in language comprehension. *Science*, 304(5669), 438-441.
- Lau, E., Phillips, C. & Poeppel, D. (2008). A cortical network for semantics: (de)constructing the N400. *Nature Reviews Neuroscience*, 9(12), 920-933.
- Osterhout, L. & Holcomb, P. (1992). Event-related brain potentials elicited by syntactic anomaly. *Journal of Memory and Language*, 31(6), 785-806.
- Kuperberg, G. (2007). Neural mechanisms of language comprehension: challenges to syntax. *Brain Research*, 1146, 23-49.
- Šoškić, A., Jovanović, V., Styles, S., Kappenman, E. & Ković, V. (2021). How to do better N400 studies: reproducibility, consistency and adherence to research standards in the existing literature. *Neuropsychology Review*, 32, 577-600.
- Luck, S. & Gaspelin, N. (2017). How to get statistically significant effects in any ERP experiment (and why you shouldn't). *Psychophysiology*, 54(1), 146-157.
- Michaelov, J. et al. (2024). Strong prediction: language model surprisal explains multiple N400 effects. *Neurobiology of Language*.
