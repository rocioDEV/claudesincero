---
name: spinnerd
description: Installs or removes a Spanish-language spinner verb pack for Claude Code, replacing the default English status words ("Thinking...", "Analyzing...") with Spanish ones via the spinnerVerbs setting. Use when the user asks to install Spanish spinners, switch the spinner language, or remove/reset a spinner pack.
---

# Instalar spinners en español

Este skill instala un paquete de verbos de spinner en español para Claude
Code, usando la clave soportada `spinnerVerbs` de `~/.claude/settings.json`.

## Instalación

1. Lee el paquete disponible en `spinners/claudesincero.json` (relativo a la
   carpeta de este skill, es decir, junto a este `SKILL.md`).
2. Lee el archivo `~/.claude/settings.json` del usuario.
3. Copia el campo `spinnerVerbs` del paquete dentro de `settings.json`:
   - Si `spinnerVerbs` ya existe, reemplaza su valor.
   - Si no existe, créalo.
   - IMPORTANTE: no modifiques ningún otro campo de `settings.json`.
4. Confirma la instalación con:

   ```
   Spinner en español instalado correctamente.
   No hace falta reiniciar Claude Code — el cambio aplica de inmediato.
   ```

## Formato del paquete

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": ["Pensando", "Revisando el código", "..."]
  }
}
```

`mode` puede ser `"replace"` (sustituye los verbos por defecto) o
`"append"` (los añade a los verbos por defecto en inglés).

## Quitar el spinner en español

Si el usuario pide quitar o restablecer los spinners: lee
`~/.claude/settings.json`, elimina por completo el campo `spinnerVerbs` y no
toques ningún otro campo. Confirma con:

```
Spinner en español eliminado. Los spinners por defecto están de vuelta.
No hace falta reiniciar Claude Code — el cambio aplica de inmediato.
```
