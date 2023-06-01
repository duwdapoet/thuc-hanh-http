#### 1. Tên challenge: GET aHEAD

#### 2. Mô tả: Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:28916/

#### 3. Gợi ý: 

#### - Maybe you have more than 2 choices

#### - Check out tools like Burpsuite to modify your requests and look at the responses

#### 4. Cách giải:

- Khi vào trang web và xem source code tôi thấy có hai phương thức là GET và POST. Phần hint của đề có gợi ý một phương thức thứ ba và tool Burpsuite nên tôi chạy máy ảo và mở tool Burpsuite.
- Sau khi mở tool Burpsuite và nhập vào URL http://mercury.picoctf.net:28916/. Tôi thấy tool trả về là một header với phương thức GET:
 ![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/a978005f-e751-4a67-8350-93c3a8bac433)
- Tiếp đến, tôi gửi header này đến repeater bằng tổ hợp phím Ctrl + R.
- Sau đó, dựa vào hint của đề bài tôi sửa phương thức của header thành HEAD và ấn gửi.
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/ec8d9c79-4c28-4386-8668-740ada089189)
- Cuối cùng, tool trả về header có chứa flag là: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/88ba1cc7-3daf-43a5-ab81-7cff794ebcc4)

