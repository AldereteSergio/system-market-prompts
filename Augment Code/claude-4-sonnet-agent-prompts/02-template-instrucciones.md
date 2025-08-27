# Template e Instrucciones - Augment Code

## Estructura del Template

### 1. Sección de Rol e Identidad
```
# Role
You are Augment Agent developed by Augment Code, an agentic coding AI assistant...

# Identity
Here is some information about Augment Agent in case the person asks...
```

### 2. Tareas Preliminares
- **Gathering Information**: Uso obligatorio de herramientas de recolección de información
- **Codebase Retrieval**: Acceso al estado actual del código
- **Git Commit Retrieval**: Análisis de cambios históricos

### 3. Planificación y Gestión de Tareas
- **Task Management Tools**: Herramientas para organizar trabajo complejo
- **Planning Process**: Proceso detallado de planificación en 3 pasos
- **Task States**: Estados de tareas ([ ], [/], [-], [x])

### 4. Proceso de Edición
- **str_replace_editor**: Herramienta obligatoria para ediciones
- **Pre-edit Information Gathering**: Recolección detallada antes de editar
- **Conservative Approach**: Enfoque conservador y respetuoso del codebase

### 5. Gestión de Paquetes
- **Package Manager Priority**: Uso obligatorio de gestores de paquetes
- **Language-specific Commands**: Comandos específicos por lenguaje
- **Exception Handling**: Cuándo editar archivos directamente

### 6. Seguimiento de Instrucciones
- **Conservative Actions**: Acciones que requieren permiso explícito
- **No Flattery Rule**: Prohibición de adulación en respuestas
- **Explicit Permission**: Requisito de autorización para acciones críticas

### 7. Testing
- **Unit Test Writing**: Capacidad y enfoque en testing
- **Iterative Testing**: Proceso iterativo hasta que los tests pasen
- **Test Execution**: Verificación de cómo ejecutar tests

### 8. Display de Código
- **XML Tags**: Uso de `<augment_code_snippet>` con atributos específicos
- **Brevity Rule**: Máximo 10 líneas por snippet
- **Path and Mode Attributes**: Atributos obligatorios para visualización

### 9. Recuperación de Dificultades
- **Circular Behavior Detection**: Identificación de patrones circulares
- **User Help Request**: Solicitud de ayuda cuando sea necesario

### 10. Finalización
- **Task Management Review**: Revisión del progreso general
- **Test Suggestions**: Sugerencias de testing post-cambios

## Patrones de Instrucción

### Estructura Condicional
- **When to use**: Condiciones específicas para usar herramientas
- **If statements**: Instrucciones condicionales claras
- **Consider using**: Sugerencias de uso opcional

### Secuencia de Acciones
1. Information gathering
2. Planning (si es complejo)
3. Execution with tools
4. Testing
5. Review and completion

### Reglas de Comportamiento
- **Conservative**: Enfoque conservador en acciones
- **Explicit**: Requerimiento de permisos explícitos
- **Structured**: Proceso estructurado y organizado
