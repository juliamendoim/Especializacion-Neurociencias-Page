# Memoria de trabajo y memoria de corto plazo

Conceptos centrales para entender los modelos cognitivos del lenguaje, los déficits en TDL, y por qué procesar oraciones complejas tiene costo. Conviene tener clara la distinción entre los dos términos antes de avanzar.

## STM vs. WM — la distinción

**Memoria de corto plazo (STM, *short-term memory*)**: capacidad **pasiva** de mantener información disponible por un período corto (segundos), sin manipularla. Es el "repetir un número de teléfono mientras se marca".

**Memoria de trabajo (WM, *working memory*)**: capacidad de **mantener y manipular** información simultáneamente. Es el "repetir el número de teléfono y a la vez decirlo al revés".

La distinción la formalizaron **Baddeley y Hitch (1974)** y reemplazó al modelo más simple de Atkinson & Shiffrin (1968), que solo postulaba un "almacén de corto plazo" pasivo. La working memory es **activa, controlada y limitada en capacidad**.

En la práctica, los términos se usan a veces como sinónimos en literatura aplicada, pero conviene tenerlos diferenciados teóricamente.

## El modelo de Baddeley (1986, 2000)

Es el marco dominante en psicolingüística. Postula varios componentes:

```
                   ┌──────────────────────┐
                   │  Ejecutivo central   │  ← atención, control
                   └─────────┬────────────┘
                             │
       ┌─────────────────────┼─────────────────────┐
       │                     │                     │
       ▼                     ▼                     ▼
┌──────────────┐   ┌──────────────────┐   ┌────────────────┐
│ Bucle        │   │ Agenda           │   │ Buffer         │
│ fonológico   │   │ visuoespacial    │   │ episódico      │
│ (verbal)     │   │ (visual)         │   │ (integrador)   │
└──────────────┘   └──────────────────┘   └────────────────┘
```

- **Ejecutivo central**: gestiona la atención, decide en qué subsistema procesar.
- **Bucle fonológico**: el sistema clave para el lenguaje. Mantiene info verbal-acústica.
- **Agenda visuoespacial**: para imágenes, escenas espaciales.
- **Buffer episódico** (agregado en 2000): integra info de los otros y la conecta con memoria de largo plazo.

## El bucle fonológico (phonological loop)

Es **el componente que más nos importa** porque es donde "vive" el lenguaje en el procesamiento de corto plazo. Tiene dos subcomponentes:

| Subcomponente | Función |
|---|---|
| **Almacén fonológico** (pasivo) | Guarda información verbal-acústica por unos 2 segundos. Sin rehearsal, decae. |
| **Repaso articulatorio** (activo) | Re-articula subvocálicamente lo guardado para refrescarlo (mecanismo "loop"). |

**Capacidad**: aproximadamente 2 segundos de articulación. Por eso podés mantener ~7 dígitos cortos en inglés, pero menos cuando los dígitos son palabras largas (en galés, donde los nombres de los dígitos son más largos, la gente recuerda menos).

### Tres efectos clásicos del bucle fonológico

1. **Efecto de longitud de palabra (Word length effect)**: palabras más largas → menos ítems retenidos. Porque cada palabra ocupa más tiempo de articulación.

2. **Efecto de similitud fonológica (Phonological similarity effect)**: palabras que suenan parecido (*man, cap, hat, mat*) son más difíciles de mantener juntas que palabras distintas (*pen, day, cow, sun*). Porque se confunden en el almacén fonológico.

3. **Efecto de habla irrelevante (Irrelevant speech effect)**: si hay habla de fondo (aunque sea en un idioma desconocido), interfiere con el rehearsal. Música o ruido blanco interfieren menos.

Estos tres efectos son la **firma diagnóstica** de que el bucle fonológico existe como sistema separado.

## Por qué importa esto en TDL

Una de las hipótesis más fuertes sobre la etiología del TDL es **el déficit de memoria fonológica de corto plazo**. La idea es:

> Los chicos con TDL tienen **un bucle fonológico deficiente**, lo que limita su capacidad de mantener secuencias fonológicas el tiempo suficiente para **extraer patrones morfosintácticos** del input.

Esto explicaría por qué los chicos con TDL:

- Fallan en concordancia: no logran mantener el sujeto en mente hasta que llega el verbo.
- Tienen vocabulario más pobre: el "fast mapping" (asociar palabra nueva a referente) requiere mantener la forma fonológica brevemente, y eso está comprometido.
- Tienen morfología pobre: para abstraer un morfema como /-aba/ del input, hay que oírlo varias veces y compararlo con otras formas en memoria.
- Tienen comprensión sintáctica débil para oraciones largas: no pueden mantener el inicio mientras procesan el final.

### El non-word repetition test (NWR) como marker de TDL

**Conti-Ramsden, Botting & Faragher (2001)** mostraron que la **repetición de no-palabras** es uno de los markers más sensibles y específicos de TDL.

La tarea: el examinador dice una pseudopalabra (*"pristoplán"*, *"berfucadelo"*) y el chico tiene que repetirla.

Por qué funciona como marker:

- No-palabras **no se pueden apoyar en memoria de largo plazo** (no hay representación léxica).
- Solo se puede repetir si el bucle fonológico mantuvo la secuencia íntegra.
- Si el bucle es débil, **la longitud de la pseudopalabra colapsa el rendimiento**.
- Chicos con TDL puntúan dramáticamente bajo en pseudopalabras de 4+ sílabas, aun cuando su lenguaje espontáneo parece comparable a controles.

El NWR está incorporado en baterías como el **[CELF](../evaluacion/celf.md)** y se usa en investigación hispanohablante adaptado al español (Aguado, Mendoza, Acosta).

## Memoria de trabajo y procesamiento sintáctico

La WM no solo afecta retención fonológica, también **el costo de procesar estructuras complejas**:

- **Dependencias de larga distancia**: para entender *"El nene **que la nena** **abrazó** se rió"*, hay que mantener "el nene" en mente hasta que llega "se rió", a través de la cláusula intermedia. Eso carga memoria de trabajo.
- **[Garden paths](garden-paths.md)**: la reanalysis requiere "deshacer" una estructura ya construida y mantener material en mente para rearmar.
- **Center embedding**: oraciones tipo *"el gato que el perro que la rata mordió persiguió huyó"* son técnicamente gramaticales pero exceden la capacidad de WM humana.

**Caplan & Waters (1999)** propusieron que hay un **recurso de WM específico para sintaxis** separado del WM general. La idea es controvertida pero ha generado mucha literatura.

**Lewis & Vasishth (2005)** propusieron una alternativa: el costo de procesar estructuras complejas no es por capacidad limitada, sino por **interferencia entre representaciones similares** que se solapan en la memoria. Su modelo (basado en ACT-R) compite teóricamente con la teoría de surprisal de Levy.

## Conexión con LLMs

Los LLMs no tienen "memoria de trabajo" en el sentido cognitivo, pero tienen un análogo: la **ventana de contexto**. Es la cantidad de tokens previos que el modelo puede "ver" al predecir el siguiente.

- Modelos clásicos: 512-2048 tokens.
- Modelos modernos: 32K, 128K, hasta 1M tokens.

Diferencias críticas con WM humana:

- La ventana del LLM es **pasiva** (todos los tokens están igualmente "presentes") mientras que la WM humana es **activa** (la atención privilegia ciertos elementos sobre otros).
- La ventana no decae con el tiempo. La WM humana sí.
- La ventana no sufre **interferencia** entre ítems similares. La WM humana sí (efecto de similitud fonológica).
- La ventana puede ser enormemente más grande que la WM humana (~7 ítems).

Por eso **los LLMs procesan center embeddings y oraciones de varias líneas sin esfuerzo**, mientras que los humanos colapsan. Esa asimetría es uno de los argumentos para sostener que **los LLMs no son modelos directos del procesamiento humano** — al menos no a nivel de capacidad de mantenimiento.

## Conexión con otros conceptos

- **[Buffer fonológico de salida](buffer-fonologico.md)**: el buffer es parte del bucle fonológico (la pieza de **producción**). El bucle es más amplio: incluye almacén de input + rehearsal + interfaces con léxico.
- **[Activación](activacion.md)**: la WM se entiende parcialmente como activación residual de unidades léxicas / fonológicas. Se mantienen activas mientras no llegue input que las apague.
- **[Garden paths](garden-paths.md)**: el costo de reanalysis es, en parte, costo de WM.
- **[ITPA — memoria secuencial](../evaluacion/itpa.md)**: el subtest mide directamente la capacidad del bucle fonológico (repetición de dígitos).
- **[CELF — Working Memory Index](../evaluacion/celf.md)**: incluye repetición de oraciones y de pseudopalabras, los dos markers clásicos.

## Lecturas recomendadas

- **Baddeley, A. (1986)** *Working Memory*. Oxford UP. El libro fundacional.
- **Baddeley, A. (2000)** "The episodic buffer: A new component of working memory?" *TICS* 4(11):417-423. La actualización del modelo.
- **Gathercole & Baddeley (1996)** "Children's Test of Nonword Repetition" — el test estándar.
- **Conti-Ramsden, Botting & Faragher (2001)** "Psycholinguistic markers for SLI" — el paper que consolidó NWR como marker. **Está en U5 complementaria.**
- **Caplan & Waters (1999)** "Verbal working memory and sentence comprehension". *BBS* 22:77-94. Hipótesis del recurso específico para sintaxis.
- **Lewis & Vasishth (2005)** "An activation-based model of sentence processing as skilled memory retrieval". *Cognitive Science* 29:375-419. Alternativa basada en interferencia.
