# El español como lengua fusional

El español es una lengua **fusional** (también llamada **inflectiva** o **sintético-fusional**). Esta clasificación tipológica tiene consecuencias directas para cómo se adquiere, cómo se procesa, cómo se rompe en trastornos del lenguaje y cómo lo manejan los LLMs.

## Las cuatro grandes categorías tipológicas

| Tipo | Característica | Ejemplos |
|---|---|---|
| **Aislante / analítico** | 1 morfema = 1 palabra. La gramática se construye con orden de palabras y partículas. | Chino mandarín, vietnamita, inglés moderno (parcialmente) |
| **Aglutinante** | Morfemas pegados uno detrás de otro, cada uno con **una función clara y separable**. | Turco, finlandés, húngaro, japonés, quechua, suajili |
| **Fusional / inflectivo** | Un solo morfema **fusiona varias categorías gramaticales** a la vez. No se pueden separar. | Español, latín, italiano, ruso, alemán, griego |
| **Polisintético** | Una sola palabra compleja equivale a una oración completa de otras lenguas. | Inuktitut, mohawk, mapuche |

Importante: **estas categorías no son puras**. Casi todas las lenguas tienen rasgos de varios tipos. La clasificación apunta al **rasgo dominante**.

## Por qué el español es fusional

Mirá un sufijo verbal típico: **-amos** en *comemos*.

Ese único morfema **/-amos/** codifica simultáneamente:

- **Persona**: 1ª
- **Número**: plural
- **Tiempo**: presente
- **Modo**: indicativo
- **Aspecto**: imperfectivo
- **Conjugación**: 2ª (verbos en *-er*)

No se puede descomponer en piezas separables. Es **un morfema con seis significados fusionados** dentro.

### Comparación con una lengua aglutinante

En turco, para decir *"no podíamos venir"* se usa algo como *gel-eme-di-k*, donde cada sílaba marca una categoría aislada:

- *gel-* = raíz "venir"
- *-eme-* = imposibilidad / negación
- *-di-* = pasado
- *-k* = 1ª plural

Identificable, separable, modular. **Cada sufijo es una pieza independiente con una función única.**

En español, en cambio, esas mismas categorías se fusionan en sufijos no descomponibles. Decir *"podíamos"* requiere acceder a una forma fusional completa, no a una secuencia de morfemas modulares.

### Comparación con una lengua aislante

En chino mandarín, las categorías se expresan con **palabras separadas o partículas**:

- *wǒ* = "yo"
- *chī* = "comer"
- *le* = partícula de aspecto perfectivo

Una oración como *"yo comí"* es *wǒ chī le* — tres palabras, tres morfemas, ninguna fusión. La raíz *chī* nunca cambia de forma.

## Por qué importa esta tipología

### Adquisición del lenguaje

- En **lenguas aglutinantes**, los chicos aprenden los morfemas de a uno (más fácil de aislar perceptualmente).
- En **lenguas fusionales** como el español, el chico tiene que aprender que *-amos* es una unidad **indivisible** que codifica varias cosas a la vez. Eso hace que la morfología verbal del español sea más difícil de "desempaquetar", pero una vez aprendida es **muy productiva** — el chico puede generar miles de formas a partir de pocos paradigmas.

### TDL morfosintáctico

Las lenguas fusionales rompen **distinto** cuando hay TDL.

- En **inglés** (más aislante en su morfología verbal), el TDL se manifiesta como **omisiones**: *"he go"* en vez de *"he goes"*, *"yesterday I walk"* en vez de *"I walked"*.
- En **español**, donde no se puede simplemente "omitir" un sufijo (la raíz aislada no es palabra), el TDL se manifiesta como **sustituciones** entre formas: *"comió"* por *"comía"*, *"come"* por *"coma"*, errores de concordancia de género (*"el casa"*).

Por eso **Bedore & Leonard (2005)** muestran que los marcadores de TDL en español son distintos de los del inglés. El test diagnóstico tiene que adaptarse a la tipología.

### LLMs

Las lenguas fusionales son **sistemáticamente más difíciles para los LLMs** que las aislantes.

- Un verbo regular español tiene 50+ formas flexivas (*como, comes, come, comemos, coméis, comen, comía, comías…* y así para cada tiempo y modo).
- Cada forma es potencialmente un **token distinto** para el sistema de tokenización (BPE, SentencePiece).
- El espacio combinatorio explota: un mismo lema español ocupa decenas de tokens, mientras que uno en inglés ocupa 4-5.
- Resultado: los LLMs **rinden notablemente peor** en español que en inglés en tareas morfológicas, **incluso cuando tienen mucho texto en español en su corpus**.

### Producción vs. comprensión

Como el español fusiona muchas categorías en cada forma, los chicos pueden **comprender** una distinción gramatical (oír *"comió"* vs *"comía"* y entender la diferencia aspectual) **antes** de poder **producir** las dos formas correctamente.

- La comprensión solo requiere **reconocer** la diferencia entre dos formas.
- La producción requiere **generar el morfema fusional correcto**, lo que implica acceder a un paradigma con muchas alternativas y elegir bien.

Esa asimetría es típica de lenguas fusionales y **mucho más marcada que en lenguas aislantes**, donde producción y comprensión tienden a ir más acopladas.

## Conexión con otros conceptos

- **[Buffer fonológico](../modelos-cognitivos/buffer-fonologico.md)**: las lenguas fusionales producen palabras más largas en promedio, lo que **carga más el buffer**. Errores morfológicos en TDL pueden estar mediados por límites de buffer, no solo por reglas mal aprendidas.
- **[ITPA — Integración gramatical](../evaluacion/itpa.md)**: el subtest de morfología flexiva del ITPA aprovecha justamente la riqueza fusional del español para detectar TDL.
- **[Unidades-t y cláusulas](../medidas-linguisticas/unidades-t-y-clausulas.md)**: la complejidad sintáctica medida en español refleja, parcialmente, la riqueza fusional — porque cada cláusula carga mucha información gramatical en pocas palabras.

## Lecturas recomendadas

- **Comrie, B. (1989)** *Language Universals and Linguistic Typology*. Blackwell. El manual clásico.
- **Whaley, L. J. (1997)** *Introduction to Typology*. Sage. Más accesible.
- **Bedore, L. & Leonard, L. (2005)** "Verb inflections and noun phrase morphology in Spanish-speaking children with SLI" — para la diferencia tipológica del TDL.
