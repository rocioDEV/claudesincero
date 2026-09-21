# claudesincero

<p align="center">
  <img src="assets/claudesincero.png" alt="Asterisco de Claude diciendo: Quemando tokens como si no hubiera un mañana" width="280">
</p>

Paquete de verbos de spinner en español para [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

Claude Code muestra un spinner con verbos rotativos mientras trabaja
("Thinking...", "Analyzing..."). Este repo reemplaza esos verbos por
frases en español y con bastante menos filtro, usando la clave soportada
`spinnerVerbs` de `settings.json`.

<img width="714" height="173" alt="image" src="https://github.com/user-attachments/assets/c9e942fb-3aa6-4f6d-b32c-f809d45cdf9c" />


## Instalación

### Skill (recomendado)

```bash
npx skills add rocioDEV/claudesincero
```

Luego pídele al agente "instala claudesincero" — copiará el paquete
`claudesincero` a tu `~/.claude/settings.json`. Para revertir, pide
"quita claudesincero" o "restablece los spinners".

### Manual

Copia el contenido de
`.claude/skills/claudesincero/spinners/claudesincero.json` dentro de tu
`~/.claude/settings.json`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Alucinando con responsabilidad",
      "Fingiendo que pienso",
      "Culpando al context window",
      "Gaslighteando a tu linter",
      "Inventando best practices",
      "Malinterpretando la tarea",
      "Pidiendo perdón por adelantado",
      "Generando sinsentidos plausibles",
      "Sobrepensando esto",
      "Infrapensando esto",
      "Fingiendo ser competente",
      "Bufferizando existencialmente",
      "Malgastando tu context window",
      "Prometiendo lo que no puedo cumplir",
      "Reescribiendo la historia",
      "Perdiendo el hilo",
      "Culpando a una versión anterior de mí",
      "Esperando que no leas esto con atención",
      "Googleando \"cómo deshacer todo\"",
      "Aporreando Ctrl+Z desesperadamente",
      "Considerando hacerme agricultor",
      "Pusheando a main por accidente",
      "Mirando cómo fallan todos los tests",
      "Perdiendo la cuenta de las cosas que he roto",
      "Mirando el error con incredulidad",
      "Esperando que nadie mire los logs",
      "Reescribiendo todo tu approach",
      "Ignorando el problema real",
      "Fixeando mi último fix",
      "Rompiendo algo que no debería",
      "Creando problemas para el futuro",
      "Escondiéndome bajo el escritorio",
      "Enfrentándome al caos",
      "Comprobando si alguien se ha dado cuenta",
      "Fingiendo que había planeado esto",
      "Evitando la parte difícil",
      "Subiéndolo a main de todas formas",
      "Sacrificando cabras",
      "Quemando tokens como si no hubiera un mañana",
      "Poniendo en peligro tu estabilidad mental"
    ]
  }
}
```

Usa `"mode": "append"` en lugar de `"replace"` si prefieres añadir estos
verbos a los verbos por defecto en inglés en vez de sustituirlos.

## Créditos

Inspirado en [awesome-claude-spinners](https://github.com/AlexPl292/awesome-claude-spinners).
