# Memoria del Trabajo de Fin de Grado (TFG)

Este repositorio contiene la memoria del **Trabajo de Fin de Grado (TFG)** titulado _"XXXXXX"_. El proyecto está desarrollado para la **carrera de Ingeniería Informática**, con especialización en **Ingeniería de Software**.

### Entorno

- Distribución LaTeX instalada: [`MikTeX`](https://miktex.org/)
- Editor de texto: [`VSCode`](https://code.visualstudio.com/) con la extensión [`LaTeX Workshop`](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

> [!IMPORTANT]  
> En entornos de **Windows** es necesario instalar [`Strawberry Perl`](https://strawberryperl.com/).

### Compilación

- **Manual**: `latexmk -pdf main.tex`
- **VSCode**: `Ctrl + S`.

### Limpieza de archivos temporales

- **Manual**: `latexmk -c`
- **VSCode**: `Ctrl + Alt + C`

### Estructura

```bash
/
├── config/               # Archivos de configuración
│   ├── ifcommands.sty    # Paquete personalizado
│   └── macros.tex        # Definición de macros
├── content/              # Contenido del documento
│   ├── chapters/         # Capítulos individuales
│   └── cover/            # Portada
├── figures/              # Imágenes y gráficos
├── main.tex              # Archivo principal LaTeX
└── referencias.bib       # Archivo de bibliografía
```

### Tipografía de EHU

Para poder usar la [tipografía oficial de EHU](https://www.ehu.eus/es/web/gizartea/ehu-tipografia):
  1. Añadir las fuentes `.otf` en una carpeta `fonts/` en la raíz.
  2. Añadir el siguente código en `main,tex`:
      ```tex
      \usepackage{fontspec}
        % ...
        % \begin{document}
        \setmainfont{EHUSans}[
        Path = {./fonts/},
        Extension = .otf,
        UprightFont    = *-Regular,
        BoldFont       = *-Bold,
        ItalicFont     = *-Italic,
        BoldItalicFont = *-BoldItalic
      ]
      ```
 3. Subir el proyecto entero a **Overleaf** en un `.zip`.
 4. Cambiar el motor de `pdfLaTeX` -> `XeLaTeX`

> [!NOTE]  
> Segun los **citerios de uso** de la normativa oficial:
> - Textos en **euskera**: uso de la versión `EHU Serif`.
> - Textos en **castellano** y en **otros idiomas**: uso de la versión `EHU Sans`.
