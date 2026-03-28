# {{ page.title }}

!!! info "Method"
    `Leaderstats` displays a leaderstat value on a text element and updates it automatically when it changes.

---

## Overview

The Leaderstats Method reads a value from the player's `leaderstats` folder and displays it on a text element. It also **listens for changes** — whenever the leaderstat value updates, the text updates instantly.

---

## Setup

1. Add the `UiUtils` tag on your text element
2. Add Attribute `Method` = `Leaderstats`
3. Add Attribute `ObjectName` with the name of the leaderstat you want to display

---

## Attributes

| Attribute | Type | Required | Default | Description |
|---|---|---|---|---|
| `ObjectName` | String | :material-check: Yes | — | The name of the value inside `leaderstats` (e.g. `Coins`, `Kills`, `Level`) |
| `FormatedText` | String | :material-close: No | — | A format string where `%s` is replaced by the value. For example, `Coins: %s` becomes `Coins: 150` |

---

## Examples

**Show a player's coins:**

- Tag: `UiUtils`
- `Method` = `Leaderstats`
- `ObjectName` = `Coins`

**Show formatted kills:**

- Tag: `UiUtils`
- `Method` = `Leaderstats`
- `ObjectName` = `Kills`
- `FormatedText` = `Kills: %s`

---

## Notes

- The instance must have a `Text` property (`TextLabel`, `TextButton`, `TextBox`)
- The player must have a `leaderstats` folder — UiUtils waits up to **20 seconds** for it to appear
- The value inside `leaderstats` must match the `ObjectName` exactly (**case-sensitive**)
- The text **updates in real time** whenever the leaderstat value changes
- The connection is automatically cleaned up when the instance is destroyed
- If `ObjectName` is missing: `No ObjectName attribute found for leaderstats`
- If the value doesn't exist in leaderstats: `No object found with the name: ...`