---
name: montar-sistema
description: Monta en la carpeta actual un sistema para que el agente recuerde el negocio del usuario entre sesiones. Crea el archivo de reglas (CLAUDE.md, o AGENTS.md en Codex), el índice INDEX.md y las carpetas memory, daily-notes y jobs, haciendo preguntas una a una. Úsala cuando el usuario diga "monta mi sistema", "quiero que sepas todo mi negocio", "configura la memoria" o algo parecido, o justo después de instalar estas skills.
---

# Montar el sistema

Vas a dejar escrito en archivos todo lo que necesitas saber del negocio del usuario, para no tener que preguntárselo
otra vez en la próxima sesión. **Lo que no está escrito, no lo sabes.**

## Reglas mientras lo haces

- **Una pregunta a la vez.** Esperas la respuesta antes de hacer la siguiente. Nunca una lista de diez preguntas.
- **Con sus palabras.** Escribe lo que el usuario dice, no tu versión resumida y genérica.
- **Si no sabe algo, se deja en blanco** con un `(pendiente)`. No inventes datos de su negocio.
- **Antes de crear cada archivo, dile en una frase qué vas a crear y para qué.**
- Si ya existe alguno de estos archivos, **no lo sobrescribas**. Léelo y complétalo.
- Habla en el idioma del usuario.

## Paso 1 · Comprobar dónde estás

Confirma que estás en la carpeta de su negocio (no en su carpeta personal ni en el escritorio). Si no lo está, dile que
cree una carpeta con el nombre que quiera y te abra dentro.

Mira si eres Claude Code o Codex. **El archivo de reglas se llama `CLAUDE.md` en Claude Code y `AGENTS.md` en Codex.**
Abajo se dice `CLAUDE.md`; usa el nombre que te toque.

## Paso 2 · El archivo de reglas

Hazle las preguntas que necesites para saber, como mínimo

1. Quién es y a qué se dedica.
2. Qué vende, a quién y a qué precio.
3. Cómo quiere que trabajes (qué tono, qué tienes que confirmar antes de hacer, qué no debes hacer nunca).

Crea `CLAUDE.md` en la raíz con esto

```markdown
# Reglas

## Quién soy
...

## Qué vendo
...

## Cómo quiero que trabajes
- ...

## Al empezar cada sesión
1. Lee INDEX.md.
2. Lee la nota del último día en daily-notes/.
3. Abre solo las notas de memory/ que hagan falta para lo que te pida.

## Antes de una tarea que se repite
Lee su nota en jobs/ antes de empezar.
```

Este archivo lo lees solo cada vez que se abre una sesión, así que **tiene que ser corto**. Lo largo va en `memory/`.

## Paso 3 · El índice

Crea `INDEX.md` en la raíz con una línea por carpeta o archivo importante: qué hay y cuándo abrirlo.

```markdown
# Índice

| Dónde | Qué hay | Cuándo se abre |
|---|---|---|
| CLAUDE.md | Las reglas | Siempre, solo |
| memory/ | Una nota por tema | Cuando el tema haga falta |
| daily-notes/ | Una nota por día | La del último día, al empezar |
| jobs/ | Tareas repetidas, paso a paso | Antes de hacer esa tarea |
```

**Cada vez que crees algo nuevo en la carpeta, añádelo aquí.** Un índice desfasado es peor que no tener índice.

## Paso 4 · La memoria

Crea la carpeta `memory/` con una nota por tema y un índice propio, `memory/memory.md`, con una línea por nota.

Empieza con dos notas, preguntándole lo que necesites

- **`memory/oferta.md`** qué vende, a quién, el precio, qué incluye y qué no.
- **`memory/como-escribo.md`** cómo habla con sus clientes, palabras que usa y que no usa. Si puede, que te pegue dos
  o tres mensajes o textos suyos de verdad.

Dile que **aquí le conviene explicarte bien su caso**, porque mientras más contexto, mejor trabajas.

Reglas de la memoria

- **Un tema, una nota.** Antes de crear una nueva, mira si ya hay una que lo cubra y amplíala.
- **Al cambiar algo, se borra lo viejo.** No dejes dos versiones que se contradigan.

## Paso 5 · Las notas del día

Crea la carpeta `daily-notes/`. Las notas van como `daily-notes/AAAA-MM-DD.md`.

Añade esta regla a `CLAUDE.md`

```markdown
## Anota todo
Cuando te diga "anota todo", escribe la nota de hoy en daily-notes/ con la hora, lo que pasó y lo que quedó pendiente,
y guarda en memory/ lo nuevo que hayas aprendido de mí.
```

Si está instalada la skill `anota-todo`, eso es lo que hace.

## Paso 6 · Las tareas

Crea la carpeta `jobs/` con su índice `jobs/jobs.md`.

Pregúntale cuál es **la tarea que más repite** (un documento para cada cliente, una propuesta, un post). Dile que la
próxima vez que la hagan juntos, al terminar, le diga *"guarda esta tarea"*, y queda escrita paso a paso. Eso es lo que
hace la skill `guardar-tarea`.

## Al terminar

1. Actualiza `INDEX.md` con todo lo creado.
2. Lee de vuelta cada archivo para comprobar que se escribió.
3. Dile en pocas líneas qué quedó montado, y que **no tiene que llenarlo todo hoy**. Con las reglas y el *anota todo*
   de cada noche ya empieza, y cada vez que te corrija, que te diga que lo guardes en la memoria.
