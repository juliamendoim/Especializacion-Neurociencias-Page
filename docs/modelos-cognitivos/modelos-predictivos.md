# Modelos predictivos del procesamiento del lenguaje

Una de las transformaciones más fuertes en psicolingüística de las últimas dos décadas: pasar de pensar el procesamiento del lenguaje como **construcción bottom-up de estructura a partir del input** (modelo generativo clásico) a pensarlo como **anticipación top-down de lo que viene** (modelos predictivos). El cambio reconfigura qué se considera la operación central del cerebro al comprender — y es una de las dos grandes alternativas modernas al modelo clásico (la otra es la familia de [modelos basados en memoria](modelos-basados-memoria.md)).

## El modelo generativo clásico — qué se está dejando atrás

El modelo dominante en psicolingüística hasta los años 90-2000 era esencialmente **bottom-up, modular y serial**. Las versiones canónicas:

- **Frazier (1987)** — modelo del **parser de dos etapas** (garden-path model): el parser construye una estructura sintáctica usando heurísticas mínimas (minimal attachment, late closure), encapsulada del léxico y la semántica. Si la estructura inicial falla cuando llega evidencia tardía, se hace **reanalysis** costosa. Estrictamente *syntax-first*.
- **Forster (1979)** — modelo modular de acceso léxico: cascada serial donde cada nivel (fonológico → léxico → sintáctico → semántico) opera de forma encapsulada antes de pasar al siguiente.
- **Levelt (1989)** — modelo generativo de **producción**: arquitectura de cascada (conceptualización → formulación → articulación) con módulos relativamente encapsulados.

Característica compartida: **el procesamiento se entiende como construcción reactiva a partir del input**. Las representaciones de niveles superiores no influyen sobre las de niveles inferiores en tiempo real. La predicción no juega un papel central — a lo sumo es un epifenómeno.

## El giro predictivo

A partir de los 2000s, dos líneas convergen:

**1. Desde la neurociencia computacional**: la **hipótesis del cerebro predictivo** (Friston, Clark, Hohwy). El cerebro no es un órgano reactivo que procesa input; es un sistema bayesiano que **genera predicciones permanentemente** y solo procesa la **diferencia entre predicción e input** (el error de predicción). Es una reformulación radical: lo que asciende por las jerarquías corticales no es el input crudo, es el residuo no predicho.

**2. Desde la psicolingüística experimental**: evidencia conductual y electrofisiológica de que **los oyentes anticipan**:

- **Altmann & Kamide (1999)** "Incremental interpretation at verbs" — eye-tracking visual world. Al oír *"el chico se va a comer..."*, la mirada anticipa la torta antes de que se diga la palabra. Anticipación semántica y sintáctica en tiempo real.
- **DeLong, Urbach & Kutas (2005)** "Probabilistic word pre-activation during language comprehension" — el N400 diferencia entre *"the airplane"* y *"an airplane"* en contextos donde "airplane" era predecible, **antes de que se diga la palabra**. Evidencia de pre-activación léxica.
- **Federmeier (2007)** propone el modelo **PARLO** (*Production-Affects-Reception-in-Left-Only*): el hemisferio izquierdo predice activamente; el derecho integra a posteriori. Asimetría hemisférica de la predicción.

## El marco teórico: lenguaje como predicción

**Pickering & Garrod (2007, 2013)** consolidan el giro con su modelo de **prediction-by-production**: el oyente comprende usando su propia maquinaria de producción para simular lo que el hablante está por decir. No hay un parser pasivo; hay simulación motora-lingüística constante.

**Kuperberg & Jaeger (2016)** "What do we mean by prediction in language comprehension?" es la revisión canónica. Distinguen varios niveles de predicción que operan en paralelo:

| Nivel | Qué se predice | Evidencia |
|---|---|---|
| **Léxico** | Qué palabra viene | N400, eye-tracking |
| **Semántico** | Qué evento se está describiendo | Visual world, ERPs tempranos |
| **Sintáctico** | Qué estructura se está construyendo | P600 anticipatorio, eye-tracking |
| **Fonológico** | Qué forma sonora viene | MMN, ERPs sublexicales |
| **Pragmático** | Qué intención comunicativa | Componentes de latencia media |

Lo crítico: estos niveles **no son serie sino paralelo**. El sistema predice en todos los niveles simultáneamente y a múltiples escalas temporales.

## La implementación computacional: surprisal

La métrica que vuelve operacionable el modelo predictivo es **surprisal** (Hale 2001, Levy 2008): cuán improbable es un token dado el contexto previo. Surprisal alta = predicción fallida = costo de procesamiento alto.

Surprisal predice empíricamente:

- Tiempos de fijación en eye-tracking.
- Amplitud del N400.
- Tiempos de reacción en decisión léxica.
- Actividad fMRI en regiones temporales y frontales del lenguaje.

Esta convergencia entre métrica computacional y datos neurales es uno de los argumentos más fuertes a favor del paradigma predictivo. Ver entrada [Surprisal](surprisal.md).

## Predictive coding como teoría neural

A nivel cerebral, **Rao & Ballard (1999)** propusieron el modelo de **predictive coding**: las capas corticales superiores envían predicciones a las inferiores; las inferiores solo transmiten hacia arriba el **error de predicción**. Aplicado al lenguaje:

- Regiones frontales (IFG, motor cortex) generan predicciones sobre formas léxicas, estructuras sintácticas, intenciones.
- Regiones temporales (STG, MTG) procesan el input acústico-fonológico.
- Lo que sube de temporal a frontal **no es el input crudo, es el error**.
- Cuando la predicción es buena, **hay poca actividad** — el sistema "ya sabía". Cuando falla, el error genera N400/P600.

Esto explica varios resultados clásicos:

- Por qué procesar lenguaje familiar es eficiente (poca actividad porque hay buena predicción).
- Por qué los hablantes nativos son rapidísimos (predicción interna optimizada).
- Por qué la dificultad de procesamiento correlaciona con improbabilidad (= magnitud del error).

## Qué cambia respecto al modelo generativo clásico

| Dimensión | Generativo clásico | Predictivo |
|---|---|---|
| Direccionalidad principal | Bottom-up (input → estructura) | Top-down (predicción → comparación) |
| Encapsulamiento modular | Sí (Frazier, Forster, Fodor) | No — interacción permanente entre niveles |
| Costo de procesamiento | Por complejidad estructural | Por surprisal / magnitud del error |
| Rol del contexto | Tardío (integración a posteriori) | Temprano (constreñe predicciones) |
| Reanalysis | Costo "estructural" de desbaratar | Magnitud del error de predicción |
| Aprendizaje | Implícito, secundario | Explícito: ajuste continuo de predicciones |

## Conexión con LLMs

Esta es probablemente la **convergencia computacional más limpia** entre cerebro y modelos de lenguaje. Los LLMs están **literalmente entrenados** en next-token prediction — minimizar la sorpresa promedio sobre un corpus. La función objetivo del entrenamiento es exactamente lo que el modelo predictivo postula como operación central del cerebro.

Esto explica por qué:

- **Surprisal de LLMs predice tan bien los tiempos de lectura humanos** (Wilcox, Futrell et al.; Schrimpf et al. 2021; Goldstein et al. 2022).
- **Las activaciones internas de LLMs predicen actividad cerebral** en regiones del lenguaje, mejor que cualquier modelo cognitivo previo.
- **Goldstein et al. (2022)** muestran que el cerebro humano también opera por predicción continua de la próxima palabra durante la escucha natural, replicando con ECoG el patrón visto en modelos.

**Caveat**: esto **no significa que los mecanismos sean iguales**. El LLM optimiza una función global vía backpropagation (biológicamente implausible); el cerebro implementa predicción con mecanismos locales (LTP/LTD, dopamina como error de recompensa de recompensa). La convergencia es **computacional a nivel 1 de Marr**, no implementacional. Ver entrada [aprendizajes generales](../aprendizajes-generales.md) sobre la sección "Autoorganización vs. big data".

## Críticas y matices

- **Huettig & Mani (2016)** "Is prediction necessary to understand language?" — argumentan que no todo es predicción. Mucho del lenguaje se comprende sin predicción activa (lectura de textos novedosos, escucha de monólogos abstractos). La predicción es **una operación facilitadora**, no la única.
- **Nieuwland et al. (2018)** intentaron replicar DeLong et al. (2005) con muestras grandes y encontraron efectos más débiles. La predicción léxica *fine-grained* es real pero menos robusta de lo que se pensaba.
- **Pickering & Gambi (2018)** matizan prediction-by-production: la simulación motora no siempre está activa; depende de la tarea, del costo cognitivo y de la previsibilidad del hablante.

## Conexiones en este sitio

- [Modelos basados en memoria](modelos-basados-memoria.md) — segunda alternativa moderna al modelo generativo clásico (no por anticipación sino por retrieval desde WM).
- [Modelos lexicalistas / constraint satisfaction (conexionistas)](modelos-lexicalistas.md) — tercera alternativa moderna (activación en paralelo de restricciones léxicas; línea genealógica directa de los LLMs).
- [Surprisal](surprisal.md) — la métrica que operacionaliza el modelo predictivo.
- [Garden paths](garden-paths.md) — un fenómeno reinterpretado por la teoría predictiva (predicción fallida + recalibración).
- [Activación](activacion.md) — sustrato común a modelos generativos y predictivos.
- [Aprendizajes generales](../aprendizajes-generales.md) — la idea del cerebro predictivo aparece transversalmente.

## Referencias clave

- **Friston, K. (2010)** "The free-energy principle: A unified brain theory?" *Nature Reviews Neuroscience* 11:127-138.
- **Clark, A. (2013)** "Whatever next? Predictive brains, situated agents, and the future of cognitive science" *Behavioral and Brain Sciences* 36:181-204.
- **Hohwy, J. (2013)** *The Predictive Mind*. Oxford UP.
- **Rao, R. P. N. & Ballard, D. H. (1999)** "Predictive coding in the visual cortex: A functional interpretation of some extra-classical receptive-field effects" *Nature Neuroscience* 2:79-87.
- **Altmann, G. T. M. & Kamide, Y. (1999)** "Incremental interpretation at verbs: Restricting the domain of subsequent reference" *Cognition* 73:247-264.
- **DeLong, K. A., Urbach, T. P. & Kutas, M. (2005)** "Probabilistic word pre-activation during language comprehension inferred from electrical brain activity" *Nature Neuroscience* 8:1117-1121.
- **Federmeier, K. D. (2007)** "Thinking ahead: The role and roots of prediction in language comprehension" *Psychophysiology* 44:491-505.
- **Pickering, M. J. & Garrod, S. (2013)** "An integrated theory of language production and comprehension" *Behavioral and Brain Sciences* 36:329-347.
- **Kuperberg, G. R. & Jaeger, T. F. (2016)** "What do we mean by prediction in language comprehension?" *Language, Cognition and Neuroscience* 31(1):32-59. **Revisión canónica del giro predictivo.**
- **Hale, J. (2001)** "A probabilistic Earley parser as a psycholinguistic model" *NAACL*.
- **Levy, R. (2008)** "Expectation-based syntactic comprehension" *Cognition* 106(3):1126-1177.
- **Goldstein, A. et al. (2022)** "Shared computational principles for language processing in humans and deep language models" *Nature Neuroscience* 25:369-380.
- **Schrimpf, M. et al. (2021)** "The neural architecture of language: Integrative modeling converges on predictive processing" *PNAS* 118(45):e2105646118.
- **Huettig, F. & Mani, N. (2016)** "Is prediction necessary to understand language? Probably not" *Language, Cognition and Neuroscience* 31:19-31.
- **Nieuwland, M. S. et al. (2018)** "Large-scale replication study reveals a limit on probabilistic prediction in language comprehension" *eLife* 7:e33468.
