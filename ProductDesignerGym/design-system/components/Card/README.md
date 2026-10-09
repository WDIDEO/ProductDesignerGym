# Card

A `surface` container that groups one piece of content — a challenge, a submission, a stat.

**Markup:** `<article class="pdg-card">` with `<h3 class="h4 pdg-card__title">`, `<p class="caption pdg-card__meta">` (`text-muted`), `<p class="body pdg-card__body">` and `.pdg-card__actions`. Add `pdg-card--panel` for larger panels (`radius-4`).

**You provide:** the content and at most one primary action per card; the parent layout sets the card width and the `space-4` gap between cards.

- `surface` on `background`, `border-width` `border` outline, `radius-3`, `space-5` padding, `space-3` between parts.
- Use `radius-4` (`--panel`) for large cards and panels; keep related cards on the same radius.
- No coloured left-edge accents or shadows — status goes in a **StatusBadge**.
