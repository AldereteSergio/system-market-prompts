# Stack Tecnológico - CodeBuddy Craft Prompt

## Tecnologías Base

### Modelo de Lenguaje
- **Base**: No especificado (probablemente Claude Sonnet 4 o GPT-4)
- **Proveedor**: CodeBuddy
- **Capacidad**: Procesamiento de lenguaje natural, programación y desarrollo

### Plataforma de Desarrollo
- **Entorno**: CodeBuddy IDE/Editor
- **Sistema Operativo**: Windows 10 Pro (win32 x64)
- **Shell**: Command Prompt (CMD)
- **Directorio de Trabajo**: Dinámico basado en {path}

## Herramientas de Desarrollo

### Gestión de Archivos
- **read_file**: Lectura de archivos con soporte para PDF y DOCX
- **write_to_file**: Escritura y creación de archivos
- **replace_in_file**: Edición específica con SEARCH/REPLACE
- **list_files**: Listado de archivos y directorios
- **search_files**: Búsqueda con regex en archivos
- **list_code_definition_names**: Análisis de definiciones de código

### Ejecución de Comandos
- **execute_command**: Ejecución de comandos CLI
- **Sistema**: Windows Command Prompt
- **Sintaxis**: Comandos de Windows con & para encadenamiento
- **Variables**: %VAR% para variables de entorno
- **Rutas**: Backslash (\) como separador

### Comunicación y Interacción
- **chat_mode_respond**: Respuestas conversacionales
- **ask_followup_question**: Preguntas de seguimiento
- **preview_markdown**: Vista previa de archivos Markdown
- **openweb**: Apertura de URLs en navegador

### Gestión de Proyectos
- **attempt_completion**: Confirmación de tareas completadas
- **use_rule**: Aplicación de reglas del sistema
- **Integración**: Soporte para múltiples integraciones

## Frameworks y Librerías Implícitas

### Sistema de Archivos
- **File System API**: Acceso completo al sistema de archivos
- **Path Management**: Gestión de rutas relativas y absolutas
- **File Operations**: Operaciones CRUD completas
- **Search Engine**: Motor de búsqueda con regex

### Procesamiento de Lenguaje
- **Regex Engine**: Motor de expresiones regulares (Rust syntax)
- **Markdown Parser**: Procesamiento de archivos Markdown
- **Code Analysis**: Análisis de definiciones de código
- **Text Processing**: Procesamiento de texto y archivos

### Integración de Herramientas
- **XML Parser**: Procesamiento de formato XML para herramientas
- **JSON Handler**: Manejo de datos JSON para MCP
- **Command Parser**: Análisis y validación de comandos
- **Tool Registry**: Registro y gestión de herramientas disponibles

## Características Técnicas

### Arquitectura
- **Modular Design**: Sistema modular con herramientas independientes
- **Dynamic Context**: Contexto dinámico basado en environment_details
- **Mode-Based Architecture**: Arquitectura basada en modos de operación
- **Tool Integration**: Integración flexible de herramientas

### Rendimiento
- **Iterative Execution**: Ejecución iterativa paso a paso
- **Efficient Context**: Uso eficiente del contexto disponible
- **Tool Optimization**: Optimización de selección de herramientas
- **Memory Management**: Gestión eficiente de memoria

### Escalabilidad
- **Extensible Tools**: Sistema de herramientas extensible
- **MCP Integration**: Integración con servidores MCP externos
- **Plugin Architecture**: Arquitectura de plugins para integraciones
- **Dynamic Loading**: Carga dinámica de capacidades

## Dependencias Técnicas

### Requisitos del Sistema
- **File System Access**: Acceso completo al sistema de archivos
- **Command Execution**: Capacidad de ejecutar comandos CLI
- **Network Access**: Acceso a red para integraciones
- **Browser Integration**: Integración con navegador web

### Integraciones Externas
- **MCP Servers**: Servidores Model Context Protocol
- **Supabase**: Backend as a Service con PostgreSQL
- **CloudStudio**: Plataforma de despliegue
- **Tencent CloudBase**: Servicios cloud chinos
- **EdgeOne Pages**: Hosting de páginas

### Configuración
- **Environment Setup**: Configuración del entorno de desarrollo
- **Tool Configuration**: Configuración de herramientas
- **Integration Setup**: Configuración de integraciones
- **Mode Configuration**: Configuración de modos de operación

## Características de Ejecución

### Procesamiento
- **Real-time Processing**: Procesamiento en tiempo real
- **Context-Aware**: Consciente del contexto del proyecto
- **Mode-Aware**: Consciente del modo de operación
- **Tool-Aware**: Consciente de herramientas disponibles

### Comunicación
- **Direct Communication**: Comunicación directa con el usuario
- **Tool Feedback**: Retroalimentación de herramientas
- **Error Handling**: Manejo de errores y excepciones
- **Progress Tracking**: Seguimiento de progreso de tareas

### Seguridad
- **Command Validation**: Validación de comandos antes de ejecución
- **File Protection**: Protección de archivos críticos
- **Access Control**: Control de acceso a recursos
- **Approval System**: Sistema de aprobación para operaciones críticas

## Herramientas MCP

### Servidores Conectados
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
- **URI Format**: Formato URI para identificación de recursos

## Integraciones Especializadas

### Supabase
- **Database**: PostgreSQL con capacidades relacionales
- **Authentication**: Sistema de autenticación
- **Storage**: Almacenamiento de archivos
- **Real-time**: Sincronización en tiempo real
- **API**: APIs RESTful y GraphQL

### CloudStudio
- **Deployment**: Despliegue de proyectos web
- **Preview**: Enlaces de vista previa remota
- **Integration**: Integración con proyectos locales

### Tencent CloudBase
- **Database**: NoSQL con sincronización en tiempo real
- **Cloud Functions**: Funciones serverless
- **Storage**: Almacenamiento de archivos con CDN
- **Authentication**: Gestión de usuarios integrada
- **Hosting**: Hosting de sitios estáticos

### EdgeOne Pages
- **Hosting**: Hosting de páginas web
- **CDN**: Red de distribución de contenido
- **Status**: Conexión perdida (requiere reautorización)
