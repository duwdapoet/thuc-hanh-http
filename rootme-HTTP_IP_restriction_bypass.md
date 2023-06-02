#### 1. Tên challenge: HTTP - IP restriction bypass.
#### 2. Mô tả:
Dear colleagues,

We’re now managing connections to the intranet using private IP addresses, so it’s no longer necessary to login with a username / password when you are already connected to the internal company network.

Regards,

The network admin

#### 3. Gợi ý: Only local users will be able to access the page

#### 4. Cách giải:

- Website có hai khung login và password kèm theo dòng chữ "You should authenticate because you're not on the LAN.". Điều này bắt buộc tôi phải đăng nhập để lấy được thông tin nhưng không có hint về tài khoản nên tôi bỏ qua khả năng này.
- Lúc này, tôi chú ý đến thông báo rằng IP của tôi không thuộc về mạng LAN, nên tôi hướng đến giải pháp làm giả IP của mình để đánh lừa website.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/7b57c6e4-22a3-4b16-8c17-2a7b9f8185b5)
- Tôi mở tool Burpsuite, mở trình duyệt và truy cập theo URL http://challenge01.root-me.org/web-serveur/ch68/

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/5ff4cefa-8f2c-49b0-ac48-d445ae810e6b)
- Tiếp đến, tôi mở Proxy Setting và tìm mục Match and replace rules. Sau đó tôi thêm một rule mới với tùy chỉnh như sau:

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/309b229f-582f-4e94-be24-8b7ba44ff7e1)

- Rule tôi vừa thêm vào cho phép tôi gửi request bằng địa chỉ 10.255.255.255 thay vì địa chỉ gốc của tôi. Lý do tôi chọn 10.255.255.255 là vì nó nằm trong dải địa chỉ IP Private - thứ được sử dụng trong mạng cục bộ.

- Sau khi hoàn tất, tôi chọn login với mục login và password để trống. Lúc này, website trả về password là Ip_$po0Fing

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/b8df03a6-7535-41b6-a0b4-9a28e5a854cc)

- Đem đi submit, thì tôi có được 10 điểm.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/bab1b613-526f-4dfd-9fe9-a0bc3654fb0e)
