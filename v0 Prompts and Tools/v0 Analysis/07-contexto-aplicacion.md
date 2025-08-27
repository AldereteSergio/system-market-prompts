# Contexto de Aplicación: v0

## Tipo de Desarrollo

### Desarrollo Web Full-Stack
v0 está diseñado específicamente para el desarrollo de aplicaciones web completas, con un enfoque particular en:

#### Aplicaciones Next.js Modernas
- **SPAs (Single Page Applications)**: Aplicaciones de página única con navegación del lado cliente
- **SSR (Server-Side Rendering)**: Renderizado en servidor para SEO y performance
- **SSG (Static Site Generation)**: Generación estática para contenido predecible
- **ISR (Incremental Static Regeneration)**: Regeneración incremental para contenido dinámico

#### Características de Desarrollo
- **Desarrollo completo**: Desde prototipos hasta aplicaciones de producción
- **Integración nativa**: Conexión directa con servicios backend y APIs
- **Despliegue automático**: Integración con plataforma Vercel
- **Desarrollo colaborativo**: Herramientas para trabajo en equipo

### Limitaciones de Desarrollo

#### Tipos de Aplicaciones No Soportadas
- **Aplicaciones móviles nativas**: iOS, Android
- **Aplicaciones de escritorio**: Electron, Tauri
- **CLI tools**: Herramientas de línea de comandos
- **Microservicios**: Arquitectura de microservicios compleja

#### Frameworks No Soportados
- **Angular**: Framework de Google
- **Vue.js**: Framework progresivo (excepto en casos específicos)
- **Svelte**: Framework compilado (solo en CodeProject específico)
- **Ember**: Framework empresarial

## Tecnologías Objetivo

### Stack Tecnológico Principal

#### Framework de Desarrollo
- **Next.js App Router**: Framework principal
  - **App Router**: Sistema de enrutamiento basado en archivos
  - **Server Components**: Componentes renderizados en servidor
  - **Client Components**: Componentes interactivos del lado cliente
  - **Server Actions**: Operaciones del servidor integradas
  - **Route Handlers**: APIs y endpoints

#### Lenguaje de Programación
- **TypeScript**: Superset de JavaScript
  - **Tipado estático**: Configuración TypeScript optimizada
  - **Interfaces**: Definición de tipos y contratos
  - **Generics**: Tipos genéricos para reutilización
  - **Decoradores**: Metadatos y metaprogramación

#### Sistema de Estilos
- **Tailwind CSS v4**: Framework CSS utility-first
  - **Clases utilitarias**: Estilos inline y composables
  - **Sistema de diseño**: Tokens y variables CSS
  - **Responsive design**: Breakpoints móvil-first
  - **Dark mode**: Soporte para temas claro/oscuro

### Componentes UI
- **shadcn/ui**: Sistema de componentes de alto nivel
  - **Componentes accesibles**: ARIA y navegación por teclado
  - **Variantes configurables**: Props para personalización
  - **Tema consistente**: Sistema de diseño integrado
  - **Componentes base**: Button, Input, Card, Modal, etc.

### Gestión de Estado
- **React Hooks**: useState, useEffect, useContext
- **Server State**: Gestión de estado del servidor
- **Client State**: Estado local de componentes
- **Form State**: Gestión de formularios

## Casos de Uso Específicos

### Desarrollo de Aplicaciones Web

#### Landing Pages y Marketing
- **Páginas de aterrizaje**: Marketing y conversión
- **Sitios corporativos**: Información empresarial
- **Portfolios**: Presentación personal o empresarial
- **Páginas de producto**: Catálogos y detalles

#### Aplicaciones de Negocio
- **Dashboards**: Paneles de control y métricas
- **CRUD applications**: Gestión de datos
- **E-commerce**: Tiendas online completas
- **SaaS applications**: Software como servicio
- **Admin panels**: Paneles de administración

#### Aplicaciones Interactivas
- **Formularios complejos**: Entrada de datos avanzada
- **Visualizaciones**: Gráficos y charts interactivos
- **Carruseles**: Galerías de imágenes
- **Modales y drawers**: Interfaces modales
- **Real-time features**: Funcionalidades en tiempo real

### Desarrollo de Componentes

#### Componentes Reutilizables
- **UI Components**: Botones, inputs, cards, modals
- **Layout Components**: Headers, footers, sidebars, grids
- **Data Components**: Tables, lists, grids, charts
- **Interactive Components**: Modals, tooltips, dropdowns, sliders

#### Hooks Personalizados
- **State Management**: useLocalStorage, useDebounce, usePrevious
- **API Integration**: useApi, useQuery, useMutation
- **UI Interactions**: useClickOutside, useHover, useIntersection
- **Utilities**: useInterval, useTimeout, useAsync

## Flujo de Desarrollo

### Proceso de Creación

#### 1. Análisis y Planificación
- **Identificación de requerimientos**: Entender necesidades del usuario
- **Selección de subagentes**: Elegir herramientas apropiadas
- **Planificación de arquitectura**: Diseñar estructura del proyecto
- **Definición de integraciones**: Identificar servicios necesarios

#### 2. Implementación Iterativa
- **Configuración inicial**: Setup del proyecto y dependencias
- **Componentes base**: Crear componentes fundamentales
- **Páginas principales**: Implementar rutas y páginas
- **Funcionalidades**: Agregar lógica de negocio
- **Integraciones**: Conectar servicios externos

#### 3. Refinamiento y Optimización
- **Optimización visual**: Mejorar diseño y UX
- **Performance**: Optimizar rendimiento y carga
- **Accesibilidad**: Asegurar inclusividad
- **Testing**: Verificar funcionalidad y compatibilidad

### Herramientas de Desarrollo

#### Sistema de Subagentes
- **TodoManager**: Gestión de tareas complejas y multi-paso
- **InspectSite**: Captura de screenshots y verificación visual
- **SearchRepo**: Exploración inteligente del código base
- **ReadFile**: Lectura inteligente de archivos
- **SearchWeb**: Búsqueda web con fuentes de primera parte
- **FetchFromWeb**: Obtención de contenido web completo
- **GetOrRequestIntegration**: Gestión de integraciones

#### CodeProject
- **Generación completa**: Aplicaciones React/Next.js funcionales
- **Edición inteligente**: Modificación de archivos existentes
- **Gestión de assets**: Imágenes, audio, modelos 3D
- **Scripts ejecutables**: Código Python, Node.js, SQL

## Entorno de Desarrollo

### Configuración del Proyecto

#### Estructura de Archivos
```
app/
├── layout.tsx          # Layout principal
├── page.tsx           # Página principal
├── globals.css        # Estilos globales
└── [routes]/          # Rutas dinámicas

components/
├── ui/                # Componentes base
├── layout/            # Componentes de layout
└── features/          # Componentes específicos

lib/
├── utils.ts           # Utilidades
├── constants.ts       # Constantes
└── types.ts           # Tipos TypeScript

scripts/
├── python/            # Scripts Python
├── node/              # Scripts Node.js
└── sql/               # Scripts SQL
```

#### Archivos de Configuración
- **package.json**: Dependencias y scripts
- **tsconfig.json**: Configuración de TypeScript
- **next.config.mjs**: Configuración de Next.js
- **tailwind.config.ts**: Configuración de Tailwind CSS
- **eslint.config.js**: Reglas de linting

### Herramientas de Desarrollo

#### Linting y Formateo
- **ESLint**: Análisis estático de código
- **TypeScript**: Verificación de tipos
- **Prettier**: Formateo de código
- **Husky**: Git hooks

#### Testing
- **Jest**: Framework de testing
- **React Testing Library**: Testing de componentes
- **Playwright**: Testing end-to-end
- **Vitest**: Testing unitario rápido

## Integraciones Nativas

### Base de Datos
- **Supabase**: Backend as a Service completo
  - **PostgreSQL**: Base de datos relacional
  - **Autenticación**: Auth integrado
  - **Real-time**: Suscripciones en tiempo real
  - **Storage**: Almacenamiento de archivos
  - **Edge Functions**: Funciones serverless

- **Neon**: Base de datos PostgreSQL serverless
  - **Serverless**: Escalado automático
  - **Branching**: Ramas de base de datos
  - **Connection pooling**: Pool de conexiones optimizado

### Cache y Colas
- **Upstash for Redis**: Cache y colas de mensajes
  - **Redis**: Cache en memoria
  - **Queues**: Colas de procesamiento
  - **Rate limiting**: Limitación de velocidad

### Almacenamiento
- **Vercel Blob**: Almacenamiento de archivos
  - **Upload/Download**: Subida y descarga de archivos
  - **CDN**: Distribución de contenido
  - **Optimización**: Optimización automática de imágenes

### Servicios de IA
- **Groq**: Modelos de IA de alta velocidad
- **Grok (xAI)**: Modelos de IA avanzados
- **Fal**: Procesamiento de IA
- **Deep Infra**: Infraestructura de IA

## Consideraciones Específicas

### Performance
- **Code Splitting**: División automática de bundles
- **Lazy Loading**: Carga diferida de componentes
- **Image Optimization**: Optimización de imágenes
- **Bundle Analysis**: Análisis de tamaño de bundles
- **Edge Caching**: Cache en edge para mejor performance

### Accesibilidad
- **ARIA Attributes**: Atributos de accesibilidad
- **Keyboard Navigation**: Navegación por teclado
- **Screen Reader Support**: Soporte para lectores de pantalla
- **Color Contrast**: Contraste de colores adecuado
- **Semantic HTML**: HTML semántico apropiado

### SEO
- **Meta Tags**: Etiquetas meta apropiadas
- **Structured Data**: Datos estructurados
- **Performance Metrics**: Métricas de rendimiento
- **Sitemap Generation**: Generación automática de sitemaps
- **Robots.txt**: Configuración de robots

### Seguridad
- **Input Validation**: Validación de entrada
- **XSS Prevention**: Prevención de XSS
- **CSRF Protection**: Protección CSRF
- **Secure Headers**: Headers de seguridad
- **Environment Variables**: Gestión segura de variables

## Ecosistema Vercel

### Plataforma de Despliegue
- **Vercel Platform**: Despliegue automático
- **Edge Functions**: Funciones serverless
- **Edge Runtime**: Runtime optimizado
- **Analytics**: Métricas de aplicación
- **Monitoring**: Monitoreo en tiempo real

### Herramientas de Desarrollo
- **Vercel CLI**: Herramienta de línea de comandos
- **Vercel Dashboard**: Panel de control
- **Vercel Toolbar**: Herramientas de desarrollo
- **Vercel Marketplace**: Integraciones de terceros

### Integración Continua
- **Git Integration**: Despliegue automático desde Git
- **Preview Deployments**: Despliegues de preview
- **Environment Management**: Gestión de entornos
- **Team Collaboration**: Colaboración en equipo

## Casos de Uso Avanzados

### Aplicaciones Empresariales
- **Dashboards ejecutivos**: Métricas y KPIs
- **Sistemas de gestión**: CRM, ERP, HR
- **Aplicaciones de colaboración**: Chat, video, documentos
- **Portales de cliente**: Self-service, facturación

### Aplicaciones de E-commerce
- **Tiendas online**: Catálogos, carritos, checkout
- **Marketplaces**: Múltiples vendedores
- **Sistemas de pago**: Integración con gateways
- **Gestión de inventario**: Stock, pedidos, envíos

### Aplicaciones de Contenido
- **CMS**: Gestión de contenido
- **Blogs**: Publicación de artículos
- **Portfolios**: Galerías de trabajo
- **Sitios de noticias**: Contenido dinámico

### Aplicaciones de IA
- **Chatbots**: Asistentes conversacionales
- **Generación de contenido**: Texto, imágenes, código
- **Análisis de datos**: Visualizaciones y insights
- **Automatización**: Workflows inteligentes
