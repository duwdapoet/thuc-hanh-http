#### 1. Tên challenge: Cookies.

#### 2. Mô tả: Who doesn't love cookies? Try to figure out the best one. http://mercury.picoctf.net:64944/

#### 3. Gợi ý: Không có.

#### 4. Cách giải:

- Khi vào trang web tôi xem source code và không nhận thấy có gì bất thường nên tôi chuyển chú ý sang thanh search.
- Bên trong khung search là dòng chữ "snickerdoodle". Tôi nhập theo và search thử thì website đưa ra thông báo:
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/e9cd7606-850f-4dc8-9bbd-9902142423fd)
- Lúc này tôi để ý trên thanh URL có /check nên tôi mở developer tool của Chrome ra và vào tab network.
- Lúc này hiện lên hai log khác nhau là search và check:
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/743cb748-fb5f-4d83-b727-254b3a959f30)
- Tôi đọc cả hai log này và nhận thấy Cookie của 2 headers này khác nhau.
  ![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/98107fea-68d5-4ec1-82c5-62bba899f62d)
  ![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/1521826e-7800-4427-bb07-4aaeec617c4b)
- Tiếp theo, tôi chuyển sang tab Application và chọn vào phần Cookies. Ở đây, tôi thấy giá trị name đang có là 0 tương ứng với dòng chữ "I love snickerdoodle cookies!" bên ngoài web:
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/c24f88ae-0e7a-4cdc-bb59-91fa2c378ebd)
- Tôi thử thay đổi giá trị thành 1 và tải lại trang. Kết quả là dòng chữ đã thay đổi thành "I love chocolate chip cookies!":
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/505f443b-cca2-4bd1-a1f6-7615ec25c9fe)
- Tiếp theo, tôi thay đổi các giá trị tăng tiến dần cho đến khi đạt 18. Lúc này, flag đã xuất hiện là: picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}
 ![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/1444dbbf-a310-417a-9886-b128115542c2)
