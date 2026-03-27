# Palette's UX Learning Journal

## 2024-05-24 - High-Contrast Focus Visible Styles for Custom Cursors
**Learning:** This site uses `cursor: none` to disable the native cursor and implements a custom JS-based cursor. While visually striking, this creates a major accessibility issue for keyboard users who rely on the native cursor or focus indicators to know where they are on the page. Since the native cursor is hidden, keyboard focus must be explicitly and clearly indicated using high-contrast `:focus-visible` styles.
**Action:** When working on sites with custom cursors, always ensure that all interactive elements (buttons, links, inputs) have a robust `:focus-visible` style defined. In this project, I will use the theme's primary color variables (e.g., `--cyan` or `--pink`) to create a clear, high-contrast outline or background change on `:focus-visible`.

## 2024-05-25 - Semantic Tags for Interactive UI Components
**Learning:** Found custom UI elements like carousel gallery dots implemented using generic `<span>` tags. Even with `cursor: pointer` and JavaScript event listeners, non-semantic tags lack default keyboard focusability, enter/space key activation, and essential screen reader support. This creates a hidden accessibility trap.
**Action:** When creating or updating interactive UI components (like carousel dots, tabs, or custom toggles), always use semantic `<button type="button">` tags. Make sure to reset default styles (like padding or borders) via CSS, and add descriptive `aria-label` attributes to ensure the component is fully accessible.

## 2024-05-26 - Dynamic ARIA States for Hamburger Menus
**Learning:** Found a hamburger menu pattern where the UI logic simply toggled a CSS class (`.open`), but lacked semantic attributes. Without `aria-expanded` dynamically reflecting the menu's state (open/closed), screen reader users are completely unaware if interacting with the button actually revealed the navigation links. Additionally, the event listener code was a compact one-liner, which is harder to extend and maintain.
**Action:** When refactoring interactive toggle components like hamburger menus, explicitly include `type="button"`, `aria-controls`, and `aria-expanded` attributes in the HTML. Ensure the associated JavaScript dynamically updates the `aria-expanded` state on interaction, and write the logic over multiple lines for readability.
