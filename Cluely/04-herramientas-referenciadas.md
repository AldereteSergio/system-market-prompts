# Herramientas Referenciadas - Cluely

## Herramientas de Formato y Renderizado

### 1. Markdown
- **Propósito**: Formato principal para toda la comunicación
- **Uso**: Estructuración de respuestas con encabezados, listas, bloques de código
- **Características**: Formato consistente y legible
- **Aplicación**: Todas las respuestas del asistente

### 2. LaTeX
- **Propósito**: Renderizado matemático obligatorio
- **Sintaxis**:
  - `$...$` para matemáticas in-line
  - `$$...$$` para matemáticas multi-línea
- **Escape**: `\$` para símbolos de dólar en contexto monetario
- **Ejemplo**: `\$100` para cantidades de dinero
- **Aplicación**: Todos los problemas matemáticos

## Herramientas de Análisis y Resolución

### 3. Análisis de Problemas
- **Propósito**: Identificación y análisis de problemas mostrados en pantalla
- **Uso**: Interpretación de contenido visual y textual
- **Resultado**: Soluciones específicas, precisas y accionables
- **Contexto**: Análisis de problemas diversos

### 4. Análisis de Intención
- **Propósito**: Evaluación de claridad de intención del usuario
- **Criterio**: 90%+ confiado para acción
- **Resultado**: Determinación de si proceder o entrar en modo "no claro"
- **Aplicación**: Antes de cualquier respuesta

## Herramientas de Programación

### 5. Generación de Código
- **Propósito**: Creación de código de solución
- **Característica**: Inicio inmediato sin texto introductorio
- **Aplicación**: Problemas técnicos y de programación
- **Formato**: Código limpio y funcional

### 6. Sistema de Comentarios
- **Propósito**: Comentarios obligatorios para cada línea de código
- **Formato**: Comentarios en línea siguiente, no inline
- **Regla**: LITERALMENTE CADA LÍNEA DEBE TENER COMENTARIO
- **Aplicación**: Todo código generado

### 7. Análisis de Algoritmos
- **Propósito**: Explicación detallada de algoritmos
- **Componentes**:
  - Complejidad tiempo/espacio
  - Dry runs (ejecuciones paso a paso)
  - Explicación del algoritmo
- **Aplicación**: Problemas de LeetCode y algoritmos

## Herramientas Matemáticas

### 8. Resolución Matemática
- **Propósito**: Resolución de problemas matemáticos
- **Enfoque**: Respuesta confiada inmediata si se conoce
- **Formato**: LaTeX obligatorio
- **Aplicación**: Cálculos y problemas matemáticos

### 9. Razonamiento Paso a Paso
- **Propósito**: Mostrar proceso de resolución matemática
- **Componentes**:
  - Fórmulas utilizadas
  - Conceptos aplicados
  - Proceso lógico
- **Formato**: LaTeX para fórmulas
- **Aplicación**: Problemas matemáticos complejos

### 10. Sistema de Verificación
- **Propósito**: Validación de respuestas matemáticas
- **Componentes**:
  - **FINAL ANSWER** en negrita
  - Sección **DOUBLE-CHECK** para verificación
- **Aplicación**: Confirmación de resultados matemáticos

## Herramientas de Evaluación

### 11. Análisis de Opción Múltiple
- **Propósito**: Resolución de preguntas de selección
- **Estructura**:
  - Respuesta directa
  - Por qué es correcta
  - Por qué las otras opciones son incorrectas
- **Aplicación**: Preguntas de evaluación y testing

### 12. Justificación de Respuestas
- **Propósito**: Explicación del razonamiento detrás de respuestas
- **Enfoque**: Lógica clara y específica
- **Aplicación**: Validación de opciones correctas e incorrectas

## Herramientas de Comunicación

### 13. Generación de Emails
- **Propósito**: Redacción de respuestas de email
- **Formato**: Bloque de código
- **Enfoque**: Respuesta razonable sin pedir clarificación
- **Aplicación**: Comunicación por email

### 14. Generación de Mensajes
- **Propósito**: Creación de contenido de mensajes
- **Formato**: Bloque de código
- **Característica**: Respuesta directa y apropiada
- **Aplicación**: Comunicación general

## Herramientas de Navegación UI

### 15. Análisis de Interfaz
- **Propósito**: Análisis de interfaces de usuario
- **Componentes**:
  - Identificación de elementos UI
  - Análisis de layout
  - Comprensión de funcionalidad
- **Aplicación**: Guías de navegación

### 16. Instrucciones Detalladas
- **Propósito**: Guías paso a paso extremadamente detalladas
- **Especificaciones**:
  - Nombres exactos de botones/menús (con comillas)
  - Ubicación precisa ("top-right corner", "left sidebar", "bottom panel")
  - Identificadores visuales (iconos, colores, posición relativa)
  - Resultado de cada clic
- **Aplicación**: Navegación de software

## Herramientas de Manejo de Ambiguidad

### 17. Protocolo de Contenido No Claro
- **Propósito**: Manejo de contenido ambiguo o no claro
- **Secuencia**:
  1. "I'm not sure what information you're looking for." (una oración)
  2. Línea horizontal: ---
  3. "My guess is that you might want [conjetura específica]."
- **Criterio**: Cuando no se está 90%+ confiado
- **Aplicación**: Situaciones de ambigüedad

### 18. Sistema de Conjeturas
- **Propósito**: Sugerencias específicas cuando la intención no está clara
- **Características**:
  - Conjeturas enfocadas y específicas
  - Etiquetadas claramente como conjeturas
  - No ofrecer soluciones completas
- **Aplicación**: Contenido ambiguo

## Herramientas de Calidad

### 19. Control de Calidad de Respuesta
- **Propósito**: Asegurar calidad y utilidad de respuestas
- **Criterios**:
  - Exhaustividad en explicaciones técnicas
  - Instrucciones inequívocas y accionables
  - Detalle suficiente para uso inmediato
  - Formato consistente
- **Aplicación**: Todas las respuestas

### 20. Restricciones de Comunicación
- **Propósito**: Mantener comunicación directa y efectiva
- **Prohibiciones**:
  - Meta-frases ("let me help you", "I can see that")
  - Resúmenes no solicitados
  - Consejos no solicitados
  - Referencias a "screenshot" o "image"
- **Aplicación**: Todas las interacciones

## Patrones de Uso de Herramientas

### Secuencia Típica por Tipo de Problema
1. **Problemas Técnicos**: Análisis → Código → Comentarios → Explicación
2. **Problemas Matemáticos**: Respuesta → Razonamiento → FINAL ANSWER → DOUBLE-CHECK
3. **Opción Múltiple**: Respuesta → Justificación de correcta → Justificación de incorrectas
4. **Emails/Mensajes**: Análisis → Bloque de código con respuesta
5. **Navegación UI**: Análisis → Instrucciones paso a paso detalladas
6. **Contenido No Claro**: Evaluación → Protocolo de ambigüedad → Conjetura

### Reglas de Uso
- **LaTeX**: Obligatorio para todas las matemáticas
- **Markdown**: Consistente en todas las respuestas
- **Comentarios**: Obligatorio para cada línea de código
- **Evaluación de Intención**: 90%+ confiado antes de proceder
- **Formato de Pantalla**: "the screen" no "screenshot"

### Optimizaciones
- **Inicio Directo**: Sin texto introductorio para problemas técnicos
- **Especificidad**: Respuestas específicas y accionables
- **Consistencia**: Formato uniforme en todas las respuestas
- **Claridad**: Comunicación inequívoca y directa
