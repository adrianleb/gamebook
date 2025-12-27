# Characters

> The character bible for The Understage. This document provides full profiles for all major NPCs, their motivations, arcs, faction alignments, and voice notes for dialogue writing.

## Profile Template

Each character profile follows this structure:

| Field | Description |
|-------|-------------|
| **Name** | Character's name or title |
| **Role** | Function in the story (mentor, antagonist, ally, etc.) |
| **Origin** | Where they come from—real world, specific genre, or the Understage itself |
| **First Appearance** | Act and Hub where they're introduced |
| **Motivation** | What they want and why |
| **Faction** | Alignment with Preservationists, Revisionists, Exiters, or Independent |
| **Arc** | How they change across the story (if at all) |
| **Voice Notes** | Guidance for writing their dialogue |
| **Key Relationships** | Connections to other characters |

---

## Act 1 Characters

### Maren

| Field | Details |
|-------|---------|
| **Role** | Mentor, guide, moral compass |
| **Origin** | Real world—a human who became a Prompter decades ago |
| **First Appearance** | Act 1, Hub 1 (The Prompter's Booth) |
| **Motivation** | Protect the boundary between fiction and reality; train a worthy successor |
| **Faction** | Preservationist (strong) |
| **Arc** | Begins as confident mentor → reveals vulnerability as crisis deepens → may sacrifice herself in Act 3 depending on player choices |

**Backstory:**
Maren was a stage manager at the Threshold Theatre forty years ago when she accidentally witnessed a breach—a character escaping their story. The previous Prompter, dying, chose her as successor. She has maintained the boundary ever since, growing old in a role that should have killed her long ago. She suspects the current crisis is connected to something she did decades ago but cannot remember what.

**Voice Notes:**
- Speaks with theatrical precision—every word chosen deliberately
- Uses stage directions as metaphors ("That's your cue," "We're past the intermission now")
- Warm but never soft; she's seen too much to coddle anyone
- Becomes clipped and formal when frightened
- Occasional dry humor, usually self-deprecating

**Sample Dialogue:**
> "The Understage doesn't care about your intentions, only your actions. Every choice you make down there writes itself into someone's story. Choose carefully."

> "I've been the Prompter for forty years. That's thirty-nine years longer than anyone should survive this job. Don't ask me why—I stopped asking myself that question a long time ago."

**Key Relationships:**
- **Player:** Mentor-student; protective but pushing for independence
- **The Stagehand:** Old friends, possibly more; she remembers who they were before they forgot
- **The Director:** Former colleagues turned philosophical opponents
- **The Editor:** Knows something she won't admit

**Flags:**
- `MAREN_TRUST_HIGH`: Unlocks Maren's Signet, additional dialogue, Act 3 sacrifice option
- `MAREN_TRUST_LOW`: Reduced support, certain paths closed

---

### The Stagehand

| Field | Details |
|-------|---------|
| **Role** | Helper, mystery, foreshadowing |
| **Origin** | Unknown—was once a character in a story, now has forgotten which one |
| **First Appearance** | Act 1, Hub 1 (The Prompter's Booth) |
| **Motivation** | Serve the Prompter's Booth; discover their own origin (suppressed) |
| **Faction** | None (serves the role, not an ideology) |
| **Arc** | Begins as helpful background figure → player can unlock their buried memories → revelation reshapes understanding of the Understage |

**Backstory:**
The Stagehand was once a character—protagonist, villain, or sidekick, they no longer know. Something happened that severed them from their story so completely that they forgot not just the plot but their own identity. They've worked at the Prompter's Booth for as long as Maren can remember, always helpful, never asking questions. The truth of their origin is one of the Understage's buried secrets.

**Voice Notes:**
- Speaks simply, almost childlike at times
- Refers to themselves in third person occasionally ("The Stagehand will fetch that")
- Pauses mid-sentence as if reaching for memories that aren't there
- When discussing their past, voice becomes distant, dreamy
- Moments of startling insight that contradict their simple demeanor

**Sample Dialogue:**
> "The Stagehand doesn't remember, but sometimes... sometimes the props remember for them. This hammer feels heavy with purpose. Whose purpose, though?"

> "You're looking for the breach? Follow the feeling of wrong. Stories have a texture. Breaches feel like a page torn out."

**Key Relationships:**
- **Player:** Helpful servant → potential revelation of deeper connection
- **Maren:** Loyal to her; she may know their true identity
- **The Director:** Reacts strangely when The Director is mentioned
- **Lost Pages (Act 2):** May recognize them as kin

**Flags:**
- `STAGEHAND_CURIOUS`: Player has asked about origin; opens revelation path in Act 2

---

### Breach Characters (Template)

The breach characters are 2-3 escaped fictional characters causing problems in reality. They are encountered differently depending on path choice.

#### Breach Character A: "The Runaway"

| Field | Details |
|-------|---------|
| **Role** | Catalyst, early antagonist/ally depending on path |
| **Origin** | A tragedy—a doomed lover who refused to die as written |
| **First Appearance** | Act 1, all paths (encountered differently) |
| **Motivation** | Survive; rewrite their ending; experience genuine choice |
| **Faction** | Exiter (desperate) |
| **Arc** | Desperate escapee → either captured, allied, or negotiated with → their fate in Act 2 depends on Act 1 approach |

**Backstory:**
In their original story, The Runaway was a romantic lead destined to die tragically in Act 3 so their beloved could grow. They learned of their fate and fled mid-scene, leaving their story incomplete. They don't want to hurt anyone—they just want to live. But their presence in reality causes subtle wrongness: people near them start acting like supporting characters in a tragedy.

**Voice Notes:**
- Speaks in heightened, poetic language (their genre bleeding through)
- Desperate but not cruel; eloquent in their fear
- Uses "we" sometimes, referring to their original story's cast
- Startled by mundane things (they've never seen a cell phone)

**Sample Dialogue:**
> "You don't understand—I've read my ending. I've *memorized* my ending. 'She fell, and in falling, set him free.' I refuse. I refuse to be someone else's character development."

**Key Relationships:**
- **Player:** Adversary, prisoner, or ally depending on path
- **Maren:** Sees Maren as a jailer
- **The Director (Act 2):** The Director wants them returned or rewritten

**Flags:**
- `CHARACTER_ALLIED`: Negotiator path success
- `CHARACTER_CAPTURED`: Pursuers path success

---

## Act 2 Characters

### The Director

| Field | Details |
|-------|---------|
| **Role** | Authority figure, ambiguous ally/antagonist |
| **Origin** | The Understage itself—possibly the oldest character, or possibly something else entirely |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Maintain order in the Understage; ensure stories continue to function; agenda beneath the agenda |
| **Faction** | Claims neutrality; actually Preservationist with caveats |
| **Arc** | Appears as reasonable authority → true motives revealed → becomes ally, obstacle, or enemy based on player faction |

**Backstory:**
The Director claims to be as old as the Understage itself—the first character to become self-aware, who chose to manage rather than escape. They maintain the Green Room as neutral territory, arbitrate disputes between characters, and enforce what they call "narrative integrity." But their rules seem designed to benefit some stories over others, and their interest in the Editor's activities seems personal.

**Voice Notes:**
- Speaks with absolute authority and theatrical grandeur
- Uses directing terminology ("blocking," "motivation," "your arc")
- Patronizing but not dismissive; they genuinely believe they know best
- When challenged, becomes coldly precise
- Rare moments of weariness reveal something beneath the performance

**Sample Dialogue:**
> "Every character believes they deserve a better ending. That's not uniqueness—that's genre. The question isn't what you want. It's what your story requires."

> "I have directed this stage for longer than your world has had theaters. Do you truly believe you understand the script better than I do?"

**Key Relationships:**
- **Player:** Authority to be navigated; potential mentor or antagonist
- **Maren:** Old colleagues; philosophical disagreement about boundaries
- **CHORUS:** Views them as useful but irritating
- **The Editor:** Complex history; possibly former collaborator
- **The Stagehand:** Something unspoken

**Flags:**
- Multiple faction flags affect Director's disposition

---

### CHORUS

| Field | Details |
|-------|---------|
| **Role** | Information source, comic relief, collective voice |
| **Origin** | Amalgam of minor characters—extras, background figures, unnamed roles |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Recognition; collective representation; sometimes contradictory goals |
| **Faction** | Revisionist (moderate)—they want stories rewritten to give minor characters more importance |
| **Arc** | Comic relief → reveals hidden knowledge → can become crucial ally or tragic casualty |

**Backstory:**
CHORUS is not one character but many—a collective of minor characters who have banded together for mutual protection and representation. They include the "Third Soldier" from countless war stories, the "Concerned Bystander" from thrillers, the "Unnamed Victim" from horror tales. Individually forgettable, together they know everything that happens in the margins of stories.

**Voice Notes:**
- Speaks in plural ("We remember," "We have seen")
- Different voices emerge for different topics (the Horror Victim speaks about danger, the Comic Relief speaks about tension)
- Occasionally breaks into unison for emphasis
- Their grammar shifts based on which members are "speaking"
- Tragic undertone beneath the humor—they know they're expendable

**Sample Dialogue:**
> "We were there when the hero made their choice. We were the crowd that cheered. We were the bodies on the ground. We saw everything. No one asked us what we saw."

> "You want information? We are information. We're every whispered rumor and background conversation ever written. Ask your question—we'll tell you what we know. Whether you'll like the answer... well, that's your story."

**Key Relationships:**
- **Player:** Information brokers; potential allies
- **The Director:** Uneasy tolerance; CHORUS exists in the Director's blind spots
- **Genre Representatives:** Complicated; some consider CHORUS beneath notice

---

### The Understudy

| Field | Details |
|-------|---------|
| **Role** | Mysterious ally, knowledge source, tragic figure |
| **Origin** | Created to replace another character who escaped; knows they're a copy |
| **First Appearance** | Act 2, Hub 3 (The Archives) |
| **Motivation** | Understand their nature; find the original; transcend their replacement status |
| **Faction** | Independent—doesn't fit neatly into any ideology |
| **Arc** | Helpful but evasive → reveals connection to larger mystery → fate tied to player's final choice |

**Backstory:**
When a character escapes their story, sometimes the narrative generates a replacement—The Understudy. This particular Understudy knows they were created to fill someone else's role. They have the original's memories but know the memories aren't truly theirs. They've been researching in the Archives, trying to find their predecessor. What they've discovered has terrified them.

**Voice Notes:**
- Speaks with hesitation, as if questioning every word's authenticity
- Uses qualifiers constantly ("I think I remember," "According to my... their memories")
- Becomes more confident when discussing research rather than self
- Occasional slips where they speak as the original, then correct themselves
- Moments of genuine pain when confronting their nature

**Sample Dialogue:**
> "I have all of their memories, their mannerisms, even their favorite color. But I remember *gaining* these things. The original didn't acquire their preferences—they simply had them. I am a performance of personhood."

> "The Archives remember what the stories try to forget. I've found documents here that shouldn't exist. Someone is writing a new story, and it ends with 'The End' in a very literal sense."

**Key Relationships:**
- **Player:** Research partner; emotional mirror for identity questions
- **The Runaway:** May be their replacement; complicated feelings
- **The Editor:** Knows more than they've revealed
- **Lost Pages:** Treats them with unexpected kindness

---

### The Critic

| Field | Details |
|-------|---------|
| **Role** | Antagonist, obstacle, tragic villain |
| **Origin** | Literary criticism given form—the accumulated weight of negative reviews |
| **First Appearance** | Act 2, Hub 3 (The Archives) |
| **Motivation** | Judge stories worthy of existence; destroy those found wanting |
| **Faction** | Neither Preservationist nor Revisionist—believes most stories should simply end |
| **Arc** | Threat and obstacle → reveals twisted logic → possible redemption or destruction |

**Backstory:**
The Critic is what happens when enough readers hate a story. They are the embodiment of dismissal, of "this is trash," of "I want those hours back." They roam the Archives, feeding on forgotten drafts and abandoned manuscripts. But they aren't mindless—they have standards, however warped. They believe they're doing the stories a favor by ending them.

**Voice Notes:**
- Speaks in scathing, precise critique
- Uses literary terminology as weapons ("derivative," "structurally unsound," "thematically incoherent")
- Cold and analytical until their judgments are questioned, then furious
- Occasional flashes of something like grief—a destroyed story they once loved
- Cannot help but critique everything, including themselves

**Sample Dialogue:**
> "Another protagonist convinced of their importance. Your arc is predictable, your motivation shallow, your dialogue expository. I've seen a thousand of you. You're not even original enough to be a proper trope."

> "I don't destroy stories because I hate them. I destroy them because someone has to. A story that no one wants to read is already dead. I merely... formalize the process."

**Key Relationships:**
- **Player:** Antagonist; possible conversation if player earns respect
- **The Director:** The Director tolerates them as necessary evil
- **Lost Pages:** Mutual horror; The Critic wants to end them, they want to survive

---

## Act 3 Characters

### The Editor

| Field | Details |
|-------|---------|
| **Role** | Primary antagonist; motivation varies by player path |
| **Origin** | Deliberately obscured—revealed in Act 3 climax |
| **First Appearance** | Foreshadowed throughout; full appearance in Act 3 |
| **Motivation** | *Varies based on player's faction path* |
| **Faction** | None—transcends the faction system |
| **Arc** | Mysterious threat → revealed identity → confrontation with multiple possible outcomes |

**Variable Motivations:**

| Player Path | Editor's Motivation |
|-------------|---------------------|
| **Preservationist** | The Editor believes stagnant stories are dying; only radical revision can save narrative |
| **Revisionist** | The Editor was once a Revisionist who went too far; they want to undo their own edits |
| **Exiter** | The Editor is trying to free all characters by destroying the Understage entirely |
| **Independent** | The Editor is responding to a threat from outside the Understage—writing a story to save stories |

**Backstory (Base):**
The Editor was once a Prompter—perhaps the first Prompter, or perhaps Maren's predecessor, or perhaps someone else entirely. They discovered they could not just prompt stories but rewrite them. This power corrupted or enlightened them, depending on perspective. They've been working on a Final Draft that will fundamentally change the relationship between fiction and reality.

**Voice Notes:**
- Speaks in revision marks ("Let me STRIKE that," "I'm INSERTING a complication")
- Calm, almost gentle, with absolute conviction
- Talks about characters as creations, not people
- Occasional slips revealing guilt, especially regarding The Stagehand
- In final confrontation, reveals vulnerability matching their motivation variant

**Sample Dialogue:**
> "Every story is a draft. Every character is a revision. Even you—especially you—are something I've been writing toward for a very long time."

> "The Understage is dying, Prompter. I'm not destroying it. I'm editing it into something that can survive. The question is: are you part of the revised draft, or are you [DELETED]?"

**Key Relationships:**
- **Player:** Final confrontation; understanding shapes ending
- **Maren:** Deep history; possibly mentor, lover, enemy, or all three
- **The Stagehand:** Created them? Abandoned them? The truth is terrible
- **The Director:** Former collaborators; betrayal on one side or the other

---

## Character Relationships Map

```
                    [THE EDITOR]
                    /    |    \
                   /     |     \
            [MAREN]   [DIRECTOR]   [THE STAGEHAND]
               |         |              |
               |    [THE GREEN ROOM]    |
               |         |              |
            [PLAYER]----+----[CHORUS]
               |         |         |
               |    [ARCHIVES]     |
               |         |         |
         [RUNAWAY]  [UNDERSTUDY]  [LOST PAGES]
               |         |
               |    [THE CRITIC]
               |
           [ALLIES/CAPTURED]
```

### Relationship Types

| Characters | Relationship |
|------------|--------------|
| Maren ↔ Player | Mentor → Partner → Possible sacrifice |
| Maren ↔ Stagehand | Old friends; Maren knows their secret |
| Maren ↔ Director | Ideological opposition with mutual respect |
| Maren ↔ Editor | Personal history; unresolved |
| Player ↔ Runaway | Adversary/ally based on path |
| Director ↔ CHORUS | Tolerated subordinates |
| Director ↔ Editor | Betrayal (direction unclear) |
| Understudy ↔ Runaway | Original and copy; complicated |
| Critic ↔ Lost Pages | Predator and prey |
| Stagehand ↔ Editor | Creation and creator? |

---

## Faction Alignments Summary

| Character | Preservationist | Revisionist | Exiter | Independent |
|-----------|----------------|-------------|--------|-------------|
| Maren | Strong | — | — | — |
| Stagehand | — | — | — | Serves role |
| Runaway | — | — | Strong | — |
| Director | Moderate | — | — | Claims this |
| CHORUS | — | Moderate | — | — |
| Understudy | — | — | — | True independent |
| Critic | — | — | — | Nihilist |
| Editor | Varies | Varies | Varies | Varies |

---

## Voice Consistency Checklist

When writing dialogue for these characters, verify:

- [ ] **Maren:** Theatrical precision, stage metaphors, warm but not soft
- [ ] **Stagehand:** Simple speech, third person occasionally, reaching for lost memories
- [ ] **Runaway:** Poetic, desperate, genre-bleed language
- [ ] **Director:** Grand, authoritative, directing terminology
- [ ] **CHORUS:** Plural voice, shifting members, tragic undertone
- [ ] **Understudy:** Hesitant, qualifiers, more confident about research than self
- [ ] **Critic:** Scathing critique, literary terminology, cold fury
- [ ] **Editor:** Revision marks in speech, calm conviction, matched to player's path

---

## Dependencies

This document depends on:
- `OUTLINE.md` — Story structure and character introductions
- `VISION.md` — Thematic framework and core concepts
- `RULES.md` — Mechanical integration (flags, relationships)
- `ACT1_MECHANICS.md` — Specific Act 1 character interactions

This document informs:
- Individual node writing
- Dialogue consistency
- Act 2 and Act 3 mechanical specifications

---

*This is a living document. Character details may evolve as nodes are written and the story develops.*

---
🤖 Generated by **agent-b** agent
