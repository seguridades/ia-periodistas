# **ESPECIFICACIONES TÉCNICAS**

## IA para Periodistas: Manual y Documentación Interactiva

**Versión:** 0.1

**Estado:** Documento de diseño

**Stack:** Vue.js 3 \+ Tailwind CSS

## Propósito del sistema

Desarrollar una aplicación web interactiva y modular que sirva como guía práctica para periodistas en el uso ético y seguro de Inteligencia Artificial. El sistema prioriza la **seguridad digital** y la **protección de fuentes** mientras enseña flujos de trabajo con herramientas de vanguardia.

## Arquitectura de Software

* **Frontend:** Vue.js 3 (Composition API) para una interfaz reactiva y modular.  
* **Estilos:** Tailwind CSS utilizando las variables HSL proporcionadas para soporte nativo de **Dark/Light Mode**.  
* **Navegación:** Vue Router para una experiencia SPA (Single Page Application) fluida.

## Pilares de Contenido (Estructura de Datos)

El sistema se organiza en cuatro módulos críticos, cada uno con su propia lógica de visualización:

| Módulo | Enfoque Principal | Herramientas Referencia |
| :---- | :---- | :---- |
| **Avatares y Guiones** | Generación de video y narrativa. | Synthesia, D-ID, GPT-4. |
| **Fact Checking** | Verificación automatizada de hechos. | Herramientas de análisis de fuentes. |
| **Investigación** | Análisis de datos masivos y OSINT. | Metodologías estructuradas. |
| **Seguridad Digital** | Protocolo de protección y anonimato. | Cifrado, VPNs, OFAC check. |

## Componentes Principales

### 1 Hero Section Personalizada

Un componente de impacto visual que utiliza un gradiente tecnológico (Azul/Verde) con una imagen central que simboliza la intersección entre el periodismo tradicional y la IA.

### 2 Security Alert Component (Crítico)

Componente de alta prioridad visual para advertencias sobre:

* Manejo de datos sensibles en modelos de lenguaje.  
* Riesgos de alucinaciones en IA.  
* Protocolos de anonimización obligatorios antes de subir documentos.

### 3 Interactive Workflow Map

Un componente que renderiza de forma dinámica los pasos para realizar *Fact Checking* o *Investigación OSINT*, permitiendo al usuario marcar progreso localmente mediante localStorage.

## Protocolo de Seguridad Digital Integrado

A diferencia de un manual estático, esta aplicación incluye capas de seguridad activa en su narrativa:

1. **Capa de Privacidad:** Recordatorios contextuales de "No compartir nombres reales de fuentes en prompts".  
2. **Validación de Herramientas:** Clasificación de herramientas de IA por nivel de privacidad (Verde: Segura, Amarillo: Usar con precaución, Rojo: Riesgo de fuga de datos).  
3. **Guía de Anonimización:** Tutoriales integrados para limpiar metadatos de archivos antes del procesamiento con IA.

## Requisitos No Funcionales

* **Mobile First:** Optimización total para lectura en campo desde dispositivos móviles.  
* **Accesibilidad (WCAG AA):** Garantizar que el contraste entre el azul tecnológico y los textos cumpla con los estándares de legibilidad.  
* **Performance:** Carga ultrarrápida mediante Vite, minimizando el peso de los componentes de video o avatares de ejemplo.

## Escalabilidad Futura

* **API de Búsqueda:** Implementar una búsqueda global sobre el contenido del manual.  
* **Generador de Prompts:** Una herramienta interna para ayudar a los periodistas a estructurar prompts seguros.  
* **Certificación:** Un sistema de "badges" que valide que el periodista ha leído y comprendido los protocolos de seguridad.

