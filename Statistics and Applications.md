
**Statistics and Applications**
Không chỉ ứng dụng trong toán học mà thống kê còn sử dụng rất nhiều trong cuộc sống hiện tại có những công thức mà chúng ta hằng ngày hay sử dụng và những ứng dụng to lớn sẽ được mình trình bày ở dưới
**1. Mean**
Mean là tổng trung bình của tất cả các phần tử có trong dãy
![image](https://user-images.githubusercontent.com/42260182/100521195-b0903280-31d4-11eb-84fa-e546f4553cac.png)

Thực hiện code:
```python
def  mean(numbers):
#tổng của tất cả các phần tử trong dãy
s = sum(numbers)
#độ dài của dãy
N = len(numbers)
m = s/N
return m
arr = [1,2,3,4,5,6,7,8,9,10,11,12,13,14]
mean_value = mean(arr)
print(mean_value)
```

Kết quả:
```
7.5
```
Ứng dụng:
![image](https://user-images.githubusercontent.com/42260182/100521370-dff36f00-31d5-11eb-9cf3-b9b0ab0b2be9.png)

**2. Convolution (tích chập)**

![image](https://user-images.githubusercontent.com/42260182/100521418-2517a100-31d6-11eb-97a7-d45692abd4aa.png)

Khi sử dụng kernel cho xử lý ảnh
![image](https://user-images.githubusercontent.com/42260182/100528519-6d53b500-3210-11eb-9905-4899300c01b9.png)

Ví dụ:

![image](https://user-images.githubusercontent.com/42260182/100529695-bd387900-321c-11eb-92a7-64f5c0cf8d59.png)

Kết quả:
* Trước
![image](https://user-images.githubusercontent.com/42260182/100529711-e6590980-321c-11eb-9cb2-f4764f47e031.png)
* Sau
![image](https://user-images.githubusercontent.com/42260182/100529727-0983b900-321d-11eb-9c1e-9b2402b6b725.png)


* Một Số thao tác trong chỉnh sửa ảnh dùng Mean
![image](https://user-images.githubusercontent.com/42260182/100535744-34d2cc00-324e-11eb-89f1-827cc31db16c.png)

Ta có thể thay đổi, chỉnh sửa, tính toán các khoảng pixel hoặc các pixel trong ảnh

**2. Median**
![image](https://user-images.githubusercontent.com/42260182/100537765-cd247d00-325d-11eb-8e63-8e416e18d00f.png)

Median là giá trị ở giữa của 1 dãy các phần tử, thường sẽ lấy median sau khi đã sắp xếp tăng dần hoặc giảm dần

![image](https://user-images.githubusercontent.com/42260182/100537796-1379dc00-325e-11eb-8d6e-0aa7e023f3d7.png)

Trong ngành toán học chỉ số bắt đầu tử 1

**3. Range**
Range là giá trị khoảng cách giữa phần tử nhỏ nhất và phần tử lớn nhất trong dãy số
Ví dụ:
```python
import numpy as np
x = np.array([1,2,3,4,5,6,3,4,7,9,2,34,23,5,6])
mx = np.max(x)
print(mx)
mn = np.min(x)
print(mn)
Range = mx-mn
print(Range)
```

Kết quả:
```
34 
1 
33
```
**4. Variance**

Variance là công thức biểu diễn độ lệch phân tán so với mean

![image](https://user-images.githubusercontent.com/42260182/100539997-0c0dff00-326d-11eb-819e-a82be3492a7d.png)

Ví dụ:
![image](https://user-images.githubusercontent.com/42260182/100540183-4a57ee00-326e-11eb-9c45-5d20a3e41734.png)

**5.Hệ số tương quan (correlation coefficient)**
![image](https://user-images.githubusercontent.com/42260182/100546574-adf51200-3294-11eb-9ddc-0b33aedc729b.png)
* Một số tính chất

![image](https://user-images.githubusercontent.com/42260182/100546775-b69a1800-3295-11eb-9452-9dd31fa7d046.png)
![image](https://user-images.githubusercontent.com/42260182/100546786-c4e83400-3295-11eb-89cb-486eb5f72d8e.png)

* Tiến hành lập trình cho công thức dưới đây

![image](https://user-images.githubusercontent.com/42260182/100736413-46aa9f80-3405-11eb-9483-1093c60ef0d9.png)
code:

![image](https://user-images.githubusercontent.com/42260182/100741385-8fb22200-340c-11eb-8c30-1a72e6aa669d.png)


