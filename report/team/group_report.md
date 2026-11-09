# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: **E305t108**
- Thành viên:
  1. **Đàm Hồng Thái** — MSSV: `2A202603927` (Trưởng nhóm)
  2. **Lê Quý Toàn** — MSSV: `2A202603941` (Thành viên)
- Candidate problem được chọn (1 câu): **Khi cần thực hiện thủ tục hành chính hoặc giải quyết vướng mắc học vụ tại trường, sinh viên gặp khó khăn khi tra cứu quy định rải rác và biểu mẫu phức tạp, dẫn đến tốn thời gian đi lại nhiều lần và làm quá tải cán bộ phòng ban.**
- Quyết định cuối: **Go, phạm vi nhỏ** (Thực hiện pilot trên 5 thủ tục hành chính có tần suất phát sinh cao nhất).

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

Nhóm gồm 2 thành viên tiến hành pitch **6 candidate** tiêu biểu (mỗi thành viên chuẩn bị 3 Problem Cards từ CP2):

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Lê Quý Toàn | Khi nhận đánh giá sao thấp đa kênh, CSKH muốn phân loại lỗi tự động để xử lý nhanh | CSKH, Quản lý chuỗi F&B | Đọc và gán tag thủ công 45'/ngày | *"Đề tài F&B này lấy đâu ra dữ liệu review thật để test trong buổi lab 3 tiếng, và liệu có phỏng vấn được quản lý nhà hàng ngay bây giờ không?"* (Đàm Hồng Thái hỏi) |
| 2 | Lê Quý Toàn | Khi làm thủ tục hành chính trường, SV muốn có hướng dẫn đủ và chuẩn để không phải đi lại nhiều lần | Sinh viên, Cán bộ đào tạo/CTSV | Đọc dò văn bản quy chế dài 20–30 trang và hỏi qua lại (45–60') | *"Lần gần nhất bạn làm thủ tục giấy tờ ở trường mất bao lâu? Sinh viên hay bị mắc kẹt nhất ở khâu nào?"* (Đàm Hồng Thái hỏi) |
| 3 | Lê Quý Toàn | Khi khách khiếu nại đơn hàng giao lỗi/thiếu món, CSKH muốn đối chiếu ảnh đóng gói để ra quyết định hoàn tiền trong 10' | CSKH, Thủ kho/Bếp | Tìm ảnh camera đóng gói và đối chiếu xác minh (25'/ticket) | *"Quy trình này phụ thuộc camera kho và shipper, liệu có vượt quá phạm vi lab không?"* (Đàm Hồng Thái hỏi) |
| 4 | Đàm Hồng Thái | Khi có nhiều thông báo bài tập, hạn nộp và lịch thi, SV muốn tổng hợp thông tin quan trọng để không trễ hạn | Sinh viên, Lớp trưởng, Giảng viên | Lọc thông báo từ Zalo, Teams, LMS, Canvas (15–20'/ngày) | *"Mỗi môn dùng một kênh khác nhau (Zalo, Teams, LMS), làm sao lấy dữ liệu tập trung mà không vi phạm phân quyền API?"* (Lê Quý Toàn hỏi) |
| 5 | Đàm Hồng Thái | Khi xem lịch học, lịch thi hoặc phòng học, SV muốn tra cứu tại một nơi để không phải tìm kiếm nhiều lần | Sinh viên, Cán bộ lớp | Mở portal, group lớp, email tìm phòng học (5–10'/lần) | *"Portal trường đã có sẵn lịch học và lịch thi, nếu làm thêm giải pháp AI thì có bị trùng lặp tính năng và lãng phí không?"* (Lê Quý Toàn hỏi) |
| 6 | Đàm Hồng Thái | Khi đến kỳ đăng ký học phần, SV muốn biết môn học phù hợp lộ trình để đăng ký đúng tiến độ và tránh trùng lịch | Sinh viên, Cố vấn học tập | Đối chiếu cây điều kiện tiên quyết và tính tín chỉ (2–3 tiếng) | *"Sinh viên kẹt môn chủ yếu do hết slot hay do không hiểu quy chế? Nếu do hết slot thì AI có giải quyết được nghẽn hạ tầng server không?"* (Lê Quý Toàn hỏi) |

---

### 2.2. Cluster

Nhóm phân loại 6 candidate thành 3 cụm vấn đề (Cluster) dựa trên bản chất nghiệp vụ:

| Cluster | Các candidate thuộc nhóm | Pattern chung |
|---|---|---|
| **Cluster A: Tra cứu & Tổng hợp Lịch học, Thông báo** | Candidate #4, #5 | Dữ liệu mang tính thời điểm, thay đổi theo tuần, phần lớn portal trường hoặc kênh chat lớp đã có sẵn nhưng bị phân mảnh. |
| **Cluster B: Hướng dẫn Quy định & Thủ tục Hành chính** | Candidate #2 | Văn bản quy chế dài, biểu mẫu phân tán nhiều phòng ban, sinh viên rất sợ làm sai; cán bộ hành chính bị hỏi lặp lại gây quá tải. |
| **Cluster C: Nghiệp vụ Vận hành & Đăng ký Học phần** | Candidate #1, #3, #6 | Phụ thuộc vào dữ liệu vận hành bên thứ ba (POS/camera đơn hàng) hoặc nghẽn hạ tầng kỹ thuật (server trường hết slot lớp học). |

---

### 2.3. Opportunity Solution Tree rút gọn

Nhóm xác định **1 Outcome trọng tâm đo lường được**: Giảm thời gian sinh viên tra cứu và hoàn tất thủ tục hành chính, đồng thời giảm số lượt hỏi lặp lại tại văn phòng khoa/phòng đào tạo.

```text
OUTCOME: Giảm 60% thời gian sinh viên tra cứu & hoàn thiện hồ sơ thủ tục hành chính, 
         đồng thời giảm 50% số câu hỏi lặp lại cho cán bộ đào tạo/CTSV.
├── Opportunity 1: Sinh viên không biết thủ tục cần những giấy tờ gì và nộp ở phòng ban nào.
├── Opportunity 2: Sinh viên không hiểu các điều kiện ngoại lệ trong văn bản quy chế (hoãn thi, miễn giảm, bảo lưu).
└── Opportunity 3: Cán bộ phòng ban mất quá nhiều thời gian giải thích các câu hỏi lặp lại mỗi ngày.
     ✗ "Chatbot AI toàn năng giải đáp mọi thắc mắc"  ← SOLUTION, gạch bỏ khỏi tầng này
     ✗ "Xây dựng cổng portal một cửa mới"           ← SOLUTION, gạch bỏ khỏi tầng này
     ✗ "Sổ tay sinh viên điện tử"                   ← SOLUTION, gạch bỏ khỏi tầng này
```

*Những ý đã gạch bỏ vì là solution đội lốt opportunity:*
- "Chatbot AI trả lời tự động": Đây là giải pháp công nghệ, không phải nỗi đau của sinh viên.
- "Cổng portal tích hợp": Đây là tính năng phần mềm lớn vượt ngoài phạm vi giải quyết vấn đề.

---

### 2.4. Chấm điểm shortlist (Thang điểm 1–5)

Nhóm rút gọn 3 candidate đại diện cho 3 cluster để chấm điểm theo 7 tiêu chí:

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Candidate 1: Hướng dẫn thủ tục hành chính & quy chế (#2)** | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35** |
| Candidate 2: Tổng hợp thông báo bài tập & lịch thi (#4) | 5 | 4 | 4 | 3 | 4 | 4 | 5 | 29 |
| Candidate 3: Lựa chọn & Đăng ký học phần theo lộ trình (#6) | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 27 |

**Candidate được chọn:** **Candidate 1 — Hướng dẫn & Tra cứu Thủ tục Hành chính, Quy chế Sinh viên tại Trường Đại học.**

**Vì sao chọn:**
1. *Actor và Quy trình cực kỳ rõ ràng:* Sinh viên cần làm giấy tờ $\rightarrow$ Tra cứu quy chế $\rightarrow$ Chuẩn bị hồ sơ $\rightarrow$ Nộp và chờ ký duyệt $\rightarrow$ Nhận kết quả.
2. *Pain thật, bằng chứng rõ ràng:* Cả 2 thành viên đều từng đi lại 2–3 lần vì thiếu giấy tờ xác nhận; cán bộ một cửa luôn trong tình trạng quá tải vào các đợt cao điểm đầu kỳ và trước kỳ thi.
3. *Đầu vào dữ liệu có sẵn và chuẩn xác:* Toàn bộ quy chế, biểu mẫu, quy trình một cửa của trường đã có sẵn trên văn bản PDF chính thức (Sổ tay sinh viên, Quyết định quy chế đào tạo).
4. *So sánh rõ ràng 4 mức giải pháp:* Có đất để phân định rạch ròi giữa việc dùng bảng FAQ tĩnh (No AI), chatbot cây quyết định (Rule), Workflow RAG trích xuất thông tin có trích dẫn, và chứng minh vì sao không được dùng Autonomous Agent.

**Vì sao loại các candidate còn lại:**
- *Loại Candidate 2 (Thông báo bài tập/lịch học):* Dữ liệu phân mảnh trên nhiều ứng dụng bảo mật của giảng viên (Zalo kín, Teams, LMS cá nhân); việc cào dữ liệu gặp rào cản phân quyền nghiêm trọng. Hơn nữa, trường đã có portal sinh viên hiển thị lịch tự động.
- *Loại Candidate 3 (Đăng ký học phần):* Vấn đề nghẽn lớn nhất của sinh viên khi đăng ký học phần thực chất là **hệ thống server bị nghẽn (quá tải băng thông)** và **hết slot lớp học**, chứ không phải do sinh viên không biết chọn môn. AI không giải quyết được vấn đề cơ sở hạ tầng mạng của nhà trường.

**Xử lý bất đồng:** Ban đầu Toàn muốn pitch đề tài F&B (phân loại review), còn Thái muốn tập trung vào bài toán thông báo học tập (#4). Tuy nhiên, sau khi Thái phản biện về rào cản kiểm chứng người thật của đề tài F&B trong buổi lab 3 tiếng, và Toàn phản biện về rào cản phân quyền API của các kênh Zalo/Teams, cả 2 bạn đã cùng thống nhất chuyển sang **Candidate #2 (Thủ tục hành chính sinh viên)** vì cả 2 đều là sinh viên, hiểu sâu domain, có sẵn văn bản quy chế trường và có thể phỏng vấn người thật ngay tại lớp.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

Nhóm lập danh sách 5 giả định rủi ro then chốt:

| # | Giả định | Loại rủi ro | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|:---:|
| 1 | Sinh viên mất nhiều thời gian đọc quy chế và hay bị nộp thiếu giấy tờ | Value | 5 | 3 | ✅ (Kiểm chứng ngay) |
| 2 | Cán bộ văn phòng khoa/CTSV bị quá tải bởi các câu hỏi thủ tục lặp lại | Value | 4 | 2 | ✅ (Kiểm chứng ngay) |
| 3 | Sinh viên sẵn sàng tra cứu qua công cụ tự động thay vì nhắn tin hỏi bạn bè | Usability | 4 | 2 | ✅ (Kiểm chứng ngay) |
| 4 | Văn bản quy chế của trường đủ rõ ràng để trích xuất điều kiện logic | Feasibility | 5 | 4 | — (Đã có file PDF) |
| 5 | Nhà trường cho phép sinh viên nộp trước bản mềm hồ sơ qua mạng | Viability | 4 | 2 | Hỏi cán bộ sau |

**Giả định nhóm tập trung kiểm chứng trong buổi lab:** Giả định #1, #2 và #3 thông qua phỏng vấn người thật theo phương pháp **The Mom Test**.

---

### 3.2. Kiểm chứng thực tế

Nhóm thực hiện phỏng vấn nhanh **3 người thật** tại khuôn viên trường theo 3 luật của The Mom Test (hỏi về trải nghiệm quá khứ, không hỏi giả định tương lai, không khen ngợi ý tưởng):

#### Interview Snapshot 1 — Sinh viên năm 2 xin hoãn thi vì lý do sức khỏe
* **Người được hỏi:** Sinh viên năm 2, Khoa Công nghệ Thông tin.
* **Câu nói đáng nhớ nhất (nguyên văn):** *"Lúc em bị sốt xuất huyết nằm viện, mẹ em lên trường nộp đơn hoãn thi thì bị bảo thiếu giấy xác nhận của bệnh viện tuyến quận trở lên. Quy chế ghi chung chung là 'cơ sở y tế có thẩm quyền', ai biết thẩm quyền là cấp nào đâu!"*
* **Lần gần nhất gặp vấn đề này:** Kỳ thi cuối kỳ II năm ngoái (tháng 6).
* **Workaround hiện tại:** Phải nhờ người nhà chạy về bệnh viện xin lại giấy xác nhận đúng tuyến, nộp lại lần 2 mất trọn 2 ngày.
* **Mất bao lâu:** Mất 2 ngày đi lại, suýt bị tính điểm 0 vì quá hạn nộp đơn 48 giờ sau khi thi.
* **Insight rút ra:** Nỗi đau không phải là không có đơn, mà là **không hiểu rõ tiêu chuẩn hợp lệ của các giấy tờ đính kèm** trong văn bản quy chế.

#### Interview Snapshot 2 — Sinh viên năm 3 xin giấy xác nhận vay vốn ngân hàng chính sách
* **Người được hỏi:** Sinh viên năm 3, Khoa Quản trị Kinh doanh.
* **Câu nói đáng nhớ nhất (nguyên văn):** *"Tải mẫu đơn trên web trường về in ra, điền xong đem lên nộp thì thầy bảo mẫu này cũ từ năm 2022 rồi, mẫu mới phải có mã định danh VNeID. Web trường có tới 3 chỗ để file tải về, không biết cái nào là bản cập nhật."*
* **Lần gần nhất gặp vấn đề này:** Đầu tháng 10/2026 khi làm hồ sơ gia hạn vay vốn sinh viên.
* **Workaround hiện tại:** Phải chạy ra quán photo cổng trường hỏi xin mẫu chuẩn mà các bạn khác hay in.
* **Mất bao lâu:** Đi lại 3 lần giữa phòng Đào tạo và phòng CTSV, mất 4 tiếng.
* **Insight rút ra:** Biểu mẫu bị phân mảnh, có tình trạng tồn tại song song biểu mẫu cũ và mới khiến sinh viên bị làm sai.

#### Interview Snapshot 3 — Lớp trưởng kiêm cán bộ hỗ trợ văn phòng khoa
* **Người được hỏi:** Lớp trưởng lớp K67, trực hỗ trợ bàn một cửa văn phòng khoa.
* **Câu nói đáng nhớ nhất (nguyên văn):** *"Mỗi đợt đầu kỳ, một ngày em nhận không dưới 30 tin nhắn hỏi cùng một câu: 'Xin giấy xác nhận sinh viên nộp ở đâu', 'Bị trùng lịch học thì làm đơn gì'. Em ghim bài trên Zalo rồi mà các bạn lười đọc, cứ inbox hỏi trực tiếp."*
* **Lần gần nhất gặp vấn đề này:** Tuần sinh hoạt công dân đầu năm học (tháng 9).
* **Workaround hiện tại:** Lưu sẵn 1 file Word chứa các link và tin nhắn mẫu, ai hỏi thì copy-paste gửi lại.
* **Mất bao lâu:** Khoảng 45–60 phút mỗi ngày trong 2 tuần cao điểm đầu kỳ.
* **Insight rút ra:** Cán bộ và lớp trưởng rất cần một hệ thống chuẩn để sinh viên tự tra cứu đúng biểu mẫu, tránh việc trả lời lặp đi lặp lại.

#### Bảng tổng hợp kiểm chứng:

| Nguồn | Số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| **Phỏng vấn trực tiếp** | 3 người (2 SV, 1 Lớp trưởng) | 3/3 đều xác nhận quy chế khó hiểu, biểu mẫu tải sai phiên bản, tốn ít nhất 2–3 lượt đi lại | 1 sinh viên cho biết các thủ tục đơn giản (như cấp bảng điểm) làm qua cổng portal trường đã tương đối ổn, chỉ có các thủ tục giải quyết việc cá biệt (hoãn thi, bảo lưu, học bổng xã hội) mới rối rắm |
| **Micro Survey nhanh trong lớp** | 12 sinh viên | 10/12 (83%) từng phải hỏi người khác về thủ tục hành chính; 8/12 từng nộp thiếu/sai giấy tờ | 2 bạn cho biết thường nhờ bạn bè làm hộ hoặc hỏi thẳng cố vấn học tập nên không tự tra cứu |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
1. **Thu hẹp phạm vi:** Không làm cho toàn bộ 50+ thủ tục của trường. Tập trung giải quyết **5 thủ tục phức tạp và hay sai sót nhất**: (1) Hoãn thi/thi bù vì lý do bất khả kháng, (2) Đơn xin nghỉ học tạm thời (bảo lưu), (3) Xác nhận sinh viên để vay vốn/hoãn nghĩa vụ quân sự, (4) Miễn giảm học phí đối tượng chính sách, (5) Quy đổi chứng chỉ tiếng Anh chuẩn đầu ra.
2. **Bổ sung yêu cầu biểu mẫu chuẩn:** Hệ thống không chỉ giải thích quy định mà phải **cung cấp đúng đường link tải biểu mẫu phiên bản mới nhất** có đóng dấu hiệu lực.

---

### 3.3. Research giải pháp đã có

| Công cụ / Case study | Link chính thức | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / Rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Chatbot Hỏi đáp Tuyển sinh & Đào tạo (HUST Bot / VNU Portal Bot)** | https://ts.hust.edu.vn/ | Giải bước 1 & 2: Giải đáp câu hỏi cơ bản về học phí, chỉ tiêu tuyển sinh | Tự động trả lời tức thì 24/7 | Sử dụng cây kịch bản (Rule-based) cứng nhắc; khi sinh viên hỏi tình huống phức tạp có điều kiện kết hợp thì trả lời vòng vo hoặc báo "không hiểu" | Không dùng Chatbot kịch bản cứng; cần dùng công nghệ trích xuất ngữ nghĩa (RAG) trên kho tài liệu quy chế |
| **Cổng Dịch vụ một cửa điện tử (Trường ĐH Bách Khoa TP.HCM)** | https://mybk.hku.edu.vn/ | Giải bước 3 & 4: Cho phép nộp đơn online và theo dõi trạng thái hồ sơ | Chuẩn hóa quy trình thành form trực tuyến, giảm việc nộp giấy | Chỉ tiếp nhận form đã điền; không có bước tư vấn hướng dẫn trước khi nộp khiến sinh viên đính kèm file sai quy cách liên tục | Bài toán nằm ở **khâu chuẩn bị hồ sơ trước khi nộp**, chứ không phải khâu truyền nhận file |
| **Sổ tay Sinh viên điện tử dạng PDF tìm kiếm (VinUni / NEU Student Handbook)** | https://vinuni.edu.vn/current-students/ | Giải bước 1: Cung cấp đầy đủ toàn bộ văn bản quy chế | Thông tin chính thống 100%, có giá trị pháp lý | File PDF dài 180 trang; sinh viên dùng Ctrl+F rất khó tra vì ngôn ngữ hành chính khác với ngôn ngữ sinh viên hay dùng | Cần công cụ chuyển đổi ngôn ngữ đời thường của sinh viên sang đúng thuật ngữ hành chính trong quy chế |

**Kết luận Research:**
Thị trường đã có cổng tiếp nhận hồ sơ và có file PDF quy chế, nhưng **hoàn toàn bỏ trống khâu hướng dẫn chuẩn bị hồ sơ thông minh**. Khoảng trống giá trị lớn nhất là: **Chuyển hóa câu hỏi tình huống của sinh viên $\rightarrow$ Đối chiếu quy chế chính thống $\rightarrow$ Đưa ra Checklist hồ sơ cần chuẩn bị kèm link biểu mẫu chuẩn.**

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

```text
HIỆN TẠI — Tổng thời gian: 4–6 tiếng (kéo dài qua 2–3 ngày làm việc)

[1. Phát sinh nhu cầu làm thủ tục] (5')
→ [2. Tìm quy chế trên web trường & hỏi bạn bè/Zalo] (30')
→ [3. Đọc dò văn bản PDF 20–30 trang & tự đoán giấy tờ cần nộp] (45') ← BOTTLENECK
→ [4. Tải biểu mẫu (dễ tải nhầm mẫu cũ) & tự điền đơn] (30')
→ [5. Lên văn phòng khoa/trường xếp hàng nộp hồ sơ] (45')
→ [6. Bị cán bộ trả về vì thiếu giấy tờ xác nhận / sai mẫu] (15') ← RỦI RO LẶP LẠI BƯỚC 3 & 4
→ [7. Bổ sung giấy tờ & nộp lại lần 2] (60')
```

```mermaid
flowchart TD
    A["1. Phát sinh nhu cầu thủ tục (5 phút)"] --> B["2. Tìm web trường & hỏi bạn bè (30 phút)"]
    B --> C["3. Đọc dò PDF quy chế & đoán giấy tờ (45 phút) ⚠️ BOTTLENECK"]
    C --> D["4. Tải biểu mẫu & điền tay (30 phút)"]
    D --> E["5. Lên phòng ban nộp hồ sơ (45 phút)"]
    E --> F{"Hồ sơ hợp lệ?"}
    F -- "Thiếu/Sai (Chiếm 40%)" --> G["6. Bị trả về, đi xin bổ sung (Mất 1-2 ngày)"]
    G --> D
    F -- "Hợp lệ" --> H["7. Nhận giấy hẹn & kết quả"]
```

| Bước | Actor | Input | Output | Thời gian / Tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Sinh viên | Sự cố phát sinh (ốm, xin nghỉ, xin giấy) | Nhu cầu làm thủ tục | 5 phút | Đột xuất hoặc theo đợt |
| 2 | Sinh viên | Web trường, group Zalo lớp | Thông tin truyền miệng rời rạc | 30 phút | Dễ nhận thông tin sai lệch |
| 3 | Sinh viên | File PDF quy chế 20–30 trang | Dự đoán danh mục giấy tờ cần nộp | **45 phút (BOTTLENECK)** | Ngôn ngữ quy chế khó hiểu, dễ đoán sai |
| 4 | Sinh viên | Link tải trên mạng | Đơn đã in và điền tay | 30 phút | Dễ tải nhầm biểu mẫu cũ |
| 5 | Sinh viên, Cán bộ | Hồ sơ giấy | Tiếp nhận hoặc từ chối | 45 phút (cả xếp hàng) | Cán bộ mất thời gian giải thích lại |
| 6 | Cán bộ, Sinh viên | Hồ sơ bị lỗi | Yêu cầu làm lại | Mất thêm 1–2 ngày | Tốn công sức đi lại của sinh viên |

**Bottleneck chính:** **Bước 3 (Đọc dò văn bản PDF quy chế để bóc tách giấy tờ cần nộp)**. Sinh viên không thể tự tin mình đã chuẩn bị đúng và đủ giấy tờ hợp lệ theo quy chế.

---

### 4.2. Quy trình tương lai (Ứng dụng Workflow AI + Rule)

```text
TƯƠNG LAI — Tổng thời gian: Dưới 30 phút (Không tính thời gian chờ phê duyệt)

[1. Sinh viên nhập câu hỏi tình huống bằng ngôn ngữ tự nhiên] (2')
→ [2. Rule lọc: Xác định thuộc 1 trong 5 nhóm thủ tục chuẩn] (1 giây) ← RULE
→ [3. AI Engine: Trích xuất điều khoản quy chế, tạo Checklist giấy tờ chuẩn xác 100%] (10 giây) ← AI (RAG)
→ [4. Hệ thống xuất link tải biểu mẫu phiên bản mới nhất + Hướng dẫn nộp] (1 giây) ← RULE
→ [5. Sinh viên kiểm tra checklist & chuẩn bị đúng ngay lần đầu] (15') ← CON NGƯỜI
→ [6. Nộp trực tiếp tại bàn một cửa hoặc tải lên cổng portal] (10') ← CON NGƯỜI
→ [7. Cán bộ tiếp nhận phê duyệt ngay, tỷ lệ trả về < 5%] ← CON NGƯỜI
```

```mermaid
flowchart TD
    A["1. SV gõ câu hỏi tình huống (2 phút)"] --> B["2. Rule xác định nhóm thủ tục (1s) ⚙️ RULE"]
    B --> C["3. AI trích xuất quy chế & sinh Checklist hồ sơ (10s) 🤖 AI"]
    C --> D["4. Cung cấp link biểu mẫu chuẩn mới nhất ⚙️ RULE"]
    D --> E["5. SV chuẩn bị đủ giấy tờ theo checklist (15 phút) 👤 HUMAN"]
    E --> F["6. Nộp hồ sơ tại phòng ban (10 phút) 👤 HUMAN"]
    F --> G["7. Cán bộ duyệt nhanh, không bị trả về 👤 HUMAN"]
```

**Phân định ranh giới & Kiểm soát:**
- **RULE xử lý:** Định tuyến nhóm thủ tục; cung cấp URL tải file `.docx` biểu mẫu chuẩn có chữ ký số của nhà trường; kiểm tra thời hạn hiệu lực của văn bản.
- **AI xử lý:** Đọc hiểu câu hỏi tự nhiên của sinh viên, tìm kiếm ngữ nghĩa (Semantic search) trong kho quy chế PDF, trích xuất điều kiện cụ thể (ví dụ: *"phải có xác nhận của bệnh viện cấp quận/huyện trở lên"*), sinh ra bảng Checklist giấy tờ cần chuẩn bị.
- **CON NGƯỜI (Human-in-the-loop):** Sinh viên tự chuẩn bị giấy tờ thật; Cán bộ hành chính là người **duyệt cuối cùng và ký xác nhận**.
- **BOUNDARY (Ranh giới an toàn):** AI **tuyệt đối KHÔNG có quyền tự động duyệt đơn, không tự cấp con dấu hoặc giấy xác nhận**.
- **PHƯƠNG ÁN QUAY VỀ (Fallback):** Nếu AI không tìm thấy quy chế tương ứng (Confidence thấp), hệ thống hiển thị thông tin liên hệ trực tiếp của Thầy/Cô phụ trách tại Văn phòng Khoa để sinh viên đến hỏi trực tiếp.

---

### 4.3. Bảng so sánh Before / After

| Chỉ số | Trước (Hiện tại) | Sau (Kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| **Tổng thời gian chuẩn bị hồ sơ** | 120–180 phút (kéo dài 2–3 ngày) | **Dưới 30 phút** | Giảm hơn 75% thời gian tra cứu và chuẩn bị |
| **Số lần sinh viên phải đi lại** | 2–3 lần | **1 lần duy nhất** | Chuẩn bị đúng đủ hồ sơ ngay từ đầu |
| **Tỷ lệ hồ sơ bị trả về do sai/thiếu** | ~40% (theo khảo sát) | **Dưới 5%** | Hạn chế tối đa việc tải nhầm biểu mẫu cũ |
| **Thời gian cán bộ giải thích thủ tục** | 45–60 phút/ngày | **Dưới 15 phút/ngày** | Giảm tải rõ rệt cho bàn một cửa |
| **Rủi ro mới phát sinh** | Không có (chỉ tốn công) | AI hiểu nhầm quy chế mới cập nhật | Xử lý bằng việc: AI bắt buộc phải trích dẫn số hiệu điều khoản và có cơ chế kiểm duyệt nội dung khi trường đổi văn bản |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Sinh viên đại học (đặc biệt sinh viên năm 1, năm 2) cần thực hiện các thủ tục hành chính, và Cán bộ phụ trách bàn một cửa tại các trường đại học. |
| **Quy trình** | Khi phát sinh nhu cầu thủ tục $\rightarrow$ Tìm kiếm quy chế trên web trường/hỏi bạn bè $\rightarrow$ Đọc dò văn bản PDF 20–30 trang $\rightarrow$ Tự tìm biểu mẫu và điền tay $\rightarrow$ Nộp tại văn phòng và chờ xử lý. |
| **Bottleneck** | Bước đọc dò văn bản PDF quy chế để xác định điều kiện và bóc tách giấy tờ cần nộp mất 45 phút, dễ hiểu sai từ ngữ hành chính dẫn đến chuẩn bị thiếu hồ sơ. |
| **Impact** | 40% sinh viên bị trả về làm lại hồ sơ, mất 2–3 ngày đi lại; cán bộ văn phòng một cửa mất 1–2 tiếng mỗi ngày chỉ để giải thích lặp đi lặp lại cùng một quy trình. |
| **Success Metric** | (1) Giảm thời gian chuẩn bị hồ sơ từ 120 phút xuống dưới 30 phút; (2) Tỷ lệ hồ sơ bị trả về do sai/thiếu giảm từ 40% xuống dưới 10%; (3) Số câu hỏi thủ tục lặp lại gửi cán bộ giảm 50% trong đợt cao điểm đầu kỳ. |
| **Boundary** | AI chỉ có nhiệm vụ trích xuất quy định và sinh checklist hướng dẫn; AI **không được tự động duyệt đơn, không can thiệp vào quyết định cấp phép của nhà trường**. Mọi hồ sơ phải có chữ ký và phê duyệt của cán bộ có thẩm quyền. |

**Phản biện nhận được (từ AI & nhóm bạn):**
- *Phản biện 1:* Metric giảm tỷ lệ trả về từ 40% xuống 10% đo bằng cách nào? $\rightarrow$ Nhóm ghi nhận: Sẽ đối chiếu sổ theo dõi tiếp nhận hồ sơ tại Văn phòng Khoa trong 2 tuần cao điểm.
- *Phản biện 2:* Nếu quy chế trường vừa đổi ngày hôm qua mà AI chưa cập nhật thì sao? $\rightarrow$ Nhóm đồng ý: Cần thêm trường ngày cập nhật văn bản và cảnh báo sinh viên đối chiếu số hiệu quyết định ở v1.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

- **Độ mơ hồ (Ambiguity):** **Trung bình**. Câu hỏi của sinh viên viết bằng ngôn ngữ tự nhiên, tiếng lóng, ngữ cảnh cá nhân rất đa dạng ("em bị té xe gãy tay lỡ thi môn Toán thì làm sao"). Tuy nhiên, đầu ra mong đợi là xác định (đúng quy chế, đúng biểu mẫu).
- **Độ phức tạp (Complexity):** **Thấp – Trung bình**. Quy trình gồm 4–5 bước cố định, kho tài liệu là tập hợp các file PDF quy chế chính thức của trường (không rẽ nhánh động, không cần tương tác nhiều hệ thống ngoài).
- **Vị trí trên ma trận:** Nằm ở ô **Workflow tích hợp AI (RAG Workflow)**. Không cần thiết và không được phép dùng Autonomous Agent.

---

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** | Sổ tay sinh viên in giấy + file FAQ tổng hợp tải về | Khi sinh viên chịu khó đọc và câu hỏi chỉ xoay quanh quy định cơ bản | Sinh viên lười đọc PDF dài, không tìm được từ khóa tương ứng với hoàn cảnh thực tế | Không chọn |
| **Rule** | Chatbot bấm nút theo kịch bản có sẵn (Menu-driven / Decision tree) | Khi sinh viên biết chính xác mình cần tìm thủ tục tên là gì | Rất dễ bế tắc khi sinh viên mô tả hoàn cảnh bằng ngôn ngữ đời thường; tạo kịch bản quá tốn công | Không chọn |
| **Workflow** | Rule lọc nhóm thủ tục $\rightarrow$ AI đọc hiểu ngữ cảnh & trích xuất điều khoản $\rightarrow$ Xuất checklist + link mẫu đơn $\rightarrow$ Người duyệt | Đủ cho 95% trường hợp câu hỏi thủ tục học vụ và hành chính sinh viên | AI có thể ảo giác nếu câu hỏi nằm ngoài tài liệu quy chế (xử lý bằng threshold tự tin) | **CHỌN** |
| **Agent** | AI tự động thay mặt sinh viên nộp hồ sơ, tự gửi email cho giảng viên, tự động duyệt đơn | Khi hệ thống hành chính của trường cho phép AI can thiệp sâu vào cơ sở dữ liệu | Cực kỳ nguy hiểm: rủi ro vi phạm quy chế đào tạo, giả mạo thông tin, chi phí xây dựng khổng lồ | Loại bỏ |

**Vì sao không chọn mức đơn giản hơn (Rule/No AI):** Khảo sát thực tế cho thấy sinh viên không dùng FAQ/sổ tay vì không biết từ khóa hành chính chuẩn (ví dụ: sinh viên tìm "nghỉ học 1 kỳ" trong khi quy chế dùng từ "nghỉ học tạm thời/bảo lưu"). Rule-based dựa trên từ khóa sẽ trả về kết quả rỗng. Chỉ có AI mới có khả năng ánh xạ ngữ nghĩa giữa hoàn cảnh đời thường của sinh viên và ngôn ngữ hành chính học thuật.

**Vì sao không chọn mức phức tạp hơn (Agent):** Rủi ro pháp lý và quy chế học vụ không cho phép bất kỳ hệ thống tự động nào được quyền ký duyệt hồ sơ thay cho cán bộ đào tạo.

---

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction (AI dự đoán gì?)** | (1) Phân loại câu hỏi của sinh viên vào đúng thủ tục hành chính tương ứng; (2) Trích xuất các điều kiện tiên quyết và danh mục giấy tờ cần nộp từ văn bản quy chế. |
| **Judgment (Con người cân nhắc gì?)** | Cán bộ kiểm tra tính xác thực của các giấy tờ gốc (chữ ký bác sĩ, con dấu bệnh viện, chứng chỉ photo công chứng); Sinh viên tự đánh giá mình có đủ điều kiện theo checklist không. |
| **Action (Hành động là gì?)** | Hệ thống cung cấp bảng Checklist hướng dẫn + Link tải file mẫu `.docx`; Sinh viên chuẩn bị hồ sơ; Cán bộ ký duyệt. |
| **Outcome (Đo kết quả bằng gì?)** | Thời gian chuẩn bị hồ sơ của sinh viên; Tỷ lệ hồ sơ nộp đúng ngay lần đầu; Số lượt hỏi lặp lại tại văn phòng. |
| **Input (Dữ liệu đầu vào mỗi lần chạy)** | Câu hỏi mô tả tình huống của sinh viên (text) + Kho văn bản quy chế, quyết định và biểu mẫu chuẩn của trường (file PDF/Docx đã index). |
| **Feedback (Lấy phản hồi ở đâu để cải thiện?)** | Đánh giá của sinh viên (Hữu ích / Không hữu ích); Phản hồi của cán bộ tiếp nhận về các lỗi giấy tờ mới phát sinh để cập nhật prompt/quy chế. |

---

### 6.4. Hai câu hỏi của Google PAIR

1. **Người dùng muốn được hỗ trợ (Augment) hay giao hẳn việc (Automate)?**
   - **Trả lời: Được hỗ trợ (Augment).** 
   - *Bằng chứng:* Phỏng vấn sinh viên cho thấy họ muốn được chỉ dẫn rõ ràng cần chuẩn bị những gì để họ tự làm; không sinh viên nào muốn giao thông tin cá nhân cho bot tự nộp vì lo ngại lỗi hệ thống làm mất hồ sơ. Cán bộ hành chính cũng khẳng định chỉ chấp nhận chữ ký sống/chữ ký số của chính sinh viên.
2. **AI sai kiểu nào tệ hơn: Báo nhầm (False Positive) hay Bỏ sót (False Negative)?**
   - **Trả lời: Bỏ sót giấy tờ cần nộp (False Negative) tệ hơn rất nhiều so với báo thừa.**
   - *Lý do:* Nếu AI bỏ sót 1 loại giấy tờ bắt buộc (ví dụ quên nhắc giấy xác nhận của địa phương), sinh viên đem hồ sơ lên trường sẽ bị trả về ngay lập tức, làm hỏng toàn bộ mục tiêu của hệ thống. Nếu AI nhắc thừa một giấy tờ phụ, sinh viên chỉ mất thêm 2 phút chuẩn bị.
   - *Thiết kế xử lý:* Bộ tiêu chí đánh giá và prompt của AI được cấu hình để ưu tiên độ bao phủ (High Recall) đối với danh mục giấy tờ yêu cầu.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Sinh viên đại học (đặc biệt sinh viên năm 1–3) cần làm thủ tục học vụ, và Cán bộ văn phòng khoa/phòng Đào tạo trực tiếp tiếp nhận hồ sơ. |
| **Quy trình** | Nhập câu hỏi tình huống $\rightarrow$ AI trích xuất quy định và sinh checklist giấy tờ $\rightarrow$ Hệ thống cấp biểu mẫu chuẩn $\rightarrow$ Sinh viên chuẩn bị giấy tờ $\rightarrow$ Nộp cán bộ duyệt. |
| **Bottleneck** | Bước đọc dò văn bản PDF quy chế để bóc tách giấy tờ cần nộp mất 45 phút, dễ hiểu sai từ ngữ hành chính dẫn đến chuẩn bị thiếu hồ sơ. |
| **Impact** | 40% sinh viên bị trả về làm lại hồ sơ, mất 2–3 ngày đi lại; cán bộ văn phòng một cửa mất 1–2 tiếng mỗi ngày chỉ để giải thích lặp đi lặp lại cùng một quy trình. |
| **Success Metric** | (1) Thời gian sinh viên chuẩn bị hồ sơ giảm từ 120' xuống dưới 30'; (2) Tỷ lệ hồ sơ bị trả về giảm từ 40% xuống dưới 5%; (3) Tỷ lệ sinh viên tự chuẩn bị đúng hồ sơ đạt $\ge 90\%$; (4) **AI Macro-F1 $\ge 0.88$**, **Recall danh mục giấy tờ $\ge 0.95$**. |
| **Boundary** | AI chỉ tư vấn và sinh checklist; **tuyệt đối không tự động duyệt đơn, không tự cấp giấy tờ**. Bắt buộc phải dẫn nguồn số hiệu điều khoản quy chế tương ứng. |
| **AI intervention point** | Nằm ở khâu tư vấn ban đầu: Ngay sau khi sinh viên nêu hoàn cảnh và trước khi sinh viên tải biểu mẫu điền thông tin. |
| **Mức chọn** | **Workflow tích hợp AI (RAG Workflow)** |
| **Rủi ro & người kiểm tra** | Rủi ro AI trích dẫn quy chế cũ hoặc hiểu sai điều kiện ngoại lệ $\rightarrow$ **Cán bộ văn phòng khoa kiểm tra định kỳ kho dữ liệu văn bản; sinh viên đối chiếu số hiệu điều khoản được trích dẫn.** |

### Thay đổi so với v0 và lý do:

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| **Success Metric** | Chỉ đo thời gian và tỷ lệ trả về chung chung | Bổ sung chỉ số chất lượng AI: Macro-F1 $\ge 0.88$, **Recall danh mục giấy tờ $\ge 0.95$** | Phản biện: Nhanh hơn nhưng AI liệt kê thiếu giấy tờ thì sinh viên vẫn bị trả về |
| **AI intervention point** | Chưa xác định cụ thể | Nằm ở bước tư vấn trước khi tải form | Làm rõ chính xác AI chen vào bước nghẽn nào trong quy trình |
| **Rủi ro & Kiểm soát** | Chỉ nêu ranh giới cấm AI duyệt đơn | Bổ sung cơ chế bắt buộc trích dẫn số hiệu điều khoản và kiểm duyệt kho văn bản | Đảm bảo tính pháp lý và khả năng đối chiếu ngược của sinh viên |

### Tiêu chí đánh giá đầu ra của AI (4 tiêu chí):

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | **Đúng quy chế & Có trích dẫn** | Nêu chính xác tên thủ tục và trích dẫn đúng số hiệu điều khoản trong Quyết định quy chế hiện hành của trường | Trích dẫn sai điều khoản, lấy quy chế của trường khác, hoặc không dẫn nguồn |
| 2 | **Đầy đủ danh mục giấy tờ (High Recall)** | Liệt kê đủ 100% các giấy tờ bắt buộc theo quy định cho trường hợp cụ thể của sinh viên | Bỏ sót dù chỉ 1 loại giấy tờ/chữ ký bắt buộc |
| 3 | **Đúng link biểu mẫu mới nhất** | Cung cấp link tải trực tiếp biểu mẫu có hiệu lực năm học hiện tại | Đưa link chết (404), link biểu mẫu cũ chưa cập nhật, hoặc không có file đính kèm |
| 4 | **Cảnh báo điều kiện tiên quyết rõ ràng** | Nêu rõ các mốc thời gian hạn chót (deadlines) và điều kiện loại trừ (ví dụ: đơn hoãn thi phải nộp trong 48h sau thi) | Không nhắc nhở về thời hạn nộp hoặc điều kiện tiên quyết |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro (Marty Cagan Framework)

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn) | Lý do / Bằng chứng |
|---|---|:---:|---|
| **Value (Giá trị)** | Sinh viên và nhà trường có thật sự cần và dùng không? | **Thấp** | 100% sinh viên được hỏi đều từng gặp khó khăn khi làm thủ tục; cán bộ một cửa cực kỳ mong muốn giảm tải việc hỏi lặp lại. |
| **Usability (Khả dụng)** | Sinh viên có dùng được và hiểu được câu trả lời của AI không? | **Thấp** | Giao diện hỏi đáp ngôn ngữ tự nhiên cực kỳ dễ tiếp cận; đầu ra là bảng Checklist giấy tờ ngắn gọn, rõ ràng hơn đọc văn bản PDF. |
| **Feasibility (Khả thi kỹ thuật)** | Có đủ dữ liệu, công cụ và kỹ năng để làm không? | **Thấp – TB** | Văn bản quy chế trường đã có sẵn ở định dạng PDF/Word công khai. Công nghệ RAG và LLM hiện tại giải quyết bài toán này rất ổn định. |
| **Viability (Vận hành & Tổ chức)** | Có phù hợp với quy định của trường, chi phí ai chịu? | **Trung bình** | Cần sự đồng thuận của Phòng Đào tạo/CTSV về việc cung cấp kho biểu mẫu chuẩn và xác nhận tính pháp lý của nội dung tư vấn. |

---

### 8.2. Kết luận

**Quyết định:** **Go, phạm vi nhỏ (Pilot)**.

**Lý do:**
1. Cả 4 rủi ro đều không có rủi ro nào ở mức **Cao (Nguy hiểm)**. Hai rủi ro ở mức Thấp (Value, Usability) đã được kiểm chứng qua phỏng vấn thực tế.
2. Bài toán có giá trị thực tiễn cao, giải quyết đồng thời nỗi đau của cả sinh viên lẫn cán bộ hành chính.
3. Không đòi hỏi tích hợp sâu vào hệ thống cơ sở dữ liệu bảo mật của trường trong giai đoạn đầu.

**Nếu Go — Pilot nhỏ nhất (Kế hoạch 2 tuần):**
- **Phạm vi thử nghiệm:** Đóng băng phạm vi trên **5 thủ tục phổ biến nhất** tại 1 Khoa cụ thể:
  1. Thủ tục hoãn thi / thi bù vì lý do bất khả kháng.
  2. Thủ tục nghỉ học tạm thời (bảo lưu kết quả học tập).
  3. Thủ tục cấp Giấy xác nhận sinh viên (vay vốn / hoãn NVQS).
  4. Thủ tục miễn giảm học phí đối tượng chính sách.
  5. Thủ tục nộp chứng chỉ tiếng Anh xét chuẩn đầu ra.
- **Dữ liệu nạp vào:** 5 quy trình chuẩn tương ứng được kiểm duyệt bởi trợ lý đào tạo khoa + 5 file biểu mẫu `.docx` mới nhất.
- **Cách đo lường pilot:** Theo dõi 50 lượt sinh viên tra cứu thực tế; đo tỷ lệ sinh viên tự chuẩn bị đúng hồ sơ nộp lên khoa trong tuần pilot.

**Ngưỡng dừng (Stopping Threshold):**
- *Ngưỡng 1:* Nếu trong 2 tuần pilot có trên **10% sinh viên bị trả về** do AI liệt kê thiếu giấy tờ bắt buộc $\rightarrow$ **Dừng pilot ngay lập tức** để kiểm tra lại toàn bộ quy trình RAG và prompt.
- *Ngưỡng 2:* Nếu tỷ lệ sinh viên đánh giá câu trả lời "Không hữu ích" vượt quá **25%** $\rightarrow$ Quay về phương án **No AI** (biên tập lại trang web tĩnh cẩm nang thủ tục một cửa dạng checklist đơn giản).
- *Ngưỡng 3:* Nếu Phòng Đào tạo/Khoa từ chối cung cấp đầu mối xác nhận biểu mẫu chính thức $\rightarrow$ **No-Go**, dừng dự án.

---

## 9. Hạn chế và hướng tiếp theo

- **Hạn chế:** Pilot mới thực hiện trên 5 thủ tục của 1 khoa, chưa mở rộng cho các thủ tục tài chính phức tạp hoặc học bổng doanh nghiệp ngoài trường.
- **Hướng tiếp theo:** 
  1. Mở rộng kho tri thức cho toàn bộ 30+ thủ tục của nhà trường sau khi đạt ngưỡng thành công ở pilot.
  2. Tích hợp trực tiếp vào cổng Zalo OA hoặc Microsoft Teams chính thức của trường để sinh viên tra cứu thuận tiện nhất.

---

## 10. Tài liệu tham khảo

1. Teresa Torres (2021), *Continuous Discovery Habits: Discover Products that Create Customer Value and Business Value* (Opportunity Solution Trees & Interview Snapshots).
2. Rob Fitzpatrick (2013), *The Mom Test: How to talk to customers & learn if your business is a good idea when everyone is lying to you*.
3. Jeff Gothelf, Josh Seiden (2021), *Lean UX: Designing Great Products with Agile Teams* (Problem Statement Framework).
4. Google PAIR (2019), *People + AI Guidebook* (User Needs, Augment vs Automate, Defining Success).
5. Anthropic (2024), *Building Effective Agents* (No AI vs Rule vs Workflow vs Agent).
6. Marty Cagan (2017), *Inspired: How to Create Tech Products Customers Love* (Four Big Risks Framework).
7. Quy chế Đào tạo và Công tác Sinh viên Đại học chính quy (Văn bản ban hành của Nhà trường).
