# Decision records and handoff

Adapted from the user-supplied project-discovery playbook.
Examples are illustrative, not live project decisions, authorizations, or results.
Load the sections relevant to the current decision; keep the conversation focused.

## 20 Reusable decision and question records

### Decision record template

**Identity:** A stable decision ID and the specific topic

**Evidence:** The exact question and options, followed by the relevant user answer and qualifications

**Current state:** The active choice and its status: confirmed, proposed, assumed, open, deferred or superseded

**Reason and impact:** The user's reason or a labeled interpretation, plus affected screens, workflows, data, cost, permissions and tests

**Follow through:** Required evidence, owner and timing, plus any earlier decision this supersedes

**Scope:** This project, this phase or a broader explicitly stated preference

### Worked decision record

D07 Review model

**Question:** Include/Pass, Pass/Maybe/Include, or five-point scoring?

**User response:** “B, and don’t make people choose an exact number.”

**Current decision:** Use Pass/Maybe/Include without a hard selection quota.

**Status and reason:** Confirmed; preserve uncertainty and avoid forcing a fixed count.

**Dependencies:** Review controls, progress indicator, host summary and completion tests

**Verification:** Prototype whether reviewers understand Maybe and completion

**Scope:** First version of this photo-selection project; replaces the proposed fixed-number shortlist

### Question planning template

**Decision and timing:** What changes based on the answer, and which dependency or risk makes it the next question?

**Known constraints:** Which facts and confirmed decisions limit the options?

**Options:** Usually three or four coherent choices with concrete consequences

**Recommendation and flexibility:** One choice, one reason and its main cost; allow combination, rejection or another route

**After the answer:** Which parts of the specification must change?

**Do not repeat if:** The answer is already known. For low-impact reversible details, propose and batch them for review; ask individually if the user has a preference or the experience materially changes. Use evidence when the uncertainty is factual rather than preferential.

### Requirement traceability

Connect each material user statement or approved proposal to a requirement ID, affected workflows and states, an acceptance condition, and a validation status. For example: “No hard quota” → R12 → review progress and completion → any number of Include responses allowed once all photos are reviewed → intent confirmed, implementation untested. This exposes requirements that were discussed but never incorporated or checked.

### Specification change note

“D07 confirmed. Removed the quota from the review flow and completion criteria. Progress now counts reviewed photographs. Added a test for changing Maybe to Include before closure. Export format remains open.”

Keep records concise enough to maintain. They should make the current project easier to understand, not become a second project. Preserve exact wording where ambiguity or authorization matters, but do not retain unnecessary personal information.

## 22 Stage gates and handoff package

### Gate 1 A direction worth exploring

A concrete problem or opportunity is named. The audience and desired outcome are plausible. The selected idea differs meaningfully from alternatives. Major uncertainty is visible. Output: a short concept statement and a proposed first-version boundary.

### Gate 2 A coherent project model

The whole-project map exists. The primary journey can be explained from entry to completion. Roles and authority are clear enough to expose conflicts. Material areas have a status. Output: coverage map, current decisions and prioritized open questions.

### Gate 3 A reviewable design

Important workflow and presentation choices are concrete. At least one realistic example or prototype demonstrates the intended experience. Rejected directions are removed from active specifications. Output: sample screens, outline, timetable or equivalent artifact, with known gaps.

### Gate 4 User validated scoped understanding

Read back the complete intended project, not only the next build. The user confirms the current version or supplies corrections that are resolved and read back again. Every material intent is answered or intentionally deferred; factual unknowns remain clearly distinguished. High-impact feasibility questions are resolved or explicitly block only the affected work. Scope, acceptance criteria and action boundaries are understood. Required approvals are obtained for the next action, not assumed from design approval. Output: a bounded execution plan with dependencies and verification steps.

### Gate 5 Ready to hand off

The promised deliverable exists in the requested form. Relevant checks were actually run. Failures and partial completion are disclosed. The user knows what is ready, what remains and how to use or continue the work. Output: verified artifact, concise result summary and a clear next owner or next step.

### A builder ready handoff

Include the purpose, audience, scope, current journey, roles and permissions, data model, visual or presentation direction, important states, integration constraints, cost assumptions, acceptance tests and unresolved decisions. Separate confirmed requirements from proposals. Give each unresolved item an owner or a clear next action.

Do not bury a blocking authentication dependency in a miscellaneous note while labeling the whole project “ready.” Do not hand off two contradictory versions and expect the next agent to infer which one is current.

### A practical acceptance example

“An invited reviewer can open a collection, respond to every image, revise a response before closure and see saved progress after returning. Another reviewer cannot read those responses while review is open. After closure, the host can create a final set and export the agreed format. Save failures are visible and recoverable.”

Each sentence should map to a test or inspection. If export is deferred, remove it from first-version acceptance and record it in the later phase rather than silently failing it.

## Editable project record

Use [the project specification template](../templates/project-spec.md) for the current version, coverage and question ledgers, decisions, requirements, evidence, and user validation. Keep one active specification; archive superseded decisions without leaving their rules active. The ledgers separate intent from verified behavior.

Track the cumulative asked-question count, provisional depth and rationale,
remaining allowance, and reserved correction/readback slots. Apply
[the 20–120 budget](../SKILL.md#adaptive-depth-and-question-budget) to selected
discovery questions, including follow-ups. Known facts and research are not new
questions. Keep the count across sessions, phases, and scope changes within the
same project; do not restart it merely to escape the cap.
