# Adaptive multiple-choice question bank

Adapted from the user-supplied project-discovery playbook.
Examples are illustrative, not live project decisions, authorizations, or results.
Load the sections relevant to the current decision; keep the conversation focused.

## Branch index

- [C1 Intent and opportunity](#c1-intent-and-opportunity) (C01–C08)
- [C2 People and first version scope](#c2-people-and-first-version-scope) (C09–C16)
- [C3 Core journey and completion](#c3-core-journey-and-completion) (C17–C24)
- [C4 Collaboration and authority](#c4-collaboration-and-authority) (C25–C32)
- [C5 Data and content](#c5-data-and-content) (C33–C40)
- [C6 Technical feasibility and operations](#c6-technical-feasibility-and-operations) (C41–C48)
- [C7 Familiar interaction patterns](#c7-familiar-interaction-patterns) (C49–C56)
- [C8 Visual design and responsive behavior](#c8-visual-design-and-responsive-behavior) (C57–C64)
- [C9 Resilience and inclusive use](#c9-resilience-and-inclusive-use) (C65–C72)
- [C10 Privacy and consequential constraints](#c10-privacy-and-consequential-constraints) (C73–C80)
- [C11 Delivery and success evidence](#c11-delivery-and-success-evidence) (C81–C88)
- [C12 Exceptions changes and clarity checks](#c12-exceptions-changes-and-clarity-checks) (C89–C96)
- [C13 Event project branch](#c13-event-project-branch) (C97–C104)
- [C14 Research project branch](#c14-research-project-branch) (C105–C112)
- [C15 Learning project branch](#c15-learning-project-branch) (C113–C120)

## Bank usage

This bank contains 120 optional prompts across meaningful project dimensions.
Use it as a menu for Hear Me Out, which asks **20–120 substantive discovery
questions in total**, with depth chosen by the agent. The total includes custom
questions, follow-ups, and final-readback confirmations; 120 bank entries do not
mean 120 required questions or an additional allowance for follow-ups. Follow the
[adaptive budget](../SKILL.md#adaptive-depth-and-question-budget).

### How to use the bank

Start with the whole-project map. Estimate the depth needed from scope,
complexity, consequence, and uncertainty. Select the highest-value prompts from
relevant branches; it is not necessary to ask every prompt in a selected branch.
Reuse known answers and adapt or write a question when the bank does not fit.
Keep dispositions for selected questions: answered, needs follow-up, needs
research, intentionally deferred, or not applicable with a reason. Do not
create 120 ledger rows just to account for unselected prompts. A recommendation
in this bank is conditional guidance; adapt it to the actual goal and evidence.

The listed options are examples, not a closed set. Users can combine them, reject them or write another answer. Where a choice contains two independent axes, ask a follow-up rather than silently treating the whole bundle as approved. Option letters are local to each question; use the question ID to avoid ambiguity.

### Branch map

C01–C08 establish intent for every project. C09–C16 cover people and scope. C17–C24 cover the working journey. C25–C32 apply to collaborative or permissioned work. C33–C40 cover data and content. C41–C48 cover technical feasibility when software is involved. C49–C56 cover interaction and familiar conventions. C57–C64 cover visual and responsive design. C65–C72 cover resilience and accessibility. C73–C80 cover privacy and consequential constraints. C81–C88 cover delivery and success. C89–C96 examine exceptions and changes. C97–C104 adapt to events. C105–C112 adapt to research. C113–C120 adapt to learning.

### Follow up within the question budget

A selection may open another question. “Group decision” requires defining eligible voters, ties and closure. “Keep it local” requires clarifying whether remote access, backups or exports may leave the device. “Make it intuitive” requires naming the audience's familiar patterns and inspecting a realistic flow.

Ask for a concrete scenario when words remain vague. Use correction slots for
conflicting choices and reserve the final-readback slot. Investigate factual
uncertainty with research or a bounded test; these do not consume questions
unless another discovery question is presented. At the cap, stop asking and
surface unresolved items or affected blockers. Never use a default to conceal
a material unknown or describe reaching the cap as validated understanding.

### Completion means validated scoped clarity

The working target is “100% clear about what the user wants” within the explicitly agreed scope: every material intent has an answer, an intentional deferral or a declared uncertainty accepted in the readback. This is not a claim of perfect knowledge about future users or technical behavior. Those require evidence during execution.

### C1 Intent and opportunity

Use these for every project. If the user already supplied an answer, record it and move to the unresolved part.

#### C01 What should improve first?

- **A.** save time on a recurring task;
- **B.** improve the quality of a result;
- **C.** create a new experience.

**Recommendation:** Recommend the outcome that matches the user's stated frustration; ask for a recent example before choosing if the goal is unclear.

#### C02 Who is the first beneficiary?

- **A.** the user alone;
- **B.** a small known group;
- **C.** an unfamiliar public audience.

**Recommendation:** Recommend A or B for a tightly bounded first effort when public reach is not itself the goal; C adds onboarding and support uncertainty.

#### C03 What kind of project sounds motivating?

- **A.** practical utility;
- **B.** creative expression;
- **C.** learning experiment.

**Recommendation:** Recommend based on motivation, not presumed commercial value. Follow up if the user wants a useful tool and a learning challenge with different success criteria.

#### C04 What should the first result be?

- **A.** a working small experience;
- **B.** a convincing design or concept;
- **C.** evidence to decide whether to proceed.

**Recommendation:** Recommend C when demand or feasibility is the main unknown; A when the problem is already well understood.

#### C05 Which existing workaround matters most?

- **A.** repeated manual work;
- **B.** scattered messages and files;
- **C.** a current tool that feels unsuitable.

**Recommendation:** Recommend examining the most recent real instance. Each answer opens a different comparison baseline, not an automatic replacement mandate.

#### C06 What would make this worthwhile?

- **A.** frequent modest benefit;
- **B.** a large benefit on rare occasions;
- **C.** a memorable one-time result.

**Recommendation:** Recommend matching effort to the expected use. A recurring system may be wasteful for a one-time need.

#### C07 How original should the concept be?

- **A.** familiar solution executed well;
- **B.** familiar workflow with a distinctive experience;
- **C.** exploratory new format.

**Recommendation:** Recommend B when differentiation matters but usability should stay familiar. C requires stronger validation and must not impose unfamiliar gestures unnecessarily.

#### C08 What would make you abandon the idea?

- **A.** insufficient benefit;
- **B.** excessive cost or maintenance;
- **C.** lack of personal interest.

**Recommendation:** Recommend naming the strongest stop condition now. This helps the agent avoid defending an attractive concept after its original rationale disappears.

### C2 People and first version scope

Use after the outcome is understood. Resolve responsibility before adding features or roles.

#### C09 Who makes the final call?

- **A.** one owner;
- **B.** equal group decision;
- **C.** group input with an owner deciding.

**Recommendation:** Recommend C for collaborative creative work requiring a coherent finish; B only when voting is the intended governance model.

#### C10 How experienced is the primary audience?

- **A.** first-time users;
- **B.** people familiar with comparable tools;
- **C.** specialists.

**Recommendation:** Recommend designing for the least experienced intended user, while preserving efficient paths for experts. Do not assume hidden gestures are universally known.

#### C11 How broad is the first version?

- **A.** one complete core journey;
- **B.** several related journeys;
- **C.** a broad exploratory prototype.

**Recommendation:** Recommend A when delivery matters. If the user explicitly needs depth across multiple journeys, map and estimate B rather than silently reducing scope.

#### C12 Which work belongs outside this phase?

- **A.** integrations;
- **B.** advanced customization;
- **C.** additional audiences.

**Recommendation:** Recommend deferring the least outcome-critical branch. If none can be deferred, acknowledge the larger phase instead of labeling it minimal.

#### C13 How should responsibilities be split?

- **A.** the owner handles setup and finish;
- **B.** responsibilities are shared;
- **C.** a dedicated operator supports participants.

**Recommendation:** Recommend A for a small group unless workload or continuity demands another role.

#### C14 How much configuration should users get?

- **A.** one strong default;
- **B.** a few important settings;
- **C.** extensive controls.

**Recommendation:** Recommend B only for demonstrated differences in need. Every setting adds combinations to explain and test; C is not automatically more capable in practice.

#### C15 What is the delivery constraint?

- **A.** fixed date with flexible scope;
- **B.** fixed scope with flexible date;
- **C.** fixed budget with a prioritized scope.

**Recommendation:** Recommend naming the real limiting resource. If all are fixed, surface the feasibility risk rather than promise all three.

#### C16 Who maintains the result?

- **A.** the user;
- **B.** a named team or partner;
- **C.** nobody after handoff.

**Recommendation:** Recommend a low-maintenance design for C. Ongoing services, subscriptions and operational alerts are poor defaults when no owner exists.

### C3 Core journey and completion

Walk a realistic example through each answer. The resulting flow should be explainable from start to finish.

#### C17 Where does the journey begin?

- **A.** a blank start;
- **B.** existing material;
- **C.** an invitation or assigned task.

**Recommendation:** Recommend showing the user's likely starting state first. A blank demo is misleading if real users always arrive with a large archive.

#### C18 How should initial setup work?

- **A.** one quick start with defaults;
- **B.** a guided sequence;
- **C.** import from an existing source.

**Recommendation:** Recommend A for simple reversible setup; B when early choices materially affect later work; C only after format and access feasibility are checked.

#### C19 What is the primary action?

- **A.** inspect then decide item by item;
- **B.** compare several items together;
- **C.** organize a whole collection.

**Recommendation:** Recommend A for focused judgments, B for relative comparisons and C for structure. Avoid combining all three into one overloaded screen.

#### C20 How should progress be measured?

- **A.** items completed;
- **B.** milestones reached;
- **C.** time or capacity remaining.

**Recommendation:** Recommend the measure that reflects actual completion. For a no-quota photo review, count reviewed photographs rather than implying an exact number must be included.

#### C21 Can people revise choices?

- **A.** anytime before closure;
- **B.** only before submission;
- **C.** by reopening after submission.

**Recommendation:** Recommend A for low-stakes creative review. C may suit a formal process but needs authority and history rules.

#### C22 What closes the activity?

- **A.** the owner closes it;
- **B.** a deadline closes it;
- **C.** completion by everyone closes it.

**Recommendation:** Recommend A when incomplete participation must not block a finish. B needs time-zone and late-action behavior; C needs an absentee plan.

#### C23 What should happen after completion?

- **A.** show a stable result;
- **B.** offer export or handoff;
- **C.** start another cycle.

**Recommendation:** Recommend B when ownership or reuse matters. If A and B are both required, record a combined final state rather than an ambiguous choice.

#### C24 How should unfinished work behave on return?

- **A.** resume exactly where left;
- **B.** show an overview;
- **C.** start a fresh session.

**Recommendation:** Recommend A for long sequential work and B when priorities may have changed. C should not discard saved progress without a clear reason.

### C4 Collaboration and authority

Use when more than one person participates or when different access levels exist. Skip with a reason for genuinely private single-user work.

#### C25 Who can join?

- **A.** individually invited people;
- **B.** anyone with a link;
- **C.** publicly discoverable users.

**Recommendation:** Recommend A for private material. B simplifies entry but makes link forwarding consequential; C adds moderation and abuse considerations.

#### C26 How is identity established?

- **A.** no persistent identity for a limited prototype;
- **B.** a project-specific identity;
- **C.** an existing account system.

**Recommendation:** Recommend based on the access and recovery needs. A is unsuitable when private persistent records must reliably belong to a person.

#### C27 What can participants see during work?

- **A.** only their own input;
- **B.** anonymous totals;
- **C.** named individual contributions.

**Recommendation:** Recommend A when independent judgment matters. If public collaboration is the purpose, C may be the correct model.

#### C28 When should results be revealed?

- **A.** immediately;
- **B.** after each participant finishes;
- **C.** after the owner closes the activity.

**Recommendation:** Recommend C when early information could influence remaining participants. B requires care if finished users can still communicate with others.

#### C29 Who may edit shared source material?

- **A.** owner only;
- **B.** designated editors;
- **C.** all participants.

**Recommendation:** Recommend A for a small shortlist and B for a maintained shared library. C adds conflict, attribution and recovery requirements.

#### C30 What happens when someone leaves?

- **A.** revoke future access while retaining permitted contributions;
- **B.** remove their contributions as well;
- **C.** archive the entire shared item.

**Recommendation:** Recommend defining contribution ownership and retention before choosing; no universal recommendation is safe without that context.

#### C31 How should disagreements resolve?

- **A.** owner judgment;
- **B.** majority rule with a tie rule;
- **C.** discussion before a final decision.

**Recommendation:** Recommend A for editorial selection and B for an explicit vote. C needs a time limit or escalation to avoid endless deliberation.

#### C32 How are invitations and reminders controlled?

- **A.** owner sends each;
- **B.** scheduled reminders with clear settings;
- **C.** no reminders.

**Recommendation:** Recommend A for small occasional groups. B adds consent, frequency and failure handling; a feature choice does not authorize real outreach now.

### C5 Data and content

Use for files, records, media, survey responses or any persistent content. Establish ownership and source of truth before storage implementation.

#### C33 What is the source of truth?

- **A.** original files in one location;
- **B.** a managed project copy;
- **C.** synchronized copies.

**Recommendation:** Recommend A when ownership and simplicity dominate, B for controlled collaboration, and C only when synchronization benefits justify conflict handling.

#### C34 What does the project retain?

- **A.** references and decisions only;
- **B.** previews plus metadata;
- **C.** full originals.

**Recommendation:** Recommend the smallest set that supports the required experience. Remote access and high-quality export may change which option is feasible.

#### C35 How does content arrive?

- **A.** manual entry or upload;
- **B.** batch import;
- **C.** ongoing synchronization.

**Recommendation:** Recommend A for infrequent small use, B for large starting collections. C requires a verified integration and an ongoing access and maintenance plan.

#### C36 How should duplicates be handled?

- **A.** allow and label;
- **B.** detect exact matches;
- **C.** suggest visually similar items.

**Recommendation:** Recommend B for reliable file deduplication. C produces candidates, not proof of duplication, and should not drive automatic destructive actions.

#### C37 How should missing metadata behave?

- **A.** leave it blank;
- **B.** ask the user;
- **C.** infer with a visible confidence label.

**Recommendation:** Recommend A for nonessential fields and B for consequential decisions. C must not present a guess as an original fact.

#### C38 What export is most useful?

- **A.** a simple human-readable report;
- **B.** structured data for another tool;
- **C.** original media plus related decisions.

**Recommendation:** Recommend according to the actual next use. Confirm formats and fidelity rather than assuming every source can export identically.

#### C39 What should deletion mean?

- **A.** remove from this view;
- **B.** move to a recoverable archive;
- **C.** permanently remove from the system.

**Recommendation:** Recommend B when appropriate. Clarify whether originals, copies, metadata and shared access are affected before choosing or executing.

#### C40 How long should inactive content remain?

- **A.** until the owner removes it;
- **B.** a defined retention period with notice;
- **C.** only for the active task.

**Recommendation:** Recommend based on user need, privacy and operating cost. Any automatic removal requires an explicit, understandable rule.

### C6 Technical feasibility and operations

Use for software or digital systems. Research factual constraints instead of asking users to guess what a platform supports.

#### C41 Where must the experience work?

- **A.** browser;
- **B.** native desktop or mobile app;
- **C.** an existing tool's workflow.

**Recommendation:** Recommend C when it meets the need with less maintenance. Choose A or B for actual capability or experience requirements, not novelty.

#### C42 Where may processing happen?

- **A.** on the user's device;
- **B.** on a hosted service;
- **C.** a deliberate split.

**Recommendation:** Recommend A for strict locality where feasible, B for shared availability, and C only with a clear boundary for what leaves the device.

#### C43 What availability is needed?

- **A.** only while the owner is present;
- **B.** on demand at any time;
- **C.** continuous time-critical operation.

**Recommendation:** Recommend the least demanding level that meets the outcome. C changes monitoring, support and reliability costs substantially.

#### C44 How should hosting ownership work?

- **A.** a user-owned account;
- **B.** an organization's account;
- **C.** a temporary demonstration environment.

**Recommendation:** Recommend A or B for a lasting project. C must have an explicit expiration and migration plan if it becomes important.

#### C45 Which scale should be supported first?

- **A.** a small known group;
- **B.** a larger bounded pilot;
- **C.** open-ended public use.

**Recommendation:** Recommend a concrete bounded target before estimating. Replace these labels with actual expected users, files and traffic for the project.

#### C46 How much integration is essential?

- **A.** none;
- **B.** one critical service;
- **C.** several connected services.

**Recommendation:** Recommend B only when the integration is necessary to the core journey. Verify account access, supported operations, limits and data permissions before promising it.

#### C47 What operating budget is acceptable?

- **A.** no recurring paid service;
- **B.** a defined monthly ceiling;
- **C.** a variable budget tied to usage.

**Recommendation:** Recommend B for predictable hosted projects. Research current prices and include storage and transfer assumptions before presenting a figure.

#### C48 How should updates be handled?

- **A.** occasional manual maintenance;
- **B.** a regular review cadence;
- **C.** an actively supported service.

**Recommendation:** Recommend B for a lasting small project. Identify the owner and expected effort; do not make ongoing support disappear from the plan.

### C7 Familiar interaction patterns

Use for interactive products. Begin with the audience's established habits, then inspect how those habits apply in this context.

#### C49 Which familiar product category is the best reference?

- **A.** file browser;
- **B.** inbox or task list;
- **C.** gallery or media viewer.

**Recommendation:** Recommend the category matching the primary action. Borrow the mental model rather than every feature or visual detail.

#### C50 How do users expect selection to begin?

- **A.** visible checkbox or selection control;
- **B.** long press on touch with a visible alternative;
- **C.** a persistent selection mode.

**Recommendation:** Recommend A for discoverability. B may suit familiar mobile lists, but test conflicts and accessibility.

#### C51 What should swipe do in this context?

- **A.** navigate items;
- **B.** reveal contextual actions;
- **C.** have no essential function.

**Recommendation:** Recommend the established convention for the specific screen and platform. Do not assign both navigation and deletion to an ambiguous gesture.

#### C52 How should deletion be presented?

- **A.** a visible menu action;
- **B.** familiar swipe-to-reveal with the same visible alternative;
- **C.** a review screen for batch removal.

**Recommendation:** Recommend C for consequential batch operations and A or B for routine recoverable item actions.

#### C53 How should navigation be organized?

- **A.** a small set of persistent destinations;
- **B.** a hierarchical collection structure;
- **C.** a guided sequence.

**Recommendation:** Recommend B for a library and C for a bounded review task. Choose based on the journey rather than visual fashion.

#### C54 What should happen after an item response?

- **A.** stay for review;
- **B.** advance automatically with clear feedback and undo;
- **C.** let the user choose a persistent mode.

**Recommendation:** Recommend A when comparison matters, B when repeated decisions need speed. C adds a setting to explain.

#### C55 How should advanced actions appear?

- **A.** in a familiar overflow menu;
- **B.** in a visible secondary toolbar;
- **C.** in a separate expert mode.

**Recommendation:** Recommend A for occasional actions and B for frequently repeated ones. Do not hide essential completion controls.

#### C56 What should the novice walkthrough inspect first?

- **A.** whether a new user can start;
- **B.** whether they can complete and recover;
- **C.** the entire core journey.

**Recommendation:** Recommend C. This is a heuristic review unless real representative users perform it; label the evidence honestly.

### C8 Visual design and responsive behavior

Use after the workflow is coherent enough to show realistic screens. Treat the examples as candidates, not universal defaults.

#### C57 Which visual character fits this project?

- **A.** restrained utility;
- **B.** editorial with strong imagery and headings;
- **C.** expressive and playful.

**Recommendation:** Recommend the character that supports the content and audience. Show comparable examples before recording an adjective as a full design specification.

#### C58 Which palette direction feels right?

- **A.** botanical green;
- **B.** cool slate;
- **C.** iris.

**Recommendation:** Recommend only after comparing the same screen. For the photo example, iris was accepted while green and slate were rejected; other projects may choose differently.

#### C59 What should lead the hierarchy?

- **A.** content imagery;
- **B.** task controls;
- **C.** explanatory text.

**Recommendation:** Recommend A for photo exploration and B for high-frequency operations. A strong visual hierarchy must still keep required actions discoverable.

#### C60 How should headings feel?

- **A.** strong serif;
- **B.** neutral sans-serif;
- **C.** compact system-like headings.

**Recommendation:** Recommend A for an editorial direction if readable at required sizes. Compare a real long title and mobile screen, not a specimen alone.

#### C61 Which control shape suits the accepted direction?

- **A.** full pill;
- **B.** rounded rectangle;
- **C.** restrained square corners.

**Recommendation:** Recommend B for a structured editorial interface. Keep palette and layout constant so the answer actually resolves shape.

#### C62 How dense should the main view be?

- **A.** spacious with fewer items;
- **B.** balanced;
- **C.** compact with many items.

**Recommendation:** Recommend B unless the core job demands scanning large collections. Test with realistic content and device sizes rather than assuming spacious always means easier.

#### C63 What should change on a small screen?

- **A.** the same information reflows;
- **B.** secondary details move behind an explicit control;
- **C.** a deliberately simplified workflow.

**Recommendation:** Recommend B when the full task remains necessary. C must not remove a required action without a reason.

#### C64 What motion should support the experience?

- **A.** minimal feedback only;
- **B.** restrained transitions explaining changes;
- **C.** expressive animation.

**Recommendation:** Recommend B when motion clarifies state. Respect reduced-motion needs and do not make an animation the only signal of success or error.

### C9 Resilience and inclusive use

These questions choose appropriate behavior. Baseline accessibility, truthful feedback and protection against avoidable loss are requirements rather than optional upgrades.

#### C65 What offline capability is needed?

- **A.** clear offline notice with no edits;
- **B.** saved read-only material;
- **C.** local edits that synchronize later.

**Recommendation:** Recommend A or B unless offline editing is central. C requires explicit conflict and pending-state rules.

#### C66 How should save failures appear?

- **A.** persistent inline status with retry;
- **B.** a blocking dialog;
- **C.** a recoverable task queue.

**Recommendation:** Recommend A for individual edits and C for batches. A disappearing message is insufficient when work remains unsaved.

#### C67 What should happen to simultaneous edits?

- **A.** prevent overlapping edits;
- **B.** detect conflicts and ask;
- **C.** merge safe fields automatically and flag the rest.

**Recommendation:** Recommend A for simple bounded workflows and B or C when collaboration requires concurrent changes.

#### C68 How should destructive mistakes be recoverable?

- **A.** immediate undo;
- **B.** recoverable archive;
- **C.** version history.

**Recommendation:** Recommend according to the action's duration and harm. A brief undo window alone may not protect a large batch or a mistake noticed later.

#### C69 Which devices need first-class testing?

- **A.** phones;
- **B.** desktops with keyboard and pointer;
- **C.** both equally.

**Recommendation:** Recommend the actual primary usage pattern. Even when one is primary, define what supported secondary devices must be able to do.

#### C70 How should dense content adapt to access needs?

- **A.** adjustable size and reflow;
- **B.** alternate list presentation;
- **C.** both where necessary.

**Recommendation:** Recommend the combination needed by the content. Do not treat readability or keyboard access as a style preference to decline.

#### C71 What should happen if a file cannot be processed?

- **A.** skip with a clear report;
- **B.** stop the whole batch;
- **C.** quarantine the item for later review.

**Recommendation:** Recommend A for independent items and B if partial output would be misleading or unsafe.

#### C72 How should slow operations communicate progress?

- **A.** determinate progress when measurable;
- **B.** named stages when totals are unknown;
- **C.** a background task with completion status.

**Recommendation:** Recommend truthful progress tied to actual work. Do not fabricate a percentage to make uncertainty look controlled.

### C10 Privacy and consequential constraints

Use for every project at an appropriate depth. These prompts clarify user intent; applicable legal, security and approval requirements still govern execution.

#### C73 Who may see the final result?

- **A.** only the owner;
- **B.** named participants;
- **C.** a public audience.

**Recommendation:** Recommend the narrowest audience that meets the goal. Public release is a separate consequential action, not implied by choosing a public-facing design.

#### C74 Which personal data is truly necessary?

- **A.** none;
- **B.** basic identity and contact details;
- **C.** sensitive information essential to the task.

**Recommendation:** Recommend data minimization. If C is necessary, clarify exact fields, purpose, recipients and retention before collection or transmission.

#### C75 How should sharing links behave?

- **A.** restricted to verified members;
- **B.** accessible to anyone holding the link;
- **C.** publicly indexed.

**Recommendation:** Recommend A for private material. Explain forwarding and revocation implications; “unlisted” does not mean access-controlled.

#### C76 What should be logged?

- **A.** operational errors without unnecessary content;
- **B.** limited activity history;
- **C.** detailed audit history.

**Recommendation:** Recommend B or C only where accountability needs justify the data. Avoid collecting private content merely because logging is convenient.

#### C77 How should a departing participant regain access?

- **A.** a verified invitation;
- **B.** owner review;
- **C.** no return after a defined cutoff.

**Recommendation:** Recommend A for ordinary collaboration and B when membership has consequences. Verify the actual identity flow before relying on it.

#### C78 How should paid dependencies be approved?

- **A.** a one-time budget;
- **B.** a capped recurring budget;
- **C.** case-by-case review.

**Recommendation:** Recommend the model matching the commitment. State merchant, service and total conditions before execution where approval is required.

#### C79 What should a real-data pilot use?

- **A.** representative fictional data;
- **B.** a small authorized real sample;
- **C.** the full dataset.

**Recommendation:** Recommend A for early interaction work and B for realistic integration testing. C is rarely necessary before the pipeline is validated.

#### C80 What should happen if required access is unavailable?

- **A.** pause the affected step and continue independent work;
- **B.** use an authorized supported alternative;
- **C.** revise the scope.

**Recommendation:** Recommend A first while investigating B. Never reinterpret denial as permission to find a workaround.

### C11 Delivery and success evidence

Use before execution and again before declaring completion. Replace broad labels with measurable project-specific criteria.

#### C81 What will count as the deliverable?

- **A.** editable plan or design;
- **B.** working prototype;
- **C.** operational production result.

**Recommendation:** Recommend matching the user's actual request. A polished prototype must not be reported as C when real data, security or deployment remain unverified.

#### C82 What is the first validation method?

- **A.** expert or heuristic inspection;
- **B.** representative user walkthrough;
- **C.** controlled real-world pilot.

**Recommendation:** Recommend A early, then B or C when user behavior or operational conditions matter. Do not equate A with tested usability.

#### C83 Which success measure is most important?

- **A.** task completion;
- **B.** quality of the resulting output;
- **C.** time or effort saved.

**Recommendation:** Recommend one primary measure plus relevant guardrails. Avoid optimizing speed while quietly degrading result quality or accessibility.

#### C84 How should the first release be introduced?

- **A.** private review;
- **B.** limited pilot;
- **C.** broad launch.

**Recommendation:** Recommend B when real-world uncertainty remains. C requires stronger support, rollback and capacity readiness than a private demonstration.

#### C85 What should happen if validation fails?

- **A.** revise the design;
- **B.** narrow the scope;
- **C.** reconsider the premise.

**Recommendation:** Recommend the option supported by the failure. Repeatedly patching an interface cannot solve a project that does not address a worthwhile need.

#### C86 What form of handoff is most useful?

- **A.** a concise guide;
- **B.** detailed operating documentation;
- **C.** a guided session plus reference.

**Recommendation:** Recommend C when unfamiliar operations matter and B when maintenance passes to another owner. Keep the current specification consistent with the artifact.

#### C87 What must be portable?

- **A.** the content;
- **B.** content and decisions;
- **C.** the complete implementation and configuration.

**Recommendation:** Recommend B for projects where reasoning and ownership matter. Verify actual export support rather than assuming portability from file access.

#### C88 How should unresolved items be handled at handoff?

- **A.** block delivery if essential;
- **B.** deliver a clearly labeled partial result;
- **C.** defer to a named later phase.

**Recommendation:** Recommend A for missing core requirements and B for useful independent work. Never hide essential gaps under “future improvements.”

### C12 Exceptions changes and clarity checks

Use throughout discovery. These prompts catch conditions that a happy-path questionnaire misses.

#### C89 What if a participant never responds?

- **A.** proceed after owner review;
- **B.** close at a deadline;
- **C.** require all responses.

**Recommendation:** Recommend A or B unless unanimity is essential. C needs an escalation route to avoid a permanently unfinished activity.

#### C90 What if the owner becomes unavailable?

- **A.** a designated backup takes over;
- **B.** the project pauses;
- **C.** participants can elect a replacement.

**Recommendation:** Recommend A for consequential ongoing work. B may be sufficient for a personal low-stakes project.

#### C91 What if the input is much larger than expected?

- **A.** enforce a clear limit;
- **B.** split into batches;
- **C.** scale the infrastructure.

**Recommendation:** Recommend A or B for a bounded first version. C requires verified cost and performance evidence.

#### C92 What if the user changes a settled decision?

- **A.** revise within the current phase;
- **B.** defer the change;
- **C.** restart the affected design branch.

**Recommendation:** Recommend based on dependency impact. Do not reopen unrelated decisions or preserve contradictory rules to avoid rework.

#### C93 How should a new major feature be handled?

- **A.** later phase;
- **B.** separate companion workflow;
- **C.** replacement of the current priority.

**Recommendation:** Recommend the path that protects the most important outcome. A is not automatically right when the user's real priority has changed.

#### C94 What level of explanation helps this user decide?

- **A.** concise options with one reason;
- **B.** options with detailed consequences;
- **C.** a concrete example before choosing.

**Recommendation:** Recommend C for unfamiliar concepts and A for familiar low-impact choices; adapt without reducing coverage.

#### C95 How should an unresolved preference be treated?

- **A.** show a prototype;
- **B.** use an explicitly accepted temporary assumption;
- **C.** intentionally defer the affected work.

**Recommendation:** Recommend A when seeing the result will clarify intent. Never call an unanswered material preference confirmed.

#### C96 Does the final readback match the intended project?

- **A.** yes, including listed deferrals;
- **B.** mostly, with named corrections;
- **C.** no, revisit the main outcome.

**Recommendation:** Recommend honest correction over premature agreement. Resolve B or C and read back the revised model before claiming scoped clarity.

### C13 Event project branch

Use for gatherings, workshops and experiences. Retain the universal intent, scope, privacy, delivery and exception questions.

#### C97 What should attendees gain?

- **A.** a relationship or connection;
- **B.** a skill;
- **C.** a finished shared experience or output.

**Recommendation:** Recommend the outcome that explains why people should attend. Activities should serve this outcome rather than merely fill time.

#### C98 What group size supports that outcome?

- **A.** a small facilitated group;
- **B.** several small groups;
- **C.** a large audience.

**Recommendation:** Recommend A for deeper participation. B needs more facilitators and C changes the format toward presentation rather than equal interaction.

#### C99 What participation structure fits?

- **A.** a guided session;
- **B.** stations with choice;
- **C.** an open social format.

**Recommendation:** Recommend A for beginners learning a skill, B for varied interests and C for relationship-focused gatherings with enough social support.

#### C100 What venue arrangement is best?

- **A.** an existing accessible community space;
- **B.** a hired specialist venue;
- **C.** an online format.

**Recommendation:** Recommend the least complex suitable option after checking availability, access, capacity and equipment. Do not treat a suggested venue as booked.

#### C101 How should materials be provided?

- **A.** organizer supplies all;
- **B.** attendees bring clearly specified items;
- **C.** a shared pool.

**Recommendation:** Recommend A for predictable beginner access if budget allows. B needs reminders and a backup for missing materials.

#### C102 How should registration work?

- **A.** direct invitation;
- **B.** a limited-capacity signup;
- **C.** open attendance.

**Recommendation:** Recommend B when materials or space depend on numbers. Clarify waitlists, cancellations and what personal information is necessary.

#### C103 What is the main contingency?

- **A.** facilitator absence;
- **B.** venue or weather disruption;
- **C.** unexpectedly low or high attendance.

**Recommendation:** Recommend addressing all applicable risks, beginning with the most consequential one. Each selected branch needs a concrete backup owner and trigger.

#### C104 What should the final run sheet contain?

- **A.** timing and activities;
- **B.** timing, responsibilities and materials;
- **C.** the above plus contingencies and contact routes.

**Recommendation:** Recommend C for a real event. Use verified details and authorized contacts; distinguish proposed arrangements from confirmed ones.

### C14 Research project branch

Use for investigations, comparisons and decision studies. Do not impose software delivery concepts on an evidence-gathering task.

#### C105 What decision will the research inform?

- **A.** whether to proceed;
- **B.** which option to choose;
- **C.** how to implement an already chosen direction.

**Recommendation:** Recommend naming the exact decision before collecting sources. A broad topic alone does not define a useful research scope.

#### C106 Which evidence should come first?

- **A.** existing authoritative sources;
- **B.** structured conversations;
- **C.** direct observation or experiment.

**Recommendation:** Recommend based on the uncertainty. Existing facts favor A; unmet needs may require B; claims about behavior often need C.

#### C107 How broad must the sample be?

- **A.** exploratory few cases;
- **B.** a defined representative target;
- **C.** comprehensive coverage of a bounded set.

**Recommendation:** Recommend A for generating hypotheses, not population claims. B requires a sampling plan; C requires a verifiable universe of cases.

#### C108 How should conflicting evidence be handled?

- **A.** present competing explanations;
- **B.** seek a discriminating source or test;
- **C.** narrow the conclusion.

**Recommendation:** Recommend B where feasible, with A and C when uncertainty remains. Do not average incompatible claims into false certainty.

#### C109 What depth of sourcing is needed?

- **A.** a short source-backed brief;
- **B.** an evidence matrix;
- **C.** a reproducible research record.

**Recommendation:** Recommend B for consequential comparisons and C when another researcher must repeat the process. Cite what actually supports each claim.

#### C110 What role should interviews play?

- **A.** illustrative context;
- **B.** structured input across comparable participants;
- **C.** the main evidence base.

**Recommendation:** Recommend B when comparisons matter. Obtain required consent and avoid implying a small set of interviews represents everyone.

#### C111 What is the stopping condition?

- **A.** enough evidence for the named decision;
- **B.** a fixed research window;
- **C.** complete coverage of the bounded source set.

**Recommendation:** Recommend A with a time constraint. If the window ends first, report the remaining uncertainty rather than forcing a conclusion.

#### C112 What should the result emphasize?

- **A.** recommendation and rationale;
- **B.** competing options with uncertainty;
- **C.** findings without a recommendation.

**Recommendation:** Recommend A when the decision basis is strong and B when material tradeoffs remain. C fits a descriptive assignment, not an unfulfilled decision request.

### C15 Learning project branch

Use for study, practice and skill-building. Apply the same clarity standard to motivation, constraints and assessment.

#### C113 What is the first useful learning outcome?

- **A.** perform an everyday task;
- **B.** finish a small project;
- **C.** understand a body of theory.

**Recommendation:** Recommend B when a tangible result sustains motivation, A for immediate practical need and C when conceptual understanding is the explicit goal.

#### C114 What starting point is most accurate?

- **A.** complete beginner;
- **B.** some practice with gaps;
- **C.** experienced but seeking depth.

**Recommendation:** Recommend a short diagnostic exercise to verify the self-assessment before setting difficulty. Do not make the learner repeat material they already understand.

#### C115 What schedule is realistic?

- **A.** short daily sessions;
- **B.** longer weekly sessions;
- **C.** flexible sessions around milestones.

**Recommendation:** Recommend the rhythm the user can actually keep. Build the plan around available time rather than assuming motivation creates extra hours.

#### C116 What practice format is most appealing?

- **A.** guided exercises;
- **B.** one ongoing project;
- **C.** varied small challenges.

**Recommendation:** Recommend B for a coherent creative outcome and A for foundational techniques. A hybrid should have a clear role for each part, not a doubled workload.

#### C117 How should feedback arrive?

- **A.** self-check against examples;
- **B.** regular review by a person or agent;
- **C.** peer exchange.

**Recommendation:** Recommend B when mistakes are hard to diagnose. Clarify what the reviewer can reliably assess and where expert instruction is needed.

#### C118 What should happen after a missed week?

- **A.** resume without catching up;
- **B.** use a shorter recovery session;
- **C.** revise the timeline.

**Recommendation:** Recommend A or B for habit formation. Avoid turning one missed interval into an unrealistic backlog.

#### C119 How should progress be demonstrated?

- **A.** a repeatable task done better;
- **B.** a finished artifact;
- **C.** an explanation or assessment.

**Recommendation:** Recommend the evidence matching the outcome. Time spent and resources consumed are activity measures, not proof of learning.

#### C120 What happens after the first milestone?

- **A.** consolidate with repetition;
- **B.** attempt a more demanding project;
- **C.** reassess goals before continuing.

**Recommendation:** Recommend C when interests may change and A when the skill is not yet reliable. Let evidence and motivation guide the next cycle.
