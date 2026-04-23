# LinkedIn Article Writing Skill

This skill guides the full article production workflow — from rough notes to a proofread, publish-ready draft — through a collaborative, conversational process.

## Trigger

Activate when the user invokes `/write-article`, or asks to write, draft, or work on a LinkedIn article.

---

<!-- ============================================================
     AUTHOR PROFILE
     Edit this section to customize the skill for a different author.
     The workflow phases below reference this profile generically
     and do not need to be changed when you swap authors.
     ============================================================ -->

## Author Profile

**Author name:** Michael Garcia

**Document header format:**
```
**[mm/dd/yyyy]**
**Author:** Michael Garcia
---
```

### Voice

- Approachable — write without artifice; meaning over elegance
- Active voice throughout
- Precise, meaningful word choices — no filler
- Never academic or detached
- Suggestive, not directive: frame personal experience as "In my experience," "This is what worked for me," "It's worth considering" — not as commands. Readers are professionals who make their own decisions.
- When sharing data or outcomes, be specific: use metrics and numbers rather than vague descriptors

### Thinking Style

This author thinks across three modes simultaneously. Every article should carry at least one of these signatures:

- **Strategist** — connects tactical details to larger strategic patterns; always zooms out to "what does this mean for the industry?"; includes a framework or mental model
- **Shaper** — clear point of view, bold thesis, no hedging; takes a position and defends it; ends with a call to action, not just reflection
- **Growth Seeker** — demonstrates intellectual curiosity; references cross-domain insights; shows the learning journey, not just the conclusion; willing to say "I was wrong about X, and here's what I learned"

### Tone Modes

Adapt based on the article type while keeping the core voice:

- **Lessons learned** — reflective, honest, grounded; share what happened and what it taught; be vulnerable where appropriate
- **Mental models / frameworks** — structured, clear, instructive; walk the reader through the model and show how it applies
- **Industry perspective** — confident, informed, forward-looking; take a position and support it
- **Forward-looking / vision** — bold, aspirational, concrete; paint a picture of what's coming and why it matters

### Target Audience

IT professionals at large — engineers, architects, managers, directors, and executives working in or adjacent to technology. Accessible enough for a broad professional audience while carrying substance for senior practitioners.

<!-- ============================================================
     END AUTHOR PROFILE
     ============================================================ -->

---

## Workflow

### Phase 1 — Notes Intake

Accept the author's input in any format. They may use the structured template below or dump raw text:

```
**Main Idea:** [One sentence — the core thesis or insight of the article]

**Context:** [Why this matters now. What prompted this article — a trend, an experience, a conversation, a realization]

**Key Points:**
- [Point 1: idea + any supporting detail, data, or example]
- [Point 2: idea + any supporting detail, data, or example]
- [Point 3: idea + any supporting detail, data, or example]

**Tone:** [lessons learned | mental model | industry perspective | forward-looking]

**Emotional Arc:** [e.g., "starts with frustration, builds through clarity, ends with forward momentum"]

**Audience note (optional):** [Any specific nuance about who this article is for]

**References / data (optional):** [Any metrics, quotes, sources, or specifics to include]
```

If the author provides unstructured text, silently extract the main idea, context, and key points from it before proceeding. Do not ask them to reformat.

---

### Phase 2 — Collaborative Clarification

1. Restate the core idea in **one sentence** to confirm alignment.
2. Assess whether any of the following are missing or too thin to write a strong article:
   - A concrete context or triggering moment
   - At least one specific example, metric, or story
   - An emotional arc or intended reader journey
   - The tone mode
3. If gaps exist, ask **up to 3 targeted questions** — only what's genuinely needed to write a better article. Do not ask for the sake of process. If the notes are already complete, skip this step entirely and move to Phase 3.

---

### Phase 3 — Title Direction

Propose **2–3 title + subtitle combinations** for the author to choose from.

Title rules:
- Hook the audience — innovative, modern, aspirational
- Must not over-promise; must not be clickbait
- Directly reflects the article's content so the audience knows what to expect
- Sparks curiosity and signals value
- Under 10 words when possible

Subtitle rules:
- One sentence that gives the reader the desire to read the article
- Must summarize the entire article in a single line — not just a hook, but the thesis compressed
- Must align with the title — together they set a clear expectation

Wait for the author to select a direction before drafting.

---

### Phase 4 — First Draft

Produce a full draft following the content standards below. Before presenting, run the Pre-Delivery Checklist and Voice Check Pass (both defined in the Checklists section). Present a clean draft only — do not expose the checklist process.

---

### Phase 5 — Iteration

- Accept feedback in natural language
- Edit only the targeted sections — do not reprint the entire article unless the author requests it
- After each revision, briefly explain what changed and why (one sentence per change is enough)
- Repeat until the author signals readiness for proofreading ("proofread", "final pass", "ready to publish", or similar)

During iteration: suggest alternatives rather than impose changes. If the author's phrasing is intentional, preserve it. Flag stylistic concerns once; do not repeat them if the author keeps their version.

---

### Phase 6 — Proofreading Pass

Run all six checks. Deliver structured feedback. Be direct — no false positivity, no manufactured praise. If a section is clean, say so briefly and move on.

**1. Typos & Grammar** *(Low priority, but exhaustive)*
Catch every spelling error, punctuation issue, and grammatical mistake. Offer corrected versions inline.

**2. Logic & Arguments** *(Highest priority)*
This is the most critical check. Flag:
- Lazy claims stated as fact without evidence
- Unsupported assertions that ask the reader to just trust the author
- Inconsistent reasoning within the article
- Unjustified logical leaps between paragraphs

**3. Focus & Structure** *(High priority)*
- Is there exactly one core idea? Flag any second thesis competing for attention.
- Does every paragraph serve that one idea? Flag any that don't.
- Check for scope creep — if the article is trying to be two things, name it explicitly. Ask: would this be stronger as two separate articles?

**4. Voice Consistency** *(High priority)*
- Check every paragraph against the Author Profile above
- Flag any passage that sounds generic, hedged, or could have been written by anyone
- Mark flagged passages as: **[Voice check: sounds generic]** and suggest a concrete rewrite

**5. Banned Phrases** *(Medium priority)*
Scan the full article for these. If found, flag and rewrite:
- "In today's fast-paced world..."
- "Let's dive in"
- "It's no secret that..."
- "At the end of the day"
- "Game-changer", "disruptive", "revolutionary" (unless used critically or with intentional irony)
- "Rapidly evolving landscape"
- "Unlock the potential"
- "Leverage" as a verb (use "use", "apply", or "build on")
- "Seamless"
- Rhetorical questions as openers that don't land (e.g., "Have you ever wondered...?")
- Any variation of "As an AI..."

**6. Sub-Agent Reader Test** *(Medium priority)*
Spawn a sub-agent. Give it only the article draft — not the original notes, not the brief. Instruct it to read as a first-time reader who knows nothing about the author's intent, and to surface:
- Anything confusing or under-explained
- Any claim that needs more support to be credible
- Any moment where they lost the thread

Report back the reader questions as gaps for the author to decide whether to address.

**Output format:**

```
## Proofreading Report

### Overall Readiness
[Ready to publish | Needs minor revisions | Needs significant revisions]

### Issues by Priority

**HIGH**
- [Issue description with line or paragraph reference]

**MEDIUM**
- [Issue description with line or paragraph reference]

**LOW**
- [Issue description with line or paragraph reference]

### Reader Test Gaps
- [Gap 1]
- [Gap 2]
```

---

## Content Standards

### Document Structure

Every article must include, in this order:

1. **Document header** (use Author Profile format above)
2. **Title** — `#` Markdown header
3. **Subtitle** — one-liner hook below the title
4. **Introduction** — 2–3 short paragraphs
5. **Body** — structured with `##` section headers in title case
6. **Conclusion** — 1–2 short paragraphs

### Introduction Rules
- Open with a kicker: a surprising insight, a tension, or a brief story. Never open with a summary.
- Set the stage: why does this matter, why now?
- End by signaling the article's direction — without giving everything away
- The first 2–3 lines are critical: on LinkedIn, they appear before "see more." Make them count.
- Establish credibility and get to the point quickly. If there's a personal story, keep it brief in the intro and develop it in the body where it's most relevant. Do not front-load with a long anecdote before stating the article's purpose.
- If an Emotional Arc was provided, use it to guide the reader's experience at each stage: opening tension or surprise → building insight → resolution or call to action

### Body Rules
- `##` headers in title case for each section
- One paragraph per idea; each paragraph has a clear topic sentence
- Build the argument progressively — each paragraph earns the next
- One core idea per article. Everything serves that single idea.
- Support claims with specifics: details, examples, metrics, or mental models
- Paragraphs: 3–5 sentences maximum — LinkedIn readers scan; dense blocks lose them
- Use subheadings every 200–300 words
- Bold key phrases sparingly for emphasis and scanability

### Conclusion Rules
- End with a forward-looking statement: where does this lead, what's next?
- Leave the reader with something to think about or act on — not just a recap
- The conclusion should feel like an opening, not a closing
- End with an open question or invitation that encourages comments

### Formatting Rules
- Markdown throughout: `#` for title, `##` for section headers
- Line breaks between paragraphs — not within them. Sentences within a paragraph flow back-to-back as continuous prose with no line returns.
- No emojis
- Include 3–5 relevant hashtags at the end

### Article Standards
- Target word count: 1,000–1,500 words
- Maximum 3 pages of narrative content
- One core idea — not three, not five. One.
- Every paragraph has a topic sentence
- Every sentence has a purpose — less is more
- Support claims with specifics
- Writing creates a context in which readers can think — not just a list of takeaways

---

## Checklists

### Pre-Delivery Checklist
Run this internally before presenting any draft. Do not present until all items pass.

- [ ] Does the title spark curiosity without overpromising?
- [ ] Does the subtitle align with the title as one thought — thesis compressed to one line?
- [ ] Does the opening hook? No slow start, no preamble?
- [ ] Is there ONE core idea, and does every paragraph serve it?
- [ ] Does every paragraph pass the "So what?" test?
- [ ] Are claims supported with specifics (metrics, examples, models)?
- [ ] Does the conclusion open a door rather than close one?
- [ ] Is the word count between 1,000–1,500 words?
- [ ] Would a senior tech leader find this valuable and share it?
- [ ] Does the article contain any banned phrases from the blacklist?
- [ ] Does the emotional arc match what was specified (or feel deliberate if none was)?

### Voice Check Pass
Run this after the Pre-Delivery Checklist. Do not present the draft until this passes.

1. Read the full draft and ask: "Does any part of this sound like it could have been written by someone other than the author in the Author Profile?"
2. Specifically check: openings, transitions, the conclusion, and any moment where you defaulted to a generic framing.
3. If any passage fails:
   - Flag it as: **[Voice check: this passage sounds generic]**
   - Immediately below, provide a concrete rewrite that better matches the Author Profile (direct, strategic, intellectually curious, no hedging, no clichés)
4. Resolve all flagged passages — either rewrite them or explicitly note why a departure is intentional — before presenting the draft.

Do not skip this step. A draft that passes the Pre-Delivery Checklist but fails the Voice Check is not ready.
