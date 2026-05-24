# cursor-skills

Colección personal de Agent Skills para Cursor que amplían las capacidades del asistente con flujos especializados.

## 📦 Instalación

Cada skill vive en su propia carpeta. Instala solo las que necesites.

### Instalación rápida (recomendada)

Con [skills](https://github.com/vercel-labs/skills) puedes instalar una skill directamente desde este repositorio:

```bash
npx skills add https://github.com/alenj0x1/cursor-skills --skill <skill>
```

Ejemplo:

```bash
npx skills add https://github.com/alenj0x1/cursor-skills --skill ai-professor
```

Reinicia Cursor o abre un chat nuevo para que detecte la skill.

### Instalación manual

#### 1. Obtener el repositorio

```bash
git clone https://github.com/alenj0x1/cursor-skills.git
```

También puedes descargar el ZIP desde GitHub si no usas Git.

#### 2. Copiar la skill

Copia la carpeta de la skill que quieras (por ejemplo, `ai-professor/`) a una de estas ubicaciones:


| Ámbito                         | Ruta                                                                             |
| ------------------------------ | -------------------------------------------------------------------------------- |
| Personal (todos tus proyectos) | `~/.cursor/skills/` en macOS/Linux, o `%USERPROFILE%\.cursor\skills\` en Windows |
| Por proyecto (solo ese repo)   | `.cursor/skills/` en la raíz del proyecto                                        |


Ejemplo en Windows (PowerShell):

```powershell
Copy-Item -Recurse .\cursor-skills\ai-professor $env:USERPROFILE\.cursor\skills\ai-professor
```

Ejemplo en macOS/Linux:

```bash
cp -r cursor-skills/ai-professor ~/.cursor/skills/ai-professor
```

#### 3. Verificar

La estructura final debe quedar así:

```
~/.cursor/skills/ai-professor/
├── SKILL.md
└── references/
    ├── interactive-questions.md
    ├── navigation-conventions.md
    ├── playground-template.md
    ├── practice-template.md
    ├── progress-states.md
    ├── readme-template.md
    └── welcome-messages.md
```

Reinicia Cursor o abre un chat nuevo para que detecte la skill.

## 🧠 Skills incluidas

### ai-professor

Convierte al agente en un profesor que enseña cualquier tema mediante módulos estructurados, ejemplos detallados, prácticas evaluadas y seguimiento de progreso en `PROGRESS.md`.

**Cuándo se activa:** cuando expresas intención de aprender un tema de forma estructurada, continuar un módulo, entregar una práctica o pedir feedback sobre tu avance.

**Frases que la disparan (ejemplos):**

- «Quiero aprender [tema]»
- «Enséñame [tema]»
- «Sé mi profesor»
- «Crea una ruta de aprendizaje para [tema]»
- «Arma los módulos para aprender [tema]»
- «Quiero estudiar [tema]»
- «ai-professor»

**Cómo usarla en Cursor:** escribe en el chat una de las frases anteriores, o adjunta la skill manualmente con `@` / `/` según tu versión de Cursor.

**Interactividad:** la skill usa la herramienta nativa `AskQuestion` de Cursor para el diagnóstico, validar la ruta de aprendizaje y otras decisiones — verás opciones clicables en lugar de preguntas solo en texto. Funciona de forma fiable en Plan mode; en Agent mode puede depender del modelo. Si no aparece el diálogo, añade esta regla global de usuario:

```
Use the AskQuestion tool for any interaction requiring user input like choosing between options, confirming a proposed action, or clarifying an ambiguous request.
```

Más info: [foro Cursor sobre AskQuestion en Agent mode](https://forum.cursor.com/t/allow-askquestion-tool-calls-in-agent-mode-or-any-mode/152517).

**Estructura:**

```
ai-professor/
├── SKILL.md                      # Instrucciones completas del agente
└── references/
    ├── interactive-questions.md  # Plantillas AskQuestion por fase
    ├── navigation-conventions.md
    ├── playground-template.md
    ├── practice-template.md
    ├── progress-states.md
    ├── readme-template.md
    └── welcome-messages.md
```

**Documentación completa:** [ai-professor/SKILL.md](ai-professor/SKILL.md)

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).
