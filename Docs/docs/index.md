# {{ page.title }}

!!! tip "Welcome! :wave:"
    You're looking at the official documentation for **UiUtils** — a free, open-source Roblox module that lets you build dynamic UI without writing a single line of code.

---

## What is UiUtils?

UiUtils is a **zero-code UI framework** for Roblox. Instead of scripting your interfaces, you configure everything directly in Roblox Studio using one **Tag**, **Attributes**, and **Methods**.

Tag your instance with `UiUtils`, set a few Attributes → UiUtils makes it work in-game. That's it.

---

## Why use UiUtils?

:material-xml: **No scripting required** — Everything is configured through Studio's Properties panel. No Luau, no LocalScripts, no headaches.

:material-lightning-bolt: **Fast to set up** — Tag an instance, set a few Attributes, and you're done. What used to take dozens of lines of code now takes seconds.

:material-puzzle: **Modular** — Each Method handles one specific behavior. Combine them freely to create complex UI without complexity.

:material-package-variant: **Presets** — Pre-configured bundles of Methods that you can apply with a single Attribute. Customize only what you need with PresetModifiers.

:material-account-group: **Beginner-friendly** — Designed for creators who want professional UI without a programming background.

---

## How does it work?

UiUtils is built around 3 simple concepts:

### 1. The `UiUtils` Tag

Every UI instance you want UiUtils to handle needs the `UiUtils` tag. This is the **only tag** you'll ever need — it tells UiUtils to look at that instance and process its Attributes.

### 2. Methods

Methods are the **engine** of UiUtils. Each one gives a UI element a specific behavior — loading an avatar, showing a username, adding a hover effect, toggling visibility, and more.

You assign Methods through Attributes that contain `Method` in their name (e.g. `Method` = `Avatar`, `Method1` = `Hover`).

### 3. Attributes

Attributes are **settings** attached directly to UI instances. They tell UiUtils which Methods to run and how to configure them.

Some Attributes are **dynamic**: type `LocalPlayer` as a value and UiUtils automatically replaces it with the current player's UserId at runtime.

---

## Quick example

Want to display each player's avatar on an `ImageLabel`? Here's all you need:

1. Add the `UiUtils` tag on your `ImageLabel`
2. Add Attribute `Method` = `Avatar`
3. Add Attribute `UserId` = `LocalPlayer`
4. Done — every player sees their own avatar :material-check-circle:

No scripts. No events. No `Players.LocalPlayer`. Just one tag and two Attributes.

---

## Available Methods

| Method | Description |
|---|---|
| :material-account-circle: **Avatar** | Loads a player's avatar image |
| :material-account: **Username** | Displays a player's username |
| :material-gradient-horizontal: **Gradient** | Applies a gradient effect |
| :material-cursor-default-click: **Hover** | Adds a hover animation |
| :material-chart-bar: **Leaderstats** | Displays leaderstat values |
| :material-information-outline: **PlaceVersion** | Shows the current place version |
| :material-cart: **PromptPurchase** | Prompts a purchase on click |
| :material-toggle-switch: **Toggle** | Toggles visibility of another element |

Each Method has its own dedicated page in the **Methods** section.

---

## Get started

Ready to try it out? Head over to the **[Installation](installation.md)** page to set up UiUtils in your game, or check out the **[FAQ](faqs.md)** if you have questions.