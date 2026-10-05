# Coverage, feasibility, and scope

Adapted from the user-supplied project-discovery playbook.
Examples are illustrative, not live project decisions, authorizations, or results.
Load the sections relevant to the current decision; keep the conversation focused.

## Find decisions missing from the brief

Hear Me Out's core strength is helping users discover requirements they did not
know they needed to decide. Use this coverage map to surface material omissions,
including details a user without domain experience may not know to mention.
For each important journey, check who controls it, what can fail, how it
recovers, what it costs to keep running, and how people finish or leave.

Convert a gap into a focused question with understandable options and a reason
to care. For example, an undefined review deadline raises questions about
closing authority, absent participants, late edits, and reopening. Ask those
in dependency order only when they matter to the agreed project. A single
answer may resolve several dependent requirements without further questions.

Keep newly surfaced preferences proposed or open until the user answers. Track
the consequence of leaving a decision undefined and the requirements affected
by the eventual answer. Investigate facts yourself; retain applicable quality
baselines. Use the adaptive 20–120 budget to guide useful depth rather than
treating every row as a compulsory question or a new feature.

## 7 Cover the experience as a complete system

A feature list is insufficient. Specify how people enter, act, recover, finish and leave. For each important action, identify the actor, starting state, allowed operation, visible feedback, resulting state and failure behavior.

### People and responsibilities

Identify primary users, occasional users, owners, reviewers, administrators and people affected without using the product. Define who can invite, edit, export, finalize, reopen or delete. Do not assume that the person who can view a collection can modify its contents.

### Journey and state coverage

Walk through first use, repeat use and completion. Include empty, loading, active, partially complete, finished, expired, unavailable and error states where applicable. A collection may have photographs but no reviewers; all reviewers may finish while the host has not; an export may fail after selection is complete. These are different states with different messages.

### Information and interaction

Specify what appears on the primary screen, what is secondary, what can be searched or filtered and how users know where they are. Describe keyboard and touch behavior, focus order, selection feedback, undo and confirmation for consequential actions. Prefer established interaction patterns that the intended audience already uses. Do not teach a novel interaction merely because it might be more efficient. Retain a distinct visual identity without changing familiar behavior unnecessarily. For example, long press may enter selection in a familiar mobile list, while swipe may reveal deletion there but navigate images in a gallery. Match the specific platform and context; provide visible and keyboard-accessible alternatives rather than relying on hidden gestures.

### Recovery and conflicting actions

If a reviewer loses connection after choosing Include, does the choice save locally, retry, or remain visibly unsaved? If the host closes review at the same time, which action wins? If two editors rename a collection, how is the conflict handled? Choose a proportionate behavior and show a truthful state. A silent lost change is not an acceptable unspecified edge case.

### Finish and exit

Define what “done” means for each role. The reviewer may be done after every image has a response; the host may be done only after finalizing and exporting. Explain reopening, archiving, leaving a group, removing access and data retention as applicable.

### Practical specification pattern

“For an invited reviewer while review is open: choosing Include updates the visible response immediately. The interface shows a pending state until saving succeeds. A failed save keeps the choice visible as unsaved and offers retry. After review closes, new changes are rejected with an explanation; previously saved responses remain available according to the access rules.”

This pattern connects interaction design to data behavior and testable outcomes.

## 8 Cover implementation and operating reality

The agent should translate the chosen experience into a feasible plan without asking the user to become a systems engineer. Recommend an implementation based on needs, verify external constraints, and surface only consequential tradeoffs for user choice.

### Data and architecture

Identify the important entities and their relationships. In the photo example these may include a collection, an image record, membership, a review response and a final selection. Describe the source of truth, identifiers, ownership and what happens when related records are removed. Separate original files from previews, metadata and user decisions.

Decide which functions run on a device and which require a service. A local-first design, a browser-only prototype and a hosted collaborative app have different access and synchronization limits. Do not promise remote group collaboration if the design depends on files that exist only on an unavailable laptop.

### Hosting and storage

Address where the project runs, who owns the account, how it is deployed and how it can be moved or shut down. For media, clarify file size limits, thumbnail generation, upload interruption, duplicate handling and export fidelity. A small prototype with sample images does not verify large real-world uploads.

### Cost and maintenance

**Estimate costs with explicit assumptions:** users, storage, traffic, paid services and maintenance time. Treat numbers as estimates until current pricing and usage conditions are checked. Explain cost drivers rather than inventing a precise monthly bill. Identify who handles expired credentials, dependency updates, failed jobs and user support.

### Security and privacy

Use appropriate access control, validation, secure handling of secrets and data minimization as baseline requirements. Ask about genuine choices such as retention, visibility or whether a feature needs sensitive data. Do not ask whether the user wants passwords protected or unauthorized access prevented.

### Performance and reliability

**Define realistic target scenarios:** album size, simultaneous reviewers, common device classes and expected network conditions. Decide what can degrade gracefully. Establish backup and recovery needs in proportion to the harm of loss. “Fast” becomes useful only when tied to a measurable operation and a test environment.

### External facts and tool limits

Check official documentation or a bounded experiment when a platform capability affects feasibility. Report what was verified, when it was verified and what remains uncertain. Never convert “the button appeared” into “authentication, permissions and production deployment are complete.”

## 9 Make visual direction concrete

Visual preferences are often easier to recognize than to describe. Replace abstract adjectives with comparable screens, exact values and realistic content. A person can dislike a slate background without knowing whether the cause is its hue, contrast or use across large surfaces.

### Compare one variable at a time

Show the same screen, photographs, copy, spacing and state across alternatives. Change the palette, typography or component shape being discussed. If every option also changes the layout, the user may choose the layout while the agent mistakenly records a color preference.

Use a contact sheet or side-by-side comparison with clear labels when available. For a screen-based project, include a realistic mobile view as well as a desktop composition when both matter. Describe static concepts as concepts; they do not demonstrate functioning behavior.

### An illustrative palette exploration

**A. Botanical:** accent #2F6F55, background #F7FAF7, text #16251D

**B. Cool slate:** accent #52657A, background #F2F4F7, text #17212D

**C. Iris:** accent #6255B8, background #FAF9FD, text #211D2F

These values are candidates for comparison, not prevalidated accessible token systems. Check actual foreground/background pairs, text sizes, focus indicators and disabled states before implementation. Color alone must not communicate Pass, Maybe or Include.

### Go beyond a palette

Define typography hierarchy, density, spacing, image treatment, icon style, corner radii, borders, shadows, motion and the relationship between content and controls. “Strong serif headers with a restrained sans-serif interface” is more actionable than “premium.” Still show the pairing in context before treating it as settled.

A full-pill button and a rounded rectangle can have the same color and label while feeling noticeably different. Compare those shapes directly. Do not introduce a new palette to answer a shape question.

### Match the intended platform feel

If the user wants an Apple-like mobile experience, clarify which qualities they mean: restrained surfaces, familiar navigation, touch behavior or typography. Do not automatically replace it with a Material-style component set. Verify platform requirements separately from visual resemblance.

The outcome of visual discovery is a small coherent system with sample screens and unresolved details, not a mood adjective attached to an otherwise generic interface.

## 10 Use prototypes to answer questions

A prototype is valuable when it resolves uncertainty faster than discussion. Choose the smallest artifact that tests the current concern: a paper-like screen, an interactive flow, a realistic sample export, an event run-through or a learning exercise.

### Match fidelity to the question

If the concern is whether users understand Pass/Maybe/Include, a static review screen with sample copy may suffice. If the concern is whether a sequence feels fast, an interactive flow is more useful. If the concern is whether a storage provider can handle files of the required size, a visual mockup supplies no evidence.

**State the test before building:** “This prototype checks whether reviewing twenty images feels manageable on a phone. It does not yet verify accounts, real uploads or shared data.” This lets the user evaluate the right thing.

### Use realistic situations

Include long titles, missing photographs, an unfinished review and a save failure. A perfect empty demo can conceal important design defects. Prefer representative sample content over the user's private data unless that data is needed and its use is authorized.

### Record observations separately from conclusions

**Observation:** A reviewer repeatedly looked for a Next button after selecting Include.

**Interpretation:** The automatic-advance behavior was not obvious.

**Proposal:** Add a brief transition and a visible “Next image” control.

**Next test:** Check whether the added control reduces hesitation without slowing experienced users.

One favorable reaction does not prove broad usability. A prototype can support a decision while leaving the generality of that evidence uncertain.

### Verify the actual result

For software, exercise the agreed core journey and important failure paths. For a document, inspect the final rendered pages. For an event, walk the timetable against venue and staffing constraints. For research, verify key claims and source coverage. For a learning plan, test whether the first exercise is achievable at the learner's current level.

### Report partial completion precisely

“The review flow works with sample images. Real invitations and persistent saves remain unverified.” This is more useful than “the app is done” and more informative than “there may be limitations.” Connect the gap to its practical consequence and the next step needed to close it.

## 11 Bound discovery and control scope

Cover the material dimensions of the agreed project with enough depth to expose
important gaps. This does not mean asking every bank prompt or expanding the
project until every imaginable feature exists. Every option, role, mode, and
integration adds behavior to design, maintain, and test.

### Adaptive discovery depth

Use [the Hear Me Out budget](../SKILL.md#adaptive-depth-and-question-budget):
20–120 substantive discovery questions per project, including follow-ups and
readback confirmations. The agent chooses and revises a provisional depth from
complexity, risk, uncertainty, and dependencies. Bounded reversible work often
fits 20–40; several workflows or integrations may need 40–80; broad or
high-consequence work may need 80–120. These ranges guide judgment, not quotas.

Reassess after decision clusters. Stop at the earliest sufficient depth after
20 when the user validates the scoped specification. Reuse answers, verify
facts, and use realistic artifacts rather than filling a questionnaire. Do not
hide material risks to save questions or ask irrelevant details to add them.
Reserve questions for corrections and readback; at 120, stop asking, disclose
remaining gaps, and defer or block affected work. A user's explicit request
to shorten or end discovery overrides the default; record the changed scope
and unresolved items. Narrow edits remain outside discovery unless requested.

### Treat new ideas as scope decisions

When the user adds a local photo organizer to a collaborative shortlist, identify the new capabilities: filesystem access, duplicate detection, metadata edits, file moves and possibly deletion. Explain how they differ from the existing web workflow. Offer a phase boundary, a separate companion or a replacement scope.

Do not automatically turn every new request into a settings toggle. Configurability can create a larger product than selecting one good default.

### Provisional checkpoint criteria

These criteria permit a bounded exploratory artifact, not a claim that the whole project is understood. The purpose and first-version boundary are clear. The primary journey is coherent. Material permissions and constraints are understood. High-risk feasibility questions are resolved or explicitly block execution. The visual or presentation direction is concrete enough for the next artifact. Acceptance conditions exist. Remaining assumptions are safe, visible and assigned a verification step.

### A useful provisional checkpoint

“We have enough to build the first reviewable version: one collection, private responses, a host final selection and an iris editorial interface. Export format remains open, so I’ll keep it out of this prototype. Before connecting real accounts or changing files, we’ll handle the specific access and action approvals.”

This checkpoint starts useful work while discovery remains open. The final discovery gate requires the user to validate the complete scoped specification, including explicitly deferred requirements and declared factual uncertainty. See the [final clarity gate](evaluation.md#24-validate-complete-understanding-of-intent).

## 12 Separate design agreement from action permission

A person can approve the experience of “Sign in with an account” without authorizing the agent to sign in, create credentials, grant ongoing access or publish anything. The specification describes intended behavior. Execution authorization concerns a specific action, target, data and consequence.

### Keep the distinction explicit

“Use local folders” is a design choice. It does not authorize moving or deleting the user's existing photographs. “Send reminders to reviewers” describes a feature. It does not authorize the agent to message real people now. “Use a paid hosting service” is a proposed architecture. It does not authorize an unbounded purchase.

Ask for whatever approval the operating environment and applicable rules require. Do not invent permission from enthusiasm, a selected option or a general desire to finish quickly. Conversely, do not repeatedly ask for permission already given for the same specific action unless the scope or risk changes.

### Explain consequential actions in practical language

Before a potentially destructive file operation, identify the exact folder, the type of change, whether originals remain, how recovery works and the preview available. Before external publication, identify what will become visible and to whom. Before payment, make the cost and commitment clear. Use the environment's required secure flow for credentials.

A technical command is not made safe by asking “OK?” without explaining its effect. An agent should prefer a dry run, a copy or an undoable operation where appropriate, but reversibility must be real rather than assumed.

### Handle access blockers honestly

When a needed tool or connection is missing, identify the blocked step and its consequence. Continue independent work that remains useful. Do not claim a login or integration succeeded because a mock screen exists, and do not seek another route around an explicit denial.

**Example:** “The interface is ready, but I cannot verify the account flow with the access currently available. We can review the prototype now. To verify real sign-in, we need the supported connection step.”

### Preserve useful momentum

A blocked deployment does not prevent refining error copy or documenting acceptance tests. A missing event booking approval does not prevent drafting the timetable. State the boundary clearly and make progress inside it. The user should always know whether they are choosing a design, approving an action or reviewing evidence.

## 21 A coverage matrix that prevents omissions

Use this matrix as a review instrument. Expand material areas into concrete requirements, and mark irrelevant areas with a reason. A checked row means it has an explicit disposition, not that every conceivable edge case has been solved.

| Area | Questions to resolve | Example status |
| --- | --- | --- |
| Purpose and success | Outcome, audience, measure, finish condition | Confirmed |
| Scope and phases | First complete version, exclusions, later work | Confirmed |
| Actors and authority | Roles, ownership, final decisions, handoff | Confirmed |
| Journey and states | Entry, progress, completion, reopening, exit | Proposed |
| Permissions | Read, change, invite, export, remove, revoke | Open |
| Information and data | Entities, originals, metadata, source of truth | Proposed |
| Architecture and tools | Device/service split, integrations, verified limits | Open |
| Hosting and storage | Accounts, deployment, capacity, portability | Open |
| Cost and operations | Assumptions, recurring costs, maintenance owner | Assumed |
| Privacy and security | Visibility, retention, access checks, secret handling | Proposed |
| Accessibility | Keyboard, touch, contrast, labels, reduced motion | Required baseline |
| Performance | Target devices, volume, latency, slow networks | Open |
| Recovery and conflict | Retry, undo, offline, simultaneous changes | Proposed |
| Notifications | Trigger, recipient, channel, frequency, opt-out | Deferred |
| Locale and content | Language, time zone, date formats, copy | Assumed |
| Responsive behavior | Mobile, desktop, long text, orientation | Proposed |
| Visual system | Type, colors, spacing, imagery, components | Confirmed direction |
| Interaction details | Focus, selection, feedback, loading, errors | Proposed |
| Rollout and support | Pilot, monitoring, rollback, ownership | Open |
| Tests and evidence | Core journey, failure paths, acceptance checks | Proposed |
| Handoff and exit | Deliverables, instructions, export, shutdown | Open |

### Separate intent from evidence

For a working ledger, use three separate fields: Scope is included, deferred or not applicable; Intent is proposed, assumed or confirmed; Evidence is untested, verified, failed or blocked. The compact table above illustrates conversation dispositions, not a completion report. A confirmed design can still be unimplemented and unverified.

### Use status precisely

“Required baseline” means the project must satisfy the applicable quality or safety requirement; implementation and verification can still be open. “Confirmed direction” means the broad preference is chosen, not every token or component. If precision matters, split a row rather than letting a vague status conceal uncertainty.

For events, replace architecture with venue and operational structure. For research, replace storage-heavy rows with sources, sampling and evidence quality. For learning, include practice, feedback and assessment. Retain the underlying questions about people, constraints, failure, evidence and completion.
