# Python some key points

## 07/07/2017

### 1. 在Python中运行指定路径下的.py文件时，可运行以下代码：
```python
import os
os.system('python 路径/文件名.py')
```

### 2. 在Python Shell里重复上一条命令，Alt + P

### 3. Conditional statements
> <b> if-elif-else <b>
```python
if   [condition] :   #! 如果此处条件满足，将跳过接下来的判断过程
elif [condition] : #! 如果此处条件满足，将跳过接下来的判断过程
else [condition] :
```
> <b> try-except <b>
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
> <b> Example: <b>
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
> <b> 另一个很好的范例：<b>
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

### 4. CMD中
```echo %cd% 用于显示当前具体路径```

## 08-07-2017

```python
def function_name([var]): #! 定义相当于存储某些指定内容的函数
```
> <b> 示例: <b>
```python
def addtwo(a,b):
    added = a + b
    return added
    
x = adddtwo(3, 5)
print(x)

8
```
