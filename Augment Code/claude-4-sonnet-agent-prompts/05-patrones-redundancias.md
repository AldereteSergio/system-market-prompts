# Patrones y Redundancias - Augment Code

## Patrones Identificados

### 1. Patrón de Información Preliminar
**Frecuencia**: Múltiples menciones
**Ubicaciones**: 
- Sección "Preliminary tasks"
- Sección "Making edits"
- Sección "Planning and Task Management"

**Descripción**: Instrucción repetida de recolección de información antes de cualquier acción

### 2. Patrón Conservador
**Frecuencia**: 3 menciones explícitas
**Ubicaciones**:
- "be very conservative and respect the codebase"
- "the more conservative you should be"
- "Conservative Actions"

**Descripción**: Enfoque conservador repetido en múltiples contextos

### 3. Patrón de Permisos Explícitos
**Frecuencia**: 2 secciones principales
**Ubicaciones**:
- "Following instructions"
- "Package Management"

**Descripción**: Requerimiento de autorización explícita para acciones críticas

### 4. Patrón de Testing
**Frecuencia**: 2 menciones
**Ubicaciones**:
- Sección "Testing"
- Sección "Final"

**Descripción**: Enfoque en testing como parte del proceso

## Redundancias Detectadas

### 1. Redundancia en Information Gathering
**Problema**: La instrucción de recolección de información aparece en:
- Líneas 15-17: "Call information-gathering tools"
- Líneas 18-19: "use the codebase-retrieval tool"
- Líneas 20-21: "use the git-commit-retrieval tool"
- Líneas 65-67: "ALWAYS first call the codebase-retrieval tool"

**Impacto**: Confusión sobre cuándo usar cada herramienta

### 2. Redundancia en Conservative Approach
**Problema**: El enfoque conservador se menciona múltiples veces:
- Línea 67: "be very conservative and respect the codebase"
- Línea 95: "the more conservative you should be"
- Línea 96: "Conservative Actions"

**Impacto**: Repetición innecesaria de la misma instrucción

### 3. Redundancia en Package Management
**Problema**: La regla de usar gestores de paquetes se repite:
- Línea 75: "Always use appropriate package managers"
- Línea 77: "Always use package managers"
- Línea 89: "Only edit package files directly when..."

**Impacto**: Énfasis excesivo en una sola regla

### 4. Redundancia en Task Management
**Problema**: Instrucciones sobre gestión de tareas dispersas:
- Líneas 25-60: Sección completa de task management
- Líneas 150-160: Referencias adicionales en "Final"

**Impacto**: Información fragmentada sobre el mismo tema

## Patrones Estructurales

### 1. Estructura Jerárquica
- **Nivel 1**: Secciones principales (# Role, # Identity, etc.)
- **Nivel 2**: Subsecciones con instrucciones específicas
- **Nivel 3**: Ejemplos y casos de uso

### 2. Patrón de Ejemplos
- **Formato**: Instrucción + ejemplo concreto
- **Ejemplo**: XML tags con sintaxis específica
- **Ejemplo**: Comandos de package managers por lenguaje

### 3. Patrón de Condiciones
- **Formato**: "When to use" + "Consider using"
- **Aplicación**: Task management, package management

## Inconsistencias Detectadas

### 1. Inconsistencia en Fechas
- **Problema**: Fecha ficticia "1848-15-03" vs fecha real de documentación
- **Impacto**: Confusión sobre la actualidad del prompt

### 2. Inconsistencia en Nomenclatura
- **Problema**: "information-gathering tools" vs "codebase-retrieval tool"
- **Impacto**: Confusión sobre si son herramientas separadas o relacionadas

### 3. Inconsistencia en Estados de Tareas
- **Problema**: Estados descritos como [ ], [/], [-], [x] pero también como "COMPLETE", "IN_PROGRESS"
- **Impacto**: Confusión sobre la nomenclatura correcta

## Optimizaciones Sugeridas

### 1. Consolidación de Information Gathering
- Unificar las instrucciones de recolección de información
- Clarificar la jerarquía de herramientas

### 2. Eliminación de Redundancias
- Consolidar las menciones del enfoque conservador
- Unificar las reglas de package management

### 3. Reorganización Estructural
- Agrupar todas las instrucciones de task management
- Consolidar las referencias a testing

### 4. Estandarización de Nomenclatura
- Unificar la nomenclatura de estados de tareas
- Clarificar la relación entre herramientas de información
