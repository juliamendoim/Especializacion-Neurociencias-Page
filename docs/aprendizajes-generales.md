# Aprendizajes generales

Documento transversal con conceptos y nociones que aparecen en distintas materias y vale la pena tener a mano.

---

## Conceptos de estadística

### t de Student

#### De dónde sale

La inventó **William Sealy Gosset** en 1908, un químico y estadístico que trabajaba en la cervecería **Guinness** en Dublín. Necesitaba comparar lotes pequeños de cebada y levadura (muestras de 4, 5, 10 observaciones), y la estadística que existía hasta ese momento — basada en la **distribución normal** — solo funcionaba bien con muestras grandes (n > 30).

Guinness le prohibió publicar bajo su nombre real (no querían que la competencia supiera que usaban estadística), así que firmó con el seudónimo **"Student"**. De ahí el nombre.

#### Qué es, conceptualmente

Es un **estadístico** (un número que se calcula a partir de los datos) que mide **cuán lejos están dos medias entre sí, en unidades de error estándar**:

```
t = (media₁ − media₂) / error estándar de la diferencia
```

Traducido:
- El **numerador** es la diferencia bruta entre los dos promedios. Si los preescolares tienen COMP-1 = 1,2 y los escolares 1,5, el numerador es 0,3.
- El **denominador** es cuánta variabilidad esperarías por puro azar dado el tamaño de las muestras y la dispersión interna de cada grupo. Es una medida de "ruido".
- El cociente te dice **cuántas veces "más grande" es la diferencia que el ruido**. Si t = 0,5, la diferencia se confunde con el ruido. Si t = 4, la diferencia sobresale claramente.

#### La distribución t

Lo que Gosset descubrió es que ese cociente, cuando trabajás con **muestras pequeñas**, **no** sigue una distribución normal — sigue una curva propia, parecida pero con **colas más pesadas** (acepta valores extremos como más probables, porque con pocos datos hay más incertidumbre).

Esa curva — la **distribución t de Student** — depende de un solo parámetro, los **grados de libertad** (df), que aproximadamente equivale a *n − 2* en una t de dos grupos. Cuantos más datos, más se parece a una normal; con n → ∞ son indistinguibles.

#### Cómo se obtiene el p-valor

1. Calculás t con la fórmula de arriba.
2. Mirás la curva t correspondiente a tus grados de libertad.
3. Calculás qué proporción del área bajo la curva queda **más allá** de tu valor de t. Esa proporción es **p**.
4. Si p ≤ 0,05 → la diferencia es lo bastante grande como para que sea improbable que haya salido por azar.

#### Para qué se usa

La t de Student es la prueba estándar para **comparar las medias de dos grupos** y decidir si la diferencia observada es estadísticamente significativa o se puede atribuir al azar.

Condiciones típicas:
- **Dos grupos** (no más).
- Variable dependiente **cuantitativa continua**.
- Datos aproximadamente **normales** (importante con n chico).

**Una cola vs. dos colas**: si la hipótesis es **direccional** ("el grupo A produce más que el B") se usa una cola; si solo se predice "que hay diferencia, sin saber en qué sentido", se usa de dos colas. Una cola da más potencia estadística pero exige tener fundamentada la dirección.

#### Variantes y alternativas

- **t pareada**: cuando son los mismos sujetos medidos antes/después (medidas repetidas).
- **ANOVA**: cuando hay 3 o más grupos.
- **U de Mann-Whitney** (no paramétrica): cuando los datos no son normales o las muestras son muy chicas. Algunos autores la prefieren con n pequeños.

#### Ejemplo concreto: Peñaloza (recontados narrativos)

Peñaloza compara dos grupos independientes de niños — G1 preescolares y G2 escolares de 1° básico — en varios índices de complejidad sintáctica (COMP-1, COMP-2, COMP-2 Adj, Sust, Adv).

Aplica **t de Student de una cola** porque:
- Son **dos grupos independientes** (niños distintos en cada grupo).
- La variable dependiente es **cuantitativa continua** (promedios de cláusulas por oración).
- La hipótesis es **direccional**: espera que los escolares produzcan **más** complejidad que los preescolares.

Umbral: p ≤ 0,05 (convención estándar en ciencias sociales).

---

### Efecto techo (ceiling effect)

Es un fenómeno metodológico que aparece cuando **la mayoría de los participantes obtienen el puntaje máximo o casi máximo** en una tarea. La medición "se choca contra el techo" del instrumento — no puede capturar diferencias por arriba de ese nivel.

#### Por qué es un problema

- **Pierde poder discriminativo**: si el 95 % de los chicos contesta bien el 100 % de los ítems, no podés saber cuál tiene mejor rendimiento que cuál. La tarea no distingue entre "muy bueno", "excelente" y "perfecto".
- **Comprime la varianza**: como casi no hay variabilidad, las correlaciones con otras variables se subestiman, y los tests estadísticos pierden potencia.
- **Oculta diferencias entre grupos**: si dos grupos rinden ambos cerca del techo, no se pueden distinguir aunque haya diferencias reales en habilidades subyacentes.

#### Su gemelo: efecto piso (floor effect)

Lo opuesto: cuando casi todos puntúan en el mínimo. Tampoco discrimina — todos parecen igual de malos aunque haya diferencias reales.

#### Aplicado a Friedmann

Las relativas de **sujeto** muestran efecto techo: tanto los chicos con desarrollo típico como los chicos con TDL las resuelven correctamente o casi. Todos andan cerca del 100 % de aciertos, así que esa tarea **no sirve para diagnosticar TDL** — no hay separación entre grupos.

Las relativas de **objeto**, en cambio, generan una distribución más amplia: los típicos siguen rindiendo alto pero los TDL caen significativamente. Ahí hay **varianza diferencial** y por eso son **sensibles al diagnóstico**. Por eso Friedmann reporta solo las no-canónicas: son las que rompen el techo y dejan ver el déficit.

#### Cómo se evita en general

- Aumentar la dificultad de los ítems.
- Agregar ítems más complejos al final (escalonar dificultad).
- Usar medidas continuas (tiempos de reacción, por ejemplo) en lugar de solo "correcto/incorrecto".

---

### Media y desvío estándar

Una **media sola no dice nada útil** sobre un grupo. Hay que saber qué tan **dispersos** están los datos alrededor de esa media para interpretar bien el resultado.

#### Qué es la media

El **promedio** del grupo: sumar todos los valores y dividir por la cantidad de sujetos. Es una medida de **tendencia central** — dónde está "el centro" de la distribución.

#### Qué es el desvío estándar (DE / SD)

Medida de **dispersión**: cuán alejados están, en promedio, los valores individuales respecto de la media del grupo.

Lógica del cálculo:

1. Para cada sujeto, calculás cuánto se aleja de la media (su "desviación").
2. Elevás al cuadrado cada desviación (para que las negativas y positivas no se cancelen).
3. Promediás esos cuadrados → **varianza**.
4. Sacás la raíz cuadrada → **desvío estándar** (vuelve a las unidades originales de la variable).

```
DE = √[ Σ(xᵢ − media)² / (n − 1) ]
```

Interpretación rápida si la distribución es aproximadamente normal:

- **~68 %** de los sujetos están dentro de **±1 DE** de la media.
- **~95 %** dentro de **±2 DE**.
- **~99,7 %** dentro de **±3 DE**.

Esa **regla 68–95–99,7** es la que vuelve útil al DE como referencia mental.

#### Por qué se reportan juntas

Dos grupos con la **misma media** pueden ser muy distintos:

| Grupo | Media | DE | Qué pasó |
|---|---|---|---|
| A | 7,0 | 0,3 | Casi todos sacaron entre 6,7 y 7,3 — grupo **homogéneo** |
| B | 7,0 | 2,5 | Hay quienes sacaron 4 y quienes sacaron 10 — grupo **heterogéneo** |

La media sola los haría parecer equivalentes; el DE es lo que muestra que no lo son.

#### Por qué importa en investigación tipo Acosta

En estudios que comparan grupo TDL vs. control, reportar media + DE permite:

1. **Evaluar si los grupos son comparables al inicio** (edad, CI no verbal del K-BIT, NSE): medias parecidas y DE no escandalosamente distintos = grupos **balanceados**.
2. **Ver heterogeneidad interna**: el TDL es un grupo heterogéneo por definición. Un DE alto revela perfiles distintos conviviendo dentro del grupo — algo que la media oculta.
3. **Calcular t de Student**: la fórmula de la t **usa el DE** en el denominador (es el "ruido"). Sin DE, no hay test inferencial posible.
4. **Interpretar la magnitud del efecto**: una diferencia de 2 puntos es enorme si el DE es 0,5 (4 desvíos) pero trivial si el DE es 5 (0,4 desvíos). Eso se formaliza en el **tamaño del efecto** (d de Cohen = diferencia de medias / DE pooled).

#### Cómo aparece típicamente en una tabla

> Grupo TDL (n = 20): M = 12,3 (DE = 3,1)
> Grupo control (n = 20): M = 18,7 (DE = 2,4)

De un vistazo: **cuánto diferían en promedio** y **cuán dispersos eran internamente** — con eso ya se intuye si la diferencia entre grupos es robusta antes de mirar el p-valor.

#### En síntesis

- **Media** = dónde está el centro del grupo.
- **DE** = qué tan disperso está el grupo alrededor de ese centro.
- Las dos juntas describen **completamente** una distribución (asumiendo normalidad).
- Sin DE no se puede comparar grupos ni juzgar si una diferencia es relevante.

---

## Modelos cognitivos del lenguaje

### Phonemic / Phonological Output Buffer (Buffer fonológico de salida)

Es un componente que aparece en los **modelos cognitivos de producción del lenguaje** (Caramazza, Coltheart, Shallice y otros) — la familia teórica en la que se mueve Friedmann. Conviene pensarlo como una **memoria de trabajo fonológica de muy corta duración** que mantiene activa la secuencia de fonemas después de que el sistema léxico la "entregó" pero antes de que la articulación motora la ejecute.

#### Dónde encaja en el modelo

En un modelo de producción típico:

```
Sistema semántico → Léxico fonológico de salida → BUFFER FONOLÓGICO DE SALIDA → Programación articulatoria → Habla
```

Cuando recuperás la palabra *elefante* del léxico, esa palabra llega al buffer como una **secuencia ordenada de fonemas** /e-l-e-f-a-n-t-e/. El buffer:

- **Almacena** esa secuencia momentáneamente.
- **Mantiene el orden** correcto.
- **Sostiene la activación** mientras el sistema articulatorio va emitiendo cada segmento.

Es indispensable porque la producción no es instantánea: necesitás "guardar" el final de la palabra mientras pronunciás el principio.

#### Cómo se sabe que existe: el patrón de daño

Su existencia se infiere de pacientes con un perfil de errores muy característico (y simétricamente, de patrones evolutivos en niños). Si el buffer falla:

- **Errores fonológicos**: sustituciones, omisiones, adiciones y **metátesis** (transposiciones) de fonemas. *elefante → "elefonte", "elenfante", "efelante"*.
- **Efecto de longitud**: cuanto más larga la palabra, más errores. Una palabra de 6 sílabas colapsa el buffer; una de 2 sale bien.
- **Efecto de lexicalidad**: las **no-palabras** se ven más afectadas que las palabras reales, porque las palabras reales tienen apoyo léxico que estabiliza la representación.
- **Tipo de errores preservado**: los errores son **fonológicamente relacionados** con el target — no son sustituciones semánticas (no dice *jirafa* por *elefante*).

#### Buffers paralelos en el modelo

El esquema postula varios buffers análogos:

| Buffer | Función |
|---|---|
| **Fonológico de entrada** | Mantiene la cadena de fonemas durante la **comprensión** auditiva |
| **Fonológico de salida** | El que estamos discutiendo: producción oral |
| **Ortográfico de entrada** | Mantiene la cadena de letras durante la **lectura** |
| **Ortográfico de salida** | Mantiene la cadena de letras durante la **escritura** |

Daño selectivo a cada uno produce un síndrome diferente — y esa **doble disociación** es justamente el argumento empírico para postularlos como módulos separados.

#### Por qué aparece en Friedmann

Friedmann (y la escuela israelí de neuropsicología cognitiva) usa esta arquitectura como marco para clasificar **subtipos de TDL y dislexia**: un chico puede tener intacto el léxico pero un buffer fonológico de salida débil, lo que produce un perfil específico (errores en palabras largas, sobre todo en no-palabras, sin problemas semánticos). Distinguir el componente afectado importa porque cada subtipo tiene un pronóstico y una intervención diferentes.

---

### Modelo dual-ruta de lectura

Marco clásico (Coltheart et al., 2001 — *Dual-Route Cascaded model*) para entender cómo el cerebro convierte letras en sonido y significado. Postula **dos vías paralelas** desde la palabra impresa hasta la pronunciación.

#### Las dos rutas

**Ruta léxica (o directa)**
```
palabra impresa → léxico ortográfico → léxico fonológico → pronunciación
```
El lector **reconoce la palabra entera** porque ya la tiene almacenada. Es rápida, automática y funciona solo con palabras conocidas. Vía dominante en lectores expertos para palabras frecuentes.

**Ruta sublexical (o indirecta, fonológica, ensamblada)**
```
palabra impresa → análisis grafemático → conversión grafema-fonema (CGF) → ensamblado → pronunciación
```
El lector **construye la pronunciación pieza por pieza**, aplicando reglas de correspondencia letra-sonido. No necesita la palabra almacenada. Es más lenta y costosa, pero funciona con **cualquier secuencia de letras**, incluso una nunca vista antes.

#### Por qué las pseudopalabras solo activan la sublexical

Una pseudopalabra (*plame*, *fortifo*, *cardomito*) es ortotácticamente legal pero inexistente en el léxico. Cuando el lector la encuentra:
- La **ruta léxica falla**: no hay entrada que matchee.
- La **ruta sublexical funciona**: aplica las reglas grafema-fonema y ensambla una pronunciación posible.

Por eso las pseudopalabras son la **prueba pura del funcionamiento de la ruta sublexical**. Marcador diagnóstico clave:
- **Dislexia fonológica**: déficit sublexical → fallan en pseudopalabras.
- **Dislexia superficial**: déficit léxico → fallan en palabras irregulares, no en pseudopalabras.
- **TDL fonológico**: representaciones fonológicas débiles → pseudopalabras largas se desploman (test de repetición de no-palabras, Conti-Ramsden et al. 2001).

#### Por qué esto importa especialmente en español

El español tiene **ortografía transparente** (~95 % de correspondencia 1:1 grafema-fonema). Consecuencias:

- La ruta sublexical es **muy eficiente** en español. Casi cualquier palabra se puede leer correctamente con CGF.
- Los lectores expertos en español dependen **menos exclusivamente de la ruta léxica** que en inglés (donde la ortografía es opaca y abundan irregularidades como *colonel*, *yacht*).
- Las pseudopalabras se leen **bastante bien desde edades tempranas** en español, comparado con inglés.
- **Cambia el patrón diagnóstico**: la dislexia en español se manifiesta más en **lentitud** (fluencia, latencias) que en exactitud, porque la ruta sublexical da el resultado correcto pero con costo de tiempo. En inglés se ve más en errores; en español, en tiempos.

#### Variables que afectan la ruta sublexical (y a las pseudopalabras)

Efectos típicos que aparecen en papers de lectura:

1. **Longitud**: más letras/sílabas → más operaciones de CGF → peor rendimiento. Pseudopalabras largas son catastróficas para lectores con problemas en esta ruta.
2. **Complejidad silábica**: sílabas CCV (*tres*, *plan*) son más costosas que CV (*pa*, *to*). Grupos consonánticos aumentan errores y latencias.
3. **Vecindad léxica ortográfica**: una pseudopalabra que se parece a muchas palabras reales (*calsoma* parecida a *calzona*, *paloma*) se procesa más rápido — hay influencia léxica indirecta.
4. **Frecuencia de bigramas/trigramas**: secuencias frecuentes (*-ado*, *-ento*, *-ista*) facilitan el ensamblado.
5. **Edad/nivel lector**: la ruta sublexical mejora con la práctica. Niños chicos dependen casi exclusivamente de ella; lectores expertos la usan menos pero la mantienen disponible.

#### Cómo se conecta con otros conceptos del curso

- **Buffer fonológico de salida** (arriba): la ruta sublexical produce una secuencia de fonemas que luego pasa por ese buffer antes de articularse. Daño al buffer afecta producción tanto de palabras como de pseudopalabras.
- **K-BIT y evaluación**: el subtest de Vocabulario es léxico; la lectura de pseudopalabras es subléxica. Disociaciones entre ambos perfiles ayudan a clasificar trastornos.
- **TDL morfosintáctico (Acosta, Bedore & Leonard)**: el TDL puede comprometer la ruta sublexical vía representaciones fonológicas pobres, sin que el sistema léxico esté afectado.

#### Cuando un paper dice "se midió lectura de pseudopalabras"

Significa que **se está midiendo selectivamente la ruta sublexical**. Comparar el rendimiento en palabras vs. pseudopalabras permite disociar las dos rutas: la diferencia entre ambas da el peso de la contribución léxica, y el rendimiento puro en pseudopalabras da el estado de la sublexical.

---

### Activación (en modelos cognitivos del lenguaje)

"Activación" es la **moneda corriente** de los modelos cognitivos: es la cantidad de "energía" o "fuerza" con que una unidad mental (un fonema, un grafema, un lexema, un concepto) está siendo procesada en un momento dado. Es un término metafórico, pero tiene definiciones operacionales concretas en los modelos formales.

#### Cómo funciona la activación

En modelos como el **DRC** (que es la **C** de *Dual-Route Cascaded*), el sistema se concibe como una **red de unidades interconectadas** — cada nivel (rasgo visual, letra, palabra, fonema) es un conjunto de unidades. Cuando ves una palabra:

1. **El input activa rasgos visuales** (líneas, curvas) → la activación arranca abajo.
2. La activación **fluye hacia arriba** por las conexiones excitatorias: rasgos → letras → palabras → fonemas.
3. Las unidades **compiten lateralmente**: cuando una unidad se activa, **inhibe** a sus vecinas del mismo nivel. Por eso "casa" gana sobre "casi" cuando ves *c-a-s-a*.
4. **Cascadea**: la activación no espera a que un nivel termine — fluye continuamente, en paralelo. Por eso es un modelo *cascaded*.
5. Cuando una unidad supera un **umbral**, dispara su salida hacia el siguiente nivel.

La dinámica de **excitación + inhibición + umbral + cascada** es lo que hace que el modelo prediga los tiempos de reacción y los patrones de error observados empíricamente.

#### Spreading activation (activación expansiva)

Concepto complementario, formulado originalmente por **Collins & Loftus (1975)** para semántica: cuando una unidad se activa, la activación **se propaga por la red** a unidades relacionadas, decreciendo con la distancia.

- Si activás *doctor*, se pre-activan *enfermera*, *hospital*, *medicina* → cuando aparezcan después, se procesan más rápido. Eso es el **priming semántico**.
- También funciona en otros niveles: ortográfico, fonológico, morfológico.

#### Cómo se mide empíricamente

La activación es teórica, pero sus **efectos** son observables:

- **Frecuencia**: palabras más frecuentes tienen umbrales más bajos → se activan más rápido. Por eso *casa* se lee más rápido que *huso* aunque tengan la misma longitud.
- **Vecindad léxica**: palabras con muchos vecinos ortográficos (*pato* tiene *pita*, *pago*, *pata*…) compiten lateralmente → activación más distribuida. Según la tarea, los vecinos facilitan o enlentecen.
- **Priming**: si se presenta *enfermera* antes de *doctor*, el segundo se procesa más rápido por activación residual del primero.
- **Imageabilidad / concreción**: palabras concretas se activan más fuerte/rápido que abstractas.

#### Conexión con la ruta sublexical y pseudopalabras

Cuando se lee una **pseudopalabra**, no hay una unidad léxica para activar al máximo, pero igual hay **activación parcial**:

- La pseudopalabra **activa parcialmente vecinos léxicos**: *plame* activa débilmente *plana*, *llama*, *clame*.
- Esos vecinos contribuyen a la activación fonológica final, aun sin haber llegado al umbral.
- Por eso pseudopalabras con **alta vecindad léxica** se leen más rápido que las que no se parecen a nada — la ruta léxica contribuye **subumbralmente**.

Esa contribución residual es la **prueba de que las dos rutas no son independientes** sino que interactúan vía activación cascadeada. Es uno de los argumentos contra los modelos dual-route estrictos y a favor de modelos más conexionistas (Plaut et al., 1996, *triangle model*).

#### Donde aparece "activación" en los papers

- **Modelo de logogen** (Morton): cada palabra es un "logogen" con un umbral; el input acumula activación; cuando se cruza el umbral, se reconoce.
- **Modelo cohort** (Marslen-Wilson) para reconocimiento auditivo: el inicio de la palabra activa un "cohort" de candidatos que se va reduciendo a medida que llega más input.
- **TRACE** (McClelland & Elman): el clásico de procesamiento del habla con activación interactiva.
- **DRC** (Coltheart et al., 2001): el dual-route con cascada.
- **Modelo de Levelt** de producción: activación cascadeada desde concepto → lema → forma fonológica → articulación.

#### Síntesis

**Activación** = fuerza con que una unidad mental está siendo procesada. Fluye por conexiones excitatorias entre niveles, compite con vecinos por inhibición lateral, y cuando supera un umbral dispara hacia adelante. Sus correlatos empíricos son **frecuencia, vecindad, priming, tiempos de reacción**. Es el mecanismo que hace que el cerebro decida cuál palabra "ganó" cuando varias compiten por explicar el input.

---

## Instrumentos de evaluación

### ITPA — Illinois Test of Psycholinguistic Abilities

#### Qué es

Test desarrollado por **Kirk, McCarthy & Kirk (1968)** en la Universidad de Illinois. La versión en español más usada es la **adaptación de Ballesteros y Cordero** (TEA Ediciones, Madrid), que es la que circula en hispanohablantes y la que usan investigadores como **Acosta** en sus trabajos sobre TDL.

Evalúa las **habilidades psicolingüísticas** de niños entre **2;6 y 10;6 años**: percepción, comprensión, organización y expresión del lenguaje, tanto a nivel oral como visual.

#### En qué se basa

En el modelo de comunicación de **Osgood (1957)**, que describe la conducta verbal en términos de tres dimensiones cruzadas:

| Dimensión | Distinción |
|---|---|
| **Canales** | Auditivo-vocal vs. visomotor |
| **Procesos** | Recepción → Asociación/Organización → Expresión |
| **Niveles** | Representacional (significado) vs. Automático (memoria, secuencia, cierre) |

Cada subtest del ITPA aísla la combinación de un canal, un proceso y un nivel. Por eso es **diagnóstico**: permite identificar el componente psicolingüístico específico que está afectado.

#### Los 12 subtests

**Nivel representacional** (manejo de significado):

1. **Comprensión auditiva** — el chico oye una pregunta y responde sí/no.
2. **Comprensión visual** — identifica una figura igual a la modelo entre varias.
3. **Asociación auditiva** — analogías verbales: *"El pájaro vuela, el pez ___"*.
4. **Asociación visual** — analogías con figuras.
5. **Expresión verbal** — describe un objeto que se le muestra.
6. **Expresión motora** — gesticula el uso de un objeto.

**Nivel automático** (procesamiento sin foco semántico):

7. **Integración gramatical** *(grammatic closure)* — completa morfología: *"acá hay un perro, acá hay dos ___"* → "perros". **El más usado en evaluaciones de TDL.**
8. **Integración visual** — encuentra figuras parcialmente ocultas.
9. **Integración auditiva** *(supl.)* — completa palabras con fonemas faltantes.
10. **Fusión de sonidos** *(supl.)* — *"m-e-s-a" → "mesa"*.
11. **Memoria secuencial auditiva** — repite series de dígitos.
12. **Memoria secuencial visual** — reproduce secuencias de figuras geométricas.

#### Para qué sirve clínicamente

- **Perfil intra-individual**: detecta áreas fuertes y débiles dentro del mismo chico, no solo un puntaje global.
- **Detección de TDL**: el subtest de **integración gramatical** es especialmente sensible al déficit morfosintáctico característico del TDL — chicos con TDL típicamente puntúan muy bajo ahí pero conservan otros subtests, lo que produce un perfil "en pico".
- **Orientación terapéutica**: como aísla componentes, ayuda a planificar intervención focalizada.

#### Críticas

- Modelo teórico (Osgood) hoy considerado superado.
- Baremos antiguos (originales de los 60-70).
- Algunos subtests tienen problemas de validez de constructo.
- Aun así sigue usándose mucho en clínica e investigación hispanohablante por inercia y porque hay pocas alternativas estandarizadas.

#### Por qué aparece en Acosta

Acosta y su equipo (Universidad de La Laguna) usan el subtest de **integración gramatical** del ITPA como una de las medidas centrales para identificar TDL morfosintáctico en niños hispanohablantes — encaja con el tipo de errores que esperan (omisiones de morfemas flexivos, errores de concordancia, etc.).

---

### K-BIT — Kaufman Brief Intelligence Test

#### Qué es

Test breve de inteligencia desarrollado por **Alan S. Kaufman y Nadeen L. Kaufman (1990)**, con una segunda edición (K-BIT 2, 2004). La adaptación española es de **Cordero y Calonge** (TEA Ediciones, 1996).

Es un **screening** de inteligencia general — no reemplaza a una evaluación completa tipo WISC, pero ofrece una estimación confiable del CI en **15-30 minutos**, lo que lo vuelve muy útil cuando la inteligencia no es el foco principal del estudio sino un **criterio de inclusión/exclusión**.

Rango de edad: **4 a 90 años** (versión española).

#### Estructura

Solo dos subtests, uno verbal y uno no verbal:

| Subtest | Qué mide | Tarea |
|---|---|---|
| **Vocabulario** | Inteligencia **cristalizada** (conocimiento adquirido, lenguaje) | Dos partes: a) **Vocabulario expresivo** — nombrar una figura; b) **Definiciones** — completar una oración dada la primera y última letra del target |
| **Matrices** | Inteligencia **fluida** (razonamiento, resolución de problemas novedosos) | Analogías visuales y completamiento de patrones con figuras geométricas o pictóricas. **No requiere lenguaje.** |

Devuelve **tres puntajes**:
- **CI Vocabulario** (verbal / cristalizado)
- **CI Matrices** (no verbal / fluido)
- **CI Compuesto** (combinación de ambos)

#### Por qué aparece tanto en investigación sobre TDL

El TDL se define por **exclusión**: trastorno específico del lenguaje **sin** déficit cognitivo, sensorial ni neurológico. Para sostener ese diagnóstico hay que demostrar que la inteligencia no verbal está dentro de lo esperado (típicamente CI ≥ 85).

El K-BIT cumple exactamente esa función:

- **Rápido**: no se quema tiempo de testeo que se necesita para evaluación lingüística específica.
- **Tiene un subtest no verbal puro (Matrices)**: clave para no contaminar la medida de CI con la propia dificultad lingüística del chico. Si usás un test verbal de inteligencia con un chico con TDL, su CI sale bajo por el lenguaje, no por razonamiento — y eso lo excluiría falsamente del grupo TDL.
- **Está estandarizado y baremado en español**: permite reportar puntajes comparables.

Por eso en muchos papers de TDL (Acosta, Mendoza, Ramírez Santana y compañía) se lee algo como: *"se incluyeron niños con CI no verbal ≥ 85 en el subtest Matrices del K-BIT"*. Esa frase es la que separa "TDL" de "discapacidad intelectual con compromiso del lenguaje".

#### Limitaciones

- Es un **screening**, no un diagnóstico de capacidad cognitiva — para perfil cognitivo completo se necesita WISC, WPPSI o equivalentes.
- Solo dos subtests: no permite analizar disociaciones finas dentro del funcionamiento intelectual.
- El subtest de Vocabulario **no** debe usarse como medida de inclusión en estudios de TDL: justamente lo que está afectado es el lenguaje, así que sirve más como descripción del perfil que como criterio.

---

## Metodología de investigación

### PRISMA — Preferred Reporting Items for Systematic Reviews and Meta-Analyses

#### Qué es

Un **protocolo internacional** que estandariza cómo deben reportarse las **revisiones sistemáticas** y los **metaanálisis**. Publicado originalmente en 2009 por Moher, Liberati, Tetzlaff y Altman; actualizado en **PRISMA 2020**. La cita que usa Ferinua (Urrútia & Bonfill, 2010) es la traducción/difusión al español de la guía original.

No es una metodología para *hacer* la revisión, sino una guía para **escribirla y reportarla** de manera transparente y replicable.

#### Por qué se necesita

Antes de PRISMA, las revisiones sistemáticas eran muy heterogéneas en cómo reportaban sus criterios, búsquedas y exclusiones. Eso impedía:

- **Replicar la búsqueda**: si no se sabe qué bases de datos se consultaron, con qué términos y en qué fecha, otro investigador no puede repetir el procedimiento.
- **Evaluar el sesgo**: una revisión que omite estudios sin justificación puede estar cherry-picking sin que el lector lo detecte.
- **Comparar revisiones**: cada autor reportaba lo que le parecía relevante, no había un esquema común.

PRISMA estandariza todo eso.

#### Qué incluye

Una **checklist de 27 ítems** que cubren las secciones de un paper de revisión sistemática:

- **Título y resumen**: declarar explícitamente que es revisión sistemática / metaanálisis.
- **Introducción**: justificación y objetivos (formulados como pregunta PICO: Población, Intervención, Comparación, Outcome).
- **Métodos**: criterios de elegibilidad, fuentes de información, estrategia de búsqueda, proceso de selección, extracción de datos, evaluación de riesgo de sesgo, métodos de síntesis.
- **Resultados**: selección de estudios, características de los estudios, resultados de cada estudio individual, síntesis cuantitativa.
- **Discusión**: resumen de evidencia, limitaciones, conclusiones.

#### El diagrama de flujo PRISMA

Probablemente el elemento más reconocible: un **flowchart** que muestra cuántos estudios se identificaron, cuántos se descartaron en cada etapa y por qué, hasta llegar al número final incluido en la síntesis. Tiene cuatro fases:

```
Identificación → Cribado → Elegibilidad → Inclusión
```

Verlo en un paper te dice de un vistazo si la búsqueda fue sistemática y proporcional al objetivo.

#### Cuando un paper dice "siguiendo PRISMA"

Significa que los autores se comprometen a haber reportado todos los ítems de la checklist y que el lector puede auditarlos. Es señal de **estándar metodológico**: no garantiza que la revisión sea buena, pero sí que se puede juzgar y replicar. En revisiones sistemáticas serias hoy es prácticamente requisito de publicación.

---

## Bases biológicas y desarrollo cerebral

### El andamiaje innato del cerebro — Dehaene

Hay un pasaje en Dehaene (2019, Parte II) que sintetiza con una imagen muy nítida cómo se forma el sustrato neural sobre el que después se monta el aprendizaje. Lo cita textual porque vale la pena tenerlo a mano:

> "La exploración es guiada y canalizada por mensajes químicos, moléculas cuya concentración varía de una región a otra y que entonces reaccionan como paneles de señalización. La cabeza del axón olfatea, literalmente, este ambiente químico, de origen genético, y deduce qué dirección debe seguir. Con esto, y sin intervención del mundo exterior, se pone en funcionamiento una red de conexiones nerviosas cruzadas propia de la especie humana. Como veremos en un instante, esta red será refinada más tarde por el aprendizaje, pero el andamiaje inicial es innato, se construye in utero."
>
> (Dehaene, 2019)

#### Por qué importa esta imagen

Está describiendo un fenómeno biológico concreto — la **guía axonal** (*axon guidance*) durante el desarrollo embrionario — pero la idea filosófica que acarrea es enorme: el cerebro **no** llega al mundo como una pizarra en blanco lista para ser escrita por la experiencia, ni como una red ya cableada de manera definitiva. Llega con un **andamiaje** previamente armado por instrucciones genéticas, y ese andamiaje **es la condición de posibilidad** de cualquier aprendizaje posterior. Sin esa estructura mínima no habría dónde anclar las experiencias.

#### El mecanismo: la cabeza del axón "olfatea"

Cada axón, durante el desarrollo fetal, tiene en su extremo un **cono de crecimiento** que avanza por el tejido nervioso buscando su destino (otra neurona específica, un músculo específico, etc.). No se mueve al azar: detecta **gradientes químicos** — concentraciones desiguales de moléculas señalizadoras como las netrinas, semaforinas, efrinas — que funcionan como un sistema de coordenadas químico. Algunas moléculas atraen, otras repelen. El axón "lee" esa geografía química y se va guiando hacia su target. El proceso es activo, dirigido y específico, no aleatorio.

Las instrucciones para producir esos gradientes están en el genoma. De ahí lo de "de origen genético". No hace falta input del mundo exterior para que el plano básico de conexiones se forme.

#### El gancho conceptual: innato + aprendizaje

Lo que vuelve a la cita potente es cómo articula los dos lados del debate clásico:

- **Lo innato** = el andamiaje, el cableado básico, la arquitectura específica de la especie. Se forma *in utero*, antes de cualquier experiencia.
- **El aprendizaje** = el refinamiento posterior, la sintonización fina, la poda de conexiones, el fortalecimiento de las que se usan. Pasa después, a lo largo de la vida postnatal, con input del ambiente.

No es **uno u otro**. Son **dos fases superpuestas**, y la segunda solo funciona porque la primera existió.

#### Conexión con los debates del programa

Es exactamente el ángulo que Dehaene aporta al debate **Tomasello (usage-based) vs. innatistas** que aparece en Psicolingüística del Desarrollo:

- Para los innatistas radicales (Chomsky, Pinker, Valian), parte del cableado lingüístico estaría pre-especificado genéticamente.
- Para los usage-based (Tomasello), todo lo específicamente lingüístico se aprendería a partir de capacidades sociocognitivas generales (intention-reading, atención conjunta) + estadística distribucional.
- Dehaene ofrece una **vía media**: hay andamiaje innato (no específicamente lingüístico, pero sí condiciones biológicas previas — circuitos sensoriales, áreas perisilvianas, conexiones tálamo-corticales) y sobre ese andamiaje se construye el aprendizaje lingüístico postnatal.

Esto **disuelve parcialmente el dilema**: la pregunta deja de ser "¿innato o aprendido?" y pasa a ser **"qué parte es innata, hasta qué granularidad, y cómo interactúa con el aprendizaje"**.

#### Conexión con la homonimia neurona biológica / neurona artificial

Esta cita es también un argumento contra la idea de que una red neuronal artificial (la de McCulloch-Pitts y sus descendientes hasta los LLMs) sea un modelo plausible del cerebro:

- En el cerebro biológico, la arquitectura específica de conexiones está **parcialmente pre-especificada por gradientes químicos genéticamente codificados**.
- En una red neuronal artificial, **la arquitectura inicial no tiene ninguna estructura específica** — los pesos arrancan aleatorios, y toda la organización emerge del entrenamiento.
- Los LLMs no tienen "andamiaje innato" de ningún tipo. Empiezan literalmente de cero y necesitan, para compensar esa ausencia, **órdenes de magnitud más datos** que un niño.

Esa asimetría — el cerebro humano se prepara biológicamente para aprender lenguaje desde antes de nacer; el modelo artificial no se prepara en absoluto — es uno de los argumentos más sólidos contra la equivalencia ingenua entre los dos sistemas, y un dato a tener presente en el TP final.

### La línea numérica cortical y la organización topográfica — Dehaene

Otra cita de Dehaene que vale la pena tener anclada, esta vez sobre cómo el cerebro **codifica información mediante la posición física** de las neuronas:

> "Mis colegas y yo propusimos un modelo matemático de gran precisión para la autoorganización de las neuronas detectoras del número, esta vez basado en la propagación de actividad de un tipo de onda a lo largo de la superficie de la corteza en desarrollo. Esta teoría puede explicar todos los detalles de las propiedades de las neuronas detectoras del número. Según el modelo, estas células terminan por formar una suerte de línea numérica, una cadena lineal en que los números 1, 2, 3, 4… ocupan posiciones sucesivas y que surge espontáneamente en el seno de una red de neuronas aleatorias (Hannagan y otros, 2017)."
>
> (Dehaene, 2019, citando Hannagan et al., 2017)

#### Qué describe esta cita

En el surco intraparietal del cerebro humano (y también en otros primates) hay neuronas que responden a **cantidades numéricas**. Una neurona específica se activa fuerte ante "tres objetos" y débilmente ante "uno" o "cinco"; la vecina se activa fuerte ante "cuatro" y débilmente ante "dos" o "seis"; y así sucesivamente.

Lo notable: estas neuronas **no están distribuidas al azar** en la corteza. Las que responden a números cercanos están **físicamente cercanas**, formando una "línea numérica" cortical donde la **posición espacial codifica el valor numérico**. La distancia física entre neuronas refleja la distancia conceptual entre los números que detectan.

Lo que Hannagan et al. (2017) muestran es que esta organización **emerge espontáneamente** durante el desarrollo, sin necesidad de un plan genético detallado, a partir de la propagación de ondas de actividad en una red inicialmente aleatoria.

#### El principio general: organización topográfica del cerebro

La línea numérica es un caso particular de un fenómeno más amplio: gran parte del cerebro está organizado **topográficamente**, es decir, **la posición física de una neurona codifica algún aspecto del estímulo que procesa**:

| Región | Qué codifica la posición |
|---|---|
| Corteza visual primaria (V1) | **Retinotopía** — la posición espacial en la retina |
| Corteza somatosensorial | **Somatotopía** — la parte del cuerpo (homúnculo sensorial) |
| Corteza auditiva | **Tonotopía** — la frecuencia del sonido |
| Surco intraparietal | **Línea numérica** — el valor numérico |
| Corteza motora | **Somatotopía motora** — la parte del cuerpo a controlar |

En todos estos casos, **valores parecidos del estímulo se procesan en neuronas físicamente vecinas**. La distancia anatómica codifica la similitud funcional.

#### "¿Como en computación?"

Acá está el contraste interesante que da la pregunta. Sí y no — la respuesta tiene matices que vale la pena distinguir.

**En memoria de computadora clásica (RAM)**, la posición es **arbitraria**. La dirección `0x7F4E2A` no significa nada en sí misma: es solo un nombre. La información en `0x7F4E2A` no tiene ninguna relación esperable con la información en `0x7F4E2B`. La cercanía física en el chip no implica cercanía semántica. El sistema accede a la información mediante su dirección, pero esa dirección es un identificador, no un atributo.

**En el cerebro**, la posición es **funcional**. Dos neuronas vecinas codifican cosas relacionadas. La cercanía física **es** la cercanía semántica. Por eso una lesión focal produce un déficit selectivo y predecible (perder una pequeña zona del córtex visual ciega una pequeña región del campo visual; perder una zona pequeña del córtex somatosensorial deja sin sensibilidad a una parte específica del cuerpo).

Hay sin embargo dos arquitecturas computacionales donde la posición sí codifica relación, y son los análogos plausibles del principio topográfico:

1. **Mapas autoorganizativos (Self-Organizing Maps, SOM)** de Teuvo Kohonen (1982). Son redes neuronales artificiales explícitamente diseñadas para imitar la organización topográfica cortical: entrenan una grilla de unidades de manera que entradas parecidas terminan activando unidades vecinas. Resultado: un mapa bidimensional donde la posición preserva relaciones de similitud del input. Es una **importación directa** del principio biológico a la computación.

2. **Embeddings vectoriales en aprendizaje automático y LLMs**. La palabra "rey" y la palabra "reina" tienen vectores cercanos en el espacio de embeddings; "rey" y "mesa" tienen vectores lejanos. La posición en el espacio vectorial codifica relación semántica. Esto es análogo al principio topográfico, aunque opera en un espacio de cientos o miles de dimensiones en lugar de en la superficie bidimensional del córtex.

Pero hay diferencias importantes incluso en estos análogos:

- En el cerebro la topografía es **anatómicamente real y restringida a 2D** (la superficie de la corteza). Esto impone limitaciones (no se pueden representar todas las relaciones de alta dimensionalidad en una superficie bidimensional, hay distorsiones inevitables).
- En los embeddings de un LLM no hay restricción dimensional: los vectores pueden tener 768 o 12.288 dimensiones. Cabe mucha más estructura, pero a costa de perder la elegancia geométrica de un mapa físico.
- En el cerebro, la organización topográfica **se autoorganiza durante el desarrollo** a partir de actividad espontánea (como muestra el modelo de Hannagan), de manera que las restricciones biofísicas (costo del cableado, sincronización de ondas corticales) dirigen la forma final. En un modelo computacional, la organización emerge de la función objetivo del entrenamiento, no de constricciones físicas.

#### Por qué importa esto para el TP

Esta cita sirve para varios capítulos del trabajo final por homonimias:

1. **Capítulo de memoria**. La memoria humana es **espacial y de contenido**: la organización topográfica del córtex significa que recuperar información es activar una región específica, y regiones vecinas activan información relacionada. En la RAM de una computadora, la posición no significa nada y la cercanía no implica relación. En embeddings sí, pero en un sentido distinto y sin sustrato físico.

2. **Capítulo de neurona y arquitectura**. Refuerza el argumento del capítulo 1 (homonimia neurona biológica vs. artificial): no solo el principio de Dale o la inactivación de canales son específicos de la neurona biológica; también lo es el hecho de que su **posición anatómica codifica función**. En una neurona artificial estándar, la "posición" en una matriz de pesos es solo una indexación de bookkeeping; en una neurona biológica, la posición es parte de lo que la neurona "es" funcionalmente.

3. **Capítulo de representación o aprendizaje**. La cita conecta con la pregunta de cómo el conocimiento queda escrito en el sustrato físico. En el cerebro, escribir conocimiento implica **especializar zonas anatómicas**. En un LLM, escribir conocimiento implica ajustar pesos numéricos en una arquitectura sin geografía física propia. Las dos cosas pueden producir comportamientos equivalentes, pero no son la misma operación.

4. **Caso de homonimia convergente parcial**. Los mapas autoorganizativos y los embeddings son ejemplos donde la idea de **"información codificada por posición"** sí cruzó entre cerebro e IA con cierto éxito. Vale como ejemplo de cuándo el préstamo conceptual fue productivo, y conviene contrastarlo con casos donde la homonimia es más ornamental.

### Autoorganización cerebral vs. big data — Dehaene

Cita central para el debate **cerebro vs. redes neuronales artificiales**, particularmente relevante para el capítulo de Aprendizaje del TP final:

> "La idea de autoorganización difiere radicalmente del enfoque actual de la inteligencia artificial, basada en big data. A diferencia de las redes neuronales actuales, nuestro cerebro no parece necesitar millones de datos para organizarse. Por el contrario, sus núcleos de conocimiento se desarrollan espontáneamente, por estimulación interna. Son escasos los informáticos que, como Joshua Tenenbaum, profesor del MIT, contemplan la posibilidad de copiar esta autoorganización en una inteligencia artificial. Tenenbaum trabaja para simular un bebé virtual que llegaría al mundo con la capacidad de generar, por sí solo, millones de imágenes realistas. Estas le servirían de base para el aprendizaje, sin que exista necesidad de algún otro dato. Según este enfoque radical, incluso antes del nacimiento, los circuitos neuronales se entrenarían con ayuda de una base de datos generada por ellos mismos (Lake y otros, 2016; de paso, señalemos que es otro ejemplo del bootstrapping del barón de Münchhausen). La mayor parte de su aprendizaje se produce de forma interna, sin interacción con el exterior, y luego solo resta realizar algunos ajustes en función de los datos suplementarios tomados del mundo real."
>
> (Dehaene, 2019, citando Lake et al., 2016)

#### El argumento central

Dehaene está señalando una **asimetría empírica fuerte** entre cerebro humano y redes neuronales artificiales contemporáneas. No es una crítica filosófica abstracta sino un dato cuantitativo:

| | Cerebro humano | LLM contemporáneo |
|---|---|---|
| Datos de entrenamiento | ~10⁷ – 10⁸ palabras hasta la adolescencia | ~10¹¹ – 10¹³ tokens |
| Asimetría | — | **4 a 6 órdenes de magnitud más** |
| Aprendizaje "preexterior" | Sí — circuitos se ensamblan in utero por actividad espontánea | No — los pesos arrancan aleatorios |
| Eficiencia de muestreo | Altísima (un niño aprende de pocos ejemplos) | Bajísima (requiere exposición masiva) |

La pregunta clave que esta cita pone sobre la mesa: **¿por qué el cerebro logra con menos datos lo que una red artificial necesita órdenes de magnitud más para alcanzar?** Dos hipótesis posibles, que no son excluyentes:

1. El cerebro tiene **andamiaje innato** (los circuitos se autoorganizan antes de cualquier input externo, por actividad espontánea pre y posnatal — la cita anterior sobre la guía axonal va por este lado).
2. El cerebro tiene **mecanismos de autoorganización** distintos del gradient descent + big data: aprende por simulación interna, por generación de hipótesis, por modelos causales, por composicionalidad de conceptos.

Ambas hipótesis aparecen articuladas en el paper de **Lake et al. (2016)** que Dehaene cita.

#### La referencia clave: Lake, Ullman, Tenenbaum y Gershman (2016)

**Lake, B. M., Ullman, T. D., Tenenbaum, J. B. y Gershman, S. J. (2016)** "Building machines that learn and think like people". *Behavioral and Brain Sciences*, 40, e253. Es uno de los papers más citados del cruce ciencia cognitiva / inteligencia artificial del último decenio, y un *must read* para el TP final.

Su argumento, en cuatro puntos:

1. **Construir modelos causales del mundo**, no solo aprender correlaciones estadísticas.
2. **Sostener principios fundamentales de cognición intuitiva**: física intuitiva (los objetos persisten, caen, ocupan espacio) y psicología intuitiva (los agentes tienen objetivos, creencias).
3. **Aprender a aprender** (*learning to learn*): adquirir rápidamente nuevas tareas a partir de pocos ejemplos, aprovechando estructura compartida con tareas previas.
4. **Pensar rápido y lento**: integrar inferencia rápida (sistema 1) con planificación deliberativa (sistema 2).

Los autores muestran que las redes neuronales profundas son potentes pero **fundamentalmente limitadas** en estos cuatro aspectos. Su propuesta: incorporar **priors estructurados** y **modelos generativos** al aprendizaje automático.

#### El bebé virtual y el bootstrapping de Münchhausen

La idea del bebé virtual que se entrena con datos que él mismo genera es **conceptualmente paradójica** —de ahí la broma con Münchhausen, el barón que decía haberse sacado del pantano tirando de su propio pelo—. Tenaza paradoja: ¿cómo puede aprender algo nuevo si solo se entrena con lo que ya puede generar?

La solución técnica que proponen Lake y Tenenbaum: el sistema arranca con un **núcleo mínimo de conocimiento innato** (física intuitiva, intuición psicológica, principios de objetos y agentes) y a partir de ese núcleo **genera escenarios coherentes** que sirven como datos de entrenamiento. La "generación" no es arbitraria: está limitada por las leyes que el núcleo innato impone (los objetos no atraviesan paredes, los agentes persiguen objetivos).

Esa idea conecta directamente con la idea filosófica más amplia de que **no se aprende todo desde cero** y que la mente humana viene con **estructura previa que hace posible el aprendizaje**. Es Kant traducido al siglo XXI.

#### Conexión con líneas del TP final

Esta cita es probablemente **el ancla más fuerte del libro de Dehaene** para los siguientes capítulos del TP:

- **Línea 1 (Aprendizaje estadístico vs. LLMs)**: Dehaene está señalando exactamente la asimetría de eficiencia que vos ya tenés identificada. Sirve para cerrar el argumento de que los LLMs no son modelos plausibles del aprendizaje infantil sin reformas profundas. Conecta directo con **Yedetore et al. (2023)** "How poor is the stimulus?", que muestra empíricamente que las redes entrenadas con input chiquito (como el del niño) fallan en generalizaciones que el niño hace.

- **Capítulo 1 (Neurona / Potencial de acción)**: refuerza el punto de que el cerebro biológico llega al mundo **ya estructurado** (andamiaje innato + capacidad de autoorganización por actividad espontánea), mientras que la red artificial llega con pesos aleatorios. Es otra forma de mostrar la asimetría de partida.

- **Capítulo 3 (Aprendizaje)**: ofrece una clasificación interesante para tu tipología de homonimias. El "aprendizaje" en el cerebro humano y el "aprendizaje" en un LLM son superficialmente equivalentes (ambos modifican parámetros internos en función de input), pero difieren radicalmente en (a) el punto de partida, (b) la cantidad de datos requerida, (c) el mecanismo subyacente (autoorganización + actualización local vs. gradient descent global). Esta cita es **el caso de homonimia engañosa** más claro de tu TP: la misma palabra para procesos que se parecen en la superficie pero que son arquitectónicamente distintos.

- **Capítulo 4 (Predicción)**: el bebé virtual de Tenenbaum es un sistema **predictivo en sentido estricto** — genera escenarios para entrenarse. Conecta con todo el programa de predictive coding (Rao & Ballard, Friston, Schrimpf, Caucheteux).

#### Una observación más para tu TP

La cita también pone sobre la mesa una pregunta que tu TP debería abordar explícitamente: **¿cuánta de la asimetría humano-LLM se debe a la cantidad de datos, y cuánta se debe a la arquitectura de partida?** Si fuera solo cantidad, entrenar un LLM con más datos cerraría la brecha. Si es arquitectura (priors innatos, capacidad de autoorganización, estructura causal del conocimiento), no hay cantidad de datos que la cierre.

La evidencia hasta ahora — Lake et al. (2016), Yedetore et al. (2023), Hosseini et al. (2024), todo este programa — apunta a que **una parte sustancial de la asimetría es arquitectónica**, no de cantidad de datos. Esa es una tesis defendible y fuerte para tu trabajo.

### Expresión génica: el aprendizaje como cambio molecular y estructural — Dehaene

Cuarta cita de Dehaene en esta sección, esta vez sobre lo que pasa **a nivel molecular** dentro de las neuronas cuando se aprende algo:

> "Allí se expresan nuevos genes, las sinapsis brotan, las arborescencias de dendritas y de axones se multiplican y, en el animal experto, todas estas ramificaciones suplementarias se traducen en un aumento del 23 % del espesor de la corteza."
>
> (Dehaene, 2019)

#### Qué significa "expresar genes"

Toda célula del cuerpo tiene el mismo ADN completo — las mismas ~20.000 instrucciones genéticas. Lo que diferencia a una neurona de una célula del hígado es **cuáles de esos genes están activos en cada momento**.

"Expresar un gen" = **leer ese gen y traducirlo en una proteína funcional**. El proceso tiene dos pasos:

1. **Transcripción**: una enzima copia la secuencia del gen del ADN a una molécula intermedia llamada ARN mensajero (ARNm).
2. **Traducción**: los ribosomas leen el ARNm y ensamblan los aminoácidos en una proteína específica.

En cualquier momento, una neurona tiene solo una fracción de sus genes activos. "Se expresan nuevos genes" significa que el aprendizaje **activa genes que estaban dormidos**, y esos genes fabrican proteínas nuevas que se necesitan para los cambios físicos siguientes en la célula.

#### Dos tipos de cambios cerebrales en el aprendizaje

| Tipo | Tiempo | Mecanismo |
|---|---|---|
| **Cambios rápidos / corto plazo** | Segundos a minutos | Modificación de proteínas que ya existen (más receptores, mayor sensibilidad). No requiere nuevos genes. |
| **Cambios duraderos / largo plazo** | Horas a días | **Nuevas proteínas, hechas a partir de nuevos genes activados.** Las proteínas construyen estructura nueva. |

Esta distinción la estableció **Eric Kandel** (Premio Nobel 2000) trabajando con el caracol marino *Aplysia*. Mostró que la memoria de corto plazo se mantiene con las proteínas que ya tenés, pero **la memoria de largo plazo solo se forma si se expresan genes nuevos y se sintetizan proteínas**. Si bloqueás la síntesis proteica con drogas, el animal aprende la tarea inmediatamente pero la olvida a las pocas horas: no hay cambio estructural duradero porque no hubo nuevos genes expresados.

#### La cascada molecular que describe Dehaene

Cuando un animal aprende, en la corteza se desencadena, en este orden:

1. **Actividad eléctrica intensa** en los circuitos involucrados en la tarea.
2. La actividad dispara **segundos mensajeros** dentro de las neuronas (calcio, AMP cíclico).
3. Los segundos mensajeros activan **factores de transcripción** — el más famoso es **CREB** (cAMP response element-binding protein).
4. CREB entra al núcleo y enciende **genes tempranos inmediatos** (c-fos, Arc, zif268), que actúan como interruptores.
5. Estos a su vez encienden **genes tardíos** que codifican proteínas estructurales (factores de crecimiento, moléculas de adhesión, componentes sinápticos).
6. Las proteínas nuevas viajan al sitio donde se necesitan y **construyen estructuras físicas**: sinapsis nuevas, espinas dendríticas nuevas, ramas axonales nuevas.
7. A escala macroscópica, después de mucho aprendizaje sostenido en una zona, **el córtex se vuelve más grueso** porque hay más estructura física. Es el "23 % de aumento del espesor cortical" que cita Dehaene.

#### Qué se ramifica concretamente

- **Sinapsis brotan**: aparecen nuevos puntos de contacto entre neuronas. Una neurona puede tener decenas de miles de sinapsis, y ese número cambia con el aprendizaje.
- **Arborización dendrítica**: las dendritas (ramas que reciben señales) crecen, se ramifican, desarrollan más espinas dendríticas — las pequeñas protuberancias donde típicamente se establecen sinapsis.
- **Arborización axonal**: los axones extienden ramas adicionales hacia otras neuronas, ampliando con qué áreas se conecta esa célula.

Todo esto requiere **proteínas nuevas**, que requieren **genes activados**, que requieren **actividad inducida por el aprendizaje**. Es una cadena causal continua desde la experiencia hasta el ADN y desde el ADN de vuelta a la estructura cerebral.

#### Conexión con el TP final

La cita refuerza la asimetría entre aprendizaje biológico y aprendizaje artificial que ya viene apareciendo en las otras citas de Dehaene:

| | Cerebro aprendiendo | LLM aprendiendo |
|---|---|---|
| Lo que cambia | Proteínas, sinapsis, dendritas, espesor cortical | Pesos numéricos en matrices |
| Sustrato físico del cambio | Estructura biológica nueva | Ninguna alteración física, solo números |
| Costo energético del cambio | Alto (síntesis proteica es costosa) | Igual al cómputo normal de inferencia |
| Velocidad del cambio | Horas a días para consolidarse | Inmediato (cada paso de gradient descent) |
| Reversibilidad | Difícil (lleva tiempo desmantelar estructuras) | Instantánea (los pesos pueden modificarse libremente) |
| Genes involucrados | Sí: CREB, c-fos, Arc, decenas más | Ninguno (no hay genes) |
| Reproducibilidad del cambio | Variable, depende del estado del organismo | Determinístico dado el algoritmo |

En una red artificial, "aprender" significa **cambiar números**. En el cerebro, aprender significa **rearmar la maquinaria celular** — fabricar proteínas nuevas, hacer crecer estructuras, modificar físicamente el órgano. Es la misma palabra para procesos arquitectónicamente muy distintos: caso clásico de **homonimia con divergencia mecanística profunda** para el Capítulo 3 (Aprendizaje) del TP. La homonimia es engañosa porque sugiere equivalencia mecánica donde la divergencia es total — el mismo verbo "aprender" describe en un caso un proceso bioquímico costoso, lento y semi-irreversible, y en el otro una actualización numérica instantánea y sin sustrato físico.

#### Referencias clave

Para anclar académicamente esta sección, los papers fundacionales son:

- **Kandel, E. R. (2001)** "The molecular biology of memory storage: A dialogue between genes and synapses". *Science*, 294(5544), 1030-1038. **El paper del Nobel.** Síntesis del programa de Kandel sobre la base molecular del aprendizaje.
- **Greenough, W. T. y Bailey, C. H. (1988)** "The anatomy of a memory: Convergence of results across a diversity of tests". *Trends in Neurosciences*, 11(4), 142-147. Los estudios clásicos sobre cambio estructural cortical por aprendizaje.
- **Bailey, C. H. y Kandel, E. R. (2008)** "Synaptic remodeling, synaptic growth and the storage of long-term memory in Aplysia". *Progress in Brain Research*, 169, 179-198.

Estos tres van directo a la **categoría 16 (Aprendizaje biológico vs. artificial)** del INDICE de bibliografía del TP.

### Calcio y glucosa: la economía energética del aprendizaje

Una nota complementaria de la entrada anterior. Toda la cascada de expresión génica y construcción estructural que describe Dehaene **es metabólicamente costosísima**, y depende de una colaboración muy estrecha entre dos moléculas:

- El **calcio (Ca²⁺)** funciona como **señal**: dice cuándo hay que aprender y qué hay que aprender.
- La **glucosa** funciona como **combustible**: paga la cuenta energética de hacer ese aprendizaje.

No forman un complejo molecular en sentido estricto — es decir, no se unen químicamente como hacen, por ejemplo, hemoglobina con oxígeno. Pero **están acoplados funcionalmente en tres niveles distintos**, y el acople es central para entender por qué aprender requiere energía y por qué el cerebro consume tanta glucosa.

#### Primer nivel: el Ca²⁺ como gatillo del aprendizaje

Cuando una neurona se activa intensamente durante el aprendizaje:

1. Se abren canales de **Ca²⁺ dependientes de voltaje**.
2. El Ca²⁺ entra al citoplasma desde el exterior (donde hay ~10.000 veces más concentración que adentro, en reposo).
3. El pico de Ca²⁺ activa **CaMKII** (calmodulin-dependent kinase II), **PKA** (protein kinase A) y otras quinasas.
4. Estas quinasas fosforilan a **CREB**, el factor de transcripción que prende los genes nuevos que vimos antes.
5. La expresión de genes y la síntesis de proteínas comienzan: aparecen sinapsis, dendritas y axones nuevos.

**Sin la señal de Ca²⁺ no hay aprendizaje duradero.** Es el primer eslabón de toda la cascada de Kandel.

#### Segundo nivel: la glucosa como combustible

Toda esa cascada consume energía en forma de **ATP** (adenosin trifosfato):

- Cada vez que una bomba devuelve Ca²⁺ del citoplasma al exterior, gasta ATP. Es esencial: si el Ca²⁺ se quedara alto demasiado tiempo, la neurona se autodestruiría (excitotoxicidad).
- Cada vez que se sintetiza una proteína nueva (para construir una sinapsis, una dendrita), se gasta ATP en cantidades enormes — la traducción es uno de los procesos celulares más costosos energéticamente.
- Cada vez que se transcribe un gen, se gasta ATP y GTP.
- Cada vez que el axón crece una ramita nueva, se gasta ATP para mover el citoesqueleto, generar membrana, transportar componentes.

El ATP en el cerebro se fabrica **casi exclusivamente a partir de glucosa**, a través de la glucólisis citoplasmática + la fosforilación oxidativa mitocondrial. El cerebro humano consume **~120 g de glucosa por día**, que representa aproximadamente **el 20 % del total de la energía del cuerpo en reposo**, aun siendo solo el 2 % de la masa corporal. La mayor parte de ese gasto va a mantener gradientes iónicos (incluido el de Ca²⁺) y a alimentar los procesos de plasticidad sináptica.

#### Tercer nivel: el diálogo bidireccional en la mitocondria

Acá está el dato más fino y es lo que se parece más a un "complejo" funcional:

Cuando hay un pico de Ca²⁺ citoplasmático por actividad neuronal, **las mitocondrias absorben parte de ese Ca²⁺** a través de un canal específico (el MCU, *mitochondrial calcium uniporter*). Una vez adentro de la mitocondria, el Ca²⁺ **activa directamente tres enzimas clave del ciclo de Krebs**: la piruvato deshidrogenasa, la isocitrato deshidrogenasa y la α-cetoglutarato deshidrogenasa.

¿Qué hacen estas enzimas? Aceleran la oxidación de la glucosa para producir más ATP.

Entonces lo que ocurre es:

> **Pico de Ca²⁺ → mitocondria absorbe Ca²⁺ → enzimas mitocondriales se activan → ciclo de Krebs se acelera → se quema más glucosa → se produce más ATP → la cascada de aprendizaje tiene combustible disponible.**

Es decir: **la misma señal que dice "hay que aprender" (Ca²⁺) también dice "preparen más energía" (al activar el metabolismo de glucosa en la mitocondria)**. Es un acople fisiológicamente elegante: cuando hace falta gastar mucho ATP en reconfiguración estructural, el sistema mismo se asegura de producirlo. Esto es lo más parecido a un "complejo" funcional entre calcio y glucosa, aunque a nivel molecular son moléculas distintas que no se unen estructuralmente.

#### Por qué importa esto para la imagen del aprendizaje

- **Aprender cuesta energía físicamente concreta**, no es una metáfora. Después de horas de estudio intenso, sentís cansancio mental porque literalmente bajó la glucosa en sangre y se acumularon metabolitos en zonas activas del cerebro.

- **Las regiones que aprenden mucho son las que consumen más glucosa**, y eso se puede medir directamente con técnicas como la **PET-FDG** (tomografía por emisión de positrones con glucosa marcada radiactivamente). En PET, las zonas más oscuras son las que están metabolizando más glucosa, es decir, las que están más activas.

- **La fMRI (resonancia magnética funcional)** mide indirectamente lo mismo: detecta el consumo de oxígeno, que sigue al consumo de glucosa, que sigue a la actividad neuronal con sus picos de Ca²⁺. Toda la neuroimagen funcional descansa sobre este acople metabólico.

- **Trastornos metabólicos afectan la cognición**: hipoglucemia severa produce confusión y eventualmente pérdida de conciencia, justamente porque las neuronas pierden la capacidad de mantener gradientes iónicos y de aprender. La diabetes mal controlada se asocia a deterioro cognitivo a largo plazo.

#### Conexión con el TP final

Este acople refuerza otra asimetría con los LLMs que vale tener en mente:

| | Cerebro humano | LLM |
|---|---|---|
| Combustible | Glucosa (~120 g/día) | Electricidad |
| Señal de aprendizaje | Ca²⁺ intracelular | Gradiente de error vía backprop |
| Acople señal-energía | Ca²⁺ activa el metabolismo de glucosa en la mitocondria — el aprendizaje "pide" su propia energía | El gradient descent no modula el consumo eléctrico del chip |
| Costo del aprendizaje | Variable, modulado por el sistema mismo (más actividad → más glucosa local) | Constante por paso de entrenamiento |
| Consecuencia de quedarse sin combustible | Neurodegeneración, muerte celular | El cómputo simplemente se detiene cuando se corta la corriente |

El cerebro tiene un **sistema metabólico inteligente** que adapta el consumo energético a la demanda cognitiva. Un LLM, en cambio, gasta electricidad de manera uniforme según el procesamiento, sin un sistema homeostático interno que regule el costo en función de lo que está aprendiendo. Es otra capa de divergencia mecanística entre los dos sistemas que la palabra "aprender" colapsa engañosamente.

#### Referencias

Para anclar académicamente esta sección:

- **Magistretti, P. J. y Allaman, I. (2015)** "A cellular perspective on brain energy metabolism and functional imaging". *Neuron*, 86(4), 883-901. **El review canónico contemporáneo** sobre cómo se acoplan actividad neural, consumo de glucosa y neuroimagen.
- **Attwell, D. y Laughlin, S. B. (2001)** "An energy budget for signaling in the grey matter of the brain". *Journal of Cerebral Blood Flow and Metabolism*, 21(10), 1133-1145. El cálculo clásico de cuánto cuesta cada potencial de acción y cada sinapsis en términos de ATP.
- **Rizzuto, R., De Stefani, D., Raffaello, A. y Mammucari, C. (2012)** "Mitochondria as sensors and regulators of calcium signalling". *Nature Reviews Molecular Cell Biology*, 13(9), 566-578. La revisión clave sobre cómo las mitocondrias absorben Ca²⁺ y lo usan para regular la producción de ATP.
- **McCormack, J. G., Halestrap, A. P. y Denton, R. M. (1990)** "Role of calcium ions in regulation of mammalian intramitochondrial metabolism". *Physiological Reviews*, 70(2), 391-425. **El paper fundacional** sobre la activación de enzimas mitocondriales por Ca²⁺. Es viejo pero sigue siendo la referencia.