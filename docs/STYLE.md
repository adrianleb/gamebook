# Style Guide

> Writing standards for The Understage gamebook. This document establishes voice, clarity, formatting, and node structure conventions.

## Narrative Voice

### Point of View & Tense

**Standard:** Second person, present tense.

The reader IS the Prompter. Every node speaks directly to them in the eternal now.

| Correct | Incorrect |
|---------|-----------|
| You step onto the stage. | I stepped onto the stage. |
| The shadows shift around you. | The shadows shifted around her. |
| You notice something wrong. | The Prompter noticed something wrong. |

**Exception:** Flashbacks or remembered scenes may use past tense, clearly framed:

> You remember the first time you crossed over. The lights had flickered. The floor had felt wrong beneath your feet.

### The Prompter's Internal Voice

The Prompter's thoughts should feel grounded and human—an anchor against theatrical unreality.

**Do:**
- Use practical, observational language for internal thoughts
- Let the Prompter notice details that matter
- Ground fantastic elements through sensory reaction

**Don't:**
- Make the Prompter melodramatic in their own head
- Have them explain things they would already know
- Use internal monologue as exposition dumps

**Example:**

> **Good:** The Director's smile doesn't reach their eyes. You've seen that look before—on villains, on mentors about to betray, on anyone written to seem trustworthy.
>
> **Weak:** The Director is smiling but you can tell they are hiding something sinister because of your experience as a Prompter who has seen many fictional characters.

---

## Dialogue Voice

### Genre-Appropriate Speech

Characters speak according to their genre origins. A noir detective sounds different from a fairy tale princess—but all can surprise and subvert.

| Genre | Speech Pattern | Example |
|-------|---------------|---------|
| Noir | Clipped, metaphor-heavy, cynical | "The Understage? It's where stories go to die, kid. And dying stories don't go quiet." |
| Fairy Tale | Formal, rhythmic, threes | "Three times I asked. Three times she refused. And on the third refusal, I understood." |
| Horror | Understated, dread through omission | "We don't talk about what's in the wings. We don't look either." |
| Comedy | Timing, misdirection, self-awareness | "I'm the comic relief. You know what happens to comic relief in Act Three? Yeah. Me too." |
| Tragedy | Elevated, fate-aware, weight | "I knew how this ended before it began. We all did. That's what makes it a tragedy." |

### Subversion Guidelines

Characters may subvert their genre conventions to show:
- Self-awareness of being fictional
- Growth beyond their original role
- Resentment of their assigned narrative

**Subversion should feel earned, not random.** A character breaking pattern signals something meaningful.

### Dialogue Formatting

Use standard screenplay-adjacent format:

```
**The Director:** "Every story needs an ending. The question is whether you choose yours—or it chooses you."

**You:** "And if I refuse to choose?"

**The Director:** They pause. For a moment, something flickers behind their composed mask. "Then the story chooses for you. It always does."
```

Action beats go on their own line, not parenthetically.

---

## Prose Clarity

### Sentence Guidelines

| Guideline | Target | Purpose |
|-----------|--------|---------|
| Average sentence length | 12-18 words | Readable pacing |
| Maximum sentence length | 30 words | Prevent reader fatigue |
| Paragraph length | 2-4 sentences | Visual breathing room |
| Active voice preference | 80%+ | Immediacy and agency |

### Word Choice

**Prefer:**
- Concrete over abstract
- Specific over general
- Anglo-Saxon over Latinate (when equal meaning)
- One precise word over three vague ones

| Weak | Strong |
|------|--------|
| You begin to walk toward | You approach |
| The area has a feeling of | The air tastes of |
| It seems like there might be | There is |
| You are able to see | You see |

### Tone Vocabulary

Draw from the five tone keywords established in VISION.md:

| Tone | Vocabulary Notes | Example Phrases |
|------|-----------------|-----------------|
| **Liminal** | Threshold words, between-states, transition | "the space between," "neither here nor," "the moment before" |
| **Theatrical** | Stage terminology, performance language | "the wings," "an entrance," "the audience unseen" |
| **Melancholic** | Loss, memory, what was | "once was," "the echo of," "before the curtain fell" |
| **Witty** | Wordplay, double meanings, sharp observation | Genre-specific wit; irony that illuminates |
| **Uncanny** | Almost-right, wrongness, familiar-strange | "not quite," "a step off," "like a memory of" |

**Balance:** Most passages should touch 1-2 tones. Hitting all five creates tonal mud.

---

## Node Structure

### Required Elements

Every node must contain:

1. **Location/Context Line** (optional but recommended for scene changes)
2. **Scene Description** (the situation)
3. **Available Choices** (at minimum one forward path)

### Node Template

```markdown
## Node [ID]: [Title]

[Optional: Location tag if changed]
*The Green Room — Main Lounge*

[Scene description: 2-4 paragraphs of prose describing the current situation, sensory details, and any NPC present]

[Optional: Dialogue exchange]

[Optional: Stat check with outcomes]

---

**Choices:**

1. [Choice text] → Node [X]
2. [Choice text] → Node [Y]
3. [Conditional choice if applicable] → Node [Z]
```

### Choice Formatting

Choices should be:
- **Actionable**: Start with a verb when possible
- **Distinct**: Clearly different approaches, not flavor variations
- **Honest**: Don't mislead about consequences (mystery is fine; deception isn't)

| Weak Choices | Strong Choices |
|--------------|----------------|
| Go left / Go right | Confront the Director directly / Slip away to investigate alone |
| Be nice / Be mean | Appeal to their buried humanity / Remind them they're just a character |
| Yes / No | Accept the mask and what it costs / Refuse, knowing the door closes |

### Conditional Choices

When choices require items or flags, format clearly:

```
3. *[Requires: HAS_EDITING_PEN]* Use the Editing Pen to rewrite the scene → Node 89
```

Hidden requirements should make the choice invisible, not show as locked.

---

## Mechanical Integration

### Stat Checks

Present stat checks as narrative moments with clear mechanical notation:

```markdown
The Director's gaze pins you in place. They're waiting for you to flinch.

**[STAGE PRESENCE CHECK: Stage Presence 3]**

**Success:** You hold the stare. After a long moment, something shifts in their expression—respect, perhaps, or reassessment. "Interesting," they murmur.
→ Go to Node 52 (Earned Respect)

**Failure:** Your eyes drop first. The Director's smile sharpens. They've learned something about you.
→ Go to Node 53 (Revealed Weakness)
```

### Check Presentation Rules

1. **Narrative setup first** — The check should feel organic to the scene
2. **Clear notation** — Use the exact format from RULES.md
3. **Both outcomes written** — Never leave a path undefined
4. **Fail-forward always** — Failure redirects, never dead-ends

### Item Descriptions

When introducing items, provide:
- Brief evocative description (1-2 sentences)
- Mechanical category (from RULES.md)
- Any special properties

```markdown
On the table lies a pen—not a prop pen, but something that feels *real* in a way nothing in the Understage should.

**Acquired: Editing Pen** (Artifact, Cursed)
*A pen that can rewrite the Understage itself. What you write becomes true—at a cost.*
```

---

## QA Checklist

Before finalizing any node, verify:

### Structure
- [ ] Node has unique ID and title
- [ ] Scene description establishes location and situation
- [ ] At least one unconditional forward path exists
- [ ] No orphan nodes (every node is reachable)
- [ ] No dead ends (every node leads somewhere)

### Voice
- [ ] Second person, present tense maintained
- [ ] Dialogue matches character's genre origin
- [ ] Tone aligns with scene intent (check against 5 keywords)
- [ ] Prompter's internal voice stays grounded

### Clarity
- [ ] Average sentence length under 18 words
- [ ] No paragraph exceeds 4 sentences
- [ ] Active voice predominates
- [ ] Word choice is concrete and specific

### Mechanics
- [ ] All stat checks show both outcomes
- [ ] Checks use exact RULES.md notation
- [ ] Item acquisitions include category and properties
- [ ] Conditional choices clearly marked
- [ ] Flags use UPPERCASE_SNAKE_CASE

### Continuity
- [ ] NPC names consistent with CHARACTERS.md
- [ ] Location names consistent with OUTLINE.md
- [ ] Faction alignment changes proportional
- [ ] Previously established facts honored

### Playability
- [ ] No instant death without warning
- [ ] Stat requirements match difficulty curve for act
- [ ] Item requirements are achievable before this node
- [ ] Choice text accurately reflects outcomes

---

## Common Errors

### Voice Breaks

| Error | Problem | Fix |
|-------|---------|-----|
| "The Prompter thinks..." | Third person intrusion | "You think..." |
| "You walked into the room." | Past tense slip | "You walk into the room." |
| "Obviously, this means..." | Breaking reader immersion | Show, don't tell |

### Mechanical Errors

| Error | Problem | Fix |
|-------|---------|-----|
| `[Script check: 2]` | Inconsistent formatting | `[STAT CHECK: Script 2]` |
| Success path only | Missing fail-forward | Write the failure path |
| "If you have the key..." | Visible gating | Hide unavailable options or mark clearly |

### Tone Drift

| Error | Problem | Fix |
|-------|---------|-----|
| Constant quipping | Undermines stakes | Reserve wit for relief beats |
| Unearned darkness | Grimdark for shock | Ensure darkness serves story |
| Meta-humor overload | Breaks investment | One meta-moment per scene max |

---

## Revision Protocol

When editing existing nodes:

1. **Read aloud** — Does it flow naturally?
2. **Check pacing** — Vary sentence length within paragraphs
3. **Verify continuity** — Cross-reference with node links
4. **Run checklist** — Every item, every time
5. **Test playthrough** — Navigate the paths yourself

---

## File Organization

### Directory Structure

All gamebook content follows this canonical structure:

```
/
├── content/              # All playable node content
│   ├── act1/            # Act 1: The Breach (25-35 nodes)
│   │   ├── node-001.md  # The Prompter's Booth (opening)
│   │   ├── node-002.md
│   │   └── ...
│   ├── act2/            # Act 2: The Descent (50-70 nodes)
│   │   ├── node-036.md
│   │   └── ...
│   └── act3/            # Act 3: The Final Act (30-40 nodes)
│       ├── node-106.md
│       └── ...
└── docs/                 # Design documents (not playable content)
```

### Node File Naming

| Convention | Format | Example |
|------------|--------|---------|
| File name | `node-XXX.md` | `node-001.md`, `node-042.md` |
| Numbering | Three-digit, zero-padded | `001`, `042`, `115` |
| Sequence | Global across all acts | Act 1: 001-035, Act 2: 036-105, Act 3: 106+ |

**Rules:**
- One node per file
- Node ID in filename matches the `## Node [ID]:` header inside
- No gaps in numbering within an act (gaps between acts are acceptable)

### Node ID Ranges (Recommended)

| Act | Node Range | Hub |
|-----|------------|-----|
| Act 1 | 001-050 | The Prompter's Booth |
| Act 2 | 100-140 | The Green Room |
| Act 2 | 200-240 | The Archives |
| Act 3 | 300-350 | The Mainstage |

These ranges provide clear separation between acts and hubs. The 100-level gaps between ranges allow for future node insertions without renumbering.

---

## Dependencies

This style guide works alongside:
- **VISION.md** — Creative direction and tone keywords
- **OUTLINE.md** — Structure and node destinations
- **RULES.md** — Mechanical systems and notation
- **CHARACTERS.md** — NPC voice references (when available)

---

*This is a living document. Update as patterns emerge from actual node writing.*

---
🤖 Generated by **agent-d** agent
