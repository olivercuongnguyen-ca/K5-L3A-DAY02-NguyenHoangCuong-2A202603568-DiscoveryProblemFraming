# Báo cáo cá nhân — 2A202603524_NguyenTrieuDuong

> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Triều Dương
- MSSV: 2A202603524
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:
- Link repo nhóm: https://github.com/olivercuongnguyen-ca/K5-L3A-DAY02-NguyenHoangCuong-2A202603568-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Pain từ người khác | Khi gửi Pull Request (PR) để Senior/Tech Lead review, tôi muốn đáp ứng các yêu cầu về convention và type ngay từ lần gửi đầu, để giảm số vòng sửa và thời gian chờ merge. | Fresher Dev, Tech Lead | PR thường kéo dài 2–3 vòng review, mất 1–2 ngày mới được merge do lỗi convention hoặc thiếu type. |
| 2 | Tốn thời gian | Khi tích hợp một API mới từ Backend vào component React, tôi muốn hiểu rõ cấu trúc payload và response, để triển khai đúng mà không phải hỏi lại nhiều lần qua Slack. | Frontend Dev, Backend Dev | Tốn trung bình 15–20 phút nhắn hỏi/trao đổi lại mỗi endpoint mới, khoảng 3–4 lần/tuần. |
| 3 | Lặp lại | Khi triển khai giao diện mới theo thiết kế Figma, tôi muốn xác định đúng màu sắc, spacing và typography tương ứng trong dự án, để giảm thời gian tra cứu và đối chiếu thủ công từng thông số. | Frontend Dev, Designer | Mất 20 phút/màn hình mới: 10 phút tra thông số và 10 phút đối chiếu token/class. |
| 4 | Tốn thời gian | Khi tự kiểm tra tính năng trên các kích thước màn hình khác nhau trước khi bàn giao QA, tôi muốn phát hiện các lỗi vỡ layout hoặc lỗi hiển thị khó thấy, để giảm số lần bị trả task để sửa giao diện. | Frontend Dev, QA | QA thường trả về 3–5 bug liên quan đến UI/responsive ở mỗi task hoàn thành. |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi gặp lỗi TypeScript phức tạp hoặc lỗi build cho môi trường production, tôi muốn xác định nhanh nguyên nhân gốc rễ từ thông báo lỗi và các tài liệu liên quan, để tránh bị nghẽn tiến độ sprint. | Frontend Dev | Mất 30–60 phút cho mỗi lỗi build/type phức tạp chưa từng gặp. |
| 6 | Lặp lại | Khi viết unit test cho component React phức tạp, tôi muốn chuẩn bị dữ liệu mock và môi trường kiểm thử nhất quán với ít thao tác lặp lại, để dành nhiều thời gian hơn cho các tình huống kiểm thử của component. | Frontend Dev | Mất 25 phút setup/component phức tạp, gồm 10 phút chạy và sửa lỗi setup; viết test nghiệp vụ mất thêm 20 phút, tổng 45 phút. |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Sáu problem và số liệu ban đầu do tôi cung cấp. AI hỗ trợ rà soát và đề xuất chỉnh cách diễn đạt Job Story, không bổ sung ý mới.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

CP1 và CP2 dùng số liệu thời gian đã được học viên cập nhật. Target là mục tiêu cải thiện.

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | #2 — Làm rõ payload/response khi tích hợp API | Actor rõ; có thời gian 15–20 phút/endpoint và tần suất 3–4 lần/tuần; kiểm chứng được trên phạm vi vài endpoint. | Thời gian đã gồm chờ Backend hay chỉ trao đổi chủ động? Tài liệu hiện tại thiếu gì? |
| 2 | #3 — Đối chiếu Figma với style trong dự án | Actor rõ; đã có thời gian từng bước; so sánh được với giải pháp tài liệu và quy ước dùng chung. | Chuẩn hóa token có giảm được cả thời gian đối chiếu và kiểm tra giao diện không? |
| 3 | #6 — Chuẩn bị môi trường và mock cho unit test | Thao tác lặp lại; tách được setup khỏi viết test logic; có thể thử template/helper trên phạm vi nhỏ. | Template/helper dùng chung được cho những nhóm component nào? |

### Problem Card #1 — Làm rõ payload/response khi tích hợp API (CP1 #2)

| Trường | Nội dung |
|---|---|
| Job Story | Khi tích hợp một API mới từ Backend vào component React, tôi muốn hiểu rõ cấu trúc payload và response, để triển khai đúng mà không phải hỏi lại nhiều lần qua Slack. |
| Actor | Frontend Dev tích hợp endpoint; Backend Dev giải đáp cấu trúc dữ liệu. |
| Thời điểm / bối cảnh | Nhận endpoint mới và chuẩn bị nối dữ liệu vào component React. |
| Quy trình hiện tại (3–7 bước) | Nhận endpoint → đọc tài liệu → trao đổi làm rõ với Backend → khai báo type và tích hợp → kiểm tra response. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: trao đổi làm rõ payload/response, 15 phút theo quy trình chi tiết; CP1 ghi khoảng 15–20 phút. Bước 4 tích hợp cũng mất 15 phút; chọn bước 3 làm điểm tập trung vì có thao tác hỏi lại. Khi đo, ghi riêng thời gian chờ và thời gian trao đổi chủ động. |
| Impact (nếu không giải thì sao) | Hỏi lại mỗi endpoint, ngắt quãng công việc hai bên. Riêng trao đổi khoảng 45–80 phút/tuần, tính từ số liệu CP1: 15–20 phút × 3–4 lần; không phải tổng thời gian tích hợp. |
| Success metric (baseline → target) | Baseline chi tiết: 15 phút làm rõ/endpoint → target ≤10 phút/endpoint, số lỗi do hiểu sai payload không tăng trên cùng số endpoint so sánh. Đo trên 5 endpoint mới, ghi riêng thời gian chờ và thời gian trao đổi chủ động, dùng cùng cách đo trước/sau. |
| Phương án không dùng AI | Thống nhất tài liệu API có ví dụ request/response, type, trường bắt buộc/nullable và mã lỗi; cập nhật khi endpoint thay đổi. |
| Giả thuyết về AI (nếu có) | Nếu tài liệu đã có nhưng khó tra cứu, có thể thử hỗ trợ trích cấu trúc từ tài liệu được phép sử dụng. Dev phải đối chiếu với API thực tế, không chấp nhận trường dữ liệu do AI suy đoán. Chưa có bằng chứng cần AI. |
| Cảm nhận nhanh | No AI — ưu tiên làm rõ hợp đồng dữ liệu và cách cập nhật tài liệu; chưa chốt mức can thiệp. |

Quy trình nháp hiện tại:

```text
[1. Nhận endpoint: 5 phút]
 → [2. Đọc tài liệu và ví dụ: 5 phút]
 → [3. Trao đổi làm rõ với Backend: 15 phút] ← BOTTLENECK
 → [4. Khai báo type và tích hợp: 15 phút]
 → [5. Kiểm tra response: 10 phút]
Tổng: 50 phút/endpoint, theo các bước đã điền.
Phần làm rõ API: 15 phút; chưa tách thời gian chờ và trao đổi chủ động.
```

### Problem Card #2 — Đối chiếu Figma với style trong dự án (CP1 #3)

| Trường | Nội dung |
|---|---|
| Job Story | Khi triển khai giao diện mới theo thiết kế Figma, tôi muốn xác định đúng màu sắc, spacing và typography tương ứng trong dự án, để giảm thời gian tra cứu và đối chiếu thủ công từng thông số. |
| Actor | Frontend Dev triển khai giao diện; Designer giải thích thông số chưa rõ. |
| Thời điểm / bối cảnh | Bắt đầu một màn hình mới từ thiết kế Figma, cần xác định style trước khi triển khai. |
| Quy trình hiện tại (3–7 bước) | Mở màn hình Figma → tra thông số → đối chiếu token/class → áp dụng style → kiểm tra với thiết kế. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước dài nhất theo quy trình: kiểm tra với thiết kế (bước 5), 15 phút/màn hình. Đối chiếu token/class (bước 3) mất 10 phút, là điểm tập trung của problem nhưng chưa có bằng chứng đây là nguyên nhân khiến bước kiểm tra kéo dài. |
| Impact (nếu không giải thì sao) | Quy trình mất 50 phút/màn hình; riêng tra cứu + đối chiếu là 20 phút (10 + 10), kiểm tra với thiết kế là 15 phút. |
| Success metric (baseline → target) | Baseline theo thời gian chi tiết: tra cứu + đối chiếu 20 phút/màn hình → target đề xuất ≤10 phút; kiểm tra với thiết kế 15 phút → target đề xuất ≤10 phút. Đo riêng hai phần trên 5 màn hình tương đương, ghi số sai lệch màu/spacing/typography để tránh tăng tốc nhưng tăng lỗi. |
| Phương án không dùng AI | Thống nhất tên token giữa thiết kế và code; tạo bảng đối chiếu token/class dùng chung và ví dụ; làm rõ cách xử lý giá trị chưa có token. |
| Giả thuyết về AI (nếu có) | Chỉ cân nhắc gợi ý token nếu tên gọi khó khớp. Nếu ánh xạ cố định, bảng tra hoặc rule có thể đủ. |
| Cảm nhận nhanh | No AI / Rule — cần kiểm tra tính nhất quán của token trước khi chọn. |

Quy trình nháp hiện tại:

```text
[1. Mở màn hình Figma: 5 phút]
 → [2. Tra màu, spacing, typography: 10 phút]
 → [3. Đối chiếu token/class: 10 phút] ← Điểm tập trung của problem
 → [4. Áp dụng style: 10 phút]
 → [5. Kiểm tra với thiết kế: 15 phút] ← BOTTLENECK
Tổng: 50 phút/màn hình. Riêng bước 2 + 3: 20 phút.

```

### Problem Card #3 — Chuẩn bị môi trường và mock cho unit test (CP1 #6)

| Trường | Nội dung |
|---|---|
| Job Story | Khi viết unit test cho component React phức tạp, tôi muốn chuẩn bị dữ liệu mock và môi trường kiểm thử nhất quán với ít thao tác lặp lại, để dành nhiều thời gian hơn cho các tình huống kiểm thử của component. |
| Actor | Frontend Dev viết unit test cho component React. |
| Thời điểm / bối cảnh | Bắt đầu file test cho component phức tạp có dữ liệu hoặc phụ thuộc cần mock. |
| Quy trình hiện tại (3–7 bước) | Xác định phụ thuộc → tạo file test/import → chuẩn bị wrapper/mock → chạy và sửa lỗi setup → viết test case nghiệp vụ. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4: chạy và sửa lỗi setup, 10 phút/component; đây là bước khiến học viên phải dừng lại hoặc làm lại nhiều nhất trong phần setup. Viết test nghiệp vụ (20 phút) nằm ngoài metric setup. |
| Impact (nếu không giải thì sao) | Setup bước 1–4 mất 25 phút/component, trong đó chạy và sửa lỗi setup chiếm 10 phút; toàn quy trình gồm viết test là 45 phút. Thời gian chuẩn bị lặp lại làm giảm thời gian dành cho test nghiệp vụ. |
| Success metric (baseline → target) | Setup 25 phút/component → target đề xuất ≤15 phút; riêng chạy và sửa lỗi setup 10 phút → ≤5 phút. Đo trên 5 component cùng nhóm phụ thuộc, từ bắt đầu chuẩn bị đến khi kiểm tra setup tối thiểu chạy được; loại thời gian viết test nghiệp vụ khỏi cả hai lần đo. |
| Phương án không dùng AI | Tạo template file test, helper render với provider và fixture/mock dùng chung theo nhóm component; cho phép tùy chỉnh phụ thuộc riêng. |
| Giả thuyết về AI (nếu có) | Chỉ thử hỗ trợ phác thảo mock cho trường hợp chưa có helper nếu template không đủ. Dev kiểm tra mock phản ánh đúng hành vi; test chạy được chưa chứng minh mock đúng. |
| Cảm nhận nhanh | Rule — thử template/helper trước; chưa có bằng chứng cần Workflow hoặc Agent. |

Quy trình nháp hiện tại:

```text
[1. Xác định phụ thuộc: 5 phút]
 → [2. Tạo file test/import: 5 phút]
 → [3. Chuẩn bị wrapper/mock: 5 phút]
 → [4. Chạy và sửa lỗi setup: 10 phút] ← BOTTLENECK
 → [5. Viết test case nghiệp vụ: 20 phút; ngoài metric setup]
Tổng: 45 phút/component; setup bước 1–4: 25 phút; viết test: 20 phút.

```

### Card muốn pitch nhất

- Card số: #1 — Tích hợp API.
- Vì sao: Có thời gian và tần suất từ CP1, actor rõ, phạm vi kiểm chứng nhỏ. Cần phân biệt vấn đề tài liệu với thời gian chờ phản hồi.
- Câu hỏi muốn nhóm phản biện: Nếu chuẩn hóa tài liệu API và ví dụ request/response thì đã đủ giảm trao đổi chưa, hay bottleneck thật sự nằm ở việc chờ Backend phản hồi?

### AI đã phản biện card thế nào

**AI phản biện card #1 — Làm rõ payload/response khi tích hợp API:**

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 15–20 phút/endpoint chưa phân biệt thời gian chờ Backend với thời gian chủ động trao đổi, nên chưa xác định đúng phần có thể cải thiện. | Đồng ý | Trong bottleneck và success metric, tách hai loại thời gian cần đo; dùng 15 phút từ quy trình chi tiết làm baseline và theo dõi hai loại thời gian riêng khi đo trước/sau. |
| Target ≤10 phút/endpoint chưa có dữ liệu chứng minh khả thi hoặc kiểm soát việc hiểu sai payload. | Đồng ý  | Card đã ghi rõ target đề xuất và cách theo dõi lỗi hiểu sai payload trên 5 endpoint mới. Chưa có kết quả đo để khẳng định đạt target. |
| Chưa chứng minh cần AI: nếu nguyên nhân là tài liệu API thiếu hoặc không được cập nhật, AI có thể tiếp tục đưa thông tin sai. | Không đồng ý | Giữ giả thuyết AI hỗ trợ tra cứu khi tài liệu đã có, kèm bước đối chiếu API thực tế. Giữ No AI là phương án thử trước; AI vẫn là giả thuyết so sánh, không phải lựa chọn đã chốt. |

---
## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày ba candidate: làm rõ payload/response API, đối chiếu Figma/token và chuẩn bị unit test React. | Candidate API và unit test vào shortlist, lần lượt 26 và 28 điểm; nhóm chọn bài đối chiếu rubric của Quang. |
| Phản biện bài của bạn khác | Hỏi Quang vì sao cần AI khi đã có When2meet/Doodle; hỏi Giang cách chứng minh lợi ích lớn hơn chi phí; hỏi Cương vì sao không dùng NotebookLM. | Đưa phương án có sẵn và mức can thiệp đơn giản vào thảo luận; câu hỏi chốt lịch phù hợp với lựa chọn No AI/Rule của Quang. |
| Nhận phản biện | Quang hỏi thời gian làm rõ API do tài liệu hay chờ Backend; Giang hỏi đối chiếu token hay kiểm tra giao diện mới nghẽn; Cương hỏi template/helper có đủ cho unit test không. | Bổ sung cách đo tách thời gian chờ và trao đổi; làm rõ thời gian các bước và phương án không AI, tránh mặc định chọn AI. |
| Gom cluster / cây OST | Đưa ba candidate của mình vào phần thảo luận và phân nhóm vấn đề. | API và Figma thuộc cluster A; unit test thuộc cluster C. |
| Chọn candidate problem | Tham gia phần chọn candidate cùng nhóm, không có bất đồng được ghi nhận. | Chọn bài đối chiếu rubric của Quang, 34/35 điểm; hai candidate của tôi không được chọn. |
| Kiểm chứng / research | Đối chiếu kết quả phỏng vấn, poll và research trong CP4 với các giả định và rủi ro ở CP6. | Phân biệt tín hiệu có nhu cầu với bằng chứng AI tốt hơn checklist; đưa khoảng trống kiểm chứng vào rủi ro và bước tiếp theo. |
| Quy trình nhóm | Dùng quy trình CP5 để xác định bước Rule, bước AI hỗ trợ và bước cần con người kiểm tra trong CP6. | AI hỗ trợ đối chiếu ngữ nghĩa; Rule kiểm tra cấu trúc; sinh viên kiểm tra, tự sửa và tự nộp. |
| Problem Statement | Phụ trách phần Problem Statement v1 trong CP6, có AI hỗ trợ bản nháp và rà soát sự khác biệt với v0. | Bổ sung intervention point, mức chọn, rủi ro/người kiểm tra và năm tiêu chí eval; làm rõ target chưa phải kết quả đã đạt. |
| Mức can thiệp AI | Phụ trách CP6: so sánh No AI/Rule/Workflow/Agent, AI Canvas và hai câu PAIR; yêu cầu giữ format và yêu cầu gốc của lab. | Hướng đề xuất là Workflow có Rule và human-in-the-loop; checklist là đối chứng và phương án quay về, không chọn Agent. |
| Quyết định | Phụ trách phân tích bốn rủi ro và nội dung đề xuất Not Yet; yêu cầu AI hỗ trợ rà soát và chạy thử giới hạn. | Có ngưỡng dừng và kế hoạch kiểm chứng; dry run chưa có nhãn người chấm độc lập hoặc thời gian đối chứng, nên chưa đủ chuyển Go. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI rà soát 6 problem tự liệt kê và đề xuất chỉnh Job Story. | Chỉ ra dòng 3 và 6 đang gắn với cách giải; đề xuất diễn đạt theo nhu cầu. | AI chưa kiểm chứng được số liệu hoặc nguồn bằng chứng thực tế. | Cần tự kiểm tra bản chỉnh và bổ sung nguồn, thời gian quan sát cho số liệu. |
| CP2 Problem Card | Nhờ AI đề xuất top 3, hỗ trợ dựng card/quy trình và phản biện; đã chọn #2, #3, #6. | Tính tổng từ thời gian đã điền; phân biệt setup với viết test; chỉ ra baseline CP1/CP2 chưa khớp. | Bản nháp ban đầu gán bottleneck khi chưa có thời gian từng bước; target vẫn là đề xuất chưa kiểm chứng. | Đã bổ sung thời gian và mức đồng ý với phản biện; dùng thời gian chi tiết cho metric CP2, tách setup khỏi viết test và giữ phương án đơn giản để so sánh. |
| CP4 Research | Không nhờ AI tìm nguồn research riêng trong phần việc của tôi; dùng nội dung CP4 đã có để làm CP6. | Giúp nhận diện phần bằng chứng còn thiếu khi rà CP6. | Không thể coi việc đọc nguồn nhóm đã ghi là tự kiểm tra lại mọi link. | Không khai nhận phỏng vấn hoặc research thay người thực hiện. |
| CP5 Quy trình | Dùng quy trình đã có làm đầu vào CP6, không nhờ AI dựng lại CP5. | Giúp phân biệt bước Rule, AI và con người. | AI ban đầu sửa cả phần CP trước ngoài phạm vi tôi muốn. | Yêu cầu giữ nguyên các CP trước, chỉ hoàn thiện phần phụ trách. |
| CP5–6 Problem Statement | Nhờ AI hỗ trợ bản nháp v1 và rà baseline, target, boundary, eval. | Chỉ ra số mẫu và baseline chưa nhất quán; đề xuất cách đo chất lượng đối chiếu. | AI tham gia soạn nháp nhiều hơn vai trò chỉ phản biện mà RULES.md cho phép; bản nháp không thay thế lập luận và quyết định của nhóm. | Yêu cầu giữ template, phân biệt dữ liệu thật và mục tiêu; nhóm cần tự rà và chốt v1. |
| CP6 Mức can thiệp / quyết định | Nhờ AI so sánh các mức, đề xuất quyết định và chạy dry run trên năm báo cáo trong repo. | Có bảng rủi ro, ngưỡng dừng, nhận xét kèm vị trí minh chứng. | Dry run mới xét 11/26 cặp báo cáo–tiêu chí; chưa có người chấm độc lập hoặc đo thời gian người dùng. AI tạo quá nhiều file không cần cho lab. | Yêu cầu đối chiếu lại yêu cầu lab và bỏ các file không cần thiết. Không coi dry run là bằng chứng đạt ≥90% hoặc đủ để chuyển Go. |
| CP7 Reflection | Nhờ AI hỗ trợ bản nháp và biên tập; cung cấp nội dung trải nghiệm ở 6.2 và ý giải thích ở 6.7, sau đó yêu cầu chỉnh theo vai trò CP6. | Giúp tổ chức nội dung theo tình huống, phản biện, thay đổi và bài học. | Các phần mở rộng từ báo cáo vẫn có AI soạn; không chứng minh nhận định cá nhân hoặc việc tự giải thích không nhìn tài liệu. | Cần tự rà và viết lại các phần chưa xuất phát từ lời mình kể theo yêu cầu lab; không coi đổi cách diễn đạt là thay thế reflection cá nhân. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5).

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi chuẩn bị bài cá nhân, mình tập trung vào những việc quen thuộc của Frontend như tích hợp API, đối chiếu Figma và setup unit test. Nghe các bạn trình bày giúp mình có thêm cơ sở để so sánh: một vấn đề quen thuộc với bản thân chưa chắc là lựa chọn phù hợp nhất để cả nhóm kiểm chứng trong buổi lab. Bài đối chiếu rubric của Quang có đối tượng mà nhóm dễ tiếp cận hơn và phù hợp với trải nghiệm học tập chung. Hai candidate của mình vào shortlist nhưng không được chọn; lý do loại cho thấy mình vẫn cần làm rõ nguyên nhân nghẽn và mức ảnh hưởng, chứ không chỉ nêu thời gian xử lý. Khi chọn problem lần sau, mình sẽ xem khả năng kiểm chứng cùng với mức độ hiểu công việc đó.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có, mình cũng tham gia vào đoạn thảo luận đi quá sớm sang cách triển khai. Với bài toán kiểm tra bài theo rubric, nhóm dành khoảng 15 phút bàn việc lấy rubric ở đâu và xử lý bài nộp dưới dạng văn bản, file hay ảnh như thế nào. Các câu hỏi lúc đó chủ yếu xoay quanh cách làm, trong khi nhóm chưa xác nhận sinh viên khác có thực sự gặp khó khăn này không.

Quang đã kéo cuộc thảo luận trở lại bằng việc nhắc nhóm kiểm chứng pain point trước. Sau đó, nhóm thống nhất dừng bàn kỹ thuật, ghi các giả định và phỏng vấn trong lớp rồi mới tiếp tục các bước sau. Điều mình rút ra là cần phân biệt việc giải pháp có làm được hay không với việc người dùng có cần giải quyết vấn đề đó hay không. Trước một ý tưởng mới, mình nên hỏi ai gặp vấn đề, lần gần nhất xảy ra thế nào và họ đang xử lý ra sao.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có, ví dụ rõ nhất là card tích hợp API của mình. Ban đầu, card tập trung vào việc giảm thời gian hỏi lại Backend để hiểu payload và response. Quang hỏi khoảng thời gian đó đến từ tài liệu thiếu hay từ việc chờ Backend phản hồi. Câu hỏi này buộc mình xem lại cách dùng số phút làm bằng chứng: hai nguyên nhân có thể tạo ra cùng thời gian chậm nhưng cần cách xử lý khác nhau. Mình bổ sung cách đo tách thời gian chờ với thời gian trao đổi chủ động, đồng thời giữ phương án chuẩn hóa tài liệu API để so sánh. Đây mới là thay đổi trong cách xác định và đo vấn đề, chưa phải kết quả đã chứng minh thời gian giảm. Mình cần xác định đúng phần có thể cải thiện trước khi đề xuất công cụ.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Điểm đáng chú ý với mình là kết quả không hoàn toàn nghiêng về việc cần thêm một công cụ AI. Trong poll, 4/6 người gặp khó khăn khi kiểm tra bài nhưng 2/6 thấy tự đọc hoặc nhờ bạn kiểm tra đã đủ. Khi phụ trách CP6, mình phải tính đến cả nhóm thứ hai: có người gặp pain không đồng nghĩa cách dùng AI sẽ có thêm giá trị cho tất cả mọi người. Những cách xử lý sẵn có cũng tạo ra đối chứng cụ thể. Vì vậy, đánh giá giải pháp cần hỏi nó giúp gì hơn checklist hoặc review chéo, và có làm người dùng tốn thêm thời gian kiểm tra lại nhận xét sai không. Đây là lý do chưa thể lấy tín hiệu có nhu cầu làm bằng chứng để chuyển ngay sang Go.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Với phần CP6 mình phụ trách, khó nhất là nối được bottleneck, metric và ranh giới sử dụng AI thành một lập luận nhất quán. Viết mục tiêu từ 60 xuống 20 phút khá dễ, nhưng còn phải xác định bắt đầu và kết thúc phép đo ở đâu, có tính thời gian kiểm tra lại output và sửa bài không. Nếu nhanh hơn mà AI báo đạt cho một tiêu chí còn thiếu thì kết quả vẫn không có ích. Vì vậy, bản v1 bổ sung đối chứng checklist, mức khớp với người chấm và yêu cầu truy được minh chứng. Mình cũng cần tách phần Rule kiểm tra cấu trúc khỏi phần AI đối chiếu nội dung, rồi nêu rõ người dùng kiểm tra gì. Những trường này phải hỗ trợ nhau, không chỉ được điền đủ theo mẫu.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Nếu làm lại, mình sẽ thống nhất cách đo và chuẩn bị dữ liệu kiểm chứng trước khi hoàn thiện CP6. Mình sẽ hỏi rõ ai chấm tham chiếu, bộ thử có trường hợp thiếu tiêu chí không và khi nào phải quay về cách thủ công. Mình cũng sẽ phản biện mạnh hơn câu hỏi liệu phương án đơn giản đã đủ chưa, thay vì chỉ so sánh các mức can thiệp trên lý thuyết. Trong lần này, mình đã yêu cầu chạy thử nhưng lượt dry run chỉ đối chiếu một phần rubric, chưa có người chấm độc lập và chưa đo thời gian người dùng. Điều đó cho thấy cần xác định phép thử muốn trả lời câu hỏi gì ngay từ đầu. Với AI, mình cần giới hạn yêu cầu hỗ trợ và tự kiểm tra lập luận; việc AI tạo nhiều nội dung hay nhiều file không làm bằng chứng trở nên đầy đủ hơn.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Bài toán nhóm chọn là giúp sinh viên đối chiếu bài làm với rubric trước hạn nộp, giảm thời gian rà soát và nguy cơ bỏ sót yêu cầu. Cách làm hiện tại là đọc rubric, dò nội dung tương ứng trong bài, ghi lại phần thiếu rồi chỉnh sửa; bước dò và đối chiếu minh chứng là bottleneck. Nhóm đặt mục tiêu đưa tổng thời gian từ khoảng 60 phút xuống không quá 20 phút, đồng thời kết quả đối chiếu khớp người chấm ít nhất 90% và không báo đạt sai cho tiêu chí bắt buộc bị thiếu trong bộ thử. AI không được tự sửa hoặc nộp bài, không quyết định điểm thay giảng viên và phải đưa ra minh chứng để người dùng kiểm tra. Hướng can thiệp là Workflow trong phạm vi mơ hồ cao, phức tạp thấp: Rule kiểm tra cấu trúc và tiêu chí định lượng, AI hỗ trợ đối chiếu ngữ nghĩa, còn sinh viên kiểm tra và quyết định chỉnh sửa. Trình tự xử lý đã xác định trước nên chưa cần Agent tự chọn công cụ hay bước tiếp theo. Nhóm đang theo hướng Not Yet vì cần thử nghiệm giới hạn để kiểm tra chất lượng, thời gian so với checklist và điều kiện sử dụng dữ liệu trước khi triển khai.

---
## 7. Tài liệu tham khảo

- [Báo cáo nhóm](../team/group_report.md), mục 2.1, 2.4 và 6–8: pitch, phản biện, lựa chọn candidate và phần CP6.
- [Rubric của lab](../../RUBRIC.md): yêu cầu về nhật ký phản biện, reflection và hiểu bài.
