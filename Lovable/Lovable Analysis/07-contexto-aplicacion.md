# Contexto de Aplicación: Lovable

## Tipo de Desarrollo

### Desarrollo Frontend Especializado
Lovable está diseñado específicamente para el desarrollo de aplicaciones web frontend, con un enfoque particular en:

#### Aplicaciones React Modernas
- **SPAs (Single Page Applications)**: Aplicaciones de página única
- **Aplicaciones web responsivas**: Diseño adaptativo para múltiples dispositivos
- **Interfaces de usuario modernas**: Componentes interactivos y atractivos
- **Aplicaciones con estado complejo**: Gestión de estado del cliente

#### Características de Desarrollo
- **Desarrollo rápido**: Iteración rápida con vista previa en tiempo real
- **Prototipado visual**: Enfoque en la experiencia visual inmediata
- **Desarrollo conversacional**: Interacción natural con el asistente
- **Desarrollo colaborativo**: Chat en tiempo real con el usuario

### Limitaciones de Desarrollo

#### Tipos de Aplicaciones No Soportadas
- **Aplicaciones móviles nativas**: iOS, Android
- **Aplicaciones de escritorio**: Electron, Tauri
- **Aplicaciones de servidor completo**: Backend tradicional
- **Aplicaciones híbridas**: React Native, Flutter

#### Frameworks No Soportados
- **Angular**: Framework de Google
- **Vue.js**: Framework progresivo
- **Svelte**: Framework compilado
- **Next.js**: Framework de React con SSR
- **Nuxt.js**: Framework de Vue

## Tecnologías Objetivo

### Stack Tecnológico Principal

#### Frontend Framework
- **React 18.3.1**: Framework principal
  - Hooks modernos (useState, useEffect, useContext)
  - Componentes funcionales
  - JSX para templating
  - Virtual DOM para rendimiento

#### Lenguaje de Programación
- **TypeScript 5.5.3**: Superset de JavaScript
  - Tipado estático
  - Interfaces y tipos
  - Generics
  - Decoradores

#### Build System
- **Vite 5.4.1**: Bundler moderno
  - Hot Module Replacement (HMR)
  - Code splitting automático
  - Optimización de producción
  - Plugin system extensible

### Sistema de Estilos

#### CSS Framework
- **Tailwind CSS 3.4.11**: Framework utility-first
  - Clases utilitarias
  - Sistema de diseño configurable
  - Responsive design
  - Dark mode support

#### Componentes UI
- **Radix UI**: Componentes primitivos
  - Accesibilidad por defecto
  - Componentes headless
  - Customización completa
- **shadcn/ui**: Componentes de alto nivel
  - Construidos sobre Radix
  - Variantes configurables
  - Sistema de diseño integrado

### Gestión de Estado

#### Estado del Servidor
- **@tanstack/react-query 5.56.2**: Gestión de estado remoto
  - Cache inteligente
  - Sincronización automática
  - Optimistic updates
  - Background refetching

#### Estado Local
- **React Hook Form 7.53.0**: Gestión de formularios
  - Validación integrada
  - Performance optimizada
  - Integración con Zod
- **useState/useContext**: Estado local simple

### Backend Integration

#### Backend as a Service
- **Supabase**: Plataforma backend completa
  - Base de datos PostgreSQL
  - Autenticación integrada
  - Funciones serverless
  - Storage de archivos
  - Real-time subscriptions

#### Limitaciones Backend
- **No ejecución directa**: No puede ejecutar código backend tradicional
- **Solo Supabase**: Integración limitada a esta plataforma
- **Funciones serverless**: Solo a través de Supabase Edge Functions

## Casos de Uso Específicos

### Desarrollo de Aplicaciones Web

#### Landing Pages
- **Páginas de aterrizaje**: Marketing y conversión
- **Portfolios**: Presentación personal o empresarial
- **Sitios corporativos**: Información empresarial
- **Páginas de producto**: Catálogos y detalles

#### Aplicaciones de Negocio
- **Dashboards**: Paneles de control y métricas
- **CRUD applications**: Gestión de datos
- **E-commerce**: Tiendas online
- **SaaS applications**: Software como servicio

#### Aplicaciones Interactivas
- **Formularios complejos**: Entrada de datos
- **Visualizaciones**: Gráficos y charts
- **Carruseles**: Galerías de imágenes
- **Modales y drawers**: Interfaces modales

### Desarrollo de Componentes

#### Componentes Reutilizables
- **UI Components**: Botones, inputs, cards
- **Layout Components**: Headers, footers, sidebars
- **Data Components**: Tables, lists, grids
- **Interactive Components**: Modals, tooltips, dropdowns

#### Hooks Personalizados
- **State Management**: useLocalStorage, useDebounce
- **API Integration**: useApi, useQuery
- **UI Interactions**: useClickOutside, useHover
- **Utilities**: usePrevious, useInterval

## Flujo de Desarrollo

### Proceso de Creación

#### 1. Planificación Conversacional
- **Discusión inicial**: Entender requerimientos
- **Exploración de diseño**: Identificar inspiración visual
- **Definición de features**: Listar funcionalidades
- **Selección de tecnologías**: Elegir stack apropiado

#### 2. Implementación Iterativa
- **Sistema de diseño**: Configurar Tailwind y tokens
- **Componentes base**: Crear componentes fundamentales
- **Páginas principales**: Implementar rutas principales
- **Funcionalidades**: Agregar lógica de negocio

#### 3. Refinamiento Continuo
- **Optimización visual**: Mejorar diseño y UX
- **Performance**: Optimizar rendimiento
- **Accesibilidad**: Asegurar inclusividad
- **Testing**: Verificar funcionalidad

### Herramientas de Desarrollo

#### Herramientas de Archivos
- **lov-write**: Crear archivos nuevos
- **lov-line-replace**: Editar archivos existentes
- **lov-view**: Leer contenido de archivos
- **lov-rename**: Renombrar archivos
- **lov-delete**: Eliminar archivos

#### Herramientas de Búsqueda
- **lov-search-files**: Búsqueda en código
- **web_search**: Búsqueda web
- **lov-fetch-website**: Obtener contenido web

#### Herramientas de Assets
- **generate_image**: Crear imágenes con IA
- **edit_image**: Editar imágenes existentes
- **lov-download-to-repo**: Descargar recursos

## Entorno de Desarrollo

### Configuración del Proyecto

#### Estructura de Archivos
```
src/
├── components/     # Componentes reutilizables
├── pages/         # Páginas de la aplicación
├── hooks/         # Hooks personalizados
├── lib/           # Utilidades y configuraciones
├── assets/        # Imágenes y recursos
└── styles/        # Estilos globales
```

#### Archivos de Configuración
- **tailwind.config.ts**: Configuración de Tailwind
- **vite.config.ts**: Configuración de Vite
- **tsconfig.json**: Configuración de TypeScript
- **eslint.config.js**: Configuración de linting

### Herramientas de Desarrollo

#### Linting y Formateo
- **ESLint**: Análisis estático de código
- **TypeScript**: Verificación de tipos
- **Prettier**: Formateo de código

#### Optimización
- **Vite**: Bundling optimizado
- **SWC**: Compilación rápida
- **Tree Shaking**: Eliminación de código no usado

## Consideraciones Específicas

### Performance
- **Code Splitting**: División automática de bundles
- **Lazy Loading**: Carga diferida de componentes
- **Image Optimization**: Optimización de imágenes
- **Bundle Analysis**: Análisis de tamaño de bundles

### Accesibilidad
- **ARIA Attributes**: Atributos de accesibilidad
- **Keyboard Navigation**: Navegación por teclado
- **Screen Reader Support**: Soporte para lectores de pantalla
- **Color Contrast**: Contraste de colores adecuado

### SEO
- **Meta Tags**: Etiquetas meta apropiadas
- **Semantic HTML**: HTML semántico
- **Structured Data**: Datos estructurados
- **Performance Metrics**: Métricas de rendimiento

### Seguridad
- **Input Validation**: Validación de entrada
- **XSS Prevention**: Prevención de XSS
- **CSRF Protection**: Protección CSRF
- **Secure Headers**: Headers de seguridad
