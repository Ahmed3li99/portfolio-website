## 2024-05-24 - Cursor Interaction State
**Learning:** Custom cursors require specific handling for interactive elements (links, buttons). When disabled state is added, the custom cursor might still show the "hover/interactive" state, confusing users.
**Action:** Always ensure that `disabled` attributes or `.disabled` classes correctly cancel out custom cursor hover effects.

## 2024-05-24 - Focus Visibility on Custom Themes
**Learning:** High-contrast `:focus-visible` styles are critical because the site uses a custom cursor (`cursor: none` on `body`) and dark themes. The native browser focus ring often blends into the background or is disabled by resets.
**Action:** Add explicit, high-contrast focus rings (e.g., using `--cyan` or `--pink`) to all interactive elements for keyboard accessibility.
