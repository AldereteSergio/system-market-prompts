# Stack Tecnológico: Lovable

## Stack Principal

### Frontend Framework
- **React 18.3.1**: Framework principal para la construcción de interfaces
- **TypeScript 5.5.3**: Tipado estático para mayor seguridad y desarrollo

### Build Tools
- **Vite 5.4.1**: Bundler y servidor de desarrollo ultra-rápido
- **SWC**: Compilador rápido para React (via @vitejs/plugin-react-swc)

### Estilos y Diseño
- **Tailwind CSS 3.4.11**: Framework CSS utility-first
- **Tailwind CSS Animate 1.0.7**: Animaciones CSS
- **Autoprefixer 10.4.20**: Auto-prefijos CSS
- **PostCSS 8.4.47**: Procesador CSS

### Componentes UI
- **Radix UI**: Componentes primitivos accesibles
  - @radix-ui/react-accordion, alert-dialog, avatar, checkbox, etc.
- **shadcn/ui**: Componentes de alto nivel construidos sobre Radix
- **Lucide React 0.462.0**: Iconografía moderna
- **Class Variance Authority 0.7.1**: Sistema de variantes de componentes

### Gestión de Estado
- **@tanstack/react-query 5.56.2**: Gestión de estado del servidor y cache
- **React Hook Form 7.53.0**: Gestión de formularios
- **Zod 3.23.8**: Validación de esquemas

### Navegación
- **React Router DOM 6.26.2**: Enrutamiento del lado del cliente

### Utilidades
- **clsx 2.1.1**: Utilidad para clases CSS condicionales
- **tailwind-merge 2.5.2**: Merge inteligente de clases Tailwind
- **date-fns 3.6.0**: Manipulación de fechas
- **cmdk 1.0.0**: Comando palette

### Características Especiales
- **Embla Carousel React 8.3.0**: Carruseles
- **React Day Picker 8.10.1**: Selector de fechas
- **React Resizable Panels 2.1.3**: Paneles redimensionables
- **Recharts 2.12.7**: Gráficos y visualizaciones
- **Sonner 1.5.0**: Notificaciones toast
- **Vaul 0.9.3**: Drawers y modales
- **Input OTP 1.2.4**: Inputs de código OTP

## Backend y Servicios

### Backend as a Service
- **Supabase**: Integración nativa para:
  - Autenticación
  - Gestión de base de datos
  - Funciones serverless
  - Storage de archivos

### Limitaciones Backend
- **No ejecución directa**: No puede ejecutar Python, Node.js, Ruby
- **Solo Supabase**: Backend limitado a la integración nativa

## Herramientas de Desarrollo

### Linting y Formateo
- **ESLint 9.9.0**: Linter de JavaScript/TypeScript
- **TypeScript ESLint 8.0.1**: Reglas específicas de TypeScript
- **ESLint Plugin React Hooks 5.1.0**: Reglas para React Hooks
- **ESLint Plugin React Refresh 0.4.9**: Reglas para React Refresh

### Herramientas Especializadas
- **Lovable Tagger 1.0.19**: Herramienta específica de Lovable
- **Next Themes 0.3.0**: Gestión de temas (claro/oscuro)

## Configuración del Proyecto

### Archivos de Configuración
- **tailwind.config.ts**: Configuración de Tailwind CSS
- **vite.config.ts**: Configuración de Vite
- **tsconfig.json**: Configuración de TypeScript
- **eslint.config.js**: Configuración de ESLint
- **postcss.config.js**: Configuración de PostCSS

### Estructura de Dependencias
- **Dependencias de producción**: 40+ paquetes
- **Dependencias de desarrollo**: 15+ paquetes
- **Total de paquetes**: ~55 paquetes

## Características Técnicas Específicas

### Optimizaciones
- **Code Splitting**: Implementado a través de Vite
- **Tree Shaking**: Eliminación automática de código no utilizado
- **Hot Module Replacement**: Recarga en caliente durante desarrollo

### Accesibilidad
- **Radix UI**: Componentes accesibles por defecto
- **ARIA**: Soporte completo para atributos ARIA
- **Navegación por teclado**: Soporte completo

### Rendimiento
- **SWC**: Compilación ultra-rápida
- **Vite**: Bundling optimizado
- **React Query**: Cache inteligente y sincronización

## Limitaciones Técnicas

### Frameworks No Soportados
- Angular
- Vue.js
- Svelte
- Next.js
- Nuxt.js

### Backend No Soportado
- Python (Flask, Django, FastAPI)
- Node.js (Express, Koa)
- Ruby (Rails, Sinatra)
- PHP
- Java
- C#

### Aplicaciones No Soportadas
- Aplicaciones móviles nativas
- Aplicaciones de escritorio
- Aplicaciones de servidor completo
