# Resource Loading Matrix Format

After KPIs and Initiatives defined, AI MUST generate a Capacity Loading Matrix.

## Format

```
CEO (100% capacity available)
├── KPI: Doanh thu luy ke          → 25%
├── KPI: So hop dong moi           → 20%
├── KPI: App published             → 20%
├── KPI: Partner certified         → 10%
├── KPI: CEO strategic time        → 15%
├── Delivery operations            → 10%
└── TOTAL ALLOCATED                → 100% Balanced

Marketing (100% capacity available)
├── KPI: Qualified leads           → 40%
├── KPI: Content published         → 30%
├── KPI: Brand awareness           → 20%
├── Support other KPIs             → 10%
└── TOTAL ALLOCATED                → 100% Balanced
```

## Assessment Thresholds

- **100% or less** (Balanced): Capacity properly allocated
- **100–120%** (Stretched): Feasible short-term, not sustainable
- **Over 120%** (Overloaded): Must delegate KPIs or defer initiatives

## Overload Handling

If anyone exceeds 120%, AI MUST flag prominently:
"[Person] is allocated [X%] capacity across [N] KPIs. This exceeds sustainable load.
Recommend: delegate [specific KPIs] to [whom], or defer [which initiatives] to later quarter."

For micro-enterprises where CEO handles multiple roles, proactively
suggest which KPIs to delegate FIRST as team grows.
