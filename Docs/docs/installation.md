# {{ page.title }}

!!! info "Installation Guide :material-download:"
    Follow these steps to get UiUtils up and running in your game. It only takes a minute!

---

## Requirements

Before you start, make sure you have:

- :material-check-circle: **Roblox Studio** installed and open
- :material-check-circle: A game project ready to work with

That's it — no plugins, no external tools, no dependencies.

---

## Step 1 — Download UiUtils

Head over to the GitHub Releases page and download the latest `.rbxm` file:

[:material-github: Download Latest Release](https://github.com/Clovis500c/UiUtils/releases){ .md-button .md-button--primary }

---

## Step 2 — Import into Roblox Studio

1. Open **Roblox Studio** and load your game
2. In the **Explorer** panel, navigate to **StarterPlayer → StarterPlayerScripts**
3. **Right-click** on `StarterPlayerScripts` → **Insert from File...**
4. Select the `.rbxm` file you just downloaded
5. You should now see the **UiUtils** module inside `StarterPlayerScripts`

!!! tip "Why StarterPlayerScripts?"
    UiUtils runs on the **client side** — it handles UI, which is purely local to each player. Placing it in `StarterPlayerScripts` ensures it loads automatically for every player who joins.

---

## Step 3 — You're done! :material-party-popper:

That's it! UiUtils is now installed and will run automatically when players join your game.

No scripts to write, no configuration files to edit. Just start tagging your UI instances with Methods and Attributes — check the **[FAQ](faqs.md)** to learn how, or explore the **Methods** section in the sidebar.

---

## Updating UiUtils

When a new version is released:

1. Download the new `.rbxm` from the [Releases page](https://github.com/Clovis500c/UiUtils/releases)
2. Delete the old UiUtils module from `StarterPlayerScripts`
3. Import the new file the same way as before

!!! tip "Keep your Presets and Tags"
    Updating UiUtils **does not affect** your Tags or Attributes on UI instances. Only the module itself gets replaced — your configuration stays intact.