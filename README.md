# cursor-skills

Colección personal de Agent Skills para Cursor que amplían las capacidades del asistente con flujos especializados.

## 📦 Instalación

Cada skill vive en su propia carpeta. Instala solo las que necesites.

### 1. Obtener el repositorio

```bash
git clone https://github.com/alenj0x1/cursor-skills.git
```

También puedes descargar el ZIP desde GitHub si no usas Git.

### 2. Copiar la skill

Copia la carpeta de la skill que quieras (por ejemplo, `ai-professor/`) a una de estas ubicaciones:

| Ámbito | Ruta |
|--------|------|
| Personal (todos tus proyectos) | `~/.cursor/skills/` en macOS/Linux, o `%USERPROFILE%\.cursor\skills\` en Windows |
| Por proyecto (solo ese repo) | `.cursor/skills/` en la raíz del proyecto |

Ejemplo en Windows (PowerShell):

```powershell
Copy-Item -Recurse .\cursor-skills\ai-professor $env:USERPROFILE\.cursor\skills\ai-professor
```

Ejemplo en macOS/Linux:

```bash
cp -r cursor-skills/ai-professor ~/.cursor/skills/ai-professor
```

### 3. Verificar

La estructura final debe quedar así:

```
~/.cursor/skills/ai-professor/
├── SKILL.md
└── references/
    ├── progress-states.md
    └── readme-template.md
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
- «Crea un currículo para [tema]»
- «Arma los módulos para aprender [tema]»
- «Quiero estudiar [tema]»
- «ai-professor»

**Cómo usarla en Cursor:** escribe en el chat una de las frases anteriores, o adjunta la skill manualmente con `@` / `/` según tu versión de Cursor.

**Estructura:**

```
ai-professor/
├── SKILL.md                      # Instrucciones completas del agente
└── references/
    ├── progress-states.md        # Estados de progreso del estudiante
    └── readme-template.md        # Plantilla para README de módulos
```

**Documentación completa:** [ai-professor/SKILL.md](ai-professor/SKILL.md)

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).
