# {{ page.title }}

!!! info "Method"
    `Avatar` loads a player's avatar image onto an `ImageLabel` automatically.

---

## Overview

The Avatar Method takes a `UserId`, fetches the player's **headshot thumbnail** at 420x420 resolution, and applies it to the instance's `Image` property.

---

## Setup

1. Add the `UiUtils` tag on your `ImageLabel`
2. Add Attribute `Method` = `Avatar`
3. Add Attribute `UserId` with one of the accepted values below

---

## Attributes

| Attribute | Type | Required | Description |
|---|---|---|---|
| `UserId` | Number / String | :material-check: Yes | The player to display. Accepts a raw UserId, `LocalPlayer`, or `Random` |

---

## Examples

**Show the local player's avatar:**

- Tag: `UiUtils`
- `Method` = `Avatar`
- `UserId` = `LocalPlayer`

**Show a specific player's avatar:**

- Tag: `UiUtils`
- `Method` = `Avatar`
- `UserId` = `12345678`

**Show a random player's avatar:**

- Tag: `UiUtils`
- `Method` = `Avatar`
- `UserId` = `Random`

---

## Notes

- The instance **must** be an `ImageLabel` or any instance with an `Image` property
- The thumbnail type is **HeadShot** at **420x420** resolution
- If `UserId` is missing, you'll see a warning in the Output: `You have not set the UserId attribute.`
- If the avatar image fails to load, you'll see: `Failed to get image for UserId: ...`