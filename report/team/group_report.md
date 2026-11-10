# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: **E305t108**
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): **Khi cần thực hiện thủ tục hành chính hoặc giải quyết vướng mắc học vụ tại trường, sinh viên gặp khó khăn khi tra cứu quy định rải rác và biểu mẫu phức tạp, dẫn đến tốn thời gian đi lại nhiều lần và làm quá tải cán bộ phòng ban.**
- Quyết định cuối: **Go, phạm vi nhỏ** (Pilot trên 5 thủ tục hành chính có tần suất phát sinh cao nhất).

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Đàm Hồng Thái | Khi cần xem lịch học/lịch thi/phòng học, tôi muốn tra cứu tại một nơi để không phải tìm nhiều kênh | SV, lớp trưởng | Hỏi & chờ lớp trưởng trả lời ~10 phút/lần | "Portal trường đã có lịch học, làm thêm AI có trùng lặp không?" (Lê Quý Toàn) |
| 2 | Đàm Hồng Thái | Khi tìm hiểu học bổng/tốt nghiệp, tôi muốn tổng hợp điều kiện/quyền lợi/hồ sơ từ nhiều nguồn | SV, phòng CTSV, phòng đào tạo | Đọc & đối chiếu ~40 phút/lần | "Tần suất 2–3 lần/năm thì khó đo trong một buổi lab?" (Lê Quý Toàn) |
| 3 | Đàm Hồng Thái | Khi các bạn hỏi lịch thi/hạn nộp, tôi muốn có nguồn chung để giảm trả lời lặp lại | Lớp trưởng, cán bộ lớp | Tìm thông báo gốc ~3 phút/câu × 8 câu | "Đây là pain của người trả lời hay người hỏi?" (Lê Quý Toàn) |
| 4 | Đàm Hồng Thái | Khi cần làm thủ tục hành chính, tôi muốn có hướng dẫn đầy đủ chính xác để không phải hỏi nhiều người | SV, lớp trưởng, cán bộ hành chính | Tự đọc quy chế ~45 phút/lần | "Sinh viên có thật sự đọc hết quy chế không?" (Lê Quý Toàn) |
| 5 | Lê Quý Toàn | Khi bắt đầu ca 8h, tôi muốn tổng hợp review 1–3 sao 24h qua để nhận diện cửa hàng gặp sự cố trước giao ban 9h | Ops Lead, Store Manager | Đọc & gõ tag thủ công 45 phút/sáng | "Lấy đâu ra dữ liệu review thật để test trong lab?" (Đàm Hồng Thái) |
| 6 | Lê Quý Toàn | Khi hết ca trực, tôi muốn tổng hợp sự cố chưa xử lý để bàn giao ca sau trong 10 phút | Trưởng ca | Gõ biên bản bàn giao 15–20 phút | "Trưởng ca có chịu ghi chép đầy đủ không?" (Đàm Hồng Thái) |
| 7 | Lê Quý Toàn | Khi khách khiếu nại đơn giao lỗi, tôi muốn đối chiếu bằng chứng để hoàn tiền trong 10 phút | Nhân viên CSKH, thủ kho | Chờ ảnh camera từ kho/bếp 15 phút | "Có rào cản phân quyền dữ liệu POS không?" (Đàm Hồng Thái) |
| 8 | Lê Quý Toàn | Khi cần xin giấy chứng nhận/hoãn thi, tôi muốn biết chính xác hồ sơ cần gì để không bị trả về | SV, cán bộ một cửa | Tự đọc quy chế + đi lại 2–3 lần | "Khác gì portal một cửa hiện có?" (Đàm Hồng Thái) |
| 9 | Đàm Hồng Thái | Khi gặp khó khăn học tập/cá nhân, tôi muốn biết nên liên hệ ai để được hỗ trợ kịp thời | SV gặp khó khăn, cố vấn | Tìm đầu mối 20–40 phút | "Có cần AI hay chỉ cần danh bạ rõ ràng?" (Lê Quý Toàn) |
| 10 | Lê Quý Toàn | Khi nhân viên mới vào ca, họ muốn biết chính sách đền bù chuẩn để phản hồi khách ngay | Nhân viên CSKH thử việc | Hỏi lặp lại 6–8 lần/ngày trên Zalo | "Có sẵn SOP rồi, sao không cải thiện SOP?" (Đàm Hồng Thái) |
| 11 | Đàm Hồng Thái | Khi gặp khó khăn làm bài/đồ án, tôi muốn tìm hướng giải quyết và tài liệu phù hợp để hoàn thành đúng hạn | SV, GV hướng dẫn | Tìm tài liệu 20–60 phút/lần | "Có phải vấn đề học vụ không?" (Lê Quý Toàn) |
| 12 | Lê Quý Toàn | Khi đối soát voucher đền bù cuối tháng, tôi muốn khớp số tiền với lý do khiếu nại để giám đốc phê duyệt | Trưởng CSKH, kế toán | Đối chiếu Excel 6–7 tiếng/tháng | "Có cần AI hay chỉ cần chuẩn hóa mã đơn?" (Đàm Hồng Thái) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | #1, #3, #4, #8, #9 | Tra cứu thông tin học vụ/thủ tục hành chính rải rác, phải hỏi lại nhiều người |
| B | #2, #5, #12 | Tổng hợp/đối soát nhiều nguồn để ra quyết định (học bổng, review, voucher) |
| C | #6, #7, #10, #11 | Phối hợp/handoff giữa các bên (bàn giao ca, chờ kho, hỏi SOP, hỗ trợ bài tập) |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian sinh viên tra cứu & giải quyết thủ tục hành chính học vụ
         (từ ~45 phút xuống < 10 phút/lần; giảm tỷ lệ hồ sơ bị trả lại từ 35% xuống < 10%)

├── Opportunity A: Sinh viên không biết chính xác hồ sơ cần giấy tờ gì và nộp ở đâu
├── Opportunity B: Sinh viên không hiểu các điều kiện ngoại lệ trong văn bản quy chế dài
└── Opportunity C: Cán bộ một cửa bị quá tải vì phải trả lời lặp lại cùng câu hỏi mỗi ngày
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- "Chatbot AI toàn năng trả lời mọi câu hỏi" — là giải pháp, không phải pain.
- "Xây Portal mới" — là giải pháp, trùng với portal hiện có.
- "Ứng dụng AI OCR tự động điền biểu mẫu" — là giải pháp, chưa chứng minh pain.
- "Dashboard tự động" / "Dùng ChatGPT" — solution đội lốt.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Thủ tục hành chính sinh viên** | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35** |
| Tra cứu lịch học/thi/thông báo | 5 | 5 | 4 | 4 | 4 | 5 | 4 | 31 |
| Gom & phân loại review F&B | 5 | 5 | 4 | 5 | 2 | 5 | 3 | 29 |

**Candidate được chọn:** Thủ tục hành chính sinh viên (35/35 điểm).

**Vì sao chọn:** Actor rõ (SV + cán bộ một cửa); quy trình vẽ được 7 bước với bottleneck cụ thể (tự đọc quy chế 45 phút); pain có bằng chứng từ phỏng vấn Mom Test và khảo sát 12 SV; impact đo được (thời gian, tỷ lệ hồ sơ trả lại); vừa sức một buổi lab; so sánh được đủ 4 mức No AI/Rule/Workflow/Agent; cả hai thành viên đều hiểu domain học vụ.

**Vì sao loại các candidate còn lại:**
- *Tra cứu lịch học/thi/thông báo:* Trùng lặp tính năng portal trường; phụ thuộc phân quyền API các kênh (Zalo, Teams, LMS) khó kiểm soát trong lab.
- *Gom & phân loại review F&B:* Rào cản kiểm chứng thực địa — không có dữ liệu review thật và không phỏng vấn được quản lý nhà hàng trong 3 tiếng lab.

**Xử lý bất đồng (nếu có):** Lê Quý Toàn ban đầu muốn bảo vệ đề tài F&B; Đàm Hồng Thái đặt câu hỏi về khả năng kiểm chứng trong lab. Sau khi đối chiếu tiêu chí "vừa sức lab" và "có bằng chứng", cả hai đồng thuận chuyển sang đề tài thủ tục hành chính — không có bất đồng kéo dài.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | SV thật sự mất >30 phút/lần tra cứu thủ tục và đi lại 2–3 lần | Value | 5 | 3 | Có (Mom Test + khảo sát) |
| 2 | SV bị "ngợp" vì quy chế dài, không phải vì thiếu tài liệu | Value | 5 | 4 | Có (Mom Test) |
| 3 | Có thể lấy văn bản quy chế chính thức từ cổng trường để làm nguồn RAG | Feasibility | 5 | 4 | Có (research) |
| 4 | SV chấp nhận dùng công cụ tra cứu trả về checklist + link biểu mẫu thay vì chatbot đối thoại dài | Usability | 5 | 4 | Có (khảo sát 12 SV) |
| 5 | Phòng ban sẵn sàng cập nhật tài liệu/quy chế định kỳ vào hệ thống | Viability | 5 | 1 | **Chưa — cần kiểm chứng** |
| 6 | AI trả lời có citation đủ chính xác để không gây hiểu sai chính sách | Value/Feasibility | 5 | 2 | Chưa — cần prototype |

*Giả định nhóm kiểm chứng trong buổi này:* #1, #2, #4 (qua Mom Test + khảo sát 12 SV). #5 và #6 để lại cho giai đoạn pilot.

### 3.2. Kiểm chứng

Cách đã dùng: **Phỏng vấn (Mom Test) + Survey**

Interview snapshot:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | SV năm 2 Khoa CNTT (ký hiệu Nguyễn V. A.) |
| Câu nói đáng nhớ nhất (nguyên văn) | "Mình không thiếu file quy chế, mình bị ngợp vì nó dài 30 trang và toàn từ pháp lý." |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Bị sốt xuất huyết nằm viện, cần xin hoãn thi; tải mẫu đơn cũ trên hội nhóm SV, nộp bị trả về vì thiếu "giấy ra viện có dấu mộc tròn bệnh viện tuyến huyện trở lên" và quá hạn 3 ngày → bị điểm F môn Giải tích 2. |
| Hiện đang xử lý bằng cách nào (workaround)? | Hỏi bạn bè, tìm trong hội nhóm sinh viên, tải mẫu đơn cũ; không đọc hết quy chế. |
| Mất bao lâu, bao lần? | ~45 phút đọc văn bản + đi lại 2–3 lần (ước tính từ mô tả). |
| Insight / opportunity rút ra | SV cần **checklist giấy tờ chính xác + link biểu mẫu chuẩn + hạn chót/địa điểm nộp**, không cần chatbot nói chuyện phiếm. |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Mom Test (SV năm 2 CNTT) | 1 | Bị trả hồ sơ vì thiếu giấy tờ; bị điểm F oan | — |
| Khảo sát lớp | 12 SV | 100% muốn checklist + link biểu mẫu + hạn chót thay vì chatbot đối thoại dài | Một số SV quen hỏi bạn bè/lớp trưởng, chưa thấy pain lớn |
| Quan sát nội bộ | — | Cán bộ một cửa bị quá tải, 35% hồ sơ bị trả lại (giả định cần xác thực) | — |

**Nhóm đã sửa problem thế nào sau kiểm chứng:** Thu hẹp từ "trợ lý AI toàn năng cho sinh viên" xuống **công cụ tra cứu ngữ nghĩa trả về checklist hồ sơ + link biểu mẫu chuẩn có trích dẫn điều khoản**; bỏ hướng chatbot đối thoại dài; nhấn mạnh giá trị "nguồn chính thống + cá nhân hóa theo phòng ban" thay vì chỉ "nhanh hơn".

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Cổng dịch vụ một cửa / Sổ tay sinh viên số (HUST, MyBK, VinUni) | Trang chính thức của các trường | Cung cấp văn bản quy chế gốc và biểu mẫu | Nguồn chính thống, có sẵn dữ liệu | Chủ yếu là file PDF dài, không có tìm kiếm ngôn ngữ tự nhiên, không cá nhân hóa theo câu hỏi | Tận dụng dữ liệu sẵn có, không xây lại nguồn |
| HUST Bot / FAQ chatbot trường | Kênh chatbot chính thức | Trả lời câu hỏi phổ biến theo kịch bản | Giải nhanh câu hỏi đơn giản | Trả lời theo kịch bản cứng, không xử lý câu hỏi phức tạp/ngoại lệ; vẫn phải đến bàn một cửa nộp giấy | Rule/FAQ giải ~60–70% câu đơn giản → làm trước |
| RAG chatbot trên tài liệu nội bộ (Dify, Flowise, LlamaIndex) | Tài liệu chính thức của các tool | Tìm & tổng hợp từ văn bản quy chế, trả lời có citation | Xử lý câu hỏi cần tổng hợp nhiều điều khoản | Cần dữ liệu sạch, cần guardrails chống bịa; cần kiểm tra citation | Workflow RAG phù hợp phần "tổng hợp"; bắt buộc citation + fallback |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ:

```text
HIỆN TẠI — ~45 phút đọc + 2–3 lần đi lại, kéo dài 2–3 ngày

[1 SV nhận ra cần làm thủ tục] 
→ [2 Tìm văn bản quy chế trên website trường: 10']
→ [3 Tự đọc quy chế 20–50 trang, hiểu điều kiện ngoại lệ: 45'] ← BOTTLENECK
→ [4 Tải mẫu đơn (thường là bản cũ) và điền: 15']
→ [5 Đến bàn một cửa nộp hồ sơ: 30–60' đi lại]
→ [6 Cán bộ kiểm tra, trả về nếu thiếu/sai: lặp lại bước 2–5]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | SV | Nhu cầu phát sinh | Xác định thủ tục cần làm | — | 1–2 lần/tháng |
| 2 | SV | Từ khóa thủ tục | File PDF quy chế | 10' | Thông tin rải rác nhiều trang |
| 3 | SV | Văn bản quy chế | Hiểu điều kiện/hồ sơ | **45'** | **BOTTLENECK** — ngôn ngữ pháp lý khó hiểu |
| 4 | SV | Mẫu đơn | Đơn đã điền | 15' | Dễ dùng mẫu cũ |
| 5 | SV | Hồ sơ | Hồ sơ nộp | 30–60' | Đi lại |
| 6 | Cán bộ một cửa | Hồ sơ | Phê duyệt / trả về | — | 35% hồ sơ bị trả lại (giả định) |

**Bottleneck chính:** Bước 3 — SV tự đọc và hiểu quy chế (~45 phút), dẫn đến bước 6 phải lặp lại nhiều lần.

### 4.2. Quy trình tương lai

```text
TƯƠNG LAI — < 30 phút, 1 lần đi lại

[1 SV chọn thủ tục & mô tả hoàn cảnh bằng ngôn ngữ tự nhiên]          ← CON NGƯỜI
→ [2 Rule: phân loại thủ tục + định tuyến phòng ban]                  ← RULE
→ [3 RAG: trích xuất điều kiện áp dụng + checklist giấy tờ + link mẫu]← AI (có citation)
→ [4 Hiển thị kết quả kèm điều khoản nguồn + nút "hỏi cán bộ"]        ← CON NGƯỜI xác nhận
→ [5 SV tự kiểm tra, điền biểu mẫu, đến bàn một cửa nộp]              ← CON NGƯỜI
→ [6 Cán bộ một cửa thẩm định và đóng dấu]                            ← CON NGƯỜI

Boundary:
- AI KHÔNG tự phê duyệt đơn, KHÔNG cấp chữ ký số, KHÔNG cam kết kết quả thay nhà trường.
- AI KHÔNG lưu trữ thông tin bệnh án/dữ liệu nhạy cảm của SV.
- AI KHÔNG trả lời khi không tìm thấy điều khoản nguồn → phải nói "không chắc" + fallback.

Phương án quay về: AI lỗi/không chắc → hiển thị hotline + địa chỉ bàn tiếp dân trực tiếp + link văn bản gốc.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 7 (bao gồm lặp) | 7 (không lặp) | Giảm vòng lặp trả hồ sơ |
| Tổng thời gian | ~45' đọc + 2–3 lần đi lại (2–3 ngày) | < 30' + 1 lần đi lại | Đo bằng log + khảo sát 4 tuần pilot |
| Số bước thủ công | 6/7 | 3/7 | Rule + RAG xử lý bước 2–3 |
| Bottleneck chính | Tự đọc quy chế 45' | RAG trích xuất + người xác nhận | Có citation để kiểm tra |
| Rủi ro mới phát sinh | — | Hallucination chính sách, lộ dữ liệu cá nhân | Guardrails + boundary + fallback |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Sinh viên đại học (năm 1–4), đặc biệt SV năm 1–2 chưa quen hệ thống; actor phụ: cán bộ một cửa/phòng đào tạo |
| **Quy trình** | Tra cứu và thực hiện thủ tục hành chính học vụ (xin giấy xác nhận, hoãn thi, miễn giảm học phí, vay vốn, học lại/học vượt) qua website trường + hỏi bạn bè + đến bàn một cửa |
| **Bottleneck** | Bước 3 — SV tự đọc và hiểu quy chế (~45 phút); dẫn đến bước 6 — hồ sơ bị trả lại (35% giả định) và phải đi lại 2–3 lần |
| **Impact** | ~45 phút/lần + 2–3 lần đi lại/SV; 35% hồ sơ bị trả lại; cán bộ một cửa quá tải vì trả lời lặp lại; SV có thể bị điểm F oan |
| **Success Metric** (baseline → target, cách đo) | Baseline: 45 phút tra cứu + 2.3 lần đi lại + 35% hồ sơ trả lại → Target: < 10 phút tra cứu, 1 lần đi lại, < 10% hồ sơ trả lại, Citation Accuracy ≥ 95%; đo bằng log hệ thống + khảo sát 4 tuần pilot + thống kê hồ sơ tại bàn một cửa |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | AI không tự phê duyệt đơn, không cấp chữ ký số, không cam kết kết quả thay nhà trường, không lưu trữ dữ liệu nhạy cảm (bệnh án). Cán bộ một cửa là người thẩm định và đóng dấu cuối cùng (HITL). |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- AI chỉ ra "Success Metric còn thiếu baseline và chưa định nghĩa rõ thế nào là giảm tải cho cán bộ" → **Đồng ý**, bổ sung baseline/target/cách đo cụ thể.
- AI gợi ý công thức ROI tài chính bằng USD → **Không đồng ý**, không phù hợp môi trường giáo dục; chuyển sang chỉ số vận hành thực tế.
- Nhóm khác hỏi "khác gì portal một cửa hiện có?" → **Đồng ý**, nhấn mạnh khác biệt: tìm kiếm ngôn ngữ tự nhiên + checklist cá nhân hóa + citation điều khoản.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ phức tạp cao × Độ mơ hồ thấp–trung bình**.

Vì sao: Quy trình nhiều bước (7 bước), nhiều nguồn văn bản, bước sau phụ thuộc bước trước (phức tạp cao). Nhưng câu trả lời chính sách cần đúng/sai rõ, có điều khoản nguồn để đối chiếu (mơ hồ thấp–trung bình). Ô này phù hợp **Workflow nhiều bước rõ ràng**, chưa cần Agent.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Cải thiện menu cổng trường + FAQ tĩnh + checklist PDF chuẩn | Câu hỏi đơn giản, phổ biến | Không giải được tình huống ngoại lệ; SV vẫn phải tự đọc quy chế | Không |
| **Rule** | Cây quyết định IF/ELSE theo từ khóa thủ tục | Câu hỏi cố định, ít biến thể | Gãy khi SV dùng ngôn ngữ tự nhiên; bỏ sót ngoại lệ | Không |
| **Workflow** | Rule phân loại thủ tục → RAG trích xuất điều kiện/checklist có citation → Rule lọc theo phòng ban → Người xác nhận/fallback | Câu hỏi đa dạng, cần tổng hợp nhiều điều khoản, cần citation | Hallucination nếu thiếu guardrails; cần dữ liệu sạch | **Có** |
| **Agent** | AI tự quyết bước tiếp theo, tự gửi email/ticket, tự điền đơn | Cần tự động hóa toàn diện, chấp nhận rủi ro | Bịa quy chế, giả mạo hồ sơ, vi phạm thẩm quyền hành chính | Không |

**Mức chọn:** **Workflow** (RAG Semantic Search + Rule routing + Human approval).

**Vì sao không chọn mức đơn giản hơn:** No AI và Rule không giải được câu hỏi ngoại lệ/ngôn ngữ tự nhiên — đúng phần lớn pain của SV. **Vì sao không lên Agent:** rủi ro hallucination chính sách và vi phạm thẩm quyền hành chính công là không chấp nhận được.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Trích xuất điều kiện áp dụng, checklist giấy tờ, link biểu mẫu, hạn chót từ văn bản quy chế; trả lời có citation |
| **Judgment** — con người cân nhắc, quyết định gì? | SV đọc kết quả + nguồn, tự kiểm tra; cán bộ một cửa thẩm định và đóng dấu |
| **Action** — hành động cuối cùng là gì, ai làm? | Hiển thị checklist + link mẫu + nút fallback; SV nộp hồ sơ; cán bộ phê duyệt |
| **Outcome** — đo kết quả bằng gì? | Thời gian tra cứu < 10'; tỷ lệ hồ sơ đúng lần đầu ≥ 90%; Citation Accuracy ≥ 95%; tỷ lệ fallback hợp lý |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Câu hỏi SV + văn bản quy chế đã index + role/phòng ban; dữ liệu quy chế có sẵn trên cổng trường (cần làm sạch) |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Nút "hữu ích/không hữu ích"; log câu hỏi fallback; thống kê hồ sơ trả lại tại bàn một cửa |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng: **Augment** — khảo sát 12 SV cho thấy 100% muốn checklist + link mẫu + hạn chót để tự làm, không muốn chatbot đối thoại dài hay AI tự nộp đơn thay.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào: **Báo nhầm** tệ hơn — nói sai chính sách khiến SV làm sai thủ tục, bị trả hồ sơ hoặc mất quyền lợi. Thiết kế: bắt buộc citation điều khoản nguồn; nếu không tìm thấy nguồn → fallback "không chắc" + hotline/bàn tiếp dân, thà bỏ sót còn hơn trả lời không có nguồn.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Sinh viên đại học (năm 1–4); actor phụ: cán bộ một cửa/phòng đào tạo |
| **Quy trình** | Tra cứu và thực hiện thủ tục hành chính học vụ qua website trường + hỏi bạn bè + bàn một cửa |
| **Bottleneck** | SV tự đọc/hiểu quy chế (~45 phút) → hồ sơ bị trả lại (35%) → đi lại 2–3 lần |
| **Impact** | 45 phút/lần + 2–3 lần đi lại/SV; 35% hồ sơ trả lại; cán bộ quá tải; SV có thể bị điểm F oan |
| **Success Metric** (baseline → target, cách đo) | 45 phút → < 10 phút; 2.3 lần → 1 lần đi lại; 35% → < 10% hồ sơ trả lại; Citation Accuracy ≥ 95%; đo bằng log + khảo sát 4 tuần pilot + thống kê bàn một cửa |
| **Boundary** | AI không tự phê duyệt đơn, không cấp chữ ký số, không cam kết thay nhà trường, không lưu dữ liệu nhạy cảm; cán bộ một cửa là người duyệt cuối (HITL) |
| **AI intervention point** | Bước RAG trích xuất điều kiện/checklist/link mẫu có citation; phân loại thủ tục và lọc theo phòng ban là Rule; fallback và phê duyệt là người |
| **Mức chọn** | **Workflow** |
| **Rủi ro & người kiểm tra** | Rủi ro: hallucination chính sách, lộ dữ liệu cá nhân. Người kiểm tra: SV đọc citation; cán bộ một cửa thẩm định; admin kiểm log định kỳ |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| AI intervention point | (chưa có) | RAG trích xuất có citation; Rule phân loại/lọc phòng ban | Cần chỉ rõ AI can thiệp ở bước nào để thiết kế guardrails |
| Mức chọn | (chưa có) | Workflow | Đã so sánh 4 mức; Workflow cân bằng giá trị và rủi ro |
| Rủi ro & người kiểm tra | (chưa có) | Hallucination + lộ dữ liệu; SV/cán bộ/admin kiểm tra | Cần gán trách nhiệm kiểm tra rõ ràng |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Có citation | Mọi câu trả lời về điều kiện/hồ sơ đều có trích dẫn điều khoản, văn bản nguồn | Không có nguồn hoặc nguồn không tồn tại |
| 2 | Không bịa | Mọi nhận định có trong văn bản quy chế | AI tự suy ra điều kiện/hạn chót không có trong văn bản |
| 3 | Đúng checklist | Danh sách giấy tờ khớp với quy định hiện hành | Thiếu/sai giấy tờ so với quy định |
| 4 | Đúng link biểu mẫu | Link mẫu đơn là bản mới nhất của năm học hiện tại | Link cũ/hỏng/sai mẫu |
| 5 | Fallback đúng | Câu hỏi không chắc → chuyển hotline/bàn tiếp dân kèm ngữ cảnh | Cố trả lời khi không đủ nguồn |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | **TB** | Mom Test + khảo sát 12 SV xác nhận pain; nhưng một số SV quen hỏi bạn bè, chưa thấy pain lớn |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | **Thấp–TB** | Kết quả dạng checklist + link mẫu dễ hiểu; cần test UI |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | **TB** | Văn bản quy chế có sẵn trên cổng trường; cần làm sạch + index; kỹ năng RAG khả thi |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | **TB–Cao** | Cần phòng ban cam kết cập nhật tài liệu định kỳ; bảo mật dữ liệu cá nhân là điều kiện tiên quyết; chưa kiểm chứng |

### 8.2. Kết luận

**Quyết định:** **Go, phạm vi nhỏ** (Pilot trên 5 thủ tục hành chính có tần suất phát sinh cao nhất).

**Lý do:** Value và Usability đã có bằng chứng ban đầu; Feasibility khả thi; Viability còn TB–Cao nhưng kiểm chứng được nhanh trong pilot hẹp. Chọn Go với phạm vi nhỏ để giảm rủi ro và có dữ liệu thực tế trước khi mở rộng.

**Nếu Go — pilot nhỏ nhất:**
1. Chọn 5 thủ tục: xin hoãn thi/nghỉ học tạm thời; xin giấy xác nhận sinh viên; vay vốn chính sách; miễn giảm học phí; đăng ký học lại/học vượt.
2. Làm sạch + index văn bản quy chế của 5 thủ tục này.
3. Prototype Workflow RAG có citation trên 5 thủ tục.
4. Pilot 2 tuần với một nhóm SV + một cán bộ một cửa; đo thời gian tra cứu, tỷ lệ hồ sơ trả lại, Citation Accuracy, tỷ lệ fallback.

**Nếu Not Yet — cần kiểm chứng gì trước:** (dự phòng) phỏng vấn 1–2 cán bộ phòng đào tạo/CTSV về khả năng cập nhật tài liệu định kỳ; khảo sát 20–30 SV về mức sẵn sàng dùng công cụ có citation.

**Nếu No-Go — nên làm gì thay AI:** cải thiện menu cổng trường + FAQ tĩnh + checklist PDF chuẩn + cập nhật mẫu đơn mới nhất; phân công đầu mối trả lời.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): Nếu sau **2 tuần pilot** mà **(1)** tỷ lệ hồ sơ bị trả lại vẫn **> 20%**, hoặc **(2)** RAG trích dẫn sai **> 5%**, hoặc **(3)** tỷ lệ fallback **> 50%** → dừng, cập nhật lại cơ sở tri thức; nếu vẫn không cải thiện → quay về FAQ tĩnh + cải thiện cổng trường + bàn tiếp dân trực tiếp.

---

## 9. Hạn chế và hướng tiếp theo

- Số liệu baseline (45 phút, 35% hồ sơ trả lại, 2.3 lần đi lại) phần lớn là **giả định/ước tính** từ Mom Test 1 người + khảo sát 12 SV; cần xác thực bằng log hệ thống và thống kê bàn một cửa.
- Chưa phỏng vấn trực tiếp cán bộ một cửa — góc nhìn Actor 2 còn dựa trên quan sát gián tiếp.
- Giả định Viability (phòng ban cập nhật tài liệu định kỳ) chưa kiểm chứng — rủi ro lớn nhất cần xử lý trước khi mở rộng.
- Chưa có prototype RAG để đo Citation Accuracy thực tế; các ngưỡng eval hiện là mục tiêu kỳ vọng.
- Hướng tiếp theo: phỏng vấn cán bộ một cửa; prototype RAG trên 5 thủ tục; pilot 2 tuần; đo 4 chỉ số (thời gian, tỷ lệ trả lại, Citation Accuracy, fallback).

---

## 10. Tài liệu tham khảo

- Intercom — Job Stories Framework.
- Teresa Torres — *Continuous Discovery Habits* (Opportunity Solution Tree, Interview Snapshot).
- Rob Fitzpatrick — *The Mom Test*.
- David Bland — *Testing Business Ideas* (Assumption Map).
- Jeff Gothelf — *Lean UX* (Problem Statement).
- Google PAIR — *People + AI Guidebook* (Augment vs Automate, AI sai kiểu nào).
- Anthropic — *Building Effective Agents* (No AI / Rule / Workflow / Agent).
- Marty Cagan — SVPG (4 rủi ro: Value, Usability, Feasibility, Viability).
- Agrawal, Gans, Goldfarb — *Prediction Machines* (AI Canvas).
- Cổng dịch vụ trực tuyến & Sổ tay sinh viên số — Trường Đại học Bách Khoa Hà Nội & VinUniversity (research giải pháp đã có).
