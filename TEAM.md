# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: **E305t108**
- Candidate problem nhóm chọn (1 câu): **Khi cần thực hiện thủ tục hành chính hoặc giải quyết vướng mắc học vụ tại trường, sinh viên gặp khó khăn khi tra cứu quy định rải rác và biểu mẫu phức tạp, dẫn đến tốn thời gian đi lại nhiều lần và làm quá tải cán bộ phòng ban.**
- Quyết định cuối (Go / Not Yet / No-Go): **Go, phạm vi nhỏ** (Pilot trên 5 thủ tục hành chính có tần suất phát sinh cao nhất).

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Đàm Hồng Thái | 2A202603927 | Trưởng nhóm: Điều phối chung, phụ trách Research & chốt Problem Statement | `itsbra1vo` |
| 2 | Lê Quý Toàn | 2A202603941 | Thành viên: Phụ trách Kiểm chứng (Mom Test, khảo sát), thiết kế quy trình Before/After, phản biện kiến trúc AI | `ToanLee5433` |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Đàm Hồng Thái | Lê Quý Toàn | Cluster, cây OST, bảng chấm điểm shortlist |
| CP4 — Kiểm chứng | Lê Quý Toàn | Đàm Hồng Thái | Assumption map, 3 Mom Test snapshots, khảo sát 12 SV |
| CP4 — Research | Đàm Hồng Thái | Lê Quý Toàn | Bảng research đối thủ có link thực tế (HUST Bot, MyBK, VinUni) |
| CP5 — Quy trình trước/sau | Lê Quý Toàn | Đàm Hồng Thái | Sơ đồ quy trình Before/After + bảng đối chiếu + phương án fallback |
| CP5 — Problem Statement v0 | Đàm Hồng Thái | Lê Quý Toàn | Problem Statement v0 (6 trường) |
| CP6 — Mức can thiệp + Problem Statement v1 | Lê Quý Toàn | Đàm Hồng Thái | Ma trận độ mơ hồ/phức tạp, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Đàm Hồng Thái | Lê Quý Toàn | Đánh giá 4 rủi ro + Quyết định Go Pilot + 3 ngưỡng dừng |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### DamHongThai-2A202603927

**Phần việc phụ trách:**

- Trưởng nhóm: điều phối chung tiến độ, phân công checkpoint, tổng hợp báo cáo nhóm.
- Phụ trách chính phần **Research giải pháp đã có** ở CP4 (tổng hợp portal trường, FAQ chatbot, RAG tool có sẵn).
- Phụ trách chính **Problem Statement v0** (6 trường) ở CP5 và cùng Lê Quý Toàn nâng cấp lên **Problem Statement v1** (thêm AI intervention point, mức chọn, rủi ro & người kiểm tra) ở CP6.
- Phụ trách chính **đánh giá 4 rủi ro và ra quyết định Go Pilot** kèm 3 ngưỡng dừng định lượng ở CP6.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Scan 8 problems theo 4 lăng kính ở CP1, trong đó có 4 problem thuộc nhóm "Lặp lại" và "Tốn thời gian" (lịch học/thi, học phí, thủ tục hành chính, tìm hướng giải quyết bài tập) — làm nền cho việc chọn đề tài thủ tục hành chính.
- Viết 3 Problem Card chi tiết ở CP2: Card #1 (tra cứu thông tin học vụ rải rác), Card #2 (tổng hợp điều kiện học bổng/tốt nghiệp), Card #3 (giảm câu hỏi lặp lại cho lớp trưởng); chỉ rõ bottleneck từng card kèm số phút.
- Pitch các card trong CP3; phản biện đề tài F&B vì rào cản kiểm chứng trong buổi lab 3 tiếng.
- Cùng Lê Quý Toàn gom 12 candidate thành 3 cluster A/B/C; dựng cây OST với các opportunity cốt lõi, kiên quyết gạch bỏ các solution đội lốt ("Chatbot AI toàn năng", "Xây cổng portal mới", "Sổ tay sinh viên điện tử").
- Chấm điểm shortlist 3 card theo 7 tiêu chí; đề xuất bài Thủ tục hành chính sinh viên (35 điểm) làm candidate chính.
- Đề xuất bộ câu hỏi Mom Test cho CP4; research 3 giải pháp đã có: portal trường, FAQ chatbot, RAG có citation — từ đó nhóm đổi hướng từ "Agent" sang "Workflow".
- Viết Problem Statement v0 đủ 6 trường (Actor, Quy trình, Bottleneck, Impact, Success Metric, Boundary), kiểm tra không lẫn giải pháp vào problem.
- Cùng Lê Quý Toàn phân tích ma trận độ mơ hồ × độ phức tạp; lập luận chọn **Workflow** thay vì Agent vì rủi ro hallucination chính sách và yêu cầu bảo mật dữ liệu cá nhân.
- Lập bảng đánh giá 4 rủi ro (Value, Usability, Feasibility, Viability); đề xuất quyết định **Go Pilot** trên 5 thủ tục hành chính phổ biến, kèm 3 ngưỡng dừng: (1) tỷ lệ hồ sơ bị trả lại > 20% sau 2 tuần, (2) RAG sai trích dẫn > 5%, (3) tỷ lệ fallback > 50% → quay về FAQ tĩnh + cải thiện cổng SV.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Báo cáo nhóm `report/team/group_report.md`:
  - Mục 1: Thông tin nhóm, candidate problem, quyết định Go Pilot.
  - Mục 2: Bảng pitch 12 candidate, cluster A/B/C, cây OST rút gọn, bảng chấm điểm shortlist.
  - Mục 3: Assumption Map giả định, Interview Snapshot, bảng research 3 giải pháp.
  - Mục 4: Quy trình hiện tại/tương lai, boundary và phương án quay về.
  - Mục 5: Problem Statement v0 (6 trường).
  - Mục 6: Ma trận mơ hồ × phức tạp, AI Canvas, 2 câu hỏi Google PAIR.
  - Mục 7: Problem Statement v1 + bảng eval 5 tiêu chí và 10 test case.
  - Mục 8: Bảng 4 rủi ro, quyết định Go Pilot, 3 ngưỡng dừng.
- Báo cáo cá nhân `report/individual/2A202603927_DamHongThai.md`.

**Điều mình học được từ phần nhóm:**

- **Phân biệt problem thật và solution đội lốt:** Khi dựng cây OST, nhóm suýt đưa "dashboard tự động" và "dùng ChatGPT" vào tầng opportunity. Việc kiểm tra nghiêm ngặt "tầng này chỉ chứa pain/nhu cầu" giúp nhóm không lạc hướng. Bài học: phải liên tục tự hỏi "nếu thay giải pháp khác, câu này còn đúng không?".
- **Giá trị của phản biện chéo:** Nhờ phản biện chéo giữa hai thành viên, nhóm đã chọn đề tài Thủ tục hành chính sinh viên có bằng chứng thực tế và vừa sức trong một buổi lab.
- **Tầm quan trọng của kiểm chứng thực tế:** Tín hiệu phản bác từ một SV năm 3 buộc nhóm thu hẹp phạm vi vào 5 thủ tục phổ biến nhất thay vì làm dàn trải.
- **Thiết kế AI có trách nhiệm:** Luôn bắt đầu từ mức can thiệp đơn giản nhất đủ dùng (Workflow + RAG có citation) thay vì Agent; luôn đặt boundary rõ (không tự truy xuất dữ liệu cá nhân chưa xác thực, không tự gửi email/ticket) và luôn có phương án quay về (FAQ tĩnh + link cổng SV + form liên hệ phòng ban).

---

### LeQuyToan-2A202603941

**Phần việc phụ trách:**

- Phụ trách chính phần Kiểm chứng thực tế (Mom Test interview & Survey) ở CP4.
- Phụ trách thiết kế và mô hình hóa Quy trình Trước/Sau (Before/After workflow), phân tích điểm nghẽn và xây dựng chốt chặn con người (HITL) cùng phương án quay về (fallback) ở CP5.
- Đồng phụ trách phân tích Mức can thiệp AI (so sánh No AI vs Rule vs Workflow vs Agent), xây dựng AI Canvas rút gọn và thiết lập các tiêu chí Eval ở CP6.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 2 Problem Cards trong buổi pitch CP3, phản biện sắc bén giúp nhóm loại bỏ các candidate không thực tế (lịch học trùng lặp tính năng portal, kẹt server đăng ký tín chỉ).
- Cùng nhóm xây dựng cây OST rút gọn, trực tiếp đề xuất gạch bỏ các giải pháp công nghệ đội lốt (Chatbot toàn năng, Portal mới) để giữ lại đúng các Opportunity cốt lõi từ người dùng.
- Trực tiếp thực hiện 01 phỏng vấn sâu Mom Test với bạn Nguyễn V. A. (SV năm 2 Khoa CNTT xin hoãn thi vì ốm) và tham gia phân tích kết quả khảo sát 12 bạn sinh viên để bóc tách nhu cầu thực tế: sinh viên cần Checklist và link mẫu đơn chuẩn chứ không cần chatbot nói chuyện phiếm.
- Vẽ và chuẩn hóa sơ đồ quy trình Hiện tại (7 bước, 4–6 tiếng kéo dài 2–3 ngày) và Tương lai (7 bước, < 30 phút), phân tích chi tiết nút thắt đọc quy chế 45 phút.
- Xây dựng bảng so sánh 4 mức giải pháp, khẳng định lý do chọn Workflow (RAG trích xuất có đối chiếu nguồn) thay vì Autonomous Agent; thiết lập các tiêu chí đánh giá AI (Eval: Đúng quy chế, Đầy đủ giấy tờ High Recall $\ge 0.95$, Đúng link mẫu, Cảnh báo deadline).
- Đề xuất các ngưỡng dừng định lượng cho quyết định Go (Pilot 5 thủ tục).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Báo cáo nhóm `report/team/group_report.md`:
  - Mục 2: Bảng pitch 12 candidate, phân loại 3 cụm, cây OST rút gọn, bảng chấm điểm 35/35.
  - Mục 3: Assumption map giả định, Mom Test Snapshot 1 (phỏng vấn bạn Nguyễn V. A.), tổng hợp khảo sát 12 sinh viên.
  - Mục 4: Quy trình hiện tại & tương lai (ASCII & Mermaid), bảng so sánh Before/After 7 bước, chốt chặn HITL và phương án fallback.
  - Mục 6: Ma trận độ mơ hồ × độ phức tạp, so sánh 4 mức giải pháp, AI Canvas, câu hỏi Google PAIR.
  - Mục 7: Problem Statement v1 và các tiêu chí eval.
  - Mục 8: Đánh giá 4 Big Risks, quyết định Go và các ngưỡng dừng định lượng.
- Báo cáo cá nhân `report/individual/2A202603941_LeQuyToan.md`:
  - Mục 2: Bảng scan 10 problem qua 4 lăng kính có dấu hiệu thật đo lường được.
  - Mục 3: 3 Problem Cards chi tiết, 3 sơ đồ quy trình nháp và bảng phản biện AI 6 điểm.
  - Mục 4: Bảng theo dõi đóng góp cá nhân từ CP3 đến CP7.
  - Mục 5: Bảng đúc kết sử dụng AI qua các checkpoint (chỉ ra chỗ AI sai và cách sửa).
  - Mục 6: Phần Reflection chi tiết 6.1–6.6 (> 1.000 từ) và câu 6.7 tóm tắt chuỗi lý luận.

**Điều mình học được từ phần nhóm:**

- Nhận thức rõ sự khác biệt sống còn giữa "Vấn đề thật của người dùng" (Problem) và "Công nghệ hào nhoáng" (Solution-first). Một mô hình AI dù tối tân đến đâu cũng vô nghĩa nếu không giải quyết đúng điểm nghẽn thực sự của quy trình.
- Thấu hiểu giá trị của việc phản biện chéo (Peer review) và phương pháp phỏng vấn Mom Test: nhờ phản biện thẳng thắn của đồng đội, tôi đã kịp thời từ bỏ đề tài F&B thiếu khả năng kiểm chứng trong buổi lab để chuyển sang đề tài Thủ tục hành chính sinh viên với dữ liệu và người dùng thật 100%.
- Kỹ năng thiết kế hệ thống AI thực tế: Luôn bắt đầu từ mức can thiệp đơn giản nhất đủ dùng (Workflow + RAG trích xuất có kiểm duyệt) thay vì vội vã dùng Autonomous Agent; luôn thiết lập ranh giới (Boundary) nghiêm ngặt để kiểm soát rủi ro pháp lý và luôn chuẩn bị phương án quay về (Fallback) cho con người.
