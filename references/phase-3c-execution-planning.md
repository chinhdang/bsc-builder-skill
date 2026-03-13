# Phase 3c: Execution Planning (Step 12c)

## Step 12c — Goal Decomposition & Execution Cadence (Optional)

Bridges the gap between quarterly BSC plan and daily execution.
Combines best of EOS Rocks, 4DX Lead Measures, OKR Cascade, and Time-Block Allocation.

**Ask user:** "Bạn có muốn chẻ nhỏ mục tiêu quý thành kế hoạch tháng/tuần cụ thể không?
Giúp chuyển Resource Loading Matrix thành lịch làm việc thực tế cho từng người."

**If user declines:** Skip to Step 13 (Export).

**If user accepts:**

### Layer 1: Quarterly → Monthly Milestones

**AI does:**
1. Take each KPI's quarterly target, split into 3 monthly milestones
   - Not always equal — consider ramp-up, seasonality, dependencies
   - Format: "From [baseline] to [monthly target] by end of [month]"
2. Add 1-2 "Rocks" (key deliverables) per objective per month
   - Rock = concrete output, not a metric. E.g., "Launch proposal template" not "Increase win rate"
   - Each Rock has: owner, deadline, binary done/not-done
3. Present monthly roadmap table per person

**Template:**
```
[Person] — Month [N] Milestones
├── [Objective code]: [KPI] → target [X] (from [baseline])
│   ├── Rock: [Deliverable] — deadline [date]
│   └── Rock: [Deliverable] — deadline [date]
├── [Objective code]: [KPI] → target [Y]
│   └── Rock: [Deliverable] — deadline [date]
└── Capacity check: [X]% allocated this month
```

**Ask user:** Monthly milestones realistic? Any front-loading or back-loading needed?

### Layer 2: Monthly → Weekly Scorecard + Time-Blocks

**AI does:**
1. **Weekly Scorecard** — Define 3-5 lead measures per person
   - Lead measure = weekly activity that PREDICTS monthly KPI achievement
   - Format: "[Activity] ≥ [number]/tuần → drives [KPI]"
   - Examples:
     - "# cuộc gọi sale ≥ 5/tuần" → drives Revenue (F1)
     - "# proposals gửi ≥ 3/tuần" → drives Win Rate (C2)
     - "# bài content ≥ 1/tuần" → drives Lead Gen (C1)
     - "# SOPs hoàn thành ≥ 1/tuần" → drives Process Doc (L2)

2. **Time-Block Agenda** — Convert % allocation to calendar blocks
   - Formula: `% × total_hours/week = hours/week → ÷ block_size (2-3h) = blocks`
   - Group by energy type:
     - **Deep work** (strategy, content, development): morning blocks
     - **Interactive** (calls, meetings, demos): afternoon blocks
     - **Admin** (email, reporting, routine): end-of-day slots
   - Leave 10-20% buffer for unexpected work

**Template:**
```
[Person] — Weekly Time-Block Agenda ([total]h/tuần)
├── Mon AM: [Objective] ([X]h) — [specific activities]
├── Mon PM: [Objective] ([X]h) — [specific activities]
├── Tue AM: [Objective] ([X]h) — [specific activities]
├── ...
├── Fri PM: Buffer + Weekly Review (2h)
└── Total allocated: [X]h / [total]h ([X]%)
```

**Ask user:** Time-blocks fit your actual schedule? Any fixed commitments (meetings, classes) to work around?

### Layer 3: Weekly Execution Cadence

**AI does:**
Present recommended weekly ritual:

**Monday Kickoff (15 min, all team):**
1. Each person states 3-5 weekly commitments (binary: will do or won't)
2. Flag any blockers from last week
3. Quick scorecard review (numbers only, no discussion)

**Daily (optional, 10 min standup):**
- What I did yesterday (which objective?)
- What I'll do today (which time-block?)
- Any blockers?

**Friday Review (20 min, all team):**
1. Score weekly scorecard: each lead measure → hit/miss
2. Rock status: on-track / off-track / done
3. Flag issues for next week (EOS IDS: Identify → Discuss → Solve)

**Monthly Review (30 min):**
1. KPI actuals vs monthly milestones
2. Adjust next month's milestones if needed
3. Recalibrate time-blocks if % allocation shifted
4. Celebrate wins, diagnose misses

### Output Format

**AI generates for each person:**
1. Monthly Milestone Card (3 months)
2. Weekly Scorecard (3-5 lead measures with targets)
3. Weekly Time-Block Agenda (hour-by-hour)
4. Meeting Cadence Summary (Monday/Friday rituals)

**Lock:** Execution Plan — monthly milestones + weekly scorecards + time-blocks + cadence.
**Save:** `bsc-data/execution-plan.md` — full execution plan per person
