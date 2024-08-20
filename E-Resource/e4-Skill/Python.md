## 一些概念


- **软件包（package）** 是一组相关的模块的集合，用于组织代码、复用代码和管理项目结构。它通过将多个模块组织在一个目录中形成一个逻辑的分层结构，便于维护和使用。一个包是一个包含模块的目录，并且该目录下有一个特殊的文件，名为 `__init__.py`。这个文件可以为空，但它标识了这个目录是一个包，可以包含多个模块或子包。包的作用是组织模块，使代码结构更加清晰和模块化。

- **模块（module）**: 一个模块是一个包含 Python 代码的文件，通常以 `.py` 结尾。模块可以定义函数、类和变量，甚至可以包含可执行代码。


## 开发环境

- pytharm
- vscode
- jupyter notebook

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

import <package_name> dir(<package_name>)

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