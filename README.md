# Especialización en Neurociencias — Apuntes compartidos

Sitio web público con apuntes y conceptos transversales de la **Especialización en Neurociencias Cognitivas del Lenguaje y la Lectura** (UBA, 2026).

## ⚠️ Sobre el contenido

**Los apuntes están producidos en diálogo con Claude (Anthropic)**, un modelo de lenguaje (LLM). Surgieron de conversaciones donde se pedía explicar, ampliar o aclarar conceptos que aparecían en clases y lecturas, y luego se curaron/editaron las respuestas útiles.

**Implicaciones**: pueden contener errores; no reemplazan la lectura de los textos del programa; reflejan un recorrido personal de cursada. Verificá con fuentes primarias antes de citar.

## 🌐 Sitio publicado

→ **https://juliamendoim.github.io/Especializacion-Neurociencias-Page/**

## 📁 Estructura

```
docs/                       # contenido (markdown)
├── index.md                # página de inicio
└── aprendizajes-generales.md
mkdocs.yml                  # config del sitio
.github/workflows/deploy.yml # CI: build automático en cada push a main
```

## ✏️ Cómo agregar contenido

1. Editá o agregá archivos `.md` en `docs/`.
2. Si es una página nueva, agregala a `nav:` en `mkdocs.yml`.
3. Commit + push a `main`.
4. El sitio se reconstruye automáticamente (~1 min).

## 🛠️ Probar localmente (opcional)

```bash
pip install mkdocs-material
mkdocs serve
```

Y abrís http://localhost:8000.

## 🤝 Contribuir

Pull requests bienvenidos. Para errores, sugerencias o pedidos: abrí un *issue*.
