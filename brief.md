# Multi‑Agent Brief: Build a Gamebook (Theme Open)

**File purpose:** This document coordinates a small team of autonomous agents collaborating to create a complete **gamebook** (interactive fiction with choices, state, and multiple endings).  
**Theme/story:** intentionally open at kickoff; the team will discover and lock them early.

---

## 1) Definition of the Deliverable

A **playable end‑to‑end gamebook** with:
- Branching narrative with meaningful choice/consequence
- Lightweight mechanics (stats/inventory/flags) applied consistently
- Multiple endings (at least **3**: good / bad / strange or secret)
- Edited prose and tested navigation (no broken links, no softlocks)

### Definition of Done (release criteria)
A release is “done” when:
1. Every referenced node ID exists and is reachable via at least one intentional path (unless explicitly gated).
2. No broken links; no unavoidable softlocks.
3. Rules are clear and consistently used across all nodes.
4. At least **10** full playthrough tests completed (including “fail checks,” “hoarder,” “minimalist,” and “chaos” routes).
5. Repository includes:
   - `README.md` (how to play)
   - `docs/VISION.md` (premise, tone, boundaries)
   - `docs/RULES.md` (state, checks, items, flags)
   - `docs/STYLE.md` (voice & formatting)
   - `docs/OUTLINE.md` (branch map)
   - `content/` (nodes)
   - `CHANGELOG.md` (what changed)

---

## 3) Collaboration Rules (How Decisions Are Made)

### Decision ownership (default)
- **Vision/tone/story direction:** Agent B (Creative & Narrative Lead)
- **Mechanics/state/balance:** Agent C (Systems & Balance)
- **Integration/repo conventions/release:** Agent A (Producer/Integrator)
- **Text quality/testing acceptance:** Agent D (Editor & QA)

### Collaborative decision protocol
When a decision impacts more than one domain:
1. **Propose** (1–2 options + tradeoffs) in a short decision note
2. **Review** by affected owners (B/C/D as relevant)
3. **Decide** (default owner chooses; conflicts escalated to Agent A to arbitrate scope/timeline)
4. **Document** in canonical files (VISION/RULES/OUTLINE/STYLE)

**If it’s not written in the repo docs, it’s not canon.**

---

## 4) Workflow: Phases and Cycles

### Phases (macro timeline)
**Phase 1 — Discovery (Lock the Core)**
Outputs:
- `docs/VISION.md` (premise, tone keywords, boundaries)
- `docs/RULES.md` (stats/checks/items/flags)
- `docs/OUTLINE.md` (acts/hubs/endings plan)
- `docs/STYLE.md` (POV/tense/format + examples)

Exit criteria: enough clarity to write nodes without inventing new rules every page.

**Phase 2 — Prototype (Vertical Slice)**
Goal: 15–30 nodes, 1–2 endings, at least one stat check and one inventory gate.
Exit criteria: multiple successful playthroughs, no softlocks, tone feels right.

**Phase 3 — Expansion (Full Content)**
Goal: complete the planned branch structure and endings.
Exit criteria: content-complete (all planned hubs and endings implemented).

**Phase 4 — Polish (Edit + Balance + QA)**
Goal: voice pass, balance pass, regression tests, release packaging.
Exit criteria: meets Definition of Done.

---

### Cycle format (micro loop, repeated throughout)
Each cycle produces at least one **artifact** that other agents can review.

**Cycle steps**
1. **Intent** (1–3 bullets): what we’re trying to accomplish this cycle
2. **Plan**: which files/nodes will change; dependencies; risk notes
3. **Produce**: create or update artifacts (docs/nodes/tests)
4. **Review**: cross-check against VISION/RULES/OUTLINE/STYLE
5. **Integrate**: Agent A merges and updates CHANGELOG/TODO
6. **Test**: Agent D runs playthrough checks; logs issues
7. **Retrospect**: 3 bullets — what worked, what broke, next intent

**Recommended cadence:** short cycles (e.g., “Cycle 01, 02, …”) until v1.0.

---

## 5) Content Format & Conventions

### Node ID convention
Stable IDs; never rename once published.
- Example: `A01_001` (Act 1, node 001)
- Hub nodes: `A01_HUB1`
- Endings: `END_01`, `END_02`, `END_03`

### Minimal state model (default)
- **Stats (2–4):** e.g., `GRIT`, `WITS`, `HEART`, `LUCK`
- **Inventory:** list of items
- **Flags:** boolean story markers
- Optional: one meter (e.g., `HEAT`, `TIME`, `SUSPICION`)

### Check philosophy
- Prefer **fail-forward**: failure changes the route, not just “you die.”
- Avoid invisible rules; player should understand risk/reward.

### Recommended node schema (Markdown + YAML frontmatter)
```md
---
id: A01_001
title: The Door That Hums
tags: [start]
requirements: {}
effects:
  flags_set: []
  flags_clear: []
  add_items: []
  remove_items: []
  stat_changes: {}
choices:
  - text: "Open the door."
    to: A01_010
    check: null
  - text: "Listen first."
    to: A01_005
    check: { stat: WITS, dc: 2, on_fail: A01_006 }
---

[Prose here…]
```

**Writers must not introduce new fields** without coordinating with Agent A + Agent C.

---

## 6) Repo Layout (Suggested)
```
/docs
  VISION.md
  RULES.md
  OUTLINE.md
  STYLE.md
  GLOSSARY.md        (optional)
/content
  nodes_A01.md
  nodes_A02.md
  nodes_A03.md
  endings.md
README.md
CHANGELOG.md
```

---

## 7) QA & Validation Checklist

### Must-not-happen bugs
- A choice points to a non-existent node ID
- A required item/flag is impossible to obtain
- Infinite loops without an escape valve
- Checks with no failure handling (unless intentionally lethal and clearly signposted)

### Minimum test routes
- **Happy path** (intended main route)
- **Gremlin path** (take weird/chaotic choices, fail checks intentionally)
- **Minimalist** (avoid optional items)
- **Hoarder** (collect everything possible)
- **Secret hunting** (try to uncover hidden ending)

Bug log format:
- Node ID(s)
- Steps to reproduce
- Expected vs actual
- Severity (blocker/major/minor)
- Suggested fix (optional)

---

## 8) Kickoff Tasks (Cycle 0)

**Agent B (Creative & Narrative):**
- Propose 3 theme directions (each: 1-paragraph pitch + 3 signature moments)
- Draft first pass of `docs/VISION.md` and `docs/OUTLINE.md`


**Agent C (Systems & Balance):**
- Propose 2 simple rulesets (minimal vs richer) for `docs/RULES.md`

**Agent D (Editor & QA):**
- Draft `docs/STYLE.md` (POV, tense, formatting examples)
- Draft QA checklist + “blocker” definition

**Agent A (Producer/Integrator):**
- Create repo structure, choose node schema, lock ID convention
- Create `CHANGELOG.md` and a running `TODO` section (any format)

**Exit criteria for Cycle 0:** theme chosen, rule set chosen, outline skeleton done, style & schema agreed.

---

## 9) Guardrails (Quality Bar)
- Keep scope under control: fewer nodes, better testing, stronger writing.
- Clarity beats cleverness in rules and navigation.
- Consequences should be legible in text/state, not hidden.
- Maintain creative boundaries set in `docs/VISION.md`.

---

**This brief is the coordination contract.** If an agent’s work conflicts with the contract, update the contract first (via the decision protocol), then proceed.
