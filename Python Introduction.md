---
slideOptions:
  transition: slide
  theme: black   #主題
---

# Introduction

---

![](https://i.imgur.com/dfVzUpg.png)

> Python is a programming language that lets you work more quickly and integrate your systems more effectively.

---

### Sample Code

[The sample code in colab](https://colab.research.google.com/drive/11ZdSRbk2C6fcI6RB10N1CbAdZQp5u6ng?usp=sharing)

---

## 計算機 calculator
```python=
2 + 2 
```
```
4
```
```python=
2 + 2 
2 - 2
2 * 3
4 / 2 
```
```
2.0
```

---

## Output 輸出
###  print() 函式 function

:::info
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
:::
```
*objects : print content can be nothing or 
           multiple things seprated by ,
sep='' : seperate charachter default ' ' is space
end='' : end character default \n is new line
```

---

## print() Example

```python=
print(1,2,3,4)
print()
print(1,2,3,4, sep=',')
print(1,2,3,4, end=' -- ')
print('end no')
print(1,2, sep='=', end=' ** \n')
```
```
1 2 3 4

1,2,3,4
1 2 3 4 -- end no
1=2 ** 
```

---

## print() Example

```python=
print('2 + 2 = ', 2 + 2) 
print('2 - 2 = ', 2 - 2)
print('2 * 3 = ', 2 * 3)
print('4 / 2 = ', 4 / 2)
print('2 ** 3 = ', 2 ** 3)
print('5 // 2 = ', 5 // 2)
print('5 % 2 = ', 5 % 2)
```
```
2 + 2 =  4
2 - 2 =  0
2 * 3 =  6
4 / 2 =  2.0
2 ** 3 =  8
5 // 2 =  2
5 %  2 =  1
```

---

### 註解 comment

:::info
註解是別人看的
 註解於 # 之後
:::
 
```python=
# 我是單獨一行的註解
print(2+2) # 我是程式之後的註解
```
```
4
```

---

### 程式加上註解
```python=
print('2 + 2 = ', 2 + 2)  #  加法
print('2 - 2 = ', 2 - 2)  #  減法
print('2 * 3 = ', 2 * 3)  #  乘法
print('4 / 2 = ', 4 / 2)  #  除法
print('2 ** 3 = ', 2 ** 3)  # 次方
print('5 // 2 = ', 5 // 2)  # 商數
print('5 % 2 = ', 5 % 2)   # 餘數
```
```
2 + 2 =  4
2 - 2 =  0
2 * 3 =  6
4 / 2 =  2.0
2 ** 3 =  8
5 // 2 =  2
5 %  2 = 1
```

---

##  使用者輸入

input() 函式
:::info
input([prompt])
prompt is hint string it is option
:::
If the prompt argument is present, it is written to standard output without a trailing newline. The function then reads a line from input, <font color=#FF6600>**converts it to a string**</font>(stripping a trailing newline), and returns that.

---

## 使用者輸入範例

```
# input no prompt
name = input("") 
print(name)

# input with prompt
name = input("please enter your name : ") 
print("hello,", name) 
```
```
Ted
Ted
please enter your name : Ted
hello,Ted
```

---

## 字串格式 f-string
### string formatting
:::info
f' ... {變數名稱}' f" ... {變數名稱}" 
用大括號 {變數名稱} 表示直接填入變數的值
:::
```python=
name1 = 'Eric'
name2 = 'John'
hello_str = f'Hello {name1}, my name is {name2}'
print(hello_str)
print(f'Hi {name2}, Lovely to meet you.')
```
```
Hello Eric, my name is John
Hi John, it is nice to meet you.
```

---

### f-string express
:::info
f' ... {表達式或呼叫函數} '
用大括號 {表達式或呼叫函數}，Python會求出其結果並填入字串
:::
```python=
print(f'The Answer of 24 * 8 + 4 is {24 * 8 + 4}')
name = 'ERIC'
print(f'My name is {name} and lowercase is {name.lower()}')
import math #　載入數學模組
print(f'The PI is {math.pi}')　# 取出pi
```
```
The Answer of 24 * 8 + 4 is 196
My name is ERIC and lowercase is eric
The Pi is 3.141592653589793
```

---

### f-string format floats

{math.pi:.3f}  the number 3 of decimal places  

```python=
import math #　載入數學模組
print(f'The PI is {math.pi:.3f}') # 取出pi 
print(f'The PI is {math.pi:.5f}') # 取出pi
```
```
The PI is 3.142
The PI is 3.14159
```

---

### f-string width and justify
```
{2:>05}
{   2   :        >                0        5  }
{number : jusity_to_right fill_character width} 
```
```python=
print("{1:5}      is -"+f'{1:5}-')
print("{12:05}    is -"+f'{1:05}-')
print("{123:>5}   is -"+f'{1:*>5}-')
print("{1234:<5}  is -"+f'{1:*<5}-')
```
```
{1:5}      is -    1-
{12:05}    is -00012-
{123:>5}   is -**123-
{1234:<5}  is -1234*-
```