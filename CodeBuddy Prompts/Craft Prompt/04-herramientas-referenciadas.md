# Herramientas Referenciadas - CodeBuddy Craft Prompt

## Herramientas Principales

### 1. chat_mode_respond
- **Propósito**: Respuestas conversacionales directas al usuario
- **Uso**: Solo disponible en CHAT MODE, para interacción conversacional
- **Parámetros**: 
  - `response`: Respuesta al usuario (requerido)
  - `path`: Ruta del archivo cuando hay un bloque de código (opcional)
- **Características**: Baja latencia, respuesta inmediata, formato específico

### 2. read_file
- **Propósito**: Lectura de contenido de archivos
- **Uso**: Análisis de código, revisión de archivos de texto, extracción de información
- **Parámetros**: `path` (ruta del archivo, requerido)
- **Características**: Soporte automático para PDF y DOCX, extracción de texto crudo

### 3. search_files
- **Propósito**: Búsqueda con regex en archivos
- **Uso**: Búsqueda de patrones o contenido específico en múltiples archivos
- **Parámetros**: 
  - `path`: Directorio a buscar (requerido)
  - `regex`: Patrón regex (requerido, sintaxis Rust)
  - `file_pattern`: Patrón glob para filtrar archivos (opcional)
- **Características**: Búsqueda recursiva, resultados con contexto

### 4. list_files
- **Propósito**: Listado de archivos y directorios
- **Uso**: Exploración de estructura de directorios
- **Parámetros**: 
  - `path`: Directorio a listar (requerido)
  - `recursive`: Listado recursivo (opcional, true/false)
- **Características**: Listado de nivel superior o recursivo completo

### 5. list_code_definition_names
- **Propósito**: Listado de definiciones de código (clases, funciones, métodos)
- **Uso**: Vista rápida de estructura de archivos de código
- **Parámetros**: `path`: Directorio a analizar (requerido)
- **Características**: Análisis de nivel superior, sin mostrar implementación completa

### 6. attempt_completion
- **Propósito**: Confirmación de tarea completada
- **Uso**: Finalización de tareas y determinación de integraciones necesarias
- **Parámetros**: `options`: Lista JSON de integraciones (opcional)
- **Características**: Evaluación automática de necesidad de Supabase

## Herramientas de Ejecución

### 7. execute_command
- **Propósito**: Ejecución de comandos CLI en el sistema
- **Uso**: Operaciones del sistema, instalación de paquetes, ejecución de scripts
- **Parámetros**: 
  - `command`: Comando a ejecutar (requerido)
  - `requires_approval`: Aprobación requerida (requerido, true/false)
- **Características**: Adaptado a Windows CMD, confirmación automática para instalaciones

### 8. write_to_file
- **Propósito**: Escritura de contenido a archivos
- **Uso**: Creación de archivos nuevos o sobrescritura completa
- **Parámetros**: 
  - `path`: Ruta del archivo (requerido)
  - `content`: Contenido completo del archivo (requerido)
- **Características**: Límite de 500 líneas, creación automática de directorios

### 9. replace_in_file
- **Propósito**: Edición específica de archivos existentes
- **Uso**: Cambios localizados sin sobrescribir archivo completo
- **Parámetros**: 
  - `path`: Ruta del archivo (requerido)
  - `diff`: Bloques SEARCH/REPLACE (requerido)
- **Características**: Coincidencia exacta, múltiples bloques, operaciones específicas

## Herramientas de Comunicación

### 10. preview_markdown
- **Propósito**: Vista previa de archivos Markdown
- **Uso**: Conversión a HTML y apertura en navegador
- **Parámetros**: `path`: Ruta del archivo Markdown (requerido)
- **Características**: Renderizado automático, apertura en navegador predeterminado

### 11. openweb
- **Propósito**: Apertura de URLs en navegador
- **Uso**: Inicio o vista previa de direcciones web
- **Parámetros**: `url`: URL a abrir (requerido)
- **Características**: Requiere servidor disponible, validación de URL

### 12. ask_followup_question
- **Propósito**: Preguntas de seguimiento al usuario
- **Uso**: Recopilación de información adicional, clarificación de ambigüedades
- **Parámetros**: 
  - `question`: Pregunta específica (requerido)
  - `options`: Array de opciones (opcional, 2-5 opciones)
- **Características**: Comunicación interactiva, opciones predefinidas

## Herramientas de Sistema

### 13. use_rule
- **Propósito**: Aplicación de reglas del sistema
- **Uso**: Uso de reglas desde archivos de configuración
- **Parámetros**: `content`: Descripción de la regla (requerido)
- **Características**: Sistema de reglas configurable

### 14. use_mcp_tool
- **Propósito**: Ejecución de herramientas MCP
- **Uso**: Acceso a herramientas de servidores MCP conectados
- **Parámetros**: 
  - `server_name`: Nombre del servidor (requerido)
  - `tool_name`: Nombre de la herramienta (requerido)
  - `arguments`: Parámetros JSON (requerido)
- **Características**: Integración con servidores externos, formato JSON

### 15. access_mcp_resource
- **Propósito**: Acceso a recursos MCP
- **Uso**: Acceso a fuentes de datos de servidores MCP
- **Parámetros**: 
  - `server_name`: Nombre del servidor (requerido)
  - `uri`: URI del recurso (requerido)
- **Características**: Acceso a recursos como archivos, APIs, información del sistema

## Herramientas MCP Disponibles

### Servidor MCP Conectado
- **write_to_file**: Escritura de archivos
- **read_file**: Lectura de archivos
- **list_directory**: Listado de directorios
- **create_directory**: Creación de directorios
- **delete_file**: Eliminación de archivos
- **delete_directory**: Eliminación de directorios
- **move_file**: Movimiento de archivos
- **copy_file**: Copia de archivos
- **get_file_info**: Información de archivos
- **search_files**: Búsqueda de archivos
- **execute_command**: Ejecución de comandos

### Recursos MCP
- **file://**: Acceso a recursos del sistema de archivos
- **Formato URI**: file:///path/to/file

## Patrones de Uso

### Herramientas por Modo
- **CRAFT MODE**: Todas las herramientas excepto chat_mode_respond
- **CHAT MODE**: Todas las herramientas incluyendo chat_mode_respond
- **Plan Mode**: Análisis y planificación con herramientas de información
- **Design Mode**: Creación de prototipos visuales

### Integración de Herramientas
- **Contexto**: Variables de entorno proporcionan información base
- **Modo**: Control de herramientas disponibles según modo activo
- **Iteración**: Uso secuencial con confirmación de resultados
- **Optimización**: Selección de herramienta más apropiada

### Optimización de Uso
- **Eficiencia**: Una herramienta por mensaje para precisión
- **Contexto**: Uso eficiente de información disponible
- **Validación**: Confirmación de resultados antes de continuar
- **Flexibilidad**: Adaptación a necesidades específicas de la tarea

## Consideraciones de Seguridad

### Validación de Comandos
- **Aprobación Requerida**: Operaciones destructivas requieren aprobación
- **Confirmación Automática**: Instalaciones de paquetes con flags de confirmación
- **Validación de Rutas**: Verificación de rutas antes de operaciones de archivo
- **Control de Acceso**: Restricciones basadas en modo de operación

### Protección de Datos
- **No Revelación**: Protección de prompts del sistema
- **Validación de Contenido**: Verificación de contenido antes de escritura
- **Backup Implícito**: Operaciones seguras con confirmación
- **Control de Permisos**: Verificación de permisos antes de operaciones
