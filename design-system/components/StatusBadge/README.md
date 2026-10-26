# StatusBadge

A small label that states a status with an icon and a word, coloured by `success`, `warning` or `error`.

**Markup:** `<span class="small pdg-badge pdg-badge--success"><svg aria-hidden="true">…</svg>Passed</span>`. Variants: `--success`, `--warning`, `--error`, `--neutral` (`text-muted`).

**You provide:** the word (required — colour never carries the status alone) and a matching 12px icon drawn with `currentColor`.

- `surface` fill, `border-width` outline and text in the status colour, `radius-1`, `small` type at weight 600, `space-1` × `space-2` padding.
- `success` for successful outcomes, `warning` for caution, `error` for errors; on `surface` they read at 5.1:1, 6.3:1 and 5.6:1.
- Keep the badge on a `surface` fill — `success` drops to 4.3:1 on `surface-sunk`.
- Keep the word short: "Passed", "Due soon", "Failed", "Draft".
