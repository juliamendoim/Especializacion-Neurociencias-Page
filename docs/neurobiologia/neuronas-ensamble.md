# Neuronas tipo ensamble (cell assemblies)

Concepto propuesto por **Donald Hebb** en 1949 en su libro *The Organization of Behavior*. Una de las ideas más influyentes de toda la neurociencia.

## Qué es

Una **neurona tipo ensamble** (o **cell assembly**, en inglés) es **un grupo de neuronas que se activan juntas** de forma sincronizada y que, por activarse repetidamente en conjunto, **quedan funcionalmente interconectadas** formando una unidad de procesamiento.

Hebb propuso que las representaciones mentales (conceptos, percepciones, recuerdos) **no viven en neuronas individuales** sino en **patrones distribuidos de actividad** sobre conjuntos de neuronas. No hay "una neurona de tu abuela" — hay un ensamble que codifica el concepto "abuela" cuando se activa coordinadamente.

## La regla de Hebb

La idea se resume en la frase célebre:

> *"Neurons that fire together, wire together."*
> *("Las neuronas que se activan juntas, se conectan entre sí.")*

Mecanismo:

1. Dos neuronas se activan al mismo tiempo por casualidad o por inputs correlacionados.
2. Las sinapsis entre ellas **se fortalecen** (mecanismo que después se identificó como **LTP** — potenciación a largo plazo).
3. Con activaciones repetidas, las dos neuronas se vuelven cada vez **más propensas a activarse juntas**.
4. Al cabo de muchas repeticiones, **una sola activa a la otra** automáticamente — forman un ensamble.

Esto es el **aprendizaje hebbiano**, sustrato fisiológico de la asociación, el condicionamiento, la formación de conceptos.

## Por qué es importante

### Conceptualmente

Resuelve un problema viejísimo: ¿cómo almacena el cerebro representaciones complejas sin tener "una neurona por concepto"? Respuesta: con **representaciones distribuidas** sobre ensambles que se reactivan.

### Empíricamente

La regla de Hebb se confirmó en los 70s con el descubrimiento de la **LTP** (Bliss & Lømo, 1973) — el mecanismo molecular concreto que fortalece sinapsis activadas en sincronía. Eso convirtió a Hebb de "filósofo de la mente" a "padre del aprendizaje sináptico".

### Computacionalmente

Las **redes neuronales artificiales** (incluyendo los LLMs) están construidas explícitamente sobre principios hebbianos:

- Las **conexiones se fortalecen** cuando dos unidades se activan correlacionadamente.
- Las **representaciones son distribuidas** sobre múltiples unidades, no localizadas.
- El **aprendizaje es ajuste de pesos** sinápticos, igual que el aprendizaje hebbiano.

Por eso a veces se dice que los LLMs son "máquinas de ensambles hebbianos a escala industrial".

## Cell assemblies vs. neurona "abuela"

Hay un debate histórico que conviene tener presente:

**Hipótesis de la neurona de la abuela** (Jerry Lettvin, 1969, en chiste): habría neuronas individuales especializadas en reconocer conceptos específicos — una neurona para tu abuela, otra para Jennifer Aniston, etc.

**Hipótesis del ensamble** (Hebb): no, las representaciones son distribuidas.

El consenso actual es **mixto**:

- Hay neuronas con **selectividad muy alta** (Quian Quiroga et al., 2005, encontraron neuronas en hipocampo humano que respondían específicamente a fotos de Jennifer Aniston o Halle Berry). Esto se llama **codificación sparse** — pocas neuronas, muy selectivas.
- Pero esas neuronas **no funcionan solas**: forman parte de ensambles más amplios.

Es decir: **el cerebro usa codificación distribuida con grados variables de sparseness**. Hebb tenía razón en lo grueso; Lettvin (en su chiste) acertó en que también hay selectividad alta.

## Conexión con conceptos contemporáneos

- **Sparse coding** (Hawkins, Ahmad — bibliografía U2 del seminario): formaliza la idea de ensambles con codificación distribuida pero sparse, donde solo un pequeño porcentaje de neuronas se activa para cada representación.
- **LTP / LTD** (programa U1): los mecanismos sinápticos que implementan la regla hebbiana.
- **Aprendizaje en redes neuronales artificiales**: los algoritmos de aprendizaje (incluyendo gradient descent en deep learning) son refinamientos del principio hebbiano.

## Lecturas

- **Hebb, D. O. (1949)** *The Organization of Behavior: A Neuropsychological Theory*. Wiley. **El libro fundacional.**
- **Bliss, T. V. P. & Lømo, T. (1973)** "Long-lasting potentiation of synaptic transmission in the dentate area of the anaesthetized rabbit following stimulation of the perforant path". *Journal of Physiology* 232:331-356. — descubrimiento de LTP.
- **Quian Quiroga, R. et al. (2005)** "Invariant visual representation by single neurons in the human brain". *Nature* 435:1102-1107. — las famosas "neuronas Jennifer Aniston".
- **Hawkins, J. & Ahmad, S. (2016)** "Why Neurons Have Thousands of Synapses". *Frontiers in Neural Circuits* 10. — interpretación contemporánea de cell assemblies.
