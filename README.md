# SSH_KEY_HOW_TO_SET_UP
SSH setup

 => cd ~/.ssh 
=> ssh-keygen -t rsa
</br>
Nhập tên VD: id_name
không cần mật khau: ENTER 
cho đến khi xong
</br>
 => cat id_name.pub
</br>
Copy mã và add vào SSH key lên GitHub
</br>
Tại shell (.ssh)
=> open config

thêm profile cho ssh như sau:
</br>
Host host_name</br>
       HostName github.com</br>
       User git</br>
       IdentityFile ~/.ssh/id_name</br>
       IdentitiesOnly yes</br>
</br>
VD link ssh clone là thanhbinh030301/smartphone-store-reactjs.git
</br>
git clone git@host_name:thanhbinh030301/smartphone-store-reactjs.git
</br>
add local config cho project
</br>
git config --local user.name "name"
</br>
git config --local user.email "account@gmail.com"
</br>
rồi sửa dụng như bình thường
