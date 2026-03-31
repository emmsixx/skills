# skills

Agent-agnostic skills for AI coding assistants, installable via [skills.sh](https://skills.sh/).

Compatible with Claude Code, Codex, Cursor, Windsurf, GitHub Copilot, and any agent that supports the [Agent Skills open standard](https://agentskills.io/specification).


## Install

```sh
npx skills add emmsixx/skills
```

To install for a specific agent:

```sh
npx skills add emmsixx/skills -a claude-code
npx skills add emmsixx/skills -a cursor
```

To install a single skill:

```sh
npx skills add emmsixx/skills --skill lecture-notes
```


## Skills

| Skill | Description |
|-------|-------------|
| [lecture-notes](./lecture-notes/) | Transform lecture materials into exam-ready Markdown notes for Obsidian |


## Adding to Dotfiles

To reproduce these skills across machines, add an install step to your setup script:

```sh
npx skills add emmsixx/skills --no-confirm
```

Or declare them in a `.skills` file at your dotfiles root and run `npx skills install`.
