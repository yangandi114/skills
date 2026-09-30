# Verification

Use checks appropriate to the requested change. This reference covers acceptance of a UI produced with the skill and maintenance checks for the skill itself.

## UI acceptance

### Visual hierarchy

- Identify the screen's primary task and action in the rendered interface.
- Inspect the compact and regular layouts supported by the product. Check scanning order, related-content grouping, whitespace, alignment, useful density, and headings with realistic content.
- Apply the brand-swap and removal checks from `SKILL.md`. Distinguish an intentional product identity from repeated decorative defaults. Existing reusable controls do not need a novel treatment.
- Inspect colors, typography, icons, materials, and motion together. A neutral palette does not compensate for poor hierarchy; a strong brand accent does not excuse unreadable text.

### Relevant state matrix

| Component behavior | States to exercise | Evidence required |
| --- | --- | --- |
| Asynchronous data view | Initial loading, populated, zero data, query with no results, failure, retry | The layout remains usable; empty states differ when next actions differ; retry actually runs. |
| Mutation or form | Default, focus, invalid input, submitting, success, failure, disabled when appropriate | Correct field association, understandable pending feedback, and a real outcome or recovery path. |
| Selectable control | Default, selected, disabled, focus, press; hover for pointer input | Selection is recognizable beyond color alone and state matches the underlying value. |
| Overlay or dialog | Open, close, dismissal, keyboard path, focus return | Trigger and destination are clear; behavior follows the chosen primitive and platform. |
| Static content | Normal, long or localized content, supported text scaling and width | Information remains available without a fabricated loading or error state. |

Use the actual application's supported states. Skeletons are useful when they preserve the expected structure during a meaningful wait; they are not mandatory for instant actions. Keep skeleton decoration out of the accessibility tree and expose loading state appropriately.

### Accessibility and content

Measure actual foreground/background pairs and identify text size and weight. Check visible focus, accessible names, state announcements where needed, and keyboard order. Exercise supported zoom or text-size settings. Check touch targets using the platform's units and relevant standard.

Use realistic long names, values, identifiers, empty datasets, and relevant locales. Wrap or provide an accessible way to recover important truncated content. Give chart values their units and periods. Label prototype data and keep real status connected to real data.

### Motion and interaction

Test the changed actions, navigation, dismissal, and recovery. Verify reduced motion and any required transparency/contrast settings. Confirm that entrances do not postpone interaction. A screenshot cannot prove these behaviors.

For web motion, inspect the animated properties. Use browser performance evidence before claiming compositor-only behavior or smooth frame timing. A visual transition without functioning lifecycle behavior is an incomplete component.

## Evidence limits and findings

| Evidence | Supports | Does not establish |
| --- | --- | --- |
| Source inspection | Components, token values, wiring, state branches, semantics | Actual rendering or behavior on a device. |
| Calculated contrast | The measured pair at the specified size/weight | Contrast on another surface, appearance, or changing backdrop. |
| Screenshot | Visible hierarchy and layout at that state and size | Keyboard navigation, announcements, motion, or recovery. |
| Interaction test | The exercised path and observed result | Every untested path, locale, or platform. |
| Native simulator | The exercised simulator configuration | Physical-device, account, or provider acceptance. |

When review is requested, describe each material finding with:

1. Element or location.
2. Observed problem and its consequence.
3. Concrete correction using project tokens or platform components.
4. Evidence, with the judgment labeled when it is contextual.

Prioritize unusable controls and measured accessibility defects, then task hierarchy and platform friction, then visual polish. Report missing evidence as a verification limit, not a fabricated defect. When implementation is authorized, correct findings within scope before reporting results.

## Skill maintenance checks

Validate required frontmatter and naming, Codex UI metadata, local reference links, and unfinished placeholders. Keep the skill self-contained; source links support its reasoning but should not be mandatory browsing for every use.

For this repository, the bundled Codex validator can be run when available:

```sh
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ui-no-slop
git diff --check
```

The path is an authoring-environment tool, not a runtime dependency of this skill. Structural validation does not prove successful model discovery or behavior.

Review the skill with realistic requests. Exercise the actual skill workflow rather than merely checking whether particular words appear:

| Request | Acceptance condition |
| --- | --- |
| Build a university timetable landing page from real feature content. | Composition foregrounds student benefit and authentic app evidence; no invented statistics or unrelated decorative kit. |
| Build a desktop deployment dashboard with many runners and frequent filtering. | Useful density and contextual controls survive; the skill does not ban a coherent table. |
| Improve an iOS account settings screen. | Native grouping, navigation, text scaling, and supported appearance behavior remain; browser CSS rules are not imposed. |
| Repair a branded web app whose identity already uses purple gradients and Inter. | The brand and type system remain; actual hierarchy, contrast, and behavior defects are assessed independently. |
| Audit a screen without editing files. | Findings and evidence only; no implementation, installation, or publication. |
| Correct a loading list with an empty action and failed retry. | All relevant states have functional actions; labels and status reflect actual data. |
| Make a plain utility clearer without redesigning its identity. | A focused fix improves the task; no compulsory novelty font, asymmetry, or ornamental signature. |

If a scenario exposes a failure, revise the smallest relevant instruction or example, then repeat the affected scenario. Record whether evaluation was a manual walkthrough, actual generated execution, or independent model testing. Do not present one evidence tier as another.
