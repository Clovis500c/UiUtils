# {{ page.title }}

!!! info "Method"
    `PlaceVersion` displays the current game's version number on a text element.

---

## Overview

The PlaceVersion Method reads the game's `PlaceVersion` and displays it on a `TextLabel`, `TextButton`, or `TextBox`. If the game is running in Studio, it displays `Studio` instead.

---

## Setup

1. Add the `UiUtils` tag on your text element
2. Add Attribute `Method` = `PlaceVersion`
3. Optionally format the text with the Attribute below

---

## Attributes

| Attribute | Type | Required | Default | Description |
|---|---|---|---|---|
| `FormatedText` | String | :material-close: No | — | A format string where `%s` is replaced by the version. For example, `v%s` becomes `v12` |

---

## Examples

**Show just the version number:**

- Tag: `UiUtils`
- `Method` = `PlaceVersion`

**Show formatted version:**

- Tag: `UiUtils`
- `Method` = `PlaceVersion`
- `FormatedText` = `Version: %s`

**Show with a prefix:**

- Tag: `UiUtils`
- `Method` = `PlaceVersion`
- `FormatedText` = `v%s`

---

## Notes

- The instance must have a `Text` property (`TextLabel`, `TextButton`, `TextBox`)
- In Roblox Studio, the version displays as `Studio` instead of a number
- In a published game, it displays the actual `PlaceVersion` number