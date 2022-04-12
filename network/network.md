* TCP/IP: 
5	Application:	tâng ứng dụng
4	Transport:	cách thức truyền tin
3	Network:	cấp địa chỉ IP
2	Data link:	phân luồng đường truyền tránh tác nghẽn
1	Physical:	các thiết bị

* OSI:
7	Application:	tâng ứng dụng
6	presentation:	chuyển thành cách chuỗi bit và ngược lại
5	session:	thiệt lập, kết nối, huỷ hoặc là phục hồi phiên 
4	Transport:	cách thức truyền tin
3	Network:	cấp địa chỉ IP
2	Data link:	phân luồng đường truyền tránh tác nghẽn
1	Physical:	các thiết bị

* TCP:
	* Giúp dữ liệu được chuyển đi đủ các dữ liệu và dữ liệu được sắp xếp
	* Sử dụng phương thức bắt tay 3 chiều:
		- Gửi một gói tin có cờ SYN để yêu cầu mở cổng dịch vụ. 
		- Sau khi nhận được gói tin, server gửi lại gói tin có cờ SYN-ACK để xác nhận. 
		- Sau khi kết nối đã được thiết lập, client gửi tới gói tin ACK để đáp ứng nhu cầu bằng cách này dữ liệu sẽ không bao h mất
 
* UDP:
	- UDP cũng gần giống như TCP nhưng UDP không thực hiện xác minh và không thực hiện chính xác phân phối dữ liệu
	- UDP sẽ phân phối dữ liệu nhanh hơn nhưng lại không đảm bảo về dữ liệu như TCP

* IPv4:
	- class A: từ 0.0.0.0 đến 127.255.255.255 dùng cho các mạng cực lớn
	- class B: 128.0.0.0 đến 191.255.255.255 dùng cho mạng vừa và lớn
	- class C: 192.0.0.0 đến 223.255.255.255 mạng phổ thông 
	- class D: 244.0.0.0 đến 239.255.255.255 lớp mutilcast, ko dùng cho thiết bị
	- class E: 240.0.0.0 đến 255.255.255.255 dùng để dự phòng


