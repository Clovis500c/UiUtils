# {{ page.title }}

!!! info "Method"
    `Toggle` turns the visibility of another UI element on or off when a button is clicked.

---

## Overview

The Toggle Method connects a **button** (`TextButton` or `ImageButton`) to a **target instance**. When the button is clicked, the target's visibility is toggled. The link between the button and the target is made through an **ObjectValue** inside the button.

---

## Setup

1. Add the `UiUtils` tag on your `TextButton` or `ImageButton`
2. Add Attribute `Method` = `Toggle`
3. Add an **ObjectValue** inside the button
4. Set the ObjectValue's `Value` to the instance you want to toggle

---

## Attributes

| Attribute | Type | Required | Description |
|---|---|---|---|
| `SwitchValue` | Boolean | :material-close: No | If set, forces the target to this value instead of toggling on/off |

---

## Supported Target Instances

The Toggle Method works with the following instance types:

| Instance | Property toggled |
|---|---|
| `ScreenGui` | `Enabled` |
| `Frame` | `Visible` |
| `CanvasGroup` | `Visible` |
| `ScrollingFrame` | `Visible` |
| `ViewportFrame` | `Visible` |
| `TextLabel` | `Visible` |
| `TextButton` | `Visible` |
| `TextBox` | `Visible` |
| `ImageLabel` | `Visible` |
| `ImageButton` | `Visible` |
| `VideoFrame` | `Visible` |

---

## Examples

**Toggle a Frame's visibility:**

- Tag: `UiUtils` on your button
- `Method` = `Toggle`
- ObjectValue inside the button → `Value` pointing to the Frame

**Force a ScreenGui to always enable on click:**

- Tag: `UiUtils` on your button
- `Method` = `Toggle`
- `SwitchValue` = `true`
- ObjectValue inside the button → `Value` pointing to the ScreenGui

---

## Notes

- The instance with the Toggle Method **must** be a `TextButton` or `ImageButton` — other instance types will be rejected
- The **ObjectValue** must be a direct child of the button and its `Value` must point to a valid instance
- The target instance must be one of the supported types listed above
- The connection is automatically cleaned up when the button is destroyed
- If the ObjectValue is missing: `No ObjectValue found for switch`
- If the ObjectValue has no Value: `No value found in ObjectValue`
- If the target type isn't supported: `No value found for InstanceType`
- If the instance isn't a button: `Your instance need to be a TextButton or an ImageButton`