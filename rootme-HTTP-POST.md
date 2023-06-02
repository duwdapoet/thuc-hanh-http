#### 1. Tên challenge: HTTP - POST
#### 2. Mô tả: Find a way to beat the top score!
#### 3. Gợi ý: Không có
#### 4. Cách giải:

- Ở challenge này, tôi ấn liên tục chữ "Give a try!" và quan sát sự thay đổi trong Sources.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/9c68087d-0574-4fc7-b7df-7d66250752ed)

- Tôi nhận thấy rằng, khi in ra dòng "Hoo tooooo sad, you lost. Your score: 284564! I'm always the best :)" thì bên Sources, số 284564 là một text nên tôi khá nghi vấn vào HTTP request.

- Tôi dùng Burpsuite để kiểm tra thử và thấy được phần Request có giá trị score=651015.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/933cadca-f918-472f-89ae-4709ecf22846)

- Tôi chuyển nó về Repeater và sửa giá trị score thành 9999999 để cho điểm của tôi lớn hơn điểm mà website đưa ra để đánh bại Machine.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/fbbe15ed-64c6-4504-8009-29005c20c0bf)

- Sau khi ấn gửi, tôi nhận về Response với flag là H7tp_h4s_N0_s3Cr37S_F0r_y0U

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/13594d81-6081-4268-9722-3bc9a8a4272e)

- Đem nó đi submit thì tôi được 15 điểm.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/1e9f62e4-8215-48f7-a988-7d508a8e34e3)
