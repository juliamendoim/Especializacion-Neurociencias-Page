# Modelo dual-ruta de lectura

Marco clásico (Coltheart et al., 2001 — *Dual-Route Cascaded model*) para entender cómo el cerebro convierte letras en sonido y significado. Postula **dos vías paralelas** desde la palabra impresa hasta la pronunciación.

## Las dos rutas

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

## Por qué las pseudopalabras solo activan la sublexical

Una pseudopalabra (*plame*, *fortifo*, *cardomito*) es ortotácticamente legal pero inexistente en el léxico. Cuando el lector la encuentra:
- La **ruta léxica falla**: no hay entrada que matchee.
- La **ruta sublexical funciona**: aplica las reglas grafema-fonema y ensambla una pronunciación posible.

Por eso las pseudopalabras son la **prueba pura del funcionamiento de la ruta sublexical**. Marcador diagnóstico clave:
- **Dislexia fonológica**: déficit sublexical → fallan en pseudopalabras.
- **Dislexia superficial**: déficit léxico → fallan en palabras irregulares, no en pseudopalabras.
- **TDL fonológico**: representaciones fonológicas débiles → pseudopalabras largas se desploman (test de repetición de no-palabras, Conti-Ramsden et al. 2001).

## Por qué esto importa especialmente en español

El español tiene **ortografía transparente** (~95 % de correspondencia 1:1 grafema-fonema). Consecuencias:

- La ruta sublexical es **muy eficiente** en español. Casi cualquier palabra se puede leer correctamente con CGF.
- Los lectores expertos en español dependen **menos exclusivamente de la ruta léxica** que en inglés (donde la ortografía es opaca y abundan irregularidades como *colonel*, *yacht*).
- Las pseudopalabras se leen **bastante bien desde edades tempranas** en español, comparado con inglés.
- **Cambia el patrón diagnóstico**: la dislexia en español se manifiesta más en **lentitud** (fluencia, latencias) que en exactitud, porque la ruta sublexical da el resultado correcto pero con costo de tiempo. En inglés se ve más en errores; en español, en tiempos.

## Variables que afectan la ruta sublexical (y a las pseudopalabras)

Efectos típicos que aparecen en papers de lectura:

1. **Longitud**: más letras/sílabas → más operaciones de CGF → peor rendimiento. Pseudopalabras largas son catastróficas para lectores con problemas en esta ruta.
2. **Complejidad silábica**: sílabas CCV (*tres*, *plan*) son más costosas que CV (*pa*, *to*). Grupos consonánticos aumentan errores y latencias.
3. **Vecindad léxica ortográfica**: una pseudopalabra que se parece a muchas palabras reales (*calsoma* parecida a *calzona*, *paloma*) se procesa más rápido — hay influencia léxica indirecta.
4. **Frecuencia de bigramas/trigramas**: secuencias frecuentes (*-ado*, *-ento*, *-ista*) facilitan el ensamblado.
5. **Edad/nivel lector**: la ruta sublexical mejora con la práctica. Niños chicos dependen casi exclusivamente de ella; lectores expertos la usan menos pero la mantienen disponible.

## Cómo se conecta con otros conceptos

- **[Buffer fonológico de salida](buffer-fonologico.md)**: la ruta sublexical produce una secuencia de fonemas que luego pasa por ese buffer antes de articularse. Daño al buffer afecta producción tanto de palabras como de pseudopalabras.
- **[K-BIT y evaluación](../evaluacion/kbit.md)**: el subtest de Vocabulario es léxico; la lectura de pseudopalabras es subléxica. Disociaciones entre ambos perfiles ayudan a clasificar trastornos.
- **TDL morfosintáctico (Acosta, Bedore & Leonard)**: el TDL puede comprometer la ruta sublexical vía representaciones fonológicas pobres, sin que el sistema léxico esté afectado.

## Cuando un paper dice "se midió lectura de pseudopalabras"

Significa que **se está midiendo selectivamente la ruta sublexical**. Comparar el rendimiento en palabras vs. pseudopalabras permite disociar las dos rutas: la diferencia entre ambas da el peso de la contribución léxica, y el rendimiento puro en pseudopalabras da el estado de la sublexical.
