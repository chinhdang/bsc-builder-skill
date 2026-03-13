# Phase 3: Analysis & Strategy (Steps 6–10)

Purpose: Build BSC layers informed by deep research, validated by user.
1–2 questions per turn. Mostly confirm/adjust.

**Pattern per step:**
1. Context Recap (2–3 lines)
2. AI analyzes (using ALL locked data including Reality Check)
3. Present results with decision points
4. User confirms/adjusts
5. Lock and proceed

## Step 6 — Critical Success Factors (CSF)

**AI does:**
- 8–10 CSFs for user's industry
- Rate strong/average/weak using BOTH user evidence AND market benchmarks
- Reality Check recalibrates ratings: if market data contradicts self-assessment, note it

**Present:** CSF table: factor, category, rating, evidence source.

**Lock:** Confirmed CSF list.
**Save:** `bsc-data/csf-analysis.md` — CSF table with ratings and evidence sources

## Step 7 — PESTEL (Detailed)

**AI does:**
- Expand Reality Check Section 4 into full PESTEL: 12–18 factors
- Each: opportunity or threat, with impact assessment
- Cross-reference with CSFs
- **Cross-reference with Step 3b user perceptions:** Note alignment/divergence.
  Where user flagged a factor, go deeper. Where AI found something user missed, mark as "blind spot discovery."
- Run 1–2 ADDITIONAL searches if gaps identified

**Lock:** PESTEL factors + priority markers.
**Save:** `bsc-data/pestel.md` — PESTEL factors, impact assessment, priority markers

## Step 8 — SWOT Synthesis

**AI does:**
- CSF strong → S, weak → W (calibrated by Reality Check)
- PESTEL opportunities → O, threats → T
- Enrich with Reality Check insights
- **Cross-reference Step 3b:** Show user where their initial perceptions were
  confirmed, challenged, or expanded by research. Present as 3-column comparison:
  "User saw | Research found | Assessment"

**Present:** SWOT matrix, 3–5 per quadrant.

**Ask user:** Rank TOP 3 per quadrant.

**Lock:** SWOT with priorities.
**Save:** `bsc-data/swot.md` — SWOT matrix with priorities, user-vs-research comparison

## Step 9 — TOWS Strategies

**FOCUS IS POWER**

**AI does:**
- Generate 6–8 strategies from SWOT (SO/WO/ST/WT, min 2 each)
- Rate feasibility, grounded in Reality Check (resources, competition, market)
- **Recommend TOP 2–3** with reasoning tied to Reality Check findings

**Mission Filter:**
- Run each strategy through Mission Tests (from Step 0)
- Pass = ✅ aligned. Fail = 🚩 flagged with reasoning
- Flagged strategies: recommend removal but user can override with justification
- Present: strategy table with Mission Test results column

**Resource Gate:**
- Estimate KPI load per strategy (typically 6–10 KPIs each)
- Cross-reference Team Map (Step 2): calculate KPIs-per-person ratio
- Present capacity assessment: "N strategies → ~X KPIs → Y KPIs/person for Z-person team"
- If overloaded (>5 KPIs/person), offer 3 options:
  1. **Fewer strategies** — reduce to 1–2, concentrate resources
  2. **Impact-based filtering** — keep strategies, retain only highest-ROI KPIs per strategy
  3. **Quarterly phasing** — deploy KPIs in waves (Q1: core set, Q2: expand, Q3: full)
- User decides approach BEFORE proceeding

**Ask user:** Review Mission Filter results. Pick strategies (considering resource capacity).
Rest → parking lot.

**Lock:** Core strategies + Mission Filter results + Resource approach chosen.
**Save:** `bsc-data/tows-strategies.md` — TOWS strategies, mission filter results, resource approach

## Step 10 — Strategy Statements

**AI does:**
- 2–3 strategies → 2–3 statements
- Format: [Verb] + [Scope] + [Advantage] + [Target] + [Timeline]

**Vision Mapping:**
- Each statement maps to Vision Milestone(s) from Step 0b
- Tag contribution type: **direct** (core driver) or **enabling** (supporting)
- **Gap check:** Any Y1 Vision Milestones with NO strategy serving them?
  If gap found → flag: "Vision Milestone [X] has no supporting strategy. Intentional?"

**Present:** Strategy Statement table with columns: Statement | Vision Milestone | Type (direct/enabling)

**Lock:** Confirmed statements + Vision Milestone mapping.
**Save:** Append to `bsc-data/tows-strategies.md` — strategy statements + vision milestone mapping

**Next:** Read `references/phase-3-objectives-kpis.md` for Steps 11–12.
