* Cac phuong phap dinh tuyen
1. Dynamic Routing
2. Static Routing
3. Default Route

* Static Routing
	+ Pros
		- Phai quan tri thu cong, bat buoc phai khai bao diem den trong mang
		- Phu hop voi he thong mang nho
		- Administrative Distance (Do tin cay cua giao thuc) la bang 0 hoac 1
	+ Cons
		- Phai cau hinh thu con toan bo
		- Khi thay doi he thong can phai thay doi thong tin dinh tuyen cua tat ca thu cong

* Default Route
	+ Su dung trong truong hop khong biet dich den cua goi tin, duoc su dung trong he thong Internet khi ma khong biet dich den
	+ Su dung tai cac vi tri cuoi trong mang
	+ Muc uu tien cuoi cung trong dinh tuyen
	+ Giup giam khoi luong thong tin ma bang dinh tuyen can co

* Dynamic Routing
	+ Cac router tu dong xay dung bang dinh tuyen
	+ Tu dong cap nhat bang dinh tuyen khi co thay doi 
	+ Hoat dong nho vao qua trinh truyen nhan, quang bo thong tin cua router

* giao thuc classfull & classless
	+ classfull: 
		- Khi cap nhat thong tin dinh tuyen se khong co subnet mask di kem theo thong tin dinh tuyen
		- Cx co nghia la toan bo cac thiet bi deu su chung subnet mask
		- VD: RIPv1, IGRP
	+ classless:
		- Khi cap nhat thong tin dinh tuyen se co subnet mask di kem trong thong tin dinh tuyen
		- VD: RIPv2, EIGRP, OSPF, IS-IS

* RIP (Routing information Protocol)
	+ Cap nhat thong tin qua Broadcast: 255.255.255.255
	+ Metric: hop count <= 15
	+ Trao doi dinh tuyen dinh ky 30s
	+ AD = 120

* EIGRP
	+ Thuoc giao thuc classless, bao gom cac tinh nang cua IGRP
	+ hop count max = 255
	+ AD =90
	+ truyen du lieu qua multicast va unicast
	+ Cap nhat thong tin qua multicast 224.0.0.10

* OSPF
	+ Giao thuc dinh tuyen classless
	+ Khong gioi han so luong hop - count
	+ metric la cost (Cost = 10^8/Bandwidth)
	+ AD = 110
	+ Duoc chia thanh cac vung cho viec de kiem soat luu luong
	+ Su dung dia chi muliticast 224.0.0.5 va 224.0.0.6
 
