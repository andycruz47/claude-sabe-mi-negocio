---
name: anota-todo
description: Cierra el día escribiendo la nota de hoy en daily-notes con la hora, lo que pasó y lo que quedó pendiente, y guarda en memory lo nuevo que se aprendió del usuario. Úsala cuando el usuario diga "anota todo", "anota", "cierra el día", "guárdalo en la memoria" o "acuérdate de esto".
---

# Anota todo

El objetivo es que la próxima sesión, que no recuerda nada de esta, sepa lo que pasó hoy y lo que aprendiste.

## 1. La fecha y la hora, del sistema

Mira la fecha y la hora reales en el sistema antes de escribir. **No las calcules de memoria**, porque una sesión puede
quedarse abierta toda la noche.

## 2. La nota de hoy

Archivo `daily-notes/AAAA-MM-DD.md`. Si no existe, créalo. Si existe, **añade al final, nunca sobrescribas**.

```markdown
## HH:MM · de qué fue

**Qué se hizo**
- ...

**Qué quedó pendiente**
- ...
```

Escribe lo que de verdad pasó, en pocas líneas. Si algo quedó a medias, se dice que quedó a medias.

## 3. Lo que aprendiste, a la memoria

Repasa la sesión y busca lo que una sesión futura necesitaría saber y **no se deduce de los archivos**

- Una corrección del usuario (*"no, así no, hazlo así"*). Escribe la regla y el porqué.
- Una decisión que tomó.
- Un dato nuevo de su negocio, sus clientes o su forma de trabajar.

Para cada cosa

1. Busca en `memory/` si ya hay una nota de ese tema. **Si la hay, amplíala.** Solo si no encaja en ninguna, crea una.
2. Si contradice algo escrito antes, **reemplaza lo viejo**, no dejes las dos versiones.
3. Si creaste una nota nueva, añádela a `memory/memory.md` y, si hace falta, a `INDEX.md`.

Una nota diaria no sustituye a la memoria. La nota es el registro del día; lo que tiene que durar va en `memory/`.

## 4. Comprobar

Lee de vuelta lo que escribiste y dile al usuario en dos o tres líneas qué anotaste y dónde.
