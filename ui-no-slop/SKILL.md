---
name: ui-no-slop
description: "Create, edit, or review web, desktop, and mobile UI to avoid generic AI-generated styling, weak hierarchy, and incomplete interactions. Use for interface implementation, redesign, or UI critique; exclude backend-only changes."
---

# UI No Slop

Build interfaces whose structure follows the user's task and whose visual choices belong to the product. Treat repeated template patterns as review signals, not proof of AI authorship. A quiet utility can be the right design.

## Scope and precedence

- Follow the user's current brief, repository instructions, existing design system, and native stack. Explicit branding or requested aesthetics take precedence over this skill's default restrictions.
- For an existing product, extend its components and tokens. Make a focused repair rather than imposing a new visual identity. For a new product, infer its audience and primary task from the brief; ask only when missing context materially changes the work.
- Preserve the requested mode: review-only requests produce findings; implementation requests produce working changes and verification. Skill invocation does not authorize installation, a framework migration, unrelated edits, or publication.

## Default visual restrictions

Apply these to newly chosen styling. When an established design or explicit request requires an exception, preserve it and assess its actual usability.

- Use color by role. Exclude decorative purple, indigo, and cyan accent gradients, gradient text, blurred background orbs, saturated shadow glows, and glass effects spread across ordinary content.
- Group through alignment, spacing, typography, and existing surface roles first. Add a card when an independent item, interaction, or genuine grouping boundary needs it. Exclude ornamental left-edge accent strips and cards nested merely to add depth.
- Choose composition from content. Exclude the automatic hero with a pill above a centered heading and two action buttons, three interchangeable icon cards, and repetitive metric strips. A product screen should open on its task rather than a marketing hero.
- Give headings and body text distinct roles. Exclude automatic serif italics on one word, gratuitous eyebrow pills, tiny widely tracked uppercase labels, and novelty fonts chosen only to escape Inter. System fonts and an established system using Inter are valid choices.
- Keep decoration subordinate to information. Icons, charts, dividers, numbering, and motion must explain something. Do not invent statistics, customers, endorsements, or live status to make a screen look complete.
- Avoid replacing one template with another: cream backgrounds with serif headings and clay accents, neon accents on black, and newspaper grids also need a reason rooted in the product.

Use [the anti-pattern catalog](references/anti-patterns.md) when choosing a new composition or diagnosing generic styling. It supplies examples, replacements, and exceptions.

## Workflow

### 1. Establish the screen's job

Inspect relevant UI code, design documentation, components, tokens, content, and available screenshots. Identify the platform, user, primary task, leading information, and primary action. Distinguish facts visible in code or measurements from assumptions about the product.

### 2. Choose the hierarchy before decoration

For a new screen or substantial redesign, form a compact working plan:

- Content order and grouping, with compact and regular layouts when needed.
- Existing token names or exact proposed color, spacing, radius, and type values with roles.
- Navigation and control patterns appropriate to the platform.
- Relevant loading, empty, error, selection, disabled, pending, and overflow behavior.
- Motion only where it explains a change; otherwise keep the interaction immediate.

Keep this proportional to the task. A small fix can reuse the current hierarchy. When implementation is already authorized, continue into code without adding another approval gate.

Run two checks:

- Brand swap: Would changing the logo and nouns make the same design equally plausible for an unrelated product? If so, revise the composition or content that lacks specificity. Familiar controls can remain familiar.
- Removal: Does removing a decoration lose information, useful grouping, affordance, or required identity? If not, remove it.

### 3. Implement the full relevant behavior

Read [platform rules](references/platform-rules.md) for the target platform, including contrast, controls, materials, typography, responsive behavior, and motion.

Use repository-native components and dependencies. Connect displayed actions to real behavior, communicate pending work, and provide recovery for actual failures. Preserve meaningful content at supported widths, text sizes, and locales. Avoid universal truncation that hides the values needed to complete the task.

### 4. Inspect and correct

Use [verification](references/verification.md) to select checks appropriate to the changed UI. Render and inspect the actual implementation when the environment supports it. Check compact and regular layouts, keyboard or touch behavior, and relevant state transitions.

Fix observed defects in the authorized scope. A source scan is evidence about code; a screenshot is evidence about the visible state; an interaction test is evidence about that interaction. Report unavailable verification explicitly rather than claiming production acceptance.

## Reporting

Follow the user's requested format. For a UI review, identify the affected element, the consequence, a concrete correction, and the evidence. Separate measured defects from contextual design judgments. Use exact token values or named platform components when available.

For implementation, report the changed files, resulting behavior, verification performed, and material remaining limits. Keep claims proportional to evidence. Avoid generic praise and closing restatements.
