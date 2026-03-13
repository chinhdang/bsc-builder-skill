# BSC Builder Skill cho Claude Code

Skill tương tác xây dựng kế hoạch chiến lược BSC (Balanced Scorecard) cho doanh nghiệp SME. 4 giai đoạn, 16 bước — từ khám phá doanh nghiệp đến xuất file chiến lược hoàn chỉnh.

## Tính năng

- Quy trình 4 giai đoạn: Discovery → Reality Check → Analysis & Strategy → Export
- Khảo sát nhận thức SWOT & PESTEL từ góc nhìn chủ quan của người dùng
- Nghiên cứu thị trường độc lập, đánh giá thực tế (Reality Check Report)
- Phân tích CSF, PESTEL, SWOT, TOWS — chiến lược tập trung 2-3 trọng tâm
- KPIs theo 4 góc nhìn BSC mở rộng + chuỗi nhân quả
- Resource Loading Matrix — phân bổ năng lực theo từng người
- 4D Mix Analysis (Do/Decide/Delegate/Design) theo framework Clockwork
- Execution Planning: milestone tháng, scorecard tuần, time-block
- Lưu trữ persistent qua file (`bsc-data/`) — tiếp tục giữa các session
- Hỗ trợ đa ngôn ngữ (tự động phát hiện)

## Cài đặt

```bash
# Copy vào thư mục skills của Claude Code
cp -r bsc-builder-skill/ ~/.claude/skills/bsc-builder/
```

## Sử dụng

Trong Claude Code CLI, gọi skill bằng lệnh:

```
/bsc-builder
```

Skill sẽ bắt đầu quy trình tương tác từng bước. Mỗi bước yêu cầu xác nhận từ người dùng trước khi tiếp tục.

## Cấu trúc

```
bsc-builder/
├── SKILL.md                          # Entry point chính
└── references/
    ├── 4d-mix-framework.md           # Framework 4D Mix (Clockwork)
    ├── backoffice-kpi-templates.md   # KPI mẫu cho back-office
    ├── edge-cases.md                 # Xử lý tình huống đặc biệt
    ├── knowledge-base-templates.md   # Template lưu trữ dữ liệu
    ├── perspective-framework.md      # 4 góc nhìn BSC mở rộng
    ├── phase-1-deep-discovery.md     # Giai đoạn 1: Khám phá sâu
    ├── phase-1b-user-perception-survey.md  # Khảo sát nhận thức
    ├── phase-1c-vision-roadmap.md    # Lộ trình tầm nhìn
    ├── phase-2-reality-check.md      # Giai đoạn 2: Đánh giá thực tế
    ├── phase-3-analysis-strategy.md  # Giai đoạn 3: Phân tích & chiến lược
    ├── phase-3-objectives-kpis.md    # Mục tiêu & KPIs
    ├── phase-3c-execution-planning.md # Kế hoạch thực thi
    ├── phase-4-export.md             # Giai đoạn 4: Xuất file
    ├── reality-check-report-structure.md  # Cấu trúc báo cáo thực tế
    ├── resource-loading-matrix.md    # Ma trận phân bổ nguồn lực
    └── standard-measures-catalog.md  # Danh mục thước đo chuẩn BSC
```

## Yêu cầu

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code)

## Giấy phép

MIT

---

# BSC Builder Skill for Claude Code

Interactive BSC (Balanced Scorecard) strategic plan builder for SMEs. 4 phases, 16 steps — from business discovery to complete strategy export.

## Features

- 4-phase process: Discovery → Reality Check → Analysis & Strategy → Export
- User perception survey for SWOT & PESTEL (subjective anchors)
- Independent market research with honest Reality Check Report
- CSF, PESTEL, SWOT, TOWS analysis — focused on 2-3 core strategies
- KPIs across 4 enriched BSC perspectives + causal chain mapping
- Resource Loading Matrix — capacity allocation per person
- 4D Mix Analysis (Do/Decide/Delegate/Design) based on Clockwork framework
- Execution Planning: monthly milestones, weekly scorecards, time-blocks
- Persistent storage via files (`bsc-data/`) — resume across sessions
- Multi-language support (auto-detect)

## Installation

```bash
# Copy to Claude Code skills directory
cp -r bsc-builder-skill/ ~/.claude/skills/bsc-builder/
```

## Usage

In Claude Code CLI, invoke the skill:

```
/bsc-builder
```

The skill runs an interactive step-by-step process. Each step requires user confirmation before proceeding.

## Structure

See the Vietnamese section above for the file tree.

## Requirements

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code)

## License

MIT
