# Sable Meridian v2.4.0 — Changelog

Status: FINAL RELEASE — approved by the user on November 25, 2026.

- Preserved the supplied v2.3.1 baseline byte-for-byte (SHA-256 E7860C518691A6E9B741B748BDE4F6A7325C5EB6C4B0ABF298E425728D07C665).
- Added advance planetary warnings, 50–90% confidence, authority/relay reliability labels, and persistent true/false outcomes. Warnings last 2–4 completed arrivals.
- Added warning, active, three-jump recovery, and disproved-report presentations. Recovery effects fade; false reports have no price or security effects.
- Added independent Global Federation, Forge Consortium, and Frontier Compact reputations. Contract completions add +2 to the relevant faction, capped at 100.
- Added sponsored contracts at reputation 5, faction payout premiums at 10, and partner requisitions at 20. Contracts use existing mission cargo, expiration, acceptance and completion systems.
- Added event-dependent destination piracy and enforcement during travel, with fading recovery effects.
- Extended the trade bulletin, career interface, player guide, and save export version labels.
- Retained career schema version 1; missing faction scores default to neutral. Legacy events retain their remaining active period before recovery. Existing market quotes are preserved on load.
- Existing career ranks, opportunities, warehouses, ship mechanics, and global reputation remain available.
- Prevented route estimates from consulting unrevealed warning outcomes.

- QA corrections: event-adjusted map and route security indicators, stage-transition notices, and clearer warning timing.
