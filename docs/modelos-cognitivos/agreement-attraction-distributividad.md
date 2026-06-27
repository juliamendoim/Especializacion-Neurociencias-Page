# Errores de concordancia (agreement attraction) y la lectura distributiva

La **attraction** o **atracción de concordancia** es un error sistemático que cometen tanto hablantes nativos como modelos computacionales del lenguaje: cuando el sujeto tiene un núcleo singular (N1) seguido de un complemento con nombre plural (N2), el verbo a veces concuerda con el N2 en lugar del N1. Es uno de los fenómenos más estudiados en psicolingüística contemporánea porque permite **diagnosticar la arquitectura del procesamiento sintáctico** — la atracción no debería existir si el parser fuera puramente estructural y modular.

## La estructura clásica

La forma canónica del experimento de attraction:

> *"La llave de las habitaciones está / **están** oxidada / **oxidadas**"*

| | Núcleo / controlador | Interferente / *attractor* | Verbo |
|---|---|---|---|
| **N1** | *la llave* (singular) | | |
| **N2** | | *las habitaciones* (plural) | |
| **Forma correcta** | controla concordancia | | *está oxidada* (singular) |
| **Forma con attraction** | (perdió control) | (gana concordancia) | ***están** oxidadas* (plural — error) |

El paper fundacional es **Bock & Miller (1991)** "Broken agreement" (*Cognitive Psychology* 23:45-93), que estableció la attraction como fenómeno robusto de la producción y disparó tres décadas de literatura sobre por qué ocurre.

## El puzzle: por qué la attraction no debería existir (pero existe)

Si el procesamiento del lenguaje funcionara como predice el [modelo generativo clásico](modelos-predictivos.md) (Frazier, Fodor), la concordancia debería ser un cómputo **estructural** entre sujeto y verbo, encapsulado, sin posibilidad de interferencia de otros constituyentes. El N2 está dentro del SP (sintagma preposicional) que modifica al N1 — no es el sujeto, no debería intervenir.

Y sin embargo:

- Los hablantes cometen attraction en tareas de producción inducida (Bock & Miller 1991, y cientos de replicaciones).
- Los oyentes notan menos los errores plurales-con-N2 plural que los plurales-con-N2 singular (Wagers, Lau & Phillips 2009) — la attraction modula la **comprensión**, no solo la producción.
- Las tasas de attraction varían sistemáticamente con propiedades del sujeto que **no son sintácticas**: número nocional, distributividad, animacidad, frecuencia de la combinación.

Este patrón es **incompatible con la modularidad estricta**. Es uno de los argumentos empíricos clásicos a favor de los [modelos lexicalistas / constraint-satisfaction](modelos-lexicalistas.md) y de los [modelos basados en memoria](modelos-basados-memoria.md): la concordancia se resuelve integrando múltiples fuentes de información, no por aplicación rígida de una regla estructural.

## La lectura distributiva — la pieza semántica clave

Un SN como *"la llave de las habitaciones"* admite **dos interpretaciones**:

### Lectura colectiva (no distributiva)

**Una sola llave** que abre todas las habitaciones. El N1 es genuinamente singular en el plano conceptual: hay 1 llave en el mundo. Ejemplo más claro: *"la madre de los chicos"* — una madre compartida.

### Lectura distributiva

**Una llave por cada habitación** — varias llaves, una asignada a cada miembro del conjunto denotado por N2. El N1 es morfológicamente singular pero **conceptualmente plural**: hay tantas llaves como habitaciones.

La lectura distributiva está disponible cuando la relación entre N1 y N2 admite esa interpretación uno-a-uno. Casos canónicos en español donde es muy natural:

- *"La etiqueta de los frascos"* (una etiqueta por frasco — distributiva por default)
- *"El nombre de los participantes"* (un nombre por participante)
- *"La página del libro"* en plural: *"la página de los libros"* (cada libro tiene su página)
- *"El sombrero de los niños"* (en contexto donde cada niño tiene el suyo)

Casos donde la colectiva domina:

- *"La capital del país"* (una capital por país, pero conceptualmente cada país tiene UNA — colectiva)
- *"La madre de los hermanos"* (típicamente colectiva)
- *"El director de los empleados"* (un director compartido)

## La predicción empírica central

**Cuando la lectura distributiva está disponible, los errores de attraction aumentan**. La razón es semántico-conceptual:

- En la lectura **colectiva**, el N1 es conceptualmente singular → el sistema mantiene el control de la concordancia con N1 sin esfuerzo, no se "deja arrastrar" por el N2 plural.
- En la lectura **distributiva**, el N1 es conceptualmente plural (aunque morfológicamente singular) → el sistema cognitivo ya tiene un rasgo de pluralidad activo asociado al N1 mismo → la interferencia del N2 se "alinea" con esa pluralidad nocional → el error de concordancia plural en el verbo se vuelve más probable **y semánticamente menos disonante**.

Esto se llama **número nocional** (*notional number*) o **número conceptual**, opuesto al **número morfológico** (lo que la palabra marca formalmente).

## El marco teórico: Marking and Morphing (Eberhard, Cutting & Bock 2005)

El modelo canónico actual es el **Marking and Morphing** de **Eberhard, Cutting & Bock (2005)** "Making syntactic sense out of nonsense" (*Psychological Review* 112:531-559). Proponen que la concordancia tiene **dos etapas separadas**:

### Etapa 1 — Marking

Se asigna un valor numérico al sujeto, basado en su **número nocional**. Esto integra:

- Morfología (singular/plural marcado en la palabra).
- Distributividad (la lectura distributiva agrega pluralidad nocional).
- Agregabilidad (objetos contables vs masas).
- Individuabilidad.

El resultado del marking no es binario singular/plural — es un **valor graduado** de pluralidad nocional. Un *"la llave de las habitaciones"* con lectura distributiva tiene valor de pluralidad **intermedio** (mayor que 0, menor que el de *"las llaves"* genuino).

### Etapa 2 — Morphing

Ese valor se traduce en la morfología del verbo. En esta etapa puede haber **interferencia del N2 plural** que se sumó al valor de marking del sujeto.

**La attraction emerge de la combinación**: cuando el marking del sujeto ya estaba "inclinado hacia el plural" por distributividad nocional, el morphing es más vulnerable a la interferencia plural del N2. La attraction no es un "error puro" sino una **consecuencia probabilística de cómo se computa el número en producción**.

## Otras variables que modulan attraction

Además de la distributividad:

- **Animacidad del N2**: N2 animado plural genera más attraction que N2 inanimado (Vigliocco et al. 1996).
- **Distancia lineal**: N2 más cercano al verbo aumenta attraction (efecto memoria, no estructural).
- **Frecuencia de la combinación N1+SP**: combinaciones poco frecuentes son más vulnerables.
- **Marca morfológica clara** en el N1: si el N1 es ambiguo (*"el análisis"* — masculino sg/pl), la attraction aumenta.
- **Carga de memoria**: bajo presión temporal o memoria de trabajo limitada, la attraction aumenta (Häussler & Bader 2009).

Todas estas variables son difíciles de acomodar para un parser modular puro. Encajan natural en [Lewis & Vasishth (2005)](modelos-basados-memoria.md) — *cue-based retrieval* con interferencia por similitud parcial.

## Cómo se explica desde los distintos modelos

| Modelo | Mecanismo propuesto |
|---|---|
| **Generativo clásico** (Frazier) | No tiene explicación natural. La attraction sería un "ruido" no predicho. |
| **Marking and Morphing** (Eberhard et al. 2005) | Dos etapas; distributividad modula marking; N2 interfiere en morphing. |
| **Lexicalista / constraint satisfaction** | Múltiples fuentes activan en paralelo; N2 plural compite con N1 por la concordancia del verbo. |
| **Basado en memoria** ([Lewis & Vasishth 2005](modelos-basados-memoria.md)) | Cue-based retrieval: la clave para el sujeto (+N, +sg) matchea parcialmente al N2 (+N), y por similitud parcial puede ganar. |
| **Predictivo** ([surprisal](surprisal.md)) | Si el contexto previo es compatible con un verbo plural, la surprisal del plural es menor → menos costo → más fácil "dejar pasar" el error. |

Wagers, Lau & Phillips (2009) "Agreement attraction in comprehension: Representations and processes" (*Journal of Memory and Language* 61:206-237) dieron evidencia experimental fuerte de que la attraction es un efecto **de retrieval** (al integrar la concordancia, no al codificar el sujeto), favoreciendo la cuenta basada en memoria.

## El caso del español

El español es particularmente rico para estudios de attraction porque:

- Es una lengua **pro-drop**: la concordancia verbal es muy informativa.
- Tiene **morfología flexiva rica** (número y persona marcados claramente en el verbo).
- Algunas combinaciones N1+SP son altamente distributivas por defecto.

**Vigliocco, Butterworth & Garrett (1996)** "Subject-verb agreement in Spanish and English: Differences in the role of conceptual constraints" (*Cognition* 61:261-298) compararon español e inglés. Hallazgo: el español muestra **más sensibilidad a restricciones conceptuales** (distributividad) que el inglés. Razón propuesta: la riqueza morfológica del español hace que el sistema preste más atención a la información nocional/semántica para producir formas correctas, así que la distributividad pesa más.

**Antón-Méndez, Nicol & Garrett (2002)** trabajaron sobre la interacción entre concordancia de género y número en español, mostrando que las restricciones de género (también presentes en español pero no en inglés) modulan los efectos de attraction.

## Conexión con TDL

Los chicos con [TDL](../tdl/index.md) muestran **tasas elevadas de errores de concordancia** en español, incluyendo attraction (Restrepo 1998; Bedore & Leonard 2001). Esto encaja con la cuenta basada en memoria: si la memoria fonológica de trabajo es débil ([markers psicolingüísticos](../tdl/markers-psicolinguisticos.md)), el sistema de retrieval del sujeto al momento del morphing del verbo es más vulnerable a la interferencia del N2 plural. La attraction es entonces uno de los marcadores morfosintácticos del TDL hispanohablante.

## Conexión con LLMs

Los LLMs también sufren attraction — y eso es teóricamente importante porque vincula directamente la psicolingüística con la evaluación de modelos:

- **Linzen, Dupoux & Goldberg (2016)** "Assessing the ability of LSTMs to learn syntax-sensitive dependencies" (*TACL*) midieron la attraction en LSTMs. Resultado: los LSTMs entrenados solo con next-token prediction aprenden mucha concordancia, pero **fallan de manera consistente** en estructuras con N2 plural interferente — igual que humanos.
- **Goldberg (2019)** "Assessing BERT's syntactic abilities" — mismo paradigma con BERT.
- **Linzen & Leonard (2018)** "Distinct patterns of syntactic agreement errors in recurrent networks and humans" — comparación fina: las redes muestran attraction, pero **el patrón** de cuándo fallan no replica perfectamente al humano. Las redes son más sensibles a la distancia lineal; los humanos, más sensibles a estructura jerárquica.

Esta línea de investigación es uno de los **mejores casos empíricos** para el debate humano vs LLM: ambos cometen los mismos tipos de error superficial, pero las **firmas finas de cuándo fallan** revelan diferencias mecánicas profundas.

## Conexiones en este sitio

- [Modelos basados en memoria](modelos-basados-memoria.md) — la attraction como caso canónico para Lewis & Vasishth (cue-based retrieval con interferencia por similitud).
- [Modelos lexicalistas / constraint satisfaction](modelos-lexicalistas.md) — la cuenta que mejor acomoda atracción modulada por información conceptual (distributividad, animacidad).
- [Modelos predictivos / surprisal](surprisal.md) — la attraction se puede leer como surprisal baja de la forma plural en contextos con N2 plural.
- [Memoria de trabajo](memoria-trabajo.md) — la attraction aumenta bajo carga de WM.
- [Markers psicolingüísticos del TDL](../tdl/markers-psicolinguisticos.md) — la concordancia es uno de los puntos vulnerables en TDL hispanohablante.

## Referencias clave

- **Bock, K. & Miller, C. A. (1991)** "Broken agreement" *Cognitive Psychology* 23:45-93. **El paper fundacional.**
- **Vigliocco, G., Butterworth, B. & Garrett, M. F. (1996)** "Subject-verb agreement in Spanish and English: Differences in the role of conceptual constraints" *Cognition* 61:261-298. **Comparación cross-lingüística clave; España como caso de alta sensibilidad conceptual.**
- **Vigliocco, G., Hartsuiker, R. J., Jarema, G. & Kolk, H. H. J. (1996)** "One or more labels on the bottles? Notional concord in Dutch and French" *Language and Cognitive Processes* 11:407-442. **El paper canónico sobre distributividad y attraction.**
- **Eberhard, K. M., Cutting, J. C. & Bock, K. (2005)** "Making syntactic sense out of nonsense: The marking and morphing of phrase number agreement" *Psychological Review* 112:531-559. **El modelo teórico de marking and morphing.**
- **Wagers, M. W., Lau, E. F. & Phillips, C. (2009)** "Agreement attraction in comprehension: Representations and processes" *Journal of Memory and Language* 61:206-237. **La evidencia experimental de attraction como efecto de retrieval.**
- **Franck, J., Vigliocco, G. & Nicol, J. (2002)** "Subject-verb agreement errors in French and English: The role of syntactic hierarchy" *Language and Cognitive Processes* 17:371-404.
- **Antón-Méndez, M. I., Nicol, J. L. & Garrett, M. F. (2002)** "The relation between gender and number agreement processing" *Syntax* 5:1-25.
- **Häussler, J. & Bader, M. (2009)** "Agreement checking and number attraction in sentence comprehension" *Memory and Cognition*.
- **Restrepo, M. A. (1998)** "Identifiers of predominantly Spanish-speaking children with language impairment" *Journal of Speech, Language, and Hearing Research* 41:1398-1411. Concordancia como marker en TDL hispanohablante.
- **Bedore, L. M. & Leonard, L. B. (2001)** "Grammatical morphology deficits in Spanish-speaking children with specific language impairment" *Journal of Speech, Language, and Hearing Research* 44:905-924.
- **Linzen, T., Dupoux, E. & Goldberg, Y. (2016)** "Assessing the ability of LSTMs to learn syntax-sensitive dependencies" *Transactions of the Association for Computational Linguistics* 4:521-535. **Attraction en LSTMs.**
- **Linzen, T. & Leonard, B. (2018)** "Distinct patterns of syntactic agreement errors in recurrent networks and humans" *CogSci*.
- **Goldberg, Y. (2019)** "Assessing BERT's syntactic abilities" arXiv:1901.05287.
