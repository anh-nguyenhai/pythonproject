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

