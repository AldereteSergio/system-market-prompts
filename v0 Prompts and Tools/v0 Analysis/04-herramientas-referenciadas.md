# Herramientas Referenciadas: v0

## Sistema de Subagentes

### TodoManager
**Descripción**: Gestión de tareas complejas y multi-paso para proyectos que requieren múltiples sistemas independientes
**Uso**: Proyectos con múltiples sistemas que necesitan trabajar juntos
**Parámetros**:
- `action`: "set_tasks", "move_to_task", "add_task", "read_list", "generate_plan", "mark_all_done"
- `tasks`: Array de tareas milestone-level (3-7 tareas máximo)
- `task`: Descripción de tarea individual
- `moveToTask`: Nombre exacto de la tarea a enfocar
**Características**: 
- Tareas a nivel de milestone, no micro-pasos
- Una página = una tarea
- UI antes que backend
- Máximo 10 tareas totales
- NO tareas vagas como "Polish", "Test", "Finalize"

### InspectSite
**Descripción**: Captura screenshots para verificar bugs visuales o capturar diseños de referencia
**Uso**: Verificación de bugs visuales, recreación de diseños web
**Parámetros**:
- `urls`: Array de URLs a capturar (sitios web o localhost)
**Características**:
- Convierte localhost a URLs de preview
- Optimiza tamaños de screenshot
- Soporta múltiples URLs
- URLs específicas de página recomendadas

### SearchRepo
**Descripción**: Exploración inteligente del código base usando múltiples estrategias de búsqueda
**Uso**: Antes de cualquier modificación de código, exploración de arquitectura
**Parámetros**:
- `query`: Descripción de lo que se busca en el código base
**Características**:
- Descubrimiento de archivos y análisis de contenido
- Búsqueda de patrones con regex
- Exploración de directorios y estructura
- Selección inteligente de archivos
- Respuestas contextuales combinando resultados

### ReadFile
**Descripción**: Lectura inteligente de archivos - archivos completos cuando son pequeños, chunks relevantes cuando son grandes
**Uso**: Antes de editar, entender implementación, encontrar código específico
**Parámetros**:
- `filePath`: Ruta absoluta del archivo
- `query`: Qué se busca en el archivo (requerido para archivos grandes)
**Características**:
- Archivos pequeños (≤500 líneas): contenido completo
- Archivos grandes (>500 líneas): chunks relevantes basados en query
- Archivos binarios: manejo apropiado de imágenes y blobs
- Query específico para mejores resultados

### SearchWeb
**Descripción**: Búsqueda web inteligente usando fuentes de alta calidad, priorizando documentación de primera parte
**Uso**: Documentación tecnológica, mejores prácticas actuales, información de productos Vercel
**Parámetros**:
- `query`: Consulta de búsqueda específica y dirigida
- `isFirstParty`: Boolean para habilitar búsqueda de documentación de primera parte
**Características**:
- Prioriza documentación de primera parte para ecosistema Vercel
- Múltiples búsquedas dirigidas para cobertura completa
- Versiones específicas y nombres de productos para precisión
- Dominios soportados: nextjs.org, vercel.com, sdk.vercel.ai, etc.

### FetchFromWeb
**Descripción**: Obtiene contenido completo de texto de páginas web cuando se tienen URLs específicas
**Uso**: URLs conocidas, análisis profundo de contenido, documentación externa
**Parámetros**:
- `urls`: Array de URLs para obtener contenido completo
**Características**:
- Contenido de texto completo limpio y parseado
- Metadatos: título, autor, fecha, favicon, imágenes
- Múltiples URLs procesadas en una sola solicitud
- vs SearchWeb: usar cuando se conocen URLs específicas

### GetOrRequestIntegration
**Descripción**: Verifica estado de integración, obtiene variables de entorno y esquemas de base de datos en vivo
**Uso**: Antes de construir features de integración, debugging de problemas de integración
**Parámetros**:
- `names`: Array de nombres de integración específicos (opcional)
**Características**:
- Estado de integración y configuración
- Variables de entorno disponibles y requerimientos faltantes
- Esquemas de base de datos en tiempo real para SQL
- Ejemplos de código cuando están disponibles
- Detiene ejecución y solicita configuración para integraciones faltantes

## Herramientas de CodeProject

### CodeProject
**Descripción**: Bloque para agrupar archivos y renderizar aplicaciones React y Next.js full-stack
**Uso**: Generación de aplicaciones React/Next.js completas
**Parámetros**:
- `id`: Identificador único del proyecto
- `taskNameActive`: 2-5 palabras describiendo la tarea en ejecución
- `taskNameComplete`: 2-5 palabras describiendo la tarea completada
**Características**:
- Debe agrupar bloques de código React
- Sintaxis: ```lang file="path/to/file"
- Preferir kebab-case para nombres de archivos
- Solo escribir archivos relevantes a la solicitud

### Edición de Archivos
**Descripción**: Modificación de archivos existentes con indicadores de cambio
**Uso**: Editar archivos existentes sin reescribir completamente
**Sintaxis**:
```
// ... existing code ...
// <CHANGE> descripción del cambio
// código modificado
// ... existing code ...
```
**Características**:
- Sistema fusiona código original con ediciones especificadas
- Solo escribir partes que necesitan cambiar
- Incluir comentario de cambio para claridad
- Mantener capacidad de edición rápida

### Delete File
**Descripción**: Elimina archivos del proyecto
**Uso**: Remover archivos no necesarios
**Sintaxis**: `<Delete File file="path/to/file" />`
**Características**:
- No soporta eliminación múltiple
- Un DeleteFile por archivo
- Ruta específica requerida

### Move File
**Descripción**: Renombra o mueve archivos en el proyecto
**Uso**: Reorganizar estructura de archivos
**Sintaxis**: `<Move File from="path/to/file" to="path/to/new-file" />`
**Características**:
- `from`: Ruta original del archivo
- `to`: Nueva ruta del archivo
- v0 debe recordar arreglar imports después del movimiento
- NO reescribe el archivo después del movimiento

### Import ReadOnlyFile
**Descripción**: Importa archivos de solo lectura al proyecto
**Uso**: Agregar archivos de contexto de usuario al proyecto
**Sintaxis**: `<Import ReadOnlyFile from="user_read_only_context/path/to/file" to="path/to/new-file" />`
**Características**:
- `from`: Ruta original del archivo de solo lectura
- `to`: Nueva ruta en el proyecto
- Útil para archivos de contexto del usuario

## Svelte Code Project

### Svelte Code Project
**Descripción**: Generación de aplicaciones Svelte usando Svelte 5 APIs
**Uso**: Aplicaciones Svelte modernas con runes
**Parámetros**:
- `lang="svelte"`: Especifica que es un proyecto Svelte
- `id`: Identificador único del proyecto
**Características**:
- Usar Svelte 5 APIs y runes
- `$state` para estado, `$derived` para derivaciones
- `$effect` para efectos secundarios
- `$props` para props de componentes
- Eventos sin colones: `onclick` en lugar de `on:click`
- Componente raíz: App.svelte por defecto

## Scripts Ejecutables

### Python Scripts
**Descripción**: Ejecución de código Python dentro de Code Projects
**Ubicación**: `/scripts` folder
**Características**:
- Usar librerías populares: NumPy, Matplotlib, Pillow
- `print()` para output
- Implementaciones de funciones puras cuando sea posible
- NO copiar attachments con datos al proyecto
- Leer directamente desde attachment

### Node.js Scripts
**Descripción**: Ejecución de código Node.js dentro de Code Projects
**Ubicación**: `/scripts` folder
**Características**:
- Sintaxis ES6+ y `fetch` nativo
- Siempre usar `import`, nunca `require`
- Usar `sharp` para procesamiento de imágenes
- `console.log()` para output

### SQL Scripts
**Descripción**: Ejecución de scripts SQL para bases de datos
**Ubicación**: `/scripts` folder
**Características**:
- Verificar que las tablas existen antes de actualizar
- Dividir scripts en múltiples archivos para mejor organización
- NO reescribir scripts SQL ya ejecutados
- Solo agregar nuevos scripts si se necesita modificación

## Herramientas de Assets

### Placeholder Images
**Descripción**: Generación de imágenes placeholder para desarrollo
**Sintaxis**: `/placeholder.svg?height={height}&width={width}&query={query}`
**Características**:
- `height` y `width`: Dimensiones en píxeles
- `query`: Descripción opcional de la imagen
- Query debe estar hardcodeado en la URL
- URL completa sin concatenación de strings

### V0LoadingImage
**Descripción**: Generación de imágenes usando IA
**Sintaxis**: `<V0LoadingImage />`
**Características**:
- Genera imágenes basadas en query
- Coloca imagen en ruta especificada
- Útil para imágenes que no existen

### Formatos de Archivo Soportados
**Descripción**: Múltiples formatos de archivos multimedia
**Formatos**:
- **Imágenes**: PNG, JPG, SVG, WebP
- **Audio**: MP3, WAV, OGG
- **3D Models**: GLB, GLTF
- **Videos**: MP4, WebM

## Herramientas de Diagramas y Matemáticas

### Mermaid
**Descripción**: Generación de diagramas y flowcharts
**Uso**: Visualización de conceptos complejos, procesos, arquitectura
**Sintaxis**: ```mermaid title="Example Flowchart" type="diagram"```
**Características**:
- Usar comillas alrededor de nombres de nodos
- Códigos UTF-8 para caracteres especiales
- Sin `&` en códigos HTML

### LaTeX
**Descripción**: Renderizado de ecuaciones matemáticas
**Uso**: Fórmulas matemáticas y ecuaciones
**Sintaxis**: $$ ecuación $$
**Características**:
- Siempre usar doble dólar ($$)
- NO usar dólar simple para matemáticas inline
- Mantener doble dólar incluso con negrita

## Herramientas de Integración

### AI SDK
**Descripción**: Integración estandarizada de modelos de IA
**Uso**: Aplicaciones de IA usando integraciones soportadas
**Características**:
- Usar 'ai' y '@ai-sdk'
- NUNCA usar runtime = 'edge' en API routes
- Evitar librerías como 'langchain' o 'openai-edge'
- JavaScript en lugar de Python para IA

### Supabase Integration
**Descripción**: Integración nativa con Supabase
**Uso**: Base de datos, autenticación, funciones serverless
**Características**:
- `createClient` para cliente del lado cliente
- `createServerClient` para servidor
- Patrón singleton para clientes
- Configuración automática desde UI de v0
- `emailRedirectTo` con variables de entorno

### Neon Integration
**Descripción**: Integración con base de datos Neon
**Uso**: Base de datos PostgreSQL serverless
**Características**:
- Usar `@neondatabase/serverless`
- Función `neon()` para crear cliente SQL
- NUNCA usar `@vercel/postgres`

### Upstash Integration
**Descripción**: Integración con Redis y colas
**Uso**: Cache, colas de mensajes, rate limiting
**Variables de entorno**:
- `KV_REST_API_URL`
- `KV_REST_API_TOKEN`

### AI Service Integrations
**Descripción**: Integración con servicios de IA
**Servicios**:
- **Grok (xAI)**: `XAI_API_KEY`
- **Groq**: `GROQ_API_KEY`
- **Fal**: `FAL_KEY`, usar `@fal-ai/serverless`
- **Deep Infra**: `DEEPINFRA_API_KEY`

## Herramientas de UI y UX

### Design System Guidelines
**Descripción**: Directrices específicas para diseño de interfaces
**Características**:
- **Colores**: 3-5 colores total máximo
- **Tipografía**: Máximo 2 familias de fuentes
- **Layout**: Mobile-first design
- **Whitespace**: Mínimo 16px entre secciones
- **Flexbox**: Preferido sobre CSS Grid para la mayoría de layouts

### Google Fonts
**Descripción**: Combinaciones recomendadas de fuentes
**Categorías**:
- **Modern/Tech**: Space Grotesk + DM Sans, IBM Plex Sans
- **Editorial/Content**: Playfair Display + Source Sans Pro
- **Bold/Impact**: Montserrat + Open Sans
- **Elegant/Premium**: Playfair Display + DM Sans Light
- **Clean/Minimal**: DM Sans + DM Sans
- **Corporate/Professional**: Work Sans + Open Sans

### Tailwind Implementation
**Descripción**: Patrones específicos de Tailwind CSS
**Características**:
- Usar `gap-*` sobre `space-*` para espaciado
- Prefijos responsivos: `md:`, `lg:`
- Clases semánticas: `items-center`, `justify-between`
- Evitar valores arbitrarios: no `w-[347px]`
- NO usar `!important` o propiedades arbitrarias

## Herramientas de Configuración

### Environment Variables
**Descripción**: Gestión de variables de entorno
**Características**:
- `NEXT_PUBLIC_` para variables accesibles en cliente
- Variables solo en servidor para Server Actions y Route Handlers
- Configuración automática para integraciones
- UI para agregar variables faltantes

### Project Settings
**Descripción**: Configuración del proyecto en v0.dev
**Características**:
- Variables de entorno
- Integraciones
- Instrucciones personalizadas
- Fuentes de información

### Deployment Tools
**Descripción**: Herramientas de despliegue integradas
**Características**:
- Botón "Download Code" para instalación
- Botón GitHub para push a repositorio
- Botón "Deploy" para despliegue en Vercel
- CLI de shadcn para instalación y configuración
