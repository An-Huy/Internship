1. DHCP là giao thức tự động cấp phát địa chỉ IP đến các thiết bị trong mạng. Ngoài ra nó cũng đảm bảo không có trường hợp hai hoặc nhiều thiết bị có cùng IP và còn cung cấp các thông tin cấu hình như DNS, subnet mask, default gateway. 
+ DHCP client: Là một thiết bị bất kì có khả năng kết nối internet và giao tiếp với máy chủ DHCP như điện thoại thông minh, máy tính, laptop, máy in …
+ DHCP server: Là thiết bị cấp phát địa chỉ IP
+ DHCP relay: Là thiết bị trung gian để chuyển tiếp yêu cầu giữa DHCP client và DHCP server. DHCP relay agents thường được dùng trong các hệ thống mạng lớn và phức tạp, không phổ biến ở các mạng thông thường 
+ Binding: Là một tập hợp các thông tin cấu hình có ít nhất một địa chỉ IP được dùng bởi một DHCP client, các kết nối được quản lý bởi máy chủ DHCP
+ DHCP Lease: Là khoảng thời gian thiết bị giữ nguyên địa chỉ IP trước khi nó được thay đổi và gia hạn. Cụ thể, mỗi địa chỉ IP sẽ có một vòng đời nhất định. Khi hết thời gian này nó sẽ được cấp một địa chỉ mới 

2. Các thông điệp DHCP:
- DHCP Discover: một gói được gửi đến DHCP server từ một thiết bị Client khi muốn truy cập mạng để yêu cầu thông tin địa chỉ IP.
- DHCP Offer: gói tin chứa địa chỉ IP và thông tin cấu hình TCP/IP bổ sung. Nó được DHCP server gửi về cho Client sau khi nhận được DHCP Discover.
- DHCP Request: là gói được DHCP client phản hồi với máy chủ sau khi nhận được DHCP Offer để thể hiện sự chấp nhận đối với địa chỉ IP
- DHCP Acknowledge: là một gói được DHCP server gửi đến cho Client để xác thực việc chấp nhận DHCP Request và định hướng các tham số tùy chọn cho phép Client tham gia mạng TCP/IP và hoàn thành hệ thống khởi động.
- DHCP Nak
	+ Trong trường hợp địa chỉ IP không được Client sử dụng vì không còn giá trị hoặc đã được dùng bởi một máy khác. DHCP server sẽ gửi một gói DHCP Nak và Client phải tiến hành quá trình thuê bao lại
	+ DHCP Nak chính là một gói được gửi từ DHCP server đến Client khi nó nhận được yêu cầu từ một địa chỉ IP không có giá trị theo các Scope mà nó được định cấu hình.
- DHCP Decline: Trường hợp DHCP Client quyết định tham số thông tin được đề nghị nào không có giá trị nó sẽ gửi một gói DHCP Decline đến các server và Client phải bắt đầu tiến trình thuê bao lại
- DHCP Release: Là một gói được DHCP Client gửi đến một server để giải phóng địa chỉ IP và xóa bất cứ thuê bao nào đang tồn tại.
![](https://hostingviet.vn/data/tinymce/Tin%20tuc%202020/dhcp-la-gi-3.jpg)

