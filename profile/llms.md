# Claude Skills - Documentación para LLMs

> Este archivo contiene toda la documentación del sitio Claude Skills en formato optimizado para modelos de lenguaje.
> Generado automáticamente el 2025-12-04.

## Acerca de Claude Skills

Claude Skills (https://claudeskills.es) es la primera academia y galería de skills en español dedicada a Claude, el modelo de lenguaje de Anthropic.

El sitio ofrece:
- **Galería de Skills**: Colección de extensiones y configuraciones descargables para Claude
- **Cursos** (próximamente): Formación práctica sobre Claude AI
- **Comunidad** (próximamente): Espacio para usuarios de Claude en español

## Instalación de Skills

### En Claude Cloud (claude.ai)
1. Descarga el archivo `.skill` desde la galería
2. Abre Claude.ai → Settings
3. Carga el archivo `.skill`

### En Claude Code (CLI / VSCode)
1. Descarga el archivo `.skill`
2. Cambia la extensión a `.zip`
3. Extrae el contenido
4. Muévelo a `~/.claude/skills/`

---

# Galería de Skills


## Img To Webp

**Descripción:** Converts and image to webp format optimized for Web Development

**Autor:** claudeskills | **Licencia:** MIT License

**Tags:** design, forntend, optimization

**Enlaces:**
- Repositorio: https://github.com/claudeskills/img-to-webp
- Descarga: https://raw.githubusercontent.com/claudeskills/img-to-webp/main/image-to-webp.skill
- Página: https://claudeskills.es/skills/img-to-webp/

### Resumen

Este es un resumen breve en español de la skill de Claude "Img To Webp":

Esta skill de Claude permite convertir imágenes a formato WebP, optimizado para desarrollo web. Soporta diferentes formatos de entrada como PNG, JPG, GIF, TIFF y BMP. Utiliza múltiples backends para realizar las conversiones de manera eficiente, y permite el procesamiento por lotes de carpetas completas. Además, ofrece control de calidad y muestra el porcentaje de compresión logrado para cada archivo.

### Documentación

![SVG Cleaner](./assets/img-to-webp.svg)

# Image to WebP Skill

A Claude skill for converting and optimizing images to WebP format with batch processing support.

## Features

- 🖼️ **Convert images to WebP**: PNG, JPG, GIF, TIFF, BMP supported
- ⚡ **Multiple backends**: sharp (Node.js), cwebp, or Python fallback
- 📦 **Batch processing**: Process entire folders at once
- 🎛️ **Quality control**: Configurable compression levels
- 📊 **Size reporting**: Shows compression percentage for each file

## Installation

**A. Claude AI** (Claude in the cloud )

1. Download `image-to-webp.skill`
2. Open Claude.ai
3. Go to Settings → Skills
4. Upload the `.skill` file

**B. Claude Code or CLI (local installation)**

1. Download `image-to-webp.skill`
2. Change the file extension to zip `image-to-webp.skill`  → `image-to-webpage.zip` 
3. De compress the .zip in the ` .claude/sillks/` folder
4. remove the zip file

## Usage Examples

**Convert a single image:**
```
Convert this PNG to WebP
```

**Process a folder:**
```
Convert all images in /path/to/images/ to WebP
```

**High quality conversion:**
```
Convert this image to WebP with 95% quality
```

## How It Works

The skill tries tools in this order:

1. **sharp** (Node.js) - Fastest, best quality
2. **cwebp** (Google CLI) - Excellent compression
3. **Python/Pillow** - Bundled fallback, always works

## Quality Presets

| Quality | Use Case |
|---------|----------|
| 75-80 | Maximum compression, acceptable quality |
| 85 | Balanced (default) |
| 90-95 | High quality, larger files |

## Output

- Single file: `filename.webp`
- Batch folder: Each image converted alongside original
- Reports size reduction percentage

## Requirements

- Claude Desktop or Claude.ai with Skills enabled
- One of: Node.js (sharp), cwebp CLI, or Python with Pillow

## License

MIT License - See LICENSE file for details

## Contributing

Issues and pull requests welcome!

## Author

Created by Daniel Serrano for Claude Skills


---


## Svg Cleaner

**Descripción:** Clean, optimize, and batch-process SVG files with support for sprite generation.

**Autor:** claudeskills | **Licencia:** MIT License

**Tags:** design, frontend, optimization-tools

**Enlaces:**
- Repositorio: https://github.com/claudeskills/svg-cleaner
- Descarga: https://raw.githubusercontent.com/claudeskills/svg-cleaner/main/svg-cleaner.skill
- Página: https://claudeskills.es/skills/svg-cleaner/

### Resumen

El SVG Cleaner es una habilidad de Claude que permite limpiar, optimizar y procesar por lotes archivos SVG, además de generar sprites. Puede fusionar trazados, eliminar fondos y aplicar el color actual. También integra SVGO para optimizar los archivos y puede extraer elementos específicos como letras de logotipos. Admite el procesamiento por lotes de carpetas completas de archivos SVG y la generación automática de sprites SVG.

### Documentación

![SVG Cleaner](./assets/svg-cleaner-banner.svg)

# SVG Cleaner Skill

A Claude skill for cleaning, optimizing, and batch-processing SVG files with support for sprite generation.

## Features

- 🧹 **Clean SVG files**: Merge paths, remove backgrounds, convert to currentColor
- ⚡ **Optimize**: SVGO integration with fallback for manual optimization
- 📦 **Batch processing**: Process entire folders of SVGs at once
- 🎨 **Sprite generation**: Automatically create SVG sprites from folders
- 🎯 **Element extraction**: Extract specific portions (e.g., single letters from logos)

## What It Does

### Single File Processing
- Merges multiple paths into one
- Removes backgrounds and clipPaths
- Applies `currentColor` for flexible theming
- Optimizes with SVGO (25-35% size reduction)

### Batch Folder Processing
- Finds all `.svg` files in a folder
- Cleans each SVG individually
- Saves as `filename-cc.svg`
- Creates combined sprite as `foldername-sprite-cc.svg`

## Installation

**A. Claude AI** (Claude in the cloud )

1. Download `svg-cleaner.skill`
2. Open Claude.ai
3. Go to Settings → Skills
4. Upload the `.skill` file

**B. Claude Code or CLI (local installation)**

1. Download `image-to-webp.skill`
2. Change the file extension to zip `svg-cleaner.skill`  → `svg-cleaner.zip` 
3. De compress the .zip in the ` .claude/sillks/` folder
4. remove the zip file

## Usage Examples

**Clean a single SVG:**
```
Clean this logo SVG and apply currentColor
```

**Process a folder:**
```
Clean all SVGs in /path/to/icons/ and create a sprite
```

**Extract specific element:**
```
Extract just the "g" letter from this logo
```

## Output Files

**Single file mode:**
- `filename-clean.svg` - Merged paths, no background
- `filename-currentcolor.svg` - With currentColor applied
- `filename-optimized.svg` - SVGO processed

**Batch folder mode:**
- `filename-cc.svg` - Each cleaned SVG
- `foldername-sprite-cc.svg` - Combined sprite with all icons

## Sprite Usage

Use the generated sprites in HTML:

```html
<svg>
  <use href="icons-sprite-cc.svg#logo"/>
</svg>
```

## Requirements

- Claude Desktop or Claude.ai with Skills enabled
- Optional: Node.js (for SVGO optimization)

## License

MIT License - See LICENSE file for details

## Contributing

Issues and pull requests welcome!

## Author

Created by Daniel Serrano for Claude Skills


---


## Css To Oklch

**Descripción:** Claude Code skill to convert CSS colors to OKLCH format

**Autor:** claudeskills | **Licencia:** No especificada

**Tags:** Ninguno

**Enlaces:**
- Repositorio: https://github.com/claudeskills/css-to-oklch
- Descarga: https://raw.githubusercontent.com/claudeskills/css-to-oklch/master/css-to-oklch.skill
- Página: https://claudeskills.es/skills/css-to-oklch/

### Resumen

Esta skill de Claude permite limpiar, optimizar y procesar por lotes archivos SVG, incluyendo la generación de sprites. Algunas de las principales características son la eliminación de fondos y agrupación de elementos, la optimización con SVGO, y la creación de sprites SVG a partir de carpetas de archivos. Esta herramienta facilita el mantenimiento y la reutilización de iconos SVG en proyectos web.

### Documentación

# SVG Cleaner Skill

![SVG Cleaner](./assets/svg-cleaner-banner.svg)

A Claude skill for cleaning, optimizing, and batch-processing SVG files with support for sprite generation.

## Features

- 🧹 **Clean SVG files**: Merge paths, remove backgrounds, convert to currentColor
- ⚡ **Optimize**: SVGO integration with fallback for manual optimization
- 📦 **Batch processing**: Process entire folders of SVGs at once
- 🎨 **Sprite generation**: Automatically create SVG sprites from folders
- 🎯 **Element extraction**: Extract specific portions (e.g., single letters from logos)

## What It Does

### Single File Processing
- Merges multiple paths into one
- Removes backgrounds and clipPaths
- Applies `currentColor` for flexible theming
- Optimizes with SVGO (25-35% size reduction)

### Batch Folder Processing
- Finds all `.svg` files in a folder
- Cleans each SVG individually
- Saves as `filename-cc.svg`
- Creates combined sprite as `foldername-sprite-cc.svg`

## Installation

1. Download `svg-cleaner.skill`
2. Open Claude.ai
3. Go to Settings → Skills
4. Upload the `.skill` file

## Usage Examples

**Clean a single SVG:**
```
Clean this logo SVG and apply currentColor
```

**Process a folder:**
```
Clean all SVGs in /path/to/icons/ and create a sprite
```

**Extract specific element:**
```
Extract just the "g" letter from this logo
```

## Output Files

**Single file mode:**
- `filename-clean.svg` - Merged paths, no background
- `filename-currentcolor.svg` - With currentColor applied
- `filename-optimized.svg` - SVGO processed

**Batch folder mode:**
- `filename-cc.svg` - Each cleaned SVG
- `foldername-sprite-cc.svg` - Combined sprite with all icons

## Sprite Usage

Use the generated sprites in HTML:

```html
<svg>
  <use href="icons-sprite-cc.svg#logo"/>
</svg>
```

## Requirements

- Claude Desktop or Claude.ai with Skills enabled
- Optional: Node.js (for SVGO optimization)

## License

MIT License - See LICENSE file for details

## Contributing

Issues and pull requests welcome!

## Author

Created by Daniel Serrano for Claudeskills


---


## Contacto

- **Web:** https://claudeskills.es
- **Email:** master@claudeskills.es
- **GitHub:** https://github.com/claudeskills
- **LinkedIn:** https://www.linkedin.com/company/claudeskills/

---

_Archivo generado siguiendo el estándar [llms.txt](https://llmstxt.org/)_
