# AI/ML y Ciencias Sociales — Grupo de Lectura

Sitio web del grupo de lectura interdisciplinario organizado por el **USFQ Data Hub**, donde profesores e investigadores de economía, ciencia política, sociología, antropología, relaciones internacionales, ciencias de la computación y matemática exploran cómo la inteligencia artificial y el machine learning están transformando las ciencias sociales.

🔗 **Sitio en vivo:** [https://TU-USUARIO.github.io/grupo-lectura-aiml/](https://TU-USUARIO.github.io/grupo-lectura-aiml/)

---

## Estructura del repositorio

```
├── index.html            ← Sitio web (no requiere edición)
├── bibliografia.xlsx     ← Archivo de datos (todo el contenido editable)
└── README.md
```

El sitio carga dinámicamente todo su contenido desde `bibliografia.xlsx` usando [SheetJS](https://sheetjs.com/). Para actualizar el contenido del sitio, solo se necesita modificar el archivo Excel y hacer push al repositorio.

---

## Contenido del archivo Excel

El archivo `bibliografia.xlsx` contiene 5 hojas:

| Hoja | Contenido | Columnas principales |
|---|---|---|
| **Sesiones** | Las 14 sesiones del semestre | `num`, `title`, `subtitle`, `tag`, lecturas principal y opcional, preguntas de discusión |
| **Libros** | Libros de referencia | `badge_type`, `badge_label`, `title`, `description`, `link_text`, `link_url` |
| **Herramientas** | Cursos y herramientas | misma estructura que Libros |
| **Paquetes** | Paquetes de R y Python | `language`, `packages` |
| **DatosAbiertos** | Fuentes de datos para América Latina | `name`, `url` |

### Detalle de columnas — Hoja "Sesiones"

| Columna | Descripción |
|---|---|
| `num` | Número de sesión (1–14) |
| `title` | Título de la sesión |
| `subtitle` | Subtítulo descriptivo |
| `tag` | Tipo: `tech`, `social`, o `bridge` |
| `main_cite` | Cita bibliográfica de la lectura principal |
| `main_access` | Acceso (ej: "✅ Open Access", "💰 Paywall") |
| `main_link` | URL de la lectura principal (dejar vacío si no hay) |
| `main_link_text` | Texto del enlace (ej: "Leer →") |
| `main_note` | Nota descriptiva sobre la lectura |
| `opt_label` | Etiqueta de la lectura opcional (ej: "Opcional") |
| `opt_cite` | Cita bibliográfica de la lectura opcional |
| `opt_access` | Acceso de la lectura opcional |
| `opt_link` | URL de la lectura opcional |
| `opt_link_text` | Texto del enlace opcional |
| `opt_note` | Nota sobre la lectura opcional |
| `discussion` | Preguntas para la discusión |

### Detalle de columnas — Hojas "Libros" y "Herramientas"

| Columna | Descripción |
|---|---|
| `badge_type` | Tipo de badge: `free`, `book`, o `course` |
| `badge_label` | Texto del badge (ej: "Gratis", "Libro", "Trad. español") |
| `title` | Título del recurso |
| `description` | Descripción breve |
| `link_text` | Texto del enlace |
| `link_url` | URL (dejar vacío si no tiene enlace) |

---

## Cómo actualizar el contenido

1. Descargar `bibliografia.xlsx` del repositorio (o desde el propio sitio web bajo "Bibliografía completa")
2. Editar en Excel, Google Sheets o LibreOffice Calc
3. Guardar como `.xlsx`
4. Subir el archivo actualizado al repositorio: **Add file → Upload files → Commit**
5. El sitio se actualiza automáticamente en 1–2 minutos

### Ejemplos de cambios comunes

| Quiero… | Qué hacer |
|---|---|
| Agregar una sesión nueva | Agregar una fila al final de la hoja "Sesiones" |
| Cambiar una lectura | Editar las columnas correspondientes en la fila de esa sesión |
| Agregar un libro de referencia | Agregar una fila en la hoja "Libros" |
| Agregar un curso o herramienta | Agregar una fila en la hoja "Herramientas" |
| Agregar una fuente de datos abiertos | Agregar una fila en la hoja "DatosAbiertos" |
| Eliminar una sesión | Eliminar la fila correspondiente |

---

## Tecnologías

- HTML + CSS + JavaScript vanilla
- [SheetJS (xlsx.js)](https://sheetjs.com/) para la lectura del archivo Excel en el navegador
- [EB Garamond](https://fonts.google.com/specimen/EB+Garamond) para títulos (Google Fonts)
- Hospedado en GitHub Pages

---

## Formato de las sesiones

Cada sesión tiene una etiqueta (`tag`) que determina su color y categoría:

| Tag | Etiqueta | Descripción |
|---|---|---|
| `tech` | Técnico | Sesiones con énfasis en herramientas y métodos |
| `social` | Crítico | Sesiones con énfasis en impacto social y político |
| `bridge` | Puente | Sesiones que conectan ambas dimensiones |

---

## Licencia

Recurso curado para uso académico por el USFQ Data Hub.
