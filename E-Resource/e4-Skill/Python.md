
>稳定发行版本==3.5~3.10==，3.8 or 3.10

## 开发环境

- VScode:代码编辑器
- Pycharm:适合复杂项目的开发
- Jupyter notebook:交互式笔记本
- Anaconda:开源的Python发行版本
- Miniconda:仅仅提供conda包管理工具

## Python 命令

- **python/python3**

```bash
>>> python
>>>
>>> python3 script.py
>>> 
>>> python --version
>>> 
>>> exit()
```

## 一些概念


- **软件包（package** 是一组相关的模块的集合。该目录下有一个特殊的文件，名为 `__init__.py`，文件可以为空。用于组织代码、复用代码和管理项目结构，使代码结构更加清晰和模块化。

- **模块（module**: 一个模块是一个包含 Python 代码的文件，通常以 `.py` 结尾。模块可以定义函数、类和变量，甚至可以包含可执行代码`if __name__ == '__main__':`。

- 






## 语法

### 数据类型和常变量

- 整数
- 浮点数
- 字符串
- 布尔值
- 空值：None
- 
### 变量和常量

#### 变量

动态语言，大小写英文、数字和_的组合，且不能用数字开头。

#### 常量

全部大写的变量名表示常量

### 字符串

#### 常用函数

- **`upper()`**：将字符串中的所有字母转换为大写。
- **`lower()`**：将字符串中的所有字母转换为小写。
- **`capitalize()`**：将字符串的第一个字母转换为大写，其余字母转换为小写。
- **`title()`**：将字符串中每个单词的首字母大写。
- **`strip()`**：移除字符串两端的空白字符（或者指定的字符)。
- **`lstrip()`**：移除字符串左侧的空白字符。
- **`rstrip()`**：移除字符串右侧的空白字符。
- **`replace(old, new)`**：将字符串中的所有指定子字符串替换为新字符串。
- **`split(separator)`**：根据指定的分隔符将字符串分割成列表，默认按空白字符分割。
- **`join(iterable)`**：将可迭代对象中的元素连接成一个字符串。
- ...

#### 字符串格式化

###### format

```bash
>>> 'Hello, {0}, 成绩提升了 {1:.1f}%'.format('小明', 17.125)
'Hello, 小明, 成绩提升了 17.1%'
```

###### f-string

```bash
>>> r = 2.5
>>> s = 3.14 * r ** 2
>>> print(f'The area of a circle with radius {r} is {s:.2f}')
'The area of a circle with radius 2.5 is 19.62'
```

### 切片

``` python
L = ['Michael', 'Sarah', 'Tracy', 'Bob', 'Jack'] # list or tuple
# 从0开始
L[:3]
# 从第二个元素开始
L[1:3]
# 倒数切片
L[-2:]
L[-2:-1]
```

### 列表

list是一种可变有序表，可以随时添加和删除其中的元素。

```bash
>>> classmates = ['Michael', 'Bob', 'Tracy']
>>> classmates
['Michael', 'Bob', 'Tracy']
>>> len(classmates)
3
```

索引从`0`开始，最后一个元素的索引是`len(classmates) - 1`。

```bash
>>> classmates[0]
'Michael'
>>> classmates[1]
'Bob'
>>> classmates[2]
'Tracy'
>>> classmates[-1]
'Tracy'
>>> classmates[3]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```

#### 常用函数

- **`append(item)`**：在列表末尾添加一个元素。
```python
lst = [1, 2, 3]
lst.append(4)
# lst 变为 [1, 2, 3, 4]
```
- **`extend(iterable)`**：在列表末尾一次性添加另一个可迭代对象的所有元素。
```python
lst = [1, 2, 3]
lst.extend([4, 5])
# lst 变为 [1, 2, 3, 4, 5]
``` 
- **`insert(index, item)`**：在指定索引位置插入一个元素。
```python
st = [1, 2, 3]
lst.insert(1, 'a')
# lst 变为 [1, 'a', 2, 3]
``` 
- **`remove(item)`**：移除列表中第一个匹配的元素。
```python
lst = [1, 2, 3, 2]
lst.remove(2)
# lst 变为 [1, 3, 2
```    
- **`pop(index=-1)`**：移除并返回指定位置的元素，默认移除最后一个元素。
```python
lst = [1, 2, 3]
lst.pop()
# lst 变为 [1, 2]
``` 
- **`clear()`**：移除列表中的所有元素。
```python
lst = [1, 2, 3]
lst.clear()
# lst 变为 []
```
- **`index(item, start=0, end=len(list))`**：返回列表中第一个匹配元素的索引，如果不存在则抛出异常。
```python
lst = [1, 2, 3, 2]
lst.index(2)
# 返回 1
```
- **`count(item)`**：返回列表中某个元素出现的次数。
```python
lst = [1, 2, 3, 2]
lst.count(2)
# 返回 2`
```
- **`sort(key=None, reverse=False)`**：对列表进行排序。可以指定 `key` 函数和排序顺序。
```python
lst = [3, 1, 2]
lst.sort()
# lst 变为 [1, 2, 3]
```  
- **`reverse()`**：将列表中的元素反转。
```python
lst = [1, 2, 3]
lst.reverse()
# lst 变为 [3, 2, 1]
```
- **`copy()`**：返回列表的浅拷贝。
```python
lst = [1, 2, 3]
new_lst = lst.copy()
# new_lst 为 [1, 2, 3]
```

### 元组

tuple，有序列表，不可修改。因为不可变，所以代码更安全。当定义一个tuple时，定义时tuple的元素就必须被确定下来。

```bash
>>> classmates = ('Michael', 'Bob', 'Tracy')

>>> t = (1, 2)
>>> t
(1, 2)

>>> t = ()
>>> t
()

```

Python规定，有歧义时按小括号进行计算，结果是`1`。所以，只有1个元素的tuple定义时必须加一个逗号`,`，来消除歧义：

```bash
>>> t = (1)
>>> t
1
>>> t = (1,)
>>> t
(1,)
```

**“可变”**的tuple

> 表面上看，tuple的元素确实变了，但其实变的不是tuple的元素，而是list的元素。

```bash
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```

### 条件判断

`if`、`elif` 和 `else` 加 `and`、`or`和`not`

```python
if 条件1: 
	执行语句1
elif 条件2:
	执行语句2
else: 
	执行语句3
```

```python
# 嵌套条件判断
x = 5
if x > 3:
    if x < 10:
        print("x 在 3 和 10 之间")

# 三元运算符（条件表达式）
x = 5 
y = 10 
result = "x 大于 y" if x > y else "x 小于等于 y" 
print(result)
```

### 内置函数

##### 数学相关

-  **`abs(x)`**：返回数字的绝对值。  
-  **`max(iterable, *iterables, key, default)`**：返回最大值。
-  **`min(iterable, *iterables, key, default)`**：返回最小值。
-  **`sum(iterable, start=0)`**：计算可迭代对象的和。   
- **`round(number, ndigits=None)`**：将数字四舍五入。

##### 类型转换

- **`int(x, base=10)`**：将一个值转换为整数。
- **`float(x)`**：将一个值转换为浮点数。  
- **`str(object)`**：将对象转换为字符串。
- **`bool(x)`**：将一个值转换为布尔值。
- **`list(iterable)`**：将可迭代对象转换为列表。
- **`tuple(iterable)`**：将可迭代对象转换为元组。
- **`dict(iterable)`**：创建字典。
- **`set(iterable)`**：将可迭代对象转换为集合。

##### 迭代相关

- **`range(start, stop, step)`**：生成一个整数序列。
- **`enumerate(iterable, start=0)`**：返回一个枚举对象，包含索引和值。
- **`zip(*iterables)`**：将多个可迭代对象打包成元组的迭代器

##### 输入输出

- **`print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`**：输出到控制台或文件。
- **`input(prompt=None)`**：接收用户输入。
- **`open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)`**：打开文件并返回文件对象。

##### 其他实用函数

- **`len()`**：返回对象（如字符串、列表、元组、字典等）的长度。
```python
len(object)

# 字符串
s = "hello"
# 列表
lst = [1, 2, 3, 4]
# 元组
tup = (1, 2, 3)
# 字典
d = {'a': 1, 'b': 2, 'c': 3}
# 集合
s = {1, 2, 3, 4}
print(len(s),len(lst),len(tup),len(d),len(s))
```
- **`type(object)`**：返回对象的类型。   
- **`sorted(iterable, *, key=None, reverse=False)`**：返回排序后的列表。
- **`eval(expression)`**：将字符串作为表达式执行并返回结果。
- **`any(iterable)`**：如果可迭代对象中有任一元素为真，返回 True。
- **`all(iterable)`**：如果可迭代对象中的所有元素为真，返回 True。
- **`map(function, iterable)`**：对可迭代对象中的每个元素应用函数并返回结果的迭代器。
- **`filter(function, iterable)`**：过滤可迭代对象中的元素，返回函数为真的元素。



### 文件路径

相对路径./../
绝对路径

### with

## 编程规范

### 注释

- Google风格
```python
"""
This module performs mathematical operations.

This module provides several functions to perform basic mathematical operations 
such as addition, subtraction, multiplication, and division.

Usage example:
    add_numbers(3, 4)
    divide_numbers(10, 2)

Modules:
    math_operations

Author:
    John Doe

Date:
    2024-08-19
"""
```
```python
"""_summary_

Args:
    pre_node_list (_type_): _description_
    last (_type_): _description_

Returns:
    _type_: _description_
"""

```

## 编程技巧

### 查找函数用法

查看官方文档

import <package_name> dir(<package_name>)
import <package_name> help(<package_name>.<function_name>)

在 Jupyter Notebook 中，您可以在函数后加上 `?` 来查看函数的文档字符串。
<package_name>.<function_name>?
import pandas as pd pd.DataFrame.head?


### 小技巧

###### 1. 变量交换
```python
a = 1
b = 2
a,b = b,a
```

## 调试技巧

print大法
pdb/ipdb命令行调试



## 使用技巧

  

1. Cell内容类型：Code。。。

2. TAB自动补全

3. 命令记不清楚可以在命令后面+'?'然后运行提示

4. 命令输入不清楚，将光标放入里边，shift双击TAB

5. jupyter notebook远程访问

6. 魔术命令

## 不同IDE的使用

### pycharm

### vscode

如果安装了 Python 插件，`# %%` 标记的代码可以分成单元块，类似于 Jupyter Notebook 的单元格。你可以通过单击单元格上方的运行按钮或者使用快捷键运行该代码块。
可以看到远程绘图等等


#### 

### jupyter notebook


## 常用软件包

##### pandas 

##### scipy

##### palettable

Python调色板库

##### pytorch

[Pytorch](https://pytorch.org/)是由Facebook开发的开源深度学习框架。

```bash
>>> python
>>> 
>>> import torch
>>> torch.cuda.is_available() #检查CPU是否可用
True
```