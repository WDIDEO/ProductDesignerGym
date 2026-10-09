# Input

A labelled single-line text field with optional hint or error message.

**Markup:** a `.pdg-field` wrapping a `<label class="caption pdg-field__label">`, an `<input class="body pdg-input">` and an optional `<p class="caption pdg-field__hint">`. Add `pdg-field--error` to the wrapper for the error state, and point `aria-describedby` at the hint.

**You provide:** the label (always visible — placeholders are not labels), the `id`/`for` pairing, the value and validation message.

- `surface` fill, `border-width` `border` outline, `radius-2`, `space-3` padding, `body` text; label in `caption` at weight 600, hint in `caption`; placeholder in `text-muted`.
- Hover lifts the outline to `text-muted`; focus adds the `focus-ring-width` `primary` ring.
- Error: `error` outline and `error` message text that says what to fix — never colour alone.
- Note: the `border` outline is 2.3:1 against `surface`, under 3:1; the visible label and `surface` fill carry the field's boundary alongside it.
