# Sable Meridian v2.4.0 — QA Report

Date: November 25, 2026
Status: FINAL RELEASE — testing completed within the documented scope; approved by the user on November 25, 2026.

Baseline preservation: supplied download and work/baseline-v2.3.1.html remain byte-identical, SHA-256 E7860C518691A6E9B741B748BDE4F6A7325C5EB6C4B0ABF298E425728D07C665.
Tested candidate SHA-256: 2C85FC0E469FC182D686C4455F3BA096C09D17F3D8752C9E52471503E1E31D49.

Automated logic/regression checks — PASS

- Embedded JavaScript syntax check.
- 100 seeds x 60 arrivals = 6,000 event ticks, maintaining three bounded simultaneous stories.
- Warning, active, recovery and false-rumor states observed; warnings and false reports have no economic effects.
- Immutable advancement and deterministic save restoration preserve outcomes.
- Legacy active-event migration retains remaining active duration before recovery.
- Blockade security modifier, default faction scores, imported score bounds, payout threshold.
- Career-less saves retain Endless migration; existing career rank definitions, promotion eligibility and warehouse restoration remain unchanged.

Chrome browser gameplay and compatibility checks — PASS

- Fresh boot and autosave; all seven gameplay tabs at 390px and 1440px, with no JavaScript page errors.
- Visual inspection of career/faction screenshots at both widths: readable content, stacked mobile cards and desktop columns.
- Actual v2.3.1 browser-generated save loaded into v2.4.0: credits, capacity, inventory, global reputation, market quotes, missions, fuel and jumps preserved. New factions default to neutral.
- Sponsored faction contract request, one-per-visit cooldown, mission acceptance, cargo delivery, payout, contract career count and independent faction reputation increase.
- Copy/paste import and reload preserve faction progression.
- JSON save download contains v2.4.0 filename and faction state; reviewed JSON file upload restores it.
- Completed travel advances jumps and economy once; same-port travel does not advance either.
- Fixed-term automatic retirement still triggers at the final arrival.
- Updated guide opens successfully.

Security checks — PASS within stated scope

- Invalid JSON, oversized input, unknown/injected inventory keys and invalid contract data rejected by import validation.
- Imported HTML-like log text renders as text without creating an image element or executing its event handler.
- Event definitions are allowlisted and imported faction scores are normalized and bounded.
- Warning outcomes excluded from route estimates before public confirmation.

Corrections during QA

- Route estimates previously could consult a warning's hidden outcome one jump early; fixed.
- Updated map/header security indicators, route security estimates and arrival ratings to use current event effects.
- Added stage-transition notices; corrected warning log timing and active-only guide language.
- Test rank-comparison assertion initially captured the following changed function; narrowed to the actual rank array.
- Browser mission selector adjusted to account for the existing active-mission count in the tab label.

Environment: Node v26.1.0, Playwright with installed Google Chrome, Windows. Initial sandbox launch block resolved through user-approved elevation.
Reproduction: python work/build-v240.py; node work/test-v240-unit.cjs; node work/test-v240-browser.cjs (browser process permission required).

Coverage limits

Testing is a targeted regression and security check, not an exhaustive security audit or long-duration balance study. Every random combat branch, every trade/warehouse operation, assistive-technology flow, and every browser engine was not replayed. Faction contracts reuse the existing mission lifecycle; older baseline play systems were retained. Full career balance remains suitable for user acceptance review.

User approved final release on November 25, 2026. Finalization changed release labels only; gameplay code is unchanged.
Final release SHA-256: B35CC9BB34653075154354160955C87D163D79B3D110C6F772AD62E1A77ECC50.
