# Knowledge Base Templates

Reference file for initializing `bsc-data/` folder. Read during Init Flow.

## A. INDEX.md Template

```markdown
# BSC Knowledge Base - {Company Name}
Last updated: {YYYY-MM-DD}
Current step: 0 (Kickoff)
Phase: 1 (Deep Discovery)

## Sections
| # | Section | Status | File | Summary |
|---|---------|--------|------|---------|
| 0 | Company Profile | ❌ | - | - |
| 0b | Vision Roadmap | ❌ | - | - |
| 1 | Products/Services | ❌ | - | - |
| 2 | Track Record & Team | ❌ | - | - |
| 3 | Competitors | ❌ | - | - |
| 3b | Perception Survey | ❌ | - | - |
| 4-5 | Reality Check | ❌ | - | - |
| 6 | CSF Analysis | ❌ | - | - |
| 7 | PESTEL | ❌ | - | - |
| 8 | SWOT | ❌ | - | - |
| 9-10 | TOWS & Strategy | ❌ | - | - |
| 11-12 | Objectives & KPIs | ❌ | - | - |
| 12b | Resource Loading | ❌ | - | - |

## Notes
- Initialized: {date}
```

## B. Detail File Frontmatter

```yaml
---
step: {number}
name: {step name}
status: locked
locked_at: {YYYY-MM-DD HH:mm}
revised_at: null
---
```

Content below frontmatter = structured summary matching the LOCKED BLOCK format.

## C. Init Checklist

1. Create `./bsc-data/` directory
2. Ask user: "Bạn muốn git-track BSC data không? (có thể .gitignore sau)"
3. Write INDEX.md from template above (fill company name from Step 0)
4. If user chose no git-track: create `./bsc-data/.gitignore` with `*`
5. Write first detail file (company-profile.md)

## D. INDEX Update Procedure

After writing/updating a detail file:
1. Update row: status → ✅ (or ⏳ if draft), file → filename, summary → 1-line
2. Update "Current step" and "Phase" header fields
3. Update "Last updated" date
4. Notify: "💾 Đã lưu Step {N} → bsc-data/{filename}.md"
