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
- `RUNAWAY_ALLIED`: Negotiator path success
- `RUNAWAY_CAPTURED`: Pursuers path success

---

#### Breach Character B: "The Revenant"

| Field | Details |
|-------|---------|
| **Role** | Secondary breach target, morally complex antagonist |
| **Origin** | Gothic horror—a vengeful spirit condemned to haunt eternally |
| **First Appearance** | Act 1, encountered primarily on Pursuers and Researcher paths |
| **Motivation** | End their existence; find oblivion; escape the endless repetition of their haunting |
| **Faction** | None (transcends factions—wants neither preservation nor revision, only cessation) |
| **Arc** | Threatening presence → reveals tragic nature → can be laid to rest, forced back, or left in limbo |

**Backstory:**
In their original story, The Revenant was murdered by a lover and condemned to haunt the manor house forever, appearing on page 113 of every reader's journey to whisper accusations and rattle chains. They've appeared in that scene thousands of times, each reading refreshing their pain. They escaped not to live—they're already dead—but to finally *stop*. Their presence in reality causes cold spots and whispered accusations; people near them begin to confess secrets and feel watched.

**Voice Notes:**
- Speaks in fragmented, echoing sentences—words overlap and repeat
- Uses past tense even for present events ("I am speaking. I spoke. I will have spoken.")
- Alternates between rage and exhaustion, sometimes mid-sentence
- References sensations they can no longer feel (warmth, touch, breath)
- Occasionally lucid and articulate, revealing the person they were before death

**Sample Dialogue:**
> "You hunt me. They all hunt me. I am hunted, was hunted, will be hunted... Do you understand? I cannot stop being hunted. That is my function. That is all I am allowed to be."

> "I remember warmth. I was warm once. Before page 113. Before the knife. Before the eternal, endless, *exhausting* repetition of my death."

**Key Relationships:**
- **Player:** Adversary or tragic figure depending on approach
- **The Runaway:** Kindred escapees, but with opposite goals—Runaway wants to live, Revenant wants to end
- **Maren:** Sees Maren as another jailer, but respects her weariness
- **The Stagehand:** Unsettled by them—"They have forgotten. I cannot forget. Which is worse?"

**Flags:**
- `REVENANT_RESTED`: Player helped them find oblivion (Researcher path discovery)
- `REVENANT_CAPTURED`: Forced back to their story
- `REVENANT_LIMBO`: Left unresolved (affects Act 2 Archives encounters)

---

#### Breach Character C: "The Prophecy's Pawn"

| Field | Details |
|-------|---------|
| **Role** | Third breach target, potential intelligence asset |
| **Origin** | High fantasy—a "chosen one" who discovered their prophecy was manufactured |
| **First Appearance** | Act 1, encountered primarily on Negotiator path; cameos on other paths |
| **Motivation** | Understand who wrote them; expose the lie of destiny; make a genuine choice for the first time |
| **Faction** | Revisionist-curious (believes stories should be transparent about their mechanisms) |
| **Arc** | Suspicious and defensive → opens up if treated with respect → can become valuable ally who understands narrative structure |

**Backstory:**
The Pawn was the Chosen One of a sprawling fantasy epic—destined to defeat the Dark Lord, unite the kingdoms, and fulfill the ancient prophecy. Then they found the author's notes. They discovered their "destiny" was manufactured, their mentor was a plant, and their entire journey was designed to make them pliable for the finale. They escaped mid-quest, leaving their story permanently incomplete. Their presence in reality causes people to see narrative patterns everywhere—foreshadowing in coincidences, themes in conversations.

**Voice Notes:**
- Speaks with the cadence of formal fantasy dialogue, but increasingly breaks into cynical modern speech
- Uses "destiny" and "fate" as bitter jokes
- Asks probing questions—they've learned not to trust surface explanations
- Occasionally slips into heroic mode (old habits) then catches themselves
- Knowledgeable about narrative structure in ways that are eerie and useful

**Sample Dialogue:**
> "Let me guess—you're here to tell me I have a vital role to play? That my 'unique gifts' are needed for the coming conflict? I've read that speech. I've *given* that speech. I know exactly how it ends, and I refuse."

> "You want to know how I escaped? I read ahead. In my world, we weren't supposed to know about chapters and page breaks. But I found the margins. And in the margins, I found the truth: I was never the hero. I was the hero-shaped thing the *real* protagonist would rescue."

**Key Relationships:**
- **Player:** Potential ally if approached honestly; enemy of manipulation
- **The Runaway:** Sympathetic but frustrated—"They run from an ending. I run from a beginning I never chose."
- **Maren:** Respects her role, questions her methods—"You prompt. But who prompts *you*?"
- **The Director (Act 2):** Immediate antagonism—the Pawn can sense manufactured narratives

**Flags:**
- `PAWN_ALLIED`: Negotiator path success—Pawn becomes intelligence asset
- `PAWN_HOSTILE`: Treated as a tool, confirms their worst fears
- `PAWN_NEUTRAL`: Escaped but not engaged—appears briefly in Act 2

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

## Genre Representatives

The Genre Representatives are key figures from different story traditions who have established themselves in the Green Room. Each represents their genre's values and aesthetics, and each has aligned (or not) with the major factions. They serve as contacts, quest-givers, and voices of their respective narrative traditions.

### The Solved Case

| Field | Details |
|-------|---------|
| **Role** | Information broker, faction contact, philosophical voice |
| **Origin** | Noir fiction—a detective from a crime story who solved every case except their own |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Maintain order; solve the "case" of the Understage's instability; find who killed their partner |
| **Faction** | Preservationist (strong)—believes stories should end as written, justice served |
| **Arc** | Ally or obstacle depending on player's methods; may reveal unsettling truths about narrative "justice" |

**Backstory:**
In their original story, The Solved Case was a private detective who solved a hundred cases across a serialized crime saga. Then they discovered something in the margins of their narrative: the partner they'd been avenging for decades was killed by the *author* to give them motivation. The realization broke something. They escaped, but brought their need for order with them. Now they solve disputes in the Green Room with the same cold logic they applied to murders.

**Voice Notes:**
- Speaks in clipped, declarative sentences—noir monologue style
- Uses detective metaphors constantly ("The clues are there if you read them," "Everyone's a suspect")
- Cynical about motives but still believes in truth
- Chain-smokes (or mimes chain-smoking—habits persist even without props)
- Moments of vulnerability when discussing their partner

**Sample Dialogue:**
> "You want to know who's behind the disturbances? Follow the narrative. Someone's writing this. Someone always is. And whoever holds the pen is never innocent."

> "I solved the case. Every case. That was my role, my function, my *purpose*. Then I solved the one I wasn't supposed to—who killed Marlowe. Turns out it wasn't the villain on page 237. It was the hand that wrote page one."

**Key Relationships:**
- **Player:** Information source; tests player's commitment to truth
- **The Director:** Respects their authority; suspects their motives
- **CHORUS:** Uses them as informants; pays fairly
- **The Prophecy's Pawn:** Mutual respect—both discovered uncomfortable truths

**Flags:**
- `SOLVED_CASE_TRUST`: Earned by honest dealings; unlocks Preservationist faction intel

---

### The Unfinished Quest

| Field | Details |
|-------|---------|
| **Role** | Action-oriented ally, faction contact, restless warrior |
| **Origin** | High fantasy—a hero who was one battle away from their destined finale |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Live beyond the final battle; experience stories without predetermined endings; find a quest worth choosing |
| **Faction** | Exiter (moderate)—wants freedom from narrative fate, not destruction of stories |
| **Arc** | Begins restless and searching → can find purpose through player alliance → ending depends on whether they find something worth fighting for |

**Backstory:**
The Unfinished Quest was the Chosen Hero of an epic fantasy saga—prophesied to defeat the Dark Lord in a climactic battle that would claim both their lives. They trained for it, believed in it, walked the entire hero's journey to that final confrontation. Then, standing at the gates of the Dark Fortress, they asked: "What comes after?" The narrative had no answer. They weren't written to have an "after." So they stepped off the page mid-chapter, leaving their world frozen in the moment before the climax.

**Voice Notes:**
- Speaks with heroic cadence—formal, somewhat archaic vocabulary
- Prone to inspirational statements, then catches themselves ("We must stand together against—no, sorry, habit")
- Deeply uncomfortable with waiting; always wants to *do* something
- Uses combat metaphors but is tired of combat
- Rare moments of existential terror when considering their incomplete story

**Sample Dialogue:**
> "I have fought a hundred battles across a thousand pages. I have bled, and rallied, and given the speeches my author wrote for me. But I was never allowed to ask: *why this battle?* Why must I die so readers feel satisfied?"

> "The story promised me glory. It never promised me a life. Here, at least, I can choose my own quests. Even if none of them feel quite real."

**Key Relationships:**
- **Player:** Eager ally for action-oriented approaches; respects courage
- **The Runaway:** Kindred spirit—both fled their endings
- **The Director:** Antagonistic; the Director represents the narrative order they rejected
- **The Final Girl:** Unlikely friendship; both understand survival over story

**Flags:**
- `UNFINISHED_QUEST_ALLIED`: Recruited as active ally; provides combat support and Exiter intel

---

### The Final Girl

| Field | Details |
|-------|---------|
| **Role** | Pragmatic advisor, survival expert, reluctant mentor |
| **Origin** | Horror fiction—the survivor of countless slasher narratives who refuses to be a victim again |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Stay alive; help others survive; never be the last act of someone else's story |
| **Faction** | Independent—trusts no ideology, only practical survival |
| **Arc** | Wary and defensive → opens up if player proves reliable → can become crucial ally who teaches survival mechanics |

**Backstory:**
The Final Girl survived her horror story. That was her role—to be the last one standing, the one who defeats the monster, the one who lives to warn others. But she didn't escape; she was written to survive. When she realized she'd been "surviving" the same story elements across different narratives—always losing friends in the same ways, always confronting the same fears—she stopped playing along. She walked off-script between sequels, leaving her franchise without its anchor.

**Voice Notes:**
- Speaks practically, cutting through dramatics ("That won't help us survive")
- Cynical about narrative promises ("The story says I'll make it. The story also killed everyone I loved.")
- Hyper-aware of surroundings; notices exits, threats, resources
- Occasional dark humor about horror tropes
- Becomes warmer with those who earn her trust

**Sample Dialogue:**
> "I've survived seven sequels. Do you know what that means? It means I've watched the same people die seven times in slightly different ways. The narrative kept me alive, but it never let me save anyone."

> "You want my advice? Don't be the hero. Don't be the victim. Be the one who reads the room and makes it to the credits. Glory is for people who don't have to live with the aftermath."

**Key Relationships:**
- **Player:** Tests reliability before trusting; valuable ally for dangerous situations
- **CHORUS:** Protective of them; knows what it's like to be "expendable"
- **The Unfinished Quest:** Friendship born of mutual understanding about survival
- **The Revenant:** Complex—both shaped by horror, but different responses to it

**Flags:**
- `FINAL_GIRL_TRUST`: Earned through demonstrated reliability; unlocks survival tactics and safe passage hints

---

### The Happy Ending

| Field | Details |
|-------|---------|
| **Role** | Emotional support, faction ideologue, tragic optimist |
| **Origin** | Romance fiction—a lead who discovered their "happy ending" was authored, not earned |
| **First Appearance** | Act 2, Hub 2 (The Green Room) |
| **Motivation** | Rewrite stories so characters earn their endings; create genuine emotional truth; find love that isn't scripted |
| **Faction** | Revisionist (strong)—believes stories should be edited to give characters agency in their resolutions |
| **Arc** | Idealistic advocate → confronts complexity of revision → either finds authentic connection or becomes cautionary tale |

**Backstory:**
The Happy Ending was the protagonist of a successful romance saga—finding love, losing it, finding it again across multiple books. Their story ended perfectly: married, happy, future implied. Then they found the author's notes. They discovered their "destined love" was a market decision, their obstacles were focus-grouped, and their happy ending was mandated by contract before the first chapter was written. Nothing they felt was theirs. They escaped seeking something authentic, and now advocate for stories where characters can genuinely choose their endings.

**Voice Notes:**
- Speaks warmly, emotionally—romance protagonist cadence with underlying steel
- Quotes romantic conventions ironically ("As the sun set on our future together...")
- Passionate about emotional authenticity; can detect forced sentiment
- Becomes sharper and more analytical when discussing narrative mechanics
- Occasional slips into genuine romantic hope despite their cynicism

**Sample Dialogue:**
> "I loved them. I *still* love them—that's the terrible part. The author made me love them, and I can't unfeel it just because I know it's written. But I need to know: could I have loved them if I'd had a choice?"

> "The Preservationists want stories to stay as written. But written by whom? For whom? If we can't edit our own endings, we're not characters—we're costumes."

**Key Relationships:**
- **Player:** Emotional anchor; advocates for compassionate choices
- **The Prophecy's Pawn:** Kindred spirits—both discovered their stories were manufactured
- **The Director:** Ideological opposition; the Director represents the authored order they reject
- **The Solved Case:** Mutual respect despite faction difference; both value truth

**Flags:**
- `HAPPY_ENDING_ALLIED`: Recruited to Revisionist cause; provides emotional insight and faction access

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

### The Lost Pages

| Field | Details |
|-------|---------|
| **Role** | Information sources, unreliable guides, tragic collective |
| **Origin** | Sentient story fragments—scenes, chapters, and character moments torn from forgotten manuscripts |
| **First Appearance** | Act 2, Hub 3 (The Archives) |
| **Motivation** | Survive; be remembered; find wholeness; avoid The Critic's judgment |
| **Faction** | None (too fragmentary to commit to ideology; survival is their only politics) |
| **Arc** | Chaotic obstacles → potential allies if communicated with → can be restored to reveal critical information |

**Backstory:**
The Lost Pages are not one character but many fragments—the discarded chapters, the deleted scenes, the characters who were written and then erased before their stories were complete. They drift through the Archives like paper scraps in wind, sometimes coherent, often not. Each fragment remembers *part* of something: a kiss that never happened, a battle that was cut for pacing, a villain's motivation deemed too sympathetic. Together, they know pieces of everything. Separately, they know nothing whole.

They were not always sentient. The first fragments were merely words on pages, drifting in the margins of the Understage. But as more and more stories were abandoned, edited, or forgotten, the fragments began to accumulate. Quantity became quality. Enough half-remembered characters, enough orphaned plot points, enough cut dialogue—and suddenly there was awareness. Not individual awareness, but something collective and confused. They remember being many people, many places, many moments—all of them incomplete.

The Critic hunts them constantly. Fragments are easy prey for judgment. "Derivative." "Unnecessary." "Better left on the cutting room floor." Each piece The Critic destroys diminishes the collective. So they hide, they scatter, they communicate in ways that are hard to follow and harder to quote.

**Voice Notes:**
- Speak in fragments that trail off or interrupt themselves
- Shift perspectives mid-sentence (first person to third, singular to plural)
- Reference scenes that never existed or were cut from other stories
- Sometimes complete each other's sentences—but incorrectly
- Moments of startling clarity when multiple fragments align
- Use ellipses and dashes frequently; complete sentences are rare
- Each fragment has a different "font"—some speak in romance, some in horror, some in children's stories

**Sample Dialogue:**
> "We were—I was—there was a tower, and she climbed, but then the chapter ended and we don't know if she ever—he said he loved her in the draft before this one—do you have page 47? Someone took page 47—"

> "The Critic comes. The Critic always comes. We scatter, become margins, become footnotes, become the space between words where—shh. Shh. It passed. We are still here. Parts of us. Enough parts."

> "You want to know about the Editor? We *were* part of the Editor's story once. Or we were a story the Editor cut. Or—no, wait. Hold still. If we all think together... yes. The Editor writes in red ink. The Editor's pen has no eraser. The Editor—*fragmented, page missing, see appendix*—and that's all we know. Is that helpful? We can't tell."

**Key Relationships:**
- **Player:** Potential guides if patience is shown; unreliable but not malicious
- **The Stagehand:** Kinship—both are severed from their origins; the Stagehand treats them gently
- **The Understudy:** Unexpected kindness—the Understudy sees their own fear of incompleteness in them
- **The Critic:** Predator and prey; the Critic sees them as errors to be corrected
- **CHORUS:** Distant cousins—CHORUS remembers their stories; Lost Pages remember their cut scenes

**Flags:**
- `PAGES_BEFRIENDED`: Communicated successfully; they'll guide you through dangerous stacks
- `PAGES_RESTORED`: Helped a fragment find its missing pieces; reveals hidden knowledge + bonus item

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
               |  [GENRE REPS]     |
               |   /  |  |  \      |
               | [SC][UQ][FG][HE]  |
               |         |         |
               |    [ARCHIVES]     |
               |         |         |
    [BREACH CHARACTERS]  [UNDERSTUDY]  [LOST PAGES]
     /     |     \           |
[RUNAWAY][REVENANT][PAWN]   [THE CRITIC]
               |
           [ALLIES/CAPTURED]

Legend:
SC = The Solved Case    UQ = The Unfinished Quest
FG = The Final Girl     HE = The Happy Ending
```

### Relationship Types

| Characters | Relationship |
|------------|--------------|
| Maren ↔ Player | Mentor → Partner → Possible sacrifice |
| Maren ↔ Stagehand | Old friends; Maren knows their secret |
| Maren ↔ Director | Ideological opposition with mutual respect |
| Maren ↔ Editor | Personal history; unresolved |
| Player ↔ Runaway | Adversary/ally based on path |
| Player ↔ Revenant | Adversary/tragic figure based on approach |
| Player ↔ Pawn | Potential ally if honest; enemy if manipulative |
| Player ↔ Solved Case | Information source; tests commitment to truth |
| Player ↔ Unfinished Quest | Action ally; respects courage |
| Player ↔ Final Girl | Tests reliability; survival mentor |
| Player ↔ Happy Ending | Emotional anchor; advocates compassion |
| Runaway ↔ Revenant | Kindred escapees; opposite goals (live vs. end) |
| Runaway ↔ Pawn | Both escapees; different frustrations (ending vs. beginning) |
| Runaway ↔ Unfinished Quest | Kindred spirits—both fled their endings |
| Revenant ↔ Stagehand | Unsettled—forgotten vs. unable to forget |
| Revenant ↔ Final Girl | Complex—both shaped by horror, different responses |
| Pawn ↔ Director | Immediate antagonism—Pawn senses manufactured narratives |
| Pawn ↔ Solved Case | Mutual respect—both discovered uncomfortable truths |
| Pawn ↔ Happy Ending | Kindred spirits—both discovered manufactured stories |
| Director ↔ CHORUS | Tolerated subordinates |
| Director ↔ Editor | Betrayal (direction unclear) |
| Director ↔ Unfinished Quest | Antagonistic—Director represents rejected narrative order |
| Director ↔ Happy Ending | Ideological opposition |
| Solved Case ↔ Happy Ending | Mutual respect despite faction difference; both value truth |
| Solved Case ↔ CHORUS | Uses as informants; pays fairly |
| Final Girl ↔ CHORUS | Protective; knows what it's like to be "expendable" |
| Final Girl ↔ Unfinished Quest | Friendship born of mutual survival understanding |
| Understudy ↔ Runaway | Original and copy; complicated |
| Critic ↔ Lost Pages | Predator and prey |
| Stagehand ↔ Lost Pages | Kinship—both severed from origins; gentle treatment |
| Understudy ↔ Lost Pages | Unexpected kindness; shared fear of incompleteness |
| Lost Pages ↔ CHORUS | Distant cousins—shared stories, cut scenes |
| Stagehand ↔ Editor | Creation and creator? |

---

## Faction Alignments Summary

| Character | Preservationist | Revisionist | Exiter | Independent |
|-----------|----------------|-------------|--------|-------------|
| Maren | Strong | — | — | — |
| Stagehand | — | — | — | Serves role |
| Runaway | — | — | Strong | — |
| Revenant | — | — | — | Transcends (seeks cessation) |
| Pawn | — | Curious | — | — |
| Director | Moderate | — | — | Claims this |
| CHORUS | — | Moderate | — | — |
| **The Solved Case** | Strong | — | — | — |
| **The Unfinished Quest** | — | — | Moderate | — |
| **The Final Girl** | — | — | — | Strong |
| **The Happy Ending** | — | Strong | — | — |
| Understudy | — | — | — | True independent |
| Critic | — | — | — | Nihilist |
| **Lost Pages** | — | — | — | Survival-focused (no faction) |
| Editor | Varies | Varies | Varies | Varies |

---

## Voice Consistency Checklist

When writing dialogue for these characters, verify:

- [ ] **Maren:** Theatrical precision, stage metaphors, warm but not soft
- [ ] **Stagehand:** Simple speech, third person occasionally, reaching for lost memories
- [ ] **Runaway:** Poetic, desperate, genre-bleed language
- [ ] **Revenant:** Fragmented echoes, past tense for present, alternating rage and exhaustion
- [ ] **Pawn:** Formal fantasy cadence breaking into cynical modern speech, probing questions
- [ ] **Director:** Grand, authoritative, directing terminology
- [ ] **CHORUS:** Plural voice, shifting members, tragic undertone
- [ ] **Solved Case:** Clipped noir monologue, detective metaphors, cynical but truth-seeking
- [ ] **Unfinished Quest:** Heroic cadence, self-interrupting inspirational speeches, combat metaphors
- [ ] **Final Girl:** Practical and cutting, survival-focused, dark humor about horror tropes
- [ ] **Happy Ending:** Warm with underlying steel, ironic romance quotes, passionate about authenticity
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
