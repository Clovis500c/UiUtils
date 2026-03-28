# {{ page.title }}

!!! info "Preset"
    `DefaultButton` is a ready-made Preset that combines hover animation and toggle functionality in one tag.

---

## Overview

The `DefaultButton` Preset is designed for standard interactive buttons. Apply it with a single tag and your button gets a hover effect and toggle behavior out of the box.

---

## Included Methods

| Attribute | Method | Default Parameters |
|---|---|---|
| `Method` | **Hover** | `SizePercent` = `0.9` |
| `Method1` | **Toggle** | — |

---

## How to use

1. Select your `TextButton` or `ImageButton` in Roblox Studio
2. In the **Properties** panel, find the **Tags** section
3. Add the tag `DefaultButton`
4. Add an **ObjectValue** inside the button, pointing to the instance you want to toggle
5. Done! :material-check-circle:

---

## Customization

You can override any default value using **PresetModifiers**:

| PresetModifier | What it changes | Default |
|---|---|---|
| `PresetModifier_SizePercent` | How much the button shrinks on hover | `0.9` |

??? example "Example: Bigger hover effect"
    Want the button to barely shrink on hover?

    - Add Attribute: `PresetModifier_SizePercent` = `0.95`
    - The hover effect is now subtler, Toggle stays unchanged