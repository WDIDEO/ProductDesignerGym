A light, open system for Product Designer Gym: interfaces that feel like a bright training floor for design skills — a soft light-grey canvas, big white rounded cards, near-black pill buttons, one lime accent for "you" and "selected", and plain, confident DM Sans type.

## Brand

- Write the name as **Product Designer Gym** — three words, title case, never abbreviated in UI copy.
- The logo is a photographed neon sign: a flexed-arm icon inside a design-tool selection frame (corner handles), a sparkle and a cursor, over the stacked wordmark. Use `product-designer-gym-neon.png` from **Logos** as a hero or brand image. It carries its own dark brick-wall backdrop, so show it as a rounded image card (`radius-5` or `radius-6`, no border) — never cut it out as a mark on the light canvas, and never crop the sign's glow tightly.
- The sign's violet sparkle, pink frame and orange cursor belong to the logo image only. They are **not** UI colours: interfaces use the tokens below.
- No vector mark has been supplied, so there is no small-size logo or favicon yet. Do not redraw the sign; set the name in `h4` / `text` where a compact mark is needed.

## Colour

The system has one theme, **Light** (`[data-theme="light"]`).

- Paint the app canvas `background` (soft light grey); cards, modals, panels and input fields `surface` (white). Use `surface-sunk` for wells, the segmented-control track and disabled fills.
- Set headings and body copy in `text` (16.5:1 on `background`, 18.1:1 on `surface`, 15.2:1 on `surface-sunk`); secondary text, hints, descriptions and section labels in `text-muted` (5.2:1 / 5.7:1 / 4.8:1).
- Use `primary` (near-black) for primary actions and active elements, and `primary-hover` only for their hover state — it is not a second brand colour. `primary` matches `text`, so underline links rather than relying on colour.
- Label any `primary`, `primary-hover` or `error` fill with `on-primary` (white): 18.1:1, 11.4:1 and 5.6:1.
- Use `accent` (lime) as a fill for selection and "you": selected chips, the current step, the location pill. Label it with `on-accent` (9.6:1). Never use `accent` for text or icons on a light ground — it is only 1.2:1 against `background` — so an accent fill always carries a text label or an outline as well.
- The category tints `tint-coffee`, `tint-cold`, `tint-food` and `tint-bakes` are for card gradients only, one per menu category — never for status, buttons or text. `text` reads at 14.5:1 or better and `text-muted` at 4.6:1 or better on every tint.
- Use `success` for successful outcomes, `warning` for caution and `error` for errors or destructive actions. As text they read at 4.7 / 5.8 / 5.1:1 on `background` and 5.1 / 6.3 / 5.6:1 on `surface`. Never signal status through colour alone: pair it with an icon and a word (see **StatusBadge**).
- Use `border` for decorative dividers only (1.2:1 on `background`, 1.3:1 on `surface`). Outline inputs and other control boundaries in `border-strong` (3.1:1 / 3.5:1). Cards and panels have no border or shadow: the white `surface` on the grey `background`, plus whitespace, separates them.
- Check contrast for each actual pairing; target WCAG AA — 4.5:1 for normal text, 3:1 for large text and for meaningful graphics and control boundaries.

## Typography

- Set everything in DM Sans (`--font-sans`). It is a hosted Google Font: load it in the project before applying these tokens, e.g. `https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,400..700&display=swap`.
- Display: `display` (500 weight, `clamp(48px, 7.4vw, 92px)` / 1, −0.045em tracking) for the hero title only — one per page.
- Headings: `h1` 40/48 bold for page titles (one per page; about 32px on small screens), `h2` 32/40 bold for sections, `h3` 24/32 semibold for subsections, `h4` 20/28 semibold for card and component titles. Keep them in descending order.
- Text: `body` 16/24 for primary content, `caption` 14/20 for supporting information, `small` 12/16 for secondary labels and timestamps.
- Labels: `label` (14/20, 500, uppercase, 0.08em tracking, in `text-muted`) for section labels above groups of content. Keep them short.
- Reserve `tiny` (10/12, medium) for nonessential decorative metadata; keep anything essential at 12px or larger.
- Apply type through the type-style classes (`class="body"`, `caption`, `h4`, `small`, `display`, `label`…), never by hard-coding a font size. Components set only a weight on top of them (labels, buttons, chips and badges at 600).

## Spacing and layout

- Use only the spacing scale `space-1` (4px) to `space-7` (48px) — no arbitrary numbers.
- Default gaps are `space-4` (16px), card padding is `space-5` (24px), panel padding is `space-6` (32px), and major sections sit `space-7` (48px) apart. Inputs pad at `space-3`.
- Be generous with whitespace: let big white cards breathe on the grey canvas rather than packing them edge to edge.

## Radii

- Buttons, segmented controls and chips `radius-full` (pills); inputs `radius-3` (12px); cards `radius-5` (24px); large cards and panels `radius-6` (32px); badges and small controls `radius-1` (4px).
- Use `radius-2` (8px) and `radius-4` (16px) for smaller elements nested inside cards, such as thumbnails and dropdown menus.
- Use `radius-none` (0) for full-bleed images and tables that run edge to edge, and `radius-full` (9999px) for pills and circles.
- Keep radii consistent between related components.

## Borders

- Draw every outline and divider at `border-width` (1px) and every focus outline at `focus-ring-width` (2px) — never a literal pixel width.

## Interaction

- One visually dominant primary button per screen or task area; everything else is secondary or ghost.
- Every interactive element shows a visible keyboard focus state: a solid `focus-ring-width` `primary` ring with a 2px offset (16.5:1 on `background`, 18.1:1 on `surface`).
- Show selection with `accent` plus a label (chips, current step) or with a raised `surface` segment (segmented controls) — never with colour alone.
- Destructive actions use `error` and say what they destroy ("Delete workout").

## Iconography

No icon set has been supplied. The logo's motifs — the selection frame with corner handles, the sparkle and the cursor — are the brand's visual language; when an icon set is chosen, prefer a single-weight outline style that matches the neon tubing, and always pair status icons with a word.

## Components

The component styles live in `components/bundle.css` as plain CSS classes (prefix `pdg-`); there is no JavaScript bundle. The spec names actions, inputs, cards and status colours, so the system includes **Button**, **Input**, **Card** and **StatusBadge**, plus **Segmented** for mode switches (Pickup | To table) and **Chip** for filters, all built strictly from these tokens.
