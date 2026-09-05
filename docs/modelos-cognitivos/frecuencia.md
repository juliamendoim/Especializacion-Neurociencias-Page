# Frecuencia y cómo se representa mentalmente

La **frecuencia** — qué tan seguido aparece una palabra, una estructura o una construcción en la experiencia lingüística — es uno de los conceptos más empíricamente robustos y teóricamente cargados de la psicolingüística. Las palabras frecuentes se reconocen más rápido. Las estructuras frecuentes se procesan con menos esfuerzo. Las construcciones frecuentes se aprenden antes. **Esto está fuera de discusión a nivel comportamental**. Lo que sí se discute, y mucho, es **cómo se supone que esa frecuencia "vive" en la mente**: qué tipo de representación mental implementa la sensibilidad a la frecuencia.

Esta entrada es transversal a las tres alternativas modernas al [modelo generativo clásico](modelos-predictivos.md): [modelos predictivos](modelos-predictivos.md), [basados en memoria](modelos-basados-memoria.md) y [lexicalistas/conexionistas](modelos-lexicalistas.md). Cada una propone una mecánica distinta para la frecuencia.

## El punto de partida: el modelo clásico casi no incluye frecuencia

Frazier, Forster y Fodor pensaron el procesamiento del lenguaje como **categórico y modular**. Las heurísticas del parser (*minimal attachment*, *late closure*) son universales — se aplican igual a oraciones frecuentes que a infrecuentes. Forster reconoció que la frecuencia influye en el **acceso léxico** (más frecuente, más rápido), pero **no en el parsing**.

Este es uno de los puntos débiles que los modelos modernos atacan: si la frecuencia no juega un rol durante el procesamiento estructural, ¿por qué procesamos más rápido las estructuras frecuentes? ¿Por qué *send NP NP* se procesa de manera distinta a *send NP PP* dependiendo del verbo? El clásico no tiene buena respuesta. Las alternativas modernas hacen de la frecuencia un mecanismo central, pero la implementan de **cuatro maneras profundamente distintas**.

## Las cuatro propuestas modernas

### 1. Activación residual con decaimiento (ACT-R, Lewis & Vasishth)

Cada *chunk* en memoria tiene un **nivel de activación base** que es función explícita del historial de uso. La fórmula canónica de ACT-R:

$$B_i = \ln\left(\sum_{j=1}^{n} t_j^{-d}\right)$$

donde *t_j* es el tiempo desde el j-ésimo uso del chunk *i*, y *d* es una constante de decaimiento (típicamente 0.5). Cada uso "refresca" la activación; el decaimiento la erosiona con el tiempo.

**Implicaciones mentales**:

- Más frecuente y reciente → más activación → más rápido se recupera.
- La frecuencia y la recencia están **integradas en una sola medida**.
- El logaritmo en la fórmula predice que el efecto de la frecuencia es **logarítmico** — la diferencia entre 10 y 100 ocurrencias es similar a la diferencia entre 1000 y 10000.

**Mecanismo mental propuesto**: existe una "memoria de uso" que mantiene activación residual de cada representación lingüística, actualizada en cada uso. Es la versión más explícita y matemáticamente formal de cómo la frecuencia opera en la mente. Es la cara central de los [modelos basados en memoria](modelos-basados-memoria.md).

### 2. Pesos en redes neuronales (Elman, SRN, conexionismo, LLMs)

**No hay contador**, hay **pesos sinápticos**. Cada experiencia lingüística ajusta los pesos vía aprendizaje hebbiano o *error-driven* (backpropagation). Una palabra o estructura frecuente termina con conexiones más fuertes porque hubo más oportunidades de ajuste.

**Implicaciones mentales**:

- La frecuencia no es algo "almacenado" en ningún lugar específico — emerge de la **facilidad con que la red activa una representación**.
- Es completamente **implícita y distribuida** sobre toda la red.
- Una palabra rara cuesta más porque sus patrones de activación no están bien establecidos.
- No hay un "contador de frecuencia" inspeccionable — solo hay pesos.

**Mecanismo mental propuesto**: la sensibilidad a la frecuencia es una propiedad emergente de la arquitectura, no una operación explícita. Esta es la cara central de los [modelos conexionistas/lexicalistas](modelos-lexicalistas.md), y por extensión, de los LLMs.

### 3. Probabilidades léxicas almacenadas (MacDonald, Pearlmutter & Seidenberg 1994)

El léxico **carga representaciones probabilísticas explícitas**. Cada palabra tiene "*frequency biases*" para sus posibles estructuras: *send* sabe que aparece ~70 % en transitivo simple y ~30 % en ditransitivo; *give* sabe lo opuesto.

**Implicaciones mentales**:

- El léxico **es** un repositorio probabilístico.
- Estas frecuencias **no son derivadas de otro lado** — son **constitutivas de qué significa "saber una palabra"**.
- Saber una palabra es saber su distribución de uso, no solo su forma y significado.

**Mecanismo mental propuesto**: la frecuencia es información léxica de primer nivel, igual de fundamental que la categoría gramatical o el significado. Esta es la cara central del **lexicalismo** (MacDonald et al. 1994; Trueswell & Tanenhaus 1994).

Ambigüedad sobre si las probabilidades son realmente "almacenadas explícitamente" o son **descripción computacional** de algo implementado vía pesos (familia 2). El propio MacDonald oscila entre lecturas más realistas y más instrumentalistas.

### 4. Ejemplares almacenados (Bybee, Pierrehumbert)

Cada experiencia lingüística se almacena como un **ejemplar concreto** (token episódico) en una memoria de gran capacidad. No hay abstracción separada de los datos: la "regla" no es una regla, es una **nube densa de ejemplares similares** en el espacio de representación.

**Implicaciones mentales**:

- La frecuencia es **literalmente número de ejemplares almacenados**.
- Categorías más frecuentes son nubes más densas; más fácil acceder, más resistentes al olvido.
- El conocimiento lingüístico es **conocimiento episódico** del lenguaje, no abstracciones.
- Bybee aplica esto especialmente a morfología y construcciones; Pierrehumbert a fonología.

**Mecanismo mental propuesto**: la memoria lingüística funciona como la memoria episódica — guarda eventos concretos, no abstracciones. La sensibilidad a la frecuencia emerge de la densidad de ejemplares en torno a una región del espacio de representación.

## Una segunda tradición: los modelos de acceso léxico

Las cuatro propuestas anteriores vienen del debate sobre **aprendizaje y parsing** (usage-based vs. innatismo). Hay una tradición paralela, la del **reconocimiento visual de palabras**, que se hizo la misma pregunta con otro vocabulario y llegó a respuestas distintas. Vale tenerlas juntas porque responden más literalmente a "¿dónde vive la frecuencia?".

### 5. Umbral o nivel de reposo (logogen, activación interactiva)

En el [modelo de logogen](activacion.md) de Morton (1969), cada palabra tiene una unidad detectora con un **umbral**. La frecuencia fija ese umbral: las palabras frecuentes lo tienen más bajo y necesitan menos evidencia para dispararse. El modelo de activación interactiva de McClelland y Rumelhart (1981) hace lo mismo con **niveles de activación en reposo**.

Es la respuesta más literal posible a la pregunta: la frecuencia vive **en el estado basal de la unidad léxica**, antes de que llegue ningún estímulo. Es también la más fácil de conectar con la clínica: un léxico degradado pierde primero las unidades de umbral más alto, es decir, las de baja frecuencia.

### 6. Rango, no magnitud (Forster; Murray & Forster 2004)

En el modelo de búsqueda serial de Forster (1976), el léxico está organizado en "cajones" recorridos **en orden de frecuencia**. Lo que importa no es cuán frecuente es una palabra sino **en qué posición del orden está**.

La distinción no es cosmética. Murray y Forster (2004) argumentan que los datos ajustan mejor al **rango** que a la frecuencia bruta o a su logaritmo. Si tienen razón, el sistema no almacena cantidades: almacena un **orden**. Es una hipótesis más económica y bastante menos discutida de lo que merece.

### 7. Probabilidad previa (Norris 2006, *Bayesian Reader*)

No hay contador, ni umbral, ni orden: hay **inferencia**. El reconocimiento es una decisión bayesiana óptima que combina la evidencia perceptual con el **prior** de cada candidato, y ese prior es la frecuencia.

La consecuencia teórica es fuerte: los efectos de frecuencia dejan de ser una propiedad del almacenamiento y pasan a ser **una propiedad de la decisión**. De ahí que el modelo prediga —correctamente— que el tamaño del efecto **varía con la tarea y con el contexto**. Norris lo formula así: los efectos de frecuencia son una especie de efecto de predictibilidad que aparece **cuando el contexto está ausente o no restringe**, y el sistema tiene que caer en el prior.

Esto tiene consecuencias metodológicas directas: una tarea con contexto reducido no es una tarea "más simple", es una tarea diseñada para **forzar la exhibición del prior**.

### 8. Acumulación de evidencia (modelos de difusión)

En los modelos de difusión (Ratcliff), la decisión se modela como acumulación ruidosa de evidencia hasta un límite. La frecuencia puede entrar en **dos parámetros distintos**:

- **Tasa de deriva** (*drift rate*): la evidencia a favor de una palabra frecuente se acumula más rápido.
- **Punto de partida**: el acumulador arranca sesgado hacia la respuesta frecuente, antes de ver nada.

Son mecanismos diferentes con la misma firma gruesa en latencias medias, y se separan solo modelando **la distribución completa de tiempos de respuesta**. Es un buen recordatorio de que "efecto de frecuencia" nombra un fenómeno conductual, no un mecanismo.

---

## ¿Es la frecuencia la variable correcta?

Dos resultados le pegan al concepto mismo, y conviene conocerlos antes de tratar la frecuencia como primitivo.

### Diversidad contextual

**Adelman, Brown y Quesada (2006)** compararon la frecuencia con la **diversidad contextual**: en cuántos contextos distintos (documentos, películas) aparece una palabra, sin importar cuántas veces en cada uno.

El resultado es asimétrico y por eso contundente: al controlar diversidad contextual, **el efecto de frecuencia desaparece; al revés no**. Lo que estaría representado no sería un conteo de ocurrencias sino algo más cercano a **en cuántas situaciones distintas esa palabra resultó útil**.

Es una diferencia conceptual, no estadística: sugiere que el sistema no registra repeticiones sino **contextos de utilidad**.

### Edad de adquisición

Buena parte de lo que se atribuye a la frecuencia puede ser **orden de entrenamiento**. Las palabras aprendidas temprano quedan más entrenadas en la red, y frecuencia y edad de adquisición están fuertemente correlacionadas en cualquier corpus.

En español, Cuetos y colegas muestran efectos de edad de adquisición **independientes** de la frecuencia en denominación, modulados por la tarea y por la imaginabilidad de los ítems: en denominación inmediata y rápida solo pesa la frecuencia; en decisión léxica pesan ambas. O sea que ninguna de las dos es reducible a la otra, pero tampoco son separables sin diseños específicos.

### La moraleja

Si la diversidad contextual predice mejor que la frecuencia, y la edad de adquisición aporta varianza propia, entonces **el cerebro nunca contó nada**. Lo que llamamos frecuencia es un resumen externo de una historia de aprendizaje que incluye cuándo se aprendió algo, en cuántas situaciones y con qué utilidad. "Frecuencia" es una variable de investigador, no necesariamente una magnitud representada.

---

## Dónde vive la frecuencia en el cerebro

Un argumento neural sencillo apunta en la misma dirección. Si existiera un contador, un ítem frecuente debería producir **más** actividad. Se observa lo contrario: **supresión por repetición**, menos respuesta neural para lo repetido y lo frecuente. Esa es la firma de un sistema **sintonizado** —representaciones más eficientes y más selectivas— no de una tabla que se consulta.

A nivel de localización, la frecuencia léxica modula sobre todo el **giro frontal inferior izquierdo** y regiones **temporales posteriores y fusiformes**: las palabras de baja frecuencia producen más activación, consistente con una recuperación más costosa.

### La frecuencia no es una sola cosa

El punto más importante para no simplificar: **Carreiras, Mechelli y Price (2006)** manipularon **frecuencia léxica y frecuencia silábica en el mismo experimento** y encontraron firmas neurales distintas — las sílabas de baja frecuencia modularon la ínsula anterior izquierda, con un patrón disociable del de la frecuencia de palabra.

O sea que la frecuencia no vive en un lugar. **Vive en cada nivel de representación que aprende**: correspondencias fonema-grafema, sílabas, morfemas, palabras, construcciones. Cada nivel tiene la suya, y en cualquier tarea concreta varias están operando a la vez.

Esto tiene una consecuencia práctica para leer literatura clínica: cuando un trabajo reporta "un efecto de frecuencia", la primera pregunta es **frecuencia de qué unidad**. Ver la entrada sobre [disgrafía superficial y homófonos](../lectura/disgrafia-superficial-homofonos.md), donde el mismo sesgo conductual admite cuatro loci distintos según el nivel en que se resuelva.

---

## Distinciones que organizan el debate

### Type frequency vs token frequency

Distinción central propuesta por Bybee y adoptada por Tomasello:

- **Token frequency**: cuántas veces aparece un ítem concreto. *"-ed"* aparece, digamos, 50.000 veces en un corpus.
- **Type frequency**: con cuántos ítems distintos se combina. *"-ed"* se combina con 800 verbos distintos.

Para **productividad** (extender la regla a casos nuevos, tipo wug test), lo que importa es la **type frequency**. Para **automatización** (acceso rápido, *chunking*), la **token frequency**.

Tomasello argumenta que el niño aprende gramática vía type frequency creciente — no es que escuche muchas veces los mismos plurales, es que escucha muchos sustantivos distintos pluralizados. Esto es la base empírica del giro *usage-based* contra el innatismo: si se puede mostrar que los chicos extienden reglas en proporción a la type frequency observada, se debilita el argumento innatista.

### Frecuencia logarítmica vs lineal

El efecto de la frecuencia sobre tiempo de reacción es **logarítmico** (Whaley 1978; Murray & Forster 2004). La diferencia entre 10 y 100 ocurrencias es similar a la diferencia entre 1000 y 10000. Esto es compatible con:

- ACT-R (donde la fórmula tiene log explícito).
- SRN y conexionismo (que aprenden representaciones comprimidas y saturan al alto rango).
- Modelos probabilísticos (donde lo que importa es la sorpresa, que también es log).

Es **menos obvio** en modelos de ejemplares puros, que predicen efectos más lineales — esto es una crítica empírica al exemplarismo.

### Decaimiento — ¿la frecuencia se mantiene indefinidamente?

ACT-R dice que **sí, con decaimiento explícito** (la activación cae con el tiempo desde el último uso). Algunos PDP dicen que el conocimiento es **permanente** una vez aprendido (los pesos se quedan ahí). Modelos de ejemplares con olvido proponen una posición intermedia.

Datos empíricos: hay olvido pero también hay ***savings*** (re-aprender es más rápido que aprender de cero), sugiriendo que ni un extremo ni el otro. La representación no desaparece del todo cuando deja de usarse — algo queda.

### Probabilidad condicional vs frecuencia absoluta

Cuando se habla de "frecuencia" en parsing, casi siempre se quiere decir **frecuencia condicional**: P(estructura | verbo), no frecuencia bruta de la estructura. Esto es lo que mide [surprisal](surprisal.md): cuán improbable es el token dado el contexto previo. Cuanto más improbable, mayor sorpresa, mayor costo.

Surprisal es la formalización moderna más usada para operacionalizar "efectos de frecuencia" en el procesamiento. Conecta frecuencia con los [modelos predictivos](modelos-predictivos.md).

## El debate Tomasello / innatistas se libra acá

Una de las grandes peleas de la psicolingüística — ¿hay gramática innata o se aprende? — pasa fuertemente por **qué se hace con la frecuencia**:

- **Tomasello, Bybee, MacWhinney, conexionistas**: la frecuencia es suficiente para explicar el aprendizaje gramatical. El niño abstrae patrones a partir de exposición probabilística masiva. No hace falta gramática universal.
- **Pinker, dual-route, innatistas**: la frecuencia es necesaria pero no suficiente. Hay que postular **sesgos inductivos específicos** que decidan qué patrones extraer del input frecuencial. La frecuencia sola no explica la diferencia entre regulares e irregulares ni la productividad selectiva.
- **Yang (2002, 2016) — posición intermedia**: hay reglas, pero se aprenden probabilísticamente. La ***tolerance principle*** es una fórmula explícita: una regla es productiva si las excepciones son menos que **N / ln(N)** ítems en el rango cubierto. Cuantifica cuánta evidencia frecuencial se necesita para que el sistema abstraiga una regla. Reconcilia "hay reglas" con "se aprenden del input".

Esta pelea no se resuelve por argumento teórico — se resuelve (o no) empíricamente, mostrando dónde la frecuencia alcanza y dónde no.

## Conexión con LLMs

Los LLMs aprenden frecuencias **completamente implícitamente** en los pesos durante el entrenamiento — encajan en la familia 2 (pesos en redes neuronales). No tienen contadores explícitos. La frecuencia se "lee" de la probabilidad que asignan a tokens:

$$P(w_i \mid contexto) \approx \frac{frecuencia(w_i, contexto)}{frecuencia(contexto)}$$

matizado por capacidad de generalización (los LLMs no solo memorizan frecuencias brutas, abstraen patrones combinatorios).

**Problemas documentados**:

- **Frequency bias**: los LLMs son notablemente mejores con palabras y estructuras frecuentes del corpus de entrenamiento. Las palabras raras o las construcciones poco frecuentes activan representaciones más débiles.
- **Confusión memorización vs comprensión**: cuando se los evalúa en *targeted assessments* psicolingüísticos, parte del éxito puede ser "está prediciendo frecuencias del training, no entendiendo estructura". Esto se controla con baselines basados en frecuencia: ¿el modelo supera lo que se podría predecir solo con n-gramas? Si no, el "éxito" sintáctico es ilusorio.
- **Yedetore, Linzen et al. (2023)** muestran que entrenadas con cantidades de input comparables al humano (~10⁷ palabras), las redes no logran las generalizaciones que los niños hacen sin esfuerzo. Sugiere que la frecuencia sola — aun en cantidades realistas — **no basta** sin sesgos inductivos.

Esto es importante para el debate IA / neurociencia: la convergencia entre LLMs y humanos en sensibilidad a la frecuencia es real, pero **la fuente de la convergencia** puede ser distinta. En humanos hay aprendizaje frecuencial *más* sesgos. En LLMs hay aprendizaje frecuencial sobre **órdenes de magnitud más datos** sin sesgos específicos. Que produzcan resultados parecidos no implica mismo mecanismo.

## Conexiones en este sitio

- [Modelos predictivos](modelos-predictivos.md) — surprisal como formalización moderna del efecto de frecuencia condicional.
- [Modelos basados en memoria](modelos-basados-memoria.md) — ACT-R y la activación base como mecanismo explícito de frecuencia.
- [Modelos lexicalistas / conexionistas](modelos-lexicalistas.md) — la frecuencia como información léxica de primer nivel; pesos en redes neuronales como sustrato implícito.
- [Surprisal](surprisal.md) — la operacionalización dominante hoy.
- [Activación](activacion.md) — el sustrato común a varios de estos modelos; ahí está el modelo de logogen que acá se desarrolla como familia 5.
- [Disgrafía superficial y homófonos](../lectura/disgrafia-superficial-homofonos.md) — un caso clínico donde la pregunta "¿dónde vive la frecuencia?" tiene cuatro respuestas empíricamente separables.
- [La sílaba como unidad subléxica](../lectura/silaba-unidad-sublexical.md) — frecuencia silábica con signo inhibitorio frente a frecuencia de raíz con signo facilitatorio: la mejor demostración de que "frecuencia" no nombra una sola cosa.
- [Aprendizajes generales](../aprendizajes-generales.md) — la sección sobre autoorganización vs. big data discute si la frecuencia bruta alcanza.

## Referencias clave

- **Bybee, J. (1985)** *Morphology: A Study of the Relation Between Meaning and Form*. Benjamins. La fundación del enfoque basado en frecuencia y uso.
- **Bybee, J. (1995)** "Regular morphology and the lexicon" *Language and Cognitive Processes* 10(5):425-455.
- **Bybee, J. (2006)** "From usage to grammar: The mind's response to repetition" *Language* 82:711-733. Síntesis del programa.
- **Pierrehumbert, J. B. (2001)** "Exemplar dynamics: Word frequency, lenition, and contrast" en *Frequency and the Emergence of Linguistic Structure*. Benjamins. Modelo exemplarista para fonología.
- **Whaley, C. P. (1978)** "Word—nonword classification time" *Journal of Verbal Learning and Verbal Behavior* 17:143-154. El efecto logarítmico de la frecuencia.
- **Murray, W. S. & Forster, K. I. (2004)** "Serial mechanisms in lexical access: The rank hypothesis" *Psychological Review* 111:721-756. El efecto de rank, no de frecuencia bruta.
- **Anderson, J. R. (1993)** *Rules of the Mind*. Lawrence Erlbaum. Activación base en ACT-R.
- **Anderson, J. R. & Lebiere, C. (1998)** *The Atomic Components of Thought*. Lawrence Erlbaum.
- **MacDonald, M. C., Pearlmutter, N. J. & Seidenberg, M. S. (1994)** "The lexical nature of syntactic ambiguity resolution" *Psychological Review* 101:676-703.
- **Trueswell, J. C. & Tanenhaus, M. K. (1994)** "Toward a lexicalist framework for constraint-based syntactic ambiguity resolution" en *Perspectives on Sentence Processing*. Lawrence Erlbaum.
- **Tomasello, M. (2003)** *Constructing a Language: A Usage-Based Theory of Language Acquisition*. Harvard UP.
- **Yang, C. (2002)** *Knowledge and Learning in Natural Language*. Oxford UP.
- **Yang, C. (2016)** *The Price of Linguistic Productivity*. MIT Press. La *tolerance principle* formalizada.
- **Ellis, N. C. (2002)** "Frequency effects in language processing: A review with implications for theories of implicit and explicit language acquisition" *Studies in Second Language Acquisition* 24:143-188. Síntesis amplia.
- **Hay, J. & Baayen, R. H. (2005)** "Shifting paradigms: Gradient structure in morphology" *Trends in Cognitive Sciences* 9:342-348.
- **Morton, J. (1969)** "Interaction of information in word recognition" *Psychological Review* 76:165-178. El modelo de logogen; la frecuencia como umbral.
- **Forster, K. I. (1976)** "Accessing the mental lexicon" en *New Approaches to Language Mechanisms*. North-Holland. La frecuencia como orden de búsqueda.
- **McClelland, J. L. & Rumelhart, D. E. (1981)** "An interactive activation model of context effects in letter perception" *Psychological Review* 88:375-407.
- **Norris, D. (2006)** "The Bayesian Reader: explaining word recognition as an optimal Bayesian decision process" *Psychological Review* 113(2):327-357. La frecuencia como probabilidad previa.
- **Ratcliff, R. & McKoon, G. (2008)** "The diffusion decision model: theory and data for two-choice decision tasks" *Neural Computation* 20(4):873-922. Tasa de deriva vs. punto de partida.
- **Adelman, J. S., Brown, G. D. A. & Quesada, J. F. (2006)** "Contextual diversity, not word frequency, determines word-naming and lexical decision times" *Psychological Science* 17(9):814-823.
- **Cuetos, F. & Barbón, A. (2006)** "Word naming in Spanish" *European Journal of Cognitive Psychology* 18:415-436. Efectos independientes de edad de adquisición y frecuencia acumulada.
- **Davies, R., Barbón, A. & Cuetos, F. (2013)** "Lexical and semantic age-of-acquisition effects on word naming in Spanish" *Memory & Cognition* 41(2):297-311.
- **Carreiras, M., Mechelli, A. & Price, C. (2006)** "Effect of word and syllable frequency on activation during lexical decision and reading aloud" *Human Brain Mapping* 27(12):963-972. Frecuencia léxica y silábica con firmas neurales disociables.
- **Grill-Spector, K., Henson, R. & Martin, A. (2006)** "Repetition and the brain: neural models of stimulus-specific effects" *Trends in Cognitive Sciences* 10(1):14-23. Supresión por repetición.
- **Yedetore, A., Linzen, T. et al. (2023)** "How poor is the stimulus? Evaluating hierarchical generalization in neural networks trained on child-directed speech" *ACL*.
