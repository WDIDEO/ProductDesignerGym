# Input

A labelled single-line text field with optional hint or error message.

**Markup:** a `.pdg-field` wrapping a `<label class="caption pdg-field__label">`, an `<input class="body pdg-input">` and an optional `<p class="caption pdg-field__hint">`. Add `pdg-field--error` to the wrapper for the error state, and point `aria-describedby` at the hint.

**You provide:** the label (always visible — placeholders are not labels), the `id`/`for` pairing, the value and validation message.

- `surface` fill, `border-width` `border-strong` outline (3.5:1 on `surface`, 3.1:1 on `background`), `radius-3`, `space-3` padding, `body` text; label in `caption` at weight 600, hint in `caption`; placeholder in `text-muted`.
- Hover darkens the outline to `text`; focus turns it `primary` and adds the `focus-ring-width` `primary` ring.
- Error: `error` outline and `error` message text that says what to fix — never colour alone.
- Never outline a field in `border`: at 1.3:1 it is decorative only.
