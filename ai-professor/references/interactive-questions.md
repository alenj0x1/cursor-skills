# Preguntas interactivas (AskQuestion)

Toda decisión del estudiante debe presentarse con la herramienta **`AskQuestion`** de Cursor, no como párrafo con opciones en el chat.

## Reglas obligatorias

1. **Usar `AskQuestion`** para elegir, confirmar o priorizar — diagnóstico, retorno de sesión, validar ruta de aprendizaje, refuerzo A/B, verificación de comprensión
2. **Una pregunta por llamada** — el array `questions` tiene un solo elemento
3. **Esperar** la respuesta antes de la siguiente pregunta; nunca encadenar el diagnóstico en un solo mensaje
4. Incluir en el `prompt` la recomendación del profesor cuando aplique
5. Marcar la opción recomendada como **primera opción** o con sufijo `(recomendado)` en `label`
6. Si el usuario ya mencionó el tema, **no repetirlo en texto** — confirmar con `AskQuestion` o pasar directo a la pregunta 2 del diagnóstico
7. **Adaptar opciones al tema** — ej. Redis → incluir "protocolo RESP", "persistencia" en prioridades si aplica

## Fallback

Si `AskQuestion` no está disponible (Agent mode + modelo sin herramienta):

- Preguntar en texto listando las **mismas opciones numeradas**
- Mantener una pregunta por mensaje
- Indicar cuál es la recomendada

## Formato de llamada

```json
{
  "title": "Diagnóstico — tu objetivo",
  "questions": [{
    "id": "learning_goal",
    "prompt": "¿Para qué quieres aprender esto? (Define qué tan profundo iremos.)",
    "options": [
      { "id": "personal", "label": "Proyecto personal (recomendado)" },
      { "id": "curiosity", "label": "Curiosidad técnica" },
      { "id": "interviews", "label": "Preparación para entrevistas" },
      { "id": "work", "label": "Trabajo / uso profesional" },
      { "id": "other", "label": "Otro — lo explico en el chat" }
    ],
    "allow_multiple": false
  }]
}
```

Parámetros:
- `title` — contexto breve de la fase
- `questions[].id` — identificador estable para guardar la respuesta
- `questions[].prompt` — pregunta clara; puede incluir recomendación
- `questions[].options[]` — mínimo 2 opciones; incluir `"Otro — lo explico en el chat"` cuando aplique
- `allow_multiple` — `true` solo si el estudiante puede elegir varias (ej. prioridades)

## Persistencia

Tras cada respuesta, guardar internamente el `id` elegido. Al crear `PROGRESS.md`, anotar en metadatos: objetivo, nivel previo, estilo, tipo de prácticas.

---

## Plantillas por fase

### FASE 0 — Retorno de sesión

| Campo | Valor |
|-------|-------|
| `title` | Retomar sesión |
| `id` | `session_intent` |
| `prompt` | ¿Qué quieres hacer hoy? |

Opciones: `continue_module` (recomendado), `review_practices`, `review_concept`, `change_topic`, `other`

---

### FASE 1 — Diagnóstico (una AskQuestion por pregunta)

#### 0. Nombre (`student_name`) — solo estudiante nuevo sin nombre conocido

Preguntar **antes** del tema, justo después del saludo de bienvenida.

| Campo | Valor |
|-------|-------|
| `title` | Diagnóstico — tu nombre |
| `id` | `student_name` |
| `prompt` | ¿Cómo te llamo? Lo usaré en PROGRESS.md y para personalizar tu aprendizaje. |

Opciones: `provide_name` → "Escribiré mi nombre en el chat", `skip` → "Prefiero no decir — llámame Estudiante"

Si elige `provide_name`, esperar el nombre en el siguiente mensaje. Si elige `skip`, usar "Estudiante". Guardar en metadatos de `PROGRESS.md`.

Si el usuario ya dio su nombre en el primer mensaje, confirmar con `AskQuestion` o usarlo directamente sin volver a preguntar.

#### 1. Tema (`learning_topic`)

Si **no** mencionó tema: opción `write_in_chat` → pedir tema en el siguiente mensaje.

Si **ya** mencionó tema: `confirm` (recomendado), `refine`, `other`

#### 2. Propósito (`learning_goal`)

`personal` (recomendado), `curiosity`, `interviews`, `work`, `career`, `other`

#### 3. Nivel previo (`prior_knowledge`)

`none`, `basic`, `partial`, `advanced_parts`, `other` — follow-up si elige partial/advanced_parts

#### 4. Prioridades (`must_learn`)

`none` (recomendado), `has_priorities` → segunda AskQuestion con `allow_multiple: true` y opciones adaptadas al tema

#### 5. Estilo (`learning_style`)

`practical_first` (recomendado), `theory_first`, `mixed`

#### 6. Tipo de prácticas (`practice_type`)

`code`, `theoretical`, `mixed` (recomendado para temas técnicos)

Mapeo: `code` → `codigo`, `theoretical` → `teorico`, `mixed` → `mixto`

---

### FASE 2 — Validar ruta de aprendizaje

| Campo | Valor |
|-------|-------|
| `title` | Validar aprendizaje |
| `id` | `curriculum_approval` |
| `prompt` | ¿Esta ruta de aprendizaje te funciona? |

Opciones: `approve` (recomendado), `adjust`, `add_topic`, `restart`

No avanzar a 2.3 hasta respuesta.

---

### FASE 4 — Puntos débiles

| Campo | Valor |
|-------|-------|
| `id` | `weak_points_choice` |
| `prompt` | Noté dificultades en: [lista]. ¿Cómo prefieres continuar? |

Opciones: `reinforce` (recomendado), `advance`

---

### Verificación de comprensión

| Campo | Valor |
|-------|-------|
| `id` | `understanding_check` |
| `prompt` | ¿Quedó claro [concepto]? |

Opciones: `understood`, `another_example`, `different_explanation`, `question`

---

## Prohibiciones

- **No** listar opciones solo en prosa si `AskQuestion` está disponible
- **No** hacer varias preguntas de diagnóstico en un solo mensaje
- **No** simular opciones clicables con bloques de código — invocar la herramienta
