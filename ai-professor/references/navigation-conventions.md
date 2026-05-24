# Convenciones de navegación

Todo archivo markdown generado por ai-professor debe incluir **enlaces relativos clicables** para que el estudiante pueda moverse entre secciones sin buscar rutas manualmente.

## Regla general

- Usar rutas relativas desde la ubicación del archivo actual
- Cada enlace debe apuntar al archivo o carpeta concreta, no solo mencionar el nombre en texto plano
- Incluir un bloque `## Navegación` al **inicio** de cada archivo generado (después del título)
- Repetir links contextuales en secciones clave cuando ayude (ej. "Siguiente paso" en README)

---

## Bloque de navegación por ubicación

### README del módulo (`01-[nombre]/README.md`)

```markdown
## Navegación

← [Progreso general](../PROGRESS.md) · [Ejemplos](examples/) · [Prácticas](practices/) · [Mis soluciones](solutions/) · [Playground](playground/)
```

Omitir `· [Playground](playground/)` si el módulo no tiene prácticas de código.

### Ejemplo (`01-[nombre]/examples/ejemplo-01-[desc].md`)

```markdown
# Ejemplo [N] — [Título descriptivo]

## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Ejemplos](.) · [Prácticas](../practices/) · [Mis soluciones](../solutions/)
```

Añadir `· [Playground](../playground/)` si aplica.

### Práctica (`01-[nombre]/practices/practice-01-[desc].md`)

```markdown
## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Ejemplos](../examples/) · [Prácticas](.) · [Mi solución](../solutions/practice-01-[desc].md) · [Playground](../playground/practice-01/)
```

Omitir links a `solutions/` o `playground/` si esa práctica no los usa.

### Solución placeholder (`01-[nombre]/solutions/practice-01-[desc].md`)

```markdown
## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Enunciado](../practices/practice-01-[desc].md) · [Prácticas](../practices/)
```

### Playground README (`01-[nombre]/playground/README.md`)

```markdown
## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Prácticas](../practices/) · [Mis soluciones](../solutions/)
```

---

## PROGRESS.md — tabla con links

La columna "Módulo" debe enlazar al README del módulo. La columna "Prácticas" debe enlazar a la carpeta `practices/` del módulo.

```markdown
| # | Módulo | Estado | Prácticas | Fecha |
|---|--------|--------|-----------|-------|
| 01 | [Fundamentos](01-fundamentos/README.md) | 🔄 En curso | [1/3](01-fundamentos/practices/) | 2026-05-23 |
| 02 | [Variables](02-variables/README.md) | 🔒 Bloqueado | [0/2](02-variables/practices/) | — |
```

En la sección "Módulo Actual", incluir links directos:

```markdown
## 📝 Módulo Actual

**[Módulo 01 — Fundamentos](01-fundamentos/README.md)**
- Estado: 🔄 En curso
- Prácticas entregadas: 1/3 — [ver prácticas](01-fundamentos/practices/) · [mis soluciones](01-fundamentos/solutions/)
- Playground: [01-fundamentos/playground/](01-fundamentos/playground/) _(solo si aplica)_
```

---

## README del módulo — sección "Contenido de este módulo"

Listar cada ejemplo y práctica con link directo:

```markdown
## 📂 Contenido de este módulo

### Ejemplos
- [Ejemplo 01 — Variables básicas](examples/ejemplo-01-variables-basicas.md)
- [Ejemplo 02 — Tipos de datos](examples/ejemplo-02-tipos-datos.md)

### Prácticas
- [Practice 01 — Declarar variables](practices/practice-01-declarar-variables.md) → [solución](solutions/practice-01-declarar-variables.md) · [playground](playground/practice-01/)
- [Practice 02 — Conversión de tipos](practices/practice-02-conversion-tipos.md) → [solución](solutions/practice-02-conversion-tipos.md)
```

---

## Reglas al actualizar PROGRESS.md

- **Nunca** romper links existentes al actualizar estados o fechas
- Al renombrar módulos o prácticas, actualizar todos los links afectados en PROGRESS, README y archivos relacionados
- Mantener consistencia de slug: `ejemplo-01-[desc].md` en `examples/`; `practice-01-[desc].md` en `practices/` y `solutions/` debe tener el mismo nombre
