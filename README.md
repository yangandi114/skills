# skills

My personal collection of agent skills. No skills have been added yet.

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
