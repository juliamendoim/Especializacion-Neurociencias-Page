# Bases físico-químicas para entender la neurona

Repaso mínimo de los conceptos de química y física que aparecen en cuanto se empieza a hablar de potencial de membrana, sinapsis y canales iónicos. Está pensado para alguien sin background en ciencias duras — la idea es **lo justo y necesario para leer la bibliografía sin atascarse en cada palabra**.

## Átomos y moléculas

**Átomo**: la unidad mínima de un elemento químico. Tiene:

- Un **núcleo** con **protones** (carga eléctrica positiva) y **neutrones** (sin carga).
- **Electrones** (carga negativa) girando alrededor del núcleo.

En un átomo **neutro**, la cantidad de protones es igual a la cantidad de electrones — las cargas positivas y negativas se cancelan, la carga total es cero.

**Molécula**: dos o más átomos unidos por enlaces químicos. Ejemplos:

- **Agua** (H₂O) — dos átomos de hidrógeno + uno de oxígeno.
- **Glucosa** (C₆H₁₂O₆).
- **Sal de mesa** (NaCl) — un átomo de sodio + uno de cloro.
- **ATP** (adenosín trifosfato) — la "moneda energética" de las células.

## Iones — el concepto central para neurofisiología

Un **ion** es un átomo (o molécula) que **ganó o perdió electrones** y por lo tanto **tiene carga eléctrica neta**.

- Si **perdió** electrones → tiene **carga positiva** (queda con más protones que electrones).
- Si **ganó** electrones → tiene **carga negativa**.

Los iones que importan en neurofisiología:

| Ion | Símbolo | Carga | De dónde viene |
|---|---|---|---|
| **Sodio** | Na⁺ | +1 | Átomo de sodio que perdió 1 electrón |
| **Potasio** | K⁺ | +1 | Átomo de potasio que perdió 1 electrón |
| **Cloruro** | Cl⁻ | –1 | Átomo de cloro que ganó 1 electrón |
| **Calcio** | Ca²⁺ | +2 | Átomo de calcio que perdió 2 electrones |

Cuando se disuelve sal (NaCl) en agua, **se disocia** en Na⁺ y Cl⁻ flotando libres en el líquido. Por eso el medio interno y externo de las células (que es básicamente agua con sales disueltas) está lleno de iones.

**Iones ≠ moléculas**: una molécula como el agua o la glucosa no tiene carga neta. Un ion sí. Esta distinción es clave porque **solo los iones generan corriente eléctrica** cuando se mueven.

## Cargas eléctricas: atracción y repulsión

Regla básica (ley de Coulomb):

- **Cargas opuestas se atraen** (un Na⁺ se acerca a un Cl⁻).
- **Cargas iguales se repelen** (dos Na⁺ se alejan; dos Cl⁻ se alejan).

Esto es lo que ordena el comportamiento de los iones dentro y fuera de la neurona: tienden a moverse hacia donde hay carga opuesta y a alejarse de donde hay carga igual.

## Voltaje (diferencia de potencial eléctrico)

**Voltaje** = diferencia de carga eléctrica entre dos puntos. Se mide en **volts (V)** o **milivolts (mV)** — 1 V = 1000 mV.

Una analogía útil: el voltaje es como la **diferencia de altura** entre dos puntos. Si hay diferencia, "algo puede caer" — en este caso, los iones tienden a moverse para igualar las cargas.

En neurociencia, casi siempre se habla del **voltaje del interior de la célula medido contra el exterior**:

- **Potencial de membrana en reposo**: el interior de la neurona está **alrededor de –70 mV** respecto del exterior. Es decir, **el interior es más negativo** que el exterior por unos 70 milivolts.

Por qué hay esa diferencia: dentro y fuera de la célula hay **distintas concentraciones** de los distintos iones, y los iones no pueden pasar libremente por la membrana (necesitan canales específicos).

## Concentración y gradientes

**Concentración**: cuántas partículas hay en un volumen determinado. Por ejemplo, "alta concentración de K⁺ adentro" significa "muchos iones K⁺ por unidad de volumen del citoplasma".

En condiciones normales en una neurona:

| Ion | Concentración INTRA-celular | Concentración EXTRA-celular |
|---|---|---|
| Na⁺ | Baja | **Alta** |
| K⁺ | **Alta** | Baja |
| Cl⁻ | Baja | **Alta** |
| Ca²⁺ | **Muy baja** | Mucho más alta |

**Gradiente**: una diferencia entre dos lugares. Hay dos tipos relevantes:

- **Gradiente de concentración**: los iones tienden a moverse desde donde hay mucha concentración hacia donde hay poca, para igualar (como una gota de tinta que se difunde en agua).
- **Gradiente eléctrico**: los iones positivos tienden a moverse hacia donde hay carga negativa (atracción) y viceversa.

Cuando se combinan ambos se habla de **gradiente electroquímico** — la "fuerza" total que mueve a un ion a través de la membrana.

Ejemplo: el Na⁺ tiene **alta concentración afuera** (quiere entrar para igualar) y además el interior es **negativo** (lo atrae). Las dos fuerzas empujan en la misma dirección → si se abre un canal de Na⁺, el Na⁺ entra rapidísimo.

## Por qué los canales son selectivos (canal de Na⁺ vs. canal de K⁺)

Pregunta natural: si un canal es un agujero en la membrana, ¿cómo hace para dejar pasar **solo un tipo de ion** y no otros? Los canales **no son simples agujeros** — son proteínas con una arquitectura química que distingue un ion de otro con una precisión enorme.

### El "filtro de selectividad"

Cada canal tiene una región específica llamada **filtro de selectividad** (*selectivity filter*), donde el ion tiene que pasar **uno por uno** y donde se decide quién entra y quién no.

### El truco contraintuitivo: la hidratación

A primera vista uno esperaría que un canal "pequeño para Na⁺" deje pasar fácil al K⁺ (que es más chico)... pero al revés: **el K⁺ desnudo es MÁS GRANDE que el Na⁺ desnudo** (mayor radio atómico).

Y peor: en agua los iones no están desnudos — están rodeados por una **capa de agua** (*hydration shell*) porque las moléculas de agua se orientan alrededor de la carga del ion. Esto invierte la relación de tamaños:

- **Na⁺ hidratado** → más grande (porque, al ser más chico el ion, atrae al agua con más fuerza y carga una capa más gruesa).
- **K⁺ hidratado** → más chico (capa de agua más floja).

Cuando un ion entra al canal tiene que **deshidratarse** (soltar el agua), y eso cuesta energía. El canal hace su magia precisamente en cómo facilita o impide ese paso.

### Canal de K⁺ (Nobel 2003 a Roderick MacKinnon)

El filtro del canal de K⁺ tiene **4 oxígenos** orientados con una geometría exactísima que **imita la capa de agua del K⁺**. Cuando el K⁺ entra, el filtro lo "abraza" como si fuera su capa de agua → **no le cuesta energía deshidratarse**.

Para el Na⁺ en el mismo canal:

- Es más chico → si entrara, no llegaría a tocar los 4 oxígenos del filtro (le quedan grandes).
- Para deshidratarse necesita un reemplazo perfecto del agua, y el filtro de K⁺ no se lo da.

Resultado: el K⁺ pasa unas **10.000 veces mejor** que el Na⁺ por un canal de K⁺.

### Canal de Na⁺

Estrategia distinta pero con la misma lógica:

- El filtro tiene un anillo cargado negativamente (un aminoácido glutamato).
- La geometría del poro y la disposición de las cargas favorece al **Na⁺ con una sola molécula de agua** (parcialmente hidratado).
- El K⁺ es demasiado grande para acomodarse en esa geometría.

### El principio general

Los canales **no filtran por tamaño bruto**. Filtran por una combinación de:

1. **Geometría del poro** (encaje físico).
2. **Cargas eléctricas** dentro del filtro.
3. **Energía de hidratación** — cuánto cuesta soltar el agua y si el filtro la "reemplaza" bien.

Es química fina, no plomería.

Por qué importa: esto justifica que se hable de "canales de Na⁺", "canales de K⁺", "canales de Ca²⁺" como entidades **funcionalmente distintas**. La selectividad es lo que permite que el potencial de acción tenga fases bien separadas (entrada de Na⁺ y luego salida de K⁺) — sin selectividad no habría potencial de acción tal como lo conocemos.

## Por qué importa todo esto

Sin este vocabulario mínimo, los textos del seminario son una sopa de letras. Pero con esto en la mano, frases como:

> *"Al abrirse los canales de Na⁺, el ion entra siguiendo su gradiente electroquímico, despolarizando la membrana."*

se vuelven leíbles: "se abre la puerta para el Na⁺ → el Na⁺ entra porque afuera hay más y porque adentro es negativo → al entrar cargas positivas, el interior se vuelve menos negativo".

## Conexión con el resto del sitio

Este es **pre-requisito** para:

- **Potencial de acción** (futura entrada) — usa todos estos conceptos.
- **Sinapsis química** — el neurotransmisor abre canales que dejan pasar iones específicos.
- **[Plasticidad estructural y sináptica](plasticidad-estructural-mecanismos.md)** — los receptores AMPA/NMDA son canales iónicos.
- **[Mecanismos de recuperación post-lesión](mecanismos-recuperacion-post-lesion.md)** — el primer paso de la recuperación es restablecer el equilibrio iónico.

## Lecturas

- **Carlson, N. R. (2013)** *Fundamentos de Fisiología de la Conducta*. Pearson. Cap. 2. — repaso de bases biológicas accesible.
- **Kandel, Schwartz & Jessell (2013)** *Principios de Neurociencia*. McGrawHill. Caps. 5–7. — todo el detalle, ya un poco técnico.
- **Doyle, D. A. et al. (1998)** "The structure of the potassium channel: molecular basis of K⁺ conduction and selectivity". *Science* 280:69-77. — el paper de MacKinnon que cristalizó el canal de K⁺ y desentrañó el filtro de selectividad (Nobel 2003).
- **Khan Academy** y **Concept Neuroscience**: tienen videos muy claros de 5–10 minutos sobre cada uno de estos conceptos si la lectura no alcanza.
