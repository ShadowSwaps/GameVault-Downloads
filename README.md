# GameVault

Your personal gaming library, with local saves, cover artwork and playtime tracking.

**[Download 0.3.9 for Windows](https://github.com/ShadowSwaps/GameVault-Downloads/releases/download/v0.3.9/GameVault_0.3.9_x64-setup.exe)** · [Release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.9) · [Changelog](docs/CHANGELOG.md)

**Windows x64 · Collection saved locally · Latest verified release: 0.3.9**

[Get started](#get-started) · [Features](#features) · [Development timeline](#development-roadmap) · [Help and release information](#help-and-release-information)

## Get started

1. Run the Windows installer and open **GameVault** from the Start menu.
2. Add games manually, import a CSV, or connect your Steam and installed-game libraries.
3. Use **Settings → Export backup** to keep an external copy of your collection.

<details>
<summary><strong>Updating, offline use and Windows setup</strong></summary>

Updater-enabled 0.3.2 installations can update directly to 0.3.9 through **Settings → Check for updates → Update and restart**. Finish any running session first. Browser copies and desktop previews need one manual installation of the public release to enable updates.

Setup may use the internet to install WebView2 if it is missing. After installation, your saved collection and cached artwork work offline. Store searches and provider refreshes need a connection.

Windows publisher certificate signing is not configured yet, so Windows may show an unknown-publisher prompt. GameVault's updater checks package signatures.

</details>

## Features

| Area | Available in 0.3.9 |
| --- | --- |
| Your library | Favorites, tags, ratings, notes, shelves, grid/list views, CSV transfers and backups. |
| Connections | Owned Steam games and installed PC games from Epic Games, Ubisoft Connect, GOG, EA app and Battle.net. |
| Artwork | SteamGridDB covers or your own images, saved for offline use. |
| Play and achievements | Sessions, playtime, recommendations, Steam achievement icons and rarity sorting. |
| Wishlist | Search Steam, Epic Games and GOG; save exact products with optional sale alerts. |
| Appearance | Gaming, Dark, Light, Cozy or Calm, plus five core interface languages. |

<details>
<summary><strong>Library connections and cover artwork</strong></summary>

- Imports show a review before saving and preserve existing notes, covers, ratings and sessions.
- Full Steam owned-library sync uses your Steam connection. Installed-game detection is a separate option.
- SteamGridDB is the only automatic cover provider and requires its free API key. Custom cover images are supported.
- Your collection stays on your device. Provider keys are kept out of collection backups.

</details>

<details>
<summary><strong>Wishlist alerts, achievements and background work</strong></summary>

- Wishlist searches use the selected store and region. Save an exact product and choose an optional discount threshold from 5% to 100%.
- Current price checks and notifications run while GameVault is open. They do not modify your online store wishlists.
- Achievements appear beside Games on the left. Cached Steam icons work offline; global unlock percentages support rarity sorting.
- Artwork and achievement refreshes show progress and **Stop**. Ordinary browsing and edits remain available while provider requests wait; another bulk refresh waits for the active task.

</details>

<details>
<summary><strong>Themes and languages</strong></summary>

Choose **Gaming, Dark, Light, Cozy or Calm** and **English, Norwegian Bokmål, German, Spanish or French**. Some detailed help and advanced messages remain in English.

Comfort preferences, optional accounts, mobile sync, the planned in-app Settings panel and closed-app/email alerts are future work.

</details>

## Development roadmap

[![GameVault development timeline: ten planned milestones from 0.1 through 0.9, then 1.0](docs/images/GameVault_Development_Timeline.png?v=99384b311bf9)](https://raw.githubusercontent.com/ShadowSwaps/GameVault-Downloads/main/docs/images/GameVault_Development_Timeline.png?v=99384b311bf9)

**[Open the timeline at full resolution](https://raw.githubusercontent.com/ShadowSwaps/GameVault-Downloads/main/docs/images/GameVault_Development_Timeline.png?v=99384b311bf9)**

The approved showcase groups the maintained plan into **ten milestones**, covering **15 phases, 58 items and 62 research topics**. Read the upper row from 0.1 to 0.5, then the lower row from 0.6 to 1.0. Every milestone is planned until its requirements and checks pass.

<details>
<summary><strong>Milestones and estimated windows</strong></summary>

| Target | Focus | Planning estimate |
| --- | --- | --- |
| 0.1 | Foundation and connections | October 2026 |
| 0.2 | Play and collection | November 2026 |
| 0.3 | Progress and value | December 2026 |
| 0.4 | Discovery and wishlist | January–February 2027 |
| 0.5 | Desktop readiness | March–April 2027 |
| 0.6 | Mobile and sync | May–August 2027 |
| 0.7 | macOS and Linux | September–November 2027 |
| 0.8 | Standalone Wishlist | December 2027–January 2028 |
| 0.9 | Friends and private chat | February–May 2028 |
| 1.0 | Open-source release | After all preceding completion gates |

These are planning estimates, not promised release dates. Platform support and online features depend on verified provider access, testing and owner decisions. Environmental reporting precedes the final approved public source release.

</details>

<details>
<summary><strong>Milestone versions and partial releases</strong></summary>

Completed milestones release as **0.1 through 0.9, then 1.0**. Partial releases use **0.0.1, 0.0.2, …** before the first milestone, then patches under the last completed milestone, such as **0.1.1** on the way to 0.2.

Existing 0.3.9 and earlier downloads keep their historical numbers. The installer/updater transition will be verified before the first renumbered release; these targets do not declare roadmap phases complete.

</details>

<details>
<summary><strong>Project direction and illustration credit</strong></summary>

GameVault's owner creates its ideas and directs the project. OpenAI tools assist coding, research and selected illustrations. The timeline scenery was edited with OpenAI ImageGen; its text and paths received a precise local finish.

The full working roadmap is internal. This repository presents the approved high-level timeline; earlier published roadmap documents are historical snapshots.

</details>

## Help and release information

**0.3.9 fixes the empty dashboard after recovery and Steam reconnection**, and makes background refresh progress and cancellation clearer. [Read the release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.9).

<details>
<summary><strong>Release files and verification</strong></summary>

| Verification | Checks passed |
| --- | ---: |
| 0.3.9 production Windows build | 701 |
| Separate Windows preview | 693 |

These are separate run totals and should not be added together. The installer, updater signature, checksums and update feed were verified. Automated checks do not replace real-account and wider Windows compatibility checks.

The [0.3.9 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.9) contains the installer, signature, update information and checksums. [Browse all releases](https://github.com/ShadowSwaps/GameVault-Downloads/releases).

</details>

<details>
<summary><strong>Reporting a problem</strong></summary>

Include your GameVault version, Windows version, the action you took, what you expected and what happened. Include a screenshot when useful, with personal information removed. Share collection data only when necessary.

Use the existing [issue tracker](https://github.com/ShadowSwaps/GameVault-Downloads/issues) for public reports. Planned in-app Feedback and Bug Report destinations will be agreed before implementation.

</details>
