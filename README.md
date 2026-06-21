<div align="center">

# Estrés Psicológico y Percepción del Dolor en Mujeres con Endometriosis

> **Revisión Narrativa con Estrategia de Búsqueda Sistemática**

[![LaTeX](https://img.shields.io/badge/Escrito%20en-LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)](https://www.latex-project.org/)
[![PDF](https://img.shields.io/badge/Artículo-PDF%20disponible-DC143C?style=for-the-badge&logo=adobe-acrobat-reader&logoColor=white)](./endometriosis_articulo.pdf)
[![Citas](https://img.shields.io/badge/Normas-APA%207%C2%AA%20edición-003087?style=for-the-badge)](https://apastyle.apa.org/)
[![Biber](https://img.shields.io/badge/Bibliografía-BibLaTeX%20%2B%20Biber-6A0DAD?style=for-the-badge)](http://biblatex-biber.sourceforge.net/)
[![Licencia](https://img.shields.io/badge/Licencia-CC%20BY--NC%204.0-lightgrey?style=for-the-badge)](https://creativecommons.org/licenses/by-nc/4.0/)

</div>

---

---

## Autoras

| Nombre | Programa | Institución |
|---|---|---|
| Rosaura Sandoval Carreño | Psicología | Universitaria de Colombia |
| Sara Nohelia Gómez Salazar | Psicología | Universitaria de Colombia |
| Ana María Estévez Caraballo | Psicología | Universitaria de Colombia |

📍 Bogotá, D.C., Colombia — 2025
📧 psicologia@unicolombia.edu.co

---

## Resumen

La endometriosis afecta aproximadamente al **10 % de las mujeres en edad reproductiva** a nivel global (más de 190 millones de personas), constituyendo una de las enfermedades ginecológicas crónicas de mayor impacto en la calidad de vida. A pesar de su elevada prevalencia, su dimensión psicológica permanece subvalorada en los modelos de atención clínica.

Este artículo examina, a partir de la evidencia científica disponible, la **relación entre el estrés psicológico crónico y la percepción del dolor** en mujeres con endometriosis, identificando los mecanismos neurobiológicos implicados y las estrategias de intervención desde la psicología de la salud.

---

## Hallazgos Principales

```
Estrés Crónico
     │
     ▼
Activación sostenida del Eje HPA
(CRH → ACTH → Cortisol / Catecolaminas)
     │
     ├──▶ Estado proinflamatorio (↑ IL-6, TNF-α, prostaglandinas)
     │         └──▶ Asociación con proliferación endometrial ectópica
     │
     └──▶ Sensibilización Central del Dolor
               ├── Hiperalgesia · Alodinia
               ├── Alteración de circuitos: Amígdala — CPF — PAG
               └── Disociación lesión anatómica / intensidad subjetiva
                         │
                         ▼
              Ciclo de retroalimentación negativa
         Dolor  ──────▶  Estrés  ──────▶  Dolor
```

### Impacto Psicológico documentado

- **>75 %** de pacientes presentan síntomas depresivos clínicamente relevantes
- Prevalencia de ansiedad y depresión significativamente superior a la población general
- Retraso diagnóstico promedio: **7–10 años** desde inicio de síntomas
- Factores amplificadores: catastrofización del dolor, kinesiofobia, aislamiento social

### Intervenciones con evidencia prometedora

| Componente | Técnicas | Mecanismo de acción |
|---|---|---|
| Educación en Neurociencia del Dolor (PNE) | Psicoeducación sobre mecanismos del SNC | Reduce amenaza percibida y catastrofización |
| Terapia Cognitivo-Conductual (TCC) | Reestructuración cognitiva, activación conductual | Modifica patrones disfuncionales |
| Técnicas Mente-Cuerpo | Mindfulness, yoga terapéutico, respiración diafragmática | Regula eje HPA y favorece inhibición descendente |
| Intervención en Red de Apoyo | Psicoeducación familiar, grupos entre pares | Reduce aislamiento y fortalece afrontamiento |

---

## Estructura del Repositorio

```
📦 Estr-s_Psicol-gico_y_Percepci-n_del_Dolor_en_Mujeres_con_Endometriosis
 │
 ├── 📄 README.md                        ← Este archivo
 ├── 📕 endometriosis_articulo.pdf       ← Artículo compilado (listo para leer)
 │
 └── 📁 files/
      ├── endometriosis_articulo.tex     ← Código fuente LaTeX
      ├── referencias.bib               ← Base de datos bibliográfica (BibLaTeX)
      └── README.md                     ← Guía de compilación LaTeX detallada
```

---

## Lectura Rápida

El PDF compilado está disponible directamente en la raíz del repositorio:

**[📕 Descargar / Ver artículo completo](./endometriosis_articulo.pdf)**

---

## Compilación desde Fuente

> Requiere una distribución LaTeX (TeX Live o MiKTeX) con Biber.

```bash
# Secuencia completa de compilación
pdflatex endometriosis_articulo.tex
biber    endometriosis_articulo
pdflatex endometriosis_articulo.tex
pdflatex endometriosis_articulo.tex
```

Consulta [`files/README.md`](./files/README.md) para instrucciones detalladas de configuración en VS Code con LaTeX Workshop.

### Dependencias principales

| Paquete | Función |
|---|---|
| `biblatex` + `biber` | Referencias en formato APA 7.ª ed. |
| `babel` (spanish) | Tipografía y separación silábica en español |
| `mdframed` | Cajas de texto y preguntas de investigación |
| `titlesec` | Estilos de sección personalizados |
| `xcolor` + `tabularx` | Tablas con color y ancho flexible |
| `fancyhdr` | Encabezados y pies de página |
| `hyperref` | Hipervínculos y metadatos del PDF |
| `qrcode` | Código QR en portada |

---

## Palabras Clave

`endometriosis` · `estrés crónico` · `percepción del dolor` · `eje HPA` · `sensibilización central` · `psicología de la salud` · `modelo biopsicosocial` · `terapia cognitivo-conductual` · `mindfulness` · `dolor pélvico crónico`

---

## Citación

Si este trabajo resulta útil para tu investigación, puedes citarlo como:

```bibtex
@article{SandovalGomezEstevez2025,
  author    = {Sandoval Carreño, Rosaura and
               Gómez Salazar, Sara Nohelia and
               Estévez Caraballo, Ana María},
  title     = {Estrés Psicológico y Percepción del Dolor
               en Mujeres con Endometriosis},
  year      = {2025},
  note      = {Revisión narrativa con estrategia de búsqueda sistemática.
               Universitaria de Colombia, Programa de Psicología, Bogotá},
  url       = {https://github.com/AlejoTechEngineer/Estr-s_Psicol-gico_y_Percepci-n_del_Dolor_en_Mujeres_con_Endometriosis}
}
```

---

## Licencia

Este trabajo se distribuye bajo la licencia
**Creative Commons Atribución–NoComercial 4.0 Internacional (CC BY-NC 4.0)**.

Puedes compartirlo y adaptarlo libremente para fines no comerciales,
siempre que se otorgue el crédito correspondiente a las autoras.

---

<div align="center">
  <sub>
    Universitaria de Colombia · Programa de Psicología · Bogotá, D.C. · 2025
  </sub>
</div>
