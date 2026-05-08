# Activación

"Activación" es la **moneda corriente** de los modelos cognitivos: es la cantidad de "energía" o "fuerza" con que una unidad mental (un fonema, un grafema, un lexema, un concepto) está siendo procesada en un momento dado. Es un término metafórico, pero tiene definiciones operacionales concretas en los modelos formales.

## Cómo funciona la activación

En modelos como el **DRC** (que es la **C** de *Dual-Route Cascaded*), el sistema se concibe como una **red de unidades interconectadas** — cada nivel (rasgo visual, letra, palabra, fonema) es un conjunto de unidades. Cuando ves una palabra:

1. **El input activa rasgos visuales** (líneas, curvas) → la activación arranca abajo.
2. La activación **fluye hacia arriba** por las conexiones excitatorias: rasgos → letras → palabras → fonemas.
3. Las unidades **compiten lateralmente**: cuando una unidad se activa, **inhibe** a sus vecinas del mismo nivel. Por eso "casa" gana sobre "casi" cuando ves *c-a-s-a*.
4. **Cascadea**: la activación no espera a que un nivel termine — fluye continuamente, en paralelo. Por eso es un modelo *cascaded*.
5. Cuando una unidad supera un **umbral**, dispara su salida hacia el siguiente nivel.

La dinámica de **excitación + inhibición + umbral + cascada** es lo que hace que el modelo prediga los tiempos de reacción y los patrones de error observados empíricamente.

## Spreading activation (activación expansiva)

Concepto complementario, formulado originalmente por **Collins & Loftus (1975)** para semántica: cuando una unidad se activa, la activación **se propaga por la red** a unidades relacionadas, decreciendo con la distancia.

- Si activás *doctor*, se pre-activan *enfermera*, *hospital*, *medicina* → cuando aparezcan después, se procesan más rápido. Eso es el **priming semántico**.
- También funciona en otros niveles: ortográfico, fonológico, morfológico.

## Cómo se mide empíricamente

La activación es teórica, pero sus **efectos** son observables:

- **Frecuencia**: palabras más frecuentes tienen umbrales más bajos → se activan más rápido. Por eso *casa* se lee más rápido que *huso* aunque tengan la misma longitud.
- **Vecindad léxica**: palabras con muchos vecinos ortográficos (*pato* tiene *pita*, *pago*, *pata*…) compiten lateralmente → activación más distribuida. Según la tarea, los vecinos facilitan o enlentecen.
- **Priming**: si se presenta *enfermera* antes de *doctor*, el segundo se procesa más rápido por activación residual del primero.
- **Imageabilidad / concreción**: palabras concretas se activan más fuerte/rápido que abstractas.

## Conexión con la ruta sublexical y pseudopalabras

Cuando se lee una **pseudopalabra**, no hay una unidad léxica para activar al máximo, pero igual hay **activación parcial**:

- La pseudopalabra **activa parcialmente vecinos léxicos**: *plame* activa débilmente *plana*, *llama*, *clame*.
- Esos vecinos contribuyen a la activación fonológica final, aun sin haber llegado al umbral.
- Por eso pseudopalabras con **alta vecindad léxica** se leen más rápido que las que no se parecen a nada — la ruta léxica contribuye **subumbralmente**.

Esa contribución residual es la **prueba de que las dos rutas no son independientes** sino que interactúan vía activación cascadeada. Es uno de los argumentos contra los modelos dual-route estrictos y a favor de modelos más conexionistas (Plaut et al., 1996, *triangle model*).

## Donde aparece "activación" en los papers

- **Modelo de logogen** (Morton): cada palabra es un "logogen" con un umbral; el input acumula activación; cuando se cruza el umbral, se reconoce.
- **Modelo cohort** (Marslen-Wilson) para reconocimiento auditivo: el inicio de la palabra activa un "cohort" de candidatos que se va reduciendo a medida que llega más input.
- **TRACE** (McClelland & Elman): el clásico de procesamiento del habla con activación interactiva.
- **DRC** (Coltheart et al., 2001): el dual-route con cascada.
- **Modelo de Levelt** de producción: activación cascadeada desde concepto → lema → forma fonológica → articulación.

## Síntesis

**Activación** = fuerza con que una unidad mental está siendo procesada. Fluye por conexiones excitatorias entre niveles, compite con vecinos por inhibición lateral, y cuando supera un umbral dispara hacia adelante. Sus correlatos empíricos son **frecuencia, vecindad, priming, tiempos de reacción**. Es el mecanismo que hace que el cerebro decida cuál palabra "ganó" cuando varias compiten por explicar el input.
