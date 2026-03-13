# Phase 3b: Strategic Objectives & KPIs (Steps 11–12)

## Step 11 — Strategic Objectives (4 Enriched Perspectives)

Read `references/standard-measures-catalog.md` for standard BSC measures per perspective.
Use as ADVISORY reference — filter by company's industry tag from Step 0.
Ensure objectives cover sub-categories where standard measures exist, unless strategy dictates otherwise.

**AI does:**
- Strategy statements → objectives across 4 perspectives with enriched sub-categories
- 3–5 per perspective, each with causality explanation
- Targets calibrated against Reality Check benchmarks

Read `references/perspective-framework.md` for the enriched perspectives tree.

**Causality rules:**
- **Strategy map: FIVE layers bottom-up.** Foundation → Process → Customer → Financial → **VISION MILESTONES (Roof)**
- Top Financial objectives must show HOW they feed current-period Vision Milestone
- Vision Milestone = the "so what" above Financial
- **Causality text: acknowledge FEEDBACK LOOPS.** Example: "Financial growth enables
  reinvestment in Foundation (hiring, tech) — creating a virtuous cycle." But do NOT
  draw downward arrows on the strategy map.
- Each causality text answers: "This drives [upper objective] because [mechanism].
  Feedback loop: [any reverse dependency, if exists]."

**Traceability:**
- Each objective traces: Objective → Strategy Statement → Vision Milestone
- Present traceability table: Objective | Perspective | Strategy | Vision Milestone
- Flag orphan objectives (no clear Vision Milestone connection)

**Ask user:** Priorities? Sub-categories that need objectives but don't have one?

**Lock:** Objectives by perspective + causality links + feedback loops noted.
**Save:** `bsc-data/objectives-kpis.md` — objectives by perspective, causality links, traceability table

## Step 12 — KPIs + Initiatives + Resource Loading

### KPIs
- 2–3 per objective (leading + lagging mix)
- Reference `references/standard-measures-catalog.md` — pick standard measures that fit company context
- Industry-tagged measures matching company's sector get priority
- Custom measures allowed when standard ones don't fit specific strategy
- Baselines from user data; targets vs. industry benchmarks
- Flag estimates: "Industry benchmark is [X]. I suggest [Y] — confirm?"
- Each KPI must have: **owner** (primary department/person) and **contributors** with weight %

### KPI Causal Chain Mapping (REQUIRED)

After defining all KPIs, build cross-perspective causal chains:

**AI does:**
1. For each lagging KPI, trace backwards: which leading KPI(s) in lower perspectives drive it?
2. Build causal chain hypotheses: `L:[leading] → P:[process] → C:[customer] → F:[financial]`
3. Present each chain as hypothesis: "If [leading KPI] improves by X → [lagging KPI] improves by Y because [mechanism]"
4. Flag **orphan KPIs** (no causal link up or down) — these may be vanity metrics
5. Flag **broken chains** (perspective gap: eg Financial KPI with no Customer driver)
6. Generate **Causal Chain Map** table:

```
| Chain # | Foundation (Leading) | Process | Customer | Financial (Lagging) |
|---------|---------------------|---------|----------|-------------------|
| 1 | Training hours ↑ | Cycle time ↓ | On-time delivery ↑ | Revenue ↑ |
| 2 | AI adoption ↑ | Error rate ↓ | CSAT ↑ | Margin ↑ |
```

**Ask user:** "Các chuỗi nhân quả này đúng với thực tế công ty không? Link nào sai? Thiếu link nào?"

**Human validates:** User confirms, adjusts, or adds missing links based on business context.
AI refines chains based on feedback. Iterate until agreement.

**Lock:** Agreed causal chain map. Each KPI now has upstream/downstream connections.

**Monthly validation:** During execution (Step 12c), when lagging KPI misses target → trace backwards through chain to find root cause at leading indicator level.

### Initiatives
- 3–6 initiatives: name, linked objectives, priority, timeline, budget, milestones
- Budget fits within stated capacity
- Timeline realistic for team size

### Resource Loading Matrix (REQUIRED)

Two dimensions per KPI:

**A. Responsibility weight (per KPI, sums to 100%):**
Who is accountable? E.g., Lead generation → Marketing 80%, Sales 20%.

**B. Capacity allocation (per person, sums to ~100%):**
How much of each person's time does each KPI consume?

Read `references/resource-loading-matrix.md` for format and thresholds.

**Resource Check (from Step 9 decision):**
- If "fewer strategies" chosen: enforce strict KPI count (max 2 per objective)
- If "impact-based": rank KPIs by expected impact, present top N that fit capacity
- If "quarterly phasing": tag each KPI with deployment quarter (Q1/Q2/Q3/Q4)
- Recalculate capacity allocation — warn if any person >120%

**Ask user:** CRITICAL VALIDATION.
1. Baselines correct? Targets realistic?
2. Capacity allocation: does this reflect real time split? Who is overloaded?

**Lock:** KPIs (with ownership & responsibility) + Initiatives + Resource Loading Matrix.
**Save:** Append to `bsc-data/objectives-kpis.md` — KPIs, initiatives, resource loading matrix

## Step 12a — Back-Office & Wellbeing KPIs

**Ask user:** "Trong team có vai trò back-office (kế toán, HR, admin, pháp lý) không?
Nếu có, cần KPIs cho họ để đảm bảo operational backbone vận hành tốt."

**If user confirms back-office roles exist:**

Read `references/backoffice-kpi-templates.md` for KPI templates by function.

**AI does:**
1. Identify back-office functions from team roster (Step 2 data)
2. Select relevant KPIs from template library, scaled by company size:
   - **Micro (≤15 people, kiêm nhiệm):** Max 3–5 KPIs total per person across all functions
   - **SME (15–50, chuyên biệt):** 4–6 KPIs per department
3. Map KPIs to correct perspective (mostly Process + Foundation)
4. Add wellbeing KPIs for ALL team sizes:
   - Micro: sick days, retention rate (practical proxies)
   - SME: eNPS, engagement pulse, benefits utilization
5. Recalculate capacity allocation — warn if back-office person >100%

**Capacity warning for micro-teams:**
"[Person] kiêm nhiệm [N] functions. Chỉ nên có tối đa 3–5 KPIs tổng.
Ưu tiên KPIs có tác động cao nhất đến operational stability."

**Lock:** Back-office KPIs + wellbeing KPIs added to Resource Loading Matrix.
**Save:** Append to `bsc-data/objectives-kpis.md` — back-office + wellbeing KPIs

## Step 12b — 4D Mix Analysis (Optional)

Based on Mike Michalowicz's Clockwork framework: Do, Decide, Delegate, Design.

**Ask user:** "Bạn có muốn phân tích 4D Mix (Do-Decide-Delegate-Design) cho từng vai trò?
Giúp xác định CEO đang làm đúng tầm hay đang quá tải với tác vụ cấp dưới."

**If user declines:** Skip to Step 12c (Execution Planning) or Step 13 (Export).

**If user accepts:**

Read `references/4d-mix-framework.md` for benchmarks and format.

**AI does:**
1. Tag each KPI with primary D category based on the nature of work required
2. Calculate current 4D split per person from KPI allocation weights
3. Compare vs role benchmarks (from reference file)
4. Generate **quarterly transition roadmap** from current → ideal ratio
   - Current state = actual D distribution from Step 12
   - Q2/Q3/Q4 targets = gradual shift toward ideal
   - Each quarter: specific KPIs to delegate/redesign + enablers needed
5. Flag critical misalignments with specific recommendations

**Present:**
- Per-person 4D current vs ideal table
- Quarterly transition roadmap with specific actions per quarter
- Enablers needed (hiring, AI SOP, delegation training, etc.)

**Ask user:** Confirm roadmap is realistic given team constraints.

**Lock:** 4D Mix Analysis + Quarterly Transition Roadmap.
**Save:** `bsc-data/resource-loading.md` — 4D Mix analysis, quarterly transition roadmap
