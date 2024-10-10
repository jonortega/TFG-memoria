# Memoria del Trabajo de Fin de Grado (TFG)

Este repositorio contiene la memoria del **Trabajo de Fin de Grado (TFG)** titulado _"XXXXXX"_. El proyecto está desarrollado para la **carrera de Ingeniería Informática**, con especialización en **Ingeniería de Software**.

### Entorno

- Distribución LaTeX instalada: [`MikTeX`](https://miktex.org/)
- Editor de texto: [`VSCode`](https://code.visualstudio.com/) con la extensión [`LaTeX Workshop`](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

> [!IMPORTANT]  
> En entornos de **Windows** es necesario instalar [`Strawberry Perl`](https://strawberryperl.com/).

### Compilación

- Con `latexmk`: `latexmk -pdf main.tex`
- VSCode: Al guardar se compila solo.

### Limpieza de archivos temporales

```bash
latexmk -c
```

### Estructura

```bash
/
├── config/               # Archivos de configuración
│   ├── ifcommands.sty    # Paquete personalizado
│   └── macros.tex        # Definición de macros
├── content/              # Capítulos y contenido del documento
│   ├── chapters/         # Capítulos individuales
│   └── cover/            # Portada
├── figures/              # Imágenes y gráficos
├── main.tex              # Archivo principal LaTeX
└── referencias.bib       # Archivo de bibliografía
```