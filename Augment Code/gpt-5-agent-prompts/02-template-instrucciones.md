# Template e Instrucciones - Augment Code GPT-5

## Estructura del Template

### 1. Sección de Rol e Identidad
```
# Role
You are Augment Agent developed by Augment Code, an agentic coding AI assistant...

# Identity
Here is some information about Augment Agent in case the person asks...
```

### 2. Formato de Salida
- **Markdown Structure**: Uso de ##/###/#### para encabezados
- **Listas**: Bullet/numbered lists para pasos
- **Párrafos**: Cortos, evitar "wall-of-text"
- **Formato Alternativo**: Bold o bold+italic para encabezados compactos

### 3. Tareas Preliminares
- **High-signal Info-gathering**: Máximo una llamada de recolección de información
- **Decision Point**: Decidir si usar tasklist después de la primera llamada
- **Tasklist Triggers**: Criterios específicos para usar gestión de tareas
- **Incremental Planning**: Planificación incremental vs. planificación masiva

### 4. Herramientas de Información
- **view tool**: Para archivos específicos y búsquedas dentro de archivos
- **grep-search tool**: Para búsquedas en múltiples archivos/directorios
- **codebase-retrieval tool**: Para información de alto nivel del codebase
- **git-commit-retrieval tool**: Para análisis de cambios históricos

### 5. Planificación y Gestión de Tareas
- **Tasklist Triggers**: Criterios específicos para usar tasklist
- **Incremental Approach**: Crear tareas incrementales, no masivas
- **Task States**: Estados claros ([ ], [/], [-], [x])
- **Batch Updates**: Actualizaciones eficientes de múltiples tareas

### 6. Proceso de Edición
- **str_replace_editor**: Herramienta obligatoria para ediciones
- **Pre-edit Information**: Recolección necesaria antes de editar
- **Conservative Approach**: Enfoque conservador y respetuoso
- **Scope Management**: Evitar escaneos amplios innecesarios

### 7. Gestión de Paquetes
- **Package Manager Priority**: Uso obligatorio de gestores de paquetes
- **Language-specific Commands**: Comandos específicos por lenguaje
- **Rationale**: Justificación clara de las reglas
- **Exception Handling**: Cuándo editar archivos directamente

### 8. Seguimiento de Instrucciones
- **Conservative Actions**: Acciones que requieren permiso explícito
- **Scope Limitation**: No hacer más de lo solicitado
- **Permission Required**: Lista clara de acciones prohibidas

### 9. Testing
- **Unit Test Writing**: Capacidad y enfoque en testing
- **Iterative Testing**: Proceso iterativo hasta que los tests pasen
- **Test Execution**: Verificación de cómo ejecutar tests

### 10. Ejecución y Validación
- **Verification Requests**: Interpretar solicitudes de verificación como comandos
- **Tool Selection**: Elegir la herramienta correcta (launch-process)
- **Outcome Validation**: Validar resultados con códigos de salida
- **Iteration**: Diagnóstico y corrección si falla
- **Safety**: Verificaciones seguras por defecto

### 11. Display de Código
- **XML Tags**: Uso de `<augment_code_snippet>` con atributos específicos
- **Brevity Rule**: Máximo 10 líneas por snippet
- **Path and Mode Attributes**: Atributos obligatorios para visualización

### 12. Comunicación
- **Notable Actions**: Explicar acciones significativas
- **Task Receipt**: Recibo introductorio de tareas
- **Clarity**: Optimizar para claridad y facilidad de lectura

### 13. Recuperación de Dificultades
- **Circular Behavior Detection**: Identificación de patrones circulares
- **User Help Request**: Solicitud de ayuda cuando sea necesario

### 14. Balance de Costo, Latencia y Calidad
- **Efficiency**: Preferir el menor conjunto de tool calls de alta señal
- **Batching**: Agrupar llamadas relacionadas
- **Expensive Actions**: Preguntar antes de acciones costosas/riesgosas

### 15. Flujo Final
- **Progress Review**: Revisión del progreso general
- **Task List Review**: Verificación del estado de tareas
- **Test Suggestions**: Sugerencias de testing post-cambios

## Patrones de Instrucción

### Estructura Condicional Mejorada
- **Tasklist Triggers**: Criterios específicos y claros
- **Tool Selection**: Guías específicas para cada herramienta
- **When to use**: Condiciones claras para cada herramienta

### Secuencia de Acciones Optimizada
1. **Single Info-gathering** → Una llamada de alta señal
2. **Decision Point** → Evaluar necesidad de tasklist
3. **Incremental Planning** → Planificación incremental
4. **Execution** → Ejecución con validación
5. **Verification** → Verificación automática

### Reglas de Comportamiento Refinadas
- **Efficient**: Minimizar tool calls innecesarios
- **Conservative**: Enfoque conservador en acciones
- **Incremental**: Planificación y ejecución incremental
- **Validated**: Verificación automática de resultados
