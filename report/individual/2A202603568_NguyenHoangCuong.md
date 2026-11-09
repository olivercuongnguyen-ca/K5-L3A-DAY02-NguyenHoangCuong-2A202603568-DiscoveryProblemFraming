# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Hoàng Cương
- MSSV: 2A202603568
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: 
- Link repo nhóm: https://github.com/olivercuongnguyen-ca/K5-L3A-DAY02-NguyenHoangCuong-2A202603568-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi kết thúc buổi học, tôi muốn viết nhận xét cá nhân hóa cho từng học viên mà không phải dành quá nhiều thời gian cho việc soạn báo cáo lặp lại, để phụ huynh nắm được tiến độ học tập | Giáo viên, CM, phụ huynh  | Khoảng 30 phút sau mỗi buổi cho lớp 15-20 học viên, 1-2 buổi/ngày |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận yêu cầu từ nhiều phòng ban, tôi muốn tổng hợp và phát hiện các yêu cầu mâu thuẫn, để thiết kế hệ thống đúng ngay từ đầu | PM, BA, manager, các trưởng bộ phận, kho, QA/QC, bảo trì | Làm việc với 4-6 phòng ban; mất 1-2 ngày tổng hợp SOP, biên bản họp và file Excel; thường có yêu cầu mâu thuẫn cần xác nhận lại |
| 3 | Pain từ người khác | Khi quy trình nghiệp vụ thay đổi trong lúc dự án đang phát triển, tôi muốn nhanh chóng xác định các chức năng, dữ liệu và tài liệu bị ảnh hưởng, để hệ thống luôn bám sát quy trình thực tế | PM, BA, manager, developer, các trưởng bộ phận | hệ thống thường cập nhật chậm hơn 1-2 tuần so với quy trình; người dùng phải vận hành quy trình mới trên hệ thống cũ dẫn đến phát sinh lỗi chức năng và sai lệch dữ liệu, mỗi tuần mất thêm khoảng 4-8 giờ để đối soát, làm sạch dữ liệu |
| 4 | Lặp lại | Khi tới giờ standup, tôi muốn có sẵn update hôm qua, để không phải nhớ lại | PM | 15 phút/ngày |
| 5 | | Khi cuối tháng, tôi muốn có KPI từ nhiều dashboard trong một bảng, để báo cáo tháng | PM, manager | Mỗi tháng khoảng 2 tiếng |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.
AI gợi ý break down job story #2 để làm rõ hơn mục đích thiết kế đúng **ngay từ đầu**
-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tổng hợp yêu cầu mâu thuẫn từ nhiều phòng ban (#2) | Tốn 1-2 ngày/dự án, làm việc với 4-6 phòng ban, sai từ đầu thì kéo theo thiết kế sai; quy trình rõ (SOP, biên bản, Excel) | Phát hiện "mâu thuẫn" đo thế nào cho khách quan? AI có đọc đúng ngữ cảnh nghiệp vụ không? |
| 2 | Quy trình đổi, hệ thống cập nhật chậm (#3) | Pain thật, nhiều vai trò gặp; có số đo: chậm 1-2 tuần, mất 4-8 giờ/tuần đối soát dữ liệu | Khó xác định đầy đủ chức năng/dữ liệu bị ảnh hưởng; phạm vi dễ quá rộng |
| 3 | Viết nhận xét cá nhân hóa cho học viên (#1) | Lặp lại hằng ngày, baseline rõ (~30 phút/buổi, 1-2 buổi/ngày), người dùng dễ tiếp cận để kiểm chứng | Nhận xét "đủ cá nhân hóa" và chất lượng đo thế nào? Dữ liệu đầu vào về từng học viên có sẵn không? |

### Problem Card #1 — Tổng hợp yêu cầu mâu thuẫn từ nhiều phòng ban

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận yêu cầu từ nhiều phòng ban, tôi muốn tổng hợp và phát hiện các yêu cầu mâu thuẫn, để thiết kế hệ thống đúng ngay từ đầu |
| Actor | BA/PM phụ trách phân tích yêu cầu cho dự án hệ thống nội bộ |
| Thời điểm / bối cảnh | Giai đoạn thu thập yêu cầu, trước khi chốt thiết kế hệ thống |
| Quy trình hiện tại (3–7 bước) | 1. Họp/phỏng vấn từng phòng ban (kho, QA/QC, bảo trì, trưởng bộ phận…) · 2. Thu thập SOP, biên bản họp, file Excel · 3. Đọc và ghi chú từng tài liệu · 4. Đối chiếu yêu cầu giữa các phòng ban · 5. Ghi lại các điểm mâu thuẫn · 6. Hỏi lại các bên để xác nhận · 7. Chốt bảng yêu cầu |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 và 4, đọc tài liệu rồi đối chiếu chéo giữa các phòng ban: khoảng 6–12 giờ trong tổng 8–16 giờ (1–2 ngày) cho 4–6 phòng ban; số cặp cần đối chiếu tăng nhanh theo số phòng ban. Cần bấm giờ từng bước để xác nhận |
| Impact (nếu không giải thì sao) | Mất 1–2 ngày mỗi dự án chỉ để tổng hợp. Nếu bỏ sót mâu thuẫn, chỉ lộ ra khi dev/UAT và phải sửa thiết kế, làm lại. Cần đếm số lần đã xảy ra và tốn bao lâu để sửa (chưa có số liệu) |
| Success metric (baseline -> target) | Thời gian tổng hợp từ 1–2 ngày xuống dưới 4 giờ (BA vẫn kiểm tra lại); tỷ lệ mâu thuẫn AI gợi ý mà BA xác nhận là đúng ≥ 70%; số mâu thuẫn phát hiện muộn (sau khi chốt yêu cầu) giảm so với dự án trước. Baseline đo thật ở dự án tiếp theo |
| Phương án không dùng AI | Template bảng yêu cầu chuẩn theo phòng ban + ma trận đối chiếu (requirement × phòng ban) + checklist câu hỏi xác nhận |
| Giả thuyết về AI (nếu có) | AI đọc SOP, biên bản, Excel, trích yêu cầu theo phòng ban và gợi ý các cặp yêu cầu có khả năng mâu thuẫn kèm trích dẫn nguồn; BA kiểm tra và xác nhận với các bên |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 1-2 ngày

[1 Họp các phòng ban] -> [2 Thu thập SOP/biên bản/Excel]
-> [3 Đọc + ghi chú: ~3-5h] <- BOTTLENECK -> [4 Đối chiếu chéo: ~3-7h] <- BOTTLENECK
-> [5 Ghi điểm mâu thuẫn] -> [6 Hỏi lại các bên] -> [7 Chốt bảng yêu cầu]

(Thời gian từng bước là ước lượng, cần bấm giờ thật)
```

### Problem Card #2 — Quy trình đổi, hệ thống cập nhật chậm

| Trường | Nội dung |
|---|---|
| Job Story | Khi quy trình nghiệp vụ thay đổi trong lúc dự án đang phát triển, tôi muốn nhanh chóng xác định các chức năng, dữ liệu và tài liệu bị ảnh hưởng, để hệ thống luôn bám sát quy trình thực tế |
| Actor | BA/PM của dự án đang phát triển, cùng developer và các trưởng bộ phận dùng hệ thống |
| Thời điểm / bối cảnh | Quy trình nghiệp vụ thay đổi giữa chừng khi dự án đang phát triển |
| Quy trình hiện tại (3–7 bước) | 1. Bộ phận thông báo quy trình mới · 2. BA ghi nhận thay đổi · 3. Tự dò xem chức năng/dữ liệu/tài liệu nào bị ảnh hưởng · 4. Cập nhật tài liệu và yêu cầu cho dev · 5. Dev sửa hệ thống · 6. Test và triển khai · 7. Đối soát, làm sạch dữ liệu sai lệch |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5, xác định phạm vi ảnh hưởng và cập nhật hệ thống: hệ thống chậm 1–2 tuần so với quy trình; bước 7 tốn 4–8 giờ/tuần |
| Impact (nếu không giải thì sao) | Người dùng phải chạy quy trình mới trên hệ thống cũ, phát sinh lỗi chức năng và sai lệch dữ liệu; mất thêm 4–8 giờ/tuần để đối soát |
| Success metric (baseline -> target) | Độ trễ cập nhật từ 1–2 tuần xuống dưới 3 ngày; thời gian đối soát từ 4–8 giờ xuống dưới 2 giờ/tuần |
| Phương án không dùng AI | Ma trận truy vết (traceability) quy trình ↔ chức năng ↔ dữ liệu ↔ tài liệu, cùng quy trình change request bắt buộc có bước đánh giá ảnh hưởng |
| Giả thuyết về AI (nếu có) | AI so sánh mô tả quy trình cũ/mới với tài liệu và danh sách chức năng, gợi ý các mục có khả năng bị ảnh hưởng; BA xác nhận trước khi giao dev |
| Cảm nhận nhanh | Workflow hoặc Chưa biết (phụ thuộc có sẵn ma trận truy vết hay không) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — hệ thống trễ 1-2 tuần

[1 Thông báo quy trình mới] -> [2 BA ghi nhận] -> [3 Dò phạm vi ảnh hưởng] <- BOTTLENECK
-> [4 Cập nhật tài liệu/yêu cầu] -> [5 Dev sửa] -> [6 Test + triển khai]
-> [7 Đối soát, làm sạch dữ liệu: 4-8 giờ/tuần]
```

### Problem Card #3 — Viết nhận xét cá nhân hóa cho học viên

| Trường | Nội dung |
|---|---|
| Job Story | Khi kết thúc buổi học, tôi muốn viết nhận xét cá nhân hóa cho từng học viên mà không phải dành quá nhiều thời gian cho việc soạn báo cáo lặp lại, để phụ huynh nắm được tiến độ học tập |
| Actor | Giáo viên (có CM và phụ huynh là người nhận/kiểm tra) |
| Thời điểm / bối cảnh | Ngay sau mỗi buổi học, lớp 15–20 học viên, 1–2 buổi/ngày |
| Quy trình hiện tại (3–7 bước) | 1. Nhớ lại/xem ghi chú về từng học viên trong buổi · 2. Mở mẫu báo cáo · 3. Viết nhận xét từng em · 4. Chỉnh giọng văn, tránh trùng lặp · 5. CM duyệt · 6. Gửi phụ huynh |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 1 và 3, nhớ lại và viết nhận xét từng em: khoảng 30 phút/buổi (≈ 1,5–2 phút/em) |
| Impact (nếu không giải thì sao) | Mất khoảng 30–60 phút/ngày mỗi giáo viên; nhận xét dễ bị rập khuôn hoặc trễ, phụ huynh nắm tiến độ kém |
| Success metric (baseline -> target) | Thời gian soạn nhận xét từ 30 phút xuống dưới 10 phút/buổi; tỷ lệ nhận xét được CM duyệt không phải sửa lớn ≥ 80% |
| Phương án không dùng AI | Ngân hàng câu nhận xét theo mức độ/kỹ năng + form chấm nhanh (tick) sinh nhận xét theo mẫu |
| Giả thuyết về AI (nếu có) | AI soạn nháp nhận xét từ ghi chú ngắn/điểm từng học viên; giáo viên sửa và CM duyệt trước khi gửi |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~30 phút/buổi

[1 Nhớ lại/xem ghi chú] -> [2 Mở mẫu báo cáo] -> [3 Viết nhận xét từng em: ~20'] <- BOTTLENECK
-> [4 Chỉnh giọng văn] -> [5 CM duyệt] -> [6 Gửi phụ huynh]
```

### Card muốn pitch nhất

- Card số: #1 — Tổng hợp yêu cầu mâu thuẫn từ nhiều phòng ban
- Vì sao: Tốn 1–2 ngày/dự án, hậu quả lớn nếu sai từ đầu, quy trình có tài liệu đầu vào rõ để so sánh 4 mức can thiệp
- Câu hỏi muốn nhóm phản biện: AI chỉ gợi ý mâu thuẫn dựa trên văn bản thì có bỏ sót các mâu thuẫn ngầm (chỉ lộ ra khi hỏi trực tiếp các phòng ban) không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Bottleneck "1–2 ngày" gộp cả bước 3–5, chưa tách bước nào thật sự tốn nhất; chưa bấm giờ | Đồng ý | Tách bottleneck thành bước 3 và 4 với thời gian ước lượng từng bước, ghi rõ cần bấm giờ thật |
| Success metric "mâu thuẫn phát hiện muộn về gần 0" không thực tế và chưa có baseline | Đồng ý | Đổi thành "giảm so với dự án trước" và thêm chỉ số tỷ lệ gợi ý của AI được BA xác nhận đúng ≥ 70% |
| Impact chưa có bằng chứng về chi phí làm lại khi bỏ sót mâu thuẫn | Đồng ý | Ghi rõ cần đếm số lần và thời gian sửa; đưa vào danh sách giả định cần kiểm chứng ở CP4 |
| Nhiều mâu thuẫn chỉ lộ ra khi hỏi trực tiếp các phòng ban, AI đọc tài liệu có thể bỏ sót | Đồng ý một phần | Giữ bước 6 "hỏi lại các bên" do BA làm; AI chỉ gợi ý, không kết luận thay BA |

---

## 4. Tôi đã tham gia phần nào (CP3 -> CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch các statement của mình và tham gia phản biện | Đóng góp ý tưởng để mọi người sửa statement của mình |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | Chạy và sửa lỗi setup 10 phút/component, setup tổng 25 phút | Dùng template và helper chung có đủ giảm lỗi mà không cần AI không?, Nếu rubric chứa các tiêu chí định tính, không rõ ràng (như 'phân tích sâu sắc', 'ý tưởng sáng tạo') hoặc bài nộp là code/ảnh chứ không chỉ văn bản, làm sao đảm bảo AI không báo sai hoặc ảo giác?, Nếu nhà trường đã có FAQ hoặc chatbot RAG để tra cứu thông tin, tại sao cần xây dựng AI Agent? |
| Nhận phản biện | Câu hỏi tôi nhận được: Tại sao không dùng ChatGPT mà lại cần xây dựng sản phẩm mới?, Tại sao không dùng các công cụ có sẵn như NotebookLM? Làm sao để chứng minh sản phẩm có độ chính xác cao hơn?, Vấn đề hệ thống cập nhật chậm có thể do việc code, làm sao để chứng minh hiệu quả của việc sử dụng AI tổng hợp dữ liệu? | Tôi đã sửa gì: Sửa metric để so sánh, đánh giá lại bottleneck |
| Gom cluster / cây OST | Thảo luận với nhóm | Giúp nhóm tổng hợp pattern chung |
| Chọn candidate problem | Chia sẻ góc nhìn cá nhân | Củng cố lại lựa chọn vấn đề #4 của nhóm |
| Kiểm chứng / research | Hỗ trợ thiết kế câu hỏi interview | Giúp nhóm interview theo The Mom Test |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Đánh giá problem statement | Chỉ ra các phần trong statement viết còn mơ hồ hoặc chung chung | Đề xuất sửa chưa đủ chính xác và rõ ràng, thiếu dữ liệu và số liệu định lượng | Chia nhỏ pain point, thêm số liệu thật cho phần bằng chứng |
| CP2 Problem Card | Đề xuất các phương án kỹ thuật | Đưa ra một số hướng đi để có thể bắt đầu tìm hiểu | Chưa chi tiết và sát với vấn đề | Bắt đầu từ các gợi ý, tra google và hỏi AI để hiểu sâu hơn về các phương án trước khi chọn |
| CP4 Research | Đánh giá câu hỏi interview | Đánh giá xem câu hỏi đã đủ open chưa | Không có | Dựa vào các đề xuất của AI để bàn bạc với nhóm, chỉnh sửa câu hỏi |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Mình học được một vài điều khi nghe các bạn pitch problem. Đầu tiên, mình nhận ra có nhiều problem thực tế rất gần gũi nhưng mình lại không nghĩ đến lúc scan (VD vấn đề của bạn Quang và Giang về việc sắp xếp lịch học và làm bài tập). Có nhiều quy trình thực ra mình đang làm theo kiểu workaround mà không coi nó là pain point, nhưng các bạn khác thì có, từ đó suy ra pain point sẽ khác biệt theo từng nhóm đối tượng. Bên cạnh đó, mình cũng có thể so sánh cách các bạn viết problem statement và pitch, từ đó đối chiếu với cách mình làm để nhìn ra điểm cải thiện, đặc biệt là về phần dữ liệu thêm cho dấu hiệu thật. Cuối cùng, mình cũng học được các insight của các bạn khi tham gia phản biện, ví dụ như chia sẻ của bạn Dương về các nghiệp vụ trong coding và các bottleneck theo trải nghiệm của bạn. Những góc nhìn này giúp mình hiểu rằng một problem tốt không chỉ đúng với bản thân mà còn cần được kiểm chứng từ nhiều người khác nhau. Lần sau, trước khi chọn problem, mình sẽ chủ động hỏi thêm các bạn xung quanh để mở rộng góc nhìn và tránh chỉ dựa vào trải nghiệm riêng của mình.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có, thực tế đến từ chính mình. Khi bàn luận về vấn đề kiểm tra bài tập so với rubric, mình và cả nhóm đi chệch hướng và bắt đầu thảo luận về việc liệu rubric đó có được công khai không, hoặc làm sao để đọc thông tin bài và so với rubric nếu ở các định dạng file hoặc ảnh khác nhau. Nhóm mình mất khoảng 15 phút thảo luận về vấn đề này, tuy nhiên Quang đã chỉ ra mình cần xác nhận lại xem đây có đúng là pain point của những sinh viên khác không. Sau khi được chỉ ra thì nhóm mình đồng ý là đã đi theo hướng "solution-first" vì đang hỏi theo hướng "làm sao để..." mà không ai nhắc tới người dùng là ai hay họ có thật sự gặp vấn đề đó không, sau đó bắt đầu quay lại kiểm chứng vấn đề. Tiếp theo, nhóm mình đặt ra các giả định rồi đi phỏng vấn trong lớp để xác nhận lại, rồi mới đến các bước sau. Từ trải nghiệm này, mình rút ra được lần sau sẽ hỏi trước "ai là người đang thật sự gặp vấn đề", rồi mới bàn cách làm.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Có. Thực tế, khi mình pitch ý tưởng về việc muốn xác định chức năng, dữ liệu và tài liệu bị ảnh hưởng để hệ thống theo sát thực tế khi quy trình nghiệp vụ thay đổi, Giang đã nêu phản biện rằng có thể việc hệ thống cập nhật chậm là do phía lập trình chứ chưa chắc đã là do khâu tổng hợp và xử lý dữ liệu. Ban đầu thì mình chưa đồng ý lắm, vì theo ý kiến của mình vấn đề có thể đến từ cả hai, và nếu không sớm tổng hợp dữ liệu thì cũng không thể đặt ra được mô hình mới hoặc hệ thống lại các thay đổi cần implement, không thể bắt đầu code. Vậy nên có thể coi đó là bottleneck. Tuy nhiên, sau khi thảo luận thêm, mình nhận ra là việc tiết kiệm thời gian tổng hợp có thể giảm thời gian chậm trễ của hệ thống, nhưng có thể không đủ hiệu quả để giải quyết vấn đề. Theo trải nghiệm cá nhân của mình, kể cả khi có thể bắt đầu sớm, thời gian thực tế cần để đưa code mới vào vận hành vẫn sẽ chậm hơn thay đổi quy trình từ vài ngày cho đến 1 tuần. Đây là một phần lý do mình thấy cần thêm thời gian để đánh giá lại problem và không push nó thành vấn đề mà nhóm mình làm, và mình rút ra rằng lần sau sẽ kiểm chứng kĩ hơn trước khi khẳng định đâu là bottleneck.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Kết quả kiểm chứng của nhóm không thật sự khiến mình thấy bất ngờ. Khi mình nghe problem statement, mình ngay lập tức cảm thấy đây đúng là một vấn đề lớn mà bản thân mắc phải, và cũng đoán rằng sẽ có nhiều sinh viên khác có cùng trải nghiệm. Tuy nhiên, mình cũng không để những thiên kiến và giả định đó ảnh hưởng khi thiết kế bộ câu hỏi phỏng vấn cùng nhóm, mà vẫn cố gắng thiết kế các câu hỏi mở để có thể hiểu và đồng cảm với những người được phỏng vấn hơn. Khi đi phỏng vấn và được nghe chia sẻ, dù việc mọi người cũng gặp vấn đề tương tự không nằm ngoài dự đoán của mình, mình cũng học được thêm về một số cách mà các bạn đang dùng để workaround như nhờ bạn bè kiểm tra chéo hoặc tự đưa file cho LLM như ChatGPT check hộ. Những workaround này không làm nhóm mình thay đổi phương án, nhưng có ảnh hưởng đến việc bọn mình thiết kế giải pháp: làm sao để chứng minh sản phẩm của nhóm có giá trị hơn những cách mọi người đang sử dụng. Mặc dù số người phỏng vấn trực tiếp không phải lớn (chỉ có 2 người) nhưng cũng cho nhóm mình một số insight hữu ích.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Điều khó nhất đối với mình khi viết Problem Statement là việc follow theo đúng không thức "Khi..., muốn..., để...". Mình cảm thấy việc viết ra một câu như vậy thì không khó, thực tế có thể viết rất nhanh, nhưng điểm khó nằm ở việc viết như vậy đã đúng và đủ chưa. Ví dụ như với problem tổng hợp báo cáo nhận xét học sinh sau giờ học, version ban đầu của mình còn chưa nêu rõ được ý "để đỡ tốn thời gian" hay chưa nhấn mạnh được tính lặp lại của công việc (do đã nhận xét trực tiếp trên lớp rồi nhưng lại phải viết báo cáo lại y hệt). Ở phần này, mình đã phải cải thiện dần bằng cách viết đi viết lại và nhờ bạn cùng nhóm góp ý, sau đó đưa cho copilot và claude đánh giá dựa trên đúng mẫu trong phần 02-deliverable-example.md. Tuy gặp nhiều khó khăn, mình cũng thấy rằng đã học được nhiều thứ về cách viết Problem Statement rõ ràng, và có lẽ dù lần sau mình cũng không thấy nó dễ dàng hơn, nhưng ít nhất sẽ có thể luyện tập nhiều hơn để tăng kinh nghiệm.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu làm lại, mình sẽ thay đổi ở khá nhiều phần. Đầu tiên, ở phần CP1, mình cảm thấy chưa hoàn toàn hài lòng với cả 3 problem statement của mình. Do có giới hạn về thời gian và cần làm việc cùng nhóm, mình đã cố gắng scan đủ 5 problem dù chưa thật sự ưng ý. Nếu làm lại, mình sẽ muốn dồn sâu hơn vào 1 problem để làm thật tốt, vì đây sẽ là điểm bắt đầu trong việc nhận diện các pain point thực tế, ảnh hưởng đến cả các bước sau. Tiếp theo là ở phần problem card, chỗ này mình cũng thấy còn khá mơ hồ khi phải viết. Những thông tin về successful metric, bottleneck là những thứ mình thấy khá khó xác định, và thực tế mình nghĩ lần sau mình sẽ đi research nhiều hơn để có thể viết chính xác hơn. Về phần phản biện, mình thấy nhóm đã có nhiều câu hỏi rất hay, chạm được vào các góc nhìn khác nhau của các problem, cá nhân mình có thể sẽ phản biện mạnh hơn về các yếu tố liên quan đến metric, ví dụ làm sao để biết được metric đó có phản ánh đúng hiệu quả không.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem -> quy trình -> metric -> boundary -> mức can thiệp AI -> quyết định* của bài nhóm mình.
Problem nhóm quyết định đi theo là việc muốn đối chiếu bài làm với rubric trước hạn nộp để tránh bị mất điểm. Quy trình hiện tại của những người được phỏng vấn là đọc rubric, đối chiếu với các phần trong bài (bottleneck), note lại các lỗi hoặc thiếu, sau đó đi sửa lại. Metric nhóm dùng là giảm tổng thời gian mỗi lần nộp bài từ 60 phút xuống 20 phút và đảm bảo mức độ khớp người chấm >= 90%. Boundary là AI không được tự sửa bài mà phải do chính sinh viên sửa, không đưa ra điểm số thay cho giáo viên. Mức độ can thiệp của AI là Workflow (mơ hồ cao - phức tạp thấp) kết hợp Rule cho phần so sánh và định lượng và HITL để đánh giá các câu định tính. Quyết định cuối cùng là Not Yet, cần thực hiện kiểm chứng giới hạn với Workflow trước.
---

## 7. Tài liệu tham khảo

-
