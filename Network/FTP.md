1. FTP
- Duoc dung trong viec trao doi du lieu trong mang thong qua giao thuc TCP/IP
- Hoat dong tren port 20/21
- Mo hinh hoat dong cua FTP
	+ Dua tren mo hinh client-server, mo hinh nay lai duoc tao tu 2 tien trinh TCP logic va Control Connection va Data Connection
![](https://bit.ly/3uzHRhV)
	+ Control Connection (port 21 - tren server): 
		- La phien lam viec dau tien duoc tao khi qua trinh truyen du lieu bat dau.
		- Tien trinh nay chi kiem soat thong tin dieu khien di qua no
	+ Data Connection (port 20 - tren server): La ket noi du lieu TCP duoc tao ra de truyen tai du lieu giu may client va server. Ket noi se ngat sau khi truyen tai du lieu hoan tat
![](https://news.cloud365.vn/wp-content/uploads/2020/01/Screenshot_2.png)
2. Cac phuong thuc truyen tai trong giao thuc FTP
- Co 3 giao thuc truyen tai du lieu la steam mode, block mode, compressed mode 
	+ stream mode: Du lieu se duoc truyen di duoi dang khong lien tiep, thiet bi chi don thuan day luong du lieu qua ket noi TCP toi phia nhan ma khong co tiet de nhat dinh
	+ Block mode: Du lieu se duoc chia thanh khoi nho va duoc dong goi thanh cac FTP blocks
	+ compressed mode: Su dung ki thuat nen, cac doan du lieu bi lap se bi phat hien va loai bo de giam chieu dai toan bo thong diep gui di
