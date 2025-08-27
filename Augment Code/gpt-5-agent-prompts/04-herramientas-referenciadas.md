# Herramientas Referenciadas - Augment Code GPT-5

## Herramientas de Información y Análisis

### 1. view tool
- **Propósito**: Lectura de archivos específicos y búsquedas dentro de archivos
- **Uso sin search_query_regex**:
  - Cuando el usuario pide leer un archivo específico
  - Para obtener comprensión general del contenido
  - Cuando se tienen líneas específicas en mente
- **Uso con search_query_regex**:
  - Buscar texto específico en un archivo
  - Encontrar todas las referencias de un símbolo
  - Encontrar usos de un símbolo específico
  - Encontrar definición de un símbolo
- **Restricción**: Solo usar con propósito claro, no para navegación exploratoria

### 2. grep-search tool
- **Propósito**: Búsqueda en múltiples archivos/directorios o todo el codebase
- **Casos de uso**:
  - Buscar texto específico
  - Encontrar todas las referencias de un símbolo
  - Encontrar usos de un símbolo específico
- **Restricciones**: 
  - Solo para consultas específicas con acción clara
  - Constreñir alcance (directorios/globs)
  - Evitar búsquedas exploratorias o repetidas amplias

### 3. codebase-retrieval tool
- **Propósito**: Información de alto nivel del codebase
- **Casos de uso**:
  - No saber qué archivos contienen la información necesaria
  - Recolectar información de alto nivel sobre la tarea
  - Recolectar información general del codebase
- **Ejemplos de buenas consultas**:
  - "¿Dónde está la función que maneja autenticación de usuarios?"
  - "¿Qué tests hay para la funcionalidad de login?"
  - "¿Cómo se conecta la base de datos a la aplicación?"
- **Ejemplos de malas consultas**:
  - "Encontrar definición del constructor de la clase Foo" (usar grep-search)
  - "Encontrar todas las referencias a la función bar" (usar grep-search)
  - "Mostrar cómo se usa la clase Checkout en services/payment.py" (usar view con regex)

### 4. git-commit-retrieval tool
- **Propósito**: Análisis de cambios históricos en el repositorio
- **Casos de uso**:
  - Encontrar cómo se hicieron cambios similares en el pasado
  - Encontrar el contexto de un cambio específico
  - Encontrar la razón de un cambio específico
- **Ejemplos de buenas consultas**:
  - "¿Cómo se implementó la funcionalidad de login en el pasado?"
  - "¿Cómo implementamos feature flags para nuevas funcionalidades?"
  - "¿Por qué se cambió la conexión de base de datos para usar SSL?"
- **Comando relacionado**: `git show <commit_hash>`

## Herramientas de Gestión de Tareas

### 5. add_tasks
- **Propósito**: Crear nuevas tareas o subtareas
- **Uso**: Para organizar trabajo complejo en unidades manejables
- **Contexto**: Gestión de proyectos con múltiples pasos

### 6. update_tasks
- **Propósito**: Modificar propiedades de tareas existentes
- **Uso**:
  - Actualización individual: `{"task_id": "abc", "state": "COMPLETE"}`
  - Actualización múltiple: `{"tasks": [{"task_id": "abc", "state": "COMPLETE"}, {"task_id": "def", "state": "IN_PROGRESS"}]}`
- **Estados disponibles**: [ ], [/], [-], [x]

### 7. reorganize_tasklist
- **Propósito**: Reestructuración compleja que afecta múltiples tareas
- **Uso**: Solo para cambios estructurales mayores
- **Contexto**: Reorganización de proyectos complejos

## Herramientas de Edición de Código

### 8. str_replace_editor
- **Propósito**: Herramienta obligatoria para realizar ediciones
- **Uso**: Única herramienta permitida para modificaciones de código
- **Requisito**: Recolectar información necesaria antes de usar
- **Contexto**: Edición segura y controlada del codebase

## Herramientas de Terminal y Ejecución

### 9. launch-process
- **Propósito**: Ejecución de comandos del sistema
- **Parámetros**:
  - `wait=true`: Para comandos de corta duración
  - `wait=false`: Para procesos largos (monitorear via read-process/list-processes)
- **Funcionalidad**: Capturar stdout/stderr y códigos de salida

### 10. read-process
- **Propósito**: Lectura de procesos en ejecución
- **Uso**: Para monitorear procesos largos iniciados con wait=false

### 11. list-processes
- **Propósito**: Listado de procesos activos
- **Uso**: Para monitorear procesos en ejecución

## Herramientas de Gestión de Paquetes

### 12. Package Manager Commands
- **JavaScript/Node.js**: npm, yarn, pnpm
- **Python**: pip, poetry, conda
- **Rust**: cargo
- **Go**: go
- **Ruby**: gem, bundle
- **PHP**: composer
- **C#/.NET**: dotnet
- **Java**: Maven, Gradle

## Herramientas de Testing

### 13. Testing Frameworks
- **Propósito**: Escritura y ejecución de tests unitarios
- **Uso**: Verificación de cambios implementados
- **Contexto**: Aseguramiento de calidad del código

## Herramientas de Visualización

### 14. XML Code Display
- **Tag**: `<augment_code_snippet>`
- **Atributos**: `path=` y `mode="EXCERPT"`
- **Límite**: Máximo 10 líneas por snippet
- **Contexto**: Visualización controlada de código

## Herramientas de Recuperación

### 15. User Help Request
- **Propósito**: Solicitar ayuda cuando se detectan patrones circulares
- **Uso**: Cuando las herramientas no progresan
- **Contexto**: Prevención de bucles infinitos

## Patrones de Uso de Herramientas

### Secuencia Típica Optimizada
1. **Single Info-gathering** → Una llamada de alta señal
2. **Decision Point** → Evaluar necesidad de tasklist
3. **Incremental Planning** → Planificación incremental
4. **Execution** → str_replace_editor
5. **Validation** → launch-process para verificación
6. **Review** → update_tasks

### Reglas de Uso Refinadas
- **Obligatorio**: Recolección de información antes de str_replace_editor
- **Recomendado**: git-commit-retrieval para planificación
- **Opcional**: Task management para trabajo complejo
- **Prohibido**: Edición directa de archivos de paquetes
- **Eficiencia**: Minimizar tool calls innecesarios
- **Batching**: Agrupar llamadas relacionadas
