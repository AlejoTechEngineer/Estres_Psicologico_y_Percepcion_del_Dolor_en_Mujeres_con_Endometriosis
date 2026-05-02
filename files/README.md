# Instrucciones de Compilación — VS Code + LaTeX Workshop

## Archivos del proyecto

```
📁 proyecto/
 ├── endometriosis_articulo.tex   ← Archivo principal
 ├── referencias.bib              ← Base de datos bibliográfica (BibLaTeX)
 └── README.md                    ← Este archivo
```

---

## Requisitos previos

### 1. Distribución LaTeX
Instala **TeX Live** (recomendado) o **MiKTeX**:
- TeX Live (Windows/Mac/Linux): https://tug.org/texlive/
- MiKTeX (Windows): https://miktex.org/

### 2. Extensión VS Code
Instala **LaTeX Workshop** desde el Marketplace de VS Code:
`Ext ID: James-Yu.latex-workshop`

### 3. Biber
Biber viene incluido con TeX Live y MiKTeX.
Verificar instalación en terminal:
```bash
biber --version
```

---

## Configuración de LaTeX Workshop

Agrega esto a tu `settings.json` de VS Code
(`Ctrl+Shift+P` → "Open User Settings JSON"):

```json
"latex-workshop.latex.recipes": [
  {
    "name": "pdflatex → biber → pdflatex × 2",
    "tools": ["pdflatex", "biber", "pdflatex", "pdflatex"]
  }
],
"latex-workshop.latex.tools": [
  {
    "name": "pdflatex",
    "command": "pdflatex",
    "args": [
      "-synctex=1",
      "-interaction=nonstopmode",
      "-file-line-error",
      "%DOC%"
    ]
  },
  {
    "name": "biber",
    "command": "biber",
    "args": ["%DOCFILE%"]
  }
],
"latex-workshop.latex.autoBuild.run": "onSave"
```

---

## Compilación manual (terminal)

Si prefieres compilar desde la terminal, ejecuta los
siguientes comandos en orden dentro de la carpeta del proyecto:

```bash
pdflatex endometriosis_articulo.tex
biber endometriosis_articulo
pdflatex endometriosis_articulo.tex
pdflatex endometriosis_articulo.tex
```

> **¿Por qué cuatro pasos?**
> pdflatex genera las referencias auxiliares → biber procesa
> la bibliografía → las dos últimas pasadas de pdflatex
> resuelven las citas y la numeración final correctamente.

---

## Paquetes requeridos

Todos incluidos en TeX Live Full. Si usas MiKTeX se instalan
automáticamente al compilar:

| Paquete         | Uso                              |
|-----------------|----------------------------------|
| babel (spanish) | Tipografía y separación silábica |
| biblatex + biber| Referencias APA 7                |
| geometry        | Márgenes de página               |
| titlesec        | Formato de secciones             |
| mdframed        | Cajas de texto destacadas        |
| xcolor + table  | Colores en tablas                |
| booktabs        | Tablas profesionales             |
| tabularx        | Tablas de ancho flexible         |
| fancyhdr        | Encabezados y pies de página     |
| hyperref        | Hipervínculos y metadatos PDF    |
| microtype       | Mejoras tipográficas automáticas |
| setspace        | Control de interlineado          |

---

## Solución de problemas frecuentes

**"Package babel Error: Unknown option `es-tabla`"**
→ Actualiza babel: `tlmgr update babel babel-spanish`

**"I found no \bibdata command"**
→ Asegúrate de que `referencias.bib` está en la misma
  carpeta que el `.tex` y vuelve a correr biber.

**Las citas aparecen como [?]**
→ Ejecuta la secuencia completa de 4 pasos nuevamente.

**Caracteres especiales (á, é, ñ) no aparecen**
→ Verifica que el archivo está guardado en UTF-8
  (`File → Save with Encoding → UTF-8` en VS Code).
