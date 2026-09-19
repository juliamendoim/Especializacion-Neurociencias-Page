# La crisis de replicación

A partir de 2011 la psicología —y después varias disciplinas vecinas— atravesó un episodio que cambió sus estándares metodológicos: se descubrió que **una proporción grande de resultados publicados no se sostenía al intentar reproducirlos**.

Saber esto no es un dato de cultura general: cambia **cómo hay que leer un paper**, y explica por qué hoy se exigen cosas (preregistro, datos abiertos, muestras grandes) que hace quince años eran excepcionales.

---

## El dato que le puso número al problema

El **Reproducibility Project: Psychology** (Open Science Collaboration, 2015, *Science*) intentó replicar **100 estudios** tomados de tres revistas prestigiosas, usando diseños de alta potencia y los materiales originales cuando estaban disponibles.

| | |
|---|---|
| Estudios **originales** con resultado significativo | **97 %** |
| **Replicaciones** con resultado significativo | **36 %** |
| Efectos juzgados subjetivamente como replicados | 39 % |
| Tamaños de efecto originales dentro del IC 95 % de la replicación | 47 % |
| Magnitud media del efecto en las replicaciones | **la mitad** del original (r = .20 vs. r = .40) |

Ese contraste entre 97 % y 36 % es el corazón del asunto. No es que la mayoría de los hallazgos sea falsa: es que la literatura publicada **no es una muestra representativa** de lo que los estudios encontraron.

---

## Por qué pasó: no fue fraude

Casi nada de esto se explica por mala fe. Son incentivos y prácticas que parecían razonables:

**Grados de libertad del investigador**
: En cualquier análisis hay decenas de decisiones legítimas: a quién excluir, qué transformación aplicar, qué covariables incluir, dónde cortar una ventana temporal. Si se toman **después** de ver los datos, cada una empuja un poquito hacia el resultado deseado. Es el *jardín de senderos que se bifurcan*: no hace falta hacer trampa para llegar a un falso positivo.

**El caso demostrativo**
: Simmons, Nelson y Simonsohn (2011) mostraron, con datos reales y análisis "normales", que escuchar cierta canción **rejuvenecía a los participantes**. Era falso por construcción. El punto era exhibir cuánta flexibilidad alcanza para producir cualquier resultado.

**Sesgo de publicación**
: Los resultados nulos no se publican. Quedan en el cajón, y la literatura queda sobrepoblada de efectos positivos.

**HARKing**
: Formular la hipótesis después de conocer los resultados, y presentarla como si hubiera sido previa. Convierte un hallazgo exploratorio en uno confirmatorio sin que se note.

**Potencia estadística baja**
: Muestras chicas. Una muestra chica no solo detecta menos efectos: cuando detecta uno, lo **sobreestima**, porque solo los efectos exagerados por azar cruzan el umbral. Es el *efecto del ganador*.

Diez años antes, Ioannidis (2005) ya había argumentado formalmente por qué, con estas condiciones, cabía esperar que la mayoría de los hallazgos publicados fueran falsos.

---

## Qué sobrevivió y qué no

La crisis **no afectó a todo por igual**, y la distinción es la parte útil.

**Se cayeron o quedaron muy debilitados**: buena parte de los efectos de *priming* social, la postura de poder, el agotamiento del ego, la hipótesis de la retroalimentación facial. Rasgos comunes: **entre sujetos**, **una sola medición por persona**, muestras chicas, efectos chicos y tamaños de efecto llamativamente grandes para lo que prometían.

**Aguantaron sin problema**: los efectos básicos de la psicología cognitiva y psicolingüística — Stroop, efecto de frecuencia, priming de repetición, el [N400](n400-p600-potenciales.md).

### Por qué la psicolingüística salió mejor parada

No es virtud moral, es estructura de diseño:

- **Intrasujeto**: cada participante pasa por todas las condiciones, así que cada uno es su propio control y se elimina la varianza entre personas.
- **Muchos ensayos por persona**: decenas o cientos, en lugar de una medición única. Eso da una potencia enormemente mayor con las mismas 30 personas.
- **Efectos grandes y estables**: el contraste entre una palabra frecuente y una infrecuente, o entre un final congruente y uno incongruente, no es un efecto sutil.

Conviene tenerlo presente al leer literatura de este campo: **es más confiable que el promedio de la psicología**, pero por razones concretas, no por prestigio.

---

## Qué cambió en la práctica

**Preregistro**
: Declarar hipótesis, diseño y plan de análisis en un repositorio público **antes** de recolectar datos. Cierra los grados de libertad y separa lo confirmatorio de lo exploratorio. No prohíbe explorar: obliga a decir cuál es cuál.

**Informes registrados** (*registered reports*)
: La revista evalúa y acepta el trabajo **por el diseño**, antes de que existan resultados. Elimina el sesgo de publicación en la raíz, porque la aceptación no depende de qué dé.

**Datos, materiales y código abiertos**
: Permite verificar el análisis y reanalizar. Es también lo que hace posible el tipo de reanálisis de corpus públicos que hoy es una vía legítima de investigación.

**Replicaciones multi-laboratorio**
: Proyectos tipo *ManyLabs*, donde decenas de laboratorios corren el mismo protocolo.

**Reporte de tamaños de efecto e intervalos de confianza**, no solo valores p.

---

## Cómo leer un paper después de esto

| Preguntá | Por qué importa |
|---|---|
| ¿Está preregistrado? | Distingue confirmatorio de exploratorio |
| ¿Cuántos participantes, y cuántos ensayos por condición? | La potencia depende de las dos cosas |
| ¿El diseño es intra o entre sujetos? | Intrasujeto con muchos ensayos es mucho más robusto |
| ¿Reporta tamaño de efecto e intervalo? | Un p < .05 sin magnitud no dice cuánto |
| ¿Hay datos y código disponibles? | Verificabilidad |
| ¿Cuántos análisis se probaron antes de este? | Si no se declara, asumí que varios |
| ¿Se replicó en otro laboratorio? | El mejor criterio disponible |

Y una advertencia sobre el otro extremo: la conclusión **no** es que nada sea confiable. Es que **la confianza hay que graduarla por evidencia y no por prestigio de la revista o del autor**. Un efecto replicado en diez laboratorios con preregistro es otra cosa que un efecto llamativo publicado una vez.

---

## Cómo se conecta con otros conceptos

- **[N400 y P600](n400-p600-potenciales.md)** — un caso donde el efecto central es sólido pero la literatura tiene problemas reales de flexibilidad analítica: la distinción entre "el efecto" y "un hallazgo específico sobre el efecto".
- **[PRISMA](prisma.md)** — estándares de reporte para revisiones sistemáticas; la misma lógica de hacer explícitas las decisiones.
- **[Tiempo de reacción](tiempo-reaccion.md)** — los diseños intrasujeto con muchos ensayos que explican por qué la psicología cognitiva resistió mejor.
- **[CATALISE](catalise.md)** — consenso explícito y documentado como alternativa a criterios heredados sin revisar.

---

## Referencias de entrada

- Open Science Collaboration (2015). Estimating the reproducibility of psychological science. *Science*, 349(6251).
- Simmons, J., Nelson, L. & Simonsohn, U. (2011). False-positive psychology: undisclosed flexibility in data collection and analysis allows presenting anything as significant. *Psychological Science*, 22(11), 1359-1366.
- Ioannidis, J. (2005). Why most published research findings are false. *PLoS Medicine*, 2(8), e124.
- Gelman, A. & Loken, E. (2014). The statistical crisis in science. *American Scientist*, 102(6), 460-465. (El jardín de senderos que se bifurcan.)
- Button, K. et al. (2013). Power failure: why small sample size undermines the reliability of neuroscience. *Nature Reviews Neuroscience*, 14(5), 365-376.
- Nosek, B. et al. (2018). The preregistration revolution. *PNAS*, 115(11), 2600-2606.
- Chambers, C. (2013). Registered reports: a new publishing initiative at *Cortex*. *Cortex*, 49(3), 609-610.
- Luck, S. & Gaspelin, N. (2017). How to get statistically significant effects in any ERP experiment (and why you shouldn't). *Psychophysiology*, 54(1), 146-157.
