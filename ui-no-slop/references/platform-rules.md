# Platform rules

Read the sections relevant to the target UI. Apply browser-specific rules to browser-rendered interfaces, not mechanically to native frameworks.

## Color, typography, and geometry

Use the existing semantic tokens. For a new system, assign concrete values to surface, text, accent, selection, and status roles before styling the screen. Keep status meaning consistent and pair color with a label or other recognizable cue.

Calculate text contrast from the actual foreground and background, including alpha compositing, gradients, and changing backgrounds. WCAG AA requires 4.5:1 for normal text and 3:1 for qualifying large text. On the web, large text is at least 24 CSS px regular or approximately 18.67 CSS px bold. Inactive controls and other defined exceptions have different requirements. Important non-text controls and state indicators generally need 3:1 against adjacent colors under the applicable criterion.

Examples calculated with the WCAG relative-luminance formula:

| Foreground | Background | Ratio | Interpretation |
| --- | --- | --- | --- |
| `#71717a` | `#09090b` | 4.12:1 | Fails normal-text AA; passes the qualifying large-text threshold. |
| `#71717a` | `#18181b` | 3.67:1 | Fails normal-text AA; use the actual content surface when testing. |
| `#525252` | `#ffffff` | 7.81:1 | Passes normal-text AA. |
| `#d4d4d4` | `#1e1e1e` | 11.25:1 | Passes normal-text AA. |

Rounded figures are explanatory. Compare the unrounded result against the threshold. A passing pair does not establish whole-screen conformance.

Typography needs a clear role and readable measure. Preserve platform text styles and scaling; evaluate long titles, identifiers, localized content, and mixed scripts. A modest size difference can work with weight and spacing. Avoid demanding a novel font or a fixed ratio on every screen.

For concentric rounded surfaces, an inner radius can follow `max(0, outer radius - inset)`. Measure the actual inset, including border geometry. This is a geometric aid for aligned shapes, not a rule for unrelated buttons placed inside panels.

Sources: [WCAG text contrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [non-text contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html), [Apple typography](https://developer.apple.com/design/human-interface-guidelines/typography).

## Web

- Reuse the site's component library and semantic HTML. Use links for navigation, buttons for actions, and appropriate heading, list, table, and definition-list structure.
- Give every interactive element an accessible name and visible keyboard focus. `outline: none` is acceptable only with a visible replacement. A tooltip by itself does not guarantee an accessible name; use actual label text, `aria-label`, or `aria-labelledby` as appropriate.
- Use comfortable touch targets. This skill defaults to at least 44 by 44 CSS px for touch-oriented controls. WCAG 2.2 AA's minimum target criterion is 24 by 24 CSS px with defined exceptions; distinguish this from the skill's preferred sizing.
- Preserve functionality at supported widths and zoom settings. For ordinary pages, verify reflow at 320 CSS px where the WCAG criterion applies. A genuinely two-dimensional table or diagram may require another treatment; preserve access to its controls and data.
- Scope filters and batch actions to the content they affect. Dense tables can be useful. Avoid putting them into narrow ornamental cards that force unnecessary truncation.
- Use platform or library dialog primitives when available. A custom modal needs appropriate focus entry, containment, dismissal, return, and semantics; a visual backdrop alone is insufficient.

Sources: [WCAG focus visibility](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html), [target sizing](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html), [reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html), [dialog behavior](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/).

## Native mobile

Follow the target platform's navigation, back behavior, safe areas, text scaling, keyboards, and standard controls. Use framework-native tabs, lists, sheets, menus, and pickers where they fit the task. Grouped settings rows should follow the platform's conventions rather than imitate a web landing page.

On iOS, prefer a 44 by 44 pt interaction region for ordinary touch controls. On Android, use the platform's 48 by 48 dp guidance for ordinary touch targets. CSS px, native points, and dp are separate units. Respect any applicable component-specific guidance and the product's supported devices.

Check compact and larger screens, long translations, the largest supported text sizes, keyboard appearance, and system back or dismissal behavior. Hover is relevant only where an input device supplies it. Focus and accessibility semantics still matter.

Sources: [Apple accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [Apple layout](https://developer.apple.com/design/human-interface-guidelines/layout), [Android touch targets](https://support.google.com/accessibility/android/answer/7101858).

## Native desktop and desktop wrappers

Preserve standard window behavior, shortcuts, keyboard navigation, contextual menus, pointer feedback, and resizable content. Use the framework's native menu, toolbar, and settings facilities where available. An Electron or Tauri app still has browser-rendered content, so the web rules apply to that content as well.

Keep the main task visible at supported window sizes. Navigation chrome should orient users without competing with the workspace. Preserve suitable density for experienced users rather than spreading a desktop tool into mobile-sized cards.

Source: [Apple macOS design](https://developer.apple.com/design/human-interface-guidelines/designing-for-macos).

## Materials and appearance

Support the appearances and accessibility preferences required by the product and platform. Preserve existing user theme controls. Do not create an extra appearance switch or mandatory second theme for a narrowly scoped change unless needed by the brief.

Apple's Liquid Glass belongs primarily to the functional controls/navigation layer. Standard materials have different content-layer uses. Reuse system components and respect reduced-transparency and increased-contrast settings. This does not justify copying a glass effect onto every web content card.

Sources: [Apple materials](https://developer.apple.com/design/human-interface-guidelines/materials), [dark appearance](https://developer.apple.com/design/human-interface-guidelines/dark-mode).

## Motion

For newly authored web motion under this skill:

- Animate explicitly named `transform` and `opacity` properties. Exclude `transition: all` and `transition-all`; they can unintentionally animate other changing properties. Their presence does not itself prove a layout recalculation.
- Keep layout changes immediate when possible. Animating `height`, `width`, spacing, positions, or `grid-template-rows` changes geometry. A CSS grid accordion is not compositor-only merely because it avoids JavaScript measurements.
- Use a brief decelerating transition for positional movement, with its origin anchored to the triggering object. Exclude ornamental bouncing and elastic loops. Linear progress indicators have a different purpose and can use linear timing.
- Avoid entry delays on routine lists. If a decorative entrance is justified, keep the total stagger delay within 150 ms and leave content and controls usable immediately. Delay budget and animation duration are separate quantities.
- Respect reduced-motion preferences by removing unnecessary movement. Preserve understandable progress and feedback. Prefer targeted alternatives over a global duration hack that may disrupt unrelated components or event logic.
- Confirm compositing and performance with browser tools when making such claims. `transform` and `opacity` are preferred candidates, not evidence that a particular implementation was GPU-verified.

Example for an already functional anchored popover, whose visibility and focus are managed by the target application:

```css
.context-panel {
  transform-origin: top right;
  transition: opacity 120ms ease-out, transform 120ms ease-out;
}
.context-panel[data-entering] {
  opacity: 0;
  transform: scale(0.98);
}
@media (prefers-reduced-motion: reduce) {
  .context-panel { transition: none; }
  .context-panel[data-entering] { transform: none; }
}
```

This CSS describes a visual transition only. It does not implement popover dismissal, focus behavior, or menu semantics. Use the target library's lifecycle rather than shipping it as a standalone component.

For native motion, use platform APIs and settings. Preserve purposeful system springs or native transitions; do not translate browser property restrictions into a ban on standard native behavior. In every platform, motion must remain interruptible and must not gate input for decorative reasons.

Source: [web.dev animation performance](https://web.dev/articles/animations-guide).
