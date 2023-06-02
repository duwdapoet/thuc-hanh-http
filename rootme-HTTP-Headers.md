#### 1. Tên challenge: HTTP - Headers
#### 2. Mô tả: Get an administrator access to the webpage.
#### 3. Gợi ý: HTTP response give informations
#### 4. Cách giải:

- Website cho biết rằng "Content is not the only part of an HTTP response!". Điều này làm tôi nghĩ đến HTTP response nên tôi đã dùng Burpsuite để kiểm tra.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/4b3bb9ba-637c-49e2-bcf7-bca58cd51f6b)

- Đúng như tôi dự đoán, phần Response cho tôi biết thêm một thuộc tính là Header-RootMe-Admin đang ở none. Nên tôi đã thêm một rule mới trong Match and replace để sửa giá trị none thành true.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/af2d808e-e6b1-4330-9ec9-947cd0ffc377)

- Sau khi hoàn tất, tôi tải lại trang và nhận được password là HeadersMaybeUseful

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/39942799-fb6d-4a3a-be3a-6e7688899e27)

- Đem password đi submit thì tôi nhận được 15 điểm.

![image](https://github.com/duwdapoet/thuc-hanh-http/assets/131479672/445b4fa9-4035-42be-afed-a0a1ebb75586)
