# GIỚI THIỆU VỀ PYTHON

**I. BIẾN VÀ KIỂU DỮ LIỆU**
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

**II**. **CÁC PHÉP TOÁN CƠ BẢN TRONG PYTHON**
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

**III. HÀM**
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
**IV. TOÁN TỬ**
1. Các toán tử so sánh
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
2. Các toán tử điều kiện
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
**V. HÀM RANDOM VÀ CÁC MODULES TOÁN HỌC TRONG PYTHON**
##### CÁC HÀM TOÁN HỌC
1. Hàm tính giá trị tuyệt đối của 1 số:
```python
import math 
a = 3
b = -2
print(math.fabs(a)) #3.0
print(math.fabs(b)) #2.0
```
2. Hàm tính log(x)
```python
import math
x = 5
print(math.log(x)) # 1.6094379124341003 
print(math.log(math.e)) # log(e) = 1.0
```
3. Hàm tính sin(x)
```python
import math
x=2
print(math.sin(x)) #0.9092974268256817
```
4. Hàm tính số e
```python
import math
print(math.e) #2.718281828459045
```
5. Hàm tính exp
```python
import math
x=3
print(math.exp(x)) #20.085536923187668
```
6. Hàm tính căn bậc 2
```python
import math
x = 9
print(math.sqrt(x)) #3
```
7. Hàm tính cos
```python
import math
x = 3
print(math.cos(x)) #-0.9899924966004454
```
* Ta có thể dùng hàm sin,cos để tính tag, cotg

8. Hàm tính số PI
```python
import math
print(math.pi) #3.141592653589793
```
#### HÀM TÍNH RANDOM

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

# END WEEK 1

