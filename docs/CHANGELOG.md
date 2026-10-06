# GameVault changelog

This changelog explains what changed in GameVault and what each change does. Changes are grouped by feature area, then version, starting at 0.3.4. Source links and test results are included. Release details were checked against the project and public downloads on 5 October 2026.

Version 0.3.9 is the latest verified release. The download and in-app update feed are available.

**Latest verified release:** 0.3.9  |  **Updated:** 6 October 2026

This public release history follows the maintained Markdown changelog. Internal/unreleased planning is not included.

**Contents**

- [1. Dashboard, navigation and Settings](#1-dashboard-navigation-and-settings)
- [2. Library connections and importing](#2-library-connections-and-importing)
- [3. Collection organization and last-played dates](#3-collection-organization-and-last-played-dates)
- [4. Personal recommendations and game discovery](#4-personal-recommendations-and-game-discovery)
- [5. Achievement tracking](#5-achievement-tracking)
- [6. Storefront wishlists and sale alerts](#6-storefront-wishlists-and-sale-alerts)
- [7. Themes, branding and installer appearance](#7-themes-branding-and-installer-appearance)
- [8. Languages and text handling](#8-languages-and-text-handling)
- [9. Cover artwork recovery](#9-cover-artwork-recovery)
- [10. Reliability, persistence and performance](#10-reliability-persistence-and-performance)
- [11. Updates and release publishing](#11-updates-and-release-publishing)
- [12. Testing, build tooling and documentation](#12-testing-build-tooling-and-documentation)
- [Earlier preview work first shipped publicly with 0.3.4](#earlier-preview-work-first-shipped-publicly-with-034)



## 1. Dashboard, navigation and Settings

<details>

<summary><strong>0.3.9</strong></summary>

- Fixed a dashboard that kept showing zero games and Explore demo after recovery and Steam reconnection in Settings, even though the games were saved. Saved games now appear without restarting.
- Added artwork and achievement task progress and Stop above the library. Blocked sync buttons explain which refresh is running; browsing and ordinary edits remain available while a provider request waits.

</details>

<details>

<summary><strong>0.3.8</strong></summary>

- Added Games and Achievements tabs at the top of the left library column, so achievement progress is easy to find.
- Added keyboard switching between the tabs. Recommendations stay on the right at desktop widths.
- Ctrl/Cmd+K now focuses store search when viewing Wishlist, so you can quickly find a new game.

</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Brought the overview, library, wishlist, sessions, suggestions and achievements onto one dashboard.
- Added shortcuts to dashboard sections and a Wishlist tab beside the library.
- Placed session history below your games. On mobile, it appears before suggestions and achievements.
- Kept the timer handy and let you open full session history on the dashboard. Filters keep your selected timer game.
- Moved the Settings cog beside the window controls and opened Settings in its own window.
- Made saved Settings changes appear on the dashboard without clearing unfinished edits.
- Kept normal window controls working. Update prompts wait while you are busy or Settings is open.

</details>

<details>

<summary><strong>0.3.5</strong></summary>

- Put your library, game suggestions and achievement progress in one view.
- Placed games on the left and suggestions on the right. Smaller screens stack the panels.
- Removed the separate achievement and game-picker pages. Old links now open Library.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added a familiar cogwheel icon for Settings.

Sources: Library companion guide, [0.3.7 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.7), 0.3.7 validation.

</details>

## 2. Library connections and importing

<details>

<summary><strong>0.3.7</strong></summary>

- Changed the button to Steam Connected after connection. It still opens Steam settings and returns to Connect to Steam after disconnecting.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added connections for installed games from Epic Games, Ubisoft Connect, GOG, EA app and Battle.net.
- Added Connect libraries in the library and connection controls in Settings.
- Let you find installed games on this PC without logging in or entering API keys.
- Added a review before import, manual refresh and a separate Refresh on launch option for each library.
- Let you choose custom game folders for Epic, GOG and EA.
- Prevented duplicate imports and matched existing games carefully. Unclear matches are skipped.
- Linked store copies to one game while keeping your notes, covers, ratings, prices, tags, sessions and playtime.
- Showed where each game came from and kept that information after disconnecting a launcher.
- Kept previous installation information when a scan failed or was incomplete. Missing games stay in your collection.
- Made canceled folder choices and scans leave your collection unchanged, even if results arrive later.
- Made scans handle damaged launcher files safely and reject unsupported launchers or network folders.
- Removed outdated installation information when a game's Steam App ID changed or was cleared.

Sources: [0.3.4 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.4), 0.3.4 validation, Library regression results, [0.3.7 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.7).

</details>

## 3. Collection organization and last-played dates

<details>

<summary><strong>0.3.7</strong></summary>

- Added last-played dates at the bottom of game covers in every theme.
- Showed last-played dates beside games in list view and recommendation panels.
- Used dates from Steam and logged sessions, keeping the most recent available date.
- Added Last played sorting, with dated games first and unknown dates last.
- Left missing dates unknown. Playtime alone does not tell us when you last played.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added custom tags and filters for tags and game libraries.
- Added Installed and Missing covers shelves to help organize your games.
- Removed extra spaces and duplicate tags. Each game can have 12 tags of up to 32 characters.
- Included tags in backups and CSV imports and exports.


</details>

## 4. Personal recommendations and game discovery

<details>

<summary><strong>0.3.5</strong></summary>

- Suggested games using your playtime and favorite genres, with ratings and favorites providing extra guidance.
- Counted playtime once and stopped one heavily played game from dominating suggestions.
- Kept Wishlist and Dropped games out of preference calculations and respected your chosen genres.
- Suggested Backlog, Playing and On hold games that match your platform and genre filters.
- Gave normal picks a 25% chance to try another genre when suitable games are available.
- Added Surprise me and avoided repeating the same game when other choices exist.
- Explained each suggestion and kept recommendation calculations on your device.
- Added a collection of 46 game suggestions that works offline.
- Let the Windows app refresh suggestions from Steam, excluding unreleased games, DLC and bundles.
- Limited each refresh to 24 game pages and up to 12 valid suggestions.
- Left out games already recognized as owned, including copies on other platforms.
- Added links to official Steam pages and an Add to wishlist button that avoids duplicates.
- Saved suggestions across restarts and backups. Failed refreshes keep the previous suggestions.
- Added useful Steam genre information without replacing the genre you entered.

Sources: [0.3.5 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.5), Library companion guide.

</details>

## 5. Achievement tracking

<details>

<summary><strong>0.3.8</strong></summary>

- Added Steam achievement images, including gray images for locked achievements. Downloaded images are saved for offline viewing and backups.
- Kept hidden locked achievements behind a generic icon to avoid spoilers.
- Added Steam's global unlock percentage to each imported achievement, showing how common it is.
- Added Rarest first and Most common first sorting, alongside Unlocked first and Title A-Z. Missing percentages appear last, and your sort choice is saved.
- Expanded the achievement list with game filtering and 20 achievements per page.
- Kept saved progress and percentages when rarity information is unavailable. Image failures leave a generic icon and retry on the next progress refresh.

Sources: Achievement update, [Steam achievement and global percentage API](https://partner.steamgames.com/doc/webapi/ISteamUserStats).

</details>

<details>

<summary><strong>0.3.5</strong></summary>

- Added automatic Steam achievement information and progress using your existing Steam connection.
- Added refreshes after connection and on launch, plus manual refresh for all games or one game.
- Checked up to 30 games automatically or 100 manually, so large libraries update in manageable batches.
- Waited for other work to finish and limited automatic retries to once every six hours.
- Kept your manual achievements editable and Steam-synced achievements read-only.
- Updated existing achievements without creating duplicates.
- Hid spoilers for locked secret achievements and clearly marked missing unlock dates.
- Kept saved progress when Steam was private, unavailable or returned incomplete information.
- Stopped late results from a canceled request or a different game or profile from being saved.
- Kept each Steam account's progress separate. Saved achievements remain available offline after disconnecting.

Achievements from other launchers still need to be entered manually.


</details>

## 6. Storefront wishlists and sale alerts

<details>

<summary><strong>0.3.8</strong></summary>

- Added game searches for Steam, Epic Games and GOG. Choose one store or all three and select the region for prices.
- Showed each result's store, available price, discount and official product link. Search lists up to 12 games per store, including upcoming Steam games.
- Added an Add to wishlist dialog with optional notifications, a discount threshold from 5% to 100%, and a region for that game. Alerts start only when you enable them.
- Extended manual and background price checks to games selected from Epic Games and GOG search, alongside Steam. Qualifying offers appear in the sale notification bell while the app is open.
- Selecting an already saved product edits its notification settings without adding a duplicate. You can save the same title separately for each store; owned Steam games are marked In your library.
- Kept Filter wishlist separate from store search, so you can still find games you have already saved.
- Searches and price checks use public store data without account sign-in or API keys. GameVault keeps your wishlist locally, and store prices do not change your recorded spending.
- Kept successful results usable if one store failed. Canceling a search or changing its title, store or region prevents old results from appearing. Failed saves keep your previous collection and allow a retry.


</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Let you choose Steam, Epic Games, Ubisoft, GOG, EA, Battle.net or a console store for wishlist games.
- Added official store links. Steam games can use an App ID or a Steam product link.
- Let you choose a sale threshold from 5% to 100% in 5% steps.
- Added Notify me in GameVault. A discount at or above your threshold qualifies, including temporary 100% discounts.
- Added Check wishlist offers and optional automatic checks while the app is open.
- Let you choose a Steam region and see prices in that region's currency. No Steam API key is needed.
- Checked up to 20 products every 15 minutes, with at least six hours between automatic checks of the same product.
- Added saved sale alerts and a notification bell beside Settings.
- Stopped repeated alerts for the same offer. Opening alerts marks them read; a later sale can trigger a new alert.
- Showed when an offer was last checked and linked to the official product page.
- Kept saved offers and alerts during failed checks. Late results cannot change games removed from the wishlist.
- Skipped discounts when Steam did not provide a valid paid offer for the selected region.

In 0.3.7, automatic sale alerts supported Steam while the app was open; other stores kept product links. The 0.3.8 changes above add searches and price alerts for Epic Games and GOG. GameVault does not change online wishlists or convert prices you entered yourself.


</details>

## 7. Themes, branding and installer appearance

<details>

<summary><strong>0.3.8</strong></summary>

- Added a shortcut repair tool for an old or blank GameVault icon in Windows Search. It uses the icon in the installed app and can restart the Search panel to refresh its display.
- Saved a backup of the shortcut before changing its icon. The repair keeps the app, collection and launch settings intact.

Sources: Windows Search icon repair guide, [Microsoft shortcut refresh guidance](https://devblogs.microsoft.com/oldnewthing/20150903-00/?p=91671/).

</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Made Calm darker, using slate and forest backgrounds, soft sage accents and off-white text.
- Removed bright glows, extra decoration and hover movement from Calm.
- Kept original cover colors and made date labels readable in every theme.

</details>

<details>

<summary><strong>0.3.6</strong></summary>

- Added Gaming, Dark, Light, Cozy and Calm to the Theme menu.
- Made Gaming navy and cyan, Dark charcoal and lavender, Light pale and purple, Cozy brown and peach, and the original Calm sage and teal.
- Applied each theme to the whole app, including forms, dialogs, badges, suggestions and achievements.
- Translated theme names and controls into all five supported languages.
- Remembered your theme through restarts and backups. Older backups use Gaming.
- Kept searches, unfinished Settings fields and open game editors when changing themes.
- Restored the previous theme if the new choice could not be saved.
- Improved text readability, keyboard focus and small-screen layouts. Controls follow the chosen light or dark theme.
- Added a matching controller-and-vault icon to the app, installer and uninstaller.
- Kept the installer in the Gaming theme, whichever theme you use in the app.


</details>

## 8. Languages and text handling

<details>

<summary><strong>0.3.8</strong></summary>

- Translated the main store-search and notification controls into Norwegian Bokmål, German, Spanish and French, alongside English.

</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Translated new controls as they appeared and updated the interface when you changed language, without redoing unchanged text.
- Kept special characters intact when long imported titles and descriptions had to be shortened.

Some detailed help and advanced messages are still in English.

</details>

<details>

<summary><strong>0.3.6</strong></summary>

- Translated theme names and controls.

</details>

<details>

<summary><strong>0.3.5</strong></summary>

- Translated the update prompt, including Install now and Later.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added English, Norwegian Bokmål, German, Spanish and French in Settings.
- Translated common menus, forms and connection controls. Dates and numbers follow your selected language.
- Remembered your language without changing the data used in backups and CSV files.
- Kept your game titles, notes, tags and achievement text exactly as you wrote them.

Sources: Library regression results, Maintenance results, [0.3.7 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.7).

</details>

## 9. Cover artwork recovery

<details>

<summary><strong>0.3.8</strong></summary>

- SteamGridDB is now the only service used to find new covers. Connect its free API key before searching.
- Completely removed AI cover setup, generation, labels, research fields and old preferences, plus Steam default cover downloads and their metadata support.
- Cover settings and backups now support SteamGridDB and custom images only. Missing matches and failed replacements keep your current supported image.
- Background searches after Steam sync or CSV import wait until SteamGridDB is connected. New covers keep their contributor credit and work offline.

</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Kept missing-cover searches running when AI generation failed or the account had access or billing problems.
- Skipped further AI requests in that scan and continued searching for existing artwork.
- Retried SteamGridDB for the affected game when it was connected.
- Explained why AI was skipped and credited community artwork correctly.
- Kept existing covers safe and respected the Stop action and AI attempt limit.

In that version, SteamGridDB needed its free API key and optional AI covers needed separately paid OpenAI API access. The 0.3.8 changes above remove the AI option.

Source: [0.3.7 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.7).

</details>

## 10. Reliability, persistence and performance

<details>

<summary><strong>0.3.9</strong></summary>

- Kept collection updates connected after an unreadable startup save or a recovery reset. A valid recovered collection clears recovery mode and resumes normal services and saves.
- Prevented delayed window updates from replacing newer saved edits. Invalid incoming collections leave the valid displayed collection intact. Deferred dashboard updates appear after leaving a field or closing a dialog, while unfinished Settings fields stay intact.
- Made Stop pause the rest of the automatic genre and achievement refresh pass, so stopping one stage does not immediately start the next. Canceled results are ignored when an in-flight request finishes.

</details>

<details>

<summary><strong>0.3.8</strong></summary>

- Cover progress and completed results now appear correctly in Settings as well as the dashboard.
- Steam achievement images download only for visible rows, in small batches, and are saved with the collection.
- Saved each wishlist product's store identity and notification region across restarts and backups. Failed or mismatched price responses cannot replace its saved offer.
- Kept existing Steam alert records, so an unchanged offer already reported by 0.3.7 does not notify you again after upgrading.

</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Reduced repeated playtime checks and game searches to improve large-library performance.
- Updated only the changing timer text during play sessions.
- Updated playtime totals immediately after editing or deleting sessions.
- Kept the previous sort order if the new choice could not be saved.
- Applied a backup's saved sort order as soon as it was restored.
- Restored launcher checkboxes when their new settings could not be saved.
- Kept a launcher connected if disconnecting failed and showed the failure correctly.
- Stopped older scan, sale and window results from replacing newer collection changes.

The changes in these earlier released versions preserved existing games, covers, notes, sessions and settings. The 0.3.8 cover changes above remove the old provider settings and metadata.

</details>

<details>

<summary><strong>0.3.6</strong></summary>

- Stopped automatic game and cover refreshes from clearing unfinished Settings edits.
- Made late connection-status updates change only their own Settings panel.


</details>

## 11. Updates and release publishing

<details>

<summary><strong>0.3.9</strong></summary>

- Published the recovery and background sync hotfix with the Windows installer, update signature, update information and checksum file. It is available through the existing in-app updater.
- Downloaded all four public files and checked their sizes and checksums. Confirmed that the latest update feed serves the exact verified 0.3.9 update information.

Sources: [0.3.9 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.9), Production validation.

</details>

<details>

<summary><strong>0.3.8</strong></summary>

- Published the checked Windows installer with its update signature, update information and checksum file. The download is available through the existing in-app updater.
- Downloaded all four published files and checked their sizes and file checksums. Confirmed that the public update feed serves the same 0.3.8 update information.

Sources: [0.3.8 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.8), 0.3.8 production validation.

</details>

<details>

<summary><strong>0.3.6</strong></summary>

- Made the publishing result link to the final public release page.

All six releases include signed update files. Public downloads and update checks were verified.

Windows publisher signing is still not set up. Updates are checked with GameVault's own signing key, keep your collection and create a local backup first.

</details>

<details>

<summary><strong>0.3.5</strong></summary>

- Showed release notes with Install now and Later when an update was found on launch, once per version per launch.
- Waited while you were busy and stayed quiet when offline or already up to date. Updates require your choice.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added a clear release request that can start publishing a verified build. Manual runs still prepare a draft by default.
- Checked that a release used the tested version and did not contain untested app changes.
- Checked all four release files: installer, update signature, update information and file checksum.
- Checked that the version, notes, links and file checks all matched before publishing.
- Prevented published installers from being replaced and blocked older releases from becoming the latest update.
- Checked the complete draft before publishing and confirmed the public update feed afterward.


</details>

## 12. Testing, build tooling and documentation

<details>

<summary><strong>0.3.9</strong></summary>

- Reproduced the empty dashboard with isolated copies of the saved data, then confirmed that the games were still saved. The owner verified that reopening the app restored the library. The installed collection and pre-update backup were inspected without changing them.
- Passed 562 local checks, including 23 new checks for recovery, separate-window imports, delayed updates, failed saves, unfinished fields, task status and Stop. Added three real Windows recovery checks to the disposable installer test suite.
- Made the Windows test runner wait for the recovery dialog before clicking its confirmation, avoiding a timing failure while still checking that the dialog opens.
- Passed 693 Windows preview checks and 701 production checks, including the actual installed app and three new recovery checks. The production installer also passed verification with the permanent update key.
- Updated installation instructions to the current installer, documented the background task controls, and saved the preview and production evidence.


</details>

<details>

<summary><strong>0.3.8</strong></summary>

- For the cover and achievement update, passed 509 local checks, including SteamGridDB setup and cover workflows, the left-side achievement tab, image caching, rarity sorting, backups and restart behavior.
- For that update, passed 630 checks on Windows, including 39 native code tests, installer checks, installed-app and reinstall tests, and 14 signed upgrade checks. The installer build passed too.
- Updated the guides, browser preview and Windows build checks for the cover and achievement changes.
- Checked the shortcut repair on the owner's installed 0.3.7 app. After refreshing the shortcut and restarting Search, the owner confirmed that the new controller icon appeared. This manual check is separate from the automated test totals above.
- Made the PDF more compact and added expandable bookmarks for categories, versions and individual changes, with direct links to each change.
- Passed 539 local checks after the wishlist update, including 30 new checks for store searches, notification rules, duplicates, existing Steam alert records, failed requests and saves, backups and narrow screens.
- Added wishlist checks and their reports to the Windows preview, release and local build workflows, and updated the browser preview and user guide.
- Passed 667 checks on Windows after the wishlist update, including 46 native code tests, installer checks, installed-app and reinstall checks, and 14 signed upgrade checks. The installer built successfully.
- Updated the app, installer and update labels to the same version, and prepared release notes for the store-search, cover and achievement changes.
- Passed 675 production checks, including the actual installer, installed app and verification with the permanent updater key. The separate versioned preview passed 667 checks, including signed upgrades.


</details>

<details>

<summary><strong>0.3.7</strong></summary>

- Added tests for the dashboard, last-played dates, sale alerts, cover recovery and separate Settings window.
- Checked large-library behavior with 500 games and 20,000 sessions.
- Made local Windows build checks run every relevant test outside the installed-app suite.
- Fixed the window-close test to check that the window actually closed.

</details>

<details>

<summary><strong>0.3.6</strong></summary>

- Added tests for all themes, readability, mobile layouts, backups and unfinished edits, plus theme saving in the installed Windows app.

</details>

<details>

<summary><strong>0.3.5</strong></summary>

- Added tests for recommendations, achievements and update prompts, including real Windows installs and upgrades. Kept test launches separate to avoid interference.

</details>

<details>

<summary><strong>0.3.4</strong></summary>

- Added tests for game imports, tags and languages, using realistic launcher files.
- Added release checks and verified that the finished installer had a valid update signature.
- Reorganized the guides and made older version notes easier to browse.

Test reports, file checks, build details, screenshots and update-feed checks were saved for every release.

| Version | Preview checks passed | Production checks passed |
| --- | ---: | ---: |
| 0.3.4 | 383 | 392 |
| 0.3.5 | 474 | 481 |
| 0.3.6 | 520 | 528 |
| 0.3.7 | 619 | 627 |
| 0.3.8 | 667 | 675 |
| 0.3.9 | 693 | 701 |

These totals come from separate test runs and should not be added together. Preview and production checks cover different steps. Automated tests use sample provider responses, without real accounts or paid AI requests. Real account behavior, system dialogs and wider Windows compatibility still need hands-on checks.


</details>

## Earlier preview work first shipped publicly with 0.3.4

<details>

<summary><strong>0.3.4</strong></summary>

These features were built for the 0.3.3 preview and first reached the public installer in 0.3.4:

- Added step-by-step Steam setup help beside both fields, with offline pictures and enlarged views.
- Used the original Steam logo and let you import installed Steam games without an API key.
- Added the earlier dark-and-lavender installer, later replaced by the Gaming design.
- Added optional AI covers with research links, an AI label and a limit on generation attempts.

Source: [0.3.4 release](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.4).

</details>
