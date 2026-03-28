# {{ page.title }}

!!! info "Method"
    `PromptPurchase` prompts the player to buy a Gamepass or Developer Product when a button is clicked.

---

## Overview

The PromptPurchase Method connects a **button** (`TextButton` or `ImageButton`) to Roblox's MarketplaceService. When clicked, it opens the native purchase prompt for either a **Gamepass** or a **Developer Product**.

---

## Setup

1. Add the `UiUtils` tag on your `TextButton` or `ImageButton`
2. Add Attribute `Method` = `PromptPurchase`
3. Add Attribute `Id` with the Gamepass or Product ID
4. Add Attribute `PurchaseType` with either `Gamepass` or `Product`

---

## Attributes

| Attribute | Type | Required | Description |
|---|---|---|---|
| `Id` | Number | :material-check: Yes | The ID of the Gamepass or Developer Product |
| `PurchaseType` | String | :material-check: Yes | Either `Gamepass` or `Product` |

---

## Examples

**Prompt a Gamepass purchase:**

- Tag: `UiUtils`
- `Method` = `PromptPurchase`
- `Id` = `123456789`
- `PurchaseType` = `Gamepass`

**Prompt a Developer Product purchase:**

- Tag: `UiUtils`
- `Method` = `PromptPurchase`
- `Id` = `987654321`
- `PurchaseType` = `Product`

---

## Notes

- The instance **must** be a `TextButton` or `ImageButton`
- `Id` must be a valid number — you can find it on the Gamepass/Product page on Roblox
- `PurchaseType` must be exactly `Gamepass` or `Product` (**case-sensitive**)
- The connection is automatically cleaned up when the button is destroyed
- If `Id` is missing: `No Id found in attributes`
- If `Id` isn't a number: `Your id need to be a number`
- If `PurchaseType` is missing: `No PruchaseType found in attributes`