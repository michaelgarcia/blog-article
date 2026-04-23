# write-article

A Claude Code skill for writing long-form LinkedIn articles — from rough notes to a proofread, publish-ready draft — through a collaborative, conversational workflow.

## What It Does

You share your raw ideas. The skill guides you through the rest: clarifying questions, title options, a first draft calibrated to your voice, iterative revisions, and a structured proofreading pass before you publish.

The workflow has six phases:

1. **Notes Intake** — paste structured notes or free-form text; the skill extracts structure silently if needed
2. **Clarification** — up to 3 targeted questions to fill genuine gaps before drafting (skipped if your notes are complete)
3. **Title Direction** — 2–3 title + subtitle combinations to choose from before the draft begins
4. **First Draft** — produced against your voice profile, with a pre-delivery checklist and voice check run internally
5. **Iteration** — targeted edits with brief explanations; suggest alternatives rather than impose changes
6. **Proofreading** — six-area check (typos, logic/arguments, focus/structure, voice consistency, banned phrases, sub-agent reader test) with High/Medium/Low prioritized output

## Installation

Copy the `SKILL.md` file into your project's skill directory:

```
your-project/
└── .claude/
    └── skills/
        └── write-article/
            └── SKILL.md
```

Then invoke it in Claude Code:

```
/write-article
```

## Customizing for Your Voice

The skill ships with a default **Author Profile** for Michael Garcia. To use it as yourself, edit the `## Author Profile` section in `SKILL.md` — it is clearly marked with comments:

```
<!-- ============================================================
     AUTHOR PROFILE — Edit this section to customize for a new author
     ============================================================ -->
```

Update these fields:

| Field | What to change |
|---|---|
| **Author name** | Your name, used in the document header |
| **Voice** | How you write — tone, sentence style, what to avoid |
| **Thinking Style** | The mental models or perspectives that shape your work |
| **Tone Modes** | The types of articles you write and how each should feel |
| **Target Audience** | Who you are writing for |

Everything else — the workflow phases, checklists, and proofreading logic — stays the same. You only edit the Author Profile.

## Usage

Invoke the skill, then paste your notes in any format:

```
/write-article

Main Idea: Most cloud migrations fail not because of technology, but because of governance gaps no one talks about.

Context: After leading three enterprise migrations in the past two years, I keep seeing the same pattern...

Key Points:
- Governance is treated as a post-migration concern, not a prerequisite
- The teams that succeed define ownership before they touch infrastructure
- ...

Tone: lessons learned
Emotional Arc: starts with the pattern of failure, builds toward a framework for avoiding it
```

Or just paste free-form notes — the skill will structure them for you.

## Proofreading

When you are satisfied with the draft, trigger the proofreading pass:

> "Proofread this" / "Final pass" / "Ready to publish"

The skill will run six checks and return a prioritized report. The sub-agent reader test spawns a fresh agent with only the article — no brief, no original notes — to surface gaps a first-time reader would encounter.

## Article Standards

The skill enforces these defaults, aligned with the Author Profile:

- **Format:** Long-form LinkedIn article (not a post)
- **Length:** 1,000–1,500 words
- **Structure:** Title, subtitle, introduction (2–3 paragraphs), body with `##` section headers, conclusion
- **One core idea** per article — not three, not five
- **No emojis**
- **3–5 hashtags** at the end