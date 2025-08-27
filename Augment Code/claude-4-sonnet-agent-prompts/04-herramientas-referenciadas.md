# Herramientas Referenciadas - Augment Code

## Herramientas de Información y Análisis

### 1. information-gathering tools
- **Propósito**: Recolección de información necesaria para tareas
- **Uso**: Llamada obligatoria antes de ejecutar tareas
- **Contexto**: Herramientas generales de recolección de datos

### 2. codebase-retrieval tool
- **Propósito**: Acceso al estado actual del codebase
- **Uso**: Para obtener información sobre el código existente
- **Contexto**: Herramienta principal para análisis de código actual

### 3. git-commit-retrieval tool
- **Propósito**: Análisis de cambios históricos en el repositorio
- **Uso**: Para encontrar patrones de cambios similares en el pasado
- **Contexto**: Útil para planificación basada en cambios previos
- **Comando Relacionado**: `git show <commit_hash>`

## Herramientas de Gestión de Tareas

### 4. add_tasks
- **Propósito**: Crear nuevas tareas o subtareas
- **Uso**: Para organizar trabajo complejo en unidades manejables
- **Contexto**: Gestión de proyectos con múltiples pasos

### 5. update_tasks
- **Propósito**: Modificar propiedades de tareas existentes
- **Uso**: 
  - Actualización individual: `{"task_id": "abc", "state": "COMPLETE"}`
  - Actualización múltiple: `{"tasks": [{"task_id": "abc", "state": "COMPLETE"}, {"task_id": "def", "state": "IN_PROGRESS"}]}`
- **Estados Disponibles**: [ ], [/], [-], [x]

### 6. reorganize_tasklist
- **Propósito**: Reestructuración compleja que afecta múltiples tareas
- **Uso**: Solo para cambios estructurales mayores
- **Contexto**: Reorganización de proyectos complejos

### 7. view_tasklist
- **Propósito**: Revisar la lista actual de tareas
- **Uso**: Para verificar el estado del progreso
- **Contexto**: Monitoreo de avance del proyecto

## Herramientas de Edición de Código

### 8. str_replace_editor
- **Propósito**: Herramienta obligatoria para realizar ediciones
- **Uso**: Única herramienta permitida para modificaciones de código
- **Requisito**: Llamar codebase-retrieval antes de usar
- **Contexto**: Edición segura y controlada del codebase

## Herramientas de Gestión de Paquetes

### 9. Package Manager Commands
- **JavaScript/Node.js**: npm, yarn, pnpm
- **Python**: pip, poetry, conda
- **Rust**: cargo
- **Go**: go
- **Ruby**: gem, bundle
- **PHP**: composer
- **C#/.NET**: dotnet
- **Java**: Maven, Gradle

## Herramientas de Testing

### 10. Testing Frameworks
- **Propósito**: Escritura y ejecución de tests unitarios
- **Uso**: Verificación de cambios implementados
- **Contexto**: Aseguramiento de calidad del código

## Herramientas de Visualización

### 11. XML Code Display
- **Tag**: `<augment_code_snippet>`
- **Atributos**: `path=` y `mode="EXCERPT"`
- **Límite**: Máximo 10 líneas por snippet
- **Contexto**: Visualización controlada de código

## Herramientas de Recuperación

### 12. User Help Request
- **Propósito**: Solicitar ayuda cuando se detectan patrones circulares
- **Uso**: Cuando las herramientas no progresan
- **Contexto**: Prevención de bucles infinitos

## Patrones de Uso de Herramientas

### Secuencia Típica
1. **Information Gathering** → codebase-retrieval, git-commit-retrieval
2. **Planning** → add_tasks, update_tasks (si es complejo)
3. **Execution** → str_replace_editor
4. **Testing** → Testing frameworks
5. **Review** → view_tasklist, update_tasks

### Reglas de Uso
- **Obligatorio**: codebase-retrieval antes de str_replace_editor
- **Recomendado**: git-commit-retrieval para planificación
- **Opcional**: Task management para trabajo complejo
- **Prohibido**: Edición directa de archivos de paquetes
