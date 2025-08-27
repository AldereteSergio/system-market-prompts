# Herramientas Referenciadas - CodeBuddy Chat Prompt

## Herramientas Principales

### 1. chat_mode_respond
- **Propósito**: Herramienta específica para generar respuestas en modo chat
- **Uso**: Respuestas directas y conversacionales sin recopilación previa de información
- **Contexto**: Exclusiva del modo CHAT
- **Características**: Baja latencia, respuesta inmediata

### 2. Environment Variables
- **visible_files**: Lista de archivos visibles en el editor
- **open_tabs**: Pestañas actualmente abiertas
- **datetime**: Tiempo y fecha actual
- **file_list**: Archivos en el directorio de trabajo actual
- **path**: Ruta del directorio actual

## Herramientas de Contexto

### 3. Context Management
- **Propósito**: Gestión dinámica del contexto del entorno
- **Uso**: Proporcionar información contextual al asistente
- **Variables**: Procesamiento de placeholders dinámicos
- **Integración**: Conexión con el sistema de archivos

### 4. Language Detection
- **Propósito**: Detección automática del entorno de idioma
- **Uso**: Configuración automática del idioma de respuesta
- **Configuración**: Chino Simplificado (zh-cn) por defecto
- **Adaptación**: Cambio automático según el entorno

## Herramientas de Configuración

### 5. Custom Instructions System
- **Propósito**: Sistema de instrucciones personalizadas del usuario
- **Uso**: Priorización de preferencias del usuario sobre configuración del sistema
- **Integración**: Sin interferencia con directrices de herramientas
- **Flexibilidad**: Adaptación a necesidades específicas

### 6. Mode Management
- **Propósito**: Gestión del sistema de modos (Chat/Craft)
- **Uso**: Control de comportamiento según el modo activo
- **Restricciones**: Limitación de herramientas según modo
- **Transición**: Protocolo de cambio entre modos

## Herramientas de Comunicación

### 7. Response Formatting
- **Propósito**: Formateo de respuestas según el contexto
- **Uso**: Adaptación del formato según el idioma y modo
- **Características**: Soporte multiidioma
- **Integración**: Con sistema de detección de idioma

### 8. Tool Restriction System
- **Propósito**: Control de acceso a herramientas según modo
- **Uso**: Restricción de herramientas de Craft Mode en Chat Mode
- **Protocolo**: Solicitud de cambio manual de modo
- **Seguridad**: Aislamiento entre modos de operación

## Herramientas de Integración

### 9. File System Integration
- **Propósito**: Integración con el sistema de archivos del editor
- **Uso**: Acceso a archivos y directorios
- **Capacidades**: Lectura de archivos visibles y listado de directorios
- **Contexto**: Información del entorno de desarrollo

### 10. Tab Management
- **Propósito**: Gestión de pestañas abiertas en el editor
- **Uso**: Acceso a archivos abiertos actualmente
- **Integración**: Con sistema de archivos
- **Contexto**: Estado actual del editor

## Herramientas de Validación

### 11. Instruction Priority System
- **Propósito**: Sistema de priorización de instrucciones
- **Uso**: Resolución de conflictos entre instrucciones del sistema y del usuario
- **Jerarquía**: Usuario > Sistema
- **Aplicación**: En configuración de idioma y comportamiento

### 12. Mode Validation
- **Propósito**: Validación del modo de operación actual
- **Uso**: Confirmación de restricciones y capacidades
- **Aplicación**: Antes de usar herramientas específicas
- **Seguridad**: Prevención de uso incorrecto de herramientas

## Patrones de Uso

### Herramientas por Modo
- **Chat Mode**: `chat_mode_respond`, variables de contexto, detección de idioma
- **Craft Mode**: Referenciado pero no implementado en este prompt
- **Transición**: Protocolo de cambio manual entre modos

### Integración de Herramientas
- **Contexto**: Variables de entorno proporcionan información base
- **Idioma**: Sistema de detección y configuración automática
- **Modo**: Control de comportamiento y herramientas disponibles
- **Usuario**: Priorización de preferencias personalizadas

### Optimización de Uso
- **Eficiencia**: Respuestas directas sin recopilación previa
- **Contexto**: Uso eficiente de información disponible
- **Restricciones**: Respeto a límites de modo actual
- **Flexibilidad**: Adaptación a necesidades del usuario
