# Chip

A pill toggle for filters and small on/off choices — menu categories, dietary filters.

**Markup:** `<button class="body pdg-chip" aria-pressed="false">Oat milk</button>`; set `aria-pressed="true"` when selected (or use `role="checkbox"` with `aria-checked`).

**You provide:** a short label (an optional leading icon with `aria-hidden="true"`), and the handler that toggles `aria-pressed`.

- Resting: `surface` fill, `text` label, no outline, `radius-full`, `space-2` × `space-4` padding, weight 600.
- Selected: `accent` fill with an `on-accent` label (9.6:1). The accent is 1.2:1 against `background`, so the label — and a leading check icon where several chips sit together — carries the state as well.
- Focus: `focus-ring-width` `primary` ring, 2px offset.

On a white card, the resting chip has no visible edge; place chip rows on `background` or a `surface-sunk` well. Never use `accent` for the chip's text.
