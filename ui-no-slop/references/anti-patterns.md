# UI anti-pattern catalog

Use this reference for a new composition or a review of generic styling. These are this skill's design policies and contextual judgments unless a row identifies a measurable defect. A pattern's presence alone does not establish AI authorship or poor usability.

## Color, surfaces, and grouping

| Signal | Why it fails in the default case | Replacement and legitimate exception |
| --- | --- | --- |
| Purple, indigo, or cyan accent gradients on headings, buttons, and panels | One effect supplies every hierarchy level without expressing a role. | Use the product's semantic palette. Preserve explicitly requested gradients and assess contrast across them. |
| Ambient blurred orbs behind text | Decorative depth distracts from the message and complicates legibility. | Start with the existing canvas and content. Subject-specific artwork may belong in a marketing composition. |
| Saturated glows under controls or cards | Emphasis spreads across competing objects. | Use the established elevation system. Status and selection should remain legible without the glow. |
| Translucent content cards everywhere | Layering no longer distinguishes navigation, overlays, and content. | Use opaque content surfaces; reserve platform materials for a real layering function. |
| Thick colored strip on a rounded card | An arbitrary accent adds another visual boundary. | Remove it, or express a meaningful status with a labeled indicator. Established status treatments remain valid. |
| A card around each field, label, or sentence | Padding and boundaries fragment scanning. | Group related content with alignment and spacing. Independent selectable items can justify cards. |
| Card inside card inside card | Each wrapper consumes space without adding useful hierarchy. | Flatten decorative wrappers. A collection inside a real parent workspace can still contain independent items. |
| One radius and shadow for every object | Fields, panels, menus, and content become visually interchangeable. | Reuse role-based tokens. A shared radius is acceptable when the design system deliberately defines it. |

## Typography and composition

| Signal | Why it fails in the default case | Replacement and legitimate exception |
| --- | --- | --- |
| Inter or system type selected without considering context | A font default substitutes for a hierarchy decision. | Evaluate roles, weights, widths, and text scaling. Preserve suitable platform and established brand fonts. |
| One italic serif word in an otherwise sans-serif headline | A stock accent replaces content-led emphasis. | Use a coherent heading treatment. Preserve an intentional identity that uses this treatment. |
| Pill above every centered heading | Decorative labels repeat information and make sections interchangeable. | Remove redundant labels; keep a meaningful release, category, or state label. |
| Tiny uppercase text with wide tracking | The visual style reduces readability, especially in repeated data labels. | Use readable sizing and natural capitalization. Short established acronyms remain valid. |
| Headings scarcely distinguishable from body text | Readers cannot quickly locate sections or priorities. | Establish hierarchy through size, weight, spacing, and placement. Dense tools may use modest size differences successfully. |
| Badge, centered headline, subtitle, paired CTAs for every product | The same shell appears before the product's characteristic content. | Lead with a real task, demonstration, image, or message suited to the brief. Centering itself is permissible. |
| Repeated icon-title-paragraph feature cards | Equal boxes conceal unequal information value. | Show actual product evidence and group content by meaning. Comparable choices may warrant a uniform grid. |
| Oversized icons on tinted square tiles | Decoration occupies more attention than the content it introduces. | Size symbols for recognition and align them with useful labels. An illustration can be the content itself. |
| Large metrics repeated in identical strips | Numbers imply importance without explaining decisions or context. | Supply units, period, source, comparison, and the task they support. Never invent credibility claims. |
| Bento cells chosen before their contents | Tile geometry drives the information hierarchy. | Assign space according to content and interaction. Use a grid when the modules are genuinely independent. |
| Dashboard full of filters, KPIs, charts, and actions without ordering | The starting task and primary workspace are unclear. | Prioritize the task; keep frequent controls nearby and disclose less frequent detail. Expert density can be appropriate. |
| Cream/serif/clay, neon-dark, or newspaper styling by reflex | A different palette disguises the same lack of product specificity. | Draw identity from the brief, content, and established visual language. Each aesthetic can be valid when requested. |
| Numbers on content that has no sequence | Decorative ordering implies a relationship that does not exist. | Number actual steps, rankings, or timelines; otherwise use the content's own labels. |
| Monospace applied to every label to imply technicality | A stereotype overwhelms the information's actual roles. | Reserve it for code, identifiers, or alignment needs; follow the existing type system elsewhere. |
| The same gap inside groups and between sections | Relationships become difficult to distinguish. | Use tighter spacing within a group and greater separation between groups, following project tokens. |

## Interactions and content

| Signal | Why it fails in the default case | Replacement and legitimate exception |
| --- | --- | --- |
| Every action uses the primary button style | Competing emphasis obscures the intended next action. | Establish primary, secondary, and destructive roles per local task. Independent tasks can each have a primary action. |
| Unnamed icon buttons | The action is ambiguous visually or inaccessible programmatically. | Provide an accessible name and discoverable meaning. Familiar compact controls can remain icon-only. |
| A modal for every edit or status message | Interruptions replace the user's working context. | Prefer an inline edit, contextual popover, or appropriate sheet. Focused irreversible confirmations may justify a dialog. |
| A long settings workflow squeezed into a modal | Scrolling and crowded controls weaken orientation. | Give the workflow a suitable page or platform settings view. A short focused task can remain modal. |
| Chart fragments without meaningful data | Visual sophistication implies evidence that is absent. | Show interpretable real data, or identify fixture data explicitly in a prototype. |
| Repeated heading, subtitle, placeholder, and helper instructions | Readers must scan more words without learning more. | Give each piece one job. Retain useful format requirements and consequences. |
| Missing loading, empty, failure, or overflow behavior | The polished example works only with ideal data. | Implement the states the component can actually encounter. Static content does not need a fabricated lifecycle. |
| Essential controls disappear on mobile | A layout compromise removes the ability to complete the task. | Reflow or relocate the control and preserve access. Deliberately desktop-only workflows must be identified. |
| Every section slides in; every card lifts; badges keep moving | Motion consumes attention without explaining changes. | Prefer immediate access and brief feedback tied to an action. A purposeful brand moment may be appropriate. |

## Grouping example

These static fragments illustrate structure, not an entire application. They introduce no buttons or simulated live state.

Decorative nesting:

```html
<div class="profile-card">
  <h2>Account</h2>
  <div class="field-card">
    <div class="value-card">
      <span>Email</span>
      <p>alex@example.com</p>
    </div>
  </div>
</div>
```

One semantic group, with values allowed to wrap:

```html
<section class="account" aria-labelledby="account-title">
  <h2 id="account-title">Account</h2>
  <dl class="account-fields">
    <div><dt>Email</dt><dd>alex@example.com</dd></div>
    <div><dt>Notifications</dt><dd>Enabled</dd></div>
  </dl>
</section>
```

```css
.account { color: #171717; background: #ffffff; }
.account h2 { margin: 0 0 1rem; font-size: 1.5rem; }
.account-fields { margin: 0; }
.account-fields > div {
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(0, 2fr);
  gap: 0.5rem 1rem;
  padding-block: 0.75rem;
}
.account-fields dt { color: #525252; }
.account-fields dd { margin: 0; overflow-wrap: anywhere; }
@media (max-width: 30rem) {
  .account-fields > div { grid-template-columns: minmax(0, 1fr); }
}
```

The neutral colors demonstrate contrast rather than define a global palette. Substitute the target project's verified tokens. The primary and secondary text pairs on white measure approximately 17.93:1 and 7.81:1 respectively.

## Evidence and visual examples

Research checked on 2026-09-30. The policies above adapt the user's supplied specification. Supporting sources inform particular decisions; their examples are not universal prescriptions.

- [Anthropic's generated comparisons](https://claude.com/blog/improving-frontend-design-through-skills): published SaaS, blog, and dashboard examples.
- [Anthropic's frontend-design guidance](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md): subject-led composition and recurring newer defaults.
- [Impeccable's synthetic specimens](https://subclaude.com/slop/): deliberately constructed examples, including [nested containers](https://subclaude.com/antipattern-examples/cardocalypse.html), [gradients](https://subclaude.com/antipattern-examples/purple-gradients.html), [icon grids](https://subclaude.com/antipattern-examples/massive-icons.html), and [redundant form text](https://subclaude.com/antipattern-examples/redundant-ux-writing.html). Treat detector output as a lead to inspect, not an automatic verdict.
- [Linear's redesign](https://linear.app/now/how-we-redesigned-the-linear-ui): deliberate Inter usage, platform adaptation, and hierarchy testing.
- [Linear's interface refresh](https://linear.app/now/behind-the-latest-design-refresh): reducing competing emphasis and unnecessary separators.
- [IBM Carbon data tables](https://carbondesignsystem.com/components/data-table/usage/): task-focused density, contextual actions, and progressive disclosure.
