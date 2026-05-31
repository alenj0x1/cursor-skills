# Plantilla de playground por módulo

El playground vive en `01-[nombre-modulo]/playground/` y solo se crea cuando el diagnóstico (FASE 1) confirma que el estudiante quiere practicar escribiendo código.

**Calidad:** cumplir [`content-quality-checklist.md`](content-quality-checklist.md). Comentarios **en español**, detallados, solo inline (sin README por práctica).

## Estructura

```
01-[nombre-modulo]/playground/
├── README.md                 ← Cómo instalar y ejecutar (nivel módulo)
├── practice-01/
│   └── [archivos starter]
├── practice-02/
│   └── [archivos starter]
└── ...
```

Cada carpeta `practice-[NN]/` corresponde a una práctica de código del módulo. Las prácticas teóricas/escritas no tienen carpeta aquí.

**No crear** `README.md` dentro de `practice-[NN]/` — la guía va en comentarios del código.

---

## playground/README.md

```markdown
# Playground — Módulo [N] — [Nombre]

## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Prácticas](../practices/) · [Mis soluciones](../solutions/)

---

## Requisitos

[Dependencias mínimas: versión de lenguaje, herramientas necesarias]

## Instalación

```bash
[comandos]
```

## Cómo ejecutar

| Práctica | Comando |
|----------|---------|
| [Practice 01](../practices/practice-01-[desc].md) | `[comando]` |
| [Practice 02](../practices/practice-02-[desc].md) | `[comando]` |

## Prácticas de código

- [practice-01/](practice-01/) — [Breve descripción]
- [practice-02/](practice-02/) — [Breve descripción]
```

---

## Archivos starter por práctica

Cada `playground/practice-[NN]/` debe contener:

- Archivos mínimos para empezar (no la solución completa)
- Comentarios en **español**, detallados (ver sección siguiente)
- **Sin** README local en la carpeta de la práctica

**Regla:** nunca incluir la solución final. Solo scaffolding + instrucciones en comentarios.

---

## Comentarios inline obligatorios (español)

En el archivo entry de cada práctica incluir:

1. **Encabezado** — título de la práctica + ruta al enunciado: `../practices/practice-NN-[desc].md`
2. **Mapa del archivo** — qué hace cada sección o archivo del starter
3. **Por función/bloque** — propósito del código ya escrito (scaffolding)
4. **Cada TODO** — qué implementar, por qué importa en el módulo, cómo comprobar localmente (sin dar la solución)
5. **Qué no modificar** — líneas o archivos fijos del boilerplate

Ejemplo mínimo aceptable (Python):

```python
# Práctica 01 — [Título]
# Enunciado completo: ../practices/practice-01-[desc].md
#
# Este archivo es tu punto de partida. No borres las funciones marcadas;
# completa solo los bloques TODO.

def solve():
    # TODO: [qué implementar — acción concreta]
    # Por qué: [vincula con el concepto del README]
    # Comprobar: [comando o salida esperada al ejecutar main.py]
    pass

if __name__ == "__main__":
    # Ejecuta: python practice-01/main.py desde la carpeta playground/
    solve()
```

---

## Configuración por stack

Adaptar según el tema del aprendizaje. Elegir el stack detectado en FASE 1 / FASE 2.

### Python

```
playground/
├── README.md
├── requirements.txt          ← solo si hay dependencias externas
├── practice-01/
│   └── main.py
└── practice-02/
    └── main.py
```

`main.py` starter (comentarios en español):

```python
# Práctica 01 — [título]
# Enunciado: ../practices/practice-01-[desc].md

def solve():
    # TODO: implementa aquí tu solución (ver enunciado, paso 1)
    # Comprobar: python practice-01/main.py — debe [descripción breve]
    pass

if __name__ == "__main__":
    solve()
```

Ejecutar: `python practice-01/main.py`

### JavaScript / Node.js

```
playground/
├── README.md
├── package.json              ← solo si hay dependencias
├── practice-01/
│   └── index.js
└── practice-02/
    └── index.js
```

Ejecutar: `node practice-01/index.js`

### TypeScript

```
playground/
├── README.md
├── package.json
├── tsconfig.json
├── practice-01/
│   └── index.ts
└── practice-02/
    └── index.ts
```

Ejecutar: `npx tsx practice-01/index.ts` o script definido en package.json

### HTML / CSS / JavaScript (frontend)

```
playground/
├── README.md
├── practice-01/
│   ├── index.html
│   ├── style.css
│   └── script.js
└── practice-02/
    └── index.html
```

Comentarios en español en `script.js` y en HTML con `<!-- -->` donde haga falta.

Ejecutar: abrir `index.html` en el navegador o usar Live Server

### SQL

```
playground/
├── README.md
├── schema.sql                  ← setup compartido del módulo si aplica
├── practice-01/
│   └── query.sql
└── practice-02/
    └── query.sql
```

Comentarios SQL con `--` en español. Incluir en README del módulo cómo conectar (SQLite, PostgreSQL, etc.)

### Otros lenguajes

Seguir el mismo patrón:
- `README.md` del módulo con install + run
- Una carpeta por práctica (sin README local)
- Archivo entry point con nombre convencional del lenguaje (`main.go`, `Main.java`, `lib.rs`, etc.)
- Comentarios inline en español según sintaxis del lenguaje

---

## Evaluación (FASE 4)

Al revisar prácticas de código:

1. Leer el enunciado en `practices/practice-[NN]-[desc].md`
2. Revisar archivos en `playground/practice-[NN]/`
3. Verificar criterios de éxito del enunciado, no solo que el código compile
4. Si la práctica también requiere explicación escrita, leer `solutions/practice-[NN]-[desc].md`

No ejecutar código automáticamente a menos que el entorno lo permita; leer e inferir corrección, y señalar al estudiante si debe verificar localmente.
