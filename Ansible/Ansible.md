1. Ansible OCnecpt
    + Controller Machine: Là máy cài Ansible, chịu trách nhiệm quản, điều khiển và gửi các task đến những máy con cần quản.
    + Inventory: Là file chứa thông tin những server cần quản.
    + Playbook: Là file chứa các task được ghi dưới định dạng YAML. Máy controller sẽ đọc các task này trong Playbook sau đó đẩy các lệnh thực thi tương ứng bằng Python xuống các máy con.
    + Task: Một block ghi lại những tác vụ cần thực hiện trong playbook và các thông số liên quan.
    + Module: Trong Ansible có rất nhiều module khác nhau. Ansible hiện có hơn 2000 module để thực hiện các tác vụ khác nhau, bạn cũng có thể tự viết thêm những module của mình khi có nhu cầu. Một số Module thường dùng cho những thao tác đơn giản như: System, Commands, Files, Database, Cloud, Windows,...
    + Role: Là một tập playbook đã được định nghĩa để thực thi 1 tác vụ nhất định. Nếu bạn có nhiều server, mỗi server thực hiện những tasks riêng biệt. Khi này nếu chúng ta viết tất cả vào cùng một file playbook thì khá là khó để quản. Do vậy roles sẽ giúp phan chia khu vực với nhiệm vụ riêng biệt.
