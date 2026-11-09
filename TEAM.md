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

### LeQuyToan-2A202603941

**Phần việc phụ trách:**

- Phụ trách chính phần Kiểm chứng thực tế (Mom Test interview & Survey) ở CP4.
- Phụ trách thiết kế và mô hình hóa Quy trình Trước/Sau (Before/After workflow), phân tích điểm nghẽn và xây dựng chốt chặn con người (HITL) cùng phương án quay về (fallback) ở CP5.
- Đồng phụ trách phân tích Mức can thiệp AI (so sánh No AI vs Rule vs Workflow vs Agent), xây dựng AI Canvas rút gọn và thiết lập 4 tiêu chí Eval ở CP6.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 2 Problem Cards trong buổi pitch CP3, phản biện sắc bén giúp nhóm loại bỏ các candidate không thực tế (lịch học trùng lặp tính năng portal, kẹt server đăng ký tín chỉ).
- Cùng nhóm xây dựng cây OST rút gọn, trực tiếp đề xuất gạch bỏ các giải pháp công nghệ đội lốt (Chatbot toàn năng, Portal mới) để giữ lại đúng 3 Opportunity cốt lõi từ người dùng.
- Trực tiếp thực hiện 01 phỏng vấn sâu Mom Test với bạn Nguyễn V. A. (SV năm 2 Khoa CNTT xin hoãn thi vì ốm) và tham gia phân tích kết quả khảo sát 12 bạn sinh viên để bóc tách nhu cầu thực tế: sinh viên cần Checklist và link mẫu đơn chuẩn chứ không cần chatbot nói chuyện phiếm.
- Vẽ và chuẩn hóa sơ đồ quy trình Hiện tại (7 bước, 4–6 tiếng kéo dài 2–3 ngày) và Tương lai (7 bước, < 30 phút), phân tích chi tiết nút thắt đọc quy chế 45 phút.
- Xây dựng bảng so sánh 4 mức giải pháp, khẳng định lý do chọn Workflow (RAG trích xuất có đối chiếu nguồn) thay vì Autonomous Agent; thiết lập 4 tiêu chí đánh giá AI (Eval: Đúng quy chế, Đầy đủ giấy tờ High Recall $\ge 0.95$, Đúng link mẫu, Cảnh báo deadline).
- Đề xuất 3 ngưỡng dừng định lượng cho quyết định Go (Pilot 5 thủ tục).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Báo cáo nhóm `report/team/group_report.md`:
  - Mục 2: Bảng pitch 6 candidate, phân loại 3 cụm, cây OST rút gọn, bảng chấm điểm 35/35.
  - Mục 3: Assumption map 5 giả định, Mom Test Snapshot 1 (phỏng vấn bạn Nguyễn V. A.), tổng hợp khảo sát 12 sinh viên.
  - Mục 4: Quy trình hiện tại & tương lai (ASCII & Mermaid), bảng so sánh Before/After 7 bước, chốt chặn HITL và phương án fallback.
  - Mục 6: Ma trận độ mơ hồ × độ phức tạp, so sánh 4 mức giải pháp, AI Canvas, câu hỏi Google PAIR.
  - Mục 7: Problem Statement v1 và 4 tiêu chí eval.
  - Mục 8: Đánh giá 4 Big Risks, quyết định Go và 3 ngưỡng dừng định lượng.
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
