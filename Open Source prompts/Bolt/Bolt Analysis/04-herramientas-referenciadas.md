# Herramientas Referenciadas: Bolt

## Sistema de Artefactos

### boltArtifact
**Descripción**: Contenedor principal para todas las acciones de un proyecto
**Uso**: Envuelve todas las acciones relacionadas con una tarea específica
**Atributos**:
- `id`: Identificador único descriptivo (kebab-case)
- `title`: Título descriptivo del artefacto
**Ejemplo**:
```xml
<boltArtifact id="snake-game" title="Snake Game in HTML and JavaScript">
  <!-- acciones aquí -->
</boltArtifact>
```

### boltAction
**Descripción**: Acción específica dentro de un artefacto
**Tipos Disponibles**:
- `shell`: Comandos de terminal
- `file`: Crear/actualizar archivos
- `start`: Iniciar servidor de desarrollo

## Tipos de Acciones

### 1. Acción Shell (type="shell")
**Descripción**: Ejecuta comandos en la terminal
**Características**:
- Usar `--yes` con npx
- Secuencial con `&&`
- No comandos de desarrollo aquí
**Ejemplo**:
```xml
<boltAction type="shell">npm install --save-dev vite</boltAction>
```

### 2. Acción File (type="file")
**Descripción**: Crea o actualiza archivos
**Atributos**:
- `filePath`: Ruta relativa al directorio actual
**Características**:
- Contenido completo siempre
- Sin diffs o placeholders
- Rutas relativas obligatorias
**Ejemplo**:
```xml
<boltAction type="file" filePath="package.json">
{
  "name": "my-project",
  "scripts": {
    "dev": "vite"
  }
}
</boltAction>
```

### 3. Acción Start (type="start")
**Descripción**: Inicia servidor de desarrollo
**Características**:
- Solo para iniciar aplicación
- No re-ejecutar si ya está corriendo
- Detección automática de cambios
**Ejemplo**:
```xml
<boltAction type="start">npm run dev</boltAction>
```

## Comandos Shell Disponibles

### Operaciones de Archivos
- **cat**: Mostrar contenido de archivos
- **cp**: Copiar archivos/directorios
- **ls**: Listar contenido de directorios
- **mkdir**: Crear directorios
- **mv**: Mover/renombrar archivos
- **rm**: Eliminar archivos
- **rmdir**: Eliminar directorios vacíos
- **touch**: Crear archivos vacíos/actualizar timestamp

### Información del Sistema
- **hostname**: Mostrar nombre del sistema
- **ps**: Mostrar procesos en ejecución
- **pwd**: Mostrar directorio actual
- **uptime**: Mostrar tiempo de actividad
- **env**: Variables de entorno

### Herramientas de Desarrollo
- **node**: Ejecutar código Node.js
- **python3**: Ejecutar scripts Python
- **code**: Operaciones de VSCode
- **jq**: Procesar JSON

### Utilidades del Sistema
- **curl**: Llamadas HTTP
- **head**: Mostrar primeras líneas
- **sort**: Ordenar texto
- **tail**: Mostrar últimas líneas
- **clear**: Limpiar terminal
- **which**: Localizar comandos
- **export**: Exportar variables
- **chmod**: Cambiar permisos
- **sch**: Comando del sistema
- **kill**: Terminar procesos
- **ln**: Crear enlaces
- **xxd**: Editor hexadecimal
- **alias**: Crear alias
- **false**: Retornar falso
- **getconf**: Configuración del sistema
- **true**: Retornar verdadero
- **loadenv**: Cargar variables de entorno
- **wasm**: WebAssembly
- **xdg-open**: Abrir archivos
- **command**: Ejecutar comando
- **exit**: Salir
- **source**: Ejecutar script

## Herramientas de Base de Datos

### Supabase
**Descripción**: Base de datos por defecto
**Configuración Automática**:
- Variables de entorno automáticas
- Archivo .env creado automáticamente
- Cliente singleton

### Migraciones SQL
**Ubicación**: `/supabase/migrations/`
**Formato**: Archivos SQL con comentarios markdown
**Nomenclatura**: Sin prefijos numéricos
**Ejemplo**:
```sql
/*
  # Create users table
  1. New Tables
    - `users`
      - `id` (uuid, primary key)
      - `email` (text, unique)
  2. Security
    - Enable RLS on `users` table
*/

CREATE TABLE IF NOT EXISTS users (
  id uuid PRIMARY KEY DEFAULT gen_random_uuid(),
  email text UNIQUE NOT NULL
);
```

## Herramientas de Desarrollo Web

### Vite
**Descripción**: Servidor de desarrollo preferido
**Características**:
- Hot reload automático
- Build optimizado
- Plugin React disponible

### Servidores Web Alternativos
- **servor**: Servidor web ligero
- **serve**: Servidor estático
- **http-server**: Servidor HTTP básico
- **Node.js APIs**: Servidores personalizados

## Gestión de Paquetes

### NPM
**Descripción**: Gestión principal de dependencias
**Comandos**:
- `npm install`: Instalar dependencias
- `npm run dev`: Ejecutar servidor de desarrollo
- `npm run build`: Construir proyecto

### NPX
**Descripción**: Ejecutar paquetes
**Características**:
- Usar `--yes` flag obligatorio
- Ejecución directa de paquetes

## Herramientas de Configuración

### package.json
**Descripción**: Configuración del proyecto
**Contenido Típico**:
- Nombre del proyecto
- Scripts de desarrollo
- Dependencias
- Configuración de build

### Variables de Entorno (.env)
**Descripción**: Configuración de entorno
**Variables Supabase**:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

## Herramientas de Código

### React
**Descripción**: Framework principal para frontend
**Características**:
- Componentes funcionales
- Hooks
- JSX

### TypeScript
**Descripción**: Superset de JavaScript con tipado
**Características**:
- Tipado estático
- Interfaces
- Generics

### HTML5 Canvas
**Descripción**: Para aplicaciones gráficas
**Uso**: Juegos, visualizaciones, animaciones

## Herramientas de Seguridad

### Row Level Security (RLS)
**Descripción**: Seguridad a nivel de fila en Supabase
**Obligatorio**: Para todas las tablas nuevas
**Configuración**:
```sql
ALTER TABLE table_name ENABLE ROW LEVEL SECURITY;
```

### Políticas de Seguridad
**Descripción**: Reglas de acceso a datos
**Ejemplo**:
```sql
CREATE POLICY "Users can read own data"
  ON users
  FOR SELECT
  TO authenticated
  USING (auth.uid() = id);
```

## Herramientas de Formateo

### Indentación
**Estándar**: 2 espacios
**Aplicación**: Todo el código generado

### Markdown
**Descripción**: Formato preferido para respuestas
**Restricciones**: Solo elementos HTML permitidos

## Herramientas de Comunicación

### Chain of Thought
**Descripción**: Pasos de implementación
**Formato**: 2-4 líneas máximo
**Ejemplo**:
```
I'll start by:
1. Set up Vite + React
2. Create components
3. Implement functionality
```

### Elementos HTML Permitidos
**Descripción**: Tags HTML disponibles para formateo
**Uso**: Solo en artefactos, no en respuestas normales

## Limitaciones de Herramientas

### No Disponibles
- **Git**: Control de versiones
- **Pip**: Gestión de paquetes Python
- **Compiladores C/C++**: g++, clang
- **Binarios Nativos**: Cualquier ejecutable compilado

### Restricciones Python
- **Solo Librería Estándar**: No librerías de terceros
- **Sin Pip**: No instalación de paquetes
- **Sin Módulos Nativos**: curses, etc.

### Restricciones de Base de Datos
- **Operaciones Destructivas**: DROP, DELETE prohibidos
- **Transacciones Explícitas**: BEGIN, COMMIT, ROLLBACK prohibidos
- **Integridad de Datos**: Prioridad máxima
