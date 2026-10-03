# Transmisión sináptica, paso a paso

Del potencial de acción a la liberación del neurotransmisor. Es la secuencia que conviene poder recitar en orden, porque casi todo lo demás en neurofisiología se cuelga de ella: los fármacos, las patologías de la unión neuromuscular, la plasticidad y la codificación de información.

Esta entrada continúa donde termina **[bases físico-químicas](bases-fisicoquimicas.md)** — ahí están iones, voltaje, gradientes y canales; acá, qué hacen cuando el sistema se pone en marcha.

---

## La secuencia breve

1. **Reposo** — ~−70 mV.
2. **Despolarización local** → si alcanza el **umbral** (~−55 mV), dispara.
3. **Potencial de acción**: entra Na⁺ (sube a ~+40 mV) → sale K⁺ (**repolarización**) → hiperpolarización → período refractario.
4. **Conducción saltatoria** por el axón: se regenera en cada **nodo de Ranvier**.
5. Llega al **terminal presináptico** y lo despolariza.
6. Entra **Ca²⁺** — el paso que convierte lo eléctrico en químico.
7. **Fusión de la vesícula** (complejo SNARE) y **liberación del neurotransmisor**.
8. Unión a **receptores postsinápticos** → potencial postsináptico → vuelve al paso 2 en la neurona siguiente.

El resto de la entrada desarrolla cada bloque.

---

## Bloque A — El potencial de acción

### Reposo

La membrana está a ~**−70 mV** (negativa adentro). Lo mantiene la **bomba Na⁺/K⁺ ATPasa**, que saca 3 Na⁺ por cada 2 K⁺ que mete, consumiendo ATP. El resultado: mucho Na⁺ afuera, mucho K⁺ adentro, y un gradiente listo para usarse.

### Umbral y ley de todo o nada

La despolarización que llega desde otras sinapsis es **graduada**: puede ser chica o grande. El potencial de acción, en cambio, **no es graduado**. O se alcanza el umbral (~−55 mV) y se dispara completo, o no se dispara.

!!! info "La consecuencia de codificación"
    Si la amplitud es siempre la misma, la intensidad del estímulo no puede estar codificada en ella. Está codificada en la **frecuencia de disparo**. Esto es lo que vuelve a la tasa de descarga la variable central en electrofisiología, y es el origen de la noción de *rate coding*.

### Las fases

| Fase | Qué pasa a nivel de canales | Voltaje |
|---|---|---|
| **Despolarización** (fase ascendente) | se abren canales de **Na⁺** voltaje-dependientes; entra Na⁺, lo que abre más canales de Na⁺ — **retroalimentación positiva** | −55 → ~+40 mV |
| **Repolarización** | los canales de Na⁺ se **inactivan** (una compuerta distinta de la de apertura) y se abren los de **K⁺**, más lentos; sale K⁺ | +40 → −70 mV |
| **Hiperpolarización posterior** (*undershoot*) | los canales de K⁺ cierran con retraso | baja de −70 mV transitoriamente |

!!! warning "Error frecuente"
    El potencial de acción **no** es un paso entre la despolarización y la repolarización. **Es** esa secuencia. Listar "despolarización → potencial de acción → repolarización" como tres pasos sucesivos cuenta dos veces lo mismo.

### Períodos refractarios

- **Absoluto**: los canales de Na⁺ están inactivados y no hay estímulo que dispare otro potencial de acción.
- **Relativo**: se puede disparar, pero hace falta un estímulo mayor.

No es un detalle técnico: el período refractario **le da dirección a la propagación**. El impulso no puede volver hacia atrás, porque el tramo que acaba de disparar está inactivado. Y además **pone un techo a la frecuencia máxima** de disparo, lo que acota cuánta información puede transmitir un axón por unidad de tiempo.

---

## Bloque B — Propagación por el axón

### Conducción saltatoria

!!! danger "El error más común sobre la mielina"
    El impulso **no viaja "por la mielina"**. La mielina es un **aislante**: aumenta la resistencia de membrana y reduce su capacitancia, impidiendo que la corriente se fugue hacia afuera. La corriente fluye **pasivamente por el axoplasma** (el interior del axón) debajo de los tramos mielinizados, y el potencial de acción se **regenera activamente solo en los nodos de Ranvier**, donde se concentran los canales de Na⁺ voltaje-dependientes.

    La mielina acelera la conducción porque **impide** el paso de corriente por la membrana, no porque la conduzca.

De ahí el nombre: el impulso "salta" de nodo a nodo.

| | Axón amielínico | Axón mielínico |
|---|---|---|
| **Propagación** | continua, punto a punto | **saltatoria**, nodo a nodo |
| **Velocidad** | ~0,5-2 m/s | hasta ~120 m/s |
| **Costo metabólico** | alto (toda la membrana despolariza) | bajo (solo los nodos) |

### Quién produce la mielina

- **Oligodendrocitos** en el sistema nervioso central (cada uno mieliniza segmentos de varios axones).
- **Células de Schwann** en el sistema nervioso periférico (una célula por segmento de un solo axón).

Esa diferencia tiene consecuencias clínicas: explica por qué la **esclerosis múltiple** (central) y el **síndrome de Guillain-Barré** (periférico) son cuadros distintos, y por qué la regeneración es mucho mejor en el periférico.

La desmielinización **enlentece o bloquea la conducción sin que la neurona esté dañada**. Es un punto conceptual útil: se puede perder función sin perder neuronas.

---

## Bloque C — La sinapsis química

### El estado previo

Las vesículas no flotan sueltas. Están en la **zona activa** del terminal, en dos estados que conviene distinguir:

- **Acopladas** (*docked*) — pegadas a la membrana presináptica.
- **Cebadas** (*primed*) — con el complejo de fusión semiensamblado, listas para soltar en microsegundos.

### Los pasos

1. **El potencial de acción invade el terminal** y lo despolariza.
2. **Se abren canales de Ca²⁺ voltaje-dependientes** (tipo P/Q y N), concentrados en la zona activa.
3. **Entra Ca²⁺**, a favor de un gradiente enorme: ~2 mM afuera contra ~100 nM adentro, unas 10.000 veces de diferencia.

!!! info "El paso que no hay que saltear"
    La **entrada de Ca²⁺ es el eslabón que convierte la señal eléctrica en química.** Sin Ca²⁺ no hay liberación, por más potencial de acción que llegue al terminal. En las versiones abreviadas de la secuencia este paso es el que más se omite, y es el único que no se puede omitir.

4. **El Ca²⁺ se une a la sinaptotagmina-1**, el sensor de calcio de la vesícula, que desplaza a la **complexina** — hasta ese momento, el freno del complejo de fusión.
5. **Exocitosis**, ejecutada por el **complejo SNARE**:

| Proteína | Ubicación |
|---|---|
| **Sinaptobrevina (VAMP)** | membrana de la vesícula (v-SNARE) |
| **Sintaxina-1** y **SNAP-25** | membrana plasmática (t-SNAREs) |

Las tres se enrollan entre sí y tiran de ambas membranas hasta fusionarlas.

6. **Liberación a la hendidura sináptica**, que mide **20-40 nm**. La liberación es **cuántica**: ocurre en múltiplos del contenido de una vesícula —un "cuanto"—, lo que estableció **Katz**. No es un chorro graduable, son paquetes discretos.
7. **Difusión** por la hendidura, en menos de un milisegundo.
8. **Unión a receptores postsinápticos.** Acá la vía se bifurca, y la distinción es importante:

| | Ionotrópicos | Metabotrópicos |
|---|---|---|
| **Qué son** | el receptor **es** el canal iónico | acoplados a proteína G, actúan vía segundos mensajeros |
| **Latencia** | milisegundos | cientos de ms a segundos |
| **Ejemplos** | AMPA, NMDA, GABA_A, nicotínico, glicina | mGluR, GABA_B, muscarínico, dopaminérgicos, serotoninérgicos |
| **Rol típico** | transmisión rápida punto a punto | **modulación** del estado del circuito |

9. **Potencial postsináptico**, graduado y local:
    - **PEPS** (excitatorio): entra Na⁺ o Ca²⁺ → despolariza → acerca al umbral.
    - **PIPS** (inhibitorio): entra Cl⁻ o sale K⁺ → hiperpolariza → aleja del umbral.
10. **Integración** en el soma: **sumación espacial** (varias sinapsis a la vez) y **temporal** (una misma sinapsis en ráfaga). Si la suma alcanza el umbral en el **segmento inicial del axón** —no en el soma—, se dispara un potencial de acción nuevo.

### Terminación de la señal

Tres vías, no una. Que la señal se corte es tan necesario como que se produzca:

- **Recaptación** por transportadores, hacia la neurona o hacia la glía: **DAT** (dopamina), **SERT** (serotonina), **NET** (noradrenalina), **EAAT/GLT-1** (glutamato), **GAT** (GABA).
- **Degradación enzimática**: la **acetilcolinesterasa** es el caso canónico; **MAO** y **COMT** para monoaminas.
- **Difusión** fuera de la hendidura.

### Reciclado

Endocitosis mediada por **clatrina** y **dinamina**, y recarga de la vesícula mediante transportadores vesiculares (**VGLUT, VMAT, VGAT**) que aprovechan el gradiente de protones generado por la **V-ATPasa**.

---

## El retardo sináptico

La transmisión química tarda **~0,5-1 ms**, y el paso que determina ese tiempo es la entrada de Ca²⁺ y la fusión vesicular.

No es un detalle: una cadena de muchas sinapsis es necesariamente lenta, y **contar sinapsis sirve para estimar tiempos de procesamiento**. Es uno de los argumentos clásicos para acotar cuántas etapas puede tener un proceso cognitivo que se completa en, digamos, 200 ms — el tipo de razonamiento que sostiene la lectura de latencias en [potenciales evocados](../metodologia/n400-p600-potenciales.md).

---

## Modulación: la sinapsis no es una vía de un solo sentido

- **Autorreceptores presinápticos** (D2, α2, GABA_B): el propio terminal detecta cuánto neurotransmisor liberó y **frena la liberación**. Retroalimentación negativa local.
- **Señalización retrógrada**: la neurona postsináptica manda señales hacia atrás, sobre todo vía **endocannabinoides**, que reducen la liberación presináptica.

Esto importa porque desarma la imagen de la sinapsis como un cable con dirección fija. Hay control en ambos sentidos.

---

## Sinapsis eléctrica, para contrastar

Todo lo anterior es la **sinapsis química**. La **eléctrica** —uniones *gap*, formadas por **conexinas**— saltea los bloques de Ca²⁺, vesícula y receptor por completo:

| | Química | Eléctrica |
|---|---|---|
| **Mecanismo** | neurotransmisor, vesículas, receptores | citoplasmas conectados, la corriente pasa directo |
| **Retardo** | ~0,5-1 ms | prácticamente nulo |
| **Dirección** | unidireccional | típicamente **bidireccional** |
| **Plasticidad** | alta | baja |
| **Dónde abunda** | casi todo el SNC | sincronización rápida: retina, interneuronas, glía |

Más sobre esto en **[sincitio y la doctrina de la neurona](sincitio.md)** — históricamente, la existencia de uniones *gap* fue el argumento tardío a favor de la intuición de Golgi.

---

## Por qué conviene saber la lista en orden

Porque casi cada paso tiene un fármaco o una patología asociada, y es la forma más rápida de fijarla:

| Paso | Qué lo ataca |
|---|---|
| Canal de Na⁺ (bloque A) | **tetrodotoxina**; anestésicos locales como la lidocaína |
| Mielina (bloque B) | **esclerosis múltiple**, **Guillain-Barré** |
| Canal de Ca²⁺ presináptico | **síndrome de Lambert-Eaton** (anticuerpos anti-canal) |
| Complejo SNARE | **toxina botulínica** (corta SNAP-25 y sintaxina), **toxina tetánica** (corta sinaptobrevina) |
| Receptor nicotínico | **miastenia gravis** (anticuerpos anti-receptor) |
| Receptor NMDA | **encefalitis anti-NMDAR**; ketamina y fenciclidina como antagonistas |
| Recaptación | **ISRS** (bloquean SERT), cocaína y metilfenidato (DAT) |
| Degradación | **organofosforados**, donepecilo (inhiben acetilcolinesterasa) |

La lógica de la tabla es útil por sí misma: un cuadro clínico puede surgir de **cualquier** eslabón de la cadena, y cuadros que se parecen en la superficie (debilidad muscular) pueden venir de pasos distintos.

---

## Errores frecuentes, resumidos

| Formulación habitual | Qué corregir |
|---|---|
| "despolarización → potencial de acción → repolarización" | el potencial de acción **es** despolarización + repolarización, no un paso intermedio |
| "el impulso viaja por la mielina" | viaja por el **axoplasma** y se regenera en los **nodos de Ranvier**; la mielina **aísla** |
| "llega el potencial de acción y se libera el neurotransmisor" | falta la **entrada de Ca²⁺**, que es el disparador real de la liberación |
| "el umbral se alcanza en el soma" | se alcanza en el **segmento inicial del axón**, donde la densidad de canales de Na⁺ es mayor |
| "más estímulo, más grande el potencial de acción" | es **todo o nada**; más estímulo significa **más frecuencia** |

---

## Conexiones con el sitio

- **[Bases físico-químicas para entender la neurona](bases-fisicoquimicas.md)** — iones, voltaje, gradientes y selectividad de canales. Es el prerrequisito directo de esta entrada.
- **[Sincitio y la doctrina de la neurona](sincitio.md)** — la sinapsis eléctrica y el debate Golgi-Cajal.
- **[Plasticidad estructural y sináptica](plasticidad-estructural-mecanismos.md)** — LTP y LTD son modificaciones de la eficacia de los pasos 8 y 9; los receptores AMPA y NMDA son el sustrato.
- **[Sinaptogénesis y poda sináptica](sinaptogenesis-poda-sinaptica.md)** — cómo se forman y se eliminan estas sinapsis durante el desarrollo. La poda selecciona según la **actividad**, es decir según cuánto se usó esta maquinaria.
- **[Neuronas tipo ensamble](neuronas-ensamble.md)** — la regla de Hebb opera sobre la coincidencia temporal de estos potenciales postsinápticos.
- **[Arousal](arousal.md)** — los sistemas moduladores (noradrenalina, acetilcolina) actúan sobre receptores metabotrópicos, que es la columna derecha de la tabla del paso 8.
- **[N400 y P600](../metodologia/n400-p600-potenciales.md)** — lo que se registra en un ERP es la suma de potenciales postsinápticos (paso 9) de poblaciones grandes de neuronas alineadas, no potenciales de acción.

---

## Lecturas

- **Kandel, E. R., Schwartz, J. H., Jessell, T. M., Siegelbaum, S. A. & Hudspeth, A. J.** *Principles of Neural Science* (hay traducción, *Principios de Neurociencia*) — los capítulos sobre potencial de acción, transmisión sináptica y liberación de neurotransmisores. **La referencia estándar**, y la que conviene tener a mano para esta secuencia.
- **Hodgkin, A. L. & Huxley, A. F. (1952)** "A quantitative description of membrane current and its application to conduction and excitation in nerve". *Journal of Physiology* 117(4):500-544. — el modelo del potencial de acción, y uno de los trabajos más influyentes de la biología del siglo XX.
- **Katz, B. (1969)** *The Release of Neural Transmitter Substances*. Liverpool University Press. — la naturaleza cuántica de la liberación.
- **Südhof, T. C. (2013)** "Neurotransmitter release: the last millisecond in the life of a synaptic vesicle". *Neuron* 80(3):675-690. — revisión del mecanismo SNARE por uno de los autores del Nobel 2013.
- **Purves, D. et al.** *Neuroscience* — alternativa a Kandel, con figuras más claras para la conducción saltatoria.
