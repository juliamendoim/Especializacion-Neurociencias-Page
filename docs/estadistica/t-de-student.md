# t de Student

## De dónde sale

La inventó **William Sealy Gosset** en 1908, un químico y estadístico que trabajaba en la cervecería **Guinness** en Dublín. Necesitaba comparar lotes pequeños de cebada y levadura (muestras de 4, 5, 10 observaciones), y la estadística que existía hasta ese momento — basada en la **distribución normal** — solo funcionaba bien con muestras grandes (n > 30).

Guinness le prohibió publicar bajo su nombre real (no querían que la competencia supiera que usaban estadística), así que firmó con el seudónimo **"Student"**. De ahí el nombre.

## Qué es, conceptualmente

Es un **estadístico** (un número que se calcula a partir de los datos) que mide **cuán lejos están dos medias entre sí, en unidades de error estándar**:

```
t = (media₁ − media₂) / error estándar de la diferencia
```

Traducido:
- El **numerador** es la diferencia bruta entre los dos promedios. Si los preescolares tienen COMP-1 = 1,2 y los escolares 1,5, el numerador es 0,3.
- El **denominador** es cuánta variabilidad esperarías por puro azar dado el tamaño de las muestras y la dispersión interna de cada grupo. Es una medida de "ruido".
- El cociente te dice **cuántas veces "más grande" es la diferencia que el ruido**. Si t = 0,5, la diferencia se confunde con el ruido. Si t = 4, la diferencia sobresale claramente.

## La distribución t

Lo que Gosset descubrió es que ese cociente, cuando trabajás con **muestras pequeñas**, **no** sigue una distribución normal — sigue una curva propia, parecida pero con **colas más pesadas** (acepta valores extremos como más probables, porque con pocos datos hay más incertidumbre).

Esa curva — la **distribución t de Student** — depende de un solo parámetro, los **grados de libertad** (df), que aproximadamente equivale a *n − 2* en una t de dos grupos. Cuantos más datos, más se parece a una normal; con n → ∞ son indistinguibles.

## Cómo se obtiene el p-valor

1. Calculás t con la fórmula de arriba.
2. Mirás la curva t correspondiente a tus grados de libertad.
3. Calculás qué proporción del área bajo la curva queda **más allá** de tu valor de t. Esa proporción es **p**.
4. Si p ≤ 0,05 → la diferencia es lo bastante grande como para que sea improbable que haya salido por azar.

## Para qué se usa

La t de Student es la prueba estándar para **comparar las medias de dos grupos** y decidir si la diferencia observada es estadísticamente significativa o se puede atribuir al azar.

Condiciones típicas:
- **Dos grupos** (no más).
- Variable dependiente **cuantitativa continua**.
- Datos aproximadamente **normales** (importante con n chico).

**Una cola vs. dos colas**: si la hipótesis es **direccional** ("el grupo A produce más que el B") se usa una cola; si solo se predice "que hay diferencia, sin saber en qué sentido", se usa de dos colas. Una cola da más potencia estadística pero exige tener fundamentada la dirección.

## Variantes y alternativas

- **t pareada**: cuando son los mismos sujetos medidos antes/después (medidas repetidas).
- **ANOVA**: cuando hay 3 o más grupos.
- **U de Mann-Whitney** (no paramétrica): cuando los datos no son normales o las muestras son muy chicas. Algunos autores la prefieren con n pequeños.

## Ejemplo concreto: Peñaloza (recontados narrativos)

Peñaloza compara dos grupos independientes de niños — G1 preescolares y G2 escolares de 1° básico — en varios índices de complejidad sintáctica (COMP-1, COMP-2, COMP-2 Adj, Sust, Adv).

Aplica **t de Student de una cola** porque:
- Son **dos grupos independientes** (niños distintos en cada grupo).
- La variable dependiente es **cuantitativa continua** (promedios de cláusulas por oración).
- La hipótesis es **direccional**: espera que los escolares produzcan **más** complejidad que los preescolares.

Umbral: p ≤ 0,05 (convención estándar en ciencias sociales).
