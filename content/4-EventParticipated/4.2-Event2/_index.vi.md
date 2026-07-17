---
title: "Event 2"
date: "2026-07-31"
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Saturday Meet up

## Thông tin sự kiện

| **Thông tin**             | **Chi tiết**                                                                           |
| ------------------------- | -------------------------------------------------------------------------------------- |
| **Tên sự kiện**           | Saturday Meet up                                                                       |
| **Thời gian**             | 09:00 - 12:00, ngày 06/06/2026                                                         |
| **Địa điểm**              | Tầng 26, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh |
| **Vai trò trong sự kiện** | Người tham dự                                                                          |

---

## Tóm tắt nội dung và bài học rút ra

### 1. Docker – A Containerization Technology

#### Thông tin diễn giả

> Diễn giả là **Bảo Huỳnh**, Junior Cloud Native Developer tại Endava Vietnam, Founder/Head Lab của ITea Lab và từng làm Cloud DevOps Engineer tại NAB Innovation Centre Vietnam.

#### Nội dung chính

Bài trình bày giới thiệu sự khác nhau giữa virtualization và containerization.

Virtual machine có khả năng cách ly tốt nhưng cần hệ điều hành riêng, tiêu tốn nhiều CPU, RAM và dung lượng lưu trữ. Trong khi đó, container nhẹ hơn vì dùng chung hệ điều hành của máy chủ.

Docker giúp đóng gói ứng dụng cùng thư viện, dependency và cấu hình để ứng dụng có thể hoạt động nhất quán trên nhiều môi trường.

Các thành phần chính của Docker gồm:

- **Container:** Ứng dụng đang chạy.
- **Image:** Mẫu chứa các thành phần cần thiết để chạy ứng dụng.
- **Dockerfile:** File mô tả các bước tạo image.
- **Layer và cache:** Giúp quá trình build nhanh và hiệu quả hơn.

Docker được ứng dụng trong CI/CD, microservices, development, testing và cloud-native applications.

#### Bài học rút ra

Em hiểu rõ hơn sự khác nhau giữa virtual machine và container. Docker giúp giải quyết vấn đề ứng dụng chạy được trên máy này nhưng không chạy được trên máy khác.

Để sử dụng Docker hiệu quả, cần nắm vững các khái niệm image, container, Dockerfile, layer và cache.

---

### 2. Combining AWS WAF with Machine Learning for Cyber Attack Detection on AWS

#### Thông tin diễn giả

> Diễn giả là **Lê Hoàng Gia Đại**, sinh viên năm cuối tại HUTECH University, định hướng trở thành AWS Cloud Engineer và Cyber Security Engineer.

#### Nội dung chính

Bài trình bày giới thiệu cách kết hợp **AWS WAF** với **Machine Learning-based NIDS** để phát hiện các cuộc tấn công mạng.

AWS WAF giúp bảo vệ website, API và ứng dụng khỏi các cuộc tấn công như:

- SQL Injection.
- Cross-site Scripting.
- Bot traffic.
- Brute force.
- Request bất thường.

Tuy nhiên, WAF chủ yếu dựa trên rule và signature nên có thể gặp khó khăn với zero-day attack hoặc những hành vi chưa được định nghĩa trước.

Machine Learning-based NIDS giúp phân tích traffic, phát hiện hành vi bất thường và nhận diện các mẫu tấn công mới.

Mô hình sử dụng dataset **CSE-CIC-IDS2018**, được xử lý qua các bước làm sạch dữ liệu, loại bỏ giá trị lỗi, cân bằng class và chia tập train/test.

Kiến trúc triển khai sử dụng nhiều dịch vụ AWS như WAF, Lambda, S3, CloudWatch, GuardDuty, Security Hub và Kinesis Data Firehose.

#### Bài học rút ra

AWS WAF là một lớp bảo vệ quan trọng nhưng không nên được sử dụng độc lập. Việc kết hợp WAF với Machine Learning giúp hệ thống phát hiện các hành vi bất thường linh hoạt hơn.

Chất lượng dữ liệu ảnh hưởng trực tiếp đến hiệu quả của mô hình, vì vậy data preprocessing và class balancing là những bước rất quan trọng.

---

### 3. AWS Neptune for Building a Graph Knowledge Base for GraphRAG

#### Thông tin diễn giả

> Diễn giả là **Việt Phát**, sinh viên ngành Artificial Intelligence tại Swinburne University of Technology.

#### Nội dung chính

Bài trình bày giới thiệu **GraphRAG**, phương pháp kết hợp Retrieval-Augmented Generation với knowledge graph.

RAG truyền thống truy xuất các đoạn văn bản liên quan để bổ sung ngữ cảnh cho Large Language Model. Tuy nhiên, phương pháp này có thể gặp khó khăn với những câu hỏi cần suy luận qua nhiều thực thể và mối quan hệ.

GraphRAG biểu diễn:

- Thực thể bằng **node**.
- Mối quan hệ bằng **edge**.

Nhờ đó, hệ thống có thể thực hiện multi-hop reasoning và trả lời tốt hơn những câu hỏi có cấu trúc quan hệ phức tạp.

Hai hướng triển khai được giới thiệu gồm:

- **Fully Managed Route:** Sử dụng Amazon Bedrock Knowledge Bases và Amazon Neptune Analytics.
- **Custom Route:** Sử dụng LlamaIndex kết hợp Amazon Neptune.

#### Bài học rút ra

GraphRAG phù hợp với những hệ thống có dữ liệu chứa nhiều thực thể và mối quan hệ.

Fully managed route giúp triển khai nhanh và giảm công việc vận hành, trong khi custom route linh hoạt hơn nhưng đòi hỏi nhiều kỹ năng và nguồn lực kỹ thuật hơn.

---

### 4. Multiplayer in the Cloud – Connecting Godot Clients with AWS WebSockets

#### Thông tin diễn giả

> Diễn giả là **Nguyễn Quốc Bảo**.

#### Nội dung chính

Bài trình bày giới thiệu cách kết nối Godot Client với AWS WebSockets để xây dựng game multiplayer trên cloud.

Ba phương pháp multiplayer networking được đề cập gồm:

- **UDP/ENet:** Phù hợp với FPS hoặc racing game cần độ trễ thấp.
- **HTTP Polling:** Đơn giản nhưng có độ trễ cao.
- **WebSocket:** Phù hợp với turn-based game, lobby, chat và matchmaking.

Kiến trúc hệ thống gồm:

- Godot Client.
- API Gateway WebSocket.
- AWS Lambda.
- Amazon DynamoDB.
- Amazon CloudWatch.

Lambda xử lý kết nối, ngắt kết nối, ghép cặp người chơi, lưu lựa chọn và gửi kết quả về hai client.

DynamoDB lưu các thông tin như `connectionId`, `status`, `opponentId`, `choice` và `createdAt`.

#### Bài học rút ra

Việc lựa chọn kiến trúc multiplayer cần phụ thuộc vào loại game.

WebSocket kết hợp API Gateway và Lambda phù hợp với các game đơn giản, turn-based hoặc matchmaking. Tuy nhiên, serverless architecture không phù hợp với những game cần realtime physics, state liên tục và độ trễ cực thấp.

Khi hệ thống mở rộng, cần tối ưu truy vấn DynamoDB, quản lý stale connection và cân nhắc AWS GameLift cho các game phức tạp hơn.

---

## Một số hình ảnh khi tham gia sự kiện

Sử dụng code giảm giá: AWS_50_Standard trong web Tử Vi Đại Việt

![Event photo](/images/4-EventParticipated/4.2-Event2/AWS_50_STANDARD.png)