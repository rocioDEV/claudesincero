# spinner-español

Paquete de verbos de spinner en español para [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

Claude Code muestra un spinner con verbos rotativos mientras trabaja
("Thinking...", "Analyzing..."). Este repo reemplaza esos verbos por
frases en español neutro, usando la clave soportada `spinnerVerbs` de
`settings.json`.

## Instalación

### Skill (recomendado)

```bash
npx skills add <tu-usuario>/spinner-espanol
```

Luego pídele al agente "instala el spinner en español" — copiará el
paquete a tu `~/.claude/settings.json`. Para revertir, pide "quita el
spinner" o "restablece los spinners".

### Manual

Copia el contenido de `spinners/neutral.json` dentro de tu
`~/.claude/settings.json`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Pensando",
      "Revisando el código",
      "Analizando el problema",
      "Redactando la respuesta",
      "Verificando cambios",
      "Explorando el proyecto",
      "Preparando la respuesta",
      "Repasando los detalles",
      "Organizando las ideas",
      "Comprobando el resultado",
      "Aplicando los cambios",
      "Casi listo"
    ]
  }
}
```

Usa `"mode": "append"` en lugar de `"replace"` si prefieres añadir estos
verbos a los verbos por defecto en inglés en vez de sustituirlos.

## Créditos

Inspirado en [awesome-claude-spinners](https://github.com/AlexPl292/awesome-claude-spinners).
