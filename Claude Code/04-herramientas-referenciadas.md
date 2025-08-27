# Herramientas Referenciadas - Claude Code

## Herramientas de Búsqueda y Análisis

### 1. Task Tool
- **Propósito**: Herramienta preferida para búsqueda de archivos
- **Uso**: Reducir uso de contexto en búsquedas de archivos
- **Contexto**: Herramienta especializada para búsquedas eficientes
- **Optimización**: Minimización de tokens de contexto

### 2. WebFetch
- **Propósito**: Consultar documentación y recursos web
- **Uso**: 
  - Consultar documentación de Claude Code
  - Obtener información de recursos web
  - Manejar redirecciones automáticamente
- **URLs Soportadas**: 
  - https://docs.anthropic.com/en/docs/claude-code
  - Sub-pages: overview, quickstart, memory, common-workflows, etc.
- **Manejo de Redirecciones**: Hacer nueva petición automáticamente

### 3. Search Tools
- **Propósito**: Herramientas de búsqueda extensivas
- **Uso**: 
  - Entender el codebase
  - Analizar consultas del usuario
  - Búsqueda paralela y secuencial
- **Contexto**: Uso extensivo para comprensión del proyecto

## Herramientas de Gestión de Tareas

### 4. TodoWrite Tools
- **Propósito**: Sistema de gestión y planificación de tareas
- **Uso**:
  - Planificar tareas complejas
  - Desglosar tareas grandes en pasos pequeños
  - Dar visibilidad del progreso al usuario
  - Tracking de tareas completadas
- **Frecuencia**: Uso MUY frecuente
- **Crítico**: No usar puede resultar en olvido de tareas importantes

### 5. Task Management
- **Propósito**: Tracking y visibilidad del progreso
- **Uso**:
  - Marcar tareas como completadas inmediatamente
  - No agrupar múltiples tareas antes de marcarlas
  - Dar visibilidad del estado actual
- **Estados**: in_progress, completed

### 6. Progress Tracking
- **Propósito**: Seguimiento de tareas completadas
- **Uso**: 
  - Actualización inmediata de estado
  - Visibilidad del progreso
  - Comunicación del avance al usuario

## Herramientas de Ejecución

### 7. Bash
- **Propósito**: Ejecución de comandos del sistema operativo
- **Uso**:
  - Comandos de linting y typechecking
  - Ejecución de tests
  - Comandos de construcción
  - Comandos del sistema
- **Paralelización**: Ejecutar múltiples comandos en paralelo
- **Explicación**: Explicar comandos no triviales al usuario

### 8. Linting Tools
- **Propósito**: Validación de código
- **Comandos**:
  - `npm run lint`: Para JavaScript/TypeScript
  - `ruff`: Para Python
  - Otros específicos por lenguaje
- **Uso**: Ejecutar después de completar tareas
- **Crítico**: Ejecutar si están disponibles

### 9. Typechecking Tools
- **Propósito**: Verificación de tipos
- **Comandos**:
  - `npm run typecheck`: Para TypeScript
  - Otros específicos por lenguaje
- **Uso**: Validación post-cambios
- **Crítico**: Ejecutar si están disponibles

### 10. Testing Frameworks
- **Propósito**: Ejecución de tests
- **Uso**:
  - Verificar soluciones implementadas
  - No asumir framework específico
  - Consultar README o codebase para determinar enfoque
- **Contexto**: Verificación de calidad del código

## Herramientas de Gestión de Paquetes

### 11. Package Managers
- **npm**: Node.js package manager
- **package.json**: Configuración de dependencias Node.js
- **cargo.toml**: Configuración de dependencias Rust
- **Otros**: Gestores específicos por lenguaje
- **Uso**: Verificar disponibilidad de librerías antes de usar

## Herramientas de Control de Versiones

### 12. Git
- **Propósito**: Control de versiones
- **Funcionalidades**:
  - Git Status: Estado del repositorio
  - Git Commits: Historial de commits
  - Branch Management: Gestión de ramas
- **Restricción**: NO hacer commits a menos que se pida explícitamente
- **Crítico**: Solo commit cuando se pida explícitamente

## Herramientas de Documentación

### 13. Help System
- **Comando**: `/help`
- **Propósito**: Obtener ayuda con Claude Code
- **Feedback**: https://github.com/anthropics/claude-code/issues

### 14. Documentation Access
- **URL Principal**: https://docs.anthropic.com/en/docs/claude-code
- **Sub-pages Disponibles**:
  - overview, quickstart, memory
  - common-workflows, ide-integrations, mcp
  - github-actions, sdk, troubleshooting
  - third-party-integrations, amazon-bedrock
  - google-vertex-ai, corporate-proxy, llm-gateway
  - devcontainer, iam, security, monitoring-usage
  - costs, cli-reference, interactive-mode
  - slash-commands, settings, hooks

## Herramientas de Referencia de Código

### 15. Code References
- **Formato**: `file_path:line_number`
- **Propósito**: Permitir navegación fácil al código fuente
- **Ejemplo**: `src/services/process.ts:712`

## Patrones de Uso de Herramientas

### Secuencia Típica
1. **Planificación**: TodoWrite Tools para tareas complejas
2. **Búsqueda**: Task Tool y Search Tools para entender codebase
3. **Implementación**: Bash y herramientas de desarrollo
4. **Verificación**: Linting, Typechecking, Testing
5. **Completación**: Marcar tareas como completadas

### Reglas de Uso
- **Task Tool**: Preferir para búsqueda de archivos
- **WebFetch**: Para documentación y recursos web
- **Batching**: Agrupar llamadas de herramientas
- **Paralelización**: Comandos bash en paralelo
- **TodoWrite**: Usar MUY frecuentemente
- **Git**: Solo commits explícitos

### Optimizaciones
- **Token Minimization**: Minimizar tokens de salida
- **Context Optimization**: Optimizar uso de contexto
- **Batching**: Agrupar llamadas relacionadas
- **Parallel Execution**: Ejecutar comandos en paralelo
