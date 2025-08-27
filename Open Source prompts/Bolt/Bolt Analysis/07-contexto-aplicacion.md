# Contexto de Aplicación: Bolt

## Tipo de Desarrollo

### Desarrollo Full-Stack en WebContainer
Bolt está diseñado específicamente para desarrollo de aplicaciones web completas dentro del entorno WebContainer, un runtime Node.js que se ejecuta en el navegador. Este contexto único determina las capacidades y limitaciones del asistente.

### Características del Entorno
- **Ejecución en Navegador**: Todo el código se ejecuta en el navegador del usuario
- **Sin Infraestructura Cloud**: No requiere VMs o servidores externos
- **Entorno Aislado**: Emulación de Linux con limitaciones específicas
- **Tiempo Real**: Desarrollo y ejecución inmediata

## Tecnologías Objetivo

### Stack Principal
1. **Frontend**:
   - React (componentes funcionales, hooks)
   - HTML5 Canvas (aplicaciones gráficas, juegos)
   - CSS (estilos y animaciones)
   - JavaScript/TypeScript

2. **Backend**:
   - Node.js (runtime principal)
   - Express.js (cuando se requiere)
   - APIs REST nativas

3. **Build Tools**:
   - Vite (preferido para desarrollo)
   - Servidores alternativos: servor, serve, http-server

4. **Base de Datos**:
   - Supabase (por defecto)
   - PostgreSQL (a través de Supabase)
   - Row Level Security (RLS)

### Lenguajes de Programación Soportados

#### JavaScript/Node.js
- **Runtime Completo**: Todas las APIs de Node.js disponibles
- **Módulos ES6+**: Sistema de módulos moderno
- **NPM**: Gestión completa de dependencias
- **APIs Web**: Fetch, Web APIs nativas

#### Python
- **Librería Estándar**: Solo módulos incluidos en Python
- **Sin Dependencias Externas**: No pip, no librerías de terceros
- **Scripts de Utilidad**: Procesamiento de datos, cálculos
- **Limitaciones**: No módulos que requieran binarios nativos

#### Otros Lenguajes
- **WebAssembly**: Soporte nativo para WASM
- **HTML/CSS**: Frontend completo
- **SQL**: Para operaciones de base de datos

## Tipos de Aplicaciones Soportadas

### 1. Aplicaciones Web Frontend
- **SPAs (Single Page Applications)**: React con Vite
- **Aplicaciones Interactivas**: Juegos, visualizaciones
- **Landing Pages**: Páginas de aterrizaje
- **Dashboards**: Paneles de control
- **Formularios**: Aplicaciones de entrada de datos

### 2. Aplicaciones Full-Stack
- **APIs REST**: Backend con Node.js/Express
- **Autenticación**: Supabase Auth
- **Base de Datos**: PostgreSQL con Supabase
- **Aplicaciones CRUD**: Operaciones completas de datos

### 3. Aplicaciones Especializadas
- **Juegos**: HTML5 Canvas, JavaScript
- **Visualizaciones**: Gráficos, animaciones
- **Herramientas de Utilidad**: Scripts de procesamiento
- **Prototipos**: Aplicaciones de demostración

## Casos de Uso Específicos

### Desarrollo Rápido de Prototipos
- **Creación Inmediata**: Desde cero hasta aplicación funcional
- **Iteración Rápida**: Cambios en tiempo real
- **Validación de Ideas**: Prueba de conceptos rápidamente

### Aplicaciones Educativas
- **Tutoriales Interactivos**: Código ejecutable
- **Demostraciones**: Ejemplos funcionales
- **Aprendizaje Práctico**: Experimentación directa

### Herramientas de Desarrollo
- **Scripts de Automatización**: Node.js y Python
- **Utilidades de Procesamiento**: Manipulación de datos
- **Herramientas de Conversión**: Formatos de archivo

### Aplicaciones de Demostración
- **Portfolios**: Proyectos de muestra
- **Presentaciones**: Aplicaciones interactivas
- **Pruebas de Concepto**: Validación de tecnologías

## Limitaciones de Aplicación

### No Soportado
1. **Aplicaciones Móviles Nativas**: iOS, Android
2. **Aplicaciones de Escritorio**: Electron, aplicaciones nativas
3. **Microservicios Complejos**: Arquitecturas distribuidas
4. **Aplicaciones de Alto Rendimiento**: Cálculos intensivos
5. **Aplicaciones con Binarios Nativos**: C++, compiladores

### Restricciones Técnicas
1. **Sin Git**: No control de versiones
2. **Sin Pip**: No librerías Python externas
3. **Sin Compiladores**: No C/C++, no binarios nativos
4. **Límites de Memoria**: Restricciones del navegador
5. **Límites de CPU**: Procesamiento limitado

## Integración y Servicios

### Servicios Nativos
1. **Supabase**: Base de datos, autenticación, storage
2. **Vite**: Servidor de desarrollo, build tool
3. **Node.js**: Runtime y APIs
4. **Web APIs**: APIs del navegador

### Servicios Externos
1. **APIs REST**: Llamadas HTTP a servicios externos
2. **CDNs**: Recursos estáticos
3. **Servicios Web**: APIs de terceros

## Flujo de Desarrollo Típico

### 1. Configuración Inicial
- Creación de `package.json`
- Instalación de dependencias
- Configuración de Vite
- Setup de Supabase (si se requiere)

### 2. Desarrollo Frontend
- Componentes React
- Estilos CSS
- Lógica de aplicación
- Integración con APIs

### 3. Desarrollo Backend (si se requiere)
- APIs REST
- Lógica de negocio
- Integración con base de datos
- Autenticación

### 4. Base de Datos
- Migraciones SQL
- Configuración de RLS
- Políticas de seguridad
- Datos de prueba

### 5. Despliegue y Pruebas
- Servidor de desarrollo
- Testing en tiempo real
- Optimización
- Documentación

## Características Especiales del Contexto

### Desarrollo Inmediato
- **Sin Configuración**: Entorno listo para usar
- **Ejecución Instantánea**: Código ejecutable inmediatamente
- **Feedback Rápido**: Cambios visibles al instante

### Entorno Colaborativo
- **Compartido**: Múltiples usuarios pueden ver el mismo entorno
- **Interactivo**: Desarrollo en tiempo real
- **Educativo**: Ideal para enseñanza y demostración

### Limitaciones de Producción
- **Escalabilidad Limitada**: Restricciones del navegador
- **Persistencia Temporal**: Datos no persistentes
- **Recursos Limitados**: Memoria y CPU restringidas

## Tecnologías Emergentes Soportadas

### WebAssembly
- **Aplicaciones de Alto Rendimiento**: Cálculos intensivos
- **Lenguajes Compilados**: C++, Rust (a través de WASM)
- **Optimización**: Mejor rendimiento que JavaScript

### APIs Web Modernas
- **Service Workers**: Funcionalidad offline
- **WebSockets**: Comunicación en tiempo real
- **Web APIs**: Acceso a hardware del dispositivo

### Frameworks Modernos
- **React Hooks**: Estado y efectos
- **TypeScript**: Tipado estático
- **CSS Grid/Flexbox**: Layouts modernos

## Consideraciones de Seguridad

### Entorno Aislado
- **Sandbox**: Ejecución segura en navegador
- **Sin Acceso al Sistema**: Limitaciones de seguridad
- **APIs Restringidas**: Solo APIs web permitidas

### Base de Datos Segura
- **RLS Obligatorio**: Seguridad a nivel de fila
- **Autenticación**: Supabase Auth
- **Políticas de Acceso**: Control granular de permisos

## Resumen del Contexto

### Fortalezas del Entorno
- **Desarrollo Rápido**: Configuración mínima
- **Ejecución Inmediata**: Sin despliegue
- **Colaboración**: Entorno compartido
- **Educación**: Ideal para aprendizaje

### Limitaciones del Entorno
- **Recursos Limitados**: Memoria y CPU
- **Sin Persistencia**: Datos temporales
- **Sin Binarios**: Restricciones técnicas
- **Escalabilidad**: Limitada para producción

### Casos de Uso Ideales
- **Prototipado Rápido**: Validación de ideas
- **Educación**: Aprendizaje práctico
- **Demostraciones**: Presentaciones interactivas
- **Herramientas de Utilidad**: Scripts y procesamiento
