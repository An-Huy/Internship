1. Spanning tree
* Bridging loops
	+ Ket noi 2 hoac nhieu link giua cac switch cung cap kha nang du phong
	+ Tuy nhien kha nang cao cac switch se bi loops khi thuc hien truyen broadcast
		- Bao broadcast
		- Dia chi MAC khong on dinh
		- Bang thong chiem dung qua nhieu frame trao doi
	+ Giai phap:
		- Khong co ket noi du phong chi co ket noi 1 link
		- Tam thoi ngat cac link mo rong, du phong

2. Giao thuc STP
	+ STP cho phep chan dung kha nang loops xay ra khi nhieu link duoc su dung de ket noi giua cac switch
	+ Tranh duoc rui ro nhu bao broadcast, qua nhieu tin sao chep hoac du lieu bang MAC khong on dinh
	+ STP hoat dong gom 3 buoc:
		- Lua chon Root Bridge
			- Sw co gia tri BID nho nhat chon lam Root Bridge
			- BID (BridgeID): BID = Priority + MAC address
			+ Priority(2byte): 0 -> 65535
			+ MAC address(6 byte)
			- Moi LAN deu chi co duy hat 1 Root Bridge, cac sw con lai coi la Non-root Bridge
		- Lua con Root Port
			- Port co khoang cach duoc tinh bang cost nho nhat toi Root Bridge
			- Tat ca cac Non-root Bridge nhin Root Port la huong toi uu nhat de den Root Bridge
			- Tat ca Non-root Bridge chi co duy nhat 1 Root Port
			- Dua tren Path Cost nho nhta
			- Dua tren Sw nho nhat, neu bang nhau thi gia tri se dua tren Port Priority va Port-ID
		- Lua chon Designed Port, Non Designed Port cx dua tren 3 buoc:
			- Port Cost nho nhat
			- Tiep den dua tren Sw ID nho nhat
			- Dua tren Port Priority va Port-ID
3. BPDU
* Tất cả các switch trao đổi thông tên dựa trên BPDU
	- BPDU được gửi mỗi 2 giây và có thời gian dead interval là 20 giây.
	- 1 BPDU chứa đựng thông tin bao gồm port, switch, port priority và địa chỉ.

* Các trạng thái port của STP
 - Blocking 20 giây hoặc không giới hạn.
 - Listening 15 giây.
 - Learning 15 giây.
 - Forwarding không giới hạn thời gian.
 - Disable không giới hạn thời gian.

4. Etherchannel
	+ gom 2 hay nhiều kết nối truyền tải dữ liệu vật lí thành 1 đường ảo duy nhất (Logic)
	+ Gom 2 đến 8 link thành 1 link
	+ Traffic không phải lúc nào cũng đồng đều, phụ thuộc vào load balancing mà sw sử dụng
	+ 1 link bị down, traffic chuyển sang các link khác
	+ 2 switch tương đồng: Tốc đô, băng thông, full duplex, Native VLAN và các VLANs, Switchport mode

