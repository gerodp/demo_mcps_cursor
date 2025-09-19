# 🚀 Demo MCPs - Cursor Integrations

Una demostración práctica de las capacidades de integración de Cursor con herramientas de desarrollo mediante Model Context Protocols (MCPs).

🌐 **[Demo Web](https://gerodp.github.io/demo_mcps/)** 

## 📋 Descripción

Este proyecto demuestra cómo integrar Cursor IDE con servicios externos como Jira y Bitbucket utilizando MCPs, incluyendo configuraciones de reglas personalizadas y comandos automatizados. Incluye tanto ejemplos prácticos como una presentación web interactiva sobre las novedades de Cursor y modelos de IA.

## 🏗️ Estructura del Proyecto

```
demoMCPs/
├── 📁 .cursor/                    # Configuraciones de Cursor
│   ├── 📁 rules/                  # Reglas personalizadas de Cursor
│   │   ├── jira.mdc              # Configuración de Jira
│   │   └── bitbucket.mdc         # Configuración de Bitbucket
│   └── 📁 commands/               # Comandos personalizados
│       └── createpr.md           # Comando para crear PRs
├── 📁 web_demo/                   # Demo web interactiva
│   ├── index.html                # Presentación sobre MCPs
│   ├── script.js                 # Lógica de navegación
│   └── styles.css                # Estilos modernos
├── 📄 bitbucket_examples.md       # Ejemplos de comandos Bitbucket
├── 📄 jira_examples.md           # Ejemplos de comandos Jira
├── 📄 cursor_misc.md             # Comandos misceláneos
└── 📄 README.md                  # Este archivo
```

## 🛠️ Características Principales

### 🔗 Integraciones MCPs

#### Jira MCP
- **Operaciones soportadas**:
  - ✅ Crear, editar y transicionar tickets
  - ✅ Buscar issues con JQL
  - ✅ Gestionar comentarios y subtasks
  - ✅ Administrar proyectos y sprints

#### Bitbucket MCP
- **Operaciones soportadas**:
  - ✅ Listar repositorios y pull requests
  - ✅ Crear, mergear y gestionar PRs
  - ✅ Revisar diferencias y actividad
  - ✅ Configurar modelos de branching

### 📏 Cursor Rules

El proyecto incluye reglas personalizadas que automatizan configuraciones específicas:

- **Jira Rules** (`jira.mdc`): Configuración automática del proyecto
- **Bitbucket Rules** (`bitbucket.mdc`): Configuración del workspace y repositorio
- **Estándares de código**: Uso de espacios en lugar de tabs para Python

### 🎯 Comandos Personalizados

- **Crear PR** (`createpr.md`): Comando completo para generar pull requests automáticamente
  - Análisis de rama actual
  - Recopilación de cambios
  - Generación automática de título y descripción
  - Confirmación antes de crear

## 🌐 Demo Web Interactiva

La carpeta `web_demo/` contiene una presentación web moderna que explica:

1. **¿Qué son los MCPs?** - Introducción a Model Context Protocols
2. **Herramientas de Jira** - 25+ funciones disponibles
3. **Herramientas de Bitbucket** - 15+ operaciones de repositorio
4. **Cursor Rules** - Personalización del comportamiento de IA
5. **Comandos de Cursor** - Automatización de tareas complejas

## 🚀 Comenzar

### Prerrequisitos

1. **Cursor IDE** instalado
2. **Acceso a Jira**
3. **Acceso a Bitbucket**
4. **MCPs configurados** en Cursor

### Instalación

1. Clona este repositorio:
```bash
git clone <repository-url>
cd demoMCPs
```

2. Abre el proyecto en Cursor IDE

3. Las reglas y comandos se cargarán automáticamente

## 📚 Ejemplos de Uso

### Gestión de Jira
```
# Crear tickets para un proyecto
"Estoy planificando mi proyecto y quiero crear los tickets:
* Diseñar el nuevo estilo
* Definir las secciones y el contenido
* Crear la home..."

# Gestionar estados
"asígname el ticket CPG-26 y ponlo a En Curso"

# Añadir comentarios
"Añade un comentario al ticket X con el resultado de ejecutar el comando Date"
```

### Gestión de Bitbucket
```
# Listar repositorios
"lista los repositorios"

# Gestionar pull requests
"lista las PRs abiertas"
"crea una pull request con estos cambios, incluyendo un resumen detallado"
```

## 🎯 Casos de Uso

### Para Desarrolladores
- **Automatización de flujo de trabajo**: Desde código hasta deployment
- **Gestión de proyectos**: Sincronización entre código y tickets
- **Revisión de código**: PRs automáticas con contexto

### Para Teams
- **Estándares consistentes**: Rules que aseguran calidad
- **Procesos automatizados**: Menos trabajo manual
- **Mejor colaboración**: Integración entre herramientas

## 🔧 Configuración Avanzada

### Personalizar Reglas de Cursor

Edita los archivos en `.cursor/rules/` para adaptar a tu proyecto:

```markdown
---
description: Mi configuración personalizada
globs: ["*.js", "*.ts"]
alwaysApply: true
---

Usar siempre TypeScript strict mode
Preferir functional components en React
```

### Añadir Comandos Personalizados

Crea archivos `.md` en `.cursor/commands/` con instrucciones específicas:

```markdown
# Mi Comando Personalizado

## Objetivo
Descripción de lo que hace el comando

## Instrucciones
1. Paso 1
2. Paso 2
3. Paso 3
```
