1. ARP
* La phuong thuc phan giai dia chi dong giua lop network va datalink
	+ Mot thiet bi gui mot goi tin broadcast den toan mang yeu cau thiet bi khac gui tra lao dia chi phan cung (MAC)
* MAC la giao thuc lop 2 - lop datalink
2. Cach thuc hoat dong cua ARP
* Hoat dong cua ARP trong mang LAN
- B1: May gui ktra cache cua minh. Neu da co thong tin mapping giua IP va MAC chuyen sang B7
- B2: May khoi tao goi tin ARP request vs dia chi SHA, SPA la dia chi cua no, dia chi TPA la cua may can biet MAC (TPA hien gia tri toan 0 de bieu hien chua co MAC)
- B3: Gui goi tin broadcast ARP tren toan mang
- B4: Cac thiet bi trong mang nhan duoc goi tin ARP request. Goi tin duoc xu ly bang cach nhin vao TPA
	+ Cac thiet bi khong trung TPA thi huy goi tin
	+ Thiet bi co IP trung voi IP trong TPA se bat dau khoi tao goi tin ARP reply bang cach	lay SHA vs SPA trong goi tin ARP nhan duoc dua vao lam Target trong goi tin duoc gui di. Dong thoi thiet bi cx se lay dia chi MAC cua minh cho vao SHA va cap nhat gia tri anh xa dia chi IP, MAC cua may gui vao bang ARP cache cua minh de giam thoi gian xu ly cho phan sau
- B5: Thiet bi dich gui goi tin reply da duoc khoi tao den thiet bi nguon vua gui ARP request (goi tin reply la goi tin unicast)
+ SSH gom 3 layer:
- B6: Thiet bi nguon nhan duoc goi tin reply va xu ly bang cach luu truong SHA trong goi reply nhu la MAC address cua thiet bi can tim
- B7: Thiet bi nguon update ARP vao cache cua minh gia tri tuong duong giua IP va MAC. Lan sau khong can toi ARP request
    
