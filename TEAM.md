# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm:
- Candidate problem nhóm chọn (1 câu):
- Quyết định cuối (Go / Not Yet / No-Go):

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | | | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | | | Assumption map, snapshot hoặc survey |
| CP4 — Research | | | Bảng research có link |
| CP5 — Quy trình trước/sau | | | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | | | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | | | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | | | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### DamHongThai-2A202603927

**Phần việc phụ trách:**

- Trưởng nhóm: điều phối chung tiến độ 4 tiếng, phân công checkpoint, tổng hợp báo cáo nhóm.
- Phụ trách chính phần **Research giải pháp đã có** ở CP4 (tổng hợp portal trường, FAQ chatbot, RAG tool có sẵn).
- Phụ trách chính **Problem Statement v0** (6 trường) ở CP5 và cùng Lê Quý Toàn nâng cấp lên **Problem Statement v1** (thêm AI intervention point, mức chọn, rủi ro & người kiểm tra) ở CP6.
- Phụ trách chính **đánh giá 4 rủi ro và ra quyết định Go Pilot** kèm 3 ngưỡng dừng định lượng ở CP6.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Scan 8 problems theo 4 lăng kính ở CP1, trong đó có 4 problem thuộc nhóm "Lặp lại" và "Tốn thời gian" (lịch học/thi, học phí, thủ tục hành chính, tìm hướng giải quyết bài tập) — làm nền cho việc chọn đề tài thủ tục hành chính.
- Viết 3 Problem Card chi tiết ở CP2: Card #1 (tra cứu thông tin học vụ rải rác), Card #2 (tổng hợp điều kiện học bổng/tốt nghiệp), Card #3 (giảm câu hỏi lặp lại cho lớp trưởng); chỉ rõ bottleneck từng card kèm số phút.
- Pitch Card #1 trong CP3 và đề xuất giữ làm candidate chính; phản biện Card #2 vì tần suất thấp (2–3 lần/năm), khó đo trong buổi lab.
- Cùng Lê Quý Toàn gom 7–8 candidate thành 3 cluster A/B/C; dựng cây OST với 4 opportunity, kiên quyết gạch bỏ các solution đội lốt ("Chatbot AI toàn năng", "Xây app mobile", "Dùng ChatGPT").
- Chấm điểm shortlist 3 card theo 7 tiêu chí; đề xuất Card #1 (32 điểm) làm candidate chính, Card #2 và #3 giữ làm mở rộng.
- Đề xuất bộ câu hỏi Mom Test cho CP4; research 3 giải pháp đã có: portal trường (có dữ liệu gốc nhưng thiếu tìm kiếm ngôn ngữ tự nhiên), FAQ chatbot (giải 60–70% câu đơn giản), RAG có citation (giải phần tổng hợp nhưng cần guardrails) — từ đó nhóm đổi hướng từ "Agent" sang "Workflow".
- Viết Problem Statement v0 đủ 6 trường (Actor, Quy trình, Bottleneck, Impact, Success Metric, Boundary), kiểm tra không lẫn giải pháp vào problem.
- Cùng Lê Quý Toàn phân tích ma trận độ mơ hồ × độ phức tạp; lập luận chọn **Workflow** thay vì Agent vì rủi ro hallucination chính sách và yêu cầu bảo mật dữ liệu cá nhân.
- Lập bảng đánh giá 4 rủi ro (Value, Usability, Feasibility, Viability); đề xuất quyết định **Go Pilot** trên 5 thủ tục hành chính phổ biến, kèm 3 ngưỡng dừng: (1) tỷ lệ hồ sơ bị trả lại > 20% sau 2 tuần, (2) RAG sai trích dẫn > 5%, (3) tỷ lệ fallback > 50% → quay về FAQ tĩnh + cải thiện cổng SV.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Báo cáo nhóm `report/team/group_report.md`:
  - Mục 1: Thông tin nhóm, candidate problem, quyết định Go Pilot.
  - Mục 2: Bảng pitch, cluster A/B/C, cây OST rút gọn, bảng chấm điểm shortlist.
  - Mục 3: Assumption Map 6 giả định (G1–G6), Interview Snapshot, bảng research 3 giải pháp.
  - Mục 4: Quy trình hiện tại/tương lai, boundary và phương án quay về.
  - Mục 5: Problem Statement v0 (6 trường).
  - Mục 6: Ma trận mơ hồ × phức tạp, AI Canvas, 2 câu hỏi Google PAIR.
  - Mục 7: Problem Statement v1 + bảng eval 5 tiêu chí.
  - Mục 8: Bảng 4 rủi ro, quyết định Go Pilot, 3 ngưỡng dừng.
- Báo cáo cá nhân `report/individual/2A202603927_DamHongThai.md`:
  - Mục 2: Bảng scan 8 problem qua 4 lăng kính có dấu hiệu thật đo lường được.
  - Mục 3: 3 Problem Cards chi tiết, 3 sơ đồ quy trình nháp và bảng phản biện AI.
  - Mục 4: Bảng theo dõi đóng góp cá nhân từ CP3 đến CP7.
  - Mục 5: Bảng đúc kết sử dụng AI qua các checkpoint (chỉ rõ chỗ AI sai và cách sửa).
  - Mục 6: Reflection 6.1–6.7.

**Điều mình học được từ phần nhóm:**

- **Phân biệt problem thật và solution đội lốt:** Khi dựng cây OST, nhóm suýt đưa "dashboard tự động" và "dùng ChatGPT" vào tầng opportunity. Việc kiểm tra nghiêm ngặt "tầng này chỉ chứa pain/nhu cầu" giúp nhóm không lạc hướng. Bài học: phải liên tục tự hỏi "nếu thay giải pháp khác, câu này còn đúng không?".
- **Giá trị của phản biện chéo:** Nhờ Lê Quý Toàn phản biện Card #2 (tần suất thấp, khó đo trong lab), tôi đã chuyển từ ủng hộ Card #2 sang ủng hộ Card #1 — thay đổi quan điểm dựa trên tiêu chí đánh giá thay vì cảm tính.
- **Tầm quan trọng của kiểm chứng thực tế:** Tín hiệu phản bác từ một SV năm 3 ("mình mất tầm 5 phút thôi, chủ yếu xem nhóm chat lớp") buộc nhóm thu hẹp actor và nhấn mạnh giá trị "nguồn chính thống + cá nhân hóa theo phòng ban" thay vì chỉ hứa "nhanh hơn".
- **Thiết kế AI có trách nhiệm:** Luôn bắt đầu từ mức can thiệp đơn giản nhất đủ dùng (Workflow + RAG có citation) thay vì Agent; luôn đặt boundary rõ (không tự truy xuất dữ liệu cá nhân chưa xác thực, không tự gửi email/ticket) và luôn có phương án quay về (FAQ tĩnh + link cổng SV + form liên hệ phòng ban).
