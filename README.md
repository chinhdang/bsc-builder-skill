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

## Sử dụng trên các AI platform khác

Ngoài Claude Code, bạn có thể dùng skill này trên **bất kỳ AI platform nào** (Claude Chat, Gemini, ChatGPT, v.v.) bằng file tổng hợp:

1. Download file [`bsc-builder-full.md`](bsc-builder-full.md) (60KB, 1 file duy nhất)
2. Upload vào conversation hoặc paste nội dung
3. Prompt: *"Hãy đóng vai BSC consultant theo hướng dẫn trong file. Bắt đầu từ Step 0."*

| Platform | Cách dùng |
|----------|-----------|
| **Claude Code CLI** | `/bsc-builder` — tự động load |
| **AntiGravity** | Tự detect từ SKILL.md — hỏi agent dùng skill |
| **Claude Chat** | Upload `bsc-builder-full.md` → prompt bắt đầu |
| **Gemini** | Upload file hoặc paste content |
| **ChatGPT** | Upload file, hoặc tạo Custom GPT với file làm knowledge |

## Cài đặt cho AntiGravity (Google)

```bash
git clone https://github.com/chinhdang/bsc-builder-skill.git ~/.gemini/antigravity/skills/bsc-builder
```

Hoặc workspace-level:
```bash
git clone https://github.com/chinhdang/bsc-builder-skill.git .agents/skills/bsc-builder
```

AntiGravity tự detect skill từ `SKILL.md` — không cần config thêm.

## Yêu cầu

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code), hoặc
- [AntiGravity](https://antigravity.google) (Google), hoặc
- Bất kỳ AI chat nào hỗ trợ file upload (dùng `bsc-builder-full.md`)

## Giấy phép

MIT

---

# BSC Builder Skill for Claude Code

Interactive BSC (Balanced Scorecard) strategic plan builder for SMEs. 4 phases, 17 steps — from business discovery to complete strategy export.

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
git clone https://github.com/chinhdang/bsc-builder-skill.git ~/.claude/skills/bsc-builder
```

## Usage

In Claude Code CLI:

```
/bsc-builder
```

## Install for AntiGravity (Google)

```bash
git clone https://github.com/chinhdang/bsc-builder-skill.git ~/.gemini/antigravity/skills/bsc-builder
```

## Use on other AI platforms

Download [`bsc-builder-full.md`](bsc-builder-full.md) (60KB single file) and upload to any AI chat (Claude Chat, Gemini, ChatGPT). Prompt: *"Act as a BSC consultant following the guide in this file. Start from Step 0."*

## Requirements

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code), or
- [AntiGravity](https://antigravity.google) (Google), or
- Any AI chat with file upload support (use `bsc-builder-full.md`)

## License

MIT
