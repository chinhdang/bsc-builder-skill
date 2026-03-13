# Phase 4: Compilation & Export (Step 13)

## Step 13 — Final Assembly

**AI does:**
1. Read ALL `bsc-data/*.md` files to gather full analytical context from each step
2. Compile deliverables (see structure below)
3. **4D Mix Analysis** (if Step 12b was completed) — include in BSC Plan + DOCX

**Save:** Update INDEX.md — all rows, Current step → 13, Phase → 4 (Export), Last updated → today.

**Ask user:** Final review → export.

---

## Quy tắc trình bày chung (áp dụng toàn bộ báo cáo)

### Ngôn ngữ
- **100% tiếng Việt.** KHÔNG trộn Anh-Việt trong cùng heading hoặc câu.
- Sai: "PHÂN TÍCH THỊ TRƯỜNG — MARKET ANALYSIS" | Đúng: "PHÂN TÍCH THỊ TRƯỜNG & THỰC TẾ"
- Thuật ngữ chuyên ngành giữ nguyên tiếng Anh NẾU không có tương đương phổ biến: BSC, KPI, SWOT, PESTEL, NPS, MRR, SaaS. Khi dùng lần đầu, ghi kèm giải thích tiếng Việt trong ngoặc.

### Mỗi mục (section) BẮT BUỘC có phần mở đầu
Ngay sau heading, trước khi vào nội dung chi tiết, viết 2-4 câu **mở đầu bối cảnh** trả lời:
1. Phần này **là gì** — nội dung chính sẽ trình bày
2. **Tại sao** thực hiện — vai trò trong chuỗi nhân quả tổng thể
3. **Tầm quan trọng** — nếu bỏ phần này, kế hoạch thiếu gì?

**Ví dụ:**
> Phần này phân tích bức tranh toàn cảnh thị trường chuyển đổi số SME Việt Nam — quy mô, tốc độ tăng trưởng, đối thủ, và những rủi ro chưa được nhận diện. Đây là nền tảng thực tế để hiệu chỉnh các giả định chiến lược: nếu thị trường không đúng như kỳ vọng, mọi mục tiêu phía sau đều cần điều chỉnh.

### Định dạng Key Insight / Nhận định quan trọng
Không viết raw text thuần. Sử dụng:
- **In đậm** cho từ/cụm từ trọng tâm
- *In nghiêng* cho nhận định, bình luận
- Callout box (trong DOCX) hoặc blockquote `>` (trong Markdown) cho insight nổi bật
- Màu sắc (DOCX): text nhấn mạnh dùng **xanh đậm** (#1F4E79), cảnh báo dùng **đỏ**

**Ví dụ Markdown:**
```
> **Nhận định:** *Thị trường CĐS cho SME VN đang ở giai đoạn "switching market" —
> 55% người dùng CRM không hài lòng. Đây là cơ hội hiếm có cho giải pháp mới,
> nhưng cũng đồng nghĩa rào cản chuyển đổi thấp — khách hàng dễ đến, dễ đi.*
```

### Nội dung trong bảng (table)
- **Xuống dòng** cho từng ý khác nhau trong cùng 1 ô — tạo điểm ngắt cho mắt reader
- Sai: "Chi phí quảng cáo, Đơn hàng từ ads, ROAS, CPC trung bình"
- Đúng:
  ```
  • Chi phí quảng cáo
  • Đơn hàng từ ads
  • ROAS
  • CPC trung bình
  ```
- Trong DOCX: dùng `\n` hoặc `cell.add_paragraph()` cho mỗi ý

### Diễn giải insight cho CEO/BoD
Sau mỗi bảng số liệu (objectives, KPIs, resource loading...), BẮT BUỘC có:
- **Insight box** giải thích ý nghĩa các con số trong bối cảnh doanh nghiệp
- Không chỉ liệt kê "F1: Doanh thu 2.4 tỷ" — mà phải giải thích TẠI SAO 2.4 tỷ, dựa trên giả định nào, rủi ro gì nếu không đạt

**Ví dụ:**
> **Ý nghĩa:** Mục tiêu 2.4 tỷ dựa trên giả định 4-7 deals/tháng × 30-50M/deal từ Q2.
> Với pipeline hiện tại gần như zero, Q1 phải đặt nền tảng lead gen để Q2 có deal.
> *Nếu Q1 thất bại trong việc tạo pipeline, mục tiêu Q2+ sẽ bất khả thi.*

### Dẫn nguồn nghiên cứu
- Mọi số liệu thị trường, benchmark PHẢI có nguồn trích dẫn
- Format: `(Nguồn: [tên báo cáo/tổ chức], [năm])`
- Nếu từ research reports nội bộ: `(Xem chi tiết: plans/reports/[filename])`
- Cuối báo cáo: phần "Nguồn tham khảo" liệt kê đầy đủ

### Kế hoạch theo năm tài chính — Tính toán quý còn lại
**AI PHẢI:**
1. Hỏi user năm tài chính: "Năm tài chính của bạn bắt đầu từ tháng mấy? (mặc định: tháng 1)"
2. Tính số quý còn lại từ thời điểm hiện tại đến cuối năm tài chính
3. Phân bổ mục tiêu cho TOÀN BỘ quý còn lại, không cố định Q1-Q3

**Ví dụ:** Nếu bây giờ là tháng 3/2026, năm tài chính Jan-Dec:
- Q1 (Jan-Mar) sắp kết thúc → chỉ còn Q2, Q3, Q4
- Bảng mục tiêu phải có CỘT cho Q2, Q3, Q4 (3 quý)
- Nếu bắt đầu giữa Q1 → Q1 có thể là "partial quarter" với mục tiêu điều chỉnh

**Ví dụ:** Nếu năm tài chính Apr-Mar:
- Tháng 3/2026 = cuối năm tài chính cũ → kế hoạch mới bắt đầu từ Q1 (Apr-Jun)
- Bảng có Q1, Q2, Q3, Q4 đầy đủ

---

## Kế hoạch chiến lược BSC — Cấu trúc tài liệu

Tài liệu chiến lược BSC (Markdown) là sản phẩm CHÍNH. Phải là **tài liệu tự giải thích** — bất kỳ ai đọc đều hiểu được MÀ KHÔNG cần tham gia quá trình xây dựng.

**Nguyên tắc:** Mỗi chỉ số, đánh giá, hay quyết định PHẢI có phần giải thích **TẠI SAO**. Bảng biểu tóm tắt; phần diễn giải giải thích lý do.

### Các mục bắt buộc (theo thứ tự):

#### 1. TÓM TẮT ĐIỀU HÀNH (tối đa 1 trang)
**Mở đầu:** Tổng quan toàn bộ kế hoạch trong 1 trang — giúp lãnh đạo nắm bắt nhanh trước khi đọc chi tiết.

Nội dung:
- Tổng quan công ty (tên, ngành, giai đoạn, quy mô team)
- Thách thức cốt lõi — 1-2 vấn đề sống còn mà kế hoạch này giải quyết
- Luận điểm chiến lược: 2-3 chiến lược cốt lõi, mỗi chiến lược 1 câu
- Mục tiêu trọng yếu: doanh thu, MRR, cột mốc quan trọng
- Điểm liên kết tầm nhìn (Vision Alignment Score)

#### 2. BẢNG TỔNG HỢP CHỈ SỐ
Bảng tra cứu nhanh: Mục tiêu doanh thu, Số chiến lược, Số mục tiêu, Số KPI, Số sáng kiến, Ngân sách, Team, Trạng thái phân bổ nguồn lực, Trạng thái 4D, Điểm liên kết tầm nhìn.

#### 3. HỒ SƠ DOANH NGHIỆP
**Mở đầu:** Bức tranh tổng thể về doanh nghiệp — nền tảng để hiểu mọi quyết định chiến lược phía sau.

Từ Step 0. Bao gồm: tên pháp nhân, ngành, giai đoạn, danh sách team với vai trò, doanh thu hiện tại, mục tiêu doanh thu.

#### 4. TẦM NHÌN & SỨ MỆNH
**Mở đầu:** Tầm nhìn và sứ mệnh là "bộ lọc" cho mọi quyết định chiến lược — mọi mục tiêu, KPI, sáng kiến đều phải phục vụ tầm nhìn này.

- Tuyên bố tầm nhìn + Tuyên bố sứ mệnh
- **Cột mốc tầm nhìn** (Năm 1 → Năm 3 → Năm 5+) kèm lý do cho từng giai đoạn
- **Kiểm tra sứ mệnh** — 3 câu hỏi nhị phân để đánh giá mỗi chiến lược có phục vụ sứ mệnh không

#### 5. SẢN PHẨM & DỊCH VỤ
**Mở đầu:** Hiểu danh mục sản phẩm/dịch vụ và thế mạnh cạnh tranh — nền tảng để đánh giá chiến lược nào khả thi với năng lực hiện có.

Từ Step 1. Bao gồm: sản phẩm/dịch vụ kèm % đóng góp doanh thu, USP, lợi thế cạnh tranh, chân dung khách hàng mục tiêu (ICP).

#### 6. PHÂN TÍCH THỊ TRƯỜNG & THỰC TẾ
**Mở đầu:** Phần này đối chiếu nhận thức chủ quan của doanh nghiệp với dữ liệu thị trường khách quan. Nếu thực tế khác xa kỳ vọng, toàn bộ chiến lược cần hiệu chỉnh — đây là bước "chẩn đoán" trước khi "kê toa".

**Đây là phần DIỄN GIẢI, không chỉ bảng số liệu.**

Từ Steps 4-5 (Reality Check). Bao gồm:
- **Bối cảnh thị trường:** Quy mô, tốc độ tăng trưởng, xu hướng chính — kèm trích nguồn `(Nguồn: ..., năm)`
- **Vị thế cạnh tranh:** Doanh nghiệp đang dẫn/theo sau/điểm mù ở đâu — phân tích đối thủ cụ thể
- **Rủi ro trọng yếu:** Top 3-5 rủi ro kèm đánh giá mức độ nghiêm trọng và cách ứng phó
- **Khoảng cách nhận thức vs thực tế:** Nơi nhận thức ban đầu của user (khảo sát Step 3b) khác biệt so với nghiên cứu. Format: "Doanh nghiệp đánh giá [X] ở mức [rating]. Nghiên cứu cho thấy [bằng chứng]. Khoảng cách: [đánh giá]."
- **Nhận định tổng hợp:** 2-3 đoạn văn giải thích những phát hiện quan trọng nhất đã định hình quyết định chiến lược
- **Nguồn nghiên cứu:** Dẫn link đến các báo cáo chi tiết `(Xem chi tiết: plans/reports/[filename])`

#### 7. MA TRẬN SWOT
**Mở đầu:** SWOT tổng hợp thế mạnh, điểm yếu nội tại cùng cơ hội, thách thức bên ngoài — là cơ sở trực tiếp để sinh ra các chiến lược ở mục 8.

Ma trận SWOT với các mục ưu tiên đánh dấu sao (★).

**Bắt buộc sau ma trận:**
- **Lý do xếp hạng** (1-2 câu cho mỗi mục đánh ★ giải thích TẠI SAO ưu tiên cao)
- **Nhận định SWOT:** 1 đoạn — quy luật/pattern gì nổi lên từ SWOT dẫn đến lựa chọn chiến lược?

#### 8. CHIẾN LƯỢC CỐT LÕI
**Mở đầu:** Từ hàng chục tổ hợp SWOT/TOWS, chỉ 2-3 chiến lược được chọn — đây là kết quả của việc đánh đổi và tập trung. Phần này giải thích TẠI SAO chọn những chiến lược này mà không phải các phương án khác.

Từ Steps 9-10. Với MỖI chiến lược (tối đa 2-3):

- **Tuyên bố chiến lược** (1 câu)
- **Loại hình:** Trực tiếp tạo doanh thu / Hỗ trợ / Phòng thủ
- **Gốc TOWS:** Tổ hợp S-O / W-O / S-T / W-T nào sinh ra chiến lược này
- **Lý do lựa chọn:** TẠI SAO chọn chiến lược này thay vì các phương án khác. Phương án nào đã cân nhắc và loại bỏ? Yếu tố quyết định là gì?
- **Liên kết tầm nhìn:** Phục vụ cột mốc Y1/Y3/Y5+ nào?
- **Kiểm tra sứ mệnh:** Đạt/không đạt từng câu kiểm tra
- **Phù hợp nguồn lực:** Team có đủ năng lực không? Thiếu hụt gì?

**Bắt buộc có:** Mục "Chiến lược KHÔNG được chọn" — liệt kê 2-3 chiến lược đã được sinh ra nhưng bị loại, kèm lý do.

#### 9. MỤC TIÊU CHIẾN LƯỢC (4 Góc nhìn)
**Mở đầu:** Mục tiêu chiến lược là cầu nối giữa chiến lược (ý tưởng) và KPI (đo lường). Được tổ chức theo 4 góc nhìn BSC: Tài chính → Khách hàng → Quy trình → Nền tảng, tạo thành chuỗi nhân quả từ dưới lên.

Từ Step 11. Bảng theo từng góc nhìn (Tài chính, Khách hàng, Quy trình, Nền tảng).

**Bắt buộc sau mỗi bảng góc nhìn:**
- **Diễn giải nhân quả:** 2-3 câu giải thích các mục tiêu ở góc nhìn này **tác động lên góc nhìn phía trên như thế nào**
- **Ghi chú hiệu chỉnh:** Chỉ tiêu nào đã điều chỉnh so với ước tính ban đầu và tại sao
- **Insight box:** Giải thích ý nghĩa con số trong bối cảnh doanh nghiệp

**Bắt buộc sau tất cả 4 bảng:**
- **Bảng truy vết:** Mục tiêu → Chiến lược → Cột mốc tầm nhìn (chuỗi đầy đủ)
- **Kiểm tra mục tiêu mồ côi:** Mục tiêu nào không liên kết rõ ràng đến tầm nhìn (mong đợi = 0)

#### 10. CHỈ SỐ ĐO LƯỜNG (KPI)
**Mở đầu:** KPI là "nhiệt kế" đo tiến độ từng mục tiêu. Mỗi KPI có chủ sở hữu rõ ràng và phân biệt chỉ số dẫn dắt (leading — dự báo tương lai) với chỉ số kết quả (lagging — đo đầu ra).

Từ Step 12. Bảng theo góc nhìn: tên KPI, loại (dẫn dắt/kết quả), baseline, mục tiêu theo quý, chủ sở hữu, đóng góp.

**Bắt buộc sau bảng KPI:**
- **Bối cảnh benchmark:** Với các KPI chính, ghi benchmark ngành và so sánh chỉ tiêu `(Nguồn: ...)`
- **Cờ ước tính:** Baseline nào là ước tính vs dữ liệu thực? Chỉ tiêu nào cần xác nhận thêm?
- **Insight box:** Giải thích logic đằng sau con số — tại sao chỉ tiêu này, dựa trên giả định nào

#### 11. BẢN ĐỒ CHUỖI NHÂN QUẢ
**Mở đầu:** Đây là "xương sống" của BSC — cho thấy các KPI không đứng riêng lẻ mà liên kết nhân quả: cải thiện ở Nền tảng → tác động Quy trình → tác động Khách hàng → tác động Tài chính. Nếu chuỗi nào đứt gãy, ta biết KPI đó có thể là "số liệu ảo".

Bảng: Chuỗi # | Nền tảng (Dẫn dắt) → Quy trình → Khách hàng → Tài chính (Kết quả).

**Bắt buộc sau bản đồ:**
- **Diễn giải giả thuyết nhân quả:** Với mỗi chuỗi, 2-3 câu: "Nếu [KPI dẫn dắt] cải thiện → [cơ chế] → [KPI kết quả] cải thiện vì [lý do]."
- **Cách kiểm chứng:** Team sẽ kiểm tra chuỗi nhân quả này đúng hay sai bằng cách nào?
- **Cảnh báo:** KPI mồ côi (không có liên kết lên/xuống), chuỗi đứt gãy

#### 12. SÁNG KIẾN TRIỂN KHAI
**Mở đầu:** Sáng kiến là các dự án cụ thể để hiện thực hóa mục tiêu — chuyển từ "muốn đạt gì" sang "làm gì để đạt". Mỗi sáng kiến gắn với mục tiêu, có timeline, ngân sách, và ưu tiên rõ ràng.

Bảng: Tên sáng kiến, mục tiêu liên kết, ưu tiên, timeline, ngân sách, cột mốc.

**Bắt buộc:** Diễn giải lý do xếp hạng ưu tiên (tại sao P0 vs P1).

#### 13. PHÂN BỔ NGUỒN LỰC
**Mở đầu:** Phân bổ nguồn lực trả lời câu hỏi "Ai làm gì, bao nhiêu % thời gian?" — đảm bảo chiến lược không chỉ đúng mà còn THỰC HIỆN ĐƯỢC với đội ngũ hiện có.

Bảng theo người: vai trò, % phân bổ theo hoạt động, tổng, trạng thái.

**Bắt buộc:**
- **Cảnh báo quá tải:** Ai >100% và kế hoạch giảm tải
- **Sự phù hợp năng lực-chiến lược:** Phân bổ có khớp với ưu tiên chiến lược không? Lệch ở đâu?
- **Insight:** Nhận xét về rủi ro nhân sự, single-point-of-failure, kiêm nhiệm

#### 14. PHÂN TÍCH 4D (nếu hoàn thành)
**Mở đầu:** Phân tích 4D (Làm-Quyết định-Ủy quyền-Thiết kế) theo framework Clockwork cho thấy mỗi người đang phân bổ thời gian ở CẤP ĐỘ nào. CEO dành 45% thời gian "Làm" thay vì "Thiết kế" = doanh nghiệp phụ thuộc vào 1 người.

Từ Step 12b. Bảng tỷ lệ 4D hiện tại vs lý tưởng theo vai trò. Lộ trình chuyển đổi theo quý.

**Bắt buộc:**
- **Diễn giải lệch hướng:** Vai trò nào đang làm việc dưới tầm? Lộ trình sửa chữa là gì?
- **Điều kiện hỗ trợ:** Cần gì (tuyển dụng, AI, SOP, ủy quyền) để chuyển đổi thành công?

#### 15. LỘ TRÌNH TRIỂN KHAI (nếu Step 12c hoàn thành)
**Mở đầu:** Chuyển kế hoạch quý thành hành động tháng/tuần cụ thể — từ "mục tiêu" sang "lịch làm việc" cho từng người.

Phân tích theo quý kèm cột mốc tháng, checklist, mục tiêu doanh thu.

**Lưu ý:** Số quý phải khớp với tính toán năm tài chính (xem quy tắc ở trên).

#### 16. ĐÁNH GIÁ LIÊN KẾT TẦM NHÌN
**Mở đầu:** Bước cuối cùng — đánh giá xem toàn bộ kế hoạch có thực sự phục vụ tầm nhìn hay chỉ là tập hợp các mục tiêu rời rạc.

Kiểm tra:
- % mục tiêu truy vết được đến cột mốc tầm nhìn
- Tỷ lệ đạt kiểm tra sứ mệnh theo chiến lược
- Điểm mù: Cột mốc tầm nhìn nào không có chiến lược hỗ trợ
- Đánh giá sử dụng nguồn lực
- Xếp hạng tổng thể: Mạnh (≥80%) / Trung bình (50-79%) / Yếu (<50%)

**Bắt buộc:** 1 đoạn nhận định về tính nhất quán tổng thể — điểm mạnh và lỗ hổng đã biết.

### PHỤ LỤC
- **Nguồn tham khảo:** Danh sách đầy đủ các nghiên cứu, báo cáo, nguồn dữ liệu đã sử dụng
  - Link đến research reports: `plans/reports/[filename]`
  - Nguồn bên ngoài: tên tổ chức, năm, URL (nếu có)
- Tham chiếu file dữ liệu BSC
- Ghi chú phương pháp: "Xây dựng theo phương pháp luận BSC với phân tích cộng tác AI-chuyên gia"

---

## Các sản phẩm khác

### Báo cáo Thực tế (Reality Check Report - Markdown)
File riêng — toàn bộ Reality Check từ Steps 4-5. Export nguyên trạng từ `bsc-data/reality-check.md`.

### JSON Export
Tuân thủ schema. Chỉ dữ liệu, không có diễn giải.

### DOCX Export

**Hỏi user:** "Bạn muốn xuất file DOCX chuyên nghiệp không?"

**Nếu đồng ý:**

**AI thực hiện:**
1. Đọc `references/docx-export-script.py` để sử dụng thư viện component
2. Populate dict `DATA` với nội dung thực từ `bsc-data/*.md`
3. Chạy script: `python3 references/docx-export-script.py`
4. Thông báo: "📄 Đã xuất DOCX → bsc-data/BSC-Strategic-Plan-{Company}.docx"

**Script cung cấp** (chất lượng DOCX chuyên nghiệp):
- Trang bìa: tiêu đề 28pt bold xanh đậm, phụ đề, metadata
- Callout box: bảng 1 ô nền xanh nhạt (#DEEAF1) — dùng cho Key Insight
- Feature card có số thứ tự: badge xanh + mô tả nền xanh nhạt
- Bảng dữ liệu: header row xanh đậm (#1F4E79), chữ trắng, hàng xen kẽ
- Ma trận SWOT: lưới 2x2 với 4 màu quadrant
- Bảng so sánh Trước/Sau: nền đỏ nhạt / xanh lá nhạt
- Bảng KPI, bản đồ nhân quả, phân bổ nguồn lực, 4D Mix
- Hỗ trợ hình ảnh kèm chú thích nghiêng xám
- Bảng màu: Xanh đậm (#1F4E79), Xanh vừa (#2E75B6), Xám (#595959)
- Font: Calibri 10pt body, heading H1-H3 styled
- Trang A4, margins 2cm

**Lưu ý DOCX:**
- Nội dung ô bảng: sử dụng `cell.add_paragraph()` cho mỗi ý → xuống dòng rõ ràng
- Key Insight: dùng `add_callout_box()` — nền xanh nhạt, chữ đậm/nghiêng
- Phần mở đầu section: dùng paragraph style italic hoặc color gray để phân biệt với body text

**Dependency:** `pip install python-docx`
