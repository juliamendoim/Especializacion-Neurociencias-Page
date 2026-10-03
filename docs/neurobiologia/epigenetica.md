# Epigenética

Conjunto de mecanismos moleculares que **regulan si un gen se expresa o no, sin modificar la secuencia del ADN**. La metáfora habitual: el genoma es la partitura y la epigenética decide qué instrumentos la tocan, cuándo y con qué volumen.

Es un campo real, con mecanismos bien caracterizados, y al mismo tiempo **uno de los más sobrevendidos de la biología contemporánea** — sobre todo cuando salta a la divulgación, la educación y el discurso sobre políticas sociales. Esta entrada intenta separar las dos cosas: qué está establecido, qué está en disputa y qué es directamente hype.

!!! note "Por qué aparece en neurociencias del lenguaje y la educación"
    Tres debates del campo pasan por acá: **períodos críticos vs. sensibles** (¿qué fija una ventana de desarrollo?), **el efecto de la pobreza y la adversidad temprana sobre el desarrollo cognitivo** (¿cómo se "mete" el ambiente en el cerebro?) y el problema de los **neuromitos** (la epigenética es hoy una de las fuentes principales de afirmaciones educativas mal fundadas).

---

## 1. El problema que viene a resolver

Todas las células de un organismo tienen el mismo genoma. Una neurona y un hepatocito comparten el ADN y expresan programas completamente distintos. Algo tiene que estar apagando y prendiendo tramos del genoma de forma **estable y heredable entre divisiones celulares**. Eso es, en su sentido estricto y original (Waddington, años 40), la epigenética: el estudio de cómo el genotipo da lugar al fenotipo durante el desarrollo.

El sentido estricto importa porque hay una **definición amplia y una restringida** circulando a la vez, y el deslizamiento entre ambas es la fuente de la mitad de las confusiones:

| | Definición restringida | Definición amplia |
|---|---|---|
| **Qué exige** | Marca molecular **heredable a través de divisiones celulares** (o generaciones) sin cambio de secuencia | Cualquier regulación de la expresión génica |
| **Qué incluye** | Metilación del ADN, algunas marcas de histonas, impronta, inactivación del X | Además: todo factor de transcripción, toda señal intracelular |
| **Problema** | Difícil de demostrar | Tan amplia que se vuelve trivialmente cierta |

Cuando un texto de divulgación dice "la experiencia modifica tu epigenoma", suele estar usando la definición amplia — donde la afirmación es casi tautológica — y dejando que el lector la entienda en la restringida, donde implicaría herencia.

---

## 2. Los mecanismos

### Metilación del ADN

Es el mecanismo más estudiado y el más medido. Se agrega un grupo metilo (**—CH₃**) a una citosina, típicamente en un contexto **CpG** (una citosina seguida de una guanina). Las enzimas que lo hacen son las **DNMT** (ADN metiltransferasas); las que lo quitan, de la familia **TET**.

- Metilación alta en una **región promotora** → típicamente **silenciamiento** del gen (el promotor queda menos accesible y se reclutan proteínas represoras).
- Las **islas CpG** son regiones ricas en CpG asociadas a promotores; su estado de metilación es informativo.
- Es **mitóticamente estable**: se copia a las células hijas. Esto es lo que la vuelve candidata a "memoria celular".

### Modificaciones de histonas

El ADN está enrollado sobre octámeros de histonas. Las colas de esas histonas reciben modificaciones químicas — **acetilación, metilación, fosforilación, ubiquitinación** — que cambian qué tan compacta queda la cromatina y qué proteínas se reclutan.

- **Acetilación** (vía HAT, enzimas acetiltransferasas) → cromatina más abierta → **más transcripción**. Las **HDAC** (deacetilasas) hacen lo inverso.
- La metilación de histonas no tiene un signo único: **H3K4me3** marca promotores activos, mientras **H3K27me3** y **H3K9me3** marcan represión.
- Los inhibidores de HDAC (por ejemplo la **tricostatina A**) son la herramienta farmacológica estándar para probar causalidad en modelos animales.

### ARN no codificantes

**miARN, lncARN, piARN**: regulan la traducción y la estabilidad de los mensajeros, y en algunos casos dirigen maquinaria de silenciamiento a loci específicos. En la discusión sobre herencia transgeneracional son hoy **los candidatos más plausibles**, por una razón concreta: a diferencia de la metilación, los ARN pequeños del gameto no se borran en la reprogramación germinal.

### Cromatina de orden superior

Dominios topológicos (**TAD**), bucles de cromatina, posición del locus respecto de la lámina nuclear. Menos presente en la discusión psicológica, central en la molecular.

---

## 3. Los casos sólidos: donde nadie discute

Antes de entrar en lo polémico, vale fijar que hay fenómenos epigenéticos **completamente establecidos**, y que son los que le dan credibilidad al campo:

- **Impronta genómica (imprinting)**. Alrededor de 100-200 genes humanos se expresan solo desde la copia materna o solo desde la paterna, según marcas de metilación puestas en la gametogénesis. Cuando la impronta falla aparecen cuadros clínicos definidos: **síndrome de Prader-Willi** y **síndrome de Angelman** (ambos en 15q11-q13, según qué copia se pierda), **Beckwith-Wiedemann**, **Silver-Russell**. Esto es herencia epigenética real, intergeneracional, documentada.
- **Inactivación del cromosoma X**. En células de mamíferos hembra, uno de los dos X se silencia casi por completo, de forma estable y clonal, mediante el lncARN **XIST**. Es el ejemplo canónico de silenciamiento epigenético a escala de cromosoma.
- **Diferenciación celular**. El perfil de metilación y de marcas de histonas es lo que mantiene a una neurona siendo una neurona. La reprogramación a células madre inducidas (**iPSC**, Yamanaka) funciona precisamente borrando ese perfil.
- **Oncología**. La hipermetilación de promotores de supresores tumorales y la hipometilación global son hallazgos robustos, y hay fármacos epigenéticos aprobados (azacitidina, decitabina).

Nada de lo que viene después invalida esto. La pregunta es cuánto se puede extrapolar de acá a afirmaciones sobre conducta, aprendizaje y herencia de la experiencia.

---

## 4. El modelo que fundó la "epigenética del comportamiento"

**Weaver, Cervoni, Champagne, Meaney y colaboradores (2004)**, en *Nature Neuroscience*, es el trabajo que abrió el campo conductual. Vale conocerlo en detalle porque es el estándar metodológico contra el que conviene medir todo lo demás.

El diseño, en ratas:

1. Las madres varían naturalmente en cuánto **lamen y acicalan** (*licking and grooming*) a sus crías en la primera semana.
2. Las crías de madres de alto cuidado muestran, de adultas, **menor metilación del promotor del gen del receptor de glucocorticoides (GR, exón 1₇)** en el hipocampo, más acetilación de histonas en ese sitio, más unión del factor de transcripción **NGFI-A**, más expresión de GR y una **respuesta de estrés atenuada** (eje HPA mejor regulado).
3. **Crianza cruzada** (*cross-fostering*): crías de madres de bajo cuidado criadas por madres de alto cuidado adquieren el patrón de la madre adoptiva. Esto descarta la explicación genética y establece que **la conducta materna es la causa**.
4. **Reversión farmacológica en el adulto**: infundir un inhibidor de HDAC (tricostatina A) o metionina revierte las diferencias de metilación, de expresión y de conducta. Esto establece que la marca es **causalmente necesaria**, no un correlato.

Por qué es un buen estudio: tiene **manipulación experimental** del supuesto causante, un mecanismo molecular medido en **el tejido relevante** (hipocampo, no sangre), **intervención sobre el mecanismo** en ambas direcciones y un resultado conductual medido.

Y acá está el problema de todo lo que vino después: **casi ningún estudio humano puede hacer nada de eso.** No se puede randomizar el cuidado materno, no se puede biopsiar hipocampo, no se puede infundir un inhibidor de HDAC. Lo que queda son estudios de asociación en tejidos accesibles. Lo que se pierde es, justamente, la causalidad.

---

## 5. El caso humano más citado

**Heijmans, Lumey y colaboradores (2008)**, en *PNAS*: el **Hongerwinter** holandés, la hambruna provocada por el bloqueo alemán entre 1944 y 1945. Es el experimento natural mejor documentado que existe, porque los registros civiles y sanitarios holandeses siguieron funcionando con precisión durante la hambruna.

El hallazgo: las personas expuestas **en el período periconcepcional** tenían, **seis décadas después**, un **5,2% menos de metilación** en la región diferencialmente metilada (DMR) del gen **IGF2**, comparadas con hermanos del mismo sexo no expuestos. La comparación intrafamiliar es la fortaleza del diseño: controla parcialmente genética y entorno familiar.

Y el efecto era **específico del momento de la exposición**: aparecía en los expuestos periconcepcionalmente, no en los expuestos al final del embarazo.

Qué muestra y qué no:

- ✅ Que una exposición ambiental en una ventana muy temprana deja una marca molecular detectable décadas después. Esto, en sí, es notable.
- ⚠️ Es un **único locus** candidato, con un efecto **pequeño en magnitud** (5,2%), medido en **sangre**, y **sin demostración de que medie** ningún resultado de salud o cognición. La cohorte tiene consecuencias de salud documentadas, pero el vínculo causal entre esta marca de metilación y esas consecuencias no está establecido.
- ⚠️ Es **intergeneracional, no transgeneracional**: la exposición ocurrió sobre el individuo medido, en el útero. No hay herencia de nada.

Esa última distinción es la que más se abusa en divulgación, y vale fijarla.

---

## 6. Intergeneracional vs. transgeneracional

!!! warning "La distinción que casi todo el hype atropella"
    **Intergeneracional**: el ambiente afecta a un individuo que estaba **presente y expuesto** — un feto en el útero (F1), o incluso los gametos que ya existían dentro de ese feto (F2, en el caso de una hembra expuesta). Esto es **exposición directa**, no herencia.

    **Transgeneracional (herencia epigenética propiamente dicha)**: el efecto aparece en una generación que **nunca estuvo expuesta, ni como gameto**. En la línea materna eso exige llegar a **F3**; en la paterna, a **F2**. Es lo único que justificaría hablar de "herencia".

Casi todos los hallazgos humanos citados como "herencia epigenética" son intergeneracionales. Y el salto a lo transgeneracional enfrenta obstáculos mecanísticos serios.

### Por qué es difícil: la barrera de Weismann

La **barrera de Weismann** (1892) es la separación entre línea germinal y línea somática: lo que le pasa a las células del cuerpo no se transmite a los gametos. Es uno de los pilares de la síntesis moderna y la razón por la cual el lamarckismo quedó descartado. La herencia epigenética transgeneracional, si existe, tiene que **atravesarla**.

### Por qué es difícil: la reprogramación germinal

Hay **dos oleadas de borrado** masivo de marcas epigenéticas:

1. Durante la **diferenciación de las células germinales**, la cromatina se remodela extensamente y la metilación se borra casi por completo (incluidas las marcas de impronta, que se reponen después según el sexo).
2. **Después de la fertilización**, en el cigoto y el embrión temprano, hay una segunda ronda de desmetilación y remetilación.

O sea: el sistema está **organizado para borrar** justamente lo que la hipótesis transgeneracional necesita que se conserve. Hay loci que **escapan** a la reprogramación — algunos retrotransposones, algunos loci improntados — y son el candidato mecanístico serio, junto con los ARN pequeños del espermatozoide.

### Por qué es difícil: los confusores en humanos

**Horsthemke (2018)**, en *Nature Communications*, es la revisión crítica de referencia. Su punto central: en humanos, lo que se interpreta como herencia epigenética es **indistinguible** de

- **herencia genética** — incluyendo variantes de secuencia que controlan la metilación (**mQTL**: una fracción sustancial de la variación interindividual en metilación, con estimaciones de hasta ~20%, es atribuible a variantes de secuencia; es decir, es *genética* disfrazada de epigenética);
- **herencia ecológica** — los hijos heredan el barrio, la dieta, la exposición a tóxicos, el microbioma, el nivel socioeconómico;
- **herencia cultural** — y las prácticas de crianza, que se transmiten sin ningún mecanismo molecular especial.

**Heard & Martienssen (2014)**, en *Cell*, llegan a una conclusión parecida desde la biología molecular: hay evidencia buena en plantas, en *C. elegans* y en algunos casos de ratón, evidencia **débil y mal controlada** en humanos, y una brecha grande entre lo que el campo afirma y lo que los mecanismos permiten.

---

## 7. Los problemas de medición en estudios humanos

Esta es la sección más útil para leer papers con criterio.

### El problema del tejido: sangre no es cerebro

Casi todos los estudios epigenéticos humanos de fenotipos cognitivos o psiquiátricos miden metilación en **sangre periférica** (o saliva, o epitelio bucal), porque el cerebro no está disponible. Pero la metilación es **específica de tejido** — es el mecanismo mismo de la diferenciación celular, así que su especificidad tisular no es un ruido molesto: es su función.

**Hannon, Lunnon, Schalkwyk & Mill (2015)**, en *Epigenetics*, midieron metilación en muestras pareadas de sangre y **cuatro regiones cerebrales** (corteza prefrontal, corteza entorrinal, giro temporal superior y cerebelo) de 122 individuos. Resultado: **para la mayoría de los sitios, la variación interindividual en sangre no predice bien la variación en cerebro** — algo mejor para regiones corticales que para cerebelo. Existe un **subconjunto minoritario** de sitios donde la correlación entre tejidos sí es fuerte (incluso cuando el nivel absoluto de metilación difiere), y ese subconjunto es el que vale la pena usar; de ahí herramientas como **BECon**, que ayudan a estimar si un sitio hallado en sangre es interpretable en cerebro.

Qué preguntarle entonces a un paper: **¿el sitio reportado está en ese subconjunto con correlación sangre-cerebro documentada, o se asume la extrapolación sin más?**

Y un confusor adicional: la sangre es una **mezcla de tipos celulares** en proporciones variables. Un cambio aparente de metilación puede ser, en realidad, un cambio en la **composición celular** de la muestra (más linfocitos, menos neutrófilos). Un paper serio corrige por composición celular; conviene verificar que lo haga.

### El problema de la dirección causal

Un estudio de asociación encuentra que cierto patrón de metilación va con cierta conducta. La lectura intuitiva es que la metilación es la **base** de la conducta. Pero puede ser la **consecuencia**.

El estudio longitudinal **IMAGEN** (publicado en *Biological Psychiatry*) midió metilación y problemas de conducta en los mismos adolescentes a los **14 y a los 19 años** (n ≈ 506), lo que permite ordenar temporalmente las variables. Los análisis de mediación longitudinal indicaron que la metilación asociada a problemas de conducta externalizante era **más probablemente un resultado** de esas conductas (acentuadas por eventos vitales negativos) **que su base epigenética**. Las *methylation risk scores* correlacionaban además con menor volumen de materia gris en corteza orbitofrontal medial y cingulada anterior/media.

Es un recordatorio incómodo y necesario: **conducta → biología** es una dirección tan posible como la inversa, y la mayoría de los diseños no la distingue.

### El problema del tamaño de efecto y la potencia

Un array de metilación mide cientos de miles de sitios CpG a la vez. Los **EWAS** (estudios de asociación epigenómica) tienen por lo tanto el mismo problema de comparaciones múltiples que los GWAS, pero históricamente con muestras **mucho más chicas**. El resultado previsible es una literatura con muchos hallazgos de un solo locus que no replican. Vale aplicar acá exactamente los criterios de [la crisis de replicación](../metodologia/crisis-replicacion.md): preguntar por el *n*, por la corrección por comparaciones múltiples, por la replicación en cohorte independiente, por el preregistro.

### Los relojes epigenéticos: predicen sin explicar

El **reloj de Horvath** (2013) es un predictor de edad cronológica construido con regresión regularizada (*elastic net*) sobre **353 sitios CpG**, entrenado en alrededor de 8.000 muestras de múltiples tejidos. Funciona notablemente bien, y la "aceleración epigenética de la edad" predice morbilidad y mortalidad.

Pero conviene ser preciso sobre lo que es: **un modelo predictivo, no un mecanismo**. Los sitios fueron seleccionados por su valor predictivo, no por su función biológica; el modelo asume aditividad y tasa de cambio constante a lo largo de la vida, dos supuestos que no se sostienen en todos los CpG; y los procesos moleculares que determinan la velocidad del reloj **no están establecidos**. Es un biomarcador excelente y una explicación nula — una distinción que la divulgación suele colapsar.

---

## 8. El hype y por qué no es inocuo

**Isles (2015)**, "Neural and behavioural epigenetics; what it is, and what is hype", en *Genes, Brain and Behavior*, es el artículo que conviene leer para calibrar. El argumento general del campo crítico tiene dos partes.

La primera es epistémica: **"es epigenético" no explica nada por sí solo.** Decir que la adversidad temprana deja marcas epigenéticas es compatible con prácticamente cualquier mecanismo de efecto ambiental duradero, y por eso no discrimina entre hipótesis. La palabra funciona como un sello de respetabilidad molecular sobre una afirmación que podría formularse sin ella.

La segunda es ética y política, y está desarrollada en trabajos como **"Epigenetics Changes Nothing: What a New Scientific Field Does and Does Not Mean for Ethics and Social Justice"**. El punto: la retórica epigenética se usa en dos direcciones opuestas, y ninguna de las dos se sigue de la evidencia.

- **Dirección optimista**: "la epigenética demuestra que el ambiente importa, entonces hay que invertir en primera infancia". La conclusión puede ser correcta, pero **no necesita la epigenética** — que el ambiente temprano importa está establecido por epidemiología, estudios de intervención y psicología del desarrollo desde mucho antes. Fundamentar una política en el eslabón molecular más frágil de la cadena la vuelve vulnerable a que ese eslabón no replique.
- **Dirección pesimista, más preocupante**: "la pobreza deja marcas epigenéticas" puede derivar en una **biologización del daño social** — en tratar a los chicos de hogares pobres como molecularmente dañados, con una ventana que ya se cerró. Eso reintroduce determinismo por la puerta de atrás y traslada la responsabilidad del Estado al cuerpo de la madre, que es donde la narrativa epigenética suele depositarla.

Hay una asimetría retórica digna de atención: la epigenética entró al discurso público **como antídoto del determinismo genético** ("tus genes no son tu destino") y puede terminar funcionando como un determinismo nuevo, con una ventana temporal más estrecha y una atribución de responsabilidad más individual.

---

## 9. Cómo leer un paper de epigenética

Una lista de verificación, ordenada por cuánta diferencia hace cada punto:

1. **¿Es un estudio de asociación o hay manipulación?** Sin manipulación experimental del supuesto causante, lo que hay es correlación. La crianza cruzada de Weaver et al. es el estándar; en humanos rara vez es alcanzable.
2. **¿En qué tejido se midió?** Si es sangre o saliva y el fenotipo es cognitivo, preguntar si los sitios reportados tienen correlación sangre-cerebro documentada.
3. **¿Se corrigió por composición celular?** En sangre es obligatorio.
4. **¿Se controló la genética?** ¿Hay datos de mQTL, diseño intrafamiliar, gemelos monocigóticos discordantes? Sin esto, una fracción del "efecto epigenético" puede ser secuencia.
5. **¿Es intergeneracional o transgeneracional?** Si se habla de herencia: ¿llegaron a F3 en línea materna, o a F2 en paterna?
6. **¿Cuál es la dirección temporal?** ¿Hay diseño longitudinal que permita distinguir causa de consecuencia?
7. **¿Hay un mecanismo o solo una marca?** ¿Se midió expresión del gen? ¿Proteína? ¿Función? Una diferencia de metilación sin cambio de expresión no es un efecto funcional.
8. **¿Es gen candidato o epigenoma completo?** Y si es epigenoma completo: corrección por comparaciones múltiples, tamaño muestral, replicación independiente.
9. **¿El tamaño de efecto es interpretable?** Un 5% de diferencia de metilación en un locus no se traduce automáticamente en nada fenotípico.

---

## 10. Dónde queda, entonces

Un resumen por niveles de confianza:

| Afirmación | Estado |
|---|---|
| Existen marcas epigenéticas que regulan la expresión génica de forma estable | **Establecido** |
| La impronta genómica y la inactivación del X son fenómenos epigenéticos con consecuencias clínicas | **Establecido** |
| El perfil epigenético es específico de tejido y sostiene la identidad celular | **Establecido** |
| El ambiente temprano puede dejar marcas epigenéticas detectables mucho después, en el individuo expuesto | **Bien apoyado**, con el Hongerwinter y los modelos animales |
| En roedores, la conducta materna causa cambios epigenéticos que median la respuesta al estrés | **Bien apoyado** (Weaver et al. 2004, con manipulación y reversión) |
| En humanos, marcas epigenéticas específicas median efectos de la adversidad sobre la cognición | **En disputa** — problemas de tejido, de dirección causal y de potencia |
| Existe herencia epigenética transgeneracional en humanos | **No establecido** — mecanísticamente problemática y empíricamente confundida |
| Hallazgos epigenéticos justifican intervenciones educativas concretas | **No establecido** — y ninguna intervención con evidencia depende de ellos |

La posición razonable no es ni el entusiasmo ni el descarte. La epigenética molecular es sólida; la epigenética **conductual humana** es un campo joven con problemas metodológicos severos y bien identificados; y la epigenética **de divulgación** es, en buena medida, una metáfora que viaja mucho más rápido que su evidencia.

---

## Conexiones con el sitio

- **[Ontogenia y filogenia](ontogenia-filogenia.md)** — la distinción intergeneracional/transgeneracional es exactamente el límite entre esos dos planos. La herencia epigenética es interesante precisamente porque, si existiera, haría pasar algo de lo ontogenético al plano filogenético.
- **[Sinaptogénesis y poda sináptica](sinaptogenesis-poda-sinaptica.md)** — el otro gran candidato a explicar "cómo el ambiente temprano se inscribe en el cerebro", y con el mismo patrón de sobreinterpretación educativa. La poda tiene la ventaja de un mecanismo celular identificado; conviene leer las dos entradas juntas.
- **[Plasticidad estructural y sináptica](plasticidad-estructural-mecanismos.md)** — la LTP y la consolidación de memoria a largo plazo requieren transcripción génica, y hay regulación epigenética involucrada. Es el punto donde los dos temas se tocan en serio.
- **[La crisis de replicación](../metodologia/crisis-replicacion.md)** — los EWAS tienen el mismo perfil de riesgo que cualquier campo de muestras chicas y muchas comparaciones.
- **[Las 4 preguntas de Tinbergen](tinbergen-niveles-analisis.md)** — útil para ubicar de qué se está hablando: la epigenética es una respuesta de nivel **mecanismo**, que a veces se presenta como si respondiera **ontogenia** o **filogenia**.
- **[FOXP2](foxp2.md)** — el precedente directo de cómo un hallazgo molecular real se convierte en una etiqueta demasiado grande ("el gen del lenguaje") y después hay que desarmarla.

---

## Fuentes

**Mecanismos y revisiones generales**

- **Waddington, C. H. (1942)** "The epigenotype". *Endeavour* 1:18-20. — el origen del término, en un sentido bastante distinto del actual.
- **Heard, E. & Martienssen, R. A. (2014)** "Transgenerational epigenetic inheritance: myths and mechanisms". *Cell* 157(1):95-109. — **la revisión de referencia.** Ordena qué evidencia hay por organismo y cuáles son las barreras mecanísticas.

**El modelo conductual fundacional**

- **Weaver, I. C. G., Cervoni, N., Champagne, F. A., D'Alessio, A. C., Sharma, S., Seckl, J. R., Dymov, S., Szyf, M. & Meaney, M. J. (2004)** "Epigenetic programming by maternal behavior". *Nature Neuroscience* 7(8):847-854. — crianza cruzada y reversión farmacológica. El estándar metodológico del campo.

**El caso humano**

- **Heijmans, B. T., Tobi, E. W., Stein, A. D., Putter, H., Blauw, G. J., Susser, E. S., Slagboom, P. E. & Lumey, L. H. (2008)** "Persistent epigenetic differences associated with prenatal exposure to famine in humans". *PNAS* 105(44):17046-17049. — [acceso abierto](https://www.pnas.org/doi/10.1073/pnas.0806560105).

**La crítica (lo más útil para calibrar)**

- **Horsthemke, B. (2018)** "A critical view on transgenerational epigenetic inheritance in humans". *Nature Communications* 9:2973. — **acceso abierto.** La demolición ordenada del caso humano: herencia genética, ecológica y cultural como confusores.
- **Isles, A. R. (2015)** "Neural and behavioural epigenetics; what it is, and what is hype". *Genes, Brain and Behavior* 14(1):64-72.
- **Juengst, E. T., Fishman, J. R., McGowan, M. L. & Settersten, R. A. (2014)** "Serving epigenetics before its time". *Trends in Genetics* 30(10):427-429. — sobre la traducción prematura a política pública.
- **"Epigenetics Changes Nothing: What a New Scientific Field Does and Does Not Mean for Ethics and Social Justice"** — el argumento de que la epigenética no agrega premisas a los debates sobre justicia social, y de los riesgos de pretender que sí.

**Problemas de medición**

- **Hannon, E., Lunnon, K., Schalkwyk, L. & Mill, J. (2015)** "Interindividual methylomic variation across blood, cortex, and cerebellum: implications for epigenetic studies of neurological and neuropsychiatric phenotypes". *Epigenetics* 10(11):1024-1032. — [en PMC](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4844197/). El paper que hay que citar cada vez que alguien extrapola de sangre a cerebro.
- **Edgar, R. D., Jones, M. J., Meaney, M. J., Turecki, G. & Kobor, M. S. (2017)** "BECon: a tool for interpreting DNA methylation findings from blood in the context of brain". *Translational Psychiatry* 7:e1187.
- **Horvath, S. (2013)** "DNA methylation age of human tissues and cell types". *Genome Biology* 14:R115. — el reloj epigenético original.
- **Bell, C. G. et al. (2019)** "DNA methylation aging clocks: challenges and recommendations". *Genome Biology* 20:249. — qué no hay que concluir de un reloj.
- **Chen, Z. et al. (2023)** "Associations of DNA methylation with behavioral problems, gray matter volumes, and negative life events across adolescence: evidence from the longitudinal IMAGEN study". *Biological Psychiatry* 94(4):342-351. — el estudio longitudinal que sugiere causalidad inversa.
