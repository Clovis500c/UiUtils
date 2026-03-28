# {{ page.title }}

!!! info "Method"
    `Hover` adds a smooth hover animation to any UI element — it grows when the mouse enters and returns to its original size when the mouse leaves.

---

## Overview

The Hover Method creates a **tween-based size animation** on mouse enter/leave. When the player hovers over the element, it smoothly scales up. When the mouse leaves, it returns to its original size. The animation uses **Quad easing** for a natural feel.

---

## Setup

1. Add the `UiUtils` tag on your UI instance
2. Add Attribute `Method` = `Hover`
3. Optionally tweak the animation with the Attributes below

---

## Attributes

| Attribute | Type | Required | Default | Description |
|---|---|---|---|---|
| `SizePercent` | Number | :material-close: No | `1.3` | How much the element scales on hover. `1.3` = 130% of original size |
| `Duration` | Number | :material-close: No | `0.15` | Duration of the animation in seconds |

---

## Examples

**Default hover effect (grows to 130%):**

- Tag: `UiUtils`
- `Method` = `Hover`

**Subtle hover effect:**

- Tag: `UiUtils`
- `Method` = `Hover`
- `SizePercent` = `1.1`

**Slow, dramatic hover:**

- Tag: `UiUtils`
- `Method` = `Hover`
- `SizePercent` = `1.5`
- `Duration` = `0.4`

---

## Notes

- The element's **original size** is saved when the game starts — the animation always returns to it
- The size is calculated using **Scale values** (`UDim2.Scale`), so it works best on instances sized with Scale rather than Offset
- The animation uses `Enum.EasingStyle.Quad` with `EasingDirection.Out` for a smooth deceleration
- All connections are automatically cleaned up when the instance is destroyed