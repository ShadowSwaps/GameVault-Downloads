# Library recommendations and achievements

Library now combines the collection, **What to play**, **Discover new games** and **Achievements**. Recommendations and achievement progress sit on the right at desktop widths and stack below the collection on smaller screens. The former standalone achievement and picker navigation entries are removed; legacy routes redirect to Library.

## What to play

Recorded playtime includes previously played hours and logged sessions, once. Games with more hours carry more influence, with a square-root weighting to keep one very long game from overwhelming the rest of the collection. Wishlist and Dropped games do not determine taste. Owner genres take precedence over fetched metadata. Favorite flags and ratings provide small secondary signals.

Suggestions include Backlog, Playing and On hold. Explicit platform and genre choices always apply. A normal pick has a 25% chance to explore outside the leading genre when an eligible alternative exists. **Surprise me** selects randomly among eligible games. Immediate repeats are avoided when other choices exist. Nothing launches automatically.

The picker explains whether a suggestion follows recorded playtime, introduces variety or is a starting point with little history. Scoring runs on the device; no playtime, notes or session history is sent to a recommendation service.

## Discover games outside your library

A 46-game starter catalog works offline. Each identity and title was checked against official Steam metadata on 2026-10-04. Genre groupings add familiar play styles such as Shooter and Puzzle to Steam's broader genre labels. The starter catalog is included with GameVault.

**Refresh game suggestions** in the Windows app reads Steam's public featured catalog and validates individual app metadata. Only released Windows games with supported genres are accepted; DLC, bundles and invalid identities are excluded. The native request reads at most 24 candidate pages and retains at most 12 valid results. Cached results survive restart and JSON backups. Provider errors leave the previous catalog intact.

Known Steam identities and normalized owned titles are excluded, including games recorded on another platform. Suggestions may include a game already on the wishlist because it is not owned; adding it again is disabled. An untracked or differently named store purchase cannot be recognized until it is imported into GameVault.

The first recommendations follow your preferences, with a varied final suggestion. **Official game page** opens the game's HTTPS Steam store page in the default browser. URLs are constructed from numeric App IDs; provider-supplied links are ignored. **＋ Wishlist** saves a suggestion without marking it owned.

Steam imports without a genre can gain metadata for recommendations without overwriting the owner's Genre field. The most-played linked games are prioritized. Public store requests contain only App IDs and fixed metadata parameters; Steam keys are never sent to the store host.

Steam's public storefront endpoints are not a documented Steamworks API contract. They may change. The bounded native parser, cached catalog and offline starter catalog provide a fallback. No price or availability guarantee is displayed; the official page provides current regional information.

## Achievement syncing

Steam uses the saved Steam Web API key and profile from the existing connection. The native reader combines [GetSchemaForGame](https://partner.steamgames.com/doc/webapi/ISteamUserStats#GetSchemaForGame) with [GetPlayerAchievements](https://partner.steamgames.com/doc/webapi/ISteamUserStats#GetPlayerAchievements) by stable achievement ID. It reads progress; it never unlocks achievements on Steam.

Automatic refresh is enabled by default for connected API profiles and can be disabled in the Library panel. It runs after connection/sync and on launch for stale games, while no other task, modal or session is active. Requests are sequential. Automatic passes cover up to 30 games; manual passes cover up to 100. Oldest attempts are prioritized so larger libraries advance over successive passes. Successful progress and unavailable attempts have a six-hour automatic retry interval. **Refresh Steam achievements** in game details targets one game.

Manual achievements remain separate and editable, even when they share a title with imported achievements. Steam rows are read-only and identified by game, account, App ID and achievement ID. Repeated refreshes update records without duplication. Hidden locked achievements conceal their title and description. Unknown unlock dates are labeled as unavailable.

Private, incomplete or invalid responses preserve cached progress. Stopped requests cannot attach late results. Changed game identities and switched profiles are checked before saving. Previous-account progress stays in backups but is hidden when another account is active. Disconnecting preserves cached progress for offline viewing.

### Other connected libraries

| Library | Current achievement support | Reason / next requirement |
| --- | --- | --- |
| Steam | Automatic and manual refresh of account progress | Existing user API key and public game details. |
| Epic Games | Manual tracking | EOS achievements operate inside a product/deployment and require product-specific client policies and user identity. The installed-game scanner has no account authorization. |
| GOG | Manual tracking | The official GALAXY SDK uses client credentials issued per developed game, rather than a general key for all owned games. |
| Ubisoft Connect / EA app | Manual tracking | Current connections read installed-game metadata and do not supply authenticated achievement progress. No supported general account-wide reader was verified for this update. |
| Battle.net | Manual tracking | Blizzard exposes game-specific APIs for selected titles, requiring a separate API/OAuth and game-profile connection. The current installed-game connection has no account or character identity. |

Primary references: [Steam user statistics API](https://partner.steamgames.com/doc/webapi/ISteamUserStats), [Epic achievements interface](https://dev.epicgames.com/docs/epic-online-services/player-and-game-data/achievements-interface), [Epic client-policy setup](https://dev.epicgames.com/docs/epic-online-services/player-and-game-data/leaderboards-interface/leaderboards-guide/set-up-leaderboards), [GOG GALAXY credentials](https://docs.gog.com/galaxyapi/), [Battle.net developer authentication](https://community.developer.battle.net/documentation/guides/using-oauth).

This update does not extract launcher login tokens or copy achievement progress from one store to another. Steam and store fixtures exercise the flows without live owner accounts or paid AI requests. Wider compatibility and live-account privacy settings remain hands-on checks.
