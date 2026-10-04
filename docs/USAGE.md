# Using GameVault

[Back to GameVault](../README.md) · [Latest Windows release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/latest)

## Install and update

Download **GameVault_0.3.5_x64-setup.exe** from the [0.3.5 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.5), run setup, and open GameVault from the Start menu. Setup may need internet access to install WebView2 if that runtime is missing. The application stores your collection locally and runs offline after installation.

In the public Windows release, choose **Settings → Check for updates**, review the notes, then select **Update and restart**. Finish or discard a running session first. A local pre-update database backup is created and the existing collection is retained. Updater-enabled 0.3.2 installations can upgrade directly to 0.3.5.

GameVault 0.3.5 also checks at launch. When a newer version is confirmed, a pop-up shows its version and release notes with **Install now** and **Later**. The prompt waits for an open dialog, save or library task to finish. Later keeps the update available in the banner and Settings, and the same version will not prompt again until the next app launch. An offline check, a current version or a preview with updates disabled never opens this pop-up. Nothing installs without your choice.

Desktop preview installers have production updates disabled and need one manual installation of the public release. Windows publisher signing is not configured yet; the permanent updater key verifies update packages.

## Library companion

Library combines your collection with What to play, discovery and achievement progress on the right at desktop widths. [Read the recommendations and achievements guide](LIBRARY_COMPANION.md) for personal picks, new-game discovery, automatic Steam progress and supported stores.

## Start your collection

Choose **Explore demo**, add your own games, import a CSV, or connect a library. Set your display name, currency and language in Settings. Export a JSON backup regularly, especially before a major import or recovery.

## Collection and playtime

Dashboard, library, wishlist, add/edit/delete games, search, platform/status filters, ratings, notes, manual achievements, session logs, timer, random game picker, JSON backups, and CSV export.

The picker includes Backlog, Playing, and On hold. Previously played hours are added to logged sessions. Timed sessions round to the nearest minute, minimum one minute; timers over 24 hours must be discarded and logged manually. Prices are manually entered. Currency selection changes labels, not values. Demo game data is illustrative.

## Other PC libraries, tags and languages

Choose **Connect libraries** in Library or **Settings → Connected libraries**. Epic Games, Ubisoft Connect, GOG, EA app and Battle.net can import installed PC games without login or API keys. Each connection shows a review before saving. Epic, GOG and EA support custom folders. Source identities prevent repeated imports; a unique PC title can link a CSV entry or another store copy to the same game. Ambiguous titles are skipped. Notes, covers, ratings, statuses, favorites, prices, sessions and playtime remain unchanged.

These connections detect installed games on this PC. They do not import uninstalled purchases or account playtime. Enable **Refresh on launch** for individual connected libraries, or choose **Refresh connected libraries**. Complete scans update installation evidence; partial or unavailable scans keep previous flags. Absent games stay in the collection. Disconnecting keeps imported games and provenance. Refresh does not install or remove games and never requests paid AI covers. Steam's existing API connection still supports owned games and playtime.

The library has source and tag filters, **Installed** and **Missing covers** shelves, and editable custom tags. Steam games enter the Installed shelf after an installed-game scan, not merely because the API reports ownership. Tags accept up to 12 values of 32 characters, separated by commas; they survive JSON backups and CSV import/export. Tags, titles and notes are never translated.

**Settings → Your profile → Language** offers English, Norwegian Bokmål, German, Spanish and French. Choose a language and save preferences. Navigation, common forms, library controls and connection actions are translated; dates and numbers use the selected locale. Canonical collection values stay stable for CSV and backup compatibility. Detailed Steam tutorials, some long descriptions and provider messages currently retain an English fallback. Settings now uses a conventional cogwheel.

## Steam and cover artwork

Choose **Connect to Steam** in the library. The button uses Valve's original Steam logo. The default connection imports your full owned library and Steam playtime using your Steam profile URL and your own Steam Web API key. Both visible fields have a **Help** button that opens a separate step-by-step guide while keeping anything already entered. The guides include offline illustrations with numbered highlights and a larger view, and can open Steam's official pages in your browser or copy their links. They explain profile URL formats, key registration and Steam's game visibility settings. Preview the library, then choose **Connect & import**. Your existing API connection remains usable. Finish a running session before importing or reconciling playtime.

For installed games without an API key, expand **Use installed games on this PC instead · no API key**, choose **Find my Steam games**, and review the import. This detects the Steam folder from Windows and reads installed-game manifests, including other local Steam library folders. **Choose Steam folder** handles custom locations. Your chosen folder is saved for subsequent refreshes. Local import links Steam App IDs and keeps existing playtime; it does not fetch uninstalled owned games or Steam's total hours. Unreadable entries are reported, and games absent from a scan are never deleted.

Existing CSV entries without App IDs are linked only by a unique normalized exact title on PC or Steam Deck. Ambiguous matches are skipped. Notes, prices, ratings, statuses, favorites, covers, achievements and sessions are preserved. Steam API hours include already logged sessions and never reduce a larger local total.

Choose **Find missing covers**. Steam App IDs allow official portrait artwork without an artwork key. Optional **Connect SteamGridDB** adds title searches and community art with your own API key. Existing covers are preserved in bulk; open a game and choose **Replace cover artwork** for a replacement. Each completed cover is saved immediately, including when a batch is stopped.

### Optional AI cover fallback

In **Settings → Steam & cover artwork → Set up AI covers**, enter an OpenAI API key and enable the fallback. This uses separately billed API access and is disabled by default. When you click **Find missing covers**, Steam and SteamGridDB are tried first. If no artwork is found, the provider searches for that specific game, produces a sourced visual brief and generates one original portrait cover. Unverified research, authentication errors or provider billing limits do not produce a replacement.

The default cap is **3 AI attempts per run**, configurable from 1 to 10. Generation uses low image quality with one image per attempt. Attempts include failed requests; there are no automatic retries. Background cover checks only download existing artwork and never generate paid images. Stop prevents subsequent work and can prevent generation after research; an image request already sent can still finish and be billed. Interrupted requests should be checked in the provider dashboard before retrying.

Every AI cover has a small top-right **AI** mark baked into its saved pixels, plus an accessible indicator. Research sources and model attribution are available in game details and survive backups and restart. The default documented models are `gpt-6-astra` for web research and `gpt-image-2.5-flare` for images; advanced model settings accommodate account access. The provider receives only the game title, platform and optional Steam App ID. Game notes, history and Steam credentials are not sent.

All provider keys stay in Windows Credential Manager and are excluded from exports. They must be entered again on another computer. Covers are saved locally for offline use. Downloaded raster images are bounded and decoded before saving; backups retain the 25 MB collection limit.

The library opens in A–Z order with status shelves, labeled filters and persistent grid/list layout. Native Steam and AI connections require the Windows app; the browser HTML supports the collection and organization features.

## CSV import

Export a single worksheet from Excel as **CSV UTF-8**. Open **Settings → Import CSV**, choose the file, review the preview, and confirm. [CSV_Import_Template.csv](../CSV_Import_Template.csv) shows the supported columns.

Required header: `Title` (also accepts `Name`, `Game`, `Game Title`, or `Game Name`).

Optional headers: `Platform`, `Genre`, `Status`, `Hours`, `Price`, `Currency`, `Rating`, `Release`, `Notes`, `Steam App ID` (or `AppID`), `Tags`.

- Comma or semicolon separators, quoted text, and Norwegian decimal commas are supported.
- Release dates must be YYYY-MM-DD. Ratings are whole numbers from 0 to 10.
- Missing platform defaults to PC; status to Backlog; genre to Other; numeric fields to zero.
- Titles matching an existing title and platform are skipped, including duplicates within the file. Existing entries are never overwritten.
- Every reported error must be fixed before importing. An import is saved as one operation.
- Imported hours become previously played hours. Sessions and achievements are not recreated from CSV.
- A Currency column must match your current currency setting; prices are not converted.
- CSV export contains total hours and plain game fields. Use JSON backups to preserve the full collection, including covers, favorites, sessions, and achievements.

Direct `.xlsx` import is not included.

## Backups and recovery

Use **Settings → Export backup** to save the full collection, including covers, favorites, sessions and achievements. **Restore backup** brings it into the desktop app or browser copy. Export your current collection before replacing it. Provider keys are excluded and must be entered again on a new computer.

Open Settings → Recover previous save to review the last valid collection saved before your current one. Confirming replaces your collection and clears a running timer. Export your current collection first if you want to keep both versions. Recovery stores only one prior version and can be replaced by the next successful save. Browser profile deletion also removes the recovery copy.

If startup cannot read your save, recovery settings offer previous-save recovery, JSON backup restoration, and an explicitly confirmed fresh start. Export backup preserves the unreadable original for troubleshooting.

## Browser preview

The standalone **GameVault.html** supports the collection and organization features. Open it in Chrome, Edge or Firefox, then explore the demo or restore a JSON backup. It needs no installation, server, account or internet connection.

Keep the HTML at the same path and use the same browser profile. Private browsing or clearing browser data may remove saves. Native launcher connections and automatic Windows updates require the desktop app. The desktop and browser copies keep separate collections; use a JSON backup to move between them.

### Updating an old browser collection

Export a backup from your old copy first. Replace your old GameVault.html with this file at the same location. This version copies an existing localStorage save into IndexedDB automatically. The old copy is retained. If you use a new file location or browser, restore the backup from Settings. Avoid editing your collection in the old 0.1 app after upgrading: its saves do not synchronize with the upgraded app.

## Image and collection limits

Custom JPG, PNG and WebP images can be up to 8 MB. They are resized to a maximum of 600 pixels per side and converted to JPEG; originals are unchanged. Each stored cover is limited to 180,000 characters. Downloaded portrait art is resized to fit 600 × 900 pixels. The full collection and backup limit is 25 MB.

## Reporting a problem

Include your GameVault version, Windows version, the action you tried and what happened. A screenshot can help. Collection and backup files can contain personal notes, so share only what is needed.
