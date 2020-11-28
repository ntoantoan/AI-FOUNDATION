# III. PYTHON ADVANCED 2
**1. TUPLE**

![image](https://user-images.githubusercontent.com/42260182/99186616-297a9d80-2784-11eb-9d25-c76d3569271d.png)

+Tạo 1 tupple
```python
t = (1,'Toàn',3)
print(t[0])
print(t[1])
print(t[2])
```
kết quả:
```
1
Toàn
3
```
Nhận biết giữa list và tupple list kí hiệu [], tupple ()
**1.1 Phép toán + và phép***

+Phép cộng
```python
t1 = (1,0)
print(t1)
#phép cộng ở đây chính là phép nối tupple
t1+=(2,)
print(t1)
```
kết quả:
```
(1, 0) 
(1, 0, 2)
```
+Phép nhân
```python
t1 = (1,)
t2 = t1 * 5
print(t2)
```
kết quả:
```
(1, 1, 1, 1, 1)
```


**1.2 Các hàm trong tupple**
* Hàm len()
trả về số lượng phần tử trong tupple

```python
tupple = (1,2,3,4,'toan',5,6)
len(tupple)
```
kết quả:
```
7
```
* Hàm Index()
Nhận vào một giá trị và trả về vị trí của phần tử đó trong tupple
* Hàm count()
 Tương tự như trong list count() nhận vào một giá trị và trả về số lần xuất hiện của nó trong tupple
 * Hàm sorted()
 Tương tự như trong list, sorted() nhận vào một tupple ngẫu nhiên và trả về tupple đã sắp xếp
 * Hàm zip()
 Hàm zip có chức năng nối 2 tupple lại thành 1 tupple nó gần giống với pair<> trong c++ 

ví dụ: 
```python
t1 = (1,2,3,4,5,6,7,8)
t2 = ('Nguyễn','Đình','Toàn','1999','a','b')
t3 = zip(t1,t2)
for a,b in t3:
print(a,b)
```
 kết quả:
 ```
 1 Nguyễn 
 2 Đình 
 3 Toàn 
 4 1999
 5 a 
 6 b
 ```
từ ví dụ ta có thể thấy với 2 tupple nó sẽ lấy theo tupple có độ dài ngắn hơn

* Hàm tính min() ,max(), sum()
ví dụ:
```python
t = (1,2,3,4,5,6,7,8,9)
#trả về phần tử nhỏ nhất trong tupple
print(min(t))
#trả về phần tử lớn nhất trong tupple
print(max(t))
#trả về tổng các phần tử trong tupple
print(sum(t))
```
kết quả:
```
1
9
45
```

**1.3 IMMUTABLE**
+Trong tupple ta không cho phép chỉnh sửa các phần tử, trong trường hợp trong tupple có object thì có thể thay đổi được
xem xét 2 ví dụ dưới đây:
```python
t = (1,2,3,4,5,6,7,8,9,10)
t[2]=1
```
```
---------------------------------------------------------------------------

TypeError Traceback (most recent call last)

[<ipython-input-2-6edbdb6a09e8>](https://localhost:8080/#) in <module>()  1  t  =  (1,2,3,4,5,6,7,8,9,10)  ----> 2  t[2]=1  

TypeError: 'tuple' object does not support item assignment
```


```python
t = (1,2,3,[4,5])
t[3][2] = 10
t
```
kết quả:
```
(1, 2, 3, [10, 5])
```

**2 SET**
+Set là một tập hợp mà trong đó mỗi phần tử chỉ xuất hiện 1 lần
+kí hiệu trong set là {}
```python
set = {1,2,2,3,3,4}
set
```

**2.1 Các hàm trong set**

![image](https://user-images.githubusercontent.com/42260182/99421112-9d59a900-2930-11eb-98de-585b2ae02712.png)

**3. DICTIONARY**
Cấu trúc:
            dictionary_name = {key-1:value-1, …, key-n:value-n}
 +Dictionary gọi là 1 từ điển bao gồm các key và value được ngăn cách nhau bởi dấu hai chấm và mỗi phần tử cách nhau bằng dấu phẩy, trong dictionary các key phải khác nhau

ví dụ:
```python
para={'learning_rate':0.1,'optimizer':'Adam','metric':'Accuracy','drop_out':0.2}
para
```
kết quả:
```
{'drop_out': 0.2,
 'learning_rate': 0.1,
 'metric': 'Accuracy',
 'optimizer': 'Adam'}
```

* Update 1 gía trị:
```python
para = {'learning_rate':  0.1,  'optimizer':'Adam','metric':'Accuracy','drop_out':0.2}
para['metric'] = 'F1 score'
para
```
kết quả:
```
{'drop_out': 0.2,
 'learning_rate': 0.1,
 'metric': 'F1 score',
 'optimizer': 'Adam'}
```  

* Hàm copy()

```python
para = {'learning_rate':  0.1,  'optimizer':'Adam','metric':'Accuracy','drop_out':0.2}
para2 = para.copy()
para2
```
kết quả:
```
{'drop_out': 0.2,
 'learning_rate': 0.1,
 'metric': 'Accuracy',
 'optimizer': 'Adam'}
```

+Hàm copy() có nhược điểm là nó có thể thay đổi cả đối tượng mà mình đã copy, để khắc phục điều này ta sử dụng một hàm chính là deepcopy()

![image](https://user-images.githubusercontent.com/42260182/99469551-91dca100-2975-11eb-8b67-14a9f1841599.png)

* Hàm keys() trả về toàn bộ key trong dictionary
* Hàm getvalues() trả về toàn bộ value trong dictionary
* 
![image](https://user-images.githubusercontent.com/42260182/99469918-5ee6dd00-2976-11eb-9910-4108cd7c55e8.png)

* Hàm get() 
Nhận vào một key và trả về 1 value 
![image](https://user-images.githubusercontent.com/42260182/99470319-1f6cc080-2977-11eb-801e-89c406438462.png)

* Hàm pop() 
Xóa một cặp key-value tương ứng

![image](https://user-images.githubusercontent.com/42260182/99470473-6490f280-2977-11eb-9b54-b62fd4498a24.png)

* Hàm popitem() 
Lấy ra một phần tử ở cuối dictionary
![image](https://user-images.githubusercontent.com/42260182/99470643-a326ad00-2977-11eb-9681-78ce06cdc0d6.png)

 * Hàm clear() 
 Xóa toàn bộ các phần tử của một dictionary
 ![image](https://user-images.githubusercontent.com/42260182/99470724-ccdfd400-2977-11eb-8875-8b0b37db36bb.png)

**4. FILE**
##### ĐỌC FILE
Để kết nối được các file trong colab ta tiến hành các bước sau:
```python
from google.colab import drive
drive.mount('/content/drive')
```
Sau đó copy đường link để có được quyền truy cập vào drive, dữ liệu file sau khi thao tác trên đây sẽ lưu về drive 

* Kết nối FILE
```python
#kết nối file
file = open('hello.txt','r')
#đọc dữ liệu trong file
data = file.read()
#in thông tin trong file
print(data)
data.close()
```

Kết quả:
```
xin chào
```
* Đọc từng dòng trong file

Định dạng file có dạng như sau:
![image](https://user-images.githubusercontent.com/42260182/99504888-b7d46680-29b2-11eb-95d5-a6796c03f065.png)

```python
from google.colab import drive
drive.mount('/content/drive')
file = open('hello.txt','r')
data = file.readlines()
for i in data:
  print(i)
file.close()
```
Kết quả:
```
xin chào 
tôi tên là Toàn 
21 tuổi
```


#### GHI FILE

```python
file = open('new_file.txt','w')
text1 = 'abcd xyz \n'
file.write(text1)
text2 = '1234 4567 \n'
file.write(text2)
file.close()
```

* Thêm phần tử vào file có sẵn
 open('file_path', 'a') 
ví dụ
```python
from google.colab import drive

drive.mount('/content/drive')
file = open('new_file.txt','w')
text1 = 'abcd xyz'
file.write(text1)
text2 = '1234 4567'
file.write(text2)
file.close()
# 'a' thay cho 'w' vì nếu vẫn là 'w' thì sẽ gây ra hiện tượng ghi đè
f = open('new_file.txt','a')
text3 = 'qwe'
f.write(text3)
file.close()
```

* Một số hàm hữu ích

Kiểm tra file đã tồn tại hay chưa

```python
import os

file = 'hello.txt'
check = os.path.exists(file)
print(check)
file_check = 'helloworld.txt'
check_check = os.path.exists(file_check)
print(check_check)
```
Kết quả:
```
True
False
```
+String splitting()

```python
string = 'Tôi,tên,là,Nguyễn,Đình,Toàn'
token = string.split(',')
for i in token:
  print(i)
```

Kết quả:
```
Tôi
tên
là
Nguyễn
Đình
Toàn
```
+String joining()
```python
string = ['0','hello','12-02-1999']
string_join = (',').join(string)
string_join
```
Kết quả:
```
0,hello,12-02-1999
```

### Một số famework nổi tiếng
![image](https://user-images.githubusercontent.com/42260182/99528260-a00bdb00-29d0-11eb-941d-3ac096fe4983.png)
