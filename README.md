# skills

My opinionated set of custom skills for AI coding assistants. Feel free to use them.

Compatible with Claude Code, Codex, Cursor, and any agent supporting the [Agent Skills standard](https://agentskills.io/specification).


## Install

```sh
npx skills add emmsixx/skills
```

To install a specific skill:

```sh
npx skills add emmsixx/skills --skill lecture-notes
```


## Dotfiles

Add to your setup script to reproduce across machines:

```sh
npx skills add emmsixx/skills --no-confirm
```


## Skills

| Skill | Description |
|-------|-------------|
| [lecture-notes](./lecture-notes/) | Transform lecture materials into exam-ready Markdown notes for Obsidian |
