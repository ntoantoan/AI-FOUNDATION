**1.Derivative and Applications (đạo hàm và ứng dụng)**
* 1.1 Đạo hàm cho hàm số liên tục
![image](https://user-images.githubusercontent.com/42260182/100746532-68128800-3413-11eb-83fd-c3b8964c1fb1.png)

-Theo tiếng hán đạo là con đường, hàm là hàm số nên đạo hàm chỉ sự biến đổi của hàm số hay có tên thân thương hơn là độ dốc của đồ thị.

* 2.2 Đạo hàm cho hàm rời rạc

ví dụ:

![image](https://user-images.githubusercontent.com/42260182/100748709-3cdd6800-3416-11eb-84df-4f0163cc39f5.png)


Từ ý tưởng của đạo hàm Sobel đã xây dựng lên các kernel giúp thực hiện đào hàm một cách tốt hơn


![image](https://user-images.githubusercontent.com/42260182/100749765-af027c80-3417-11eb-96f9-b9714b9a179a.png)

* Ứng dụng đạo hàm cho Edge detection


![image](https://user-images.githubusercontent.com/42260182/100750552-c726cb80-3418-11eb-9b6d-10d4850aca35.png)

**2. Phép nội suy**
Phép nội suy chính là phép suy ra những thông tin ta không rõ từ những thông tin ta đã biết

Các ví dụ cho phép nội xuy

![image](https://user-images.githubusercontent.com/42260182/100752739-82e8fa80-341b-11eb-97d2-5a42c891989d.png)

Ví dụ xác định một điểm:

![image](https://user-images.githubusercontent.com/42260182/100753401-4a95ec00-341c-11eb-8ac9-cf6d7385626a.png)

Sử dụng phép nội xuy theo hàm tuyến tính ta có thể xác định điểm P như trong hình bên phải  sử dựa trên phương trình đường thẳng đi qua các điểm Q11, Q12, Q21, Q22 

**3. Vector & Matrix**
* So sánh sự khác nhau giữa Ma trận và Vector
![image](https://user-images.githubusercontent.com/42260182/100754212-6057e100-341d-11eb-8329-549d2c02c22f.png)

**Vector** 
* Phép cộng vector


![image](https://user-images.githubusercontent.com/42260182/100755419-bc6f3500-341e-11eb-9a54-c9bb6d5528e5.png)

* Tương tự các phép toán khác trong vector

![image](https://user-images.githubusercontent.com/42260182/100755827-2b4c8e00-341f-11eb-90fb-af4f5b17198b.png)

**Matrix**
Trong ma trận các phép cộng trừ tương tự như trong vector


![image](https://user-images.githubusercontent.com/42260182/100756138-81b9cc80-341f-11eb-98f9-eade3b3fdc2d.png)

* Phép nhân ma trận
Điều kiện để nhân ma trận là chiều rộng của ma trận này phải bằng chiều cao của ma trận còn lại

![image](https://user-images.githubusercontent.com/42260182/100756250-a2822200-341f-11eb-85a4-b1f2f687c3fb.png)

code

![image](https://user-images.githubusercontent.com/42260182/100758924-a2cfec80-3422-11eb-8f5c-8e03b3b44b83.png)


* Phép chuyển vị ma trận

![image](https://user-images.githubusercontent.com/42260182/100759049-c430d880-3422-11eb-9ef8-a934e58626c9.png)

code chuyển vị ma trận

![image](https://user-images.githubusercontent.com/42260182/100768054-07904480-342d-11eb-8006-1e6ed1a7921e.png)


* Phép nhân ma trận và vector

![image](https://user-images.githubusercontent.com/42260182/100768443-7b325180-342d-11eb-9288-9e2986047c4e.png)

Điều kiện nhân ma trận với vector là số hàng của ma trận phải bằng số phần tử trong vector

**Dot Product**

 
![image](https://user-images.githubusercontent.com/42260182/100770142-88504000-342f-11eb-9a45-7c050366c8e8.png)

Phép Dot Product thực chất là phép tính tích vô hướng của 2 vector 

Ví dụ:

![image](https://user-images.githubusercontent.com/42260182/100816851-a5a9fc00-3479-11eb-97c0-165ff41f7132.png)

* Dot Product có thể dùng để tìm độ dài hình chiếu của vetor hoặc tính góc tạo bởi các vector 

* Ứng dụng trong giảm chiều dữ liệu

![image](https://user-images.githubusercontent.com/42260182/100817808-5f559c80-347b-11eb-8113-e0af6c9b579b.png)




**Hadamard product**


![image](https://user-images.githubusercontent.com/42260182/100817966-beb3ac80-347b-11eb-9ea7-85e083317d27.png)

Hadamard product là phép nhân vị trí với vị trí trong vector

**Cosine similarity**

![image](https://user-images.githubusercontent.com/42260182/100826043-10643300-348c-11eb-9bc9-eb4cb9b16fda.png)

Tiến hành code:

![image](https://user-images.githubusercontent.com/42260182/100826094-2d990180-348c-11eb-8006-91a5f68d9363.png)

**4. Integral (tích phân)**
* Cho hàm số
![image](https://user-images.githubusercontent.com/42260182/100826877-ef044680-348d-11eb-93bc-bde6d5337968.png)

Tích phân của một hàm số là diện tích của hàm số tạo ra với các cận

* Áp dụng cho hàm rời rạc

![image](https://user-images.githubusercontent.com/42260182/100827235-dc3e4180-348e-11eb-8d87-f588a0716d6b.png)

* Tính Chất: Nó là kỹ thuật cũng hay được sử dụng trong các bài toán giải thuật thường dùng 
![image](https://user-images.githubusercontent.com/42260182/100827344-14de1b00-348f-11eb-8555-404c830f4628.png)


* Với hàm 2D


![image](https://user-images.githubusercontent.com/42260182/100832709-fed65780-349a-11eb-8863-e6c38b47895b.png)

Để tính diện tích hình màu đỏ thay vì tính toán bộ các ô nhỏ từng hình dùng for thì ta sẽ sử dụng quy tắc trừ như trên để tính, độ phức tạp sẽ thấp hơn khá nhiều lần


* Ứng dụng trong computer vision 

![image](https://user-images.githubusercontent.com/42260182/100833136-e74b9e80-349b-11eb-81ee-eee47e86d035.png)

* Tính mức độ giống nhau giữa hai hình ảnh

![image](https://user-images.githubusercontent.com/42260182/100833762-29291480-349d-11eb-8d58-8c6af863a033.png)


![image](https://user-images.githubusercontent.com/42260182/100833822-4d84f100-349d-11eb-9dc3-1c0d8f496cbb.png)



![image](https://user-images.githubusercontent.com/42260182/100833868-61c8ee00-349d-11eb-99c8-6df5711a23fd.png)


