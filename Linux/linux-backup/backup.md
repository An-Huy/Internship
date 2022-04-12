* rsync options source destination
	+ -v: hiển thị trạng thái kết quả
	+ -r: copy dữ liệu recursively, nhưng không đảm bảo thông số của file và thư mục
	+ -a: cho phép copy dữ liệu recursively, đồng thời giữ nguyên được tất cả các thông số của thư mục và file
	+ -z: nén dữ liệu khi transfer, tiết kiệm băng thông tuy nhiên tốn thêm một chút thời gian
	+ -h: human-readable, output kết quả dễ đọc
	+ --delete: xóa dữ liệu ở destination nếu source không tồn tại dữ liệu đó.
	+ --exclude: loại trừ ra những dữ liệu không muốn truyền đi, nếu bạn cần loại ra nhiều file hoặc folder ở nhiều đường dẫn khác nhau thì mỗi cái bạn phải thêm --exclude tương ứng.

1. Copy file và thư mục trên local 
	+ file: rsync -zvh .bashrc /tmp/backups/
	+ dir:  rsync -zvah snap/ /tmp/backups/

2. Copy file và thư mục giữa các server
	+ Copy dir Local -> Remote Server: rsync -zvah .vimrrc root@192.168.1.100:/root/
	+ Copy dir Remote Server -> Local: sync -zvah root@192.168.1.100:/home/huy/Documents/hello.txt /home/huy/Documents

3. Rsync qua SSH
	+ Copy dir Local -> Remote Server: rsync -zvahe ssh snap/ root@192.168.1.100:/root/
	+ Copy dir Remote Server -> Local: rsync -zvahe ssh root@192.168.1.100:/root/anaconda-ks.cfg /home/huy/Documents/

4. Hiển thị tiến trình trong khi transfer dữ liệu với Rsync
	+ rsync -zvahe ssh --progress snap/ root@192.168.1.100:/root/test/

5. Giới hạn dung lượng tối đa của file được đồng bộ
	+ rsync -avzhe ssh --max-size='10k' snap/ root@192.168.1.100:/root/

6. Tự động xóa dữ liệu nguồn sau khi đồng bộ thành công
	+ rsync --remove-source-files -zvah .bashrc.bak /tmp/backups/

* using dd:
	+ using full disk: dd if=/dev/sda of=/dev/sdb bs=1M conv=noerror
	+ restore:	     dd if=/dev/sdb of=/dev/sda bs=1M conv=noerror
	+ dd if=/dev/sda | gzip -c > /tmp/test.img.gz 
	+ dd if=/dev/sda | gzip -c | ssh root@ip dd of=img.gz 
	+ gzip -dc /tmp/test.img.gz | dd of/dev/sda
 
* using tar
	+ tar -cvf file or dir full path:
	+ tar cvf test.dir ~/Documents/test
