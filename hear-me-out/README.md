# Hear Me Out

**Discover requirements you didn't know you needed to decide.**

You may know the outcome you want without knowing every decision it depends on.
A request for a photo-sharing app, community workshop, research study, or
learning plan can leave authority, recovery, ownership, cost, and completion
undefined. These details shape whether the result actually fits your needs.

Hear Me Out helps the AI bring those overlooked decisions into the conversation.
It explains the consequences, offers tailored choices with recommendations, and
records your answers in a coherent project specification. You keep control of
the meaningful decisions throughout discovery.

## Why choose Hear Me Out?

- **Discover the gaps you would not know to ask about.** The agent examines the
  whole project, including failure paths, conflicting actions, maintenance,
  handoff, and domain-specific constraints. You do not have to arrive with a
  complete requirements checklist.
- **Make unfamiliar decisions approachable.** Focused multiple-choice questions
  explain what each option changes and why one might fit your goal. You can
  combine options, reject them, or answer freely.
- **Keep the project faithful to your intent.** A newly surfaced consideration
  starts as a proposal or open item. Your preference confirms the chosen
  behavior; the AI's recommendation does not settle it for you.
- **Carry decisions into the result.** Answers and corrections update the
  current specification and affected workflows, permissions, states, and
  acceptance conditions. A final readback lets you confirm the complete scoped
  project, including exclusions and deferrals.

The useful outcome is a clearer, more complete account of what you want and
why, with material uncertainty visible. Question count alone is not evidence
that the agent understood you.

## Details it helps you notice

| Area | An overlooked question | Why the answer changes the project |
| --- | --- | --- |
| Authority | Who makes the final decision when participants disagree? | Determines roles, closing rules, and conflict resolution. |
| Privacy | When may participants see one another's responses? | Determines visibility, independence of feedback, and access rules. |
| Failure and recovery | What happens if a save or upload fails halfway through? | Determines pending states, retry behavior, and protection of unfinished work. |
| Reversibility | Can someone revise a choice after submission or reopen finished work? | Determines state transitions, history, and who can reopen it. |
| Ownership and exit | What should people be able to export, keep, or remove when they leave? | Determines portability, retention, and access revocation. |
| Cost and maintenance | Who maintains the result, and what recurring cost is acceptable? | Determines service choices, operating responsibility, and support expectations. |
| Completion and exceptions | What happens if a participant never responds or a key person becomes unavailable? | Determines finish conditions, deadlines, and fallback ownership. |

These are examples, not mandatory features or a fixed questionnaire. The agent
selects the material issues for your project. Accessibility and applicable
security requirements remain baselines; preference questions address genuine
tradeoffs such as visibility, retention, and offline behavior. Uncertain
capabilities and prices need research or testing, rather than a preference vote.

## A small example

Your initial idea: “Help our group choose the best travel photos.”

One easily overlooked decision is **when people can see the group's responses**.
That affects how independent their judgments remain.

The agent might ask:

> When should reviewers see the group's responses?
>
> **A. After each person finishes.** Gives that person immediate feedback, but
> they may influence people who are still reviewing.
>
> **B. After the host closes review.** Keeps input independent until closure;
> participants wait for the host.
>
> **C. Only show the final selection.** Keeps individual responses private;
> participants see less of the group's reasoning.
>
> I recommend B if independent input matters most. You can describe another rule.

If you choose B, the agent records the reveal timing and updates closure and
visibility requirements. It still clarifies what the reveal contains: named
answers, anonymous totals, or another agreed view. A preference about timing
does not silently approve every downstream detail.

## How discovery works

1. Start with your idea, or compare a few distinct directions if it is still open.
2. Map the whole project and inspect the gaps, dependencies, and likely omissions.
3. Ask the next consequential question with options, tradeoffs, and a recommendation.
4. Update the specification as you answer, correcting related sections together.
5. Use examples, research, or a prototype when they resolve uncertainty better.
6. Read back the scoped specification and incorporate your corrections before
   recording that it matches your intent.

The agent chooses an adaptive depth of **20–120 substantive discovery
questions**. Simpler projects start near the lower end; unfamiliar, complex, or
high-consequence work receives more depth. Follow-ups and final confirmations
count toward the cap. The bank's 120 prompts are optional starting points, and
the agent can write better project-specific questions. It stops at the earliest
sufficient depth after 20 when you validate the specification; your explicit
instruction to shorten or end discovery takes precedence.

Confirmed intent, temporary assumptions, and verified behavior are recorded
separately. A prototype or a design choice does not establish that an integration
works or authorize new external actions.

## Choosing among related skills

Related skills also uncover requirements and edge cases. Hear Me Out's focus is
making overlooked project decisions understandable, letting you settle them,
and keeping the whole specification faithful to those choices. The table below
helps you choose a workflow that fits your needs.

| Related workflow | Its emphasis in the inspected instructions | Choose Hear Me Out when you want… |
| --- | --- | --- |
| [Grill Me / grilling](https://github.com/mattpocock/skills/blob/4588b32ecab9ecc9fc8cc6b6c5e7d675b6004b0d/skills/productivity/grilling/SKILL.md) | A dependency-tree interview, recommendations, and rounds of currently answerable questions; multiple choices are permitted. | Usually one focused decision at a time, an explicit 20–120 budget, and the bundled coverage, specification, and readback records. |
| [Spec Kit: clarify](https://github.com/github/spec-kit/blob/5364d7ce6ecaedbaac6caf847541465927eb93c2/templates/commands/clarify.md) | Up to five questions per session to resolve ambiguity in an existing feature specification. | Broader discovery from an initial idea, with room to explore overlooked operating details across the agreed project. |
| [Questionnaire](https://github.com/srinitude/questionnaire/blob/35bb0262eabf6c1302525082a149ee01bfec910c/skills/questionnaire/SKILL.md) and [Interactive Questionnaire](https://github.com/duskykitecn/interactive-questionnaire/blob/60252ae6bd29bef2a6782434770dcf6270196908/interactive-questionnaire/SKILL.md) | Guided answer capture, browser/form interfaces, and durable or structured answers. | A discovery conversation and a complete intent readback through the host's supported chat or artifact tools, without requiring a separate browser-form runtime. |
| [interview-me](https://github.com/Sorbh/interview-me/blob/ad9e1a886396095989d05381519bc479df01db87/skills/interview-me/SKILL.md) | A software-architect interview with evolving coverage, codebase analysis, security checks, and optional red-team review. | Coverage adapted to software, events, research, or learning, with the same guided-choice and intent-confirmation method. |

The comparison reflects published instructions reviewed on 6 October 2026;
it is a workflow comparison, not a performance benchmark. The individual
techniques are shared by other skills. Hear Me Out's value is the way this
package combines broad omission checking, approachable decisions, and faithful
specification maintenance.

## Use it

Install through the [skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add yangandi114/skills --skill hear-me-out
```

Choose your agent when prompted. For Codex, invoke `$hear-me-out`. If you install
through the skills CLI for Claude Code, invoke `/hear-me-out`.

Claude Code users can also install the skill as a plugin from this repository's
marketplace:

```text
/plugin marketplace add yangandi114/skills
/plugin install hear-me-out@yangandi114-skills
```

With that plugin installation, invoke `/hear-me-out:hear-me-out`.

Hear Me Out contains instructions and supporting documents, with no bundled
executable scripts, API clients, services, or telemetry. It uses your agent's
tools for questions, notes, research, and optional prototypes, following your
instructions and environment permissions. Project details and saved artifacts
follow your agent's data handling and workspace policies.

For manual installation:

Copy the `hear-me-out` folder into your agent's configured skills directory. For
Codex, use `$CODEX_HOME/skills/` when configured, otherwise usually
`~/.codex/skills/`. Then invoke:

> Use $hear-me-out to help me shape this idea. Surface requirements I might
> overlook, explain the choices and your recommendation, and keep a specification
> that reflects my answers.

See [the skill instructions](SKILL.md), [coverage guidance](references/coverage.md),
[question bank](references/question-bank.md),
[specification template](templates/project-spec.md), and
[evaluation scenarios](references/evaluation.md). Narrow edits and simple factual
questions do not need a full discovery engagement unless you request one.

## License

Hear Me Out is available under the [MIT License](LICENSE). You may use, modify,
share, and include it in commercial projects. Keep the copyright and license
notice with copies or substantial portions of the skill. External projects
linked in this guide retain their own licenses.
