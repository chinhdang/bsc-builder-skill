# Back-Office KPI Templates

Scale-aware KPI library for back-office functions.
Select KPIs based on company size and role structure.

**Usage rules:**
- **Micro (≤15 people, kiêm nhiệm):** Max 3–5 KPIs total per person across ALL functions
- **SME (15–50, chuyên biệt):** 4–6 KPIs per department
- Map KPIs to correct BSC perspective (column "Persp.")
- Warn if back-office person capacity >100%

---

## Kế toán / Finance Ops

| KPI | Unit | Freq | Micro | SME | Persp. |
|-----|------|------|-------|-----|--------|
| Báo cáo thuế đúng hạn | Y/N or % on-time | Quarterly | ✅ | ✅ | Process |
| Cash flow forecast accuracy | Variance % | Monthly | ✅ | ✅ | Financial |
| Monthly close cycle time | Days | Monthly | — | ✅ | Process |
| DSO (Days Sales Outstanding) | Days | Monthly | — | ✅ | Financial |
| Accounts receivable aging | % > 90 days | Monthly | — | ✅ | Financial |
| Audit findings / year | Count | Yearly | — | ✅ | Process |

## HR / Nhân sự

| KPI | Unit | Freq | Micro | SME | Persp. |
|-----|------|------|-------|-----|--------|
| Tuyển đúng timeline | Y/N or % on-time | Per hire | ✅ | ✅ | Process |
| Onboarding completion rate | % | Per hire | ✅ | ✅ | Foundation |
| Employee turnover rate | % annual | Yearly | — | ✅ | Foundation |
| Training hours / person | Hours/quarter | Quarterly | — | ✅ | Foundation |
| Payroll accuracy | Error count or % | Monthly | ✅ | ✅ | Process |

## Pháp lý / Legal

| KPI | Unit | Freq | Micro | SME | Persp. |
|-----|------|------|-------|-----|--------|
| Contract review turnaround | Days | Per contract | ✅ | ✅ | Process |
| Compliance checklist completion | % | Quarterly | ✅ | ✅ | Process |
| Legal dispute count | Count | Yearly | — | ✅ | Process |
| License/permit renewal on-time | Y/N or % | Per event | ✅ | ✅ | Process |

## Admin / Hành chính

| KPI | Unit | Freq | Micro | SME | Persp. |
|-----|------|------|-------|-----|--------|
| Vendor payment on-time rate | % | Monthly | ✅ | ✅ | Process |
| Office ops uptime | % | Monthly | — | ✅ | Process |
| Procurement cost savings | % vs budget | Quarterly | — | ✅ | Financial |
| Facility satisfaction score | Survey score | Quarterly | — | ✅ | Foundation |

## Employee Wellbeing

| KPI | Unit | Freq | Micro | SME | Persp. |
|-----|------|------|-------|-----|--------|
| Sick days / person / quarter | Count | Quarterly | ✅ | ✅ | Foundation |
| Employee retention rate | % | Yearly | ✅ | ✅ | Foundation |
| Engagement pulse score | eNPS or 1-10 | Quarterly | — | ✅ | Foundation |
| Benefits utilization rate | % | Quarterly | — | ✅ | Foundation |
| Work-life balance index | Survey | Quarterly | — | ✅ | Foundation |
| Burnout risk indicator | Proxy metrics | Monthly | — | ✅ | Foundation |

---

## Capacity Guidelines

**Micro-team warning template:**
> "[Person] kiêm nhiệm [N] functions. Chỉ nên có tối đa 3–5 KPIs tổng.
> Ưu tiên KPIs có tác động cao nhất đến operational stability."

**Perspective mapping summary:**
- **Process:** Operational efficiency (turnaround, accuracy, compliance)
- **Foundation:** People development, wellbeing, engagement
- **Financial:** Only cost-related (DSO, cash flow, procurement savings)
- **Customer:** Rarely — only if measuring internal customer satisfaction

**Wellbeing proxy guidance for small teams (N<10):**
- eNPS meaningless with N=5 → use sick days + retention as practical proxies
- Skip survey-based KPIs → use observable metrics (turnover, absenteeism)
