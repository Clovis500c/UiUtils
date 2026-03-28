# {{ page.title }}

!!! info "Method"
    `Username` displays a player's username on a text element.

---

## Overview

The Username Method takes a `UserId`, fetches the player's **username**, and applies it to the instance's `Text` property. You can optionally format the text around the name.

---

## Setup

1. Add the `UiUtils` tag on your text element
2. Add Attribute `Method` = `Username`
3. Add Attribute `UserId` with one of the accepted values

---

## Attributes

| Attribute | Type | Required | Default | Description |
|---|---|---|---|---|
| `UserId` | Number / String | :material-check: Yes | — | The player to display. Accepts a raw UserId, `LocalPlayer`, or `Random` |
| `FormatedText` | String | :material-close: No | — | A format string where `%s` is replaced by the username. For example, `Welcome, %s!` becomes `Welcome, PlayerName!` |

---

## Examples

**Show the local player's name:**

- Tag: `UiUtils`
- `Method` = `Username`
- `UserId` = `LocalPlayer`

**Show a welcome message:**

- Tag: `UiUtils`
- `Method` = `Username`
- `UserId` = `LocalPlayer`
- `FormatedText` = `Welcome, %s!`

**Show a specific player's name:**

- Tag: `UiUtils`
- `Method` = `Username`
- `UserId` = `12345678`

---

## Notes

- The instance must have a `Text` property (`TextLabel`, `TextButton`, `TextBox`)
- If `UserId` is missing: `You have not set the UserId attribute.`