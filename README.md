# IA para Periodistas Ninja 🥷📰

**[seguridades.org](https://seguridades.org)** | Un manual profesional y de código abierto para integrar Inteligencia Artificial en el periodismo de manera ética, segura y táctica.

[![Licencia](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-sa/4.0/)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.0-4FC08D?logo=vue.js&logoColor=white)](https://vuejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.0-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

---

## 🎯 Sobre el Proyecto

Frente al avance de la IA y los crecientes riesgos de vigilancia digital, los periodistas de investigación y defensores de DD.HH. necesitan herramientas prácticas y protocolos de seguridad (OPSEC) inquebrantables.

**"IA para Periodistas Ninja"** es una aplicación web interactiva de página única (SPA) diseñada para dotar a comunicadores con:

- Técnicas de ofuscación de identidad (Avatares y Clonación de Voz).
- Metodologías para Fact Checking forense.
- Herramientas OSINT gratuitas y de grado militar para investigar Leaks masivos.
- Protocolos Air-Gapped y tácticas de Seguridad Digital Extrema para proteger a fuentes confidenciales frente al rastreo de APIs comerciales (OpenAI, Anthropic).

## 🛠️ Stack Tecnológico

La web está construida priorizando la carga rápida, diseño moderno (Glassmorphism), y un empaquetado 100% estático listo para hospedarse gratuitamente.

- **Core:** [Vue 3](https://vuejs.org/) (Composition API)
- **Construcción:** [Vite](https://vitejs.dev/)
- **Estilos:** [Tailwind CSS v4](https://tailwindcss.com/) (diseño responsive, dark/light mode nativo)
- **Iconografía:** [Lucide Vue Next](https://lucide.dev/)

## 🚀 Despliegue Local (Desarrollo)

Si deseas clonar el proyecto para estudiarlo, modificarlo o traducirlo, los pasos son rápidos. Necesitas tener instalado **Node.js**:

1. **Clona el repositorio**

   ```bash
   git clone https://github.com/seguridades/ia-periodistas.git
   cd ia-periodistas
   ```

2. **Instala las dependencias**

   ```bash
   npm install
   ```

3. **Inicia el entorno de desarrollo**
   ```bash
   npm run dev
   ```
   _La app estará viva en `http://localhost:5173/` con la recarga en caliente ("hot-reload") activa._

## 📦 Producción y Hospedaje (Build)

Para lanzar el proyecto a la web (GitHub Pages, Vercel, Netlify):

1. **Compila la aplicación**

   ```bash
   npm run build
   ```

   _Esto generará una carpeta `dist/` con código super-comprimido HTML/CSS/JS._

2. **Opcional: Previsualiza la versión compilada**
   ```bash
   npm run preview
   ```
   _Verifica cómo se verá en el servidor real antes de subirlo._

## 🤝 Uso y Licencia

Este proyecto y todo su contenido editorial son impulsados por [seguridades.org](https://seguridades.org) con el fin de fortalecer el conocimiento libre.

Se distribuye bajo la licencia **Creative Commons Reconocimiento-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)**.

Eres totalmente libre de _clonar/forkear_ este repositorio, copiar su diseño o adaptar los textos de investigación para la realidad de tu propio país u organización, bajo el único requisito de dar la atribución adecuada al proyecto original.
