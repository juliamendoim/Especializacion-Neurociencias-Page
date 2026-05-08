# Chi cuadrado (χ²)

## De dónde sale

La desarrolló **Karl Pearson** en 1900, en plena consolidación de la estadística moderna. Pearson buscaba una manera formal de responder a una pregunta concreta: **¿se ajustan los datos observados a una distribución teórica esperada?** El test fue una de las primeras herramientas de **estadística inferencial** y abrió la puerta al análisis de datos categóricos.

El nombre viene de la letra griega **χ** (chi), porque la distribución que rige el estadístico es la "distribución chi cuadrado" — que ya existía antes en otros contextos matemáticos (Helmert la había estudiado en 1875).

## Qué es, conceptualmente

A diferencia de la t, que compara **medias** de variables continuas, chi cuadrado se aplica a **variables categóricas** (cuántos casos caen en cada categoría) y mide **cuánto se desvían los datos observados de los datos esperados** bajo una hipótesis:

```
χ² = Σ [(observado − esperado)² / esperado]
```

Traducido:

- Para cada celda de la tabla de frecuencias, se calcula la diferencia entre lo que **se observó** y lo que **se esperaría** si la hipótesis nula fuera verdadera.
- Esa diferencia se eleva al cuadrado (para que las desviaciones positivas y negativas no se cancelen) y se divide por el valor esperado (para escalarla relativamente al tamaño de cada celda).
- Se suman todas las celdas. Cuanto **mayor** es χ², más se alejan los datos del modelo nulo.

## La distribución chi cuadrado

El estadístico χ² sigue una distribución propia, también dependiente de los **grados de libertad**:

- En un test de **bondad de ajuste**: df = (número de categorías − 1).
- En un test de **independencia** (tabla de contingencia): df = (filas − 1) × (columnas − 1).

A diferencia de la t (simétrica alrededor de 0), la distribución χ² es **asimétrica y siempre positiva** — porque el estadístico nunca puede ser negativo (es una suma de cuadrados).

## Para qué se usa

Tres usos principales:

1. **Bondad de ajuste**: ¿los datos observados se ajustan a una distribución teórica?
   - Ejemplo: tirar un dado 600 veces. ¿Las frecuencias observadas (cuántas veces salió cada cara) se ajustan a lo esperado bajo "dado justo" (100 cada una)?

2. **Test de independencia**: ¿dos variables categóricas son independientes entre sí?
   - Ejemplo: ¿el tipo de error fonológico (sustitución / omisión / metátesis) depende del grupo etario (3 / 4 / 5 años)?

3. **Homogeneidad**: ¿dos o más poblaciones tienen la misma distribución en una variable categórica?
   - Ejemplo: ¿la proporción de niños con TDL es igual en dos colegios?

## Cómo se obtiene el p-valor

1. Se construye la tabla de frecuencias **observadas**.
2. Se calculan las frecuencias **esperadas** bajo H₀ (independencia, ajuste, etc.).
3. Se calcula χ² con la fórmula.
4. Se busca el p-valor en la curva χ² con los grados de libertad correspondientes: la proporción del área bajo la curva más allá del valor calculado.
5. Si p ≤ 0,05 → se rechaza H₀ (los datos se desvían significativamente del modelo).

## Condiciones de aplicación

- Variables **categóricas** (nominales u ordinales).
- Observaciones **independientes** entre sí.
- Frecuencias esperadas razonablemente grandes: regla práctica, **al menos 5** en cada celda. Si hay celdas con frecuencias menores, se prefiere el **test exacto de Fisher**.

## Diferencia clave con t de Student

| | t de Student | Chi cuadrado |
|---|---|---|
| Tipo de variable | Cuantitativa continua | Categórica (frecuencias) |
| Qué compara | Medias entre 2 grupos | Distribuciones / conteos |
| Pregunta típica | ¿Difieren los promedios? | ¿Hay asociación o ajuste? |
| Distribución | Simétrica, parecida a la normal | Asimétrica, siempre positiva |

## Cuando un paper dice "se realizó χ²"

Significa que están **comparando proporciones o conteos** entre grupos o condiciones. Buscá la tabla de contingencia (filas × columnas) y los datos crudos: el χ² te dice si la asociación entre las dos variables categóricas es significativa, pero no la *magnitud* del efecto. Para eso se reportan medidas adicionales como la **V de Cramer** o **odds ratio**.
