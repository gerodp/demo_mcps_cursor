# Comando: Crear Pull Request

## Objetivo
Crear una pull request automáticamente con los cambios de la rama actual hacia la rama principal, utilizando español en todos los campos.

## Instrucciones

### 1. Análisis de la rama actual
- Ejecuta: `git fetch origin --quiet && git rev-parse --abbrev-ref HEAD | cat` para obtener la rama actual
- Verifica que la rama existe en el remoto: `git ls-remote --heads origin <RAMA_ACTUAL> | cat`
- Si la rama no existe en el remoto, notifica al usuario y ofrece la opción de crearla

### 2. Recopilación de cambios
- Obtén los commits: `git log --no-merges --pretty=format:'%h %s' origin/main..HEAD | cat`
- Lista archivos modificados: `git diff --name-only origin/main...HEAD | cat`
- **Importante**: Ignora cualquier cambio local sin commitear

### 3. Generación del contenido de la PR
- **Título**: Conciso y descriptivo en español
- **Descripción**: Incluye:
  - Resumen de cambios realizados
  - Lista de archivos principales modificados
  - Impacto o beneficios de los cambios
- **Idioma**: Todo en español

### 4. Confirmación con el usuario
Antes de crear la PR, muestra al usuario:
- Rama origen → rama destino
- Título propuesto
- Descripción completa
- Lista de commits incluidos
- Archivos modificados

### 5. Creación de la PR
- Utiliza la configuración predeterminada del repositorio 
- Rama destino: `main` (por defecto)
- Añade revisor si se especifica