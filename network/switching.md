1. Broadcast Domain: Được định nghĩa là nhóm các thiết bị nhận được tin broadcast khởi tạo từ bất kỳ thiết bị nào trong nhóm

2. Collison Domain:
	- Xảy ra khi 2 hoặc là nhiều máy truyền dữ liệu đồng thời trong 1 mạng chia sẻ
	- Đụng độ xảy ra các gói tin đều bị hủy, các máy ngưng truyền dữ liệu và cho 1 khoảng thời gian ngẫu nhiên theo CSMA/CD

3. VLAN:
	- Kỹ thuật sử dụng để chia 1 switch vật lý thành nhiều switch logic
	- Mỗi switch logic được gọi là VLAN
	- Chia miền broadcast thành nhiều miền broadcast nhỏ hơn

4. Cac loai VLAN
	* Static VLAN
	- Cần được định nghĩa dựa trên port
	- Cần được gắn thủ công 1 port trên switch vào 1 VLAN
	- 1 port chỉ có thể gắn cho 1 VLAN, không thể có 2 VLAN trên cùng 1 port
	
	* Dynamic VLAN
	- Dua tren dia chi MAC cua 1 PC
	- Switch tu dong gan port cho 1 VLAN
	- Moi port co the la thanh vien cua nhieu VLAN
	- Su dung 1 server luu tru dia chi MAC cua cac thiet bi VLAN
	
	* Trunk
	- Giai quyet van de VLAN tren nhieu switch co the ket noi voi nhau
	- Ky thuat nay cho phep dung chung 1 duong ket noi vat ly cho du lieu cac VLAN di qua
	- Su dung phuong phap Tagging, Tag dung de phan biet cac VLAN khac nhau
	- Tag VLAN chi xay r tren duong Trunk
	- Su dung cac giao thuc ISL, IEEE 802.1Q

5. VLAN Trunking protocol
	- Giup cau hinh VLAN luon dong nhat khi xoa, them, sua VLAN trong he thong mang
	- VTP quang ba cac thong tin cau hinh VLAN den cac switch khac de cac cau hinh VLAN khac trong mang cung se cap nhat duoc
	- VTP se thuong quang ba cac thong tin nhu: ID, NAME, rivision number va kieu VLAN cho tung VLAN
    - VTP gửi thông điệp quảng bá khi có sự thay dổi xảy ra trong cấu hình VLAN
    - Thông điệp VTP bao gồm: rivision number, VLAN name, VLAN number, thông tin switch có cổng gắn với mỗi VLAN
    - Mỗi lần VTP Server điều chỉnh thông tin VLAN, tăng revision-number lên 1, rổi VTP Server gửi thông tin quảng bá VTP đi
    - Khi switch nhận VTP với revision number lớn hơn, nó sẽ cập nhật cấu hình VLAN

6. Routing in VLAN
	- 1 máy tính trong 1 VLAN A muốn liên lạc với 1 máy tính khác trong 1 VLAN B thì phải qua thiết bị định tuyến
	- Router trong VLAN:
		+ Ngăn chặn quảng bá, bảo mật và quản lí các lưu lượng mạng
	- Định tuyến cho các VLAN: switch tạo 3 VLAN, 1 cổng router kết nối với 1 cổng trên switch -> trunk (trunk layer 3) Ưu điểm: giảm số lượng cổng cần sử dụng của router và switch
