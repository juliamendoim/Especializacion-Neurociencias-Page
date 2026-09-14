# El problema de las interfaces: qué viaja por las flechas

Los modelos de cajas y flechas de la neuropsicología cognitiva —el [dual-ruta](dual-ruta-lectura.md) entre ellos— especifican las **cajas** con enorme detalle: qué representa cada componente, cómo se rompe, qué patología produce. Las **flechas**, en cambio, casi no tienen teoría. Dicen "de acá pasa a allá" sin decir en qué código viaja la información, qué se conserva, qué se pierde ni quién ejecuta la conversión.

Esta entrada es sobre las flechas: el **problema de las interfaces representacionales**. Si el sistema está hecho de módulos que operan sobre formatos distintos, algo tiene que traducir entre ellos — y ese algo es, en la mayoría de los modelos, exactamente lo que no está especificado.

---

## 1. Por qué es un problema y no un detalle de implementación

Tomemos la cadena de la lectura. El análisis visual entrega algo **espacial, continuo y retinotópico**. El léxico ortográfico necesita **identidades de letra abstractas y ordenadas**. El sistema semántico opera sobre **conceptos**, que no tienen ni posición ni forma. El parser sintáctico opera sobre **categorías y relaciones estructurales**.

Son cuatro formatos que no comparten primitivos. No hay manera de que una representación retinotópica sea "leída" directamente por un sistema conceptual: no hay nada en el vocabulario de uno que el otro pueda interpretar.

El problema tiene tres caras que conviene no confundir:

**Formato**
: ¿En qué código está la representación que sale de un módulo?

**Traducción**
: ¿Qué operación convierte ese código en otro? ¿Es completa, parcial, con pérdida?

**Transmisión**
: ¿Cómo llega, cuándo, a qué velocidad, y qué pasa si productor y consumidor operan a ritmos distintos?

Los modelos clásicos suelen responder la tercera y dejar las dos primeras abiertas.

---

## 2. La respuesta clásica: un solo código

La salida más económica es negar que haya varios formatos. Si todos los módulos hablan el mismo código simbólico —el **lenguaje del pensamiento** de Fodor— entonces no hace falta traducir: solo hay que pasar tokens de un lado al otro.

Es elegante, pero resuelve el problema por decreto. Y choca con la observación de partida: fonología, sintaxis y semántica **manifiestamente** no manipulan los mismos primitivos. Un rasgo distintivo, un nodo sintáctico y un concepto no son la misma clase de objeto.

---

## 3. Jackendoff: los módulos se definen por formato, y hay módulos de interfaz

La propuesta más desarrollada sobre este problema invierte la definición misma de módulo.

Fodor define los módulos **por dominio**: visión, lenguaje, reconocimiento de caras. **Jackendoff** los define **por formato representacional**: fonología, sintaxis y semántica son módulos distintos porque las estructuras que manipulan requieren primitivos formales y principios de combinación diferentes. Eso es la **modularidad representacional**.

De ahí se sigue la consecuencia interesante:

> Como los módulos representacionales no pueden comunicarse directamente —no entienden el "idioma" del otro—, tienen que existir **módulos de interfaz**: componentes especializados cuyo único trabajo es traducir entre aspectos relevantes de dos módulos.

Tres propiedades que hacen de esto una teoría y no una etiqueta:

1. **La interfaz es un objeto teórico con estructura propia**, no una flecha. Puede tener sus propias restricciones y, en principio, su propia patología.
2. **Las interfaces también están encapsuladas.** Un módulo de interfaz no ve las representaciones completas de cada lado: ve solo los aspectos que necesita alinear. La interfaz fonología-sintaxis no accede al contenido conceptual.
3. **La traducción es parcial.** No hay isomorfismo entre formatos. Lo que hay son **reglas de correspondencia** que establecen un emparejamiento óptimo entre estructuras de tipos independientes — bastante menos que una conversión completa.

### La arquitectura paralela

En el modelo de Jackendoff, fonología, sintaxis y semántica son **tres sistemas generativos independientes** que operan en paralelo, no una cadena donde uno alimenta al siguiente. Una oración bien formada es una **tripleta** de estructuras bien formadas, más los enlaces de interfaz que las conectan.

El giro más fuerte es qué pasa a ser el léxico: deja de ser un depósito de palabras y pasa a ser **un conjunto almacenado de reglas de interfaz**. Cada entrada léxica es un fragmento de correspondencia entre fonología, sintaxis y semántica. Saber una palabra es saber un pedacito de traducción.

### El paralelo generativista

En el programa minimalista, las **interfaces** son también un objeto central: PF (forma fonológica) y LF (forma lógica) son los niveles donde la sintaxis "entrega" a los sistemas articulatorio-perceptual y conceptual-intencional. Las **condiciones de legibilidad** exigen que la sintaxis produzca representaciones que esos sistemas puedan efectivamente leer.

La diferencia de fondo: para Chomsky la sintaxis es el motor y las interfaces son las salidas; para Jackendoff los tres componentes son motores y las interfaces son el centro.

---

## 4. La respuesta implícita de la neuropsicología cognitiva: los buffers

Los modelos de cajas y flechas sí tienen una respuesta parcial, aunque rara vez se la presenta como tal: **un buffer es un componente de interfaz**.

El [buffer fonológico](buffer-fonologico.md) de salida y el buffer grafémico están postulados precisamente para resolver el problema de transmisión. Mantienen una representación en un formato determinado, durante un tiempo acotado, **desacoplando la velocidad del productor de la del consumidor**.

Y tienen firma patológica propia, distinta de la de las cajas que conectan: efectos de longitud, errores de posición de elemento, tasa de error constante a lo largo de la palabra. Que se puedan romper selectivamente es el argumento de que existen.

O sea: la boxología resuelve la **transmisión** metiendo buffers. Lo que sigue sin resolver es el **formato**.

---

## 5. El caso concreto: cómo se codifica la posición de las letras

En lectura hay una interfaz donde el problema de formato se vuelve completamente explícito y empíricamente decidible.

El análisis visual entrega algo espacial. El léxico ortográfico necesita **identidades de letra abstractas** —invariantes a fuente, tamaño y caja, las *abstract letter identities*— pero **con su orden preservado**. Si la abstracción fuera total, *CASA* y *SACA* activarían la misma entrada.

Las propuestas rivales son, literalmente, propuestas de formato de interfaz:

| Esquema | Cómo codifica el orden | Predicción distintiva |
|---|---|---|
| **Codificación por casilleros** | Posición absoluta: C en 1, A en 2, S en 3, A en 4 | Las transposiciones deberían ser tan disruptivas como las sustituciones |
| **Bigramas abiertos** | Pares ordenados, no necesariamente adyacentes: CA, CS, AS, AA… | Las transposiciones preservan muchos bigramas → efectos de similitud fuertes |
| **Codificación espacial** | Gradiente continuo de activación sobre la cadena | Similitud graduada según distancia de posición |

El dato que ordena el debate son los **efectos de transposición**: *jugdar* se confunde con *jugar* mucho más de lo que predice un esquema de casilleros estrictos. Eso favorece formatos más laxos que la posición absoluta.

Este debate es el problema de las interfaces planteado para un tramo específico, y muestra que la pregunta por el formato **es empírica**, no filosófica.

---

## 6. El nivel neural

### El caso resuelto: transformaciones de coordenadas

El ejemplo mejor entendido de una conversión de formato real en el cerebro está en la corteza parietal. La información visual llega en coordenadas **retinotópicas** y debe convertirse a coordenadas centradas en la cabeza o en el cuerpo para guiar un movimiento de alcance.

El mecanismo son los **campos de ganancia**: la respuesta retinotópica de la neurona se multiplica por una señal de posición ocular. La población, en conjunto, codifica la posición en el nuevo marco de referencia sin que ninguna neurona individual lo haga.

Importa como **prueba de existencia**: las conversiones de formato se pueden implementar neuronalmente y se pueden encontrar experimentalmente. No son un artefacto de la manera de dibujar modelos.

### La respuesta anatómica para lo transmodal: hub-and-spoke

Para el problema de integrar formatos sensoriales distintos en conceptos, el modelo dominante es el de **hub y radios**: regiones modalidad-específicas (los *radios*) conectadas a un **hub transmodal** en los **lóbulos temporales anteriores**, que destila los rasgos sensoriomotores dispersos en representaciones conceptuales coherentes y amodales.

La predicción de doble disociación es limpia y se cumple:

- Daño al **hub** → déficit semántico **en todas las modalidades**.
- Daño a un **radio** → déficit **solo en esa modalidad**.

La evidencia central viene de la **demencia semántica**, donde la atrofia temporal anterior produce un deterioro conceptual transversal a modalidades y a tipos de material.

Es una respuesta fuerte al problema de las interfaces: el formato común no está distribuido por todos lados, está **en un lugar anatómico concreto**, y ese lugar se puede romper.

### La versión sin lugar: zonas de convergencia

La alternativa de Damasio niega que exista un sitio donde resida la representación integrada. Las **zonas de convergencia** almacenan solo el **registro de cómo reactivar** los patrones distribuidos; la integración es retroactivación sincronizada hacia las cortezas de origen.

La diferencia con el hub es sustantiva: acá la transformación **no produce un objeto nuevo en un formato nuevo**, solo coordina los objetos viejos en sus formatos originales.

### El ruteo: comunicación por coherencia

Dos poblaciones neuronales se comunican efectivamente cuando sus oscilaciones están **en fase**. Eso responde *quién habla con quién y cuándo* — el problema de ruteo — sin decir nada sobre el código.

El acoplamiento **theta-gamma** en el procesamiento del habla es un caso concreto: agrupar unidades fonémicas dentro de ventanas silábicas **es** una transformación de formato, implementada por relación de fase entre dos ritmos. Ver [la sílaba como unidad subléxica](../lectura/silaba-unidad-sublexical.md).

### La respuesta que disuelve el problema: codificación predictiva

En los [modelos predictivos](modelos-predictivos.md), lo que baja por la jerarquía son **predicciones** y lo que sube son **errores de predicción ponderados por precisión**. Si eso es correcto, hay **un único formato de mensaje en todo el sistema**, y nadie traduce nada porque todos hablan la misma moneda.

Es la respuesta más económica disponible, y es parte de por qué el marco se volvió tan influyente. También es la más difícil de falsar.

---

## 7. La objeción conexionista

El conexionismo responde que **no hay formatos discretos que traducir**. Todo son vectores de activación, y una "transformación entre módulos" no es más que una multiplicación por una matriz de pesos. El problema de la interfaz sería un artefacto de haber dibujado cajas donde hay un continuo.

Es una objeción seria porque es constructiva: los modelos conexionistas de lectura producen los efectos conductuales relevantes sin postular ninguna interfaz explícita.

La contra es que la ausencia de un componente en un modelo que funciona no demuestra su ausencia en el sistema modelado — sobre todo cuando la evidencia de disociación (el hub, los buffers) apunta a que algunas de esas fronteras son reales porque se rompen selectivamente.

---

## 8. El caso de los transformers: una interfaz sin traducción

Los modelos de lenguaje actuales ofrecen un contraste instructivo, y conviene mirarlo con cuidado porque es fácil sacar la conclusión equivocada en cualquiera de las dos direcciones.

En un transformer, todos los componentes se comunican a través del **stream residual**: un espacio vectorial único, de dimensión fija, que atraviesa toda la red. El stream **no procesa nada**; es un canal de comunicación. Cada capa **lee** de él, computa, y **escribe** su resultado de vuelta sumándolo.

La descripción que hace de esto la interpretabilidad mecanicista es notablemente cercana al vocabulario de las interfaces: los componentes se comunican **leyendo y escribiendo en distintos subespacios** del stream residual, que **no tiene base privilegiada** y cuyo ancho de banda es un recurso escaso por el que los componentes compiten.

Pero la diferencia con Jackendoff es exactamente la que importa:

| | Arquitectura cognitiva | Transformer |
|---|---|---|
| Formatos | Múltiples e **inconmensurables** | **Uno solo** (vectores del mismo espacio) |
| Traducción | Módulos de interfaz dedicados | **Proyección lineal** a un subespacio |
| Encapsulamiento | Informativo, por diseño | Ninguno: todo componente puede leer todo |
| Origen de los límites | Postulados o madurativos | Emergentes del entrenamiento |

**En un transformer el problema de las interfaces no existe por construcción.** No hay traducción porque no hay dos idiomas: hay un idioma y muchos dialectos ocupando subespacios distintos del mismo espacio.

### El dato que complica la conclusión fácil

Sería cómodo cerrar diciendo que se trata de una homonimia: "módulo" e "interfaz" significan cosas distintas acá y allá, y listo.

Pero los transformers multilingües hacen algo que complica esa salida. Al procesar una entrada en cualquier idioma, las representaciones atraviesan **tres fases**: parten de un espacio ligado al idioma de entrada, pasan por un **espacio conceptual** en las capas intermedias donde la información es en buena medida independiente del idioma, y vuelven a un espacio específico del idioma de salida.

Es decir: una arquitectura sin ninguna presión de diseño hacia la modularidad **desarrolla espontáneamente algo con la forma de un hub transmodal** — representaciones amodales en el medio, específicas en los extremos. La misma forma que el modelo hub-and-spoke atribuye al lóbulo temporal anterior.

Eso sugiere una lectura más interesante que la homonimia: quizá el hub no sea un rasgo de diseño del cerebro sino **una solución convergente a una presión computacional** — la de tener que mapear muchas superficies distintas a un mismo conjunto de contenidos. Si dos sistemas con historias completamente diferentes convergen en la misma arquitectura, el candidato a explicación es la presión, no el linaje.

Queda abierto si eso es una convergencia genuina o un parecido de superficie entre dos cosas medidas con instrumentos incomparables. Es exactamente el tipo de pregunta que no se decide por argumento.

---

## Cómo se conecta con otros conceptos

- **[Modelo dual-ruta de lectura](dual-ruta-lectura.md)** — el modelo de cajas y flechas donde el problema se plantea con más claridad: cada flecha conecta formatos que no comparten primitivos.
- **[Buffer fonológico](buffer-fonologico.md)** — la respuesta implícita de la boxología al problema de transmisión.
- **[Modelos predictivos](modelos-predictivos.md)** — la propuesta de un formato de mensaje único que disuelve el problema.
- **[Modelos lexicalistas / conexionistas](modelos-lexicalistas.md)** — la posición que niega que haya formatos discretos que traducir.
- **[Marr y el modelo computacional de la visión](../neurobiologia/marr-vision-computacional.md)** — el problema del formato es justamente donde el nivel algorítmico debería tocar el implementacional.
- **[La sílaba como unidad subléxica](../lectura/silaba-unidad-sublexical.md)** — el acoplamiento theta-gamma como caso concreto de transformación de formato implementada por fase.
- **[Tarea de anagrama](tarea-anagrama.md)** — otro caso donde el formato de la representación (letras vs. tokens BPE) explica una disociación entre humanos y modelos.

---

## Referencias de entrada

- Jackendoff, R. (1997). *The Architecture of the Language Faculty*. MIT Press. (Modularidad representacional y módulos de interfaz.)
- Jackendoff, R. (2002). *Foundations of Language: Brain, Meaning, Grammar, Evolution*. Oxford University Press.
- Jackendoff, R. (2025). The Parallel Architecture in language and elsewhere. *Topics in Cognitive Science*.
- Fodor, J. (1983). *The Modularity of Mind*. MIT Press.
- Patterson, K. & Lambon Ralph, M. (2016). The hub-and-spoke hypothesis of semantic memory. En *Neurobiology of Language*. Academic Press.
- Lambon Ralph, M., Jefferies, E., Patterson, K. & Rogers, T. (2017). The neural and computational bases of semantic cognition. *Nature Reviews Neuroscience*, 18(1), 42-55.
- Damasio, A. (1989). Time-locked multiregional retroactivation: a systems-level proposal for the neural substrates of recall and recognition. *Cognition*, 33(1-2), 25-62.
- Zipser, D. & Andersen, R. (1988). A back-propagation programmed network that simulates response properties of a subset of posterior parietal neurons. *Nature*, 331, 679-684.
- Fries, P. (2005). A mechanism for cognitive dynamics: neuronal communication through neuronal coherence. *Trends in Cognitive Sciences*, 9(10), 474-480.
- Grainger, J. & van Heuven, W. (2004). Modeling letter position coding in printed word perception. En *The Mental Lexicon*. Nova Science.
- Elhage, N. et al. (2021). A mathematical framework for transformer circuits. *Anthropic / Transformer Circuits Thread*.
- Wendler, C., Veselovsky, V., Monea, G. & West, R. (2024). Do llamas work in English? On the latent language of multilingual transformers. *arXiv:2402.10588*.
- Dumas, C. et al. (2024). Separating tongue from thought: activation patching reveals language-agnostic concept representations in transformers. *arXiv:2411.08745*.
