---
title: "Worklog Tuần 10"
date: "2026-07-25"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Tham gia phát triển và hoàn thiện các chức năng backend của dự án.
* Điều chỉnh logic xác nhận thanh toán để bảo đảm đúng quyền hạn của người dùng.
* Tách phần cấu hình thông báo thành module riêng để source code dễ quản lý và mở rộng.
* Bổ sung giới hạn số lượng thành viên đối với nhóm sử dụng gói miễn phí.
* Sửa lỗi, đồng bộ source code với nhánh `main` và tạo pull request để tích hợp các thay đổi vào dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Kiểm tra source code backend và các yêu cầu cần triển khai trong tuần. <br> - Phân tích luồng xác nhận thanh toán của expense. <br> - Xác định quyền của người nợ và chủ nợ trong quá trình xác nhận settlement. <br> - Chuẩn bị nhánh làm việc riêng để triển khai và kiểm thử các thay đổi.                                                                                                                                                                                                                                                                                                                                                                                                           | 20/07/2026   | 20/07/2026      |                |
| 3   | - Sửa logic xác nhận thanh toán với commit `fix(expenses): restrict settlement confirmation to creditor`. <br>&emsp; + Giới hạn quyền xác nhận settlement cho chủ nợ. <br>&emsp; + Ngăn người dùng không có quyền thực hiện thao tác xác nhận thanh toán. <br> - Tạo và merge Pull Request `#8` vào dự án. <br> - Refactor chức năng thông báo với commit `refactor(notifications): extract notification preferences into separate module`. <br>&emsp; + Tách notification preferences thành module riêng. <br>&emsp; + Giảm sự phụ thuộc giữa các thành phần trong notification module. <br>&emsp; + Cải thiện khả năng bảo trì và mở rộng source code. <br> - Tạo và merge Pull Request `#9` vào dự án. | 21/07/2026   | 21/07/2026      |                |
| 4   | - Bổ sung giới hạn thành viên cho nhóm miễn phí với commit `feat(groups): limit free plan groups to 5 members`. <br>&emsp; + Kiểm tra loại gói của nhóm trước khi thêm thành viên. <br>&emsp; + Giới hạn nhóm sử dụng gói miễn phí tối đa 5 thành viên. <br>&emsp; + Trả về lỗi phù hợp khi số lượng thành viên vượt quá giới hạn. <br> - Tạo và merge Pull Request `#10` vào dự án. <br> - Sửa một số lỗi phát sinh với commit `fixed bug`. <br> - Merge nhánh `main` vào nhánh `be-Minh` để cập nhật source code mới nhất và xử lý các thay đổi giữa các nhánh. <br> - Tạo và merge Pull Request `#11` vào dự án.                                                                                       | 22/07/2026   | 22/07/2026      |                |
| 5   | - Kiểm tra lại các thay đổi sau khi merge vào nhánh chính. <br> - Kiểm tra các trường hợp liên quan đến quyền xác nhận settlement. <br> - Kiểm tra giới hạn số lượng thành viên của nhóm miễn phí. <br> - Kiểm tra hoạt động của notification preferences sau khi được tách thành module riêng. <br> - Rà soát các lỗi có thể phát sinh do quá trình merge source code.                                                                                                                                                                                                                                                                                                                                   | 23/07/2026   | 23/07/2026      |                |
| 6   | - Tổng hợp các commit và pull request đã đóng góp trong tuần. <br> - Kiểm tra trạng thái merge của các Pull Request `#8`, `#9`, `#10` và `#11`. <br> - Rà soát lại source code và bảo đảm các chức năng đã được tích hợp vào dự án. <br> - Ghi nhận kết quả thực hiện và chuẩn bị nội dung báo cáo tuần.                                                                                                                                                                                                                                                                                                                                                                                                  | 24/07/2026   | 24/07/2026      |                |

### Kết quả đạt được tuần 10:

* Tổng quát:
  * Trong tuần này, tôi đã tham gia phát triển backend và đóng góp các thay đổi liên quan đến expense settlement, notification preferences và giới hạn thành viên của nhóm miễn phí.
  * Tôi đã hoàn thành các chức năng, sửa lỗi, đồng bộ source code và tạo pull request để tích hợp các thay đổi vào nhánh chính của dự án.
  * Tổng cộng có 4 Pull Request được merge, bao gồm Pull Request `#8`, `#9`, `#10` và `#11`.

* Các chức năng đã hoàn thành:
  * Điều chỉnh quyền xác nhận thanh toán để chỉ chủ nợ có thể xác nhận settlement.
  * Ngăn người dùng không phải chủ nợ thực hiện thao tác xác nhận thanh toán.
  * Tách notification preferences thành một module riêng.
  * Cải thiện cấu trúc source code của chức năng notification.
  * Bổ sung business rule giới hạn nhóm sử dụng gói miễn phí tối đa 5 thành viên.
  * Bổ sung xử lý lỗi khi người dùng thêm thành viên vượt quá giới hạn của gói miễn phí.
  * Sửa các lỗi phát sinh trong quá trình phát triển và tích hợp chức năng.
  * Đồng bộ nhánh phát triển `be-Minh` với nhánh `main`.

* Các commit đã đóng góp:
  * `fix(expenses): restrict settlement confirmation to creditor`
  * `refactor(notifications): extract notification preferences into separate module`
  * `feat(groups): limit free plan groups to 5 members`
  * `fixed bug`
  * `Merge branch 'main' into be-Minh`

* Các Pull Request đã được merge:
  * Pull Request `#8`: tích hợp thay đổi giới hạn quyền xác nhận settlement cho chủ nợ.
  * Pull Request `#9`: tích hợp thay đổi refactor notification preferences.
  * Pull Request `#10`: tích hợp chức năng giới hạn nhóm miễn phí tối đa 5 thành viên.
  * Pull Request `#11`: tích hợp các thay đổi sửa lỗi và đồng bộ source code.

* Kiến thức và kinh nghiệm đạt được:
  * Hiểu rõ hơn cách triển khai business rule và kiểm tra quyền người dùng ở backend.
  * Biết cách tổ chức và tách module để source code dễ bảo trì hơn.
  * Hiểu cách giới hạn tính năng dựa trên loại gói dịch vụ của người dùng.
  * Thực hành quy trình làm việc với Git bao gồm tạo commit, cập nhật nhánh, merge nhánh và xử lý pull request.
  * Có thêm kinh nghiệm kiểm tra lại chức năng sau khi source code được merge vào nhánh chính.