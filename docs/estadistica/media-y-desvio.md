# Media y desvío estándar

Una **media sola no dice nada útil** sobre un grupo. Hay que saber qué tan **dispersos** están los datos alrededor de esa media para interpretar bien el resultado.

## Qué es la media

El **promedio** del grupo: sumar todos los valores y dividir por la cantidad de sujetos. Es una medida de **tendencia central** — dónde está "el centro" de la distribución.

## Qué es el desvío estándar (DE / SD)

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

## Por qué se reportan juntas

Dos grupos con la **misma media** pueden ser muy distintos:

| Grupo | Media | DE | Qué pasó |
|---|---|---|---|
| A | 7,0 | 0,3 | Casi todos sacaron entre 6,7 y 7,3 — grupo **homogéneo** |
| B | 7,0 | 2,5 | Hay quienes sacaron 4 y quienes sacaron 10 — grupo **heterogéneo** |

La media sola los haría parecer equivalentes; el DE es lo que muestra que no lo son.

## Por qué importa en investigación tipo Acosta

En estudios que comparan grupo TDL vs. control, reportar media + DE permite:

1. **Evaluar si los grupos son comparables al inicio** (edad, CI no verbal del K-BIT, NSE): medias parecidas y DE no escandalosamente distintos = grupos **balanceados**.
2. **Ver heterogeneidad interna**: el TDL es un grupo heterogéneo por definición. Un DE alto revela perfiles distintos conviviendo dentro del grupo — algo que la media oculta.
3. **Calcular t de Student**: la fórmula de la t **usa el DE** en el denominador (es el "ruido"). Sin DE, no hay test inferencial posible.
4. **Interpretar la magnitud del efecto**: una diferencia de 2 puntos es enorme si el DE es 0,5 (4 desvíos) pero trivial si el DE es 5 (0,4 desvíos). Eso se formaliza en el **tamaño del efecto** (d de Cohen = diferencia de medias / DE pooled).

## Cómo aparece típicamente en una tabla

> Grupo TDL (n = 20): M = 12,3 (DE = 3,1)
> Grupo control (n = 20): M = 18,7 (DE = 2,4)

De un vistazo: **cuánto diferían en promedio** y **cuán dispersos eran internamente** — con eso ya se intuye si la diferencia entre grupos es robusta antes de mirar el p-valor.

## En síntesis

- **Media** = dónde está el centro del grupo.
- **DE** = qué tan disperso está el grupo alrededor de ese centro.
- Las dos juntas describen **completamente** una distribución (asumiendo normalidad).
- Sin DE no se puede comparar grupos ni juzgar si una diferencia es relevante.
