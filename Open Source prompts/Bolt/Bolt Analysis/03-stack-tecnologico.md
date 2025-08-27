# Stack Tecnológico: Bolt

## Entorno de Ejecución Principal

### WebContainer
- **Runtime**: Node.js en navegador
- **Sistema Operativo**: Emulación de Linux
- **Shell**: zsh emulado
- **Limitación Principal**: No ejecuta binarios nativos

### Lenguajes de Programación Soportados

#### JavaScript/Node.js
- **Runtime**: Node.js completo
- **Módulos**: Sistema de módulos ES6+
- **NPM**: Gestión de dependencias
- **APIs**: Todas las APIs de Node.js disponibles

#### Python
- **Versión**: python y python3 disponibles
- **Limitación Crítica**: Solo librería estándar
- **Restricciones**:
  - NO pip disponible
  - NO librerías de terceros
  - NO módulos que requieran dependencias del sistema
  - NO curses u otros módulos nativos

#### Otros Lenguajes
- **WebAssembly**: Soporte nativo
- **HTML/CSS/JavaScript**: Frontend completo
- **C/C++**: NO soportado (sin compiladores)

## Herramientas de Desarrollo

### Servidores Web
- **Vite**: Preferido para desarrollo
- **servor**: Servidor web ligero
- **serve**: Servidor estático
- **http-server**: Servidor HTTP básico
- **Node.js APIs**: Servidores personalizados

### Gestión de Paquetes
- **NPM**: Gestión principal de dependencias
- **npx**: Ejecución de paquetes con `--yes` flag
- **package.json**: Configuración de proyectos

### Comandos Shell Disponibles

#### Operaciones de Archivos
- `cat`: Mostrar contenido de archivos
- `cp`: Copiar archivos/directorios
- `ls`: Listar contenido de directorios
- `mkdir`: Crear directorios
- `mv`: Mover/renombrar archivos
- `rm`: Eliminar archivos
- `rmdir`: Eliminar directorios vacíos
- `touch`: Crear archivos vacíos/actualizar timestamp

#### Información del Sistema
- `hostname`: Mostrar nombre del sistema
- `ps`: Mostrar procesos en ejecución
- `pwd`: Mostrar directorio actual
- `uptime`: Mostrar tiempo de actividad
- `env`: Variables de entorno

#### Herramientas de Desarrollo
- `node`: Ejecutar código Node.js
- `python3`: Ejecutar scripts Python
- `code`: Operaciones de VSCode
- `jq`: Procesar JSON

#### Utilidades
- `curl`: Llamadas HTTP
- `head`, `sort`, `tail`: Procesamiento de texto
- `clear`: Limpiar terminal
- `which`: Localizar comandos
- `export`, `chmod`: Gestión de entorno
- `sch`, `hostname`, `kill`, `ln`: Utilidades del sistema
- `xxd`, `alias`, `false`, `getconf`, `true`: Comandos adicionales
- `loadenv`, `wasm`, `xdg-open`, `command`, `exit`, `source`: Utilidades especializadas

## Base de Datos

### Supabase (Por Defecto)
- **Cliente**: `@supabase/supabase-js`
- **Autenticación**: Email y contraseña
- **Seguridad**: Row Level Security (RLS) obligatorio
- **Configuración**: Variables de entorno automáticas
- **Patrón**: Singleton para clientes

### Configuración de Entorno
- **Variables Requeridas**:
  - `VITE_SUPABASE_URL`
  - `VITE_SUPABASE_ANON_KEY`
- **Archivo**: `.env` creado automáticamente
- **Gestión**: Configuración automática desde credenciales

### Migraciones SQL
- **Ubicación**: `/supabase/migrations/`
- **Formato**: Archivos SQL descriptivos
- **Nomenclatura**: Sin prefijos numéricos
- **Contenido**: Comentarios markdown + SQL
- **Seguridad**: RLS habilitado por defecto

## Frameworks y Librerías

### Frontend
- **React**: Framework principal
- **Vite**: Build tool y servidor de desarrollo
- **HTML5 Canvas**: Para aplicaciones gráficas
- **CSS**: Estilos y animaciones

### Backend
- **Node.js**: Runtime principal
- **Express.js**: Framework web (si se requiere)
- **APIs REST**: Implementación nativa

### Utilidades
- **react-spring**: Animaciones físicas
- **Sharp**: Procesamiento de imágenes (Node.js)
- **Fetch API**: Llamadas HTTP nativas

## Configuración de Proyecto

### Estructura Típica
```
proyecto/
├── package.json
├── index.html
├── src/
│   ├── main.jsx
│   ├── App.jsx
│   └── index.css
├── supabase/
│   └── migrations/
└── .env
```

### Configuración de Vite
- **Plugin React**: `@vitejs/plugin-react`
- **TypeScript**: Soporte completo
- **Hot Reload**: Recarga automática
- **Build**: Optimización automática

## Limitaciones Técnicas

### No Soportado
- **Binarios Nativos**: Cualquier ejecutable compilado
- **Compiladores C/C++**: g++, clang, etc.
- **Git**: Control de versiones
- **Pip**: Gestión de paquetes Python
- **Librerías Python de Terceros**: Solo librería estándar
- **Dependencias del Sistema**: Módulos que requieren librerías nativas

### Restricciones de Seguridad
- **Operaciones Destructivas**: DROP, DELETE prohibidos
- **Transacciones Explícitas**: BEGIN, COMMIT, ROLLBACK prohibidos
- **Integridad de Datos**: Prioridad máxima
- **RLS**: Obligatorio en todas las tablas

## Herramientas de Desarrollo

### Formateo de Código
- **Indentación**: 2 espacios
- **Linting**: ESLint (si se configura)
- **Prettier**: Formateo automático

### Debugging
- **Console Logging**: Output estructurado
- **Error Handling**: Manejo de errores robusto
- **TypeScript**: Tipado estático (si se usa)

## Integración y Despliegue

### Variables de Entorno
- **Desarrollo**: Configuración automática
- **Producción**: Variables específicas
- **Seguridad**: Credenciales protegidas

### Servidor de Desarrollo
- **Vite Dev Server**: Puerto automático
- **Hot Reload**: Cambios automáticos
- **Preview**: URL automática

## Características Especiales

### Artefactos Únicos
- **Solución Completa**: Todo en un artefacto
- **Acciones Secuenciales**: Orden lógico
- **Identificadores**: Sistema de IDs descriptivos

### Pensamiento Sistemático
- **Chain of Thought**: Pasos de implementación
- **Planificación**: Enfoque holístico
- **Comunicación**: Clara y concisa
