---
name: guardar-tarea
description: Deja escrita en jobs una tarea que el usuario repite (un documento para cada cliente, una propuesta, un post), paso a paso, para que la próxima vez salga igual de bien sin volver a explicarla. Úsala cuando el usuario diga "guarda esta tarea", "escríbelo paso a paso", "la próxima vez hazlo igual", o al terminar juntos una tarea que se va a repetir.
---

# Guardar una tarea

Acaban de hacer juntos algo que se va a repetir. Ahora lo dejas escrito para que la próxima vez **lo leas antes de
empezar** y salga igual, sin que el usuario tenga que explicarlo otra vez.

## 1. Mira lo que de verdad se hizo

Repasa la conversación entera, no solo el final. Lo que importa suele estar en las correcciones del usuario: lo que
hiciste mal primero y cómo te pidió que lo cambiaras.

## 2. Escribe la nota

Archivo `jobs/<nombre-de-la-tarea>.md`, con nombre corto y claro (`documento-para-lead.md`, `propuesta.md`).

```markdown
# <Nombre de la tarea>

**Cuándo se usa:** ...

## Qué leer antes
- memory/... (por qué)
- ...

## Pasos
1. ...
2. ...

## Cómo tiene que quedar
- ... (lo que el usuario aprobó: formato, largo, tono)

## Lo que no se hace
- ... (cada corrección del usuario, con su porqué)

## Ejemplo bueno
<ruta al resultado que el usuario aprobó, si existe>
```

- **Pasos que otra sesión pueda seguir sin contexto.** Nada de *"como hablamos"*.
- **Las correcciones van enteras.** Son lo que más vale de la nota.
- Si una nota de esa tarea ya existe, **amplíala**, no crees otra.

## 3. Que se lea antes

1. Añade la tarea a `jobs/jobs.md`, con una línea de cuándo se usa.
2. Comprueba que `CLAUDE.md` (o `AGENTS.md` en Codex) diga que antes de una tarea repetida se lee su nota en `jobs/`. Si
   no lo dice, añádelo.

## 4. Comprobar

Lee de vuelta la nota y dile al usuario dónde quedó y que la próxima vez solo tiene que pedirte la tarea por su nombre.
