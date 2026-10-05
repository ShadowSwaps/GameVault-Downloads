# GameVault development roadmap

The owner adopted the expanded roadmap on **5 October 2026**. It is our working plan: **11 phases, 48 numbered items and 41 research topics**. All phases remain incomplete until their requirements and completion checks are verified.

![GameVault's six planned milestones, from foundation work in October 2026 to mobile and sync in May-August 2027](images/GameVault_Development_Timeline.png)

[Read the full development roadmap (PDF)](roadmap/GameVault_Development_Roadmap.pdf) · [Editable milestone data](roadmap/timeline.json)

## Major milestones

These are **estimated planning windows**, not promised release dates. They group the detailed roadmap without replacing its requirements or assigning future version numbers.

| Estimated window | Milestone | Main outcomes | Roadmap phases |
| --- | --- | --- | --- |
| October 2026 | Foundation and connections | In-app Settings, background work that survives panel closure, better backups, responsive layouts, five themes with Comfort, unified library connections and verified provider limits. Account and sync architecture is designed early. | 1-2 |
| November 2026 | Play and collection | Safe supported game launching, optional automatic session tracking, clearer play history, Installed then Uninstalled sorting, game detail panels and reviewed bulk changes. | 3-4 |
| December 2026 | Progress and value | Better SteamGridDB/custom artwork handling, per-game achievement details and refresh status, reliable price and purchase records, and library-value estimates that show their data coverage. | 5-7 |
| January-February 2027 | Discovery and wishlist | More useful recommendations, controlled suggestion history, search suggestions, cross-store wishlist rules and clearer price targets. Closed-app alerts depend on approved services and demonstrated delivery behavior. | 8-9 |
| March-April 2027 | Desktop readiness | Optional accounts and their recovery flows, resumable local-or-connected onboarding, release/recovery checks, accessible interface polish and agreed feedback/reporting routes. Readiness must be demonstrated before announcing a wider launch. | 10, with gates across earlier phases |
| May-August 2027 | Mobile and sync | Phone/tablet experience, a versioned record API, protected sign-in, offline edits and conflict-safe cross-device synchronization after desktop stability is proven. | 11 |

These windows indicate delivery order rather than months of work reserved exclusively for each phase. Designs for accounts, privacy, offline synchronization and accessibility start in the foundation stage. Recurring maintenance, regression checks and security review apply throughout. Features already present are refined rather than counted as entirely new work.

## How the estimates were formed

GameVault already has local storage, backups, signed updates, launcher imports, five themes, recommendations, Steam achievements and three-store wishlist search. These foundations reduce the amount of new work required, while the remaining roadmap adds broader state, recovery, accessibility and provider checks.

The verified release record shows **six published iterations, 0.3.4 through 0.3.9, on 4-5 October 2026**. The 0.3.4 production run passed 392 checks; 0.3.9 passed 701 in its own run. These are separate suite totals, not cumulative tests or a productivity measurement. The short release burst included work prepared earlier and a recovery hotfix, so it is too small a sample to extrapolate a reliable calendar completion date.

The initial windows therefore use conservative effort ranges and dependency order, assuming steady work by the owner with Codex. They allow for review, Windows validation, fixes, provider investigations and usage-limit pauses. Earlier desktop milestones have narrower windows; online delivery and mobile have wider windows because services, target-platform capabilities and owner decisions remain open. Accelerate or move the estimates when actual phase progress justifies it, and review them after every major milestone.

Historical release evidence: [0.3.4](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.4), [0.3.5](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.5), [0.3.6](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.6), [0.3.7](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.7), [0.3.8](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.8), [0.3.9](https://github.com/ShadowSwaps/GameVault-Downloads/releases/tag/v0.3.9).

## Completion and boundaries

- Keep the detailed roadmap's dependency order and completion gates. No phase is complete merely because the timeline window has arrived.
- Keep practical local/offline use. Accounts, connected libraries and SteamGridDB setup remain optional.
- SteamGridDB is the sole automatic game-cover provider; custom uploads remain supported. Historical AI/store-cover text in the original roadmap is superseded by the current direction.
- Verify supported provider fields and launch/tracking behavior. Unsupported favorites, DLC, achievements or prices need visible fallbacks rather than invented coverage.
- Online alerts, account services and mobile synchronization require verified access and the owner's decisions before any cost commitment. No service or payment is selected by this timeline.
- Feedback and Bug Report destinations are decided with the owner when reached. Diagnostics remain reviewable and private unless the owner chooses to send them.
- Record exact completed version/date and validation evidence before marking a phase Done. Preserve the phase completion file and saved PDF checkboxes.

## Maintaining the showcase

Update `docs/roadmap/timeline.json`, this text companion and both GitHub README sections when actual progress or the estimates change. The PNG was made with the built-in ImageGen tool; its complete generation prompt is retained in `docs/roadmap/TIMELINE_IMAGE_PROMPT.txt`. Inspect any revised image for accurate dates, wording, legibility and landscape layout. Keep the same image path, and update the canonical changelog and PDF for implemented or meaningful documentation changes.
