# skills

My personal collection of agent skills.

## Available skills

| Skill | Purpose |
| --- | --- |
| [ui-no-slop](ui-no-slop/SKILL.md) | Create, edit, and review interfaces with clear hierarchy, purposeful styling, and complete interactions. |
| [Hear Me Out](hear-me-out/SKILL.md) | Shape projects through 20–120 adaptive questions, recommendations, and a living specification validated by the user. |

`ui-no-slop` covers web, desktop, and mobile UI. It includes researched anti-pattern examples, platform rules, and verification guidance. Explicit branding and existing design systems take precedence over its default restrictions.

**Hear Me Out** (`hear-me-out`) captures the communication method in the supplied project-discovery playbook: the agent plans broadly, the user makes meaningful choices, and corrections update the current project specification. The agent chooses an adaptive depth of **20–120 substantive discovery questions** based on scope, complexity, risk, and uncertainty, stopping once the project is understood and validated. Its 120-prompt bank is a menu rather than a required questionnaire; follow-ups and the final readback count toward the cap. It also includes worked dialogues, coverage and decision records, and a reusable specification template. It adapts to software, events, research, and learning without making narrow tasks into workshops.

For Codex, copy the desired skill folder into your configured skills directory (`$CODEX_HOME/skills/` when configured, otherwise usually `~/.codex/skills/`). Invoke `$ui-no-slop` or `$hear-me-out`. Their metadata permits automatic selection when the task matches the description. Other compatible agents use the same `SKILL.md` entrypoint and may have different installation locations.

Example: “Use $hear-me-out to help me shape this idea. Bring a whole-project plan, ask one meaningful choice at a time, recommend a direction, and keep the specification updated as I answer.”

## Structure

Each skill will live in its own folder at the repository root, following the [Skills Directory file structure](https://www.skillsdirectory.com/docs/skill-file-structure).

The layout below is an example for future skills:

```text
skills/
├── README.md
├── .gitignore
└── skill-name/
    ├── SKILL.md
    ├── references/   # Optional documentation
    ├── scripts/      # Optional executable helpers
    ├── templates/    # Optional file templates
    └── assets/       # Optional static files
```

Use lowercase, hyphen-separated skill folder names. Each folder must contain an uppercase `SKILL.md` with YAML frontmatter containing `name` and `description`, followed by Markdown instructions. Add supporting directories only when the skill needs them.
