# {{ page.title }}

!!! info "Custom Attribute"
    `UserId` is a **dynamic Attribute** — instead of hardcoding a player's ID, you can use keywords that UiUtils resolves automatically at runtime.

---

## Overview

The `UserId` Attribute is used by several Methods (like **Avatar** and **Username**) to identify which player to target. It accepts both static values and dynamic keywords.

---

## Accepted Values

| Value | Type | What it resolves to |
|---|---|---|
| `12345678` | Number | Uses that exact UserId directly |
| `LocalPlayer` | String | The current player's UserId |
| `Random` | String | A random player's UserId from the server |

!!! warning "Invalid values"
    If you type a string that isn't `LocalPlayer` or `Random` and isn't a number, UiUtils will show a warning in the **Output** and fall back to a random player's UserId.

---

## Usage

Add a `UserId` Attribute on any UI instance that uses a Method requiring it:

1. Select your UI instance in Roblox Studio
2. In the **Properties** panel, scroll down to **Attributes**
3. Click **+**, name it `UserId`, set the type to **String** or **Number**
4. Set one of the accepted values above

---

## Examples

**Show the local player's avatar:**

- Attribute `Method` = `Avatar`
- Attribute `UserId` = `LocalPlayer`

**Show a specific player's username:**

- Attribute `Method` = `Username`
- Attribute `UserId` = `12345678`

**Show a random player's avatar:**

- Attribute `Method` = `Avatar`
- Attribute `UserId` = `Random`