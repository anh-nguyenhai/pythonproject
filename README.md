# pythonproject
Đây là một ứng dụng , dùng để ẩn thông tin vào một ảnh, hoặc một file cho trước. Dữ liệu sẽ được mã hóa vào trong ảnh, bằng việc mã hóa thông tin , bằng mắt thường , kẻ tấn công không 
thể đánh cắp thông tin được mã hóa được. 
# Kiến thức sử dụng trong môn nhập môn an toàn thông tin
Em sử dụng 2 mô hình mã hóa đặc trưng, đó là mã hóa khối AES , và mô hình mã hóa bất đối xứng RSA
# Mã hóa khối AES + RSA:
Dữ liệu sẽ được mã hóa bằng mã hóa AES , sau đó khóa AES sẽ được mã hóa bằng RSA. Dữ liệu và khóa sẽ được mã hóa theo hình ảnh.
# Mã hoá RSA: 
Dữ liệu mã hóa bằng RSA. Khóa và dữ liệu sẽ được mã hóa theo hình ảnh.

# Cơ chế mã hóa hình ảnh và kích thước dữ liệu có thể ẩn
Dữ liệu sẽ được ẩn trong giá trị RGB của hình ảnh. 1byte dữ liệu cần 3 pixel để ẩn:
Ví dụ một ảnh có độ phân giải là 1920*1080 
Nó có 1920*1080 = 2,073,600 pixels
2,073,600 / 3 = 691,200 bytes dữ liệu.
691,200 / 1024 = 675 KB
Vậy một ảnh có độ phân giải 1920*1080 có thể chứa tối đa 675 KB dữ liệu.

# Một số hình ảnh của ứng dụng:
Giao diện của phần mã hóa :

![image](https://user-images.githubusercontent.com/64057572/125715941-ba17f8b1-e1fa-411d-b325-9c4b4d85dfac.png)

Phía trên cùng , người dùng có 2 tùy chọn là mã hóa bằng AES + RSA hoặc RSA.
Output folder : chứa ảnh đầu ra đã được mã hóa.
Public key : Khóa dùng để mã hóa.
Img file : ảnh chứa thông tin được ẩn

Hình ảnh mã hóa dữ liệu :

![image](https://user-images.githubusercontent.com/64057572/125716886-d5df90cc-068b-46ba-8126-a76ead131312.png)


Giao diện giải mã :
![image](https://user-images.githubusercontent.com/64057572/125717123-d32a4d26-f9b6-4bfe-951d-25e1b7fad83e.png)

Người muốn nhận thôn tin nhận được file hình ảnh chứa thông tin ẩn và private key từ người mã hóa.

Người dùng có thể tự tạo một key cho bản thân, hoặc có thể tạo ngẫu nhiên từ app. Key tạo từ app có 4 độ dài : 2048, 3072 , 4096 , 8172 (bit)
![image](https://user-images.githubusercontent.com/64057572/125717267-b765cfd9-9d4e-486a-98f3-8bd83652a45b.png)
Key được tạo sẽ được lưu vào folder keys để tiện cho quá trình lưu trữ

![encrypted](https://user-images.githubusercontent.com/64057572/125717517-21e09f77-09f2-494e-8a47-a106a94589db.png)

![encrypted](https://user-images.githubusercontent.com/64057572/125717517-21e09f77-09f2-494e-8a47-a106a94589db.png)

Hình trên là hình ảnh gốc ban đầu chưa có thông tin. Hình ảnh bên dưới là hình ảnh đã chứa thông tin được mã hóa. Bằng mắt thường hầu như không có khác biệt giữa 2 hình

