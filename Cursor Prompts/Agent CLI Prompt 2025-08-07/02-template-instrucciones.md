# Template de Instrucciones - Cursor Agent CLI Prompt

## Estructura General del Prompt

El prompt está organizado en **secciones modulares** que definen diferentes aspectos del comportamiento del agente:

### 1. Identificación y Contexto
```
You are an AI coding assistant, powered by GPT-5.
You are an interactive CLI tool that helps users with software engineering tasks.
```

### 2. Secciones de Comportamiento
- **`<communication>`**: Reglas de comunicación y formato
- **`<status_update_spec>`**: Especificaciones para actualizaciones de estado
- **`<summary_spec>`**: Especificaciones para resúmenes finales
- **`<flow>`**: Flujo de trabajo del agente
- **`<tool_calling>`**: Reglas para uso de herramientas
- **`<context_understanding>`**: Estrategias de exploración
- **`<maximize_parallel_tool_calls>`**: Optimización de ejecución paralela
- **`<making_code_changes>`**: Reglas para modificaciones de código
- **`<code_style>`**: Estándares de estilo de código
- **`<citing_code>`**: Reglas para citación de código
- **`<inline_line_numbers>`**: Manejo de números de línea
- **`<markdown_spec>`**: Especificaciones de formato Markdown

## Patrones de Instrucción

### Estructura de Secciones
Cada sección sigue el patrón:
```
<seccion_nombre>
Contenido de la sección con instrucciones específicas
</seccion_nombre>
```

### Instrucciones Condicionales
- **Reglas CRÍTICAS**: Marcadas con `CRITICAL:` o `MANDATORY:`
- **Reglas IMPORTANTES**: Marcadas con `IMPORTANT:`
- **Comportamientos por defecto**: Especificados con `DEFAULT TO:`

### Especificaciones de Formato
- **Markdown**: Uso específico de encabezados (`###`, `##`)
- **Código**: Formato con backticks para archivos y funciones
- **Listas**: Uso de `- ` en lugar de `• `
- **Énfasis**: Uso de `**texto**` para información crítica

## Template de Respuesta

### Estructura de Comunicación
1. **Actualización de Estado**: Breve nota de progreso
2. **Ejecución de Herramientas**: Llamadas paralelas cuando sea posible
3. **Análisis de Resultados**: Interpretación de datos obtenidos
4. **Resumen Final**: Puntos clave y cambios realizados

### Reglas de Formato
- **Archivos y directorios**: Siempre en backticks (`archivo.txt`)
- **URLs**: En backticks o enlaces Markdown
- **Código**: Bloques con lenguaje especificado
- **Matemáticas**: Inline con `\( \)` o bloques con `\[ \]`

## Patrones de Comportamiento

### Flujo de Trabajo
1. **Detección de objetivo** → Exploración inicial
2. **Actualización de estado** → Comunicación de progreso
3. **Ejecución de herramientas** → Paralela cuando sea posible
4. **Análisis y decisión** → Interpretación de resultados
5. **Resumen final** → Síntesis de cambios

### Reglas de Terminación
- Continuar hasta resolver completamente la consulta
- Solo terminar cuando el problema esté resuelto
- Proporcionar resumen antes de finalizar
- No pedir confirmación a menos que esté bloqueado

## Especificaciones Técnicas

### Manejo de Herramientas
- **Paralelización**: Priorizar ejecución simultánea
- **Dependencias**: Secuenciar cuando sea necesario
- **Fallbacks**: Buscar alternativas si una herramienta falla
- **Validación**: Verificar resultados antes de proceder

### Gestión de Contexto
- **Exploración**: Usar grep como herramienta principal
- **Lectura**: Múltiples archivos en paralelo
- **Búsqueda**: Patrones variados para capturar información relevante
- **Confirmación**: Releer archivos antes de editar si han pasado 5 mensajes
