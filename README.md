# skills
[![Security: A — Skills Directory](https://www.skillsdirectory.com/api/skills/yangandi114-hear-me-out/badge)](https://www.skillsdirectory.com/skills/yangandi114-hear-me-out)

My personal collection of agent skills.

## Available skills

| Skill | Purpose |
| --- | --- |
| [ui-no-slop](ui-no-slop/SKILL.md) | Create, edit, and review interfaces with clear hierarchy, purposeful styling, and complete interactions. |
| [Hear Me Out](hear-me-out/SKILL.md) | Discover requirements you might overlook through guided choices, then capture a specification that reflects your intent. |

`ui-no-slop` covers web, desktop, and mobile UI. It includes researched anti-pattern examples, platform rules, and verification guidance. Explicit branding and existing design systems take precedence over its default restrictions.

## Hear Me Out

**Discover requirements you didn't know you needed to decide.**

You bring the idea; Hear Me Out helps the AI surface the decisions behind it: who has authority, what happens when something fails, how people recover mistakes, who can see the data, what ongoing costs are acceptable, and what happens after handoff. It explains meaningful options and their consequences so you can express preferences without already knowing every design or operating detail. Your answers define the requirements, and the AI keeps the specification aligned as you refine them.

Choose it when you want a thorough discovery partner that actively checks for overlooked requirements, makes those choices approachable, and reads back the complete scoped project for your confirmation. It adapts to software, events, research, and learning. [Read the guide, examples, and comparison with related skills](hear-me-out/README.md).

The agent chooses **20–120 substantive discovery questions** based on complexity, risk, and uncertainty. The 120-prompt bank is a menu; follow-ups and the final readback count toward the cap. Worked dialogues, coverage and decision records, and a specification template support the workflow.

## Use the skills

Install Hear Me Out through the [skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add yangandi114/skills --skill hear-me-out
```

The installer lets you choose a supported agent, including Codex and Claude Code.
For Claude Code's plugin system, add this repository's marketplace and install:

```text
/plugin marketplace add yangandi114/skills
/plugin install hear-me-out@yangandi114-skills
```

Then invoke `/hear-me-out:hear-me-out` in Claude Code. This repository-hosted
marketplace provides installation; it does not imply inclusion in Anthropic's
official directory.

For Codex, copy the desired skill folder into your configured skills directory (`$CODEX_HOME/skills/` when configured, otherwise usually `~/.codex/skills/`). Invoke `$ui-no-slop` or `$hear-me-out`. Their metadata permits automatic selection when the task matches the description. Other compatible agents use the same `SKILL.md` entrypoint and may have different installation locations.

Example: “Use $hear-me-out to help me shape this idea. Surface requirements I might overlook, explain the choices and your recommendation, and keep a specification that reflects my answers.”

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

## License

Hear Me Out and its marketplace metadata are available under the
[MIT License](hear-me-out/LICENSE). You may use, modify, and redistribute them,
including commercially, while retaining the copyright and license notice.
This license applies to Hear Me Out; other skills have their own licensing terms.
