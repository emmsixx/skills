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

### lecture-notes requirements

For audio or video lecture inputs, the `lecture-notes` skill uses Groq Whisper for transcription. Make sure `GROQ_API_KEY` is defined in your environment before using those workflows.

```sh
export GROQ_API_KEY=your_groq_api_key_here
```
