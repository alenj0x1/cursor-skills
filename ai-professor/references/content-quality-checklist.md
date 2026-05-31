# Checklist de calidad de contenido

Usar **antes de anunciar** un módulo al estudiante (FASE 3.5). Si algún ítem falla, corregir el contenido y volver a revisar. No entregar módulos incompletos o superficiales.

Ver también: `readme-template.md`, `practice-template.md`, `playground-template.md`.

---

## README del módulo

### Por sección (obligatorio)

| Sección | Mínimo |
|---------|--------|
| Navegación | Links relativos a PROGRESS, examples, practices, solutions, playground (si aplica) |
| Por qué importa | ≥2 párrafos; conectado al diagnóstico del estudiante (objetivo, trabajo, proyecto) |
| Mapa del módulo | Diagrama ASCII o jerarquía con todos los conceptos del módulo |
| Conceptos fundamentales | Por cada concepto: analogía + definición + **≥3 párrafos** de desarrollo + ejemplo rápido inline |
| Cómo se relacionan | Tabla o diagrama que enlace ≥2 conceptos del módulo |
| Errores comunes | **≥3** errores, cada uno con causa y cómo evitarlo |
| Resumen visual | Condensa **todos** los conceptos del módulo (tabla, mapa o lista estructurada) |
| Contenido del módulo | Enlaces relativos a cada ejemplo y práctica (y solutions/playground) |
| Referencias | URLs reales (documentación oficial, artículos) |
| Siguiente paso | Pasos claros hacia examples/ y practices/ |

### Código en README

- Comentarios en **español** en cada bloque de código
- Comentar partes no obvias línea a línea o por bloque lógico
- Identificadores de código pueden estar en inglés salvo principiante absoluto y tema que lo permita

### Anti-patrones (README inválido)

- Un solo párrafo por concepto
- Motivación genérica (“es importante en la industria”) sin vínculo al diagnóstico
- Secciones vacías, “TBD” o “pendiente”
- Referencias sin URLs o con enlaces rotos inventados
- Ejemplos o prácticas listados sin enlaces relativos
- Código sin comentarios en español

---

## Examples (`examples/`)

- Al menos **un ejemplo** por cada concepto importante del README
- Bloque Navegación en cada archivo
- Sección “¿Qué problema resuelve este ejemplo?”
- Contenido completo (no esbozos)
- Comentarios en **español** en bloques de código
- Variaciones o casos límite cuando aporten claridad

### Anti-patrones

- Ejemplo que solo repite una frase del README sin demostración
- Código copiado sin explicación entre bloques
- Títulos o archivos con “Example” en lugar de “Ejemplo” / `ejemplo-XX`

---

## Practices (`practices/`)

### Secciones obligatorias en cada enunciado

1. Navegación
2. Objetivo
3. **Prerrequisitos** (conceptos del README, herramientas, archivos previos)
4. **Tiempo estimado**
5. **Archivos involucrados** (rutas relativas)
6. Enunciado (contexto narrativo)
7. **Pasos** numerados: cada paso = acción verificable → resultado esperado
8. Criterio de éxito (≥2 criterios verificables)
9. Dónde entregar (solutions/ y/o playground/)
10. Pistas (opcional, máximo 2, progresivas)

### Código en enunciados

- Si el enunciado incluye código de referencia o plantilla: comentarios en **español**

### Anti-patrones

- Enunciado vago (“implementa X”) sin pasos
- Sin prerrequisitos en prácticas que dependen de conceptos previos
- Sección `## Mi solución` en el enunciado
- Pasos que no indican qué archivo tocar o qué comprobar

---

## Playground (`playground/`)

Solo aplica si diagnóstico = `codigo` o `mixto`.

### Por carpeta `practice-[NN]/`

- Archivos starter mínimos (no solución completa)
- **Sin** `README.md` local por práctica — la guía va en comentarios inline
- Comentarios en **español**, detallados:
  - Encabezado: título de la práctica + enlace al enunciado (`../practices/practice-NN-[desc].md`)
  - Mapa del archivo (qué hace cada parte)
  - Cada función/bloque: propósito
  - Cada `TODO`: **qué** implementar, **por qué**, **cómo comprobar** (sin revelar la solución)
  - Qué no modificar (scaffolding fijo)

### `playground/README.md` del módulo

- Requisitos, instalación, tabla de comandos por práctica
- Links al enunciado de cada práctica de código

### Anti-patrones

- Solo `pass` o `TODO` sin explicación
- Comentarios en inglés
- Solución completa en el starter
- README duplicado por práctica cuando los comentarios inline bastan

---

## Solutions (`solutions/`)

- Placeholder por práctica con mismo nombre que el enunciado
- Bloque Navegación
- Sección “Tu respuesta” vacía para que el estudiante escriba

---

## Regla operativa

1. Generar todo el contenido del módulo (3.2–3.4)
2. Recorrer este checklist **en silencio** (no mostrar el checklist al estudiante)
3. Corregir lo que falle
4. Solo entonces: anuncio del módulo (FASE 3.6)
