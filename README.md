# GameVault

Your personal gaming library, with local saves, cover artwork and playtime tracking.

**[Download GameVault 0.3.4 for Windows](https://github.com/ShadowSwaps/GameVault-Downloads/releases/download/v0.3.4/GameVault_0.3.4_x64-setup.exe)** · [Release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/latest) · [User guide](docs/USAGE.md)

## Get started

1. Download and run the Windows x64 installer, then open **GameVault** from the Start menu.
2. Add games, import a CSV, or choose **Connect to Steam** / **Connect libraries**.
3. Use **Settings → Export backup** to keep a copy of your collection.

Updater-enabled 0.3.2 installations can go straight to 0.3.4 through **Settings → Check for updates → Update and restart**. Finish a running session first. Browser copies and desktop previews need one manual installation of the public release to enable future in-app updates.

## What you can do

- Organize a library and wishlist with favorites, custom tags, ratings, notes, shelves and grid/list views.
- Connect your owned Steam library, or import installed PC games from Epic Games, Ubisoft Connect, GOG, EA app and Battle.net.
- Find Steam and SteamGridDB cover artwork; optionally generate researched covers with a visible AI mark.
- Track sessions, playtime, achievements and cost per played hour, with JSON backups and CSV import/export.
- Choose English, Norwegian Bokmål, German, Spanish or French. Some detailed help and advanced messages use English.

Your collection is stored on your device. Launcher imports show a review before saving and preserve your existing notes, covers, ratings and sessions.

## New in each version

<details>
<summary><strong>New in 0.3.4</strong></summary>

- Five installed-game connections: Epic Games, Ubisoft Connect, GOG, EA app and Battle.net, without account login or API keys.
- Reviewed imports, manual refresh and optional refresh on launch for each connected library.
- Custom tags, library/tag filters, and **Installed** and **Missing covers** shelves.
- Five interface languages and a conventional settings cogwheel.
- Safer partial/unavailable scans that retain previous installation evidence; absent games remain in your collection.

The new launcher connections detect installed PC games. Steam retains its separate API connection for owned games and account playtime. This public release also includes all the 0.3.3 changes below.

[0.3.4 release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.4)

</details>

<details>
<summary><strong>New in 0.3.3</strong></summary>

- **Connect to Steam** with Valve's Steam logo and API setup as the default.
- **Help** beside the profile URL and API key fields, with step-by-step instructions, offline numbered illustrations and an enlarged view.
- A separate installed-Steam-game import option without an API key.
- Optional researched AI covers with a small top-right AI mark, saved sources and an attempt limit.
- A matching dark and lavender installer and uninstaller, with GameVault icons and artwork.

0.3.3 was a preview; these changes are included in the public 0.3.4 release. AI covers require your own separately billed OpenAI API account and stay disabled until configured. Background checks never generate paid images.

</details>

<details>
<summary><strong>New in 0.3.2</strong></summary>

- Steam owned-library import and playtime sync, with a review before importing.
- Official Steam covers and optional SteamGridDB community artwork, saved locally.
- Cleaner poster grid and compact list, status shelves, genre/platform filters and persistent layout/sort preferences.
- Steam App IDs in editing and CSV import/export.
- Provider keys stored in Windows Credential Manager and excluded from backups.

[0.3.2 release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.2)

</details>

<details>
<summary><strong>New in 0.3.1</strong></summary>

- In-app Windows updates, checked on launch or manually in Settings.
- Release notes and **Update and restart**.
- Verified updater signatures and a local database backup before installation.
- Collection, covers, favorites, sessions, achievements and preferences retained across updates.

[0.3.1 release notes](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.1)

</details>

<details>
<summary><strong>New in 0.3</strong></summary>

- Recover one previous valid save from Settings.
- Clear recovery choices when a save is unreadable, with confirmation before starting fresh.
- Invalid or failed saves leave the current collection intact.
- Editable imported playtime and price precision.
- Windows build helper, UTF-8 packaging and preserved browser-test diagnostics.

</details>

<details>
<summary><strong>New in 0.2</strong></summary>

- Local custom covers, favorites and rating sorting.
- Recent sessions, cost per played hour, a seven-day chart and a running-session reminder.
- **Ctrl/Cmd + K** library search.
- Reviewed CSV imports with row errors and duplicate detection.
- Browser IndexedDB storage, 0.1 migration and atomic save conflict protection.
- Automated browser and native storage checks.

</details>

## Help and updates

[User guide](docs/USAGE.md) · [CSV import template](CSV_Import_Template.csv) · [All releases](https://github.com/ShadowSwaps/GameVault-Downloads/releases)

Download the **.exe installer** from a release's Assets section. GameVault saves your collection on this device; use **Settings → Export backup** to keep an external copy.

The 0.3.4 production Windows build passed **392 checks**, including browser workflows, native storage, installer interaction and the installed app. Its final installer was verified with GameVault's permanent updater key, and the public update feed was checked.

Windows publisher signing is not configured yet, so Windows may show an unknown-publisher prompt. Setup may need internet access to install WebView2 if the runtime is missing. GameVault runs offline after installation.

For feedback, include your GameVault version, Windows version, the action you tried and what happened. Share personal collection data only if needed.
