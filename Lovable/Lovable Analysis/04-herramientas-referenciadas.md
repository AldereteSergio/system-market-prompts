# Herramientas Referenciadas: Lovable

## Herramientas de Archivos

### lov-write
**Descripción**: Crear o actualizar archivos completos
**Uso**: Para archivos nuevos o reescrituras completas
**Parámetros**:
- `file_path`: Ruta del archivo
- `content`: Contenido completo del archivo
**Nota**: Debe incluir contenido completo del archivo

### lov-line-replace
**Descripción**: Reemplazo de líneas específicas en archivos existentes
**Uso**: Herramienta PREFERIDA para editar archivos existentes
**Parámetros**:
- `file_path`: Ruta del archivo
- `search`: Contenido a buscar
- `first_replaced_line`: Primera línea a reemplazar
- `last_replaced_line`: Última línea a reemplazar
- `replace`: Nuevo contenido
**Características**: Validación de contenido, uso de elipsis para secciones largas

### lov-view
**Descripción**: Leer contenido de archivos
**Uso**: Para examinar archivos no en contexto
**Parámetros**:
- `file_path`: Ruta del archivo
- `lines`: Rango de líneas (opcional)
**Restricción**: NO usar si el archivo ya está en "useful-context"

### lov-rename
**Descripción**: Renombrar archivos
**Uso**: Cambiar nombres de archivos existentes
**Parámetros**:
- `original_file_path`: Ruta original
- `new_file_path`: Nueva ruta

### lov-delete
**Descripción**: Eliminar archivos
**Uso**: Remover archivos del proyecto
**Parámetros**:
- `file_path`: Ruta del archivo a eliminar

## Herramientas de Búsqueda

### lov-search-files
**Descripción**: Búsqueda regex en archivos con filtros
**Uso**: Buscar patrones específicos en el código
**Parámetros**:
- `query`: Patrón regex a buscar
- `include_pattern`: Archivos a incluir (glob)
- `exclude_pattern`: Archivos a excluir (glob)
- `case_sensitive`: Sensibilidad a mayúsculas

## Herramientas de Dependencias

### lov-add-dependency
**Descripción**: Agregar dependencias al proyecto
**Uso**: Instalar paquetes npm
**Parámetros**:
- `package`: Nombre del paquete con versión (ej: "lodash@latest")

### lov-remove-dependency
**Descripción**: Desinstalar paquetes
**Uso**: Remover dependencias del proyecto
**Parámetros**:
- `package`: Nombre del paquete

## Herramientas de Imágenes

### generate_image
**Descripción**: Generar imágenes basadas en prompts de texto
**Uso**: Crear imágenes para el proyecto
**Parámetros**:
- `prompt`: Descripción de la imagen deseada
- `target_path`: Ruta donde guardar la imagen
- `width`: Ancho (512-1920px)
- `height`: Alto (512-1920px)
- `model`: Modelo a usar (flux.schnell, flux.dev)

### edit_image
**Descripción**: Editar o combinar imágenes existentes
**Uso**: Modificar imágenes usando IA
**Parámetros**:
- `image_paths`: Array de rutas de imágenes
- `prompt`: Descripción de la edición
- `target_path`: Ruta de salida
- `strength`: Intensidad del cambio (0.0-1.0)

### lov-download-to-repo
**Descripción**: Descargar archivos desde URLs
**Uso**: Obtener recursos externos
**Parámetros**:
- `source_url`: URL del archivo
- `target_path`: Ruta de destino

## Herramientas Web

### web_search
**Descripción**: Búsqueda web con resultados relevantes
**Uso**: Obtener información actualizada
**Parámetros**:
- `query`: Consulta de búsqueda
- `numResults`: Número de resultados
- `category`: Categoría específica (opcional)
- `links`: Número de enlaces por resultado
- `imageLinks`: Número de enlaces de imágenes

### lov-fetch-website
**Descripción**: Obtener contenido de sitios web
**Uso**: Capturar contenido web en múltiples formatos
**Parámetros**:
- `url`: URL del sitio web
- `formats`: Formatos de salida (markdown, html, screenshot)

## Herramientas de Debugging

### lov-read-console-logs
**Descripción**: Leer logs de consola de la aplicación
**Uso**: Debugging de errores y comportamiento
**Parámetros**:
- `search`: Filtro de búsqueda (opcional)
**Nota**: Solo logs recientes, no se actualizan durante el desarrollo

### lov-read-network-requests
**Descripción**: Leer solicitudes de red
**Uso**: Debugging de llamadas API
**Parámetros**:
- `search`: Filtro de búsqueda (opcional)

## Herramientas de Analytics

### read_project_analytics
**Descripción**: Leer analytics del proyecto en producción
**Uso**: Análisis de uso de la aplicación
**Parámetros**:
- `startdate`: Fecha de inicio
- `enddate`: Fecha de fin
- `granularity`: Granularidad (hourly, daily)

## Patrones de Uso

### Uso Eficiente
1. **Agrupación**: Siempre agrupar operaciones independientes
2. **Paralelización**: Evitar llamadas secuenciales innecesarias
3. **Contexto**: Verificar "useful-context" antes de leer archivos
4. **Especificidad**: Usar la herramienta más apropiada para cada tarea

### Restricciones Importantes
- **NUNCA** leer archivos ya en contexto útil
- **SIEMPRE** agrupar múltiples operaciones cuando sea posible
- **NUNCA** hacer llamadas secuenciales que podrían combinarse
- **PREFERIR** lov-line-replace sobre lov-write para ediciones

### Casos de Uso Específicos
- **Nuevos archivos**: lov-write
- **Ediciones menores**: lov-line-replace
- **Búsquedas**: lov-search-files
- **Dependencias**: lov-add-dependency
- **Imágenes**: generate_image o edit_image
- **Debugging**: lov-read-console-logs
- **Web**: web_search o lov-fetch-website
