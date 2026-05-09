# Garden path sentences (oraciones de "vía muerta")

!!! note "Nombre en español"
    En la literatura hispanohablante se traduce como **"oraciones de vía muerta"** (a veces "oraciones laberinto" o "oraciones-trampa"). La metáfora del callejón sin salida ferroviario captura bien la idea: el parser entra por una vía que no llega a destino y tiene que retroceder.

## Qué son

Una **garden path sentence** — o **oración de vía muerta** — es una oración gramaticalmente correcta que **lleva al lector por un camino interpretativo que después resulta incorrecto**, forzándolo a **reanalizar** la estructura sintáctica al llegar a una palabra que rompe la lectura inicial.

El nombre original viene de la expresión inglesa *to lead someone down the garden path* — engañar a alguien dirigiéndolo por un camino atractivo pero falso. La traducción "vía muerta" mantiene el sentido del camino que no lleva a ninguna parte.

## Ejemplos clásicos en inglés

1. *"The horse raced past the barn **fell**."*
   El parser interpreta inicialmente *"The horse raced past the barn"* como una oración principal completa (el caballo corrió). Cuando aparece *"fell"*, no encaja → hay que reanalizar: *raced* era en realidad una **cláusula relativa reducida** (*the horse [that was] raced past the barn fell* = "el caballo [que fue] llevado a galope al lado del granero, cayó").

2. *"The old man the boats."*
   *Old* parece adjetivo y *man* sustantivo → "el hombre viejo". Pero al llegar a *"the boats"* la oración no cierra. Reanálisis: *"the old"* es un sintagma nominal ("los viejos") y *man* es **verbo** ("tripular"). "Los viejos tripulan los botes."

3. *"The complex houses married and single soldiers and their families."*
   *Complex* parece adjetivo modificando *houses* → "las casas complejas". Reanálisis: *the complex* es sujeto ("el complejo [habitacional]") y *houses* es el verbo ("aloja").

## Ejemplos en español

El español tiene menos garden paths clásicos por su flexión rica (los morfemas resuelven ambigüedades), pero hay casos:

- *"El periodista que entrevistó al político **renunció** ayer."*
  Ambigüedad sobre quién renunció: ¿el periodista o el político? El parser tiende a atribuir la cláusula al sustantivo más cercano (*late closure*), pero en español hay preferencia opuesta.

- *"María vio a la chica con el telescopio."*
  ¿María usó el telescopio para ver, o la chica tenía un telescopio? Ambigüedad de adjunción.

## Por qué importan en psicolingüística

Los garden paths son **ventana al parser humano en tiempo real**. Permiten ver:

1. **El parsing es incremental**: el cerebro asigna estructura sintáctica palabra por palabra, sin esperar al final de la oración.
2. **El parser usa heurísticas**: se compromete con la interpretación más simple/probable antes de tener toda la evidencia.
3. **La reanalysis tiene costo**: se mide en mayor tiempo de lectura, mayor amplitud de potencial evocado N400/P600, fijaciones oculares más largas.

### Principios clásicos del parser (Frazier)

- **Minimal attachment**: el parser construye la estructura sintáctica más simple posible (menos nodos).
- **Late closure**: prefiere adjuntar palabras nuevas al sintagma que está procesando, no a uno anterior.
- **Cuando estos principios fallan, hay garden path**.

## Garden paths en LLMs

Esto es lo bueno: **los LLMs también muestran garden path effects**, y es uno de los paralelos psicolingüísticos más estudiados de los últimos años.

### Qué se puede hacer

#### 1. Medir *surprisal* en el punto de disambiguación

La forma técnica de testear: calcular la **surprisal** (–log probabilidad) que asigna el LLM a la palabra que rompe la lectura inicial. Si el modelo procesa la oración como un humano, la surprisal en *"fell"* (en el ejemplo del caballo) debería ser **alta** comparada con la misma palabra en una oración no-ambigua (*"The horse that was raced past the barn fell"*). Eso es lo que se reporta en papers como **Wilcox et al. (2021)** y **Futrell et al. (2019)**.

Los LLMs **sí muestran ese pico de surprisal** en garden paths, aunque la magnitud varía con el tamaño del modelo y la frecuencia de la construcción.

#### 2. Engaño tipo "qué sigue"

Más informal pero ilustrativo: pedirle al LLM que **complete una garden path** truncada y ver qué interpretación adopta. Por ejemplo:

> Prompt: "*The old man the…*"
> Continuación esperada (interpretación garden path): "*…boats*" o similar (tomando *man* como verbo).
> Continuación errónea (interpretación inicial): "*…house was sad*" (tomando *man* como sustantivo).

Los LLMs grandes (GPT-4, Claude Opus, etc.) suelen reconocer el patrón porque las oraciones clásicas están en su corpus de entrenamiento. Los modelos chicos o entrenados con poco texto se enredan más.

#### 3. Pedirle que explique la oración

Otro test: dar una garden path completa y pedirle al LLM que **parafrasee o explique** quién hizo qué. Si la entendió, parafrasea bien. Si quedó "atrapado" en la lectura inicial, te da una explicación incoherente.

#### 4. Comparar con humanos

El experimento más interesante: dar la misma garden path a humanos (medir tiempos de reacción) y a LLMs (medir surprisal), y ver si **los puntos donde más cuesta la reanalysis coinciden**. La correlación humano-LLM es notable pero no perfecta — y las disociaciones son justamente lo que dice el campo sobre los sesgos inductivos específicos del humano.

### Por qué esto es relevante

Los garden paths son uno de los lugares donde **la analogía LLM-humano es más limpia**: en ambos sistemas hay una forma de "compromiso" probabilístico con la primera interpretación que requiere "revisión" cuando llega evidencia contradictoria. Pero los mecanismos subyacentes son distintos:

- En el humano, la reanalysis es un **proceso costoso** que implica desbaratar la estructura ya construida.
- En el LLM, no hay "desbaratar" — la siguiente palabra simplemente tiene baja probabilidad porque el modelo ya estaba apostando por otra continuación. **No hay una "estructura sintáctica" interna que reanalizar**, solo distribuciones probabilísticas que se actualizan.

Esa asimetría es uno de los argumentos para sostener que los LLMs **simulan** procesamiento sintáctico sin **tenerlo** en el sentido representacional fuerte.

## Lecturas recomendadas

- **Frazier, L. (1987)** "Sentence processing: A tutorial review" — el clásico sobre minimal attachment / late closure.
- **Wilcox, Levy, Morita & Futrell (2018-2021)** — varios papers usando LLMs para testear teorías psicolingüísticas, incluidos garden paths.
- **van Schijndel & Linzen (2021)** "Single-stage prediction models do not explain the magnitude of syntactic disambiguation difficulty" — discute por qué LLMs subestiman el costo de reanalysis humano.
- **Futrell, R., Wilcox, E., et al. (2019)** "Neural language models as psycholinguistic subjects" — review de cómo se usan LLMs para testear hipótesis psicolingüísticas.
