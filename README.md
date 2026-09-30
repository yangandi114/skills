# skills

My personal collection of agent skills.

## Available skills

| Skill | Purpose |
| --- | --- |
| [ui-no-slop](ui-no-slop/SKILL.md) | Create, edit, and review interfaces with clear hierarchy, purposeful styling, and complete interactions. |

`ui-no-slop` covers web, desktop, and mobile UI. It includes researched anti-pattern examples, platform rules, and verification guidance. Explicit branding and existing design systems take precedence over its default restrictions.

For Codex, copy the `ui-no-slop` folder into your configured skills directory, usually `~/.codex/skills/`, then invoke `$ui-no-slop`. Its metadata permits automatic selection when the task matches its description. Other compatible agents use the same `SKILL.md` entrypoint and may have different installation locations.

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
