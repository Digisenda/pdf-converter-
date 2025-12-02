# 🤖 DigiSenda AI - Conversor PDF a Word con OCR

<div align="center">

![DigiSenda AI](./assets/logo.png)

**Convierte PDFs a Word con OCR inteligente**

[![Desplegar en Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/TU-USUARIO/digisenda-pdf-converter)
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)

[Demo en Vivo](#) • [Reportar Bug](https://github.com/TU-USUARIO/digisenda-pdf-converter/issues) • [Solicitar Función](https://github.com/TU-USUARIO/digisenda-pdf-converter/issues)

</div>

---

## ✨ Características

- 🔍 **OCR Inteligente** - Extrae texto de documentos escaneados usando Tesseract.js
- ⚡ **Procesamiento Híbrido** - Detecta automáticamente si el PDF tiene texto digital o requiere OCR
- 🔒 **100% Privado** - Todo se procesa localmente en tu navegador, sin enviar datos a servidores
- 📱 **Responsive** - Funciona perfectamente en móviles, tablets y escritorio
- 🎨 **Interfaz Moderna** - Diseño dark con animaciones fluidas
- 📊 **Progreso en Tiempo Real** - Visualiza el avance de la conversión
- 💾 **Exportación a DOCX** - Genera archivos Word compatibles
- 🚫 **Sin Instalación** - Funciona directamente desde el navegador

## 🚀 Demo

Visita la aplicación en vivo: **[DigiSenda AI Converter](#)**

## 📸 Capturas de Pantalla

### Interfaz Principal
![Interfaz Principal](./assets/screenshot-1.png)

### Proceso de Conversión
![Conversión en Proceso](./assets/screenshot-2.png)

## 🛠️ Tecnologías

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **PDF Processing**: [PDF.js](https://mozilla.github.io/pdf.js/)
- **OCR Engine**: [Tesseract.js](https://tesseract.projectnaptha.com/)
- **DOCX Generation**: [html-docx-js](https://github.com/evidenceprime/html-docx-js)
- **File Saving**: [FileSaver.js](https://github.com/eligrey/FileSaver.js/)

## 📦 Instalación Local

### Prerrequisitos

Solo necesitas un navegador web moderno. No se requiere Node.js ni ninguna instalación adicional.

### Pasos

1. **Clona el repositorio**
```bash
git clone https://github.com/TU-USUARIO/digisenda-pdf-converter.git
cd digisenda-pdf-converter
```

2. **Abre el archivo HTML**
```bash
# En Windows
start index.html

# En macOS
open index.html

# En Linux
xdg-open index.html
```

O simplemente arrastra el archivo `index.html` a tu navegador.

## 🌐 Despliegue en Vercel

### Método 1: Usando el botón de Deploy

Haz clic en el botón "Deploy to Vercel" al inicio de este README.

### Método 2: Desde la CLI

```bash
# Instala Vercel CLI
npm i -g vercel

# Despliega
vercel --prod
```

### Método 3: Desde la Interfaz Web

1. Ve a [vercel.com](https://vercel.com)
2. Click en "New Project"
3. Importa este repositorio desde GitHub
4. Click en "Deploy"

¡Listo! Tu aplicación estará disponible en una URL de Vercel.

## 🎨 Personalización

### Cambiar el Logo

1. Reemplaza `./assets/logo.png` con tu logo (recomendado: 512x512px, formato PNG con fondo transparente)
2. También puedes actualizar `./assets/favicon.ico` y `./assets/favicon.svg`

### Cambiar Colores

Edita las variables CSS en `index.html`:

```css
:root {
  --primary: #6366f1;        /* Color principal */
  --secondary: #8b5cf6;      /* Color secundario */
  --background: #0f172a;     /* Fondo */
  --text: #f1f5f9;          /* Texto */
}
```

### Cambiar Idioma del OCR

En el archivo `index.html`, busca:

```javascript
const result = await Tesseract.recognize(canvas, "spa", {
```

Cambia `"spa"` por:
- `"eng"` para inglés
- `"fra"` para francés
- `"deu"` para alemán
- [Más idiomas disponibles](https://tesseract-ocr.github.io/tessdoc/Data-Files-in-different-versions.html)

## 📋 Estructura del Proyecto

```
digisenda-pdf-converter/
│
├── index.html              # Aplicación principal (HTML + CSS + JS)
├── README.md              # Este archivo
├── LICENSE                # Licencia MIT
├── vercel.json            # Configuración de Vercel
├── robots.txt             # SEO - Instrucciones para crawlers
├── sitemap.xml            # SEO - Mapa del sitio
│
└── assets/                # Recursos estáticos
    ├── logo.png           # Logo de DigiSenda AI (512x512px)
    ├── favicon.ico        # Favicon formato ICO
    ├── favicon.svg        # Favicon formato SVG
    ├── screenshot-1.png   # Captura de pantalla 1
    └── screenshot-2.png   # Captura de pantalla 2
```

## 🔧 Configuración Avanzada

### Límite de Tamaño de Archivo

Por defecto, el límite es 50MB. Para cambiarlo, edita esta línea en `index.html`:

```javascript
const maxSize = 50 * 1024 * 1024; // 50MB
```

### Calidad del OCR

Ajusta la escala del canvas para mejorar la calidad (consumirá más memoria):

```javascript
const viewport = pagina.getViewport({ scale: 2 }); // Cambiar 2 por 1.5 o 3
```

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Si deseas mejorar este proyecto:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Roadmap

- [ ] Soporte para múltiples archivos simultáneos
- [ ] Modo claro / oscuro
- [ ] Selección de páginas específicas
- [ ] Preview del PDF antes de convertir
- [ ] Conversión a otros formatos (TXT, RTF)
- [ ] Mejora de calidad de imagen antes del OCR
- [ ] Detección automática de idioma

## 🐛 Problemas Conocidos

- **PDFs muy grandes (>50MB)**: Pueden causar problemas de memoria en algunos navegadores
- **OCR en móviles**: Puede ser más lento debido a limitaciones de hardware
- **Tablas complejas**: El OCR puede no preservar perfectamente la estructura de tablas

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**DigiSenda AI**

- Website: [Tu sitio web](#)
- GitHub: [@TU-USUARIO](https://github.com/TU-USUARIO)
- Twitter: [@TU-USUARIO](#)

## 🙏 Agradecimientos

- [Mozilla PDF.js](https://mozilla.github.io/pdf.js/) - Renderizado de PDFs
- [Tesseract.js](https://tesseract.projectnaptha.com/) - Motor OCR
- [html-docx-js](https://github.com/evidenceprime/html-docx-js) - Generación de DOCX
- [FileSaver.js](https://github.com/eligrey/FileSaver.js/) - Descarga de archivos

---

<div align="center">

Hecho con ❤️ por **DigiSenda AI**

⭐ Si te gusta este proyecto, dale una estrella en GitHub ⭐

</div>
