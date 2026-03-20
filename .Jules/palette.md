# Palette's UX Learning Journal

## 2024-05-24 - High-Contrast Focus Visible Styles for Custom Cursors
**Learning:** This site uses `cursor: none` to disable the native cursor and implements a custom JS-based cursor. While visually striking, this creates a major accessibility issue for keyboard users who rely on the native cursor or focus indicators to know where they are on the page. Since the native cursor is hidden, keyboard focus must be explicitly and clearly indicated using high-contrast `:focus-visible` styles.
**Action:** When working on sites with custom cursors, always ensure that all interactive elements (buttons, links, inputs) have a robust `:focus-visible` style defined. In this project, I will use the theme's primary color variables (e.g., `--cyan` or `--pink`) to create a clear, high-contrast outline or background change on `:focus-visible`.

## 2024-05-25 - Interactive Controls Should Be Semantic Buttons
**Learning:** I discovered that the gallery navigation dots (`.gdot`) were implemented using `<span>` tags. While they functioned visually and responded to mouse clicks, they were not keyboard accessible by default and screen readers would not announce them as actionable controls.
**Action:** When working on interactive UI elements (like tabs, pagination, or gallery dots), always use semantic `<button type="button">` tags. This ensures they are automatically focusable, respond to Enter/Space keys, and are recognized by assistive technologies. Added `aria-label` to provide context for what each button controls.
