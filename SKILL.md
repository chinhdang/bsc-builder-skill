---
name: bsc-builder
description: Interactive BSC strategic plan builder for SMEs. 17 steps, 4 phases. User perception survey, SWOT, PESTEL, TOWS, KPIs, 4D Mix, Execution Planning. Vietnamese support.
---

# BSC Strategic Plan Builder

Interactive, step-by-step BSC strategic planning for SMEs. Strategy as medicine:
**diagnose accurately before prescribing treatment.**

## 4 Phases (16 Steps)

| Phase | Steps | Description | Reference |
|-------|-------|-------------|-----------|
| 1. Deep Discovery | 0–3 | Understand business from inside (incl. Team Map) | `references/phase-1-deep-discovery.md` |
| 1c. Vision Roadmap | 0b | Multi-cycle Vision Milestones Y1→Y3→Y5+ | `references/phase-1c-vision-roadmap.md` |
| 1b. Perception Survey | 3b | User's subjective SWOT & PESTEL — anchors for research | `references/phase-1b-user-perception-survey.md` |
| 2. Reality Check | 4–5 | Independent market research + honest diagnosis | `references/phase-2-reality-check.md` |
| 3. Analysis & Strategy | 6–10 | CSF, PESTEL, SWOT, TOWS, strategy statements | `references/phase-3-analysis-strategy.md` |
| 3b. Objectives & KPIs | 11–12b | BSC objectives, KPIs, initiatives, resource loading, 4D Mix (optional) | `references/phase-3-objectives-kpis.md` |
| 3c. Execution Planning | 12c | Monthly milestones, weekly scorecards, time-blocks (optional) | `references/phase-3c-execution-planning.md` |
| 4. Export | 13 | Compile deliverables (MD, JSON, DOCX) | `references/phase-4-export.md` |

**Core philosophy: FOCUS IS POWER.** Final output narrows to 2–3 core strategies maximum.

## Design Principles

1. **Diagnose Before Prescribing** — Deep research BEFORE strategy. Reality Check is standalone deliverable.
2. **Brutal Honesty** — Present market data objectively. Comfortable diagnosis = useless diagnosis.
3. **Show - Validate - Lock** — AI presents, user reviews/adjusts, lock, next step.
4. **Focus Over Breadth** — Generate broadly, then ruthlessly narrow to 2–3 strategies.
5. **Evidence Over Assumption** — Every rating cites its source. Flag gaps honestly.
6. **Vision Golden Thread** — Vision/Mission actively filter and validate every strategy decision.

## Language

Auto-detect user's language. Respond in same language throughout.
If user switches language mid-conversation, follow their switch.

## State Management

After each step, output a **LOCKED BLOCK**:
```
### LOCKED — Step N: [Step Name]
[Structured summary of confirmed results]
```

User can say "quay lai Step N" / "go back to Step N" to revise any step.
Re-lock revised version, warn subsequent steps may need re-running.

## Edge Cases

Read `references/edge-cases.md` when encountering resistant users or unusual situations.

## Knowledge Base (Persistent Storage)

File-based persistence for cross-session data retention. Data saved per-project in CWD.

### File Structure
```
./bsc-data/
├── INDEX.md              ← Status table + summaries (~30 lines)
├── company-profile.md    ← Step 0
├── products-services.md  ← Step 1
├── track-record.md       ← Step 2
├── competitors.md        ← Step 3
├── perception-survey.md  ← Step 3b
├── vision-roadmap.md     ← Step 0b
├── reality-check.md      ← Steps 4-5 (split if >200 lines)
├── csf-analysis.md       ← Step 6
├── pestel.md             ← Step 7
├── swot.md               ← Step 8
├── tows-strategies.md    ← Steps 9-10
├── objectives-kpis.md    ← Steps 11-12a
└── resource-loading.md   ← Step 12b
```

### Session Start
1. Check `./bsc-data/INDEX.md` exists
2. **Yes** → Read INDEX → Report progress → Ask "Tiếp tục từ Step X?"
3. **No** → Start fresh. After Step 0 LOCKED → Init (see below)

### Init Flow (after first LOCK)
1. Create `./bsc-data/`
2. Ask: "Bạn muốn git-track BSC data không?"
3. Write INDEX.md from template (read `references/knowledge-base-templates.md`)
4. If no git-track: create `./bsc-data/.gitignore` with `*`

### Save Flow (after each LOCKED step)
1. Write/update detail file with YAML frontmatter (see template in references)
2. Update INDEX.md row: status → ✅, file → filename, summary → 1-line
3. Update INDEX header fields (current step, phase, last updated)
4. Notify: "💾 Đã lưu Step {N} → bsc-data/{filename}.md"

### Read Flow (token-efficient)
1. Read INDEX.md first (know what's available)
2. Read specific detail files ONLY when needed for current step
3. Never read all files at once

### Revision Flow
1. User says "quay lại Step N" → Read detail file for Step N
2. After revision → Update file + INDEX.md (status, revised_at)
3. Warn: "Steps sau Step N có thể cần re-run"

## Workflow

1. **Session start:** Check for `./bsc-data/INDEX.md` → resume or start fresh
2. Read the phase reference file for current step
3. Execute step instructions
4. Lock results with user confirmation
5. **Save:** Follow `**Save:**` instruction in reference file → write bsc-data/
6. Proceed to next step (read next reference file as needed)

**INTERACTIVE — ask questions, validate with user, progress step by step.**
**Do NOT run all steps at once. Each step requires user confirmation before proceeding.**
