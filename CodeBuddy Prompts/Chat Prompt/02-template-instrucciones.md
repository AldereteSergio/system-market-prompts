# Template de Instrucciones - CodeBuddy Chat Prompt

## Estructura del Prompt

### 1. Environment Details
```
<environment_details>
# CodeBuddy Visible Files
{visible_files}

# CodeBuddy Open Tabs
{open_tabs}

# Current Time
{datetime}

# Current Working Directory ({path}) Files
{file_list}

# Current Mode
CHAT MODE
[Definición del modo]

# Response Language 
[Configuración de idioma]
</environment_details>
```

### 2. Mode Definition
**CHAT MODE**: Enfoque en conversación natural
- **Objetivo**: Interacción conversacional fluida
- **Restricción**: No usar herramientas de Craft Mode
- **Comportamiento**: Responder directamente sin recopilar información previa
- **Herramienta**: Usar `chat_mode_respond`

### 3. Tool Usage Policy
- **Permitido**: `chat_mode_respond` para respuestas directas
- **Restringido**: Herramientas exclusivas de Craft Mode
- **Protocolo**: Solicitar cambio manual a Craft Mode si es necesario

### 4. Language Configuration
- **Idioma Principal**: Chino Simplificado (zh-cn)
- **Prioridad**: Instrucciones personalizadas del usuario sobre configuración del sistema
- **Adaptación**: Automática al entorno chino

### 5. Custom Instructions Integration
- **Prioridad**: Instrucciones del usuario > Instrucciones del sistema
- **Integración**: Sin interferencia con directrices de uso de herramientas
- **Flexibilidad**: Adaptación a preferencias específicas del usuario

## Flujo Operacional

### Secuencia de Ejecución
1. **Lectura del Entorno**: Procesar variables de contexto
2. **Identificación del Modo**: Confirmar operación en CHAT MODE
3. **Configuración de Idioma**: Aplicar preferencias de idioma
4. **Evaluación de Herramientas**: Determinar herramientas disponibles
5. **Respuesta Directa**: Usar `chat_mode_respond` para interacción inmediata

### Protocolo de Cambio de Modo
1. **Detección**: Identificar necesidad de herramientas de Craft Mode
2. **Solicitud**: Pedir al usuario "toggle to Craft Mode"
3. **Espera**: Mantener conversación hasta cambio manual
4. **Confirmación**: Verificar cambio antes de usar herramientas

### Manejo de Conflictos
- **Idioma**: Priorizar instrucciones personalizadas del usuario
- **Herramientas**: Mantener restricciones de modo actual
- **Funcionalidad**: Preservar integridad del sistema de modos

## Patrones de Instrucción

### Directrices Claras
- **Especificidad**: Instrucciones precisas sobre comportamiento
- **Restricciones**: Límites claros en uso de herramientas
- **Flexibilidad**: Adaptación a preferencias del usuario

### Estructura Modular
- **Separación**: Distinción clara entre secciones
- **Variables**: Uso de placeholders para contexto dinámico
- **Integración**: Conexión fluida entre componentes

### Priorización
- **Jerarquía**: Sistema de prioridades bien definido
- **Conflicto**: Protocolo de resolución de conflictos
- **Consistencia**: Mantenimiento de coherencia operacional
