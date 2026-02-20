# agents.md - Guía para Agentes de IA

## Información del Proyecto

**Nombre:** base-template **Automatización:** Taskfile  
**Documentación:** Sistema basado en templates (gomplate)

## Arquitectura Clave

## Estructura del Proyecto

### Directorios Principales

```
base-template/
├── docs/                  # Documentación
│   ├── usage.md           # Guía de uso
│   ├── examples/          # Ejemplos de código
│   ├── contributing.md    # Guía de contribución
│   └── path-aliases.md    # Guía de path aliases
├── provision/             # Templates y generadores
│   ├── generators/        # Configuraciones
│   │   └── README.yaml    # Configuración README
│   └── templates/         # Templates
│       └── README.tpl.md  # Template README
├── .ci/linters/           # Configuración de linters
│   ├── .eslintrc.js       # Configuración ESLint
│   └── prettier.config.cjs # Configuración Prettier
```

## Sistema de Documentación

### Generación Automática

**Archivos clave:**

- `provision/generators/README.yaml` → Configuración central
- `provision/templates/README.tpl.md` → Template README
- `docs/usage.md` → Guía de uso principal
- `docs/examples/common.md` → Ejemplos de código

**Comando de generación:**

```bash
task readme  # Regenera README.md desde templates
```

**Características:**

- Badges automáticos para CI, versiones, tecnologías
- Secciones dinámicas desde archivos markdown
- Formato consistente con Prettier
- Integración con Taskfile

## Configuración de Herramientas

### ESLint (`.ci/linters/.eslintrc.js`)

- TypeScript con type-checking
- Reglas estrictas para promesas
- Sin `any` explícito
- Integración con Prettier

### Prettier (`.ci/linters/prettier.config.cjs`)

- Sin punto y coma
- Comillas dobles
- 2 espacios de indentación
- 100 caracteres por línea

### Taskfile (`Taskfile.yml`)

- Automatización de workflows
- Dependencias externas via includes
- Comandos unificados para desarrollo

## Convenciones de Desarrollo

## Workflow de Desarrollo

### Comandos Principales

**Inicialización:**

```bash
task --yes       # Confiar en Taskfiles externos
task setup       # Configurar entorno y dependencias
task environment # Preparar variables de entorno
```

**Mantenimiento:**

```bash
task upgrade      # Actualizar dependencias
task check        # Verificar dependencias
task --list       # Listar todos los comandos
```

### Variables de Entorno

**Archivos:**

- `.env` → Variables desarrollo (no commit)
- `.env.example` → Template para desarrollo

## Dependencias Clave

### Herramientas

- `task` → Automatización (Taskfile)
- `gomplate` → Generación de templates
- `uv` → Gestor de entornos Python
- `pre-commit` → Hooks Git

## Guías de Referencia

## Recursos Adicionales

**Documentación:**

- `README.md` → Visión general (generado)
- `docs/usage.md` → Guía de uso detallada
- `docs/contributing.md` → Guía de contribución

**Configuraciones:**

- `Taskfile.yml` → Automatización

---

_Última actualización: $(date)_  
_Mantener este archivo actualizado con cambios significativos en la arquitectura o herramientas del proyecto._
