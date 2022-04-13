1. HTTP
- La mot trong cac giao thuc chuan ve mang, duoc dung de lien he thong tin giua cac Web Server, la giao thuc Client-Sever dung cho WWW
- La bo giao thuc ung dung cua bo giao thuc TCP/IP 
![](https://images.viblo.asia/7da268f1-718b-465c-87df-700e766df185.png)
- HTTP la mot stateless protocol: Request hien tai khong biet nhung gi da hoan thanh trong request truoc duoc

2. URL
* URL duoc su dung de xac dinh duy nhat mot tai nguyen tren Web, vs cau truc:
	+ protocol://hostname:port/path-and-file-name
	- Protocol: La giao thuc tang ung dung duoc su dung boi client-server
	- Hostname: Ten DNS Domain
	- Port: Cong TCP de server lang nghe request tu client 
	- Path-and-file-name: Ten va vi tri cua tai nguyen yeu cau
![](https://images.viblo.asia/1596a7ea-09cc-4a36-82ac-48768e0cb24f.png)

3. Cac thanh phan chinh cua HTTP
* HTTP - Requests
- HTTP Request Method: dung de chi ra hanh dong mong muon duoc thuc hien tren tai nguyen xac dinh
- Cau truc cua mot HTTP Request:
	+ Request-line = Protocol + URL-Request + HTTP version
		- Giao thuc HTTP dinh nghia mot tap cac giao thuc GET, POST, HEAD, ... Client cho the su dung 1 trong cac phuong thuc do de gui request len server
	+ Co the co hoac khong cac truong header 
	+ Mot dong trong de danh dau su ket thuc cua cac truong header	
		- Request Header Fields: Cac truong header cho phep client truyen thong tin bot sung ve yeu cau, va ve chinh client, den server
	+ Tuy chon thong diep
- Khi request den server, server thuc hien mot torng 3 hanh dong sau:
	+ Server phan tich request nhan duoc, maps yeu cua voi tap tin trong tap tai lieu cua server va tra lai tap tin cho client
	+ Server phan tich request nhan duoc, maps yeu cua vao mot chuong trinh tren server, thuc thi chuong trinh do va tra lai ket qua
	+ Request tu client khong the dap ung, Server tra lai thong bao loi
![](https://images.viblo.asia/b986dced-c499-4051-8efb-5ea5d9b93c02.png)
* HTTP - Responses
- Cau truc cua HTTP - Responses
	+ Status-line = HTTP version + Ma trang thai +  Trang thai
	+ Co the co hoac khong co header
	+ Mot dong trong de danh dau su ket thuc cua cac header
	+ Tuy chon mot thong diep
- Ma trang thai: Thong bao ket qua khi nhan duoc yeu cau va xu ly ben server cho client
- Cac kieu ma trang thai:
	+ 1xx: Thong tin (100 -> 101): 100(Continue),...
	+ 2xx: Thanh cong (200 -> 206): 200(OK), 201(CREATED)
	+ 3xx: Dieu huong lai (300 -> 307)
	+ 4xx: Loi ben client (400 -> 407)
	+ 5xx: Loi ben server (500 -> 505)

![](https://images.viblo.asia/8414d386-f4e5-4b9c-aded-d3b379dc7c20.png)

	


