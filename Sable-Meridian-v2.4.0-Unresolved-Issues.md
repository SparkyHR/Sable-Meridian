# Unresolved issues — v2.4.0

No blocking defects were found in the executed checks. The original browser-permission blocker has been resolved and the browser suite passes.

Remaining limitations for acceptance review:

- Faction economy balance has not undergone long-duration playtesting. Standing currently increases through successful contracts; faction standing does not impose new penalties or remove existing career opportunities.
- A sponsored-contract request is limited to one per port visit across all factions. This is intentional and described in this report; it prevents board spam.
- Tests cover Chrome and 390px/1440px layouts. Other browser engines and every random combat branch were not exhaustively tested.
- No downgrade guarantee: v2.3.1 remains preserved, but use a backup when returning to it; older builds do not preserve new faction/warning fields.

Final release approved by the user on November 25, 2026. The documented coverage and balance limitations remain applicable.
