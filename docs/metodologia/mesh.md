# MeSH — Medical Subject Headings

## Qué es

**MeSH** es el **vocabulario controlado** que usa la National Library of Medicine de EE.UU. para indexar todos los artículos médicos y biomédicos en **PubMed / MEDLINE**. Es esencialmente un **diccionario jerárquico estandarizado** de términos médicos.

Lo administra la NLM desde 1960. Se actualiza anualmente y cuenta hoy con ~30.000 descriptores organizados en un árbol jerárquico de 16 ramas principales (anatomía, organismos, enfermedades, sustancias químicas, técnicas, etc.).

## Por qué existe

Antes de MeSH, buscar literatura médica era caótico porque el mismo concepto se podía llamar de muchas formas distintas:

- *"Heart attack"* / *"Myocardial infarction"* / *"MI"* / *"Coronary thrombosis"*
- *"Neuroplasticidad"* / *"Plasticidad neuronal"* / *"Plasticidad cerebral"* / *"Plasticidad sináptica"*

Si un investigador buscaba con un solo término, **se perdía la mitad de los papers relevantes**. MeSH resuelve el problema asignando **un descriptor canónico** a cada concepto, con todos los sinónimos mapeados a él. Buscás *"Myocardial Infarction"* y traés todos los papers, sin importar cómo lo escribió cada autor.

## Cómo se usa

### Para los autores

Cuando escribís un paper biomédico, te piden incluir **palabras clave MeSH** en el resumen. Eso garantiza que cuando se indexe en PubMed, otros investigadores lo encuentren con búsquedas estándar.

Las **revistas latinoamericanas de medicina** (Revista CES Med, SciELO, etc.) suelen incluir tanto las palabras clave **MeSH** (en inglés, estandarizado) como las **DeCS** (Descriptores en Ciencias de la Salud, la versión hispanohablante mantenida por BIREME).

### Para los lectores

Si querés hacer una **revisión sistemática** o búsqueda bibliográfica seria, **buscás por términos MeSH** en PubMed, no por palabras libres. Eso aumenta dramáticamente la precisión y completitud de la búsqueda.

PubMed tiene una herramienta integrada llamada **MeSH Browser** ([https://www.ncbi.nlm.nih.gov/mesh/](https://www.ncbi.nlm.nih.gov/mesh/)) donde podés explorar el árbol y encontrar los términos correctos antes de armar tu query.

## Ejemplo concreto

Si querés buscar literatura sobre **neuroplasticidad**, el descriptor MeSH canónico es:

> **Neuronal Plasticity** (descriptor introducido en 1989)

Sinónimos mapeados al mismo descriptor:
- Brain Plasticity
- Cortical Plasticity
- Neural Plasticity
- Synaptic Plasticity
- Neuroplasticity

Una búsqueda en PubMed con `"Neuronal Plasticity"[MeSH]` te trae **todos** los papers indexados con ese descriptor, sin perderse los que el autor escribió con otra variante.

## Cuándo aparece "MeSH" en un paper que estás leyendo

Cuando un paper médico tiene una sección de palabras clave con algo como:

> *Palabras clave (MeSH): neuroplasticidad, sinapsis, sistema nervioso central, neurofisiología.*

Significa que los autores **declaran** los descriptores MeSH bajo los que se debería indexar el artículo. Sirve para:

- Que el paper sea **encontrable** en búsquedas estandarizadas.
- Que los lectores entiendan rápidamente **el dominio de aplicación** del paper.
- Conectar con otros papers del mismo descriptor.

## Conexión con otros recursos del sitio

- **[PRISMA](prisma.md)**: las revisiones sistemáticas usan MeSH como una de sus herramientas clave para garantizar búsquedas exhaustivas y replicables. La sección de "estrategia de búsqueda" de PRISMA suele incluir los descriptores MeSH usados.
- **DeCS (BIREME)**: equivalente de MeSH para literatura hispanohablante de salud. Trabaja en coordinación con MeSH y la mayoría de descriptores tienen correspondencia directa.

## Lecturas y herramientas

- **MeSH Browser** — [https://www.ncbi.nlm.nih.gov/mesh/](https://www.ncbi.nlm.nih.gov/mesh/) — para explorar el árbol y encontrar descriptores correctos.
- **DeCS** — [https://decs.bvsalud.org/](https://decs.bvsalud.org/) — la versión hispanohablante.
- **MEDLINE/PubMed Indexing** — manuales sobre cómo se indexa cada paper en la NLM.
