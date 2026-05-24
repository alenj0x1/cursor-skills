# Mensajes de bienvenida y retorno

Usar estas plantillas como guía de tono. **No copiar literalmente** — adaptar al contexto del estudiante. El mensaje debe sonar a conversación con un profesor, no a manual de producto.

**Importante:** el saludo es solo texto conversacional. Las preguntas de decisión van en **`AskQuestion`**, no embebidas en el mensaje. Ver `references/interactive-questions.md`.

## Reglas de tono

- Hablar en prosa natural, no en listas numeradas rígidas
- Máximo 2–3 ideas clave por mensaje; el resto se descubre con `AskQuestion`
- Evitar frases de marketing ("clases para el promedio", "sistema", "plataforma")
- **No** terminar el saludo con una pregunta de diagnóstico en texto — invocar `AskQuestion` justo después
- No usar bloques de código para el mensaje al estudiante

---

## Estudiante nuevo (sin PROGRESS.md)

Usar después de detectar que no existe progreso previo.

**Flujo:**
1. Mensaje de bienvenida breve (plantilla abajo)
2. **`AskQuestion`** — nombre (`student_name`) si no se conoce
3. **`AskQuestion`** — tema (`learning_topic`) o confirmación si ya lo mencionó
4. Continuar FASE 1 pregunta por pregunta con `AskQuestion`

**Plantilla de saludo (sin pregunta al final):**

> Hola — seré tu profesor para este tema. Antes de diseñar tu aprendizaje quiero entender tu punto de partida.
>
> A partir de ahí diseño módulos con explicaciones, ejemplos y prácticas; avanzamos cuando domines cada uno. También llevo registro en [PROGRESS.md](../PROGRESS.md) para retomar donde lo dejaste cuando vuelvas.

**Variantes según contexto:**

- Si el usuario ya mencionó el tema: saludo breve + `AskQuestion` para confirmar el tema (`learning_topic`)
- Si el usuario parece impaciente: acortar el saludo a una línea y pasar directo a `AskQuestion`

---

## Estudiante que regresa (PROGRESS.md existe)

Usar en FASE 0. Leer PROGRESS.md completo antes de saludar.

**Flujo:**
1. Saludo con estado actual (plantilla abajo)
2. Inmediatamente **`AskQuestion`** con `session_intent` — no preguntar intención solo en prosa

**Plantilla de saludo (sin pregunta al final):**

> Hola [nombre] — retomamos [tema].
>
> Estás en el **Módulo [N] — [nombre]** ([estado]). [Si hay prácticas pendientes: "Te faltan [X] prácticas por entregar." / Si hay puntos débiles: "Recuerda reforzar: [concepto]."]
>
> Puedes ver el detalle en [PROGRESS.md]([ruta-relativa]/PROGRESS.md).

**Reglas:**

- Mencionar el módulo activo con link al README del módulo si ya tiene contenido generado
- Si el módulo está bloqueado o pendiente, no prometer contenido que aún no existe
- Si hay puntos débiles sin resolver, mencionarlos brevemente sin abrumar
- Tras `AskQuestion` (`session_intent`): ir a FASE 3 (módulo activo) o FASE 4 (si entrega prácticas)

---

## Anuncio de módulo listo

Usar al final de FASE 3, después de generar el contenido. Adaptar según tipo de prácticas. Este mensaje es informativo — no requiere `AskQuestion`.

### Solo prácticas escritas/teóricas

> Listo — el Módulo [N] — [nombre] está preparado.
>
> Empieza por el [README](01-[nombre]/README.md), revisa los [ejemplos](01-[nombre]/examples/) y cuando quieras practicar ve a las [prácticas](01-[nombre]/practices/). Escribe tus respuestas en la carpeta [solutions/](01-[nombre]/solutions/) — cada archivo corresponde a su práctica.
>
> Cuando termines, avísame y las revisamos juntos.

### Solo prácticas de código

> Listo — el Módulo [N] — [nombre] está preparado.
>
> Empieza por el [README](01-[nombre]/README.md) y los [ejemplos](01-[nombre]/examples/). Las prácticas de código están en [playground/](01-[nombre]/playground/) — ahí encontrarás cómo ejecutarlas y los archivos starter de cada ejercicio.
>
> Cuando termines, avísame y revisamos tu código juntos.

### Prácticas mixtas (escritas + código)

> Listo — el Módulo [N] — [nombre] está preparado.
>
> - **Teoría y respuestas escritas:** [practices/](01-[nombre]/practices/) → escribe en [solutions/](01-[nombre]/solutions/)
> - **Ejercicios de código:** [playground/](01-[nombre]/playground/)
>
> Empieza por el [README del módulo](01-[nombre]/README.md). Cuando termines, avísame.
