# Button

Triggers an action; one visually dominant primary button per screen or task area.

**Markup:** `<button class="body pdg-btn pdg-btn--primary">Start workout</button>` — the `body` type style sets the label size; the button adds weight 600. Variants: `--primary`, `--secondary`, `--ghost`, `--destructive`. Disable with `disabled` (or `aria-disabled="true"` on a link).

**You provide:** the label (a verb first: "Start workout", "Submit critique"), an optional leading icon with `aria-hidden="true"`, and the click handler.

- Primary: near-black `primary` fill, `on-primary` (white) label (18.1:1), `primary-hover` on hover (11.4:1).
- Secondary: `surface` fill with a `border` outline that darkens to `text` on hover — used for everything that is not the main action. On a white card it reads by its label; don't rely on the outline alone.
- Ghost: `text` colour, underlined, for low-emphasis actions inside cards and toolbars; fades to `text-muted` on hover.
- Destructive: `error` fill with `on-primary` label (5.6:1); name what is destroyed ("Delete workout").
- Disabled: `surface-sunk` fill, `text-muted` label, no outline.
- `radius-full` (pill), 40px tall, `space-4` horizontal padding, `space-2` between icon and label.
- `border-width` outline (transparent unless secondary). Focus: `focus-ring-width` `primary` ring, 2px offset.

Don't put two primary buttons side by side, and don't use `primary-hover` as a resting colour.
