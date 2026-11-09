# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:Nguyễn Thị Hương Giang
- MSSV:2A202603538
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:
- Link repo nhóm:

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
## Education – Problem Statements

| STT | Loại problem | Problem statement | Người liên quan | Tần suất / Thời gian / Tác động |
|---|---|---|---|---|
| 1 | Lặp lại | Khi kết thúc mỗi buổi học, tôi muốn tự động tổng hợp nội dung bài giảng, bài tập về nhà và gửi thông báo cho phụ huynh, để không phải soạn và gửi thông tin thủ công. | Giáo viên, phụ huynh | 2–3 lớp/ngày, khoảng 15 phút/lớp |
| 2 | Tốn thời gian | Khi cần xây dựng thời khóa biểu cho học kỳ mới, tôi muốn tự động đề xuất lịch học dựa trên lịch rảnh của giáo viên, phòng học và số tiết của từng môn, để hạn chế trùng lịch và không phải điều chỉnh thủ công nhiều lần. | Nhân viên giáo vụ, giáo viên, ban giám hiệu | Mỗi học kỳ 1 lần, khoảng 2–3 ngày để hoàn thiện và điều chỉnh thời khóa biểu |
| 3 | Cần đọc, tổng hợp nhiều thông tin, lặp lại | Khi kết thúc một học kỳ, tôi muốn tổng hợp điểm số, mức độ chuyên cần và kết quả học tập của từng học sinh, để xác định những em cần được hỗ trợ thêm, những em được khen thưởng và trả về báo cáo cho từng phụ huynh. | Giáo viên chủ nhiệm, ban giám hiệu | 30–40 học sinh/lớp, khoảng 2–3 giờ/lớp |
| 4 | Đọc và tổng hợp thông tin | Quản lý việc đưa đón học sinh: Nhà trường phải tổng hợp danh sách học sinh đi xe buýt, lịch nghỉ học, tuyến xe, điểm đón/trả và thông tin người được phép đón. Khi phụ huynh thay đổi người đón, học sinh nghỉ đột xuất hoặc thay đổi điểm đón, thông tin cần được cập nhật và thông báo kịp thời để tránh nhầm lẫn hoặc bàn giao sai người. | Nhân viên phụ trách xe, giáo viên chủ nhiệm, tài xế, phụ huynh | 5–10 tuyến xe/ngày; khoảng 30–45 phút/ngày để tổng hợp, kiểm tra và cập nhật thông tin |
| 5 | Pain từ người khác | Khi phụ huynh muốn tìm hiểu lịch học, học phí, quy định hoặc chương trình đào tạo, họ muốn nhận được câu trả lời nhanh và chính xác, để không phải liên hệ trực tiếp với nhà trường cho từng câu hỏi. | Phụ huynh, nhân viên tư vấn tuyển sinh | 20–30 câu hỏi/ngày, khoảng 5–10 phút/câu |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.
Không có dùng AI gợi ý them. chỉ dùng AI để kiểm tra lại những ý tưởng đã có
-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Giải đáp thắc mắc của phụ huynh (#5) | Nhiều câu hỏi lặp lại, quy trình dễ xác định, có thể xây dựng Knowledge Base để trả lời tự động và đo tỷ lệ trả lời đúng. | Tài liệu nhà trường có đầy đủ, cập nhật và thống nhất không? |
| 2 | Quản lý đưa đón học sinh (#4) | Liên quan trực tiếp đến an toàn học sinh, cần phối hợp thông tin giữa phụ huynh, giáo viên và nhân viên phụ trách xe. | Thông tin người đón, học sinh nghỉ và thay đổi lịch được cập nhật theo thời gian thực như thế nào? |
| 3 | Lập thời khóa biểu (#2) | Tốn thời gian, có nhiều ràng buộc về giáo viên, phòng học và tiết học; có tiềm năng tự động hóa. | Các ràng buộc có thể biểu diễn đầy đủ thành quy tắc không? Có cần thuật toán tối ưu hóa thay vì AI Agent không? |

### Problem Card #1 — Giải đáp thắc mắc của phụ huynh

| Trường | Nội dung |
|---|---|
| Job Story | Khi có thắc mắc về lịch học, học phí, chương trình học hoặc quy định nhà trường, tôi muốn nhận được câu trả lời nhanh và chính xác, để không phải liên hệ trực tiếp với nhân viên nhà trường cho từng vấn đề. |
| Actor | Phụ huynh học sinh; nhân viên tư vấn hoặc bộ phận chăm sóc phụ huynh |
| Thời điểm / bối cảnh | Trong ngày, đặc biệt vào đầu năm học, thời điểm đóng học phí, đăng ký hoạt động và khi có thay đổi lịch học. |
| Quy trình hiện tại (3–7 bước) | 1. Phụ huynh gửi câu hỏi qua điện thoại, Zalo hoặc email. 2. Nhân viên tiếp nhận và phân loại câu hỏi. 3. Tìm thông tin trong tài liệu hoặc hỏi bộ phận liên quan. 4. Soạn câu trả lời. 5. Gửi lại phụ huynh. 6. Nếu chưa giải quyết được, chuyển câu hỏi đến bộ phận phụ trách. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: Tìm kiếm và xác minh thông tin trong nhiều tài liệu hoặc hỏi các bộ phận khác, khoảng 3–5 phút/câu hỏi. |
| Impact (nếu không giải thì sao) | Nhân viên mất nhiều thời gian xử lý câu hỏi lặp lại; phụ huynh phải chờ phản hồi; thông tin có nguy cơ thiếu nhất quán giữa các nhân viên. |
| Success metric (baseline → target) | Thời gian phản hồi trung bình: 5–10 phút xuống dưới 2 phút đối với câu hỏi thông thường; tỷ lệ câu trả lời chính xác đạt ít nhất 95% trên bộ câu hỏi kiểm thử. |
| Phương án không dùng AI | Xây dựng trang FAQ, phân loại câu hỏi và chuẩn hóa câu trả lời theo từng chủ đề. |
| Giả thuyết về AI (nếu có) | Chatbot sử dụng RAG để truy xuất thông tin từ tài liệu chính thức của nhà trường, sau đó tạo câu trả lời bằng ngôn ngữ tự nhiên. Nếu không tìm thấy thông tin đáng tin cậy, chatbot chuyển câu hỏi cho nhân viên phụ trách. |
| Cảm nhận nhanh | Workflow + AI (RAG) + Database|

#### Quy trình nháp hiện tại

```text
PHỤ HUYNH CÓ THẮC MẮC
          |
          v
[1. Gửi câu hỏi qua Zalo / Email / Điện thoại]
          |
          v
[2. Nhân viên tiếp nhận và phân loại câu hỏi]
          |
          v
[3. Tìm kiếm thông tin trong tài liệu]
          |
          v
[4. Xác minh thông tin với bộ phận liên quan]
          |                 BOTTLENECK
          v
[5. Soạn câu trả lời]
          |
          v
[6. Gửi phản hồi cho phụ huynh]
          |
          v
[7. Kết thúc / Chuyển cấp xử lý nếu chưa giải quyết được]
```

### Problem Card #2 — Quản lý đưa đón học sinh

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu ngày học, tôi muốn nắm được danh sách học sinh đi xe, học sinh nghỉ, người đón và các thay đổi về điểm đón/trả, để đảm bảo mỗi học sinh được đưa đón đúng lịch và bàn giao đúng người. |
| Actor | Nhân viên phụ trách xe, tài xế, giáo viên chủ nhiệm và phụ huynh |
| Thời điểm / bối cảnh | Đầu giờ sáng và cuối giờ chiều; đặc biệt khi phụ huynh thông báo học sinh nghỉ, thay đổi người đón hoặc thay đổi điểm đón/trả. |
| Quy trình hiện tại (3–7 bước) | 1. Phụ huynh đăng ký dịch vụ xe đưa đón và cung cấp thông tin người được phép đón. 2. Phụ huynh thông báo học sinh nghỉ hoặc thay đổi lịch qua điện thoại/Zalo. 3. Nhân viên tiếp nhận và cập nhật thông tin. 4. Tổng hợp danh sách học sinh theo tuyến và điểm đón/trả. 5. Gửi danh sách cập nhật cho tài xế và giáo viên. 6. Tài xế đón/trả học sinh và xác nhận tình trạng bàn giao. 7. Xử lý các trường hợp thiếu thông tin hoặc thay đổi đột xuất. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5: Đối chiếu thông tin từ nhiều nguồn và cập nhật danh sách cho các bên liên quan, khoảng 30–45 phút/ngày. |
| Impact (nếu không giải thì sao) | Tài xế có thể sử dụng danh sách cũ; học sinh có thể bị đón sai điểm hoặc bỏ sót; giáo viên và phụ huynh khó nắm được tình trạng đưa đón; nguy cơ bàn giao học sinh không đúng người. |
| Success metric (baseline → target) | Thời gian tổng hợp danh sách: 30–45 phút xuống dưới 10 phút/ngày; 100% thay đổi người đón phải được xác minh trước khi bàn giao; giảm các trường hợp sai lệch thông tin so với quy trình hiện tại. |
| Phương án không dùng AI | Sử dụng biểu mẫu đăng ký và biểu mẫu thông báo nghỉ/thay đổi người đón; lưu dữ liệu tập trung và tự động cập nhật danh sách theo tuyến bằng các quy tắc cố định. |
| Giả thuyết về AI (nếu có) | AI Agent có thể tiếp nhận và phân loại thông báo bằng ngôn ngữ tự nhiên, ví dụ: học sinh nghỉ hôm nay, đổi người đón hoặc đổi điểm đón. Workflow cập nhật dữ liệu, kiểm tra các điều kiện và gửi thông báo đến những người liên quan. |
| Cảm nhận nhanh | Workflow + Database + AI Agent |

#### Quy trình nháp hiện tại

```text
PHỤ HUYNH ĐĂNG KÝ ĐƯA ĐÓN
          |
          v
[1. Cung cấp thông tin học sinh, tuyến xe và người được phép đón]
          |
          v
[2. Thông báo nghỉ học / thay đổi người đón / điểm đón]
          |
          v
[3. Nhân viên tiếp nhận và cập nhật thông tin]
          |                 BOTTLENECK
          v
[4. Tổng hợp danh sách học sinh theo tuyến]
          |
          v
[5. Gửi danh sách cho tài xế và giáo viên]
          |
          v
[6. Đón / trả học sinh và xác nhận bàn giao]
          |
          v
[7. Xử lý trường hợp bất thường hoặc thiếu xác nhận]
```

**Lưu ý:** AI không tự xác định người có quyền đón học sinh. Danh sách người được phép đón phải dựa trên thông tin phụ huynh đăng ký; các thay đổi bất thường cần nhân viên xác minh trước khi bàn giao.

### Problem Card #3 — Lập thời khóa biểu

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu học kỳ mới, tôi muốn xây dựng thời khóa biểu phù hợp với lịch dạy của giáo viên, số lượng phòng học và số tiết của từng môn, để hạn chế trùng lịch và giảm thời gian điều chỉnh thủ công. |
| Actor | Nhân viên phòng đào tạo, ban giám hiệu và giáo viên |
| Thời điểm / bối cảnh | Trước khi bắt đầu học kỳ hoặc khi có thay đổi về giáo viên, lớp học, phòng học và kế hoạch giảng dạy. |
| Quy trình hiện tại (3–7 bước) | 1. Thu thập kế hoạch giảng dạy và số tiết của từng môn. 2. Thu thập lịch rảnh/bận của giáo viên. 3. Kiểm tra số lượng phòng học và điều kiện sử dụng phòng. 4. Sắp xếp tiết học cho từng lớp. 5. Kiểm tra các trường hợp trùng giáo viên, phòng học hoặc lịch lớp. 6. Điều chỉnh thời khóa biểu. 7. Công bố thời khóa biểu cho giáo viên và học sinh. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–6: Sắp xếp và điều chỉnh lịch để thỏa mãn nhiều ràng buộc cùng lúc, ước tính 2–3 ngày làm việc cho một đợt lập thời khóa biểu. |
| Impact (nếu không giải thì sao) | Thời khóa biểu có thể bị trùng giáo viên hoặc phòng học; giáo viên và học sinh phải thay đổi lịch; phòng đào tạo mất nhiều thời gian xử lý các yêu cầu điều chỉnh. |
| Success metric (baseline → target) | Thời gian lập và điều chỉnh thời khóa biểu: 2–3 ngày xuống dưới 1 ngày; không có xung đột về giáo viên, phòng học và thời gian học trong thời khóa biểu được công bố. |
| Phương án không dùng AI | Sử dụng bảng dữ liệu tập trung và thuật toán lập lịch dựa trên các ràng buộc cố định; tự động cảnh báo khi có trùng lịch. |
| Giả thuyết về AI (nếu có) | AI hỗ trợ đọc và chuẩn hóa yêu cầu lập lịch từ nhiều nguồn, nhận diện các ràng buộc và đề xuất phương án sắp xếp. Thuật toán tối ưu hóa có thể được sử dụng để tìm thời khóa biểu thỏa mãn các ràng buộc cứng và tối ưu các tiêu chí mềm. |
| Cảm nhận nhanh | Rule + Workflow + Optimization Algorithm |

#### Quy trình nháp hiện tại

```text
BẮT ĐẦU HỌC KỲ MỚI
          |
          v
[1. Thu thập kế hoạch giảng dạy và số tiết từng môn]
          |
          v
[2. Thu thập lịch rảnh/bận của giáo viên]
          |
          v
[3. Kiểm tra số lượng và điều kiện phòng học]
          |
          v
[4. Sắp xếp thời khóa biểu cho từng lớp]
          |                 BOTTLENECK
          v
[5. Kiểm tra trùng lịch giáo viên / phòng học / lớp]
          |
          v
[6. Điều chỉnh các lịch bị xung đột]
          |
          v
[7. Công bố thời khóa biểu]
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: dễ triển khai và giá thành thấp nhất nhóm. Card này sử dụng dữ liệu riêng của nhà trường (rule, lịch học, tư vấn...) nên sẽ cần hệ thống riêng để đảm bảo trả lời chính xác. Card này cũng có thể giải quyết một số vấn đề của card khác như lịch đưa đón, phụ huynh đăng kí đưa đón, thành tích học tập...
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Giải đáp thắc mắc phụ huynh bằng FAQ hoặc chatbot RAG đã có nhiều giải pháp tương tự. Cần làm rõ điểm khác biệt của đề xuất. | Đồng ý | Tập trung vào khả năng truy xuất thông tin từ tài liệu chính thức của nhà trường, cung cấp câu trả lời có căn cứ thay vì chỉ xây dựng chatbot FAQ thông thường. |
| Chất lượng câu trả lời phụ thuộc vào Knowledge Base. Nếu tài liệu thiếu, lỗi thời hoặc có thông tin mâu thuẫn, chatbot có thể trả lời sai. | Đồng ý | Bổ sung yêu cầu quản lý và cập nhật tài liệu. Chatbot cần thông báo khi không tìm thấy thông tin đáng tin cậy, không tự suy đoán câu trả lời. |
| Không phải câu hỏi nào của phụ huynh cũng có thể tự động trả lời. Một số trường hợp cần nhân viên nhà trường tham gia xử lý. | Đồng ý | Bổ sung cơ chế Human-in-the-loop: chatbot trả lời các câu hỏi thông thường và chuyển câu hỏi phức tạp, cần xác minh hoặc xử lý riêng cho nhân viên phụ trách. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

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

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Sử dụng AI để kiểm tra lại các vấn đề đã quan sát và ghi nhận, không dùng AI để tạo ra ý tưởng hoặc đề xuất vấn đề mới. | Giúp rà soát cách diễn đạt, kiểm tra xem vấn đề đã được mô tả rõ ràng và có hợp lý hay chưa. | AI có thể đưa ra nhận xét chung chung, chưa nắm được đầy đủ bối cảnh thực tế của nhà trường. | Giữ các vấn đề xuất phát từ quá trình quan sát và thảo luận; chỉ tiếp thu góp ý phù hợp để chỉnh sửa cách diễn đạt. |
| CP2 Problem Card | Nhờ AI rà soát nội dung Problem Card, kiểm tra các thành phần như đối tượng, bối cảnh, quy trình hiện tại, bottleneck và tác động của vấn đề. | Giúp phát hiện những thông tin còn thiếu, điểm chưa rõ trong quy trình và các giả định chưa được làm rõ. | Một số nhận xét còn mang tính suy đoán, chưa có dữ liệu thực tế để chứng minh. | Điều chỉnh nội dung Problem Card, phân biệt thông tin đã có với giả định; không xem các con số ước tính là dữ liệu đã được xác thực. |
| CP4 Research | Sử dụng AI để hỗ trợ tìm hiểu, tổng hợp và so sánh các giải pháp hiện có liên quan đến vấn đề. | Giúp hệ thống hóa thông tin, nhận diện các hướng tiếp cận và rút ra những điểm có thể tham khảo cho giải pháp. | Thông tin có thể chưa đầy đủ hoặc chưa sát với bối cảnh Vinschool; việc liệt kê công cụ chưa đủ để chứng minh giải pháp phù hợp. | Tập trung vào chức năng thực sự liên quan đến bài toán, xem xét khả năng áp dụng trong bối cảnh nhà trường thay vì chỉ dựa vào mô tả của AI. |
| CP5 Quy trình | Nhờ AI hỗ trợ rà soát Current-State Flow và Future-State Flow, kiểm tra các bước xử lý, điểm bottleneck, handoff và vị trí có thể ứng dụng AI. | Giúp phát hiện các bước còn thiếu, làm rõ sự khác biệt giữa quy trình hiện tại và quy trình đề xuất. | AI có xu hướng đề xuất tự động hóa nhiều bước mà chưa xét đến dữ liệu đầu vào, ngoại lệ và trách nhiệm của nhân viên. | Giữ lại các bước cần con người xác minh, bổ sung cơ chế chuyển tiếp cho trường hợp AI không đủ thông tin và không tự động hóa những bước chưa phù hợp. |
| CP5–6 Problem Statement | Sử dụng AI để rà soát cách diễn đạt Problem Statement, kiểm tra sự liên kết giữa vấn đề, đối tượng bị ảnh hưởng, nguyên nhân và tác động. | Giúp câu mô tả vấn đề rõ ràng, tập trung hơn và tránh đưa giải pháp vào quá sớm khi chưa xác định đúng vấn đề. | AI đôi khi diễn đạt vấn đề quá rộng hoặc chuyển trọng tâm sang giải pháp AI thay vì nhu cầu thực tế của người dùng. | Chỉnh lại Problem Statement để tập trung vào khó khăn của phụ huynh và nhân viên nhà trường, không mặc định rằng chatbot là giải pháp duy nhất. |
| CP6 Mức can thiệp / quyết định | Nhờ AI hỗ trợ phân tích mức độ phù hợp của AI trong từng bước và rà soát các rủi ro khi triển khai. | Giúp phân biệt những công việc có thể tự động hóa, những công việc AI chỉ nên hỗ trợ và những bước cần con người quyết định. | AI có thể đánh giá quá cao khả năng tự xử lý, chưa xem xét đầy đủ độ tin cậy của dữ liệu và hậu quả khi trả lời sai. | Lựa chọn hướng Workflow + RAG, giới hạn AI ở các câu hỏi có thông tin chính thức để truy xuất; các trường hợp thiếu dữ liệu, phức tạp hoặc cần xác minh được chuyển cho nhân viên nhà trường. |

---

## 6. Reflection

### 6.1. Mình học được gì từ các Problem Pitch của thành viên khác?

Mình nhận ra không phải vấn đề nào tốn thời gian cũng cần AI giải quyết. Một số vấn đề có thể xử lý đơn giản bằng công cụ hoặc quy trình sẵn có. Vì vậy, cần xác định đúng nguyên nhân trước khi nghĩ đến giải pháp.

### 6.2. Nhóm có lúc nào đi từ giải pháp trước rồi mới tìm vấn đề không?

Có. Khi trao đổi về bài toán rubric, nhóm mình ban đầu tập trung khá nhiều vào cách đọc và xử lý bài làm ở các định dạng khác nhau, cũng như việc tiếp cận rubric. Sau đó, Quang nhắc nhóm cần quay lại xác định liệu sinh viên có thực sự gặp khó khăn này hay không. Nhóm nhận ra mình đã quá tập trung vào cách triển khai mà chưa hiểu rõ người dùng và vấn đề của họ. Vì vậy, nhóm chuyển sang đặt giả định và phỏng vấn sinh viên để kiểm chứng trước khi tiếp tục xây dựng giải pháp.

### 6.3. Phản biện nào khiến mình thay đổi cách nhìn về Problem Card?

Khi mình trình bày bài toán hỗ trợ phụ huynh Vinschool, Cương đặt câu hỏi: nếu trường đã có FAQ hoặc RAG thì tại sao cần xây dựng AI Agent? Điều này khiến mình nhận ra cần làm rõ hạn chế của giải pháp hiện tại trước khi đề xuất AI.

### 6.4. Kết quả kiểm chứng có khiến mình bất ngờ không?

Có. Nhóm nhận thấy việc kiểm tra bài theo rubric mất khá nhiều thời gian, nhưng một số sinh viên vẫn thấy tự kiểm tra hoặc nhờ bạn bè là đủ. Điều đó cho thấy AI chưa chắc là lựa chọn tốt nhất cho tất cả trường hợp.

### 6.5. Phần nào trong Problem Statement khiến mình khó khăn nhất?

Với bài toán phụ huynh Vinschool, khó nhất là xác định vấn đề thực sự nằm ở đâu: phụ huynh khó tìm thông tin, thông tin chưa thống nhất hay cần nhân viên hỗ trợ trực tiếp. Mình cần phân biệt rõ vấn đề đã có bằng chứng và những giả định cần kiểm chứng.

### 6.6. Sau buổi học, mình sẽ thay đổi cách tiếp cận như thế nào?

Mình sẽ tập trung tìm hiểu quy trình và khó khăn của người dùng trước khi đề xuất giải pháp. Với bài toán phụ huynh, cần kiểm tra xem FAQ/RAG hiện tại còn thiếu sót gì; với bài toán nhóm, cần kiểm chứng độ chính xác của AI khi đối chiếu rubric.

### 6.7. Tóm tắt toàn bộ quá trình làm việc của nhóm

Nhóm chọn bài toán hỗ trợ sinh viên đối chiếu bài làm với rubric trước khi nộp. Qua phân tích, nhóm xác định bước tìm minh chứng và so sánh với rubric là bottleneck, khiến quy trình ước tính mất khoảng 55–60 phút. Nhóm đề xuất dùng Rule để kiểm tra cấu trúc và AI để phân tích nội dung, đưa ra minh chứng cho từng tiêu chí. Sinh viên vẫn là người xem xét và quyết định chỉnh sửa; AI không chấm điểm hay tự nộp bài. Nhóm chọn hướng Workflow kết hợp Human-in-the-loop, nhưng quyết định **Not Yet** vì chưa có đủ dữ liệu và kết quả thử nghiệm để chứng minh hiệu quả.
---

## 7. Tài liệu tham khảo

- Các nguồn research đã liệt kê tại mục 3.3: FeedbackFruits — Self-Assessment, Turnitin Clarity — AI Tools, OpenAI — Assessment and Feedback, Gradescope.
