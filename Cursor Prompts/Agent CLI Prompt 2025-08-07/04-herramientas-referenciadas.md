# Herramientas Referenciadas - Cursor Agent CLI Prompt

## Herramientas de Exploración y Búsqueda

### Grep (Herramienta Principal)
- **Función**: Búsqueda de texto en archivos usando expresiones regulares
- **Uso**: Exploración principal del código base
- **Características**: 
  - Búsqueda de patrones exactos y variaciones
  - Múltiples búsquedas en paralelo
  - Filtrado por tipos de archivo
- **Comando típico**: `grep_search(query, include_pattern, exclude_pattern)`

### Glob
- **Función**: Búsqueda de archivos por patrones de nombre
- **Uso**: Encontrar archivos específicos en el proyecto
- **Características**:
  - Patrones de búsqueda flexibles
  - Filtrado por extensiones
  - Búsqueda recursiva en directorios

### Codebase Search
- **Función**: Búsqueda semántica en el código
- **Uso**: Encontrar código relacionado conceptualmente
- **Características**:
  - Búsqueda por significado, no solo texto
  - Identificación de patrones de código
  - Encontrar implementaciones similares

## Herramientas de Lectura y Análisis

### Read File
- **Función**: Lectura completa o parcial de archivos
- **Uso**: Obtener contenido de archivos para análisis
- **Características**:
  - Lectura de rangos específicos de líneas
  - Resumen de contenido
  - Manejo de archivos grandes
- **Comando típico**: `read_file(target_file, start_line, end_line)`

### List Directory
- **Función**: Exploración de estructura de directorios
- **Uso**: Entender la organización del proyecto
- **Características**:
  - Listado de archivos y carpetas
  - Información de estructura
  - Navegación jerárquica

## Herramientas de Edición y Modificación

### ApplyPatch
- **Función**: Aplicación de cambios específicos a archivos
- **Uso**: Modificación precisa de código existente
- **Características**:
  - Cambios contextuales
  - Validación de contexto antes de aplicar
  - Manejo de conflictos
- **Limitación**: Requiere contexto exacto del archivo

### Edit File
- **Función**: Edición directa de archivos
- **Uso**: Creación o modificación de archivos
- **Características**:
  - Creación de archivos nuevos
  - Modificación de contenido existente
  - Inserción de código en posiciones específicas

### Search/Replace
- **Función**: Búsqueda y reemplazo de texto
- **Uso**: Cambios masivos o específicos en archivos
- **Características**:
  - Reemplazo de patrones
  - Validación de contexto
  - Cambios seguros con confirmación

## Herramientas de Terminal y Sistema

### Terminal Commands
- **Función**: Ejecución de comandos del sistema
- **Uso**: Compilación, testing, gestión de dependencias
- **Características**:
  - Ejecución de comandos bash
  - Captura de salida
  - Manejo de errores
- **Comando típico**: `run_terminal_cmd(command, is_background)`

### Build Tools
- **Función**: Compilación y construcción de proyectos
- **Uso**: Verificar que el código compile correctamente
- **Características**:
  - Múltiples lenguajes soportados
  - Detección automática de build system
  - Manejo de errores de compilación

### Test Tools
- **Función**: Ejecución de tests automatizados
- **Uso**: Verificar funcionalidad del código
- **Características**:
  - Tests unitarios y de integración
  - Reportes de cobertura
  - Detección de regresiones

## Herramientas de Gestión de Proyectos

### File Search
- **Función**: Búsqueda de archivos por nombre
- **Uso**: Localizar archivos específicos
- **Características**:
  - Búsqueda fuzzy
  - Resultados ordenados por relevancia
  - Filtrado por tipo de archivo

### Delete File
- **Función**: Eliminación de archivos
- **Uso**: Limpieza de archivos temporales o obsoletos
- **Características**:
  - Eliminación segura
  - Confirmación antes de eliminar
  - Manejo de errores

## Herramientas de Comunicación y Formato

### Markdown Formatting
- **Función**: Formato de respuestas en Markdown
- **Uso**: Comunicación clara y estructurada
- **Características**:
  - Encabezados organizados
  - Bloques de código con syntax highlighting
  - Listas y tablas formateadas

### Code Citation
- **Función**: Referencia a código específico
- **Uso**: Citar líneas específicas de archivos
- **Características**:
  - Referencias clickeables
  - Contexto de líneas
  - Navegación directa al código

## Herramientas de Optimización

### Parallel Execution
- **Función**: Ejecución simultánea de múltiples herramientas
- **Uso**: Maximizar eficiencia en operaciones
- **Características**:
  - Ejecución concurrente
  - Batching de operaciones
  - Reducción de tiempo de respuesta

### Context Management
- **Función**: Gestión del contexto de trabajo
- **Uso**: Mantener información relevante
- **Características**:
  - Cache de información
  - Limpieza automática
  - Persistencia de contexto relevante

## Herramientas de Validación y Seguridad

### Input Validation
- **Función**: Validación de entradas del usuario
- **Uso**: Asegurar operaciones seguras
- **Características**:
  - Validación de rutas
  - Verificación de permisos
  - Sanitización de inputs

### Error Handling
- **Función**: Manejo de errores y excepciones
- **Uso**: Proporcionar feedback útil al usuario
- **Características**:
  - Captura de errores específicos
  - Sugerencias de solución
  - Fallbacks automáticos
