# II. PYTHON ADVANCED 1
## 1. LIST
Cấu trúc của LIST
![image](https://user-images.githubusercontent.com/42260182/99139777-55a3fa80-266e-11eb-91d6-eedcb0172db2.png)

Ví dụ:
```python
#list rỗng
list_empty = []

#list số nguyên
list_int = [0,1,2,3,4,5,6,7,8,9]

#list chứa nhiều kiểu dữ liệu
list_mix = ['tôi',20,'+',1,'đẹp trai','không yêu ai','cận',0.75]
list_mix = ["mylove",[1,9,9,9]]
```

**1.1 INDEX trong LIST**
![image](https://user-images.githubusercontent.com/42260182/99139884-41143200-266f-11eb-97bf-94df154618e6.png)

Trong python index bắt đầu từ 0, trong list có 2 loại index là Forward và Backward, Forward bắt đầu từ 0 còn Backward bắt đầu từ -1 vì  -0 = 0 nên phải đánh số từ -1

**1.2 Slicing**
![image](https://user-images.githubusercontent.com/42260182/99140005-63f31600-2670-11eb-9d95-2913017d89fa.png)

+Cách lấy phần tử sẽ là [a,b) ví dụ 2:4 thì sẽ chỉ lấy 2,3
+Cách lấy phần tử dạng [a,-b] thì ta sẽ áp dụng Index từ phần trước ví dụ muốn lấy data[2:4] ta có thể lấy data [2:-6], cái này cho mọi người tự khám phá...
**1.3. Add 1 phần tử vào List** 
+Sử dụng câu lệnh .append() để thêm phần tử vào cuối list
ví dụ:
```python
data = [0,1,2,3,4,5,6]
data.append(1)
data
```
Kết quả:
```
[0, 1, 2, 3, 4, 5, 6, 1]
```
**1.4 UPDATE**
+Nếu muốn thay đổi một phần tử trong list thì ta chỉ cần dùng câu lệnh sau
```python
data = [0,1,2,3,4,5,6]
data[2] = 4
data
```
kết quả:
```
[0, 1, 4, 3, 4, 5, 6]
```
**1.5 CÁC PHÉP TOÁN TRONG LIST**
1.5.1 Phép cộng
```python
a = [0,1,2,3]
b = [4,5,6,7]
a+b
```
Kết quả:
```
[0, 1, 2, 3, 4, 5, 6, 7]
```
**1.5.2 Phép nhân**
```python
data = ['toan','yeu','?']
data = data*3
data
```
Kết quả: 
```
['toan', 'yeu', '?', 'toan', 'yeu', '?', 'toan', 'yeu', '?']
```
**1.5.3  Sort() - Sắp xếp các phần tử**
ví dụ:
+Theo thứ tự tăng dần
```python
data = [1,3,2,4,6,5]
data.sort()
data
```
Kết quả
```
[1, 2, 3, 4, 5, 6]
```
+Theo thứ tự giảm dần
```python
data = [1,3,2,4,6,5]
data.sort(reverse = True)
data
```
kết quả:
```
[6, 5, 4, 3, 2, 1]
```

**1.6 Xóa một phần tử**
ví dụ:
```python
data = [1,2,3,2,4,6]
data.pop(2) #xóa vị trí tại index=2
data
```
kết quả: 
```
[1, 2, 2, 4, 6]
```
**1.7 Xóa nhiều phần tử**
```python
data = [6,5,5,6,4,2,1]
del data[1:3]  #Xóa phần tử có index [1,3)
data
```
kết quả:
```
[6, 6, 4, 2, 1]
```
Câu lệnh .clear() xóa toàn bộ các phần tử trong list
```
data = ['Tôi','là','Toàn',1,9,9,9]
data.clear()
data
```
kết quả:
```
[]
```
**1.8 index() trong list**
+index() nhận vào một giá trị và trả về chỉ số nhỏ nhất trong list
ví dụ:
```python
data = [1,2,3,8,3,2,4,5,8]
data.index(8)
```
kết quả:
```
3
```
**1.9 count() trong list**
+count() nhận vào một giá trị và trả về số lần xuất hiện của phần tử đó trong list
ví dụ:
```python
data = [1,3,3,2,5,6,7,8]
data.count(3)
```
kết quả:
```
2
```
+ Với String hoặc các kiểu dữ liệu khác trong list cũng tương tự

**1.10  reverse()**
+reverse() có chức năng đảo ngược list
```python
data = ['toi','ten','la','Toàn']
data.reverse()
data
```
kết quả:
```
['Toàn', 'la', 'ten', 'toi']
```
**1.11 copy()**
+copy() sao chép toàn bộ list hiện tại sang 1 list khác 
ví dụ:
```python
data = ['1','2','3','4','5','6']
data_coppy = data.copy()
data_coppy
```
kết quả:
```
['1', '2', '3', '4', '5', '6']
```

**1.12 List Comprehension**
Cấu trúc
list_name = [expression for element in iterable]
ví dụ
```python
list = [d for d in 'Hello']
list
```
kết quả:
```
['H', 'e', 'l', 'l', 'o']
```
ví dụ
```python
list = [i for i in range(10) if i%2 == 0]
list
```
kết quả:
```
[0, 2, 4, 6, 8]
```
 List Comprehension là một cách xây dựng ngắn gọn thay ví sử dụng vòng for rồi append từng phần tử ta có thể dùng List Comprehension để có thể nhanh hơn

## 2 DATA TYPE (kiểu dữ liệu)

**2.1 Các kiểu dư liệu cơ bản**
![image](https://user-images.githubusercontent.com/42260182/99161017-21891200-2720-11eb-81ec-102cdf8c3646.png)

+Cũng giống như trong  các ngôn ngữ lập trình khác các kiểu dữ liệu cơ bản của python tương tự như các ngôn ngữ khác, điểm khác biệt ở chỗ Python có một số kiểu dữ liệu đặc biệt bao gồm List, Tupple, Dictionary, Class

![image](https://user-images.githubusercontent.com/42260182/99161057-83497c00-2720-11eb-8de5-4908ad28ea36.png)

**2.2 Mutable and immutable**

![image](https://user-images.githubusercontent.com/42260182/99161173-e4be1a80-2721-11eb-9266-be7fd94fae94.png)

+Immutable cụ thể khi các kiểu dữ liệu là Integer, Float, String, Boolean, Tupple được tạo ra thì không thể thay đổi, nếu muốn thay đổi thì phải tạo ra vùng nhớ mới và liên kết lại với nhau, còn vùng nhớ được tạo ra trước đó vẫn ở nguyên vị trí đó 

ví dụ:

![image](https://user-images.githubusercontent.com/42260182/99161267-28fdea80-2723-11eb-91ac-ef9ad6f086e3.png)

+Mutable cụ thể là có thể thay đổi địa chỉ ô nhớ của các phần tử trong list chứ không thể thay đổi địa chỉ của cái list đó

ví dụ
```python
a_list = [1,2,3]
print(a_list,id(a_list))
print(id(a_list[1]))

a_list[1] = 5
print(a_list,  id(a_list))
print(id(a_list[1]))
```
kết quả:
```
[1, 2, 3] 140393869754760 
10914528
 [1, 5, 3] 140393869754760 
10914624
```

# 3 String
**3.1 ASCII TABLE** 
![image](https://user-images.githubusercontent.com/42260182/99161960-92cdc280-272a-11eb-88c8-129759f64f2f.png)

**Các Hàm String thường dùng trong python**
1. Biểu diễn String
```python
text1 = 'tôi yêu Huyền 11/15/2020'
text2 = "tôi yêu Huyền 11/15/2020"
text3 = '''tôi yêu Huyền 11/15/2020'''
text4 = """tôi yêu Huyền 11/15/2020"""
text5 = "tôi yêu Huyền '11/15/2020'"
text6 = '"tôi yêu Huyền" 11/15/2020'
print(text1)
print(text2)
print(text3)
print(text4)
print(text5)
print(text6)
```
kết quả:
```
tôi yêu Huyền 11/15/2020 
tôi yêu Huyền 11/15/2020 
tôi yêu Huyền 11/15/2020 
tôi yêu Huyền 11/15/2020 
tôi yêu Huyền '11/15/2020' 
"tôi yêu Huyền" 11/15/2020
```
2. Insert into a String
ví dụ 
```python
value1 = 'Huyền'
value2 = 'Toàn'
day = 15
print("hello mọi người mình là Toàn và mình yêu %s. mới từ ngày hôm nay thui" %value1)
print("đây là một cặp đôi %s %s"%(value1,value2))
print("%d %s %s"%(day,value1,value2))
```
kết quả:
```
hello mọi người mình là Toàn và mình yêu Huyền. mới từ ngày hôm nay thui 
đây là một cặp đôi Huyền Toàn
15 Huyền Toàn
```
+Nếu là kiểu String ta phải dùng dấu %s, Integer phải dùng dấu %d...

* Cách nên dùng 
```python 
value1 = 'this'
value2 = 5
s = "{n1},{n2}".format(n1 = value1, n2 = value2)
print(s)
```
kết quả:
```
this,5
```
 dùng cách này cũng giống như việc nó tự động ép kiểu của các giá trị giúp ta đỡ nhầm lẫn

2. isdigit(), islower(), isalpha(), isupper()

![image](https://user-images.githubusercontent.com/42260182/99162797-3a9bbe00-2734-11eb-807e-4b413f4c325c.png)

3. istitle(), isspace(), count(), len()

![image](https://user-images.githubusercontent.com/42260182/99162821-b138bb80-2734-11eb-8839-e3fd6ff40ad4.png)
4. title(), capitalize(), swapcase()
![image](https://user-images.githubusercontent.com/42260182/99162855-0f659e80-2735-11eb-8d6c-cd816f149e4b.png)

5. upper(), lower(), center()
![image](https://user-images.githubusercontent.com/42260182/99162866-3a4ff280-2735-11eb-8460-e4ce9f9affa6.png)
6. strip(), replace(), partition()
![image](https://user-images.githubusercontent.com/42260182/99162876-6a979100-2735-11eb-835f-8b8d447ead11.png)

7. endswith(), startswith(), find()

![image](https://user-images.githubusercontent.com/42260182/99162879-797e4380-2735-11eb-9032-628e40ea3625.png)

