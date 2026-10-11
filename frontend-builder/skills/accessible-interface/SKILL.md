---
name: accessible-interface
description: Use when building or refining a web interface, including responsive layouts, keyboard interaction, forms, and loading states.
---

# Accessible interface workflow

1. Identify the user's task, target screen, content, and completion action. Read the current component library and styles before introducing new patterns.
2. Build with semantic HTML. Use buttons for actions, links for navigation, explicit form labels, meaningful headings, and text alternatives for informative images.
3. Keep keyboard navigation logical and focus visible. Avoid positive tabindex. Ensure dialogs have accessible names, appropriate focus management, and an Escape action when applicable.
4. Design mobile-first layouts that reflow without horizontal scrolling. Check long text, narrow screens, and 200 percent zoom.
5. Meet WCAG AA contrast targets: 4.5:1 for normal text and 3:1 for large text. Do not communicate errors or state using color alone. Respect reduced-motion preferences.
6. Handle loading, empty, error, disabled, and success states when the flow needs them. Preserve entered data after recoverable errors and announce status updates when appropriate.
7. Verify the main interaction with keyboard and at narrow and wide viewport sizes. If browser tools are unavailable, report that visual and interaction checks remain unverified.

## Completion criteria

The primary action works, the interface remains usable on mobile and by keyboard, and required states are represented with clear language.
