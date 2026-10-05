# skills

My personal collection of agent skills.

## Available skills

| Skill | Purpose |
| --- | --- |
| [ui-no-slop](ui-no-slop/SKILL.md) | Create, edit, and review interfaces with clear hierarchy, purposeful styling, and complete interactions. |
| [collaborative-project-discovery](collaborative-project-discovery/SKILL.md) | Shape projects through focused choices with recommendations and a living specification validated by the user. |

`ui-no-slop` covers web, desktop, and mobile UI. It includes researched anti-pattern examples, platform rules, and verification guidance. Explicit branding and existing design systems take precedence over its default restrictions.

`collaborative-project-discovery` captures the communication method in the supplied *Collaborative Project Discovery* playbook: the agent plans broadly, the user makes meaningful choices, and corrections update the current project specification. It includes 120 adaptive prompts, worked dialogues, coverage and decision records, a reusable specification template, and a final scoped-intent readback. It adapts to software, events, research, and learning without making narrow tasks into workshops.

For Codex, copy the desired skill folder into your configured skills directory (`$CODEX_HOME/skills/` when configured, otherwise usually `~/.codex/skills/`). Invoke `$ui-no-slop` or `$collaborative-project-discovery`. Their metadata permits automatic selection when the task matches the description. Other compatible agents use the same `SKILL.md` entrypoint and may have different installation locations.

Example: “Use $collaborative-project-discovery to help me shape this idea. Bring a whole-project plan, ask one meaningful choice at a time, recommend a direction, and keep the specification updated as I answer.”

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
