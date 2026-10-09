A dark, neon-lit system for Product Designer Gym: interfaces that feel like a training floor for design skills — a dark canvas, one electric-blue action colour, and plain, confident DM Sans type.

## Brand

- Write the name as **Product Designer Gym** — three words, title case, never abbreviated in UI copy.
- The logo is a photographed neon sign: a flexed-arm icon inside a design-tool selection frame (corner handles), a sparkle and a cursor, over the stacked wordmark. Use `product-designer-gym-neon.png` from **Logos** as a hero or brand image on `background`; it carries its own brick-wall backdrop, so never place it on a light ground or crop the sign's glow tightly.
- The sign's violet sparkle, pink frame and orange cursor belong to the logo image only. They are **not** UI colours: interfaces use the tokens below.
- No vector mark has been supplied, so there is no small-size logo or favicon yet. Do not redraw the sign; set the name in `h4` / `text` where a compact mark is needed.

## Colour

The system has one theme, **Dark**.

- Paint the app canvas `background`; cards, modals and input fields `surface`.
- Set headings and body copy in `text`; secondary text, hints and descriptions in `text-muted`.
- Use `primary` for primary actions, links and active elements, and `primary-hover` only for their hover state — it is not a second brand colour.
- Label any `primary`, `primary-hover` or `error` fill with `on-primary` (the dark canvas colour). White on `primary` is 1.9:1 and fails.
- Use `success` for successful outcomes, `warning` for caution and `error` for errors or destructive actions. Never signal status through colour alone: pair it with an icon and a word (see **StatusBadge**).
- Use `border` for dividers, outlines and input borders. It measures 2.6:1 on `background` and 2.3:1 on `surface`, under the 3:1 recommended for control boundaries — rely on the field's `surface` fill and its label as well as the outline, and use the `primary` focus ring to mark the active field.
- Check contrast for each actual pairing; target WCAG AA — 4.5:1 for normal text, 3:1 for large text and for meaningful graphics and control boundaries.

## Typography

- Set everything in DM Sans (`--font-sans`). It is a hosted Google Font: load it in the project before applying these tokens, e.g. `https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,400..700&display=swap`.
- Headings: `h1` 40/48 bold for page titles (one per page; about 32px on small screens), `h2` 32/40 bold for sections, `h3` 24/32 semibold for subsections, `h4` 20/28 semibold for card and component titles. Keep them in descending order.
- Text: `body` 16/24 for primary content, `caption` 14/20 for supporting information, `small` 12/16 for secondary labels and timestamps.
- Reserve `tiny` (10/12, medium) for nonessential decorative metadata; keep anything essential at 12px or larger.
- Apply type through the type-style classes (`class="body"`, `caption`, `h4`, `small`…), never by hard-coding a font size. Components set only a weight on top of them (labels and badges at 600).

## Spacing and layout

- Use only the spacing scale `space-1` (4px) to `space-7` (48px) — no arbitrary numbers.
- Default gaps are `space-4` (16px), card padding is `space-5` (24px), and major sections sit `space-7` (48px) apart. Inputs pad at `space-3`.

## Radii

- Buttons and inputs `radius-2` (8px); cards and dropdowns `radius-3` (12px); larger panels `radius-4` (16px); badges and small controls `radius-1` (4px).
- Use `radius-none` (0) for full-bleed images and tables that run edge to edge, and `radius-full` (9999px) for pills and circles.
- Keep radii consistent between related components. Use `radius-5` and `radius-full` selectively, for hero, feature and pill shapes.

## Borders

- Draw every outline and divider at `border-width` (1px) and every focus outline at `focus-ring-width` (2px) — never a literal pixel width.

## Interaction

- One visually dominant primary button per screen or task area; everything else is secondary or ghost.
- Every interactive element shows a visible keyboard focus state: a solid `focus-ring-width` `primary` ring with a 2px offset (8.8:1 on `background`, 7.8:1 on `surface`).
- Destructive actions use `error` and say what they destroy ("Delete workout").

## Iconography

No icon set has been supplied. The logo's motifs — the selection frame with corner handles, the sparkle and the cursor — are the brand's visual language; when an icon set is chosen, prefer a single-weight outline style that matches the neon tubing, and always pair status icons with a word.

## Components

The component styles live in `components/bundle.css` as plain CSS classes (prefix `pdg-`); there is no JavaScript bundle. The spec names actions, inputs, cards and status colours, so the system includes **Button**, **Input**, **Card** and **StatusBadge** built strictly from these tokens.
