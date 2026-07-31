---
title: "Worklog Tuần 11"
date: "2026-08-01"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Phát triển và hoàn thiện hệ thống thông báo của dự án.
* Xây dựng API quản lý hộp thư thông báo và tùy chọn nhận thông báo của người dùng.
* Bổ sung thông báo cho các hoạt động liên quan đến nhóm, khoản chi, thanh toán và cập nhật sản phẩm.
* Xây dựng luồng gửi khiếu nại dành cho người dùng.
* Xây dựng chức năng để quản trị viên tiếp nhận và xử lý khiếu nại.
* Kiểm tra, đồng bộ source code và tích hợp các thay đổi thông qua pull request.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích yêu cầu của hệ thống thông báo. <br> - Xác định các loại thông báo cần hỗ trợ trong dự án. <br> - Rà soát luồng thông báo liên quan đến nhóm, khoản chi và thanh toán. <br> - Kiểm tra cấu trúc notification module và chuẩn bị các API cần triển khai.                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 27/07/2026   | 27/07/2026      |                |
| 3   | - Xây dựng chức năng quản lý tùy chọn nhận thông báo và hộp thư với commit `feat: add notification preferences and inbox APIs`. <br>&emsp; + Bổ sung API quản lý notification preferences. <br>&emsp; + Bổ sung API lấy danh sách thông báo của người dùng. <br>&emsp; + Hỗ trợ quản lý trạng thái đọc và chưa đọc của thông báo. <br> - Xây dựng luồng thanh toán của người nợ với commit `feat: add debtor settlement and payment sent flow`. <br>&emsp; + Cho phép người nợ ghi nhận đã gửi tiền. <br>&emsp; + Tạo thông báo liên quan đến quá trình gửi và xác nhận thanh toán. <br> - Tích hợp các thay đổi thông qua Pull Request `#14`.                                                                          | 28/07/2026   | 28/07/2026      |                |
| 4   | - Bổ sung thông báo cho khoản chi và thành viên nhóm với commit `feat: add expense and group membership notifications`. <br>&emsp; + Tạo thông báo khi có hoạt động liên quan đến khoản chi. <br>&emsp; + Tạo thông báo khi thành viên được thêm hoặc có thay đổi trong nhóm. <br> - Bổ sung thông báo nhắc thanh toán hằng tuần với commit `feat: add weekly on-demand settlement reminder notifications`. <br>&emsp; + Hỗ trợ tạo thông báo nhắc thanh toán theo yêu cầu. <br>&emsp; + Bổ sung cơ chế nhắc thanh toán định kỳ hằng tuần.                                                                                                                                                                              | 29/07/2026   | 29/07/2026      |                |
| 5   | - Hoàn thiện hệ thống thông báo với commit `feat: add product update notifications and finalize notification APIs`. <br>&emsp; + Bổ sung thông báo cập nhật sản phẩm. <br>&emsp; + Hoàn thiện các API còn thiếu của notification module. <br>&emsp; + Rà soát response, validation và quyền truy cập của các API. <br> - Tích hợp các thay đổi thông qua Pull Request `#15`. <br> - Kiểm tra lại hoạt động của notification inbox và notification preferences sau khi merge.                                                                                                                                                                                                                                            | 30/07/2026   | 30/07/2026      |                |
| 6   | - Xây dựng chức năng gửi khiếu nại của người dùng với commit `feat(complaint): implement user complaint submission feature`. <br>&emsp; + Cho phép người dùng tạo và gửi khiếu nại. <br>&emsp; + Lưu thông tin khiếu nại và liên kết với người gửi. <br>&emsp; + Kiểm tra dữ liệu đầu vào và quyền gửi khiếu nại. <br> - Xây dựng luồng xử lý khiếu nại của quản trị viên với commit `feat(admin): implement complaint handling flow`. <br>&emsp; + Cho phép quản trị viên xem các khiếu nại cần xử lý. <br>&emsp; + Hỗ trợ cập nhật kết quả và trạng thái xử lý khiếu nại. <br>&emsp; + Bổ sung logic phân quyền cho quản trị viên. <br> - Kiểm tra luồng khiếu nại từ lúc người dùng gửi đến khi quản trị viên xử lý. | 31/07/2026   | 31/07/2026      |                |

### Kết quả đạt được tuần 11:

* Tổng quát:
  * Trong tuần này, tôi tập trung phát triển hệ thống thông báo và chức năng khiếu nại cho backend của dự án.
  * Hệ thống thông báo đã được mở rộng để hỗ trợ nhiều hoạt động như thay đổi thành viên nhóm, tạo khoản chi, gửi tiền, nhắc thanh toán và cập nhật sản phẩm.
  * Tôi cũng xây dựng luồng khiếu nại gồm hai phía: người dùng gửi khiếu nại và quản trị viên tiếp nhận, xử lý khiếu nại.
  * Các thay đổi của notification module đã được tích hợp vào dự án thông qua Pull Request `#14` và Pull Request `#15`.

* Các chức năng thông báo đã hoàn thành:
  * Bổ sung API quản lý notification preferences của người dùng.
  * Bổ sung API quản lý hộp thư thông báo.
  * Hỗ trợ lấy danh sách thông báo và quản lý trạng thái đọc, chưa đọc.
  * Bổ sung luồng người nợ ghi nhận đã gửi tiền.
  * Tạo thông báo cho các hoạt động liên quan đến settlement và payment sent.
  * Tạo thông báo khi có khoản chi mới hoặc thay đổi liên quan đến khoản chi.
  * Tạo thông báo cho các hoạt động liên quan đến thành viên nhóm.
  * Bổ sung thông báo nhắc thanh toán theo yêu cầu.
  * Bổ sung thông báo nhắc thanh toán định kỳ hằng tuần.
  * Bổ sung thông báo cập nhật sản phẩm.
  * Hoàn thiện các API chính của notification module.

* Các chức năng khiếu nại đã hoàn thành:
  * Cho phép người dùng gửi khiếu nại trên hệ thống.
  * Kiểm tra và lưu trữ thông tin khiếu nại.
  * Liên kết khiếu nại với người dùng gửi khiếu nại.
  * Xây dựng luồng để quản trị viên xem và xử lý khiếu nại.
  * Cho phép quản trị viên cập nhật kết quả và trạng thái xử lý.
  * Bổ sung kiểm tra quyền quản trị viên khi thực hiện thao tác xử lý khiếu nại.

* Các commit đã đóng góp:
  * `feat: add notification preferences and inbox APIs`
  * `feat: add debtor settlement and payment sent flow`
  * `feat: add expense and group membership notifications`
  * `feat: add weekly on-demand settlement reminder notifications`
  * `feat: add product update notifications and finalize notification APIs`
  * `feat(complaint): implement user complaint submission feature`
  * `feat(admin): implement complaint handling flow`

* Các Pull Request đã được merge:
  * Pull Request `#14`: tích hợp notification preferences, inbox APIs và luồng debtor settlement/payment sent.
  * Pull Request `#15`: tích hợp các thông báo liên quan đến expense, group membership, settlement reminder, product update và hoàn thiện notification APIs.

* Kiến thức và kinh nghiệm đạt được:
  * Hiểu rõ hơn cách thiết kế notification module cho nhiều loại sự kiện trong hệ thống.
  * Có thêm kinh nghiệm xây dựng API quản lý hộp thư và tùy chọn nhận thông báo.
  * Hiểu cách kết nối notification với các nghiệp vụ như nhóm, khoản chi và thanh toán.
  * Có thêm kinh nghiệm triển khai chức năng định kỳ như thông báo nhắc thanh toán hằng tuần.
  * Hiểu cách xây dựng luồng khiếu nại giữa người dùng và quản trị viên.
  * Cải thiện kỹ năng kiểm tra phân quyền và chuyển đổi trạng thái trong backend.
  * Thực hành quy trình tạo commit, pull request, kiểm tra và tích hợp source code vào dự án.