# Question design and interpretation

Adapted from the user-supplied *Collaborative Project Discovery* playbook.
Examples are illustrative, not live project decisions, authorizations, or results.
Load the sections relevant to the current decision; keep the conversation focused.

## 4 Ask in dependency order

Ask the question whose answer most changes the project, reduces the greatest risk or unlocks the most useful work. Do not follow a rigid list when new information changes the priorities.

### A practical sequence

1. Outcome and success: What should be better when the project is finished?
2. Audience and responsibility: Who uses it, decides and maintains it?
3. Core workflow and scope: What is the smallest complete experience?
4. Consequential constraints: Time, budget, privacy, data location and access
5. Experience structure: Information architecture, interaction model and content
6. Visual direction or presentation style: Concrete comparisons in context
7. Implementation and operations: Verified platform fit, deployment and support
8. Validation and handoff: Evidence, acceptance conditions and ownership

This is a dependency guide, not a mandatory interrogation order. A fixed venue date may come first for an event. A requirement to keep files on a computer may determine software architecture before detailed interface work. An urgent learning deadline may determine the study format before topic depth.

### Prioritize by impact and uncertainty

High-impact, uncertain and expensive-to-reverse decisions deserve an early question or research step. Low-impact, reversible details can use a clearly labeled proposal. For example, a sample album name need not interrupt the user; allowing permanent file deletion should never be treated as a harmless aesthetic preference.

**An agent can explain a priority plainly:** “Whether reviewers can change their answers affects both progress and the finalization rules. I’d settle that before designing the results page.”

### Keep one focused question in flight

Usually ask one question with three or four concrete options. A short related bundle can be appropriate when the user requests speed or the choices are inseparable, but do not hide five independent decisions inside one option. If an answer cannot be mapped cleanly to a single decision, the question is probably too broad.

### Avoid the questionnaire treadmill

Make answers tangible through a revised journey, sample screen, schedule, draft
agenda, or testable outline. Show the effects rather than just asking another
question. Use [the adaptive 20–120 budget](../SKILL.md#adaptive-depth-and-question-budget),
chosen by the agent to fit the project. Cover important intent without requiring
every question in a relevant branch. Count follow-ups, reserve readback slots,
and stop at the earliest sufficient depth after 20 when scoped intent is
validated. A plausible first version alone is insufficient; reaching 120 also
does not prove understanding. At the cap, surface open items and stop asking.

Discovery should alternate thinking, choosing and making. Twenty questions that could have been answered by one realistic prototype are poor use of the user's attention.

## 5 Write choices that reveal real tradeoffs

A good multiple-choice question makes alternatives concrete enough to compare. It uses the user's vocabulary, keeps the alternatives at the same level, and explains what changes when each is selected.

### Reusable question structure

**Decision:** State one question in ordinary language.

**Context:** Give the one or two facts that make this decision matter.

**A:** Describe one coherent approach and its main benefit or cost.

**B:** Describe a distinct approach and its main benefit or cost.

**C:** Describe another meaningful approach, only if one exists.

**Recommendation:** Name an option and explain why it best fits the current goal.

**Flexibility:** Invite a combination, rejection or free-text answer when useful.

### Example

“After reviewers finish, who should choose the final photographs?

A. The host makes the final call. Fast and editorially consistent, but not a vote.

B. The group score determines the set. Predictable and democratic, but a strong photo can lose to broadly acceptable ones.

C. The score creates a shortlist and the host finishes it. More judgment is preserved, with an extra review step.

I recommend C because this project aims for a strong collection while still involving everyone. You can also describe a different split.”

### What makes this recommendation sound

It links to a stated goal, identifies a real cost and leaves room for disagreement. If the user values a strict vote over editorial judgment, the recommendation should change. Do not smuggle an aesthetic or technical preference into an apparently objective conclusion.

### Common option defects

“Simple / advanced / both” rarely explains enough. “Fast / beautiful / secure” falsely suggests basic quality is optional. An option called “recommended” without a reason adds authority without information. An elaborate hybrid should not always occupy option C; it often increases scope and testing burden.

If two choices can independently be true, split the question or explicitly describe the combined design. “Private reviews” and “host final decision” are different axes. Calling them alternatives obscures the actual decision.

### When fewer or more options help

Use two when there are only two meaningful routes. Use four when the fourth reveals a distinct strategy. For a large option space, narrow by a high-level criterion first. Do not flood the user with ten almost-identical colors or architectures to appear comprehensive.

## 6 Interpret answers and update the plan

The answer is evidence about a particular question, not a global preference. “B” refers to the actual question being answered. It does not mean whichever option happens to be B in the most recent unrelated list.

### Resolve the reply target

Use the visible conversation and any explicit reply reference. If the user replies to an earlier question, apply the answer there. If two plausible questions remain, ask a brief clarification before changing a consequential decision: “Do you mean B for review privacy or B for the button shape?” Do not silently choose the interpretation that is easiest to implement.

### Translate without overinterpreting

If the user says “B, but let me change it later,” preserve B and identify the new reversibility requirement. Do not claim approval for every implementation detail associated with B. If the user says “neither, more like a contact sheet,” extract the useful direction and show a revised proposal.

### Separate four kinds of statement

**Confirmed decision:** The user has explicitly selected or clearly endorsed the specific choice.

**Proposal:** The agent recommends an approach that has not been accepted.

**Assumption:** A temporary working choice that needs verification or is safe to revise.

**Open item:** A decision, fact or dependency remains unresolved.

Also record deferred work and superseded decisions. A rejected green palette must not survive elsewhere as an active default after the user chooses iris.

### Revise rather than accumulate

Update the current specification in place, then keep a concise change history if needed. Do not append “actually use iris” while leaving “use green” in the primary design section. A builder should be able to read the current state without reconstructing the entire conversation.

When one decision changes, check dependent sections: components, copy, permissions, data model, tests and delivery plan. If reviews become private, both the screen and the data access rules must change.

### A checkpoint response

**“Confirmed:** private Pass/Maybe/Include reviews, with the host making the final selection. I’ve removed the hard quota from the plan. Reviewers can revise answers until the host closes review. Still open: how the final collection is exported.”

The checkpoint should expose consequential uncertainty without re-asking every settled question. It is especially useful before implementation, after a correction or when the project changes direction.
