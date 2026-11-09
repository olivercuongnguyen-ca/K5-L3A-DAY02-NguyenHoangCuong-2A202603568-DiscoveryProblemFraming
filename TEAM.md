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

### NguyenTrieuDuong-2A202603524

**Phần việc phụ trách:**

- Chính: CP6 — so sánh mức can thiệp, AI Canvas, PAIR, Problem Statement v1, tiêu chí đánh giá, bốn rủi ro và đề xuất quyết định.
- Hỗ trợ theo phân công nhóm: CP3, CP4 Research và CP5 — Problem Statement v0.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch và phản biện | Pitch ba problem về API, Figma/token và setup unit test; hỏi Quang về phương án chốt lịch có sẵn, Giang về chi phí và Cương về NotebookLM. | Hai candidate API và unit test vào shortlist; đưa việc so sánh với phương án đơn giản và công cụ có sẵn vào thảo luận. |
| Tiếp nhận phản biện | Rà lại nguyên nhân mất thời gian làm rõ API, vị trí nghẽn khi triển khai giao diện và phương án dùng template/helper cho test. | Bổ sung cách đo riêng thời gian chờ và trao đổi, làm rõ thời gian từng bước và phương án không dùng AI. |
| Mức can thiệp AI | Phụ trách so sánh No AI/Rule/Workflow/Agent, AI Canvas và hai câu hỏi PAIR, có AI hỗ trợ bản nháp và rà soát. | Đề xuất Workflow cố định: Rule kiểm tra cấu trúc, AI đối chiếu ngữ nghĩa, sinh viên kiểm tra và quyết định; chưa cần Agent. |
| Problem Statement v1 và eval | Hoàn thiện nội dung CP6 về intervention point, boundary, metric, người kiểm tra và năm tiêu chí đánh giá. | Tách mục tiêu khỏi kết quả đã đạt; bổ sung đối chứng checklist, độ khớp người chấm và yêu cầu minh chứng truy vết được. |
| Rủi ro và quyết định | Phụ trách phân tích Value/Usability/Feasibility/Viability, đề xuất Not Yet và ngưỡng dừng; yêu cầu kiểm tra lại yêu cầu lab sau lượt dry run giới hạn. | Giữ kế hoạch kiểm chứng trước khi triển khai; không coi dry run thiếu nhãn độc lập và thời gian đối chứng là bằng chứng đủ để Go. |

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- [Báo cáo nhóm](report/team/group_report.md), mục 2.1 (#1–3 và câu hỏi phản biện), 2.4 (shortlist) và 6–8 (CP6).
- [Báo cáo cá nhân](report/individual/2A202603524_NguyenTrieuDuong.md), mục 3–6: Problem Cards, nhật ký phản biện, đóng góp, sử dụng AI và reflection.

**Điều mình học được từ phần nhóm:**

- Khi nhóm dành khoảng 15 phút bàn cách lấy rubric và xử lý nhiều định dạng, câu hỏi của Quang giúp quay lại xác nhận sinh viên có thực sự gặp vấn đề. Cần kiểm chứng người dùng và pain trước khi bàn cách triển khai.
- Phải phân biệt thời gian chờ với thời gian thao tác để chọn đúng phần có thể cải thiện; có số phút chưa đủ chứng minh nguyên nhân nghẽn.
- Với CP6, Workflow chỉ đáng chọn khi tạo thêm giá trị so với checklist hoặc Rule; target về tốc độ phải đi cùng tiêu chí chất lượng và người kiểm tra.
- Not Yet là kết luận có cơ sở khi vẫn còn thiếu bằng chứng về độ chính xác, hiệu quả và điều kiện dùng dữ liệu; cần ghi rõ phép thử tiếp theo và ngưỡng dừng.

### NguyenHoangCuong-2A202603568

**Phần việc phụ trách:**
Chính: CP3, tổng hợp thông tin - Phụ: CP4, CP6

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

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
- group_report.md: 2. Hội tụ nhóm (CP3)
- report/assets/: cp2-workflow-card-1.png
- Commit: 634b835, dc6a69f, 61b56b9, 99963af, 6efcbca, 340171c

**Điều mình học được từ phần nhóm:**
- Một problem tốt không chỉ đúng với bản thân mà phải được kiểm chứng từ nhiều người, pain point khác nhau theo từng nhóm đối tượng.
- Dễ bị "solution-first", cần hỏi trước "ai thật sự gặp vấn đề" rồi mới bàn cách làm.
- Phản biện giúp đánh giá lại bottleneck (hệ thống chậm có thể do khâu code, không chỉ do tổng hợp), không nên khẳng định bottleneck khi chưa kiểm chứng.
- Phỏng vấn mở theo Mom Test, dù chỉ 2 người, vẫn cho insight về workaround (nhờ bạn check chéo, dùng ChatGPT) và buộc nhóm chứng minh giá trị hơn các cách có sẵn.
- Metric cần phản ánh đúng hiệu quả, lần sau mình sẽ phản biện mạnh hơn ở điểm này.

### VuTrongQuang-2A202603535

**Phần việc phụ trách:**

- Chính: CP5 (Quy trình trước/sau và Problem Statement v0).
- Hỗ trợ: CP3 (Hội tụ nhóm), CP4 (Research), CP6 (Mức can thiệp AI + Problem Statement v1).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Pitch card #4 "Đối chiếu bài làm với Rubric", được nhóm chọn làm candidate problem (34/35 điểm shortlist).
- Khi nhóm sa vào bàn giải pháp khoảng 15 phút (rubric có công khai không, đọc file/ảnh thế nào), đề nghị dừng lại xác nhận pain point với sinh viên khác; nhóm chuyển sang đặt giả định (1, 2, 4) và kiểm chứng ở CP4.
- Viết quy trình hiện tại (5 bước, 55–60 phút, bottleneck dò minh chứng 25'), quy trình tương lai chia Rule / AI / Con người (18–20 phút, 3/5 bước thủ công), boundary, phương án quay về và bảng before/after (hỗ trợ bởi Giang).
- Vẽ ảnh quy trình tương lai `cp5-workflow-future.png`; viết Problem Statement v0 (hỗ trợ bởi Dương) làm nền cho bản v1 ở CP6.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `group_report.md` mục 2.1 (pitch #4–#6), mục 4 (quy trình), mục 5 (Problem Statement v0).
- `report/assets/cp5-workflow-future.png`.
- Commit `99963af` (hoàn thành CP5), `3e032a0` (ảnh quy trình tương lai).

**Điều mình học được từ phần nhóm:**

- Học được cách dừng lại đúng lúc khi nhóm rơi vào bẫy "solution-first" (mất 15 phút bàn chuyện rubric có công khai không, đọc file/ảnh thế nào) để quay về hỏi "ai đang thật sự gặp vấn đề" và kiểm chứng pain point trước.
- Nhận ra không phải vấn đề nào tốn thời gian cũng cần AI hoặc Agent; việc phân tách rõ bước nào dùng Rule (kiểm tra cấu trúc), bước nào dùng AI (đối chiếu ngữ nghĩa có trích dẫn minh chứng) và bước nào con người giữ quyết định (HITL), kèm đối chứng với phương án No AI (checklist, review chéo), giúp bài toán thực tế và an toàn hơn.

### 2A202603538_NguyenThiHuongGiang

**Phần việc phụ trách:**
Chính: CP4
-
**Pitch:** #7 (Giải đáp phụ huynh), #8 (Đưa đón học sinh), #9 (Thời khóa biểu).  
**Phản biện:** #2, #5, #12.
**Phụ trách chính:** Checkpoint 4

| Hoạt động | Nội dung thực hiện | Kết quả / Ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày 3 Problem Card gồm: #7 (Giải đáp thắc mắc phụ huynh), #8 (Đưa đón học sinh) và #9 (Xây dựng thời khóa biểu). | Đưa vấn đề #7 vào Cluster A; #8 và #9 vào Cluster B. Tuy nhiên, cả 3 vấn đề đều không được lựa chọn vào shortlist. |
| Phản biện bài của nhóm khác | - **Dương (#2):** Đặt câu hỏi về việc nguyên nhân xử lý chậm đến từ token hay bước kiểm tra giao diện.- **Quang (#5):** Góp ý về nguy cơ AI tóm tắt làm mất các chi tiết quan trọng trong thông tin đầu vào.- **Cương (#12):** Đặt vấn đề về việc hệ thống chậm do code hay do AI, đồng thời yêu cầu làm rõ bằng chứng chứng minh hiệu quả của AI. | Góp phần làm rõ nguyên nhân của vấn đề, đánh giá mức độ phù hợp khi ứng dụng AI và yêu cầu về bằng chứng trước khi đề xuất giải pháp. |
| Nhận phản biện | - **Pitch #7 – Cương:** Vấn đề giải đáp thắc mắc phụ huynh có thể đã được giải quyết bằng FAQ/RAG.- **Pitch #8 – Quang:** Dữ liệu phục vụ quy trình đưa đón học sinh có thể thiếu hoặc mâu thuẫn.<br>- **Pitch #9 – Dương:** Cần xem xét chi phí triển khai và vận hành giải pháp. | Tiếp nhận các ý kiến phản biện để đánh giá lại tính cần thiết, tính khả thi và giá trị ứng dụng AI của từng vấn đề. |
| Tham gia các hoạt động chung | Tham gia các hoạt động gom nhóm vấn đề (Cluster), xây dựng Opportunity Solution Tree (OST), lựa chọn Candidate, kiểm chứng vấn đề, xây dựng quy trình hiện tại và tương lai, hoàn thiện Problem Statement và xác định mức độ can thiệp của AI. | Đóng góp vào quá trình phân tích, đánh giá và lựa chọn hướng giải quyết của nhóm, đồng thời giúp làm rõ vai trò của AI trong quy trình đề xuất. |

### Bằng chứng công việc

- `group_report`: Mục 2.1 – Nội dung Pitch Problem Card #7, #8 và #9, checkpoint 4
- File báo cáo cá nhân: Mục 3 – Ba Problem Card đã xây dựng, trong đó Card #1 được lựa chọn làm hướng trình bày ưu tiên.
- Thư `mục assets`: cp4–interview–snapshot–1.md, cp4–survey–result.png 

**Điều mình học được từ phần nhóm:**
– Cần phân biệt giữa một vấn đề gây bất tiện và một vấn đề đủ nghiêm trọng để cần giải pháp mới.

– Việc phân tích quy trình hiện tại giúp mình hiểu rõ công đoạn nào thực sự tốn thời gian, thay vì chỉ nhìn vào kết quả cuối cùng.

– AI không nhất thiết phải xử lý toàn bộ công việc. Những bước có quy tắc rõ ràng nên ưu tiên Rule, còn các quyết định cần đánh giá ngữ cảnh vẫn cần con người tham gia.

– Một giải pháp có vẻ khả thi về mặt kỹ thuật chưa chắc đã phù hợp để triển khai thực tế nếu chưa có dữ liệu đánh giá và chưa xác định được rủi ro.

– Mình học được rằng quyết định chưa triển khai cũng là một kết quả hợp lý nếu bằng chứng hiện tại chưa đủ thuyết phục.
