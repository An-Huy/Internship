+ SSH (Secure Shell): là một giao thức điều khiển từ xa cho phép người dùng kiểm soát và chỉnh sửa server từ xa qua Internet
+ ssh user@ip
+ generate key: ssh-keygen 
- default will be rsa, we'll have 3 more are: dsa, ecdsa, ed25519
- passpharse is optional but recommend
+ copy key to remote server ssh-copy-id /full/path/to/the/key.pub (using public not private) user@ip or hostname in config file
+ using with ssh has to be private key not .pub
- ssh -i /full/path/to/the/key user@ip or hostname in config file
+ Store key using ssh-agent
- Has to active ssh-agent if there is no GUI: eval "$(ssh-agent)"
- check if ssh-agent is running or not: ps aux |grep ssh-agent
- ssh-add /full/path/to/the/key
