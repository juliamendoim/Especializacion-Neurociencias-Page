# Disgrafía superficial y la elección entre homófonos

Cuando un paciente con disgrafía superficial tiene que escribir al dictado una palabra que suena igual que otra —*casa* o *caza*— y el contexto no alcanza para desambiguar, **algo tiene que decidir**. Esa decisión no es aleatoria, y de dónde venga el sesgo dice mucho sobre qué componente del sistema quedó dañado.

Esta entrada desarrolla el problema, los cuatro lugares donde podría vivir esa preferencia, y cómo se separan experimentalmente.

---

## 1. El español es transparente para leer y opaco para escribir

Es la asimetría que organiza todo el cuadro, y suele enunciarse mal. La ortografía del español se describe como "transparente", pero eso vale sobre todo **en dirección lectura**: dada una secuencia de letras, la pronunciación es casi siempre derivable por reglas.

En **dirección escritura** la relación es de uno a muchos:

| Fonema | Grafemas posibles | Ejemplos |
|---|---|---|
| /s/ (con seseo) | ⟨s⟩, ⟨c⟩, ⟨z⟩ | *casa*, *cocer*, *caza* |
| /b/ | ⟨b⟩, ⟨v⟩ | *bello*, *vello* |
| /x/ | ⟨j⟩, ⟨g⟩ | *jinete*, *gitano* |
| /ʝ/ (con yeísmo) | ⟨y⟩, ⟨ll⟩ | *cayó*, *calló* |
| ∅ | ⟨h⟩, nada | *hola*, *ola* |

La vía fonema-grafema **está obligada a elegir**, y no tiene con qué. De ahí que en español la disgrafía superficial sea un cuadro mucho más visible y mejor documentado que la alexia de superficie: la opacidad está del lado de la escritura.

### El seseo importa para el diseño

En las variedades con **seseo** —toda América y buena parte del sur peninsular— /s/ y /θ/ están fusionadas, así que *casa* y *caza* son **homófonos plenos**. En español peninsular centro-norte no lo son (/ˈkasa/ vs. /ˈkaθa/) y el par no sirve como estímulo.

Lo mismo vale para el **yeísmo** con *cayó* / *calló*, *haya* / *halla*. Cualquier batería de homófonos tiene que declarar la variedad para la que fue construida; un ítem válido en Buenos Aires o Bogotá puede no serlo en Valladolid.

---

## 2. Qué es la disgrafía superficial

En los [modelos de doble ruta](../modelos-cognitivos/dual-ruta-lectura.md) aplicados a la escritura, hay una **vía léxica** (recuperar la forma ortográfica almacenada de una palabra conocida) y una **vía subléxica** de conversión fonema-grafema.

La **disgrafía superficial** es el patrón que resulta de un daño en la vía léxica con la subléxica preservada:

- Escritura correcta de **pseudopalabras** y de palabras de ortografía predecible.
- Fallas en palabras de **ortografía arbitraria** — aquellas donde la grafía no se deriva de la pronunciación (*vaca*, *hola*, *cerveza*, *guisqui*).
- Errores **fonológicamente plausibles**: *berbo* por *verbo*, *curba* por *curva*, *ola* por *hola*. Lo escrito, leído en voz alta, suena bien.
- **Efecto de frecuencia**: las palabras de baja frecuencia se pierden primero. Es la firma de un léxico degradado, no de un léxico ausente.

Ese último punto ya es una respuesta parcial: **sí, hay efecto de frecuencia en la disgrafía superficial**, y está bien documentado. La pregunta fina es de qué frecuencia se trata.

---

## 3. Los cuatro lugares donde podría vivir la preferencia

Ante /ˈkasa/ sin contexto, un sesgo hacia ⟨s⟩ puede originarse en cuatro sitios distintos, que hacen predicciones distintas:

| Locus | Qué es | Qué predice |
|---|---|---|
| **1. Contingencia fonema-grafema** | P(⟨s⟩ \| /s/) es mucho mayor que P(⟨z⟩ \| /s/) en el léxico del español | Sesgo hacia ⟨s⟩ **independientemente de cuál sea la palabra target**, y presente también en **pseudopalabras** |
| **2. Frecuencia léxica del homófono** | *casa* es mucho más frecuente que *caza* | Errores **asimétricos**: *caza* → "casa" mucho más que a la inversa. **Ausente en pseudopalabras** |
| **3. Consistencia de vecindario** | Cómo se escribe el cuerpo *-asa* / *-aza* en el resto del léxico | Efecto de grano intermedio, sensible a la rima y no al fonema aislado |
| **4. Restricción posicional** | ⟨z⟩ ante *e*, *i* es prácticamente ilegal en español (corresponde ⟨c⟩) | No es frecuencia sino ortotaxis, pero **contamina** a las tres anteriores si no se controla |

Los loci 1 y 2 son los teóricamente interesantes porque pertenecen a **rutas distintas**: el primero es subléxico, el segundo es léxico residual.

### El test que los separa

**Dictar pseudopalabras** que contengan el fonema ambiguo: /ˈtosa/, /ˈmuza/, /ˈpeza/.

- Si el sesgo hacia ⟨s⟩ **persiste** en pseudopalabras → es contingencia subléxica (locus 1), porque no hay entrada léxica que pueda estar sesgando nada.
- Si el sesgo **desaparece** → era frecuencia léxica (locus 2).

Lo más probable es que ambos efectos existan y se sumen. El valor del diseño no es elegir un ganador sino **estimar el peso de cada uno por separado**.

Un control necesario: emparejar los pares de homófonos por **razón de frecuencia**. Si la tasa de error escala con esa razón, el locus 2 está operando; si es plana, no.

---

## 4. Por qué el contexto reducido es la manipulación crítica

Presentar la palabra sin contexto no simplifica la tarea: **fuerza al sistema a exhibir su sesgo de base**.

El **Bayesian Reader** (Norris, 2006) lo formula explícitamente: los efectos de frecuencia son *una especie de efecto de predictibilidad que aparece cuando el contexto está ausente o no restringe*. La frecuencia funciona como **probabilidad previa**, y el prior solo domina cuando la evidencia no alcanza.

De ahí una predicción directa y testeable: con contexto semánticamente restrictivo ("el cazador salió de ___"), un paciente con semántica preservada debería resolver por vía léxico-semántica y el efecto de frecuencia debería **achicarse o desaparecer**. La interacción **contexto × frecuencia** es en sí misma el resultado, más informativa que cualquiera de los dos efectos por separado.

---

## 5. Dos subtipos, y cómo mapean sobre los loci

La literatura distingue dos maneras de llegar a un cuadro de disgrafía superficial, y **cada una predice un locus distinto**:

**Léxico ortográfico degradado**
: Las representaciones ortográficas se perdieron o se debilitaron. El paciente cae en la vía fonema-grafema. Manda la **contingencia subléxica** (locus 1). Los errores no tienen por qué ser palabras existentes.

**Léxico preservado pero desconectado de la semántica**
: Las representaciones ortográficas están, pero sin información semántica el sistema no puede elegir cuál corresponde. Manda la **frecuencia léxica** (locus 2). Los errores son **palabras existentes** — típicamente el homófono.

Esta distinción se formuló para el inglés como *"to bee but not to bea"*: en el subtipo por desconexión, el error ante */biː/* es *be* (palabra) y no *bea* (pseudopalabra ortográficamente plausible), porque el léxico intacto sigue sosteniendo formas reales aunque no sepa cuál elegir.

**La consecuencia diagnóstica**: un paciente que ante *caza* escribe *casa* —una palabra— y no *cassa* o *caça*, está mostrando un léxico que funciona pero no puede consultarse desde el significado. El tipo de error importa tanto como la tasa.

---

## 6. ¿La elección es aleatoria o proporcional a la frecuencia?

Formulada así, la pregunta admite dos modelos extremos:

- **Selección aleatoria**: entre los grafemas legales para ese fonema, se elige uno al azar.
- **Selección pesada**: se elige en proporción a la contingencia sonido-grafía.

Un estudio que testeó ambos con simulaciones de Monte Carlo sobre el rendimiento de un paciente encontró un resultado **intermedio**: la selección aleatoria *subestima* sus correspondencias correctas, mientras que la selección pesada *predice más de las que produce*. Ni azar puro ni proporcionalidad perfecta.

Esto encaja con la idea general de un sistema de mapeos **probabilísticos y graduados** —listas de grafías alternativas ordenadas por contingencia— más que con un sistema de reglas categóricas con excepciones.

---

## 7. Qué mirar en una evaluación

Para que el patrón sea interpretable, la batería tiene que permitir estas comparaciones:

1. **Palabras de ortografía arbitraria vs. predecible**, emparejadas en frecuencia y longitud.
2. **Pseudopalabras** con fonemas ambiguos — separa vía subléxica de léxica.
3. **Pares de homófonos** con razón de frecuencia conocida y controlada.
4. **Contexto reducido vs. contexto restrictivo** para el mismo ítem.
5. **Tipo de error**, no solo tasa: ¿el error es una palabra existente o una pseudopalabra plausible?
6. Control de la **variedad dialectal** del paciente: sin seseo, media batería de homófonos deja de ser homófona.

---

## Cómo se conecta con otros conceptos

- **[Modelo dual-ruta de lectura](../modelos-cognitivos/dual-ruta-lectura.md)** — el mismo marco aplicado a la escritura; la asimetría lectura/escritura del español es lo que vuelve esta patología más visible en esta lengua.
- **[Frecuencia y cómo se representa mentalmente](../modelos-cognitivos/frecuencia.md)** — la pregunta de fondo: si hay un efecto de frecuencia, ¿dónde está almacenada esa frecuencia? Los cuatro loci de esta entrada son cuatro respuestas distintas.
- **[La sílaba como unidad subléxica](silaba-unidad-sublexical.md)** — el mismo debate sobre el tamaño de la unidad, del lado de la lectura.
- **[Buffer fonológico](../modelos-cognitivos/buffer-fonologico.md)** — un daño en el buffer grafémico produce un patrón distinto: efectos de longitud y errores de posición de letra, no errores fonológicamente plausibles. Es el diagnóstico diferencial.
- **[Constructivismo y palabra generadora](constructivismo-palabra-generadora.md)** — la ortografía arbitraria es justamente lo que el nivel alfabético no resuelve: los problemas que quedan después ya no son conceptuales sino ortográficos.

---

## Referencias de entrada

- Norris, D. (2006). The Bayesian Reader: explaining word recognition as an optimal Bayesian decision process. *Psychological Review*, 113(2), 327-357.
- Friedmann, N. et al. (2023). Two types of developmental surface dysgraphia: to bee but not to bea. *Cognitive Neuropsychology*, 40(5-6).
- Cuetos, F. (1998). *Evaluación y rehabilitación de las afasias*. Panamericana. (Caso con disgrafía superficial en español: *curba* por *curva*.)
- Cuetos, F. (1991). *Psicología de la escritura*. Escuela Española.
- Ellis, A. W. (1982). Spelling and writing (and reading and speaking). En A. W. Ellis (Ed.), *Normality and Pathology in Cognitive Functions*. Academic Press.
- Beauvois, M. F. & Dérouesné, J. (1981). Lexical or orthographic agraphia. *Brain*, 104(1), 21-49.
- Rapp, B. & Caramazza, A. (1997). From graphemes to abstract letter shapes: levels of representation in written spelling. *Journal of Experimental Psychology: Human Perception and Performance*, 23(4), 1130-1152.
- Iribarren, C., Jarema, G. & Lecours, A. R. (2001). Two different dysgraphic syndromes in a regular orthography, Spanish. *Brain and Language*, 77(2), 166-175.
