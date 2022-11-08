
# SSH HOW TO SET UP

Làm theo hưỡng dẫn: 

## Ví dụ/Examples

```
> cd ~/.ssh 

```
***Tại shell (.ssh)***

Generate mã key ssh
```
> ssh-keygen -t rsa 
```
Kiểm tra xem đã có file ssh chưa
```
> ls
```
VD: id_name.pub và id_name là thành công

Nhập tên VD: **id_name** không cần mật khẩu: **ENTER** cho đến khi xong
```
> cat id_name.pub
```
Đoạn mã có dạng như sau:
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQC80XuRN76l+S99
v1TalDylvC2Ue1nbdxaozpGfvhrmi2VE519uWeHu4tLd7Y5xOcbA
WQo90w6qw+HC/hLd2zoqNWzkzzfYcE87Xzis/rcuY5kfm/UR2pDO
Wjx8A2E4Sa6Tn9/vQMNHGOvwgL32jjjYxaUwmMlIl+/oDVunZGhJ
Zrj567d6SPYGSiACg1/WOuq0xLF0fnxgk8TpSSN4EFuittwEyF6PL
MwweCJ0ai16pyeCP2CJEqOGbubD+p5ScUpt9EnIsVN16mzkLu/XcF
zq/EoLrdNZlPc+pbobwJEn3mIfl8ZTc1SaQP1hQJJYDdGhLvhG95s
vZ30ATWrmScMopv1RWnHBXoF+PP7V2sk5zvko29CIad1E7ZSpJ9SM
adjD5JDmRxce+DFnUlYCx1gUpislpboKJcDj8DZZU90swH2G+AaGK
0B8TrspMFwYtlh3U8J38vCtaVQrRDHqWMBLCAniA5CZf8YQLcd6YF
krAeXhCzNwBzX21KQ1yNvKfJM= macbookpro@macbooks-macboo
k-pro.local
```
Copy mã và thêm vào SSH key cho tải khoản github
```
1. Setting 
2. SSH and GPG keys 
3. Thêm ssh vào tài khoản chứa source cần clone
```
Nếu chưa có file **config** tạo file config tại .ssh
```
> touch config.txt
```
Với MacOS
```
> open config 
```
Hoặc
```
> vim config 
```
Thêm **profile** cho ssh config như sau:
```
Host host_name
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_name
    IdentitiesOnly yes
```

**TẠI ĐƯỜNG DẪN CỦA PROJECT**

**Mới clone**

VD: URL ssh clone là:
```
 thanhbinh030301/smartphone-store-reactjs.git
```
Thì sẽ clone theo cú pháp như sau (nhớ **host_name** là Host của **profile config**)
```
> git clone git@host_name:thanhbinh030301/smartphone-store-reactjs.git

```

Thêm tài khoản local config cho project
```
> git config --local user.name "name"
> git config --local user.email "account@gmail.com"
```
**Đã clone trước đó rồi**
```
> git remote rm origin
> git remote add origin git@host_name:thanhbinh030301/smartphone-store-reactjs.git
```
SSH thử sửa add và push trên repo và lên kiểm tra



