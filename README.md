
<!-- vim-markdown-toc GFM -->

* [第一章 Python基础](#第一章-python基础)
    * [1.1 Python数学操作符](#11-python数学操作符)
    * [1.2 整型、浮点型和字符串数据类型](#12-整型浮点型和字符串数据类型)
    * [1.3 字符串连接和复制](#13-字符串连接和复制)
    * [1.4 在变量中保存值](#14-在变量中保存值)
        * [1.4.1 赋值语句](#141-赋值语句)
        * [1.4.2 变量名规则](#142-变量名规则)
    * [1.5 第一个程序](#15-第一个程序)
    * [1.6 强制类型转换](#16-强制类型转换)
        * [str()、int()和float()函数](#strint和float函数)
* [第二章 控制流](#第二章-控制流)
    * [2.1 布尔值](#21-布尔值)
    * [2.2 比较操作符](#22-比较操作符)
    * [2.3 布尔操作符](#23-布尔操作符)
        * [2.3.1 二元布尔操作符](#231-二元布尔操作符)
        * [2.3.2 not操作符](#232-not操作符)
    * [2.4 控制流语句](#24-控制流语句)
        * [2.4.1 if语句](#241-if语句)
        * [2.4.2 else语句](#242-else语句)
        * [2.4.3 elif语句](#243-elif语句)
        * [2.7.4 while循环语句](#274-while循环语句)
        * [2.7.5 跳出循环](#275-跳出循环)
        * [2.7.5 for循环和range()函数](#275-for循环和range函数)

<!-- vim-markdown-toc -->
## 第一章 Python基础 ##

### 1.1 Python数学操作符 ###


| 操作符 | 操作        |
|--------|-------------|
| \*\*   | 指数        |
| %      | 取模/取余数 |
| //     | 整除        |
| /      | 除法        |
| *      | 乘法        |
| +      | 加法        |
| -      | 减法        |

### 1.2 整型、浮点型和字符串数据类型 ###

Python中最常见的数据类型有**整型**、**浮点型**和**字符串**。其中，总是使用单引号( \')包围住字符串(例如'Hello'或'Hello World!')

### 1.3 字符串连接和复制 ###

通常情况下使用 **+** 操作符进行字符串连接

```py
>>> 'Alice' + 'Bob'
'AliceBob'
```

字符串和整型值无法使用 **+** 操作符

在用于整型或浮点型值时, **\*** 操作符表示乘法, 但 **\*** 操作符作用于一个字符串和一个整型值时，它变成了字符串复制：

```py
>>> 'Alice' \* 5
'AliceAliceAliceAliceAlice'
```

**\*** 操作符只能用于两个数字(作为乘法), 或者一个字符串和一个整型(作为字符串复制操作符)。其它则会报错

### 1.4 在变量中保存值 ###

#### 1.4.1 赋值语句 ####

格式为：

    变量名 = 值

#### 1.4.2 变量名规则 ####

1.  只能是一个词
2. 只能包含字母数字和下划线
3. 不能以数字开头

变量名是区分大小写的。这意味着，spam、Spam、SPAM、aPaM是4个不同的变量。官方命名风格是使用下划线

### 1.5 第一个程序 ###

```py
#!/usr/bin/env python
# -*- coding: utf-8 -*-

print('Hello world!')
print("What is your name?")
my_name = input()
print('It is good to meet you,' + my_name)
print('The length of your name is:')
print(len(my_name))
print('What is your age?')
my_age = input()
print('You will be ' + str(int(my_age) + 1) + ' in a year.')
```

### 1.6 强制类型转换 ###

#### str()、int()和float()函数 ####

str()、int()和float()函数将分别求值为传入值的字符串、整数和浮点数形式

---

## 第二章 控制流 ##

### 2.1 布尔值 ###

布尔值数据数值：True和False

### 2.2 比较操作符 ###

| 操作符 | 含义     |
|:-------|:---------|
| ==     | 等于     |
| !=     | 不等于   |
| <      | 小于     |
| >      | 大于     |
| <=     | 小于等于 |
| >=     | 大于等于 |

这些操作符根据给他们提供的值，求值为True和False

> 请注意，整型或浮点数的值永远不会和字符串相等, 另一方面，<、>、<=、>=操作符金作用于整型和浮点型值

### 2.3 布尔操作符 ###

3个布尔操作符（and、or和not）用于比较布尔值

#### 2.3.1 二元布尔操作符 ####

and和or操作符总是接受两个布尔值（或表达式），所以它们被认为是二元操作符。

and真值表：

| 表达式          | 求值为 | 
|:----------------|:-------|
| True and True   | True   | 
| True and False  | False  | 
| False and True  | False  | 
| False and False | False  | 

or真值表：

| 表达式         | 求值为 |
|:---------------|:-------|
| True  or True  | True   |
| False or True  | True   |
| True  or False | True   |
| False or False | False  |

#### 2.3.2 not操作符 ####

not操作符只作用于一个布尔值（或表达式）。求相反的布尔值，且可以嵌套

```py
>>> not True
False
>>> not not not not True
True
```

### 2.4 控制流语句 ###

#### 2.4.1 if语句 ####

在Python中包含以下部分：

- if关键字
- 条件（即求值为True或False的表达式）
- 冒号
- 在下一行开始，缩进的代码块（称为if子句）

```py
if name == 'Alice':
    print('Hi, Alice.')
```


#### 2.4.2 else语句 ####

else语句包含：

- else关键字
- 冒号：
- 在下一行开始，缩进的代码块（称为else子句）

```py
if name == 'Alice':
    print('Hi Alice.')
else
    print('Hello, stranger.')
```


#### 2.4.3 elif语句 ####

elif语句包括

- elif关键字
- 条件（即求值为True或False的表达式）
- 冒号：
- 在下一行开始，缩进的代码块（称为elif子句）

```py
if name == 'Alice':
    print('Hi Alice.')
elif age < 12 :
    print('You are not Alice, kiddo.')
```

#### 2.7.4 while循环语句 ####

while语句包含下面部分：

- 关键字
- 条件（即求值为True或False的表达式）
- 冒号：
- 从新行开始，缩进的代码块（称为while子句）

```py
spam = 0
while spam < 5:
    print('Hello World.')
    spam = spam + 1
```

在while循环中，条件总是在每次迭代开始检查，如果条件为True，子句就会执行，然后，再次检查条件。当条件第一次为False时， while子句跳过

#### 2.7.5 跳出循环 ####

1. break语句：直接跳出循环，执行循环之后的代码
2. continue语句：跳回循环开始处，重新对循环条件求值

#### 2.7.5 for循环和range()函数 ####

可以让循环执行固定次数，for语句格式for i in range(3)这样，总是包含以下部分：

- for关键字
- 一个变量名
- in关键字
- 调用range()函数
- 冒号
- 从下一行开始，缩退的代码块（称为for子句）

```py
print('My name is ')
for i in range(5):
    print('Jimmy Five Times (' + str(i) + ')')
```

