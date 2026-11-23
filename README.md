# Que Claude Code sepa todo tu negocio

Estas son las skills del video **Cómo hago para que Claude Code sepa todo mi negocio**. Montan en tu carpeta el mismo
sistema que enseño ahí, para que Claude Code (o Codex) recuerde quién eres, qué vendes y cómo trabajas, sin que se lo
vuelvas a explicar cada vez.

La idea de fondo es una sola. **Lo que no está escrito, Claude no lo sabe.** Así que todo lo que importa se escribe en
archivos que él lee solo.

## Qué trae

| Skill | Qué hace |
|---|---|
| `montar-sistema` | Te monta el sistema entero en tu carpeta, haciéndote preguntas una a una. Se usa una vez |
| `anota-todo` | Al terminar el día, escribe la nota de hoy y guarda en la memoria lo que aprendió de ti |
| `guardar-tarea` | Cuando terminas algo que repites seguido, lo deja escrito paso a paso para que la próxima vez salga igual |

## Cómo se instala

La forma fácil es pedírselo a tu agente. Abre Claude Code o Codex en la carpeta de tu negocio y dile

```
Instala las skills de este repositorio y luego usa montar-sistema conmigo.
https://github.com/andycruz47/claude-sabe-mi-negocio
```

Si prefieres hacerlo a mano, copia las tres carpetas de `skills/` en

- **Claude Code**, `.claude/skills/` dentro de la carpeta de tu negocio (o `~/.claude/skills/` para tenerlas en todas)
- **Codex**, `~/.codex/skills/`

Y luego le dices *"monta mi sistema"*.

## Lo que queda en tu carpeta

```
tu-negocio/
├── CLAUDE.md        tus reglas. Lo lee solo al abrir cada sesión (en Codex se llama AGENTS.md)
├── INDEX.md         el mapa de la carpeta. Así abre solo lo que necesita
├── memory/          una nota por tema. Tu oferta, cómo escribes, tus clientes
├── daily-notes/     una nota por día, con la hora, lo que pasó y lo que quedó pendiente
└── jobs/            tus tareas repetidas, escritas paso a paso
```

## Cómo se usa después

No tienes que llenarlo todo el primer día. Con las reglas y el *anota todo* de cada noche ya empiezas.

- Al terminar el día le dices **anota todo**.
- Cuando lo corrijas, le dices **guárdalo en la memoria**.
- Cuando acabes una tarea que repites, le dices **guarda esta tarea**.

Así el resto se va llenando solo, con lo que aprende de ti usándolo.

## Licencia

MIT. Úsalas, cámbialas y compártelas como quieras.
