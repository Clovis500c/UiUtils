# {{ page.title }}

!!! info "Welcome to the FAQ :wave:"
    New to UiUtils? You're in the right place! This page explains every concept in simple terms — no coding experience required. Can't find your answer? Reach out on the [DevForum](https://devforum.roblox.com/u/clovis500c/summary) or [GitHub](https://github.com/Clovis500c).

---

## :material-help-circle-outline: Getting Started

??? question "What is UiUtils?"
    UiUtils is a **free Roblox module** that lets you create dynamic, interactive UI **without writing a single line of code**. 
    
    Instead of scripting, you configure everything directly in Roblox Studio using one **Tag**, **Attributes**, and **Methods**. UiUtils reads them and does all the work for you.

    In short: tag your instance with `UiUtils`, set Attributes → UiUtils makes it work in-game. :material-magic-staff:

??? question "Do I need to know how to code?"
    **Nope!** That's the whole point of UiUtils. Everything is configured visually in Roblox Studio through the Properties panel. No scripts, no Luau, no headaches.

??? question "Is UiUtils free?"
    Yes, completely **free and open source**. :material-heart:

??? question "How does UiUtils work under the hood?"
    When the game runs, UiUtils automatically:

    1. Finds all instances tagged with `UiUtils`
    2. Checks if the instance has a `Preset` Attribute — if yes, applies all its default values
    3. Applies any `PresetModifier_` overrides you set
    4. Resolves **Custom Attributes** (e.g. `LocalPlayer` → actual UserId)
    5. Runs every **Method** found in the Attributes

    All of this happens instantly — you just set things up in Studio and UiUtils handles the rest.

---

## :material-tag-outline: The UiUtils Tag

??? question "What is the UiUtils Tag?"
    Every UI instance you want UiUtils to handle needs **one tag**: `UiUtils`.

    This is the only tag you'll ever need. It tells UiUtils: "hey, look at this instance and process its Attributes."

    Without this tag, UiUtils completely ignores the instance.

??? question "How do I add the UiUtils Tag?"
    1. Select your UI instance in Roblox Studio
    2. In the **Properties** panel, find the **Tags** section
    3. Add the tag `UiUtils`
    4. Done! :material-check-circle:

---

## :material-cog-outline: Methods

??? question "What is a Method?"
    A Method is what actually **makes things happen**. Each Method gives a UI element a specific behavior — like loading an avatar, displaying a username, or toggling visibility.

    Methods are assigned through **Attributes** that contain `Method` in their name.

??? question "How do I assign a Method?"
    1. Add the `UiUtils` tag on your instance
    2. Add an Attribute with `Method` in the name, and set its value to the Method you want

    | Attribute Name | Value | What it does |
    |---|---|---|
    | `Method` | `Avatar` | Loads a player's avatar image |
    | `Method` | `Username` | Displays a player's username |
    | `Method` | `Hover` | Adds a hover effect |

    You can assign **multiple Methods** by numbering them:

    | Attribute Name | Value |
    |---|---|
    | `Method` | `Hover` |
    | `Method1` | `Toggle` |

    UiUtils picks up anything with `Method` in the Attribute name and applies them all.

??? question "What Methods are available?"
    Here are 3 examples of built-in Methods:

    ---

    **:material-account-circle: Avatar**

    Loads a player's avatar image onto an `ImageLabel`.

    Required Attribute: `UserId` — the player whose avatar you want to display.

    ---

    **:material-account: Username**

    Displays a player's username on a `TextLabel`.

    Required Attribute: `UserId` — the player whose name you want to show.

    Optional Attribute: `FormatedText` — a format string where `%s` gets replaced by the name. For example, `Welcome, %s!` becomes `Welcome, PlayerName!`.

    ---

    **:material-toggle-switch: Toggle**

    Toggles the visibility of another UI element when a button is clicked.

    Requires an **ObjectValue** inside the button, pointing to the instance you want to toggle.

    Optional Attribute: `SwitchValue` — if set, forces the target to this value instead of toggling on/off.

    ---

    Check the **Methods** section in the sidebar for the full list.

??? question "Can I use multiple Methods on one element?"
    Yes! Just add multiple Method Attributes numbered like `Method`, `Method1`, `Method2`, etc. UiUtils applies them all.

---

## :material-format-list-bulleted: Attributes

??? question "What is an Attribute?"
    An Attribute is a **setting** you attach directly to a UI instance. UiUtils reads Attributes to know which Methods to apply and how to configure them.

    There are two kinds of Attributes in UiUtils:

    - **Method Attributes** — contain `Method` in the name, tell UiUtils *what* to do (e.g. `Method` = `Avatar`)
    - **Config Attributes** — everything else, tell the Method *how* to do it (e.g. `UserId` = `LocalPlayer`)

??? question "How do I set an Attribute?"
    1. Select your UI instance in Roblox Studio
    2. In the **Properties** panel, scroll down to the **Attributes** section
    3. Click the **+** button
    4. Give it a name, choose a type, and set a value
    5. UiUtils reads it automatically when the game runs

    !!! tip "Can't find the Attributes section?"
        It's at the very bottom of the Properties panel. Make sure you have an instance selected!

??? question "What are Custom Attributes (Dynamic Attributes)?"
    Custom Attributes are Attributes where the value **resolves automatically** based on the player.

    Instead of a fixed value, you type a **keyword** that UiUtils replaces at runtime:

    | You type... | UiUtils replaces it with... |
    |---|---|
    | `LocalPlayer` | The current player's UserId |
    | `DisplayName` | The current player's display name |

    ??? example "Example: Show each player's own avatar"
        1. Add an `ImageLabel` to your UI
        2. Add the `UiUtils` tag
        3. Add Attribute `Method` = `Avatar`
        4. Add Attribute `UserId` = `LocalPlayer`
        5. Every player sees **their own** avatar in-game :material-account-circle:

---

## :material-package-variant: Presets

??? question "What is a Preset?"
    A Preset is a **ready-made template** — a bundle of Methods with default settings already configured.

    Instead of manually adding multiple `Method` Attributes and configuring each one, you set **one Attribute** `Preset` = `PresetName` and everything is applied instantly.

??? question "How do I use a Preset?"
    1. Add the `UiUtils` tag on your instance
    2. Add an Attribute `Preset` with the Preset name as value (e.g. `DefaultButton`)
    3. Done! All the Methods and default parameters are applied automatically

??? question "Can I customize a Preset?"
    Yes! Add an Attribute named `PresetModifier_WhatYouWantToChange` to override specific defaults.

    ??? example "Example"
        Using the `DefaultButton` Preset but you want a bigger hover effect:

        1. Add the `UiUtils` tag
        2. Add Attribute `Preset` = `DefaultButton`
        3. Add Attribute `PresetModifier_SizePercent` = `0.95`
        4. The hover is now subtler, everything else stays default :material-check-circle:

    !!! tip "You only override what you need"
        Just add a PresetModifier for the setting you want to change — the rest keeps its defaults.

---

## :material-lifebuoy: Troubleshooting

??? question "Something isn't working, what do I do?"
    Quick checklist:

    - :material-check: Did you add the **`UiUtils` tag** on your instance?
    - :material-check: Did you add a **Method Attribute** (e.g. `Method` = `Avatar`) or a **Preset Attribute** (e.g. `Preset` = `DefaultButton`)?
    - :material-check: Are your Attribute names spelled correctly? (Attributes are **case-sensitive**)
    - :material-check: Did you set all **required Attributes**? (e.g. `UserId` for Avatar)
    - :material-check: Are your Attributes on the **right instance**?
    - :material-check: For Toggle: is there an **ObjectValue** inside the button pointing to the target?
    - :material-check: Is your instance a **supported UI type**? (Frame, TextLabel, ImageLabel, TextButton, etc.)
    - :material-check: Is UiUtils properly installed? (Check the [Installation](installation.md) page)

    !!! tip "Open the Output window"
        UiUtils includes built-in warning messages to help you debug. Open **View → Output** in Studio — you'll see clear error messages telling you exactly what's missing or misconfigured.

    Still stuck?

    - :material-forum: [DevForum](https://devforum.roblox.com/u/clovis500c/summary)
    - :simple-github: [GitHub](https://github.com/Clovis500c)

??? question "Where can I see all available Methods?"
    Check out the **Methods** section in the sidebar — each Method has its own dedicated page.