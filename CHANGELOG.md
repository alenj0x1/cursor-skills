# Changelog

Todos los cambios notables de este repositorio se documentan en este archivo.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) e incluye qué skills se ven afectadas en cada release.

## [Unreleased]

### Changed

- ai-professor: checklist de calidad, plan previo por módulo (AskQuestion), README con mínimos por sección, prácticas con pasos numerados, playground con comentarios en español
- repo: instalación rápida con `npx skills add` en README

**Skills:** ai-professor

## [0.2.0] - 2026-05-23

### Added

- ai-professor: flujo `AskQuestion` interactivo (diagnóstico, retorno de sesión, validación de ruta de aprendizaje, refuerzo A/B, verificación de comprensión)
- ai-professor: references `interactive-questions`, `navigation-conventions`, `playground-template`, `practice-template`, `welcome-messages`
- ai-professor: estructura `solutions/` y `playground/` por módulo; placeholders de solución separados del enunciado
- ai-professor: pregunta de nombre del estudiante (`student_name`) al inicio del diagnóstico
- ai-professor: nomenclatura `ejemplo-XX` para archivos y títulos de ejemplos

### Changed

- ai-professor: mensajes de bienvenida conversacionales; saludo separado de preguntas interactivas
- ai-professor: enlaces relativos cruzados entre README, examples, practices, solutions, playground y PROGRESS.md
- ai-professor: título visible de PROGRESS.md pasa de `PROGRESS —` a `Ruta de aprendizaje — [Tema]`
- ai-professor: terminología currículo reemplazada por ruta de aprendizaje / aprendizaje
- ai-professor: ejemplos visibles en español (`Ejemplo`, no `Example`)
- repo: README actualizado con estructura de references e interactividad AskQuestion

**Skills:** ai-professor

## [0.1.0] - 2026-05-23

### Added

- ai-professor: skill inicial con módulos estructurados, PROGRESS.md, readme-template y progress-states
- repo: README de instalación y licencia MIT

**Skills:** ai-professor
