# Sinaptogénesis y poda sináptica

El desarrollo del cerebro no consiste en ir agregando conexiones hasta llegar al cerebro adulto. Consiste en **fabricar muchas más sinapsis de las que van a quedar y después eliminar la mayoría**. Esas son las dos fases: **sinaptogénesis** (formación) y **poda sináptica** (*synaptic pruning*, eliminación selectiva).

La poda es la parte contraintuitiva y la más interesante. Es **constructiva, no degenerativa**: el circuito funcional no es lo que queda después de una pérdida, es lo que la eliminación esculpe. Y es, además, la fuente del malentendido más influyente que la neurociencia exportó a la educación.

!!! note "Por qué importa acá"
    La curva de densidad sináptica a lo largo del desarrollo es **la base empírica sobre la que se construyó el "mito de los tres primeros años"**. Entender bien la curva —y las limitaciones de los datos que la sostienen— es lo que permite ver por qué el argumento no se sigue. Es el caso testigo de cómo un hallazgo neurobiológico sólido genera una recomendación educativa infundada.

---

## 1. Las dos fases

| | Sinaptogénesis | Poda sináptica |
|---|---|---|
| **Qué hace** | Forma sinapsis en exceso respecto del estado adulto | Elimina selectivamente un subconjunto grande |
| **Cuándo** | Prenatal y primeros años, con picos regionales distintos | Infancia tardía, adolescencia y, en corteza prefrontal, hasta la tercera década |
| **Qué la guía** | Principalmente **programas genéticos** y señales moleculares | Principalmente **actividad neural**, es decir experiencia |
| **Lectura errónea frecuente** | "más sinapsis = más capacidad" | "poda = pérdida de potencial" |

La asimetría de la tercera fila es el punto importante. La sobreproducción es relativamente insensible al ambiente; **la eliminación es donde la experiencia entra**. Un cerebro que produce de más y después recorta según el uso puede terminar especificado con mucha más precisión de la que el genoma podría codificar directamente.

---

## 2. Por qué un sistema haría esto

Hay una razón de diseño, y tiene un nombre: el desarrollo neural funciona por **selección**, no por instrucción.

- **El problema del genoma insuficiente.** El genoma humano no tiene capacidad informativa para especificar cuál de ~10¹⁴ sinapsis va dónde. Lo que sí puede especificar es una regla: *producí conexiones de más en esta región, y conservá las que resulten funcionalmente coherentes con la actividad que llega*.
- **Darwinismo neural** (Changeux, Edelman). La variabilidad se genera primero y la selección actúa después, igual que en evolución. Edelman lo llamó *neural Darwinism*; Changeux, **estabilización selectiva**.
- **El ambiente hace el trabajo fino.** Esto permite que el circuito se ajuste a un cuerpo y un entorno que el genoma no puede anticipar: la longitud exacta de los miembros, las propiedades ópticas de ese ojo, los fonemas de esa lengua.

Dicho de otro modo: la poda es **el mecanismo por el cual la experiencia se inscribe en la arquitectura**. No es el precio del desarrollo, es su herramienta.

---

## 3. Sinaptogénesis: cómo se forma una sinapsis

Resumido, porque el foco de esta entrada está en la otra fase:

1. El **axón crece** guiado por moléculas de atracción y repulsión (netrinas, semaforinas, efrinas, Slit) que lee el cono de crecimiento.
2. **Contacto inicial** entre un filopodio dendrítico y el axón; adhesión mediada por **cadherinas, neurexinas-neuroliguinas, SynCAM**.
3. **Diferenciación**: el lado presináptico acumula vesículas y maquinaria de liberación; el postsináptico ensambla la densidad postsináptica (PSD-95, receptores AMPA y NMDA).
4. **Maduración o eliminación**, según la actividad. La mayoría de los contactos iniciales **no sobrevive**: muchos filopodios transitorios representan sinaptogénesis fallida, no sinapsis funcionales de vida corta.

La sinaptogénesis arranca en el feto —en corteza humana, **antes de las 27 semanas de edad conceptual**— y continúa con fuerza en los primeros años.

---

## 4. La poda: qué se elimina y con qué criterio

### La regla básica: actividad correlacionada

La sinapsis que sobrevive es la que participa de **actividad coherente con la de sus vecinas**. La formulación clásica es hebbiana, con su contracara:

- *Neurons that fire together, wire together* → la sinapsis se estabiliza.
- **"Use it or lose it"** → la sinapsis con actividad escasa, o descorrelacionada de la de su población, se marca para eliminación.

El experimento canónico es la **competencia binocular** en corteza visual: si se priva de visión un ojo durante el período crítico, las sinapsis que llevan información de ese ojo pierden territorio cortical frente a las del ojo abierto. No es que se degraden por falta de uso en abstracto: **pierden una competencia** por espacio postsináptico. La poda es competitiva.

### El mecanismo celular: microglía y complemento

Durante mucho tiempo se describió la poda sin saber **quién** ejecutaba la eliminación. La respuesta llegó en los 2000-2010 y resultó ser el sistema inmune del cerebro, reutilizado para una función de desarrollo. Tres trabajos la establecieron:

- **Stevens et al. (2007)**, *Cell*: las proteínas del **complemento C1q y C3** —parte de la cascada inmune innata— se localizan en sinapsis durante el desarrollo y funcionan como una **etiqueta molecular de "eliminar esto"**. En ratones sin C1q o sin C3, la poda de las proyecciones retinogeniculadas falla y persisten conexiones inmaduras.
- **Paolicelli et al. (2011)**, *Science*: la **microglía** —las células inmunes residentes del cerebro— **fagocita material sináptico** durante el desarrollo. En ratones deficientes en el receptor **CX3CR1** (que detecta la quimiocina neuronal CX3CL1, una señal de tipo *"find me"*), hay exceso de espinas dendríticas y maduración sináptica deficiente.
- **Schafer et al. (2012)**, *Neuron*: la microglía engloba sinapsis vía el receptor de complemento **CR3**, y lo hace preferentemente sobre las sinapsis **menos activas**. Esto cierra el circuito: da el mecanismo molecular por el cual una regla de actividad se traduce en eliminación física.

!!! info "El concepto que vale la pena retener"
    La poda sináptica es **fagocitosis dirigida**. El cerebro marca químicamente las sinapsis débiles con proteínas del complemento y una célula inmune se las come. No es desuso pasivo ni atrofia: es un proceso activo, con ejecutor identificado, etiquetas moleculares y receptores específicos.

### No es solo sinapsis

La misma lógica de sobreproducción y eliminación opera en otras escalas, y conviene no confundirlas:

- **Muerte neuronal programada (apoptosis)**: en varias poblaciones se producen muchas más neuronas de las que sobreviven, y la supervivencia depende de obtener factores tróficos del blanco. Es un nivel distinto del de la poda sináptica.
- **Poda axonal**: ramas axonales completas se retraen o se eliminan, incluidas proyecciones de larga distancia, con participación de microglía (**trogocitosis**) y complemento.
- **Eliminación de espinas dendríticas**: en corteza, la medida más usada en humanos es la **densidad de espinas**, que es un proxy de sinapsis excitatorias.

---

## 5. La cronología humana: qué dicen los datos y qué tan buenos son

Acá hay que tener cuidado, porque la curva que aparece en los manuales descansa sobre menos datos de lo que su ubicuidad sugiere.

### Huttenlocher: el trabajo fundacional

**Huttenlocher**, desde fines de los 70, contó sinapsis con **microscopía electrónica en tejido post mortem** humano de distintas edades y estableció el patrón general: una fase de **sinaptogénesis exuberante** seguida de una fase de **eliminación neta**.

**Huttenlocher & Dabholkar (1997)**, en *Journal of Comparative Neurology*, es el paper que conviene citar, porque compara dos regiones:

| Región | Pico de densidad sináptica | Fin de la fase de eliminación |
|---|---|---|
| **Corteza auditiva** (giro de Heschl) | ~**3 meses** postnatales | hacia los **12 años** |
| **Corteza prefrontal** (giro frontal medio) | **después de los 15 meses** | se extiende a la **adolescencia media** |

### La limitación metodológica, que es grande

Los estudios de Huttenlocher se apoyan en un **número reducido de cerebros post mortem**, y —el dato más citado por quienes revisan la literatura— hay **un solo cerebro en todo el rango entre 15 y 32 años**. La porción adolescente y adulta temprana de la curva más famosa del desarrollo cortical estaba, durante décadas, sostenida por un caso.

Esto no invalida el patrón general, que replicó. Pero sí significa que **la forma precisa y el momento exacto del descenso no estaban bien establecidos**, y la precisión importa mucho cuando alguien quiere derivar de ahí una ventana de intervención educativa.

### Petanjek: la corrección

**Petanjek et al. (2011)**, en *PNAS* ("Extraordinary neoteny of synaptic spines in the human prefrontal cortex"), midió densidad de espinas dendríticas en **32 cerebros, de una semana a 91 años**. Encontró que en corteza prefrontal el crecimiento dendrítico y la proliferación de espinas se prolongan hasta la **infancia tardía**, y que la eliminación posterior **se extiende a lo largo de la segunda y la tercera década de vida**.

O sea: la poda prefrontal humana **no termina en la adolescencia; sigue hasta cerca de los 30**. El título del paper no exagera — es neotenia: una prolongación extraordinaria de un rasgo juvenil.

### El correlato metabólico

**Chugani** midió consumo de glucosa cortical con **PET** y obtuvo una curva de forma similar, que suele presentarse como confirmación independiente:

- Al nacer, el metabolismo cortical está **~30% por debajo** del adulto.
- A los **3 años** supera el nivel adulto en **más del doble**.
- Desde la pubertad desciende, y llega a valores adultos hacia los **16-18 años**.

Vale ser preciso sobre qué es esto: **una medida de consumo energético, no un conteo de sinapsis**. La interpretación de que refleja densidad sináptica es razonable e indirecta. Es un correlato, no una medición del fenómeno.

---

## 6. Heterocronía: no hay *una* ventana

Un hallazgo de Huttenlocher & Dabholkar que suele perderse en la divulgación, y que es decisivo:

En humanos, la sinaptogénesis y la poda son **heterocrónicas** — ocurren en momentos distintos en regiones distintas. En el macaco rhesus, en cambio, los trabajos de **Rakic** y colaboradores encontraron un patrón **concurrente**: la sobreproducción sucede más o menos al mismo tiempo en regiones diversas de la corteza.

La consecuencia conceptual es grande: **en el cerebro humano no hay una ventana única de plasticidad, sino un escalonamiento de ventanas por región y por función**. La corteza auditiva primaria termina su fase de eliminación cuando la prefrontal todavía está produciendo. Cualquier afirmación del tipo "la ventana del aprendizaje se cierra a los X años" tiene que especificar **qué región y qué función**, y una vez que lo especifica deja de ser una afirmación general sobre el aprendizaje.

---

## 7. Poda y períodos críticos

La poda está íntimamente ligada a la noción de **período crítico** (una ventana en la que cierta experiencia es necesaria y después de la cual el circuito ya no se reorganiza igual) y de **período sensible** (ventana de mayor facilidad, sin la rigidez del "todo o nada").

El trabajo de **Hensch** en corteza visual estableció dos principios que conviene conocer porque reencuadran todo el tema:

1. **Lo que abre el período crítico es la maduración de la inhibición.** El disparador es el **balance excitación/inhibición**, y específicamente la maduración de las interneuronas **parvalbúmina positivas** de tipo *large basket cell*, que inervan el soma de sus blancos con sinapsis GABA_A que contienen la subunidad **α1**. No es que el período crítico "esté abierto por defecto y después se cierre": se **abre** cuando la inhibición madura.
2. **Lo que lo cierra son "frenos" moleculares activos.** La plasticidad adulta está **activamente restringida** por mecanismos que se regulan al alza durante el desarrollo — entre ellos las **redes perineuronales** (matriz extracelular de condroitín sulfato que envuelve preferentemente a esas mismas interneuronas PV+), más señalización de mielina (Nogo/PirB) y otros.

Y el corolario experimental, que es el que más importa para la discusión educativa: **esos frenos se pueden levantar**. Degradar las redes perineuronales con **condroitinasa** reactiva la plasticidad de dominancia ocular en animales adultos. Reducir la inhibición perisomática permite inducir cambios de dominancia ocular en la adultez.

!!! warning "Reencuadre importante"
    Si el cierre de un período crítico es un **proceso activo con frenos identificables**, entonces no es una ventana que se cierra por agotamiento ni una oportunidad biológica que se pierde. Es un **estado regulado**. Eso cambia por completo la retórica de la urgencia: lo que la biología describe no es "ahora o nunca", es "ahora es más fácil, y por mecanismos que empiezan a entenderse".

---

## 8. Cuando la poda falla: evidencia clínica en dos direcciones

Esta es la evidencia más fuerte de que la poda importa funcionalmente, y es elegante porque los dos cuadros apuntan en sentidos opuestos.

### Exceso de poda: esquizofrenia

**Feinberg (1982-83)** propuso que la esquizofrenia resulta de una poda aberrante durante la adolescencia — en su formulación, que *"se eliminan demasiadas, demasiado pocas, o las sinapsis equivocadas"*. La hipótesis explicaba bien dos cosas: el **momento de inicio** del cuadro (adolescencia tardía y adultez temprana, justo la ventana de poda prefrontal) y la reducción de densidad sináptica observada en tejido post mortem. Versiones posteriores la refinaron como **poda excesiva en circuitos prefrontales** combinada con poda insuficiente en circuitos subcorticales.

Durante tres décadas fue una hipótesis plausible sin mecanismo. Después llegó **Sekar et al. (2016)**, en *Nature*: el locus de mayor asociación genética con esquizofrenia en todo el genoma —la región del **MHC**— se explica en buena medida por **variación estructural del gen del complemento C4**. Los alelos de C4 se asocian a esquizofrenia **en proporción a cuánta expresión de C4A generan en el cerebro**, y en ratones C4 media la eliminación sináptica durante el desarrollo postnatal.

Es decir: la señal genética más fuerte de la esquizofrenia apunta a **una molécula de la maquinaria de poda**. Eso convirtió una hipótesis de los 80 en un programa mecanístico. Conviene igual leerla con los criterios habituales: sigue siendo una hipótesis en desarrollo, la relación entre expresión de C4A y poda en humanos vivos no está medida directamente, y hay revisiones que discuten cuánto de la reducción sináptica observada es poda excesiva y cuánto otros procesos.

### Déficit de poda: autismo

**Tang et al. (2014)**, en *Neuron*, encontró en tejido post mortem de lóbulo temporal de personas con autismo **mayor densidad de espinas dendríticas** en neuronas piramidales de capa V, con **reducción de la poda** del desarrollo. El déficit correlacionaba con **hiperactivación de mTOR** y **autofagia deficiente** — es decir, con la vía que la célula usa para degradar sus propios componentes.

Y la parte causal: inhibir mTORC1 con **rapamicina** corrigió la poda de espinas y la conducta social en ratones *Tsc2*⁺/⁻, pero **no** en ratones con autofagia neuronal deficiente (*Atg7* condicional). Esa disociación es lo que ubica a la autofagia como el paso necesario, en lugar de dejar el resultado en "rapamicina mejora cosas".

**La lectura conjunta**: demasiada poda y demasiado poca poda producen cuadros distintos y severos. Más sinapsis **no es mejor**. Hay un rango, y el desarrollo típico consiste en acertarle.

---

## 9. El neuromito: por qué la curva no justifica "los tres primeros años"

Este es el punto por el cual el tema aparece en cualquier materia de neurociencia y educación.

**El argumento que circuló** en los 90 y que sigue circulando, en versiones de divulgación, política pública y capacitación docente:

> La densidad sináptica alcanza su máximo en la primera infancia y después se poda. Entonces los primeros tres años son una ventana irrepetible: lo que no se estimula ahí se pierde para siempre.

**Bruer (1997)**, en "Education and the brain: a bridge too far", y después en sus textos sobre el mito de los tres primeros años, desarmó la cadena. Los problemas, ordenados:

1. **La premisa temporal es falsa.** La sinaptogénesis del desarrollo **no está confinada a los primeros tres años**. El argumento de Bruer es directo: si el período crítico fuera el de pico de densidad sináptica, ese período **no es de cero a tres** — en corteza prefrontal el pico llega después, y con Petanjek et al. (2011) sabemos que la eliminación se extiende hasta la tercera década. La ventana que el argumento invoca no coincide con la que los datos muestran.
2. **Hay heterocronía, no una ventana.** Como arriba: cada región tiene su cronología. "La ventana" no existe en singular.
3. **El salto de "más sinapsis" a "más capacidad de aprender" no tiene apoyo.** Es el error conceptual central. El pico de densidad sináptica es el momento de **máxima redundancia**, no de máxima competencia cognitiva. Un chico de 3 años tiene más sinapsis que un adulto y menos capacidad de aprendizaje en casi todos los dominios medibles. Si la densidad fuera la variable, la relación sería la inversa de la observada. Y los dos cuadros clínicos de la sección anterior muestran que el exceso de sinapsis es un problema, no un activo.
4. **Confusión entre privación y enriquecimiento.** La evidencia de períodos sensibles proviene mayormente de experimentos de **privación** (sutura de párpado, aislamiento, los casos de institucionalización extrema). Que privar de lo mínimo cause daño duradero **no implica** que agregar estimulación por encima de lo típico produzca beneficio proporcional. Son dos afirmaciones distintas y solo una está apoyada. Los experimentos de "ambiente enriquecido" en roedores comparan, en rigor, un ambiente algo menos empobrecido contra una jaula estándar — no un ambiente normal contra uno superior.
5. **El "entorno enriquecido" de laboratorio no se traduce a currículum.** No hay evidencia de que los efectos de una jaula con ruedas y túneles mapeen sobre decisiones pedagógicas concretas, como qué actividades conviene hacer a los 2 años.
6. **La genealogía del argumento.** La observación de Bruer que vale citar: lo que se presentaba como descubrimientos recientes era en realidad **neurociencia vieja, seleccionada, simplificada y sobregeneralizada**, ensamblada para apoyar una agenda de financiamiento (en EE.UU., programas de cero a tres). La agenda podía ser buena; el argumento neurocientífico era malo. Son cosas separables, y conviene separarlas — porque una política fundada en un argumento frágil queda rehén de que ese argumento no se caiga.

!!! danger "El costo de este mito"
    No es solo un error técnico. Tiene dos efectos prácticos: genera **ansiedad parental** y una industria de productos de estimulación temprana sin evidencia; y, más grave, **desalienta la inversión después de los tres años** sugiriendo que la oportunidad ya pasó — cuando la corteza prefrontal, que sostiene las funciones ejecutivas más relevantes para la escolaridad, está en reorganización activa durante toda la adolescencia y parte de la adultez.

---

## 10. Qué sigue pasando en el cerebro adulto

El cierre de la discusión anterior es empírico: la **formación y eliminación de sinapsis no se detienen**. Lo que cambia es el balance.

La imagen por **microscopía de dos fotones** en animales vivos permitió seguir espinas dendríticas individuales a lo largo del tiempo (**Trachtenberg et al. 2002**; **Holtmaat et al. 2005, 2006**). Lo que se ve en el adulto:

- Formación y eliminación están **en equilibrio**: hay recambio, pero la densidad neta es estable.
- La magnitud del recambio es **modesta**: en ratones adultos, del orden de **3-5% de las espinas** se forma y se elimina en dos semanas; en corteza de barriles, a lo largo de **18 meses** se eliminó un 26% y se formó un 19%.
- Existe una **población mayoritariamente estable** de espinas, candidata a sustrato físico del almacenamiento de información a largo plazo.
- El **aprendizaje motor** se asocia a formación de espinas nuevas, y —el dato más informativo— lo que predice la retención no es cuántas se forman sino **cuántas se estabilizan**. Hay un límite a esa estabilización, y es manipulable experimentalmente.

Dos lecturas simultáneas, y conviene sostener las dos: el cerebro adulto **no está fijo**, y tampoco es tan plástico como un cerebro en desarrollo. Ni "el cerebro adulto es inmodificable" ni "la plasticidad lo permite todo a cualquier edad".

---

## 11. Resumen por niveles de confianza

| Afirmación | Estado |
|---|---|
| El desarrollo cortical incluye sobreproducción sináptica seguida de eliminación neta | **Establecido** |
| La poda depende de actividad neural y es competitiva | **Establecido** |
| La microglía ejecuta la eliminación, con el complemento (C1q/C3) como etiqueta | **Establecido** en modelos animales |
| En humanos la cronología es heterocrónica por región | **Bien apoyado** (Huttenlocher & Dabholkar 1997) |
| La poda prefrontal humana se extiende a la tercera década | **Bien apoyado** (Petanjek et al. 2011) |
| Los períodos críticos se abren por maduración de la inhibición y se cierran por frenos moleculares | **Bien apoyado** en corteza visual de roedor |
| La esquizofrenia involucra poda aberrante, con C4 como mecanismo candidato | **En disputa / programa activo** — señal genética fuerte, mecanismo humano no medido directamente |
| El autismo involucra poda deficiente vía mTOR-autofagia | **En disputa** — evidencia post mortem y modelos animales, muestras chicas |
| Más densidad sináptica implica mayor capacidad de aprendizaje | **Falso** |
| La curva de densidad sináptica justifica priorizar la intervención de 0 a 3 años | **No se sigue** — la premisa temporal es incorrecta y el salto inferencial no tiene apoyo |

---

## Conexiones con el sitio

- **[Plasticidad estructural y sináptica](plasticidad-estructural-mecanismos.md)** — LTP/LTD, desenmascaramiento sináptico y brotes axonales son la maquinaria que opera sobre las sinapsis que la poda conservó. La poda del desarrollo y la plasticidad post-lesión comparten mecanismos.
- **[Plasticidad — experimentos fundacionales](plasticidad-experimentos-fundacionales.md)** — Merzenich, Kaas & Killackey y Wall & Egger mostraron reorganización en el adulto; la sección 10 de esta entrada es el complemento celular de esos resultados.
- **[Epigenética](epigenetica.md)** — el otro gran mecanismo candidato para explicar "cómo el ambiente temprano se mete en el cerebro", con los mismos riesgos de sobreinterpretación educativa. Las dos entradas se leen bien juntas.
- **[Ontogenia y filogenia](ontogenia-filogenia.md)** — la neotenia de la poda prefrontal humana es un rasgo filogenético: lo que distingue el desarrollo cortical humano del de otros primates no es tanto el pico como **cuánto se prolonga el descenso**. Y la heterocronía humana vs. la concurrencia del macaco es una diferencia de especie, no un detalle técnico.
- **[Neuronas tipo ensamble](neuronas-ensamble.md)** — la regla de Hebb es la misma que gobierna qué sinapsis sobrevive a la poda; acá se ve en su versión negativa.
- **[Las 4 preguntas de Tinbergen](tinbergen-niveles-analisis.md)** — la poda admite respuesta en los cuatro planos, y la discusión educativa suele mezclar el mecanismo (microglía, complemento) con la ontogenia (cronología) y derivar de ambos una recomendación que no es ninguno de los dos.
- **[La crisis de replicación](../metodologia/crisis-replicacion.md)** — el caso de Huttenlocher es instructivo en un sentido distinto del habitual: no es fraude ni mala práctica, es un hallazgo real cuyo rango de datos era delgado y que la literatura secundaria citó durante décadas como si fuera denso.

---

## Fuentes

**La cronología humana**

- **Huttenlocher, P. R. (1979)** "Synaptic density in human frontal cortex — developmental changes and effects of aging". *Brain Research* 163(2):195-205. — el trabajo que estableció el patrón.
- **Huttenlocher, P. R. & Dabholkar, A. S. (1997)** "Regional differences in synaptogenesis in human cerebral cortex". *Journal of Comparative Neurology* 387(2):167-178. — **la referencia central.** Corteza auditiva vs. prefrontal, y el hallazgo de heterocronía en humanos frente a concurrencia en rhesus.
- **Petanjek, Z., Judaš, M., Šimić, G., Rašin, M. R., Uylings, H. B. M., Rakic, P. & Kostović, I. (2011)** "Extraordinary neoteny of synaptic spines in the human prefrontal cortex". *PNAS* 108(32):13281-13286. — [acceso abierto](https://www.pnas.org/doi/10.1073/pnas.1105108108). 32 cerebros; la poda prefrontal hasta la tercera década.
- **Rakic, P., Bourgeois, J.-P., Eckenhoff, M. F., Zecevic, N. & Goldman-Rakic, P. S. (1986)** "Concurrent overproduction of synapses in diverse regions of the primate cerebral cortex". *Science* 232:232-235.
- **Chugani, H. T. (1998)** "A critical period of brain development: studies of cerebral glucose utilization with PET". *Preventive Medicine* 27(2):184-188. — la curva metabólica. Útil, e indirecta.

**El mecanismo de la poda**

- **Stevens, B. et al. (2007)** "The classical complement cascade mediates CNS synapse elimination". *Cell* 131(6):1164-1178. — el complemento como etiqueta.
- **Paolicelli, R. C. et al. (2011)** "Synaptic pruning by microglia is necessary for normal brain development". *Science* 333(6048):1456-1458. — la microglía como ejecutora; CX3CR1.
- **Schafer, D. P. et al. (2012)** "Microglia sculpt postnatal neural circuits in an activity and complement-dependent manner". *Neuron* 74(4):691-705. — el vínculo entre actividad y eliminación, vía CR3.
- **Changeux, J.-P. & Danchin, A. (1976)** "Selective stabilisation of developing synapses as a mechanism for the specification of neuronal networks". *Nature* 264:705-712. — la formulación teórica original de la selección.

**Períodos críticos**

- **Hensch, T. K. (2005)** "Critical period plasticity in local cortical circuits". *Nature Reviews Neuroscience* 6(11):877-888. — **la revisión que hay que leer** sobre disparadores y frenos.
- **Hubel, D. H. & Wiesel, T. N. (1970)** "The period of susceptibility to the physiological effects of unilateral eye closure in kittens". *Journal of Physiology* 206(2):419-436. — el experimento fundacional.
- **Pizzorusso, T. et al. (2002)** "Reactivation of ocular dominance plasticity in the adult visual cortex". *Science* 298:1248-1251. — condroitinasa y redes perineuronales.

**Poda alterada**

- **Feinberg, I. (1982-83)** "Schizophrenia: caused by a fault in programmed synaptic elimination during adolescence?". *Journal of Psychiatric Research* 17(4):319-334.
- **Sekar, A. et al. (2016)** "Schizophrenia risk from complex variation of complement component 4". *Nature* 530:177-183.
- **Tang, G. et al. (2014)** "Loss of mTOR-dependent macroautophagy causes autistic-like synaptic pruning deficits". *Neuron* 83(5):1131-1143.

**Plasticidad adulta**

- **Trachtenberg, J. T. et al. (2002)** "Long-term in vivo imaging of experience-dependent synaptic plasticity in adult cortex". *Nature* 420:788-794.
- **Holtmaat, A. et al. (2005)** "Transient and persistent dendritic spines in the neocortex in vivo". *Neuron* 45(2):279-291.

**La crítica educativa**

- **Bruer, J. T. (1997)** "Education and the brain: a bridge too far". *Educational Researcher* 26(8):4-16. — el texto que desarma la cadena inferencial.
- **Bruer, J. T. (1999)** *The Myth of the First Three Years*. Free Press. — la versión extendida, con la genealogía del argumento.
- **Howard-Jones, P. A. (2014)** "Neuroscience and education: myths and messages". *Nature Reviews Neuroscience* 15(12):817-824. — panorama de neuromitos y de por qué persisten.
