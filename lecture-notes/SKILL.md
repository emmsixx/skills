---
name: lecture-notes
description: Transform lecture materials (slides, PDFs, text snippets, transcripts) into comprehensive, exam-ready Markdown notes for Obsidian. Use when the user provides lecture content, study materials, or asks to take notes, summarize lectures, or create study guides. Outputs structured notes with key concepts, definitions, LaTeX math, and exam-important callouts.
license: MIT
metadata:
  author: emmsixx
  version: "1.0"
---

# Lecture Notes Skill

Transform lecture materials into structured, exam-ready Markdown notes for Obsidian.

## Output Format

Output all notes inside fenced codeblocks. When content spans multiple chapters or distinct topics, create separate files.

### File Naming
`Chapter X - Title.md` or `Unit X - Title.md`

### Document Structure
```markdown
---
course: [Course name if known]
lecture: [Lecture number/title]
date: [Date if provided]
tags: [relevant, topic, tags]
---

# Title
Brief overview connecting to previous material when applicable.

## Key Concepts
Bulleted summary of the most important takeaways.

## [Content Sections]
Organized by topic from the source material.

## Definitions
New terms introduced in this lecture.

## [Additional Sections as Needed]
Examples, proofs, diagrams, etc.
```

## Formatting Rules

### Headings
No empty lines after headings. Content begins immediately on the next line:
```markdown
## Section Title
Content starts here directly below the heading.
```

### Math and Equations
Use LaTeX inside `$...$` (inline) or `$$...$$` (block):
```markdown
The quadratic formula is $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$.

$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$
```

### Footnotes
Use Markdown footnotes for supplementary information. Never use citations:
```markdown
This concept was introduced in 1905[^1].

[^1]: Additional context or clarification here.
```

### Callouts for Exam-Important Content
Use Obsidian callouts to flag critical information:
```markdown
> [!important] Exam Alert
> This formula is frequently tested.

> [!note] Remember
> Supplementary context or tips.

> [!example] Worked Example
> Step-by-step demonstration.

> [!warning] Common Mistake
> Students often confuse X with Y.

> [!definition] Term
> Formal definition here.
```

### Wiki-Links
Use `[[double brackets]]` to link related concepts:
```markdown
This relates to [[Chapter 2 - Thermodynamics#Entropy]].
```

## Content Guidelines

### Completeness
Capture all information from source material, especially:
- Formulas and equations
- Definitions and theorems
- Examples and worked problems
- Diagrams (describe or recreate in text/ASCII if needed)
- Any content emphasized as important by the lecturer

### Definitions Section
Always include a `## Definitions` section. Format each term:
```markdown
## Definitions
**Term**
Precise definition immediately below.

**Another Term**
Its definition here.
```

### Connections
When possible, reference previous lectures or related concepts:
```markdown
## Key Concepts
- Builds on [[Chapter 3 - Kinematics]] by introducing forces
- Extends the velocity equations to include acceleration
```

### Examples
Preserve all examples from source material. Format with the example callout:
```markdown
> [!example] Finding the Derivative
> Given $f(x) = x^3 + 2x$, find $f'(x)$.
>
> **Solution:**
> $$f'(x) = 3x^2 + 2$$
```

## Multiple Files

When source material covers multiple distinct chapters or units, output each as a separate codeblock with clear file naming:

````markdown
```markdown
<!-- Chapter 1 - Introduction.md -->
---
course: Physics 101
...
```
````

````markdown
```markdown
<!-- Chapter 2 - Mechanics.md -->
---
course: Physics 101
...
```
````
