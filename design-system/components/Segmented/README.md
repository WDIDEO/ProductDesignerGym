# Segmented

A pill-shaped switch between two to four modes or views of the same content — "Pickup | To table", "Day | Week".

**Markup:** `<div class="pdg-segmented" role="group" aria-label="Order type">` wrapping `<button class="body pdg-segmented__opt" aria-pressed="true">Pickup</button>` per option. Set `aria-pressed="true"` on the current option and `"false"` on the rest; inside a `role="tablist"` use `role="tab"` and `aria-selected` instead.

**You provide:** short option labels (one or two words), the group's `aria-label`, and the handler that moves `aria-pressed`.

- `surface-sunk` track, `radius-full`, `space-1` padding and gap.
- Options: 44px tall, `space-5` horizontal padding, `radius-full`, weight 600; resting label `text-muted` (4.8:1 on the track), `text` on hover.
- Selected: a raised `surface` segment with a `text` label — the shape change and the label carry the state, not colour alone.
- Focus: `focus-ring-width` `primary` ring, 2px offset.

Use it for switching modes, not for filters (use **Chip**) or for actions (use **Button**). Exactly one option is always selected.
