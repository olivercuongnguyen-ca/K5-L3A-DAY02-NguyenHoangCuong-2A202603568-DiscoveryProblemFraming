# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm:
- Candidate problem nhóm chọn (1 câu): Hỗ trợ sinh viên đối chiếu bài làm với rubric, phát hiện tiêu chí chưa đáp ứng và gợi ý cải thiện trước khi nộp
- Quyết định cuối (Go / Not Yet / No-Go): Not Yet

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Thị Hương Giang | 2A202603538 | Thành viên, phụ trách research | https://github.com/nthgiang311 |
| 2 | Vũ Trọng Quang | 2A202603535 | Thành viên, vẽ quy trình, viết Problem Statement v0 | https://github.com/Quangvu256 |
| 3 | Nguyễn Triều Dương | 2A202603524 | Thành viên, viết Problem Statement v1 | https://github.com/tdisokay2 |
| 4 | Nguyễn Hoàng Cương | 2A202603568 | Nhóm trưởng, viết báo cáo, tổng hợp và rà soát | https://github.com/olivercuongnguyen-ca |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Cương | Dương, Quang | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Giang | Cương | Assumption map, snapshot hoặc survey |
| CP4 — Research | Giang | Quang, Dương | Bảng research có link |
| CP5 — Quy trình trước/sau | Quang | Giang | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Quang | Dương | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Dương | Quang, Giang | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Dương | Cương | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenHoangCuong-2A202603568

**Phần việc phụ trách:**
Chính: CP3, tổng hợp thông tin - Phụ: CP4, CP6
-

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch #10, #11, #12 | Xếp vào cluster C (#10), A (#11), B (#12); không vào shortlist |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | Chạy và sửa lỗi setup 10 phút/component, setup tổng 25 phút | Dùng template và helper chung có đủ giảm lỗi mà không cần AI không?, Nếu rubric chứa các tiêu chí định tính, không rõ ràng (như 'phân tích sâu sắc', 'ý tưởng sáng tạo') hoặc bài nộp là code/ảnh chứ không chỉ văn bản, làm sao đảm bảo AI không báo sai hoặc ảo giác?, Nếu nhà trường đã có FAQ hoặc chatbot RAG để tra cứu thông tin, tại sao cần xây dựng AI Agent? |
| Nhận phản biện | Câu hỏi tôi nhận được: Tại sao không dùng ChatGPT mà lại cần xây dựng sản phẩm mới?, Tại sao không dùng các công cụ có sẵn như NotebookLM? Làm sao để chứng minh sản phẩm có độ chính xác cao hơn?, Vấn đề hệ thống cập nhật chậm có thể do việc code, làm sao để chứng minh hiệu quả của việc sử dụng AI tổng hợp dữ liệu? | Tôi đã sửa gì: Sửa metric để so sánh, đánh giá lại bottleneck |
| Gom cluster / cây OST | Thảo luận với nhóm | Cluster A/B/C, OST 1 outcome 3 opportunity |
| Chọn candidate problem | Cùng nhóm chấm điểm; không bất đồng | Củng cố lại lựa chọn vấn đề #4 của nhóm |
| Kiểm chứng / research | Hỗ trợ thiết kế câu hỏi interview | Giúp nhóm interview theo The Mom Test |
| Quyết định | Đưa thêm góc nhìn về metric | Củng cố kết luận Not Yet |
-

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
group_report.md: 2. Hội tụ nhóm (CP3)
report/assets/: cp2-workflow-card-1.png
Commit: 634b835, dc6a69f, 61b56b9, 99963af, 6efcbca, 340171c
-

**Điều mình học được từ phần nhóm:**
- Một problem tốt không chỉ đúng với bản thân mà phải được kiểm chứng từ nhiều người, pain point khác nhau theo từng nhóm đối tượng.
- Dễ bị "solution-first", cần hỏi trước "ai thật sự gặp vấn đề" rồi mới bàn cách làm.
- Phản biện giúp đánh giá lại bottleneck (hệ thống chậm có thể do khâu code, không chỉ do tổng hợp), không nên khẳng định bottleneck khi chưa kiểm chứng.
- Phỏng vấn mở theo Mom Test, dù chỉ 2 người, vẫn cho insight về workaround (nhờ bạn check chéo, dùng ChatGPT) và buộc nhóm chứng minh giá trị hơn các cách có sẵn.
- Metric cần phản ánh đúng hiệu quả, lần sau mình sẽ phản biện mạnh hơn ở điểm này.
-
