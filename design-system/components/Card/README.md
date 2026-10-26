# Card

A big white `surface` container that groups one piece of content — a challenge, a submission, a stat.

**Markup:** `<article class="pdg-card">` with `<h3 class="h4 pdg-card__title">`, `<p class="caption pdg-card__meta">` (`text-muted`), `<p class="body pdg-card__body">` and `.pdg-card__actions`. Add `pdg-card--panel` for large cards and panels (`radius-6`, `space-6` padding).

**You provide:** the content and at most one primary action per card; the parent layout sets the card width and the `space-4` gap between cards.

- `surface` on `background`, no border, `radius-5`, `space-5` padding, `space-3` between parts.
- Use `--panel` (`radius-6`, `space-6` padding) for large cards and panels; keep related cards on the same radius.
- A category card may run a gradient from its tint (`tint-coffee`, `tint-cold`, `tint-food`, `tint-bakes`) into `surface`; `text` and `text-muted` stay readable on every tint.
- No borders, shadows or coloured left-edge accents — the white-on-grey step and whitespace separate cards, and status goes in a **StatusBadge**.
