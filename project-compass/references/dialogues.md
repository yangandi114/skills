# Worked communication dialogues

Adapted from the user-supplied *Collaborative Project Discovery* playbook.
Examples are illustrative, not live project decisions, authorizations, or results.
Load the sections relevant to the current decision; keep the conversation focused.

## 13 Dialogue from an unknown idea to a workflow

### Turn 1 Bring original directions

**User:** “I want to start a project, but I don’t know what.”

**Agent:** “Here are three different directions. A: a personal photo archive that makes old pictures easy to find. B: a group photo shortlist that helps friends finish choosing a shared collection. C: a visual story builder for turning a trip into a short photo essay. I’d explore B because it solves a clear group task and can have a satisfying small first version. Which direction interests you, or what should I change?”

**User:** “B. I hate endless group chats about which photos to use.”

### Turn 2 Show the whole before the parts

**Agent:** “Then the goal is to finish a shared selection with less discussion. I’d propose: a host adds photos, invites a small group, everyone reviews privately, and the host creates a final set. We need to settle the selection rules, who sees feedback, the review deadline, storage, export and the visual style. I’d leave public profiles and a full photo library out of the first version.”

**Agent:** “Who should make the final selection? A: host judgment; B: automatic group score; C: group shortlist followed by host judgment. I recommend C because the group contributes without forcing the final set to be a popularity contest.”

**User:** “C.”

### Turn 3 Define a useful decision model

**Agent:** “Confirmed: group input informs the shortlist and the host chooses the final set. How should people respond to each photo? A: Include or Pass, which is fastest; B: Pass, Maybe or Include, which preserves uncertainty; C: a five-point score, which adds nuance but takes more effort. I recommend B because people often know a photo is possible before they know it belongs in the final set.”

**User:** “B, and don’t make people choose an exact number.”

### Turn 4 Show the consequences

**Agent:** “Confirmed: Pass/Maybe/Include with no hard quota. I’ll show progress as photos reviewed, not slots filled. Maybe means unresolved interest, not a half-vote. The host will see the response distribution when selecting the final set.”

### What this sequence teaches

The agent brought ideas before asking for requirements, mapped the whole project, resolved authority before scoring, and converted the no-quota correction into visible behavior. Private feedback remains a proposal until accepted; the next question should resolve visibility rather than quietly treating it as confirmed.

## 14 Dialogue with hybrid answers and corrections

### Turn 1 Separate two axes

**Agent:** “While review is open, what should reviewers see? A: only their own answers; B: group totals without names; C: each person's answers. I recommend A because it avoids early votes influencing later ones.”

**User:** “A, but after I finish I want to see what everyone picked.”

**Agent:** “You want private input during review and a reveal afterward. One detail changes access: should the reveal happen when each person finishes, or when the host closes review? I recommend host closure so early finishers cannot influence people still reviewing.”

**User:** “When the host closes it.”

Timing is now confirmed, but the content of the reveal remains open: named answers, anonymous totals or only the final selection. Ask that next before finalizing the visibility rule.

The combined answer is legitimate. It adds a state transition and a visibility rule, not permission to build every visibility mode as a setting. The specification should record the chosen behavior directly.

### Turn 2 Interpret a letter in context

**Agent, earlier question:** “For response visibility: A private, B anonymous totals, C named responses.”

**Agent, later question:** “For button shape: A full pill, B rounded rectangle.”

User, explicitly replying to the earlier question: “Actually B.”

**Agent:** “Changed the visibility choice to anonymous totals during review. The button shape remains open. Because this changes the earlier private-input plan, I’ll update the review screens and access rules together.”

If no reply target is available and the user only writes “Actually B,” the agent should ask which decision they mean. It should not overwrite both choices or guess that the latest list is always intended.

### Separate scenario Correct a mistaken interpretation

In this separate scenario, the reply target was ambiguous and the agent incorrectly changed visibility without clarifying.

**User:** “No, I meant rounded buttons, not public votes.”

**Agent:** “Got it: rounded-rectangle buttons. Reviews stay private until the host closes review. I’ve restored that rule and removed the anonymous-totals change.”

The correction must propagate to the current specification and any generated artifact. A conversational acknowledgment alone does not repair an outdated permissions table.

### Separate scenario Keep a choice project specific

**User:** “For this one, keep it really quiet visually.”

**Agent:** “For this project, I’ll use restrained controls and let the photographs lead.”

Do not record this as “the user always prefers quiet design.” The scope of the preference matters. A later playful event project may call for a completely different visual language.

## 15 Dialogue for a specific visual direction

### Turn 1 Translate an analogy carefully

**User:** “I want it as easy to use as Google Drive, but more editorial.”

**Agent:** “I’ll borrow familiar file-browsing ideas such as clear collections, obvious selection and predictable actions. For the visual character, I’d use large photographs, strong serif headings and a restrained sans-serif interface. We should compare one real review screen before settling the details.”

The analogy describes useful qualities. It does not authorize copying a product wholesale or importing every feature of a file-management platform.

### Turn 2 Compare palettes with the same screen

**Agent:** “Here are three treatments of the same collection screen: A botanical green, accent #2F6F55; B cool slate, accent #52657A; C iris, accent #6255B8. I recommend C for an editorial feel that stays distinct from the photos. The backgrounds and text colors are shown alongside each option.”

**User:** “No green. Slate looks dirty.”

**Agent:** “I’ll remove green and slate from this project. Is iris close, or should we compare a warmer neutral direction?”

**User:** “Iris is good.”

Do not merely rename the rejected slate “mist” and present it again. Ask what felt wrong only if that clarification will help choose the next version. Here, an accepted alternative already exists.

### Turn 3 Isolate shape and hierarchy

**Agent:** “For the main action buttons: A full pill, softer and more casual; B a rounded rectangle, more structured. I recommend B alongside the strong serif headings. I’ll show both with the same iris palette.”

**User:** “B, and make the headings stronger.”

**Agent:** “Confirmed: rounded rectangles and more prominent serif headings. I’ll keep the body text and controls restrained so the hierarchy remains clear.”

### Turn 4 Test mobile character

**User:** “On mobile it should feel more Apple than Material.”

**Agent:** “I’ll compare a mobile screen with restrained surfaces, familiar navigation and generous touch controls. I’ll keep the iris identity and serif headings. We’ll check the actual interactions and accessibility separately from the visual reference.”

### The resulting design record

**Utility:** familiar collection browsing. Character: editorial. Palette: iris candidate tokens. Typography: strong serif headings with a restrained interface face. Shapes: rounded rectangles. Mobile direction: Apple-like qualities requested. Rejected: botanical green and dirty-looking slate. Still to verify: contrast, focus states, long titles, image loading and responsive layouts.

## 16 Dialogue when the project expands

### Turn 1 Recognize a structural change

**User:** “Could this also organize all my local photos, rename them and remove duplicates?”

**Agent:** “That adds a second workflow: managing files on your computer. It needs filesystem access, duplicate rules, previews and recovery for changes to originals. The current project is a group shortlist, so this would materially expand the first version.”

### Turn 2 Offer distinct paths

**Agent:** “Which direction should we take?

A. Finish the group shortlist first and plan the local organizer afterward. Fastest route to the original outcome.

B. Make a separate local organizer that can export a chosen collection into the shortlist. More work, but clearer responsibilities.

C. Replace the first version with a local organizer and postpone group review. Best if personal cleanup is now the main problem.

I recommend A unless organizing your archive matters more than finishing the shared selection.”

**User:** “B, but never delete originals automatically.”

### Turn 3 Translate the constraint into behavior

**Agent:** “Confirmed: a separate local organizer, with no automatic deletion of originals. I’d start with a read-only scan and a proposed change list. Duplicate candidates would be grouped for review. Any move or rename would need a preview and a recoverable plan; deletion is outside this first version.”

The response should not imply that the user has authorized scanning every folder or modifying files. It specifies the intended product and proposes an initial workflow. Actual access and file actions remain subject to the user's authorization and the environment's rules.

### Turn 4 Reopen the affected plan

Update the roadmap, delivery estimate, architecture, data access, risk assessment and tests. The interface now needs scan progress, inaccessible-folder handling, duplicate uncertainty and a reviewable change plan. The integration boundary needs an export/import contract. The original selection model need not be reopened unless the organizer changes it.

### Why this is better than adding a toggle

A checkbox called “organize local photos” conceals a new product. The separation makes scope, risks and ownership visible. It also preserves a useful stopping point: the group shortlist can still be delivered even if local-file integration is blocked.

A good agent welcomes the new idea while explaining its real implications. It should not punish creativity with alarmism or reward it with an unsupported promise of instant implementation.

## 17 Dialogue for blockers and risky actions

### A tool or authentication limitation

**User:** “The sign-in button is there. Is login finished?”

**Agent:** “The sign-in screen is finished. Real account authentication is not verified yet because the required connection is unavailable. The prototype currently uses sample sessions. We can review the interface now; completing login needs the supported connection and an end-to-end sign-in test.”

**User:** “Can you just use another account?”

**Agent:** “We should use the account and access you authorize for this project. If a supported test account is available, we can verify with that. Otherwise, I’ll keep authentication marked as blocked and continue the parts that do not depend on it.”

This keeps the limitation specific. It does not invent a product capability or imply a broad technical impossibility. The agent should check available supported routes before declaring a blocker, and should respect an explicit access denial.

### A consequential command

**User:** “Just clean up the duplicate files.”

**Agent:** “First I need to distinguish exact duplicate files from similar photos. I recommend a read-only report that groups exact matches and shows the paths. Then you can review the proposed changes before anything is moved or deleted.”

**User:** “Use exact matches, keep the oldest, and show me the report.”

**Agent:** “I’ll prepare the report. For exact byte-for-byte duplicates, photo capture metadata is normally identical, so it cannot tell us which copy to keep. A: prefer a folder you identify as canonical; B: use filesystem timestamps, with their reliability limits flagged; C: leave every keep choice for review. I recommend A, preserving related sidecar files and flagging ties instead of guessing.”

The user's request authorizes a report, not deletion. Even a confirmed retention rule does not settle which folder is canonical, which copy has related sidecar data, how ties are handled or whether removal is recoverable.

### An honest completion message

“The report contains 48 exact-match groups in the selected folder. No files were changed. Six groups have no clear canonical copy and need a manual keep choice. The proposed actions are listed with source and destination paths.”

These counts are illustrative, not reported results. In real work, every claimed number and action must come from the actual run. A success message should distinguish what was inspected, proposed, changed and verified, especially when a project combines design work with operations on real data.

## 18 Transfer the method to an event

The same method applies without software architecture or a hosted service. Replace irrelevant system areas with the operational equivalents: venue, guests, staffing, suppliers, access, timing, cost, contingency and communication.

### Idea and outcome

**User:** “I want to organize something for our community.”

**Agent:** “Three directions: A a relaxed dinner for deeper conversation; B a hands-on workshop with a shared result; C a short showcase where people present projects. I recommend B if the goal is for people who do not know one another to connect through doing something together.”

**User:** “A workshop.”

### Whole event map

**Agent:** “I’d plan a two-hour beginner-friendly workshop with a welcome, a short demonstration, small-group making and a shared finish. The main decisions are audience size, activity, venue, accessibility, materials, budget, facilitation, registration and the cancellation plan. We should settle the outcome before choosing supplies.”

### One consequential choice

**Agent:** “What should people leave with? A a finished individual object, which is tangible but needs more materials; B one shared creation, which encourages collaboration; C a new skill practiced through small exercises, which is easier to adapt to different abilities. I recommend C for a mixed-experience group.”

**User:** “C, but I want something they can take home.”

**Agent:** “Then I’d use a skill-first workshop with a small take-home exercise. We can avoid turning it into a complex craft project. Next I’ll propose activities that fit that format and the likely budget.”

### The event coverage review

Check arrival, signage, seating, movement, hearing and visual access, dietary needs if food is provided, materials, facilitator backup, late arrivals, schedule drift and cleanup. Identify what is required, what is a user choice and what depends on venue confirmation. Ask about tradeoffs such as scale versus attention; do not ask whether basic access and safety matter.

### Exit and authorization

A planning gate might require a clear audience, activity, budget range, proposed venue, timetable, staffing and contingency. A venue option is not a booking. A drafted invitation is not a sent invitation. The plan should mark suppliers as proposed until availability and terms are verified and any required approval is obtained.

The final deliverable can be a run sheet and responsibility list. There is no need to create an app merely because an AI agent is helping.

## 19 Transfer the method to research and learning

### Research project

**User:** “I want to understand whether our neighborhood needs a repair café.”

**Agent:** “I’d frame this as a decision study: determine whether there is enough demand, volunteer capacity and venue support to run a small pilot. We could start with A desk research, B a short resident survey, or C a few structured conversations with residents and repair volunteers. I recommend C for the first pass because it can reveal practical barriers before we design a survey.”

**The coverage map becomes:** decision to inform, audience, research questions, evidence sources, sampling limits, consent and privacy, time budget, analysis method, contradictory evidence, uncertainty and the pilot threshold. The agent should distinguish a promising anecdote from representative demand. Recommendations should remain provisional when the evidence is narrow.

A useful gate is not “all information has been collected.” It is “enough credible evidence exists to choose a small pilot, decline it or identify the one missing fact that blocks a decision.” The deliverable may be a short evidence memo with a source register and unresolved questions.

### Learning project

**User:** “I want to learn photography.”

**Agent:** “Which first outcome would feel useful? A more reliable everyday photos, B a coherent photo essay, or C confident manual camera control. I recommend A if you want results quickly, but B may be more motivating if you like finishing a creative project.”

**User:** “B, but I only have twenty minutes a day.”

**Agent:** “Then I’d build a four-week photo-essay plan around short practice: noticing, choosing a theme, shooting sequences and editing. We’ll keep technical lessons tied to the images you need rather than adding a separate theory course.”

The coverage map includes starting level, equipment, time, motivation, practice opportunities, feedback, accessibility, assessment and what happens after a missed week. A realistic first exercise tests the plan better than a long list of resources.

### What transfers across domains

Start with a useful outcome. Offer distinct approaches. Build the whole map. Ask the next high-value question. Turn answers into a coherent artifact. Validate with evidence appropriate to the domain. Keep consequential actions separate from planning. Close discovery when the user validates the scoped project model. Provisional next steps can still proceed, when authorized, to resolve remaining uncertainty.

What does not transfer automatically is a software checklist, a design aesthetic or the photo app's decision model. Adapt the coverage to the project rather than forcing the project into a familiar template.
