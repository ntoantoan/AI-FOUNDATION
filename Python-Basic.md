# GIỚI THIỆU VỀ PYTHON

**I. PYTHON CƠ BẢN**
**1. BIẾN VÀ KIỂU DỮ LIỆU**
 - khai báo trong python như sau:   ten_bien = giá_trị_của_biến 
 -  ví dụ: 
 ```python
    name = "Toàn"
    print(name)
    name1 = "Xin chào mình tên là Toàn"
    print(name1) 
    name2 = 't' #  lưu ý  " " = ' ' 
    print(name2)
    name3 = "a"
    print(name3)
    value = 10423343
    print(value)
    Value1 = 13.2323
    print(value1)
    value2 = True
    print(value2)
``` 
kêt quả:
 ```python
 Toàn
 Xin chào mình tên là Toàn
 t
 a 
10423343
13.2323
True
 ``` 
 Để kiểm tra kiểu dữ liệu trong biến ta có thể dùng lệnh
  ``` python
  a=4
  b="hello"
  print(type(a))
  print(type(b))
  #bạn đọc có hãy tự kiểm tra
   ``` 
Trong python không cần khai báo kiểu dữ liệu như các ngôn ngữ lập trình C,C++,JAVA...

**2**. **CÁC PHÉP TOÁN CƠ BẢN TRONG PYTHON**
+ Độ ưu tiên của các phép toán tương tự như các ngôn ngữ C,C++,JAVA
 ``` python
 #khai báo 
 a = 4 
 b = 5
 #phép cộng
 print(a+b)
 
 #phép trừ
 print(a-b)
 
 #phép nhân
 print(a*b)
 
 #phép chia
 print(a/b)
 
 #phép chia lấy dư
 print(a%b)
 
 #phép chia lấy số nguyên
 print(a//b)
 
 #phép lũy thừa 
 print(a**b)
 
  ``` 
  kết quả:
   ```python
   9 
   -1 
   20 
   0.8
   4
   0 
   1024
 ``` 
 
ví dụ:
Chuyển đổi độ C sang độ F dựa trên công thức: $$F=\frac{9C}{5}+32$$
   ```python
   temp_c = float(input('Nhập nhiệt độ theo độ C'))
   temp_f = ((9/5)*temp_c)+32
   print(temp_f)
 ```
kết quả:
`Nhập nhiệt độ theo độ C:`
`37.4`

**3. HÀM**
Khuôn dạng của hàm trong python
```python
def function_name(parameters):
    '''
    code
    '''
    return result
```
ví dụ 1: Tính diện tích hình chữ nhật biết cạnh a=3, b=4

```python
a=3
b=4
def ans(a,b):
  result = a*b
  return result
s = ans(a,b)
print(s)
#12
```
**4. TOÁN TỬ**
4.1. Các toán tử so sánh
```python
a = 4
b = 5
#kiểm tra a có bằng b hay không
print(a==b)

#kiểm tra a có khác b hay không
print(a!=b)

#kiểm tra a>b
print(a>b)

#kiểm tra a<b
print(a<b)

#kiểm tra a>=b hay không
print(a>=b)

#kiểm tra a<=b hay không
print(a<=b)

```
kết quả
```
False 
True 
False 
True 
False
True
```
4.2. Các toán tử điều kiện
* **IF**  
```
if(điều kiện):
#thực thi
else:
#thực thi
```

ví dụ 1: 
  $$ReLU(x) = \left\{\begin{matrix}
0
&if 
&x<=0
\\x
 &if 
 &x>0
\end{matrix}\right.$$

```python
def Relu(x):
  result = 0
  if(x>0):
    result = x
  return result
val1 = Relu(3)
val2 = Relu(-4)
print(val1)
print(val2)
```
kết quả:
```
3
0

```
ví dụ 2:
$$LBP(x,y) = \left\{\begin{matrix}
0
&if 
&x==y
\\1
 &if 
 &x>y
\\
-1
& if 
& x<y
\end{matrix}\right.$$

```python
def LBP(x,y):
  result = 0
  if(x>y):
   result = 1
  if(x<y):
   result = -1
  return result
val1 = LBP(1,2)
val2 = LBP(2,2)
val3 = LBP(3,2)
print(val1)
print(val2)
print(val3)
```
kết quả:
```
-1
0
1
```
**5. HÀM RANDOM VÀ CÁC MODULES TOÁN HỌC TRONG PYTHON**
##### CÁC HÀM TOÁN HỌC
5.1. Hàm tính giá trị tuyệt đối của 1 số:
```python
import math 
a = 3
b = -2
print(math.fabs(a)) #3.0
print(math.fabs(b)) #2.0
```
5.2. Hàm tính log(x)
```python
import math
x = 5
print(math.log(x)) # 1.6094379124341003 
print(math.log(math.e)) # log(e) = 1.0
```
5.3. Hàm tính sin(x)
```python
import math
x=2
print(math.sin(x)) #0.9092974268256817
```
5.4. Hàm tính số e
```python
import math
print(math.e) #2.718281828459045
```
5.5. Hàm tính exp
```python
import math
x=3
print(math.exp(x)) #20.085536923187668
```
5.6. Hàm tính căn bậc 2
```python
import math
x = 9
print(math.sqrt(x)) #3
```
5.7. Hàm tính cos
```python
import math
x = 3
print(math.cos(x)) #-0.9899924966004454
```
* Ta có thể dùng hàm sin,cos để tính tag, cotg

5.8. Hàm tính số PI
```python
import math
print(math.pi) #3.141592653589793
```
#### 6. HÀM TÍNH RANDOM

1. Random số thưc trong khoảng (0-1)
```python
#
import random
#sinh ra các số thực trong khoảng từ 0-1
print(random.random()) #0.6619725063097497
```
2. Random số tự nhiên trong khoảng (a, b)
```python
import random
print(random.randint(2,6)) #5
```

**II.  PYTHON NÂNG CAO**

#### 1. Vòng Lặp FOR
Kiến trúc của vòng lặp for
![image](https://user-images.githubusercontent.com/42260182/99060863-44f27680-25d3-11eb-8cd0-cebbaaa8f7b6.png)

Sự khác nhau giữa ngôn ngữ lập trình python ở kiến trúc vòng for với java, C, C++ chính là thụt lề thay vì cặp "{" "}" dưới đây là ví dụ cho sự khác biệt này

Ví dụ 1
```python
for i in range(10):
  print(i)
```
kết quả:
```
0 
1 
2 
3 
4 
5 
6 
7 
8 
9
```
Ví dụ 2
```python
string = ['toi','yeu','co','ay','nhung','co','ay','khong','yeu','toi']
for i in string:
  print(i)
```
Kết quả:
```
toi
yeu
co
ay
nhung
co
ay
khong
yeu
toi
```


##### 1.1. TỪ KHÓA CONTINUE
```python
for i in range(10):
  if(i==4):
    continue
  print(i)
```
Kết quả:
```
0
1
2
3
5
6
7
8
9
```
câu lệnh Continue sẽ không thoát ra khỏi vòng lặp mà nó sẽ lập tức dịch chuyển về chỗ vòng for và thực hiện tăng giá trị biến đếm trong vòng for lên 1 đơn vị, như trong ví dụ ta có thể thấy với i == 4 thì lập tức dịch chuyển về vòng for rồi biến đếm tăng lên 5 sau đó tiếp tục vòng for cho đến hết

##### 1.2 Câu Lệnh BREAK
```python
for i in range(10):
  if i==5:
    break
  print(i)
```
Kết quả:
```
0
1
2
3
4
```
=> Khi gặp câu lệnh break lập tức sẽ thoát ra khỏi vòng lặp gần nhất


* Ví dụ tính số PI
như chúng ta biết số pi ~ 3.14 ta dùng rất nhiều trong cuộc sống lẫn trong các chương trình học nhưng để tính số pi thì chắc hẳn ít người có thể biết cách tính. Trên đây mình sẽ mô phỏng cách tính số pi bằng hàm ngẫu nhiên trong python

+Về cơ sở toán học
 
![image](https://user-images.githubusercontent.com/42260182/99065531-1b891900-25da-11eb-8e22-8c7dea09e5dd.png)
Tạo hình vuông có cạnh là s = 2
Tạo hình tròn nằm bên trong hình vuông có bán kính r = 0.5 như trên hình ta có thể thấy
gọi As là diện tích của hình tròn As = pi * r^2
gọi Ac là diện tích của hình vuông Ac = s*s
Ns là số điểm ngẫu nhiên sinh ra trong hình vuông với giá trị trong [-1,1]
Nc là số điểm ngẫu nhiên sinh ra trong hình tròn với giá trị trong [-1,1]

Với Ns, Nc với số lượng cực kì lớn sẽ bao trùm toàn bộ hình vẽ 
ta có: 
![image](https://user-images.githubusercontent.com/42260182/99066285-4aec5580-25db-11eb-8615-2df44ad0a9f1.png)
<=>
![image](https://user-images.githubusercontent.com/42260182/99066389-78390380-25db-11eb-926e-223c49765654.png)

![image](https://user-images.githubusercontent.com/42260182/99066436-8b4bd380-25db-11eb-8ba0-3472072e5cd9.png)

Tiến hành lập trình:
![image](https://user-images.githubusercontent.com/42260182/99066604-cea64200-25db-11eb-84db-459f2dc511fd.png)


Ví dụ tính số Euler *e* = 2.71828
![image](https://user-images.githubusercontent.com/42260182/99066904-52f8c500-25dc-11eb-9bd0-9444de9a2a3f.png)

+Tiến hành lập trình
![image](https://user-images.githubusercontent.com/42260182/99067320-17aac600-25dd-11eb-93d7-fc5cb04d1c40.png)

Ví dụ tính căn bậc 2 của một số bất kì
dựa vào công thức:
![image](https://user-images.githubusercontent.com/42260182/99138865-7a946f80-2666-11eb-9caf-5a8de20ed641.png)
+Tiến hành lập trình:
![image](https://user-images.githubusercontent.com/42260182/99138877-94ce4d80-2666-11eb-8ed3-7f403563d7d7.png)

#### 2. VÒNG LẶP WHILE
Cấu trúc của vòng lặp while
![image](https://user-images.githubusercontent.com/42260182/99138958-43728e00-2667-11eb-982c-f56bf4a66e8e.png)

ví dụ:
```python
i = 0
while i<10:  #i<10 là điều kiện lặp
  print(i)
  i += 1
print("out_while")
```
kết quả:
```
0 
1 
2 
3 
4 
5 
6 
7 
8 
9 
out_while
```
2.1 WHILE True
while True là vòng lặp vô hạn mà nếu không có câu lệnh thoát khỏi vòng lặp thì nó sẽ lặp mãi mãi ở trong vòng lặp đó 
+Ví dụ sinh số ngẫu nhiên đến khi nào tìm được số cần tìm thì thoát khỏi vòng lặp
![image](https://user-images.githubusercontent.com/42260182/99139125-a87ab380-2668-11eb-86c8-5d692feb38d7.png)

![image](https://user-images.githubusercontent.com/42260182/99139134-bd574700-2668-11eb-8a6d-19d2834dba45.png)

END PYTHON BASIC
