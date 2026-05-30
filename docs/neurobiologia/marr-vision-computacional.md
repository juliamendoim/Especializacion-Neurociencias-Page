# El modelo computacional de la visión de Marr (y sus continuidades)

**David Marr** (1945–1980) fue un neurocientífico británico que trabajó en el MIT en la intersección entre neurofisiología, psicología cognitiva y lo que después se llamó IA. Murió a los 35 años de leucemia, y su libro *Vision* (1982, póstumo) terminó marcando la agenda de buena parte de la ciencia cognitiva y la neurociencia computacional posteriores.

La idea fuerte de Marr — y por la que se lo cita todo el tiempo — es que **un sistema biológico que procesa información se entiende sólo si se lo describe en varios niveles a la vez**, y que la visión es un caso paradigmático para mostrarlo.

## Los tres niveles de Marr

Para entender cualquier sistema cognitivo Marr distingue **tres niveles de análisis** que son **complementarios, no jerárquicos**:

| Nivel | Pregunta | Para la visión |
|---|---|---|
| **1. Computacional** | ¿Qué problema resuelve el sistema y por qué? | "Recuperar la estructura 3D del mundo a partir de imágenes 2D que llegan a la retina." |
| **2. Algorítmico / Representacional** | ¿Con qué representaciones y procedimientos lo resuelve? | "Detectar bordes con un filtro, agruparlos en superficies, reconstruir profundidad por disparidad binocular." |
| **3. Implementacional** | ¿En qué hardware está implementado? | "Capas V1, V2, V4, IT del córtex visual; neuronas con campos receptivos específicos." |

La tesis de Marr: **un análisis sólo en el nivel implementacional no explica nada**. Mostrar qué neuronas se activan no dice qué problema resuelve la red ni con qué algoritmo lo hace. Por eso muchos estudios "estamos viendo dónde se activa el cerebro" se quedan cortos: contestan el nivel 3 sin abordar el 1 ni el 2.

Es paralelo a (y a veces se confunde con) **[las 4 preguntas de Tinbergen](tinbergen-niveles-analisis.md)** — pero Marr piensa en sistemas de procesamiento de información, Tinbergen en historia evolutiva.

## El modelo de la visión propiamente dicho

Marr propone que la visión humana funciona en una **secuencia modular de representaciones**, cada vez más abstractas y cada vez más cercanas al objeto que está afuera:

| Etapa | Qué codifica | Cuándo aparece |
|---|---|---|
| **Imagen retinal** | Intensidad lumínica en cada punto. | Lo que llega al ojo. |
| **Esbozo primario** (*primal sketch*) | Bordes, manchas, terminaciones, orientaciones locales — todavía en 2D. | Procesamiento temprano (V1). |
| **Esbozo 2½D** (*2.5D sketch*) | Superficies orientadas en profundidad, **vistas desde el observador**. | Procesamiento intermedio. |
| **Modelo 3D** | Objetos completos en coordenadas **independientes del observador**. | Reconocimiento de objetos. |

La metáfora: la visión sería **reconstrucción**. El cerebro toma un dato pobre (proyección 2D en la retina) y lo va enriqueciendo etapa por etapa hasta recuperar el mundo 3D.

### Algunos algoritmos concretos que Marr propuso

- **Detección de bordes con el Laplaciano de la Gaussiana** (LoG) — suavizar la imagen y buscar los puntos donde la segunda derivada cruza por cero. Marr & Hildreth (1980) lo propusieron como modelo de lo que hacen las neuronas simples de V1.
- **Estereopsis** (Marr & Poggio 1979): algoritmo para resolver la correspondencia entre los dos ojos y recuperar profundidad por disparidad binocular.
- **Visión modular**: cada subsistema (forma, color, movimiento, profundidad) resuelve su problema en paralelo, y después se integran. Esta tesis fue un punto de partida para la **modularidad de la mente** de Fodor (1983).

## Críticas (a propósito)

Conviene tener presentes antes de comprar el paquete completo:

- **Top-down vs. bottom-up**: Marr es fuertemente **bottom-up** — empezás del píxel y vas reconstruyendo. La evidencia posterior sugiere que la visión también va al revés: expectativas y conocimiento previo modulan lo que se "ve" desde etapas tempranas. Esto es la base del **predictive coding** (ver abajo).
- **Modularidad estricta**: la corriente visual ventral y dorsal interactúan más de lo que el modelo modular sugería.
- **Reconstrucción del mundo**: críticas de la cognición encarnada (Gibson, O'Regan, Noë) argumentan que la visión no reconstruye una representación interna del mundo sino que es un **enganche activo con el entorno**.

## Continuidades — qué pasó después

### En neurociencia computacional

- **Tomaso Poggio**, colaborador de Marr en el MIT, continuó el programa y entrenó a varias generaciones de investigadores en visión computacional con anclaje biológico.
- **HMAX** (Riesenhuber & Poggio, 1999) — modelo jerárquico feed-forward de la corriente ventral inspirado en Hubel-Wiesel + Marr. Es el **antepasado directo** de las redes convolucionales modernas.
- **Yamins & DiCarlo (2014)** mostraron que las redes convolucionales profundas entrenadas para clasificar imágenes **predicen la actividad neuronal del IT** (córtex inferotemporal del macaco) mejor que cualquier modelo previo. Esto reabrió la pregunta de si **el córtex visual implementa algo parecido a una CNN** — un eco fuerte del programa de Marr a 30 años de distancia.

### En IA / aprendizaje profundo

Las **redes convolucionales** (LeCun, 1989; Krizhevsky, 2012) heredan tres ideas centrales de la tradición Marr/Hubel-Wiesel:

1. **Procesamiento jerárquico** en capas sucesivas (esbozo primario → 2½D → 3D ≈ capas tempranas → intermedias → IT).
2. **Campos receptivos locales** y compartidos (convolución).
3. **Construcción progresiva de invariancias** (translation invariance vía pooling).

Lo que **no** heredan: la separación estricta de los tres niveles. Una CNN aprende fin-a-fin sin distinción clara entre representación y algoritmo, lo cual es exactamente lo que Marr quería evitar — y la pregunta abierta es si eso es un defecto o una ventaja.

### Predictive coding y Bayesian brain

La continuación más viva del **proyecto Marr** son hoy las teorías predictivas:

- **Rao & Ballard (1999)** — el córtex visual no procesa la entrada sino el **error de predicción**: cada capa superior predice la inferior, y sólo lo no predicho sube. Marr al revés.
- **Friston** — el principio de **energía libre** generaliza esto a todo el cerebro: minimizar el error de predicción es la operación fundamental.
- **Bayesian brain** — la percepción como inferencia probabilística sobre las causas más probables de la entrada sensorial (Knill & Pouget, 2004).

Todas estas teorías se ubican en el **nivel computacional de Marr** (qué problema resuelve el sistema), pero con una respuesta distinta: no "reconstrucción del mundo 3D" sino "minimización del error de predicción".

## Por qué importa para este seminario

- Marr es un buen contrapeso a la pregunta "¿dónde se activa el cerebro cuando X?" — recuerda que ubicar la activación no equivale a entender el proceso.
- Es el puente más limpio entre **neurociencia** y **modelos computacionales de la cognición** (incluido lo que hoy se llama IA).
- En el contexto de lenguaje y lectura, el modelo dual-ruta o los modelos de comprensión también pueden leerse con los tres niveles: ¿qué problema resuelve la lectura? ¿con qué algoritmo? ¿en qué circuitos?

## Conexión con el resto del sitio

- **[Las 4 preguntas de Tinbergen](tinbergen-niveles-analisis.md)** — marco análogo desde la etología; los tres niveles de Marr son la versión cognitiva.
- **[Bottom-up vs. top-down](bottom-up-top-down.md)** — Marr es paradigma de bottom-up; el predictive coding empuja en la dirección opuesta.
- **[Modelo dual-ruta de lectura](../modelos-cognitivos/dual-ruta-lectura.md)** — otro caso donde los tres niveles permiten ordenar la discusión.

## Lecturas

- **Marr, D. (1982)** *Vision: A computational investigation into the human representation and processing of visual information*. Freeman. — el libro fundacional. El capítulo 1 ("The philosophy and the approach") es el resumen del programa de los tres niveles.
- **Marr, D. & Hildreth, E. (1980)** "Theory of edge detection". *Proc. R. Soc. London B* 207:187-217.
- **Marr, D. & Poggio, T. (1979)** "A computational theory of human stereo vision". *Proc. R. Soc. London B* 204:301-328.
- **Riesenhuber, M. & Poggio, T. (1999)** "Hierarchical models of object recognition in cortex". *Nature Neuroscience* 2:1019-1025. — el modelo HMAX, eslabón entre Marr y las CNNs.
- **Yamins, D. L. K. & DiCarlo, J. J. (2016)** "Using goal-driven deep learning models to understand sensory cortex". *Nature Neuroscience* 19:356-365. — el reencuentro entre Marr y deep learning.
- **Rao, R. P. N. & Ballard, D. H. (1999)** "Predictive coding in the visual cortex". *Nature Neuroscience* 2:79-87. — la continuación predictiva.
- **Friston, K. (2010)** "The free-energy principle: a unified brain theory?". *Nature Reviews Neuroscience* 11:127-138.
