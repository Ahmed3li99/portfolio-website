## 2024-05-24 - High-Contrast Focus Visible Styles for Custom Cursors
**Learning:** This site uses `cursor: none` to disable the native cursor and implements a custom JS-based cursor. While visually striking, this creates a major accessibility issue for keyboard users who rely on the native cursor or focus indicators to know where they are on the page. Since the native cursor is hidden, keyboard focus must be explicitly and clearly indicated using high-contrast `:focus-visible` styles.
**Action:** When working on sites with custom cursors, always ensure that all interactive elements (buttons, links, inputs) have a robust `:focus-visible` style defined. In this project, I will use the theme's primary color variables (e.g., `--cyan` or `--pink`) to create a clear, high-contrast outline or background change on `:focus-visible`.

## 2024-05-25 - Semantic Tags for Interactive UI Components
**Learning:** Found custom UI elements like carousel gallery dots implemented using generic `<span>` tags. Even with `cursor: pointer` and JavaScript event listeners, non-semantic tags lack default keyboard focusability, enter/space key activation, and essential screen reader support. This creates a hidden accessibility trap.
**Action:** When creating or updating interactive UI components (like carousel dots, tabs, or custom toggles), always use semantic `<button type="button">` tags. Make sure to reset default styles (like padding or borders) via CSS, and add descriptive `aria-label` attributes to ensure the component is fully accessible.

## 2024-05-26 - Dynamic ARIA States for Interactive Toggles
**Learning:** For interactive toggles like a hamburger menu, static ARIA attributes are insufficient. Assistive technologies need to know the current state of the expanded content. It's common to miss updating `aria-expanded` dynamically as the visual state changes.
**Action:** When working on interactive toggles (menus, accordions, dropdowns), always set the initial `aria-expanded` state in HTML and ensure the associated JavaScript updates this attribute dynamically to reflect the current state (e.g., using `classList.toggle`'s boolean return value).
