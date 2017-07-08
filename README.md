# Python some key points 

## 07/07/2017 

### 1. 在Python中运行指定路径下的.py文件时，可运行以下代码： 
```python
import os
os.system('python 路径/文件名.py')
```

### 2. 在Python Shell里重复上一条命令，Alt + P 

### 3. Conditional statements 
> **if-elif-else**
```python
if   [condition] :   #! 如果此处条件满足，将跳过接下来的判断过程
elif [condition] : #! 如果此处条件满足，将跳过接下来的判断过程
else [condition] :
```
> **try-except**
```python
#! 只要try中有一个[action]无法实现就直接进入except，不再执行try中后续指令
try: #! try sth. if the action can be completed
    [action 1] 
    [action 2]
    [action 3] 
        .
        .
        .
except: #! otherwise act other way
    [action] 
```
> **Example:**
```python
rawstr = input('Enter a number:')
try:
    ival = int(rawstr)
except:
    ival = -1
if vial > 0:
    print('Nice work')
else:
    print('Not a number')
```
> **另一个很好的范例:**
```python
score = input("Enter Score: ")
try: 
    s = float(score)    #! 尝试将字符串score转化为float并赋值于变量s
except: 
    print("Error! Please enter a numeric input!")
    quit()              #! 如果无法将string转换为float则输出错误提示并退出此次程序执行
                        #! 如果转换成功，则开始执行接下来的if-elif-else语句
if s < 0.0 or s > 1.0:
    print("Error! Please enter a numeric input between 0.0 and 1.0")
    quit()              #! 如果无用户输入数值超过给定的范围则输出错误提示并退出此次程序执行
elif s >= 0.9:
    g = 'A'
elif s >= 0.8:
    g = 'B'
elif s >= 0.7:
    g = 'C'
elif s >= 0.6:
    g = 'D'
else:
    g = 'F'
print(g)
```

### 4. CMD中/IDE中 
***echo %cd%*** 用于显示当前具体路径</br>
执行一个死循环程序，***ctrl+c*** 就会终止程序执行，但是idle不会退出

## 08-07-2017

### 5. Building functions 
```python
def function_name([var]): #! 定义相当于存储某些指定内容的函数
```
> **示例:**
```python
def addtwo(a,b):
    added = a + b
    return added
    
x = adddtwo(3, 5)
print(x)

8
```

Functions that return values are ***fruitful*** functions </br> 
Functions that don't return values are ***non-fruitful*** functions

### 6. Loop and Iteration
> **while, continue and break**
```python
while [condition]:
    [action]
```
> **示例:**
```python
while True:
    line = input('>')
    if line[0] == '#':
        continue        #! 使程序跳回到第一行while上重新开始
    if line == 'done':
        break           #! 直接跳出while循环，执行print('Done!')
    print(line)
print('Done!')
```
```
> hello there
hello there
> # don't print this    #! 在'>'后输入的'#'使此行输入不被print出来
> print this
print this
> done
Done!
```
> **for, 示例:**
```python
#! 1. 判断和寻找最大值
largest_so_far = None
print('Before')
for the_num in [9, 41, 12, 3, 74, 15]:
    if largest_so_far is None:
       largest_so_far = the_num
    elif the_num > largest_so_far:
        largest_so_far = the_num
    print(largest_so_far, the_num)
print('After', largest_so_far)
```
```
Before -1
9 9
41 41
41 12
41 3
74 74
74 15
After 74
```
```python
#! 2. 用循环数数
zork = 0
print('Before', zork)
for thing in [9, 41, 12, 3, 74, 15]:
    zork = zork + 1
    print(zork, thing)
print('After', zork)
```
```
Before 0
1 9
2 41
3 12
4 3
5 74
6 15
After 6
```
```python
#! 3. 用循环累加
zork = 0
print('Before', zork)
for thing in [9, 41, 12, 3, 74, 15]:
    zork = zork + thing
    print(zork, thing)
print('After', zork)
```
```
Before 0
9 9
50 41
62 12
65 3
139 74
154 15
After 154
```
```python
#! 4. 用循环求平均值
count = 0
sum = 0
print('Before', count, sum)
for value in [9, 41, 12, 3, 74, 15]:
    count = count + 1
    sum = sum + value
    print(count, sum, value)
print('After', count, sum, sum / count)
```
```
Before 0 0
1 9 9
2 50 41
3 62 12
4 65 3
5 139 74
6 154 15
After 6 154 25.666666666666668
```
```python
#! Search
found = False
print('Before', found)
for value in [9, 41, 12, 3, 74, 15]:
    if value == 3:
        found = True
        print(found, value)
        break
    print(found, value)
print('After', found)
```
```
Before False
False 9
False 41
False 12
True 3
After True
```
