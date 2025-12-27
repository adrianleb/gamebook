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

### Fixed
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
