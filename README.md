# SSH_KEY_HOW_TO_SET_UP
SSH setup

 => cd ~/.ssh 
=> ssh-keygen -t rsa
Nhập tên VD: id_name

 => cat id_name.pub
Copy mã và add vào SSH key lên GitHub

Tại shell (.ssh)
=> open config

thêm profile cho ssh như sau:
Host host_name
       HostName github.com
       User git
       IdentityFile ~/.ssh/id_name
       IdentitiesOnly yes
VD link ssh clone là thanhbinh030301/smartphone-store-reactjs.git

git clone git@host_name:thanhbinh030301/smartphone-store-reactjs.git

rồi sửa dụng như bình thường
