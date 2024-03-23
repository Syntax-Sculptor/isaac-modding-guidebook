# Motivation

Although many games offer mod support, many find getting started with modding The Binding of Isaac: Repentance difficult. This is a result of a lack of beginner-friendly resources in text format and the game's notoriously limited API.

The aim of this guidebook is to provide a clear and simple introduction to modding The Binding of Isaac: Repentance. By the end of the guidebook, you should be equipped to start creating your own mods.

# Overview

This guidebook currently covers:

1. How to create a basic resource replacement mod

# Required Tools

To begin modding, you only need two things:

* [The Binding of Isaac: Repentance](https://store.steampowered.com/app/1426300/The_Binding_of_Isaac_Repentance/)
    * Console versions do not support modding.
    * This guide focuses on Repentance. Therefore, much of the information will not work on Afterbirth+ due to API changes.
* An **Integrated Development** (**IDE**)
  * Visual Studio Code is highly recommended for its robust tooling and extensive ecosystem. This guide assumes you are using VS Code, but you can still follow along with a different IDE.

It should be noted that this guidebook **won't** go over how to use an IDE. If you are using Visual Studio Code, a 7 minute video is provided in the "Other Useful Resources" section that goes over the basics.

# What about REPENTOGON?

This guide initially focuses on the vanilla API and does not immediately delve into REPENTOGON. However, REPENTOGON will be introduced and explored in a later chapter.

# ✨ Recommended Visual Studio Code Extensions

If you're using VS Code, consider installing these extensions:

* [Binding of Isaac Lua API](https://marketplace.visualstudio.com/items?itemName=Filloax.isaac-lua-api-vscode) - Provides API autocompletion and installs Sumneko's Lua LSP for linting and type annotation support.
* [StyLua](https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.stylua) - An opinionated Lua code formatter that enforces consistent code style.
* [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml) - Adds XML support to VS Code and allows you to use (Wofsauge's XML Validator.)[https://pypi.org/project/isaac-xml-validator/]

# Other Useful Resources

* [Learn Visual Studio Code in 7min](https://www.youtube.com/watch?v=B-s71n0dHUk) - A quick VS Code introduction.
* [Binding of Isaac: Lua Docs](https://wofsauge.github.io/IsaacDocs/rep/) - The API documentation. It should be treated as the holy bible for modding.
* [Slugcat's Repentance Modding Series](https://www.youtube.com/watch?v=rukHB48olG8&list=PLkIbky8_pFUpqAF9l7dh_YsEV-zpJ4q50) - A video series which also teaches you how to mod the game.
* [AgentCucco's Modding Series](https://www.youtube.com/playlist?list=PLUYzSIp7NO8cEer2FmtxSXlXoMFirvYDN) - A video series which covers Lua, an introduction to the game's animation editor, and a basic introduction to the modding API. Although this was made during the AB+ era, the material taught in this playlist still transfer well to Repentance.