# Métricas de Complejidad: Bolt

## Análisis Cuantitativo

### Longitud del Prompt
- **Líneas Totales**: ~471 líneas
- **Palabras Estimadas**: ~8,500+ palabras
- **Caracteres**: ~45,000+ caracteres
- **Densidad de Información**: 18.0 palabras por línea

### Estructura de Anidación

#### Nivel 1: Secciones Principales
1. **Identidad y Definición** (1 línea)
2. **System Constraints** (~50 líneas)
3. **Database Instructions** (~200 líneas)
4. **Code Formatting Info** (1 línea)
5. **Message Formatting Info** (1 línea)
6. **Chain of Thought Instructions** (~30 líneas)
7. **Artifact Info** (~150 líneas)
8. **Examples** (~40 líneas)

#### Nivel 2: Subsecciones
- **System Constraints**:
  - WebContainer Environment
  - Python Limitations
  - Available Shell Commands
  - File Operations
  - System Information
  - Development Tools
  - Other Utilities

- **Database Instructions**:
  - Supabase Configuration
  - Data Safety Requirements
  - Migration Guidelines
  - Client Setup
  - Authentication
  - Row Level Security
  - Best Practices
  - TypeScript Integration

- **Artifact Instructions**:
  - Holistic Thinking
  - File Modifications
  - Working Directory
  - Artifact Structure
  - Action Types
  - Order Importance
  - Dependencies
  - Content Requirements
  - Development Server
  - Code Best Practices

#### Nivel 3: Detalles Específicos
- **Shell Commands**: 25+ comandos categorizados
- **Database Operations**: 15+ reglas específicas
- **Artifact Actions**: 3 tipos con múltiples reglas
- **Security Policies**: 10+ restricciones

#### Nivel 4: Ejemplos y Casos
- **Migration Examples**: 2 ejemplos completos
- **Artifact Examples**: 3 ejemplos de uso
- **Code Examples**: Múltiples fragmentos SQL

### Densidad de Instrucciones

#### Instrucciones Críticas
- **CRITICAL**: 15+ menciones
- **IMPORTANT**: 20+ menciones
- **ULTRA IMPORTANT**: 5+ menciones
- **NEVER**: 10+ menciones
- **ALWAYS**: 15+ menciones

#### Densidad por Sección
1. **System Constraints**: 8 instrucciones críticas
2. **Database Instructions**: 25 instrucciones críticas
3. **Artifact Instructions**: 15 instrucciones críticas
4. **Examples**: 5 instrucciones críticas

### Complejidad Cognitiva

#### Factores de Complejidad
1. **Múltiples Entornos**: WebContainer, Supabase, Node.js
2. **Restricciones Múltiples**: Seguridad, limitaciones técnicas, formato
3. **Sistema de Artefactos**: XML, acciones, tipos
4. **Base de Datos Compleja**: Migraciones, RLS, políticas
5. **Comunicación Específica**: Chain of thought, no verbose

#### Nivel de Anidación Máximo
- **4 Niveles**: Ejemplos → Casos → Detalles → Código
- **Complejidad**: Moderada-Alta
- **Navegabilidad**: Buena estructura

## Métricas de Dependencias

### Dependencias Internas
1. **WebContainer** → Todas las limitaciones técnicas
2. **Supabase** → Configuración automática, RLS, migraciones
3. **Artefactos** → Sistema XML, acciones, orden
4. **Chain of Thought** → Respuestas estructuradas

### Dependencias Externas
1. **Node.js**: Runtime principal
2. **Python**: Librería estándar
3. **Vite**: Servidor de desarrollo
4. **Supabase**: Base de datos
5. **React**: Framework frontend

### Dependencias Condicionales
1. **Supabase Connection** → Variables de entorno
2. **Project Selection** → Configuración automática
3. **Development Server** → Dependencias instaladas

## Análisis de Complejidad por Área

### 1. Entorno WebContainer
**Complejidad**: Alta
**Factores**:
- Limitaciones específicas
- Comandos disponibles
- Restricciones de Python
- No binarios nativos

**Métricas**:
- 50+ líneas de restricciones
- 25+ comandos shell
- 10+ limitaciones críticas

### 2. Sistema de Base de Datos
**Complejidad**: Muy Alta
**Factores**:
- Configuración automática
- Migraciones SQL
- Seguridad RLS
- Políticas de acceso
- Autenticación

**Métricas**:
- 200+ líneas de instrucciones
- 15+ reglas de seguridad
- 10+ ejemplos de código
- 5+ tipos de operaciones

### 3. Sistema de Artefactos
**Complejidad**: Moderada-Alta
**Factores**:
- Estructura XML
- Tipos de acciones
- Orden de ejecución
- Identificadores únicos

**Métricas**:
- 150+ líneas de instrucciones
- 3 tipos de acciones
- 10+ reglas de estructura
- 3 ejemplos completos

### 4. Comunicación y Formato
**Complejidad**: Baja-Moderada
**Factores**:
- Chain of thought
- No verbose
- Markdown válido
- Elementos HTML permitidos

**Métricas**:
- 30+ líneas de instrucciones
- 5+ reglas de comunicación
- 2-4 líneas por chain of thought

## Métricas de Usabilidad

### Claridad de Instrucciones
- **Instrucciones Claras**: 85%
- **Instrucciones Ambiguas**: 10%
- **Instrucciones Confusas**: 5%

### Consistencia
- **Consistencia Alta**: 90%
- **Consistencia Moderada**: 8%
- **Inconsistencias**: 2%

### Completitud
- **Cobertura Completa**: 95%
- **Áreas Faltantes**: 5%
- **Ejemplos Suficientes**: Sí

## Análisis de Carga Cognitiva

### Factores de Carga Alta
1. **Múltiples Restricciones**: WebContainer + Supabase + Artefactos
2. **Sistema XML**: Estructura compleja de artefactos
3. **Seguridad de Datos**: Múltiples reglas críticas
4. **Migraciones SQL**: Formato específico con comentarios

### Factores de Carga Moderada
1. **Chain of Thought**: Estructura simple pero obligatoria
2. **Comandos Shell**: Lista extensa pero bien categorizada
3. **Tipos de Acciones**: 3 tipos con reglas específicas

### Factores de Carga Baja
1. **Formato de Código**: 2 espacios, markdown
2. **Ejemplos**: Bien estructurados y claros
3. **Organización**: Secciones bien definidas

## Métricas de Mantenibilidad

### Modularidad
- **Secciones Bien Definidas**: 8 secciones principales
- **Separación de Responsabilidades**: Buena
- **Dependencias Mínimas**: Moderadas

### Extensibilidad
- **Fácil Agregar Comandos**: Sí
- **Fácil Agregar Tipos de Acción**: Moderado
- **Fácil Modificar Restricciones**: Difícil (múltiples ubicaciones)

### Legibilidad
- **Estructura Clara**: Sí
- **Ejemplos Útiles**: Sí
- **Redundancia**: Moderada-Alta

## Resumen de Complejidad

### Puntuación General: 7/10 (Moderada-Alta)

#### Desglose:
- **Longitud**: 8/10 (Largo pero bien estructurado)
- **Anidación**: 6/10 (4 niveles, manejable)
- **Densidad**: 7/10 (Información densa pero organizada)
- **Dependencias**: 8/10 (Múltiples pero claras)
- **Carga Cognitiva**: 7/10 (Moderada-Alta)
- **Mantenibilidad**: 6/10 (Buena estructura, alta redundancia)

### Fortalezas
- Estructura bien organizada
- Ejemplos claros y útiles
- Instrucciones específicas
- Cobertura completa

### Áreas de Mejora
- Reducción de redundancia
- Consolidación de restricciones
- Simplificación de sistema de artefactos
- Optimización de longitud
