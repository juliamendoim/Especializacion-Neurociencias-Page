# Unidades-t y cláusulas

Las **unidades de análisis** estándar para cuantificar **complejidad sintáctica** en producción discursiva. Son las "monedas" con las que se mide cuán complejas son las oraciones que produce un hablante (niño o adulto, con o sin trastorno).

## Cláusula

Una **cláusula** es una unidad con un **verbo y sus argumentos** (sujeto, complementos). Es el bloque básico del análisis sintáctico de discurso.

Una oración puede tener:

- **Una sola cláusula** → oración simple. *"El nene corre."*
- **Varias cláusulas** → oración compleja, donde una cláusula principal tiene cláusulas subordinadas anidadas. *"El nene **que vimos ayer** corre **cuando llueve**."* → 1 principal + 2 subordinadas = 3 cláusulas.

### Tipos de cláusula subordinada

- **Adjetivas** (relativas): *"el libro **que leí**"*
- **Sustantivas** (completivas): *"creo **que vendrá**"*
- **Adverbiales**: *"si llueve, no salgo"*, *"para que me escuches"*

Estas distinciones importan porque **cada tipo se desarrolla a edades diferentes**: las adverbiales aparecen antes que las sustantivas; las relativas de objeto son las últimas en consolidarse.

## Unidad-t (T-unit, unidad terminable)

Concepto introducido por **Kellogg Hunt (1965)** en su trabajo sobre desarrollo de la sintaxis en lenguaje escrito escolar. Una **unidad-t** es:

> Una cláusula independiente más todas las cláusulas subordinadas y modificadores que dependen de ella.

En otras palabras: la **mínima unidad que podría estar puntuada como oración separada**. La "T" viene de *terminable* — porque podría terminar.

### Ejemplos

- *"El nene corre."* → 1 unidad-t, 1 cláusula
- *"El nene corre y la nena salta."* → 2 unidades-t (cada una con 1 cláusula)
- *"El nene que vimos ayer corre."* → 1 unidad-t (con 2 cláusulas: principal + relativa)
- *"Cuando llueve, el nene corre, y la nena se queda."* → 2 unidades-t (la primera con 2 cláusulas, la segunda con 1)

### Por qué unidad-t y no oración

Hunt notó que **niños chicos producen muchas yuxtaposiciones con "y"** que son técnicamente una sola "oración" pero contienen varias estructuras independientes. Si contamos por oración, una concatenación larga con "y" se ve igual de "compleja" que una oración bien subordinada. La unidad-t corrige eso: separa lo que **podría haber sido una oración** independiente.

Para niños muy chicos (preescolar y antes), Brown (1973) propuso usar **"enunciado" (utterance)** en lugar de unidad-t, porque la puntuación todavía no es relevante.

## Índices de complejidad sintáctica

A partir de cláusulas y unidades-t se construyen las medidas:

### COMP-1 — Cláusulas por unidad sintáctica

```
COMP-1 = total de cláusulas / total de unidades-t (u oraciones)
```

- **Valor mínimo = 1** (cada unidad-t tiene 1 sola cláusula → solo oraciones simples).
- **Valor > 1** → hay subordinación. Cuanto más alto, más cláusulas subordinadas hay en promedio.

Es el **índice más usado** para medir madurez sintáctica general. Aumenta con la edad de manera consistente.

### COMP-2 — Subordinadas por oración compleja

```
COMP-2 = total de cláusulas subordinadas / total de oraciones complejas
```

Solo cuenta las oraciones que **tienen** subordinación. Mide **densidad de subordinación** dentro de las oraciones que ya son complejas.

- **Valor = 1** → cada oración compleja tiene exactamente 1 subordinada.
- **Valor > 1** → algunas oraciones complejas tienen 2 o más subordinadas anidadas.

### Índices secundarios

Los desagregan por tipo de subordinada:

- **COMP-2 Adj** = subordinadas adjetivas / oraciones complejas
- **COMP-2 Sust** = subordinadas sustantivas / oraciones complejas
- **COMP-2 Adv** = subordinadas adverbiales / oraciones complejas

Útiles porque **no todas las subordinadas se desarrollan al mismo ritmo**. Por ejemplo, en inglés las adjetivas (relativas) se relacionan más fuerte con la edad escolar que las adverbiales.

## Decisiones metodológicas críticas

Cuando un paper reporta análisis con unidades-t y cláusulas, conviene fijarse:

1. **¿Cuentan cláusulas no finitas?** Es decir: ¿cláusulas con infinitivo (*quiero **comer***), con gerundio (*siguió **caminando***), con participio (*la puerta **abierta***) cuentan como cláusulas?
2. **¿Qué hacen con las perífrasis verbales?** *"voy a comer"*, *"está corriendo"* — ¿son una cláusula o dos?
3. **¿Incluyen el discurso referido?** *"Dijo: 'estoy cansado'"* — ¿la cita cuenta como cláusula independiente?

Estas decisiones son **transparentes en buena investigación** y críticas para comparar resultados entre estudios. Un mismo discurso puede dar índices muy distintos según las decisiones de codificación.

## Por qué importan en investigación del desarrollo

- **A mayor edad, mayor COMP-1**: los niños emiten unidades cada vez más largas, con más cláusulas subordinadas. Es uno de los marcadores más robustos del desarrollo sintáctico.
- **Diferencias entre grupos**: chicos con TDL muestran COMP-1 significativamente menor que controles de su edad — incluso cuando otras medidas (vocabulario, MLU) son menos sensibles.
- **Diferencias entre géneros discursivos**: la narración suele exhibir más complejidad sintáctica que la conversación o el juego — por eso los recontados narrativos son una tarea predilecta para evaluar competencia gramatical.

## Aparición en Peñaloza et al. (2017)

El paper de **Peñaloza, Araya & Coloma** sobre desarrollo de complejidad sintáctica en recontados narrativos de niños chilenos hispanohablantes usa exactamente estos índices:

- COMP-1 (cláusulas por oración)
- COMP-2 (subordinadas por oración compleja)
- COMP-2 Adj, Sust y Adv (índices secundarios)

Compara dos grupos (preescolares vs. escolares de 1° básico) con [t de Student de una cola](../estadistica/t-de-student.md), encontrando que **todos los índices aumentan con la edad** — pero algunos lo hacen más bruscamente que otros, lo que marca cuáles construcciones se consolidan en qué momento del desarrollo.

## Lecturas clave

- **Hunt, K. (1965)** *Grammatical structures written at three grade levels*. NCTE Research Report. **El paper fundacional.**
- **Hunt, K. (1970)** "Syntactic maturity in schoolchildren and adults". *Monographs of the SRCD*.
- **Brown, R. (1973)** *A first language: The early stages*. Harvard UP. Para análisis de niños más chicos.
- **Jackson & Maldonado (2015)** "Sentence complexity in young children's narratives" — actualización para hispanohablantes.
- **Peñaloza, Araya & Coloma (2017)** — aplicación específica al español de Chile.
