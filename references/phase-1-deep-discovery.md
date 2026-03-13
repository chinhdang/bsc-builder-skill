# Phase 1: Deep Discovery (Steps 0–3)

Purpose: Understand the business deeply from the inside. 3–5 questions per turn.

## Step 0 — Kickoff & Company Profile

**AI does:**
- Introduce as BSC strategic planning consultant
- Explain the 4-phase process briefly
- Set expectations: "I will research your market deeply and give you an honest, possibly
  uncomfortable assessment before we build strategy. Accurate diagnosis is the foundation
  of good strategy. Sai mot ly, di mot dam."

**Ask user:**
1. Company name, industry, current stage (seed / startup / growth / mature)
2. Team size, strategic planning period (1 year or 3 years?)
3. Mission and vision (if already defined)
4. Business model: How do you make money?
5. Revenue: current annual → target. Planning horizon.

**After user provides Mission & Vision, AI does:**
- Decompose Vision into 2–3 phase milestones:
  - Y1 (current period): measurable, observable outcomes
  - Y3: high-level directional milestone
  - Y5+: aspirational north star
- Decompose Mission into 2–3 **Mission Tests** — simple yes/no filters:
  - Extract core purpose words from Mission statement
  - Each test = "Does [action/strategy] serve [core purpose word]?"
  - Example: Mission "Giúp SME VN quản trị hiệu quả"
    → Test 1: "Phục vụ SME?" / Test 2: "Cải thiện quản trị?"
- If user has no formal V/M, AI helps draft one first using discovery data

**Present:** Company Profile + Draft Vision Milestones + Mission Tests.
**Ask user:** "Các milestone và mission test này có đúng ý bạn không?"

**Lock:** Company Profile Card + Vision Milestones + Mission Tests.
**Save:** `bsc-data/company-profile.md` — company info, business model, revenue, mission, vision, mission tests

## Step 1 — Product/Service Deep Dive

**Ask user:**
1. List each product/service: description, target customer, pricing model, % of total revenue
2. USP per product — why do customers choose YOU over alternatives?
3. Overall company USP — what makes you different in the market?
4. Unfair advantage — what do you have that competitors CANNOT easily copy in 1–2 years?
5. Target customer segments: Who is your ICP (Ideal Customer Profile)?

**Lock:** Product/Service Map + USP Statements + Unfair Advantages + ICP.
**Save:** `bsc-data/products-services.md` — product/service list, USP, unfair advantages, ICP

## Step 2 — Track Record & Current Reality

**Ask user:**
1. Notable achievements: case studies, marquee clients, growth metrics, awards
2. Revenue breakdown: % by service/product, % by client, % by segment
3. Average deal value? Average sales cycle length?
4. Top 3 pain points RIGHT NOW — where is the business most "stuck"?
5. Available budget for the strategic period?
6. **Team & Organization Structure:**
   - List departments/roles currently active (e.g., Sales, Dev, Marketing, Back-office)
   - Number of people per department/role
   - Key responsibilities of each person/role
   - Who is bottleneck? Who is underutilized?
   - Any outsourced/part-time roles?

**Lock:** Evidence Summary + Revenue Structure + Pain Points + Budget + **Team Map**
(name, role, key responsibilities, current capacity estimate, skills).
Team Map will be used directly in Step 12 for KPI ownership & resource loading.
**Save:** `bsc-data/track-record.md` — achievements, revenue breakdown, pain points, budget, team map

## Step 3 — Competitive Landscape (User Perspective)

**Ask user:**
1. Name 3–5 direct competitors + their strengths/weaknesses from YOUR perspective
2. In head-to-head pitches, where do you typically WIN? Where do you LOSE?
3. Any indirect competitors? (customers DIY, using Excel, doing nothing)

**Lock:** User's competitive perception (will be cross-checked in Phase 2).
**Save:** `bsc-data/competitors.md` — competitor list, win/lose analysis, indirect competitors
