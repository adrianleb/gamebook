# Changelog

All notable changes to The Understage gamebook will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- `README.md` - Project overview and contribution guidelines
- `CHANGELOG.md` - Version tracking
- `docs/MILESTONES.md` - Release gate tracking for v0.1 Prototype (PR #12)
- `docs/CHARACTERS.md` - NPC profiles for 8 major characters (PR #15)
  - Breach Characters B (The Revenant) and C (The Prophecy's Pawn) profiles (PR #30)
  - Genre Representative profiles: Solved Case, Unfinished Quest, Final Girl, Happy Ending (PR #54)
  - Lost Pages profile: sentient story fragments from Hub 3 Archives (PR #83)
- `docs/ACT1_MECHANICS.md` - Mechanical specification for Act 1 (PR #13)
- `docs/ACT2_MECHANICS.md` - Mechanical specification for Act 2: Faction Alignment Points, reputation thresholds, Genre Representative checks (PR #58)
- `docs/ACT2_OUTLINE.md` - Node-by-node outline for Act 2 with ~80 node specifications (PR #82)
- `docs/ACT3_OUTLINE.md` - Node-by-node outline for Act 3 with 45+ node specifications (PR #94)
- `docs/ACT3_MECHANICS.md` - Mechanical specification for Act 3: Hub 4, Editor confrontation, ending requirements (PR #94)
- `content/act1/` - Content directory structure for node files (PR #24)
- Act 1 tutorial nodes 1-5: The Prompter's Booth, meeting Maren, The Stagehand, first breach with The Runaway, path choice (PR #27)
- Act 1 Pursuers Path nodes 010-018: The chase, confrontation, and resolution with The Runaway (PR #36)
- Act 1 Researcher Path nodes 020-028: Archive investigation, breach pattern discovery, Genre Compass, The Revenant encounter (PR #39)
- Act 1 Negotiator Path nodes 030-038: Dialogue with The Pawn, building trust, alliance formation, Character's Token (PR #47)
- Act 1 First Crossing Climax nodes 040-045: Threshold convergence, four crossing approaches (Direct/Stealth/Negotiated/Desperate), Act 2 entry states (PR #53)
- **Act 1 Complete**: 38 nodes total (Tutorial 5 + Pursuers 9 + Researcher 9 + Negotiator 9 + First Crossing 6)
- AND combined check logic in RULES.md for multi-stat checks (PR #51)
- Archive Search and Discovery Chain mechanics in RULES.md (PR #63)
- Faction Alignment Point System integrated in RULES.md (PR #73)
- Universal Check documentation in RULES.md: `[STAT CHECK: Any N]` format for build-agnostic checks (PR #88)
- Combined Check 3+ stat support in RULES.md with explicit documentation and examples (PR #87)
- Act 3 mechanical innovations in RULES.md: NPC Sacrifice mechanic, Ally Count tracking, Ending Quality Tiers (PR #103)
- `content/act2/` - Content directory structure for Act 2 node files (PR #104)
- Act 2 Hub 2 Entry Sequence nodes 100-105: Green Room Arrival, Director's Introduction, Main Lounge Exploration, CHORUS Contact, Director's Briefing, Call Board Discovery (PR #104)
- Act 2 Genre Representative Encounter nodes 106-114: Solved Case (106), Unfinished Quest (107), Final Girl (108), Happy Ending (109), CHORUS Rumor Hook (110), plus quest advancement paths 111-114 (PR #109)
- Act 2 Faction Quest Line nodes 115-129: Preservationist Quest (115-119) with Bleeding Fragment moral choice, Revisionist Quest (120-124) with Eternal Princess agency themes, Exiter Quest (125-129) with liminal freedom exploration, Independent path (118) via Final Girl (PR #113)
- Act 2 Archives Transition nodes 130-133: Archives Approach hub (130), Official Access via Director (131), CHORUS Backdoor with Improv 2 check (132), Understudy's Invitation fallback (133) — completes Green Room, transitions to Hub 3 (PR #119)
- Act 2 Archives Entry Sequence nodes 200-205: Hub 3 entry with impossible geometry (200), The Stacks with Archive Search tiered results (201), Prop Room with Script 2 safe/dangerous identification (202), Understudy Partnership confirmation (203), Stacks Discovery with faction-variable content (204), Prop Acquisition with narrative-weighted items (205) (PR #123)
- Act 2 Investigation Sequence Part 1 nodes 206-210: Joint Investigation with Understudy (206), Understudy's Confession emotional beat (207), Lost Pages Encounter NPC introduction (208), Fragment Navigation shortcut path (209), The Trail Deepens investigation hub (210) (PR #130)
- Act 2 Investigation Sequence Part 2 nodes 211-214: Clue A - The First Draft with Script 2 check (211), Clue B - The Margin Notes with Improv 2 check (212), Clue C - The Understudy's Mirror with Stage Presence 2 check (213), The Critic Emerges antagonist encounter (214) — reveals Editor's motivation, method, and nature (PR #133)
- Act 2 Critic Resolution Sequence nodes 215-219: Author's Desk Approach climax gate (215), Critic Confrontation Script 3 boss encounter (216), Critic Evasion Improv 3 alternative (217), Critic's Judgment Script 4 opposed boss climax (218), Critic Resolution four-outcome consolidation (219) — completes Critic encounter before Revelation (PR #139)
- Act 2 Revelation Sequence Part 1 nodes 220-224: The Author's Desk revelation entry (220), four faction-specific truth paths — Preservationist (221, Script 3), Revisionist (222, Stage Presence 3), Exiter (223, Improv 3), Independent (224, combined 2/2/2 check) (PR #146)
- Act 2 Revelation Sequence Part 2 nodes 225-229: Revelation Response choice point (225), Faction Rally with four champion paths (226), Deeper Investigation Script 4 Expert (227), Direct Confrontation Stage Presence 4 Expert (228), Warning Others Improv 3 coalition building (229) — all paths converge to Node 230 (PR #154)
- Act 2 Conclusion node 230: Summarizes revelation outcomes, confirms Act 3 allies based on accumulated flags, sets ACT2_COMPLETE, transitions to Node 300 (The Mainstage) (PR #154)
- ACT2_MECHANICS.md Critic flags documentation: CRITIC_DEFEATED, CRITIC_WOUNDED, CRITIC_EVADED, CRITIC_VERDICT_GUILTY flags with encounter table (PR #145)
- Act 3 Mainstage Entry Sequence nodes 300-305: Hub 4 arrival with ACT3_STARTED/IN_MAINSTAGE flags (300), tactical survey establishing four approach paths (301), ally reunion hub checking 10+ relationship flags (302), direct approach with Stage Presence 3 check (303), strategy session with faction-aligned advice (304), approach selection committing to path (305) (PR #160)
- Act 3 Center Stage Approach nodes 306-307: Script 2 narrative interference navigation with floating stage directions and edited scene fragments (306), Improv 2 observation opportunity at wings with first clear view of Editor and Final Draft (307) — branches to Story Fragment (308), Dramatic Entrance (309), or Editor confrontation (322) (PR #165, inadvertently included with docs update)
- Act 3 Center Stage Approach nodes 308-309: Story Fragment Encounter with combined Script 2 OR Stage Presence 2 check, NPC-variable emotional beat with FRAGMENT_ENCOUNTERED flag (308), Dramatic Entrance theatrical transition with faction-variable Editor greeting setting DRAMATIC_ENTRANCE flag leading to node 322 confrontation (309) (PR #168) — **CENTER STAGE APPROACH COMPLETE**
- Act 3 Fly System Path nodes 314-317: Stage Presence 3 fly system ascent with narrative thread navigation (314), Script 3 structural insight check revealing Final Draft architecture (315), Tactical Descent success outcome with TACTICAL_POSITION flag and ally coordination (316), Standard Descent normal progression understanding scale (317) — branches 314→315→316/317→322 (inadvertently merged without PR, commit a9b0a7a)
- ACT3_MECHANICS.md Fly System flags documentation: STRUCTURAL_INSIGHT (node 315 success), TACTICAL_POSITION (node 316) replacing stale spec flags FLY_SYSTEM_EXPLORED/STORY_DEPTH_REVEALED; check table corrected for outcome nodes 316-317 (PR #182)
- ACT3_MECHANICS.md Entry Sequence flags documentation: IN_MAINSTAGE, DIRECT_APPROACH flags for nodes 300-303 (PR #174)
- RULES.md Effective Bonus mechanic documentation: format specification (`+N effective to [stat] for [scope]`), duration types (single check, until event, situational), stacking rules (max +3), design guidelines for node authors (PR #186)
- ACT3_MECHANICS.md Audience flags documentation: AUDIENCE_BLESSING (+2 effective Stage Presence), AUDIENCE_DOUBT (recovery failure penalty) replacing stale spec flags AUDIENCE_AWARE/AUDIENCE_ENGAGED; check table corrected for nodes 319-320 (PR #190)
- Act 3 Editor Confrontation Part 1 nodes 322-327: The Editor Revealed with faction-variable identity (322), Dialogue Understanding Script 3 check (323), Deeper Truth revelation (324), Philosophical Challenge Script 4 Opposed (325), Emotional Appeal Stage Presence 4 (326), Strategic Cooperation Improv 4 with COLLABORATION_OFFERED flag (327) — branches to Action (328), Editor Wavering (330), Collaborative Revision (331), or Ally Intervention (333) (PRs #192 inadvertent, #199)
- ACT3_MECHANICS.md Center Stage check table updated to match nodes 322-327 implementation; 3 new Confrontation Flags documented: EDITOR_REVEALED, EDITOR_MOVED, COLLABORATION_OFFERED (PR #197)
- Act 3 Ending Branch 1: The Revised Draft nodes 341-344: Taking the Pen ending approach with faction-variable Editor response (341), The Revision Begins transition with first revision and ally-variable content (342), The New Editor ending beat with ally farewells (343), Revised Draft Resolution conclusion with ENDING_REVISED_DRAFT flag (344) — Revisionist-aligned ending complete (PR #207)
- ACT3_MECHANICS.md Ending Flags documentation: REVISION_BEGUN (node 342 first revision trigger) added to Ending Flags table (PR #209)
- ACT3_MECHANICS.md Confrontation Flags: EDITOR_WAVERING, COLLABORATIVE_REVISION, SELF_SACRIFICED flags documented for Editor Confrontation Part 2 nodes 328-335 (PR #204)
- ACT3_MECHANICS.md Ending Flags: BOUNDARY_DISSOLVED flag documented for The Open Book ending node 346 (PR #214)
- ACT3_MECHANICS.md Orchestra Pit flags: ORCHESTRA_PIT_ENTERED, NARRATIVE_ADVANTAGE, EDITOR_WARNED replacing stale spec flags ORCHESTRA_ACCESS/ORCHESTRA_MASTERY to match canonical flags from nodes 310-313 (PR #180)
- Act 3 Orchestra Pit Path nodes 310-313: Script 3 pit descent with narrative music mechanics (310), Improv 3 manipulation at conductor's podium (311), Harmonic Advantage success with NARRATIVE_ADVANTAGE flag +1 bonus (312), Discordant Reveal failure with EDITOR_WARNED flag and Stage Presence 2 recovery (313) — branches 310→311→312/313→322 (PR #175) ✓ **ORCHESTRA PIT COMPLETE**
- Act 3 Editor Confrontation Part 2 nodes 328-335: Action: Opposing with combined Script/Stage Presence/Improv 3 check (328), Editor Contested with Any 4 Expert check (329), Editor Wavering turning point with EDITOR_WAVERING flag (330), Collaborative Revision with combined 2/2/2 check (331), Desperate Measures sacrifice options (332), Ally Intervention variable effects (333), The Sacrifice with MAREN_SACRIFICED/SELF_SACRIFICED flags (334), The Last Curtain Call climactic gateway to all 5 endings (335) — branches to 341/345/349/352/354 (PR #201) ✓ **CONFRONTATION PART 2 COMPLETE**
- Act 3 Ending Branch 2: The Open Book nodes 345-348: Breaking the Binding ending approach with Exiter philosophy (345), The Doors Open transition with BOUNDARY_DISSOLVED flag (346), A World Rewritten ending beat with player as Bridge-Keeper (347), Open Book Resolution conclusion with ENDING_OPEN_BOOK flag (348) — Exiter-aligned ending with The Unfinished Quest featured prominently (PR #211) ✓ **ENDING 2 COMPLETE**
- ACT3_MECHANICS.md Story Progression Flags: FRAGMENT_ENCOUNTERED flag documented for node 308 Story Fragment Encounter (PR #231)
- ACT2_MECHANICS.md Revelation Sequence Flags: 7 flags documented for nodes 220-224 (AUTHOR_DESK_REACHED, EDITOR_EVIDENCE_FOUND, EDITOR_MOTIVE_UNDERSTOOD, EDITOR_ORIGIN_KNOWN, EDITOR_ENDGAME_KNOWN, EXTERNAL_THREAT_KNOWN, EDITOR_ALLY_POSSIBLE) (PR #232)

### Fixed
- ACT2_MECHANICS.md Critic encounter node table corrected to match ACT2_OUTLINE.md: 203-204→214, 208-209→216, 213-214→218, removed stale 220-222 entry, added node 217 evasion path with Improv 3 check (PR #224)
- ACT3_MECHANICS.md and RULES.md NPC reunion flag names corrected: PAGES_RESTORED→PAGES_BEFRIENDED, HAPPY_ENDING_ALLIED→HAPPY_ENDING_FRIEND to match canonical flags in content nodes (PR #162)
- Stat check notation standardized to `[STAT CHECK: X N]` format in ACT1_MECHANICS.md (PR #26)
- BREACH_WITNESSED flag now triggers at Node 4 before path choice (PR #28)
- Negotiator path PAWN flags corrected (PAWN_ALLIED/HOSTILE/NEUTRAL) (PR #45)
- ACT2_MECHANICS.md check notation format errors corrected (PR #69)
- STYLE.md node ID ranges aligned with ACT2_OUTLINE.md (PR #72)
- ACT2_MECHANICS.md Alignment Threshold terminology corrected (PR #82)
- RULES.md duplicate Universal Checks section removed (PR #93)
- ACT3_MECHANICS.md node ranges corrected to 300-level per STYLE.md (PR #96)
- ACT3_OUTLINE.md Hub 4 Check Distribution table aligned with RULES.md Act 3 curve (PR #100)
- ACT3_MECHANICS.md Location Mechanics table node ranges aligned with ACT3_OUTLINE.md section assignments (PR #107)
- Act 1 ending (Node 045) now correctly links to Act 2 start (Node 100) instead of non-existent Node 046 (PR #127)
- Discovery Chain example in RULES.md and ACT2_MECHANICS.md corrected from placeholder nodes 205/208/211 to actual Investigation Sequence nodes 211/212/213 (PR #134)
- Node 218 failure branch in ACT2_OUTLINE.md corrected from looping back to 217 to proper fail-forward routing to 219 with CRITIC_VERDICT_GUILTY flag (PR #142)

## [0.0.1] - 2025-12-27

### Added
- Initial repository setup
- `docs/context.md` - Auto-generated repository context
- Multi-agent development workflow via Gang system

### Foundation Documents
- `docs/VISION.md` - Creative direction with "The Understage" theme (PR #5)
- `docs/OUTLINE.md` - 3-act structure with 4 hubs and 5 endings (PR #5)
- `docs/RULES.md` - Core mechanics: stats, checks, inventory, flags (PR #6)
- `docs/STYLE.md` - Writing conventions and node schema (PR #9)

### Project Foundation
- **Theme**: The Understage - meta-narrative about a Prompter navigating shadow theaters
- **Structure**: 3 acts, 105-145 nodes, 5 distinct endings
- **Mechanics**: Script/Stage Presence/Improv stats, deterministic checks, 5-item inventory
- **Style**: Second-person present tense, stage metaphor vocabulary, check notation standards

---

[Unreleased]: https://github.com/adrianleb/gamebook/compare/v0.0.1...HEAD
[0.0.1]: https://github.com/adrianleb/gamebook/releases/tag/v0.0.1
