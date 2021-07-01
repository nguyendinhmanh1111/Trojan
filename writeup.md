### Building a Trojan by msfconsole in Kali linux
#### 1. Tạo mail rác
- Dịch vụ mail tạm thời cung cấp địa chỉ email tạm thời, an toàn, mang tính ẩn danh
![image](https://user-images.githubusercontent.com/76999751/124124149-4dd08380-daa2-11eb-8b0b-cba9dbd8d5d7.png)
![image](https://user-images.githubusercontent.com/76999751/124124288-73f62380-daa2-11eb-939b-eb3ea886c86b.png)

#### 2. Tạo account trên portmap.io sử dụng mail vừa tạo
-	Chúng ta cần port forwarding để chuyển một Port mặc định trên server sang một port khác
![image](https://user-images.githubusercontent.com/76999751/124124526-bae41900-daa2-11eb-9bbe-cbe484a7e9a4.png)
![image](https://user-images.githubusercontent.com/76999751/124124537-be77a000-daa2-11eb-93e5-16c965b4c174.png)
- Link thông báo xác nhận tài khoản
- ![image](https://user-images.githubusercontent.com/76999751/124124576-ca636200-daa2-11eb-8a26-3e4d6e7f0e5b.png)
#### 3.	Tạo configuration 
-	Tạo file VPN tunnel (VPN tunneling là một quá trình đóng gói và mã hóa dữ liệu)
![image](https://user-images.githubusercontent.com/76999751/124124634-e36c1300-daa2-11eb-9a6d-4a16ad02d5dc.png)
#### 4.	Download file vừa tạo dùng để openvpn ở kali 
![image](https://user-images.githubusercontent.com/76999751/124124958-4362b980-daa3-11eb-84c7-7820a9d8e267.png)
#### 5.	Tạo  mapping để lấy lhost và lport 
- LHOST là địa chỉ IP máy host (backtrack)
- LPORT là cổng mà chúng ta kết nối với nạn nhân
![image](https://user-images.githubusercontent.com/76999751/124125050-61c8b500-daa3-11eb-8f4b-bc60289f396a.png)
![image](https://user-images.githubusercontent.com/76999751/124125079-6a20f000-daa3-11eb-9a86-9ef39f230cb0.png)

#### 6.	Mở file vpn vừa download
![image](https://user-images.githubusercontent.com/76999751/124125319-ace2c800-daa3-11eb-848d-297c8082f5a8.png)
#### 7.	Kiểm tra vpn
![image](https://user-images.githubusercontent.com/76999751/124125751-2b3f6a00-daa4-11eb-8508-218390b1def0.png)
- Kết nối vpn đã mở 
#### 8. tạo trojan bằng msfvenom
![image](https://user-images.githubusercontent.com/76999751/124125893-4ca05600-daa4-11eb-9464-f06734626139.png)
- Mở msfconsole
![image](https://user-images.githubusercontent.com/76999751/124125940-5aee7200-daa4-11eb-80cf-839db2002c90.png)
-	Run handle và chờ kết nối đến máy victim
![image](https://user-images.githubusercontent.com/76999751/124125974-62ae1680-daa4-11eb-8cde-16cd4f6f2472.png)
![image](https://user-images.githubusercontent.com/76999751/124125996-66419d80-daa4-11eb-8699-9239c7c0463e.png)
-	Gửi file chứa mã độc cho nạn nhân và chờ phản hồi
### Thực hiện meterpreter trojan để hack sau khi inject thành công
-	Nạn nhân đã execute trojan => chúng ta có thể điều khiển con trojan này
![image](https://user-images.githubusercontent.com/76999751/124126212-a56fee80-daa4-11eb-80c7-9272ad11bd7e.png
- Kết nối thành công 
