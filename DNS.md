+ DNS (Domain Name System) hay hệ thống phân giải tên miền, có thể được giải thích là một hệ thống giúp con người và máy tính có thể “giao tiếp” với nhau một cách dễ dàng hơn 
+ DNS phân giải chuỗi IP dài và khó có thể nhớ thành các tên dễ nhớ và ngược lại như:
- 10.0.0.30: www.example.xyz.com
+ DNS recursor: là loại server làm ra để nhận queries từ end-user qua các ứng dụng như web broswers
+ Root nameserver: có nhiệm vụ phân giải tên miền thành những chuỗi ip có thể hiểu Root Name Server chính là một thư viện để định hướng tìm kiếm giúp
+ TLD nameserver: chính là các đuôi như: .com, .net .edu, ...
+ Authoritative nameserver: Khi DNS Resolver tìm thấy Authoritative Nameserver, đó là lúc mà việc phân giải tên miền diễn ra. Mặt khác, Authoritative Name Server có chứa thông tin cho biết tên miền đang gắn với địa chỉ nào.
+ Máy chủ tên có thẩm quyền: Nơi lưu trữ thông tin đầy đủ về một vùng
+ Máy chủ tên đệ quy: Nơi trả lời các truy vấn DNS cho người dùng Internet, đồng thời lưu trữ kết quả phản hồi của DNS trong một khoảng thời gian.
+ DNS lookup:
1.	người dùng gõ tên mình cần tìm kiếm vào công cụ tìm kiếm và sẽ được nhận bởi DNS recursive Resolver
2.	Trình phân giải sẽ truy vấn một máy chủ định danh gốc DNS
3.	Máy chủ gốc phản hồi trình phân giải bằng địa chỉ của máy chủ DNS Tên miền Cấp cao 
nhất(chẳng hạn như .com hoặc .net), máy chủ này lưu trữ thông tin cho các miền của nó
4.	Trình phân giải đưa ra yêu cầu tới .com TLD
5.	Sau đó, máy chủ TLD sẽ phản hồi bằng địa chỉ IP của máy chủ định danh của miền
6.	Cuối cùng, trình phân giải đệ quy gửi một truy vấn đến máy chủ định danh của miền 
7.	Địa chỉ IP cho example.com sau đó được trả về trình phân giải từ máy chủ định danh
8.	trình phân giải DNS sẽ phản hồi lại trình duyệt web bằng địa chỉ IP của miền được yêu cầu ban đầu.

+ DNS queries:
- Recursive query: Máy khách DNS yêu cầu máy chủ DNS sẽ trả lời máy khách với bản ghi tài nguyên được yêu cầu hoặc thông báo lỗi nếu trình phân giải không thể tìm thấy bản ghi. 

- Iterative query: trong trường hợp này, end-user sẽ cho phép máy chủ DNS trả về câu trả lời tốt nhất có thể. Nếu máy chủ DNS được truy vấn không khớp với tên truy vấn, nó sẽ giới thiệu đến máy chủ DNS có thẩm quyền thấp hơn. Sau đó, end-user sẽ thực hiện một truy vấn đến địa chỉ giới thiệu. Quá trình này tiếp tục với các máy chủ DNS bổ sung trong chuỗi truy vấn cho đến khi xảy ra lỗi hoặc hết thời gian. 

- Non-recursive query: thường điều này sẽ xảy ra khi truy vấn máy chủ DNS về bản ghi mà nó có quyền truy cập hoặc bản ghi tồn tại bên trong bộ đệm của nó. Thông thường, máy chủ DNS sẽ lưu trữ các bản ghi DNS để ngăn chặn việc tiêu thụ thêm băng thông và tải trên các máy chủ ngược dòng


