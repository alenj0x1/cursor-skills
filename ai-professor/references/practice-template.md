# Plantilla de práctica (enunciado)

Cada archivo en `practices/` contiene **solo el enunciado**. La respuesta del estudiante va en `solutions/` (escrita) o `playground/` (código). Ver `references/navigation-conventions.md` para reglas de enlaces.

**Calidad:** cumplir [`content-quality-checklist.md`](content-quality-checklist.md) — el estudiante debe poder seguir la práctica sin adivinar pasos.

---

```markdown
# Práctica [N] — [Título descriptivo]

## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Ejemplos](../examples/) · [Prácticas](.) · [Mi solución](../solutions/practice-[NN]-[desc].md)

---

## Objetivo

[Una oración clara: qué habilidad o concepto demuestra esta práctica]

---

## Prerrequisitos

- [Concepto(s) del README que debe haber leído — con link si ayuda]
- [Herramientas instaladas o archivos que ya deben existir]

---

## Tiempo estimado

[~X minutos — ajustar según complejidad]

---

## Archivos involucrados

- [ruta/relativa/al/archivo.md o carpeta]
- [otro archivo si aplica]

---

## Enunciado

[Contexto narrativo: situación, restricciones generales, inputs/outputs esperados a alto nivel.
La ejecución detallada va en Pasos.]

---

## Pasos

1. [Acción concreta] → [Resultado esperado verificable]
2. [Siguiente acción] → [Resultado esperado]
3. ...

_(Cada paso debe indicar qué hacer, dónde (archivo o sección) y cómo saber que el paso salió bien.)_

---

## Criterio de éxito

El estudiante sabe que lo hizo bien cuando:
- [Criterio verificable 1]
- [Criterio verificable 2]
- [Criterio verificable 3 si aplica]

---

## Dónde entregar

| Tipo | Ubicación |
|------|-----------|
| Respuesta escrita | [solutions/practice-[NN]-[desc].md](../solutions/practice-[NN]-[desc].md) |
| Código | [playground/practice-[NN]/](../playground/practice-[NN]/) |

_(Incluir solo las filas que apliquen a esta práctica.)_

---

## Pistas _(opcional)_

[Solo si la práctica es difícil. Máximo 2 pistas progresivas, no la solución.]
```

---

## Reglas al generar prácticas

1. **Nunca** incluir sección `## Mi solución` en el enunciado
2. Crear el placeholder correspondiente en `solutions/` al mismo tiempo (mismo nombre de archivo)
3. Si la práctica requiere código, crear carpeta `playground/practice-[NN]/` con archivos starter
4. Nomenclatura consistente: `practice-01-[desc].md` en `practices/` = `practice-01-[desc].md` en `solutions/`
5. Progresión: de lo simple a lo complejo dentro del módulo
6. Cantidad: suficientes para cubrir **cada concepto importante** del README
7. **Siempre** incluir Prerrequisitos, Tiempo estimado, Archivos involucrados y Pasos numerados
8. Código en el enunciado: comentarios en **español**

## Placeholder en solutions/

Al generar el módulo, crear cada archivo en `solutions/` con este contenido mínimo:

```markdown
# Solución — Práctica [N] — [Título]

## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Enunciado](../practices/practice-[NN]-[desc].md) · [Prácticas](../practices/)

---

## Tu respuesta

_(Escribe aquí tu solución.)_
```
