﻿# Portfolio

Sitio web de portfolio personal creado con **HTML puro, CSS y Tailwind CSS** (sin JavaScript).

## Requisitos

- Node.js (versión 14 o superior)
- npm

## Instalación

```bash
npm install
```

## Scripts disponibles

### Modo desarrollo (auto-recompilación)

Para desarrollar y que Tailwind se compile automáticamente al hacer cambios:

```bash
npm run dev
```

Este comando mantendrá Tailwind ejecutándose en modo "watch", recompilando automáticamente el CSS cada vez que guardes
cambios en el HTML o archivos CSS.

### Compilación para producción

Para compilar y minificar el CSS para producción:

```bash
npm run build
```

## Características

- ✅ **100% HTML y CSS puro** - Sin JavaScript
- ✅ **Modo oscuro automático** - Se activa según la preferencia del sistema operativo
- ✅ **Tailwind CSS v3** - Framework CSS de utilidades
- ✅ **Responsive design** - Adaptado a todos los dispositivos
- ✅ **Efectos visuales** - Backdrop blur, transiciones y animaciones CSS

## Estructura del proyecto

```
portfolio/
├── index.html              # Página principal
├── src/
│   └── tailwind.css       # Archivo fuente de Tailwind
├── public/
│   ├── build/
│   │   └── tailwind.css   # CSS compilado (generado automáticamente)
│   ├── docs/              # Documentos PDF
│   ├── favicons/          # Iconos SVG
│   └── imgs/              # Imágenes
├── tailwind.config.js     # Configuración de Tailwind
└── package.json           # Dependencias y scripts
```

## Uso de Tailwind CSS

El proyecto usa Tailwind CSS v3 con modo oscuro automático basado en `@media (prefers-color-scheme: dark)`.

Puedes usar todas las clases de utilidad de Tailwind directamente en el HTML.

Ejemplo:

```html

<header class="fixed top-0 z-10 w-full bg-zinc-900/80 backdrop-blur-md">
    <nav class="dark:text-white">
        <!-- El texto será blanco automáticamente en modo oscuro -->
    </nav>
</header>
```

El modo oscuro se activará automáticamente cuando tu sistema operativo esté en modo oscuro, **sin necesidad de
JavaScript**.

## Notas

- El CSS compilado se genera en `public/build/tailwind.css`
- No edites directamente el archivo `public/build/tailwind.css`, ya que se sobrescribirá
- Todos los cambios de estilos deben hacerse usando clases de Tailwind en el HTML
- El modo oscuro usa `darkMode: 'media'` en Tailwind, lo que permite detección automática sin JS

