# {{ page.title }}

!!! info "Method"
    `Gradient` applies an animated gradient effect to any UI element using the [ezVisualz](https://devforum.roblox.com/t/ezvisualz-uigradient-and-uistroke-effects-made-easy/2470313) library.

---

## Overview

The Gradient Method applies an **animated UIGradient** to your UI element using a built-in template. It automatically adjusts the element's color to white so the gradient renders properly, then applies the chosen effect with a smooth animation.

---

## Setup

1. Add the `UiUtils` tag on your UI instance
2. Add Attribute `Method` = `Gradient`
3. Optionally set a `GradientType` Attribute to choose which gradient to use

---

## Attributes

| Attribute | Type | Required | Default | Description |
|---|---|---|---|---|
| `GradientType` | String | :material-close: No | `Rainbow` | The name of the gradient template to apply |

---

## Available Gradient Templates

| Template |
|---|
| Bubblegum |
| Chrome |
| Death |
| Electric |
| Fire |
| Galaxy |
| Ghost |
| Gold |
| Green |
| Ice |
| Lava |
| Matrix |
| Neon |
| Oceanic |
| Rainbow |
| Silver |
| Sunset |
| Zebra |

---

## Examples

**Apply a rainbow gradient (default):**

- Tag: `UiUtils`
- `Method` = `Gradient`

**Apply a fire gradient:**

- Tag: `UiUtils`
- `Method` = `Gradient`
- `GradientType` = `Fire`

**Apply a gold gradient:**

- Tag: `UiUtils`
- `Method` = `Gradient`
- `GradientType` = `Gold`

---

## Supported Instance Types

The Gradient Method works on different instance types and adjusts the right color property automatically:

| Instance Type | Property set to white |
|---|---|
| `TextLabel` / `TextButton` | `TextColor3` |
| `ImageLabel` / `ImageButton` | `ImageColor3` |
| `Frame` | `BackgroundColor3` |

---

## Notes

- The element's color is **automatically set to white** so the gradient displays correctly — this is normal behavior
- If `GradientType` is not set, it defaults to `Rainbow`
- If the gradient template name is invalid: `[name] is not a valid gradient for [instance]!`
- Gradients are animated and pause automatically when the element is not visible
- Powered by [ezVisualz](https://devforum.roblox.com/t/ezvisualz-uigradient-and-uistroke-effects-made-easy/2470313) by arxkdev