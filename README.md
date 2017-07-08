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
> <b> Eample: <b>
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
### 4. CMD中
```echo %cd% 用于显示当前具体路径```
