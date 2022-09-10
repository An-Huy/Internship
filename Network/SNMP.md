1. SNMP 
- La giao thuc duoc chap nhan rong tai de quan ly va giam sat cac phan tu mang- La mot phan cua mo hinh TCP/IP
- Chuc nang:
	+ Theo doi toc do truyen cua 1 router, lay thong tin ve o cung cua may Chu
	+ Tu nhan canh bao khi switch co port bi down, dieu khieu shutdown port tren switch
2. Thanh phan
![](https://vietnix.vn/wp-content/uploads/2021/06/tim-hieu-giao-thuc-snmp.webp)
* SNMP Manager:
	- Agent truy van
	- Nhan respone tu cac Agent
	- Dat cac bien trong Agent
	- Xac nhan cac su kien khong dong bo tu Agent
* SNMP Agent:
	- Thu thap thong tin quan ly ve cac chi so hoat dong cua thiet bi
	- Luu tru, truy xuat thong tin quan ly dinh nghia trong MIB
	- Bao hieu su kien cho trinh quan ly 
3. Cơ sở quản lí thông tin quản lí (Management Information base - MIB)

    File .mib
    Mô tả các đối tượng được sử dụng bởi 1 thiết bị cụ thể có thể được truy vấn hoặc kiểm soát bởi SNMP.
    Mỗi MIB được gán 1 định danh đối tượng (OID)

4. Hoạt đông:
    GET: được tạo bởi trình quản lí SNMP vfa gửi đến 1 agent để lấy giá trị 1 biến số (Được xác định bởi OID trong MIB)
    Response: Được gửi bởi agent cho người quản lí SNMP, phát đi để trả lời GET
    GETNEXT: được gửi bởi người quản lí SNMP đến agent yêu cầu lấy 1 giá trị OID tiếp theo trong hệ thống phan cấp MIB.
    GETBULK: Được gửi bởi Manager SNMP cho agent để có bảng dữ liệu lớn.
    _SET: Gửi bởi Manager SNMP cho agent để đưa ra các cấu hình lệnh.
    TRAP: 1 cảnh báo không đồng bộ được gửi bởi agent đến trình quản lí SNMP chỉ ra lỗi hoặc sự cố đã xảy ra.

