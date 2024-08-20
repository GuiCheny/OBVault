
>稳定发行版本==3.5~3.10==，3.8 or 3.10

## 开发环境

- VScode:代码编辑器
- Pycharm:适合复杂项目的开发
- Jupyter notebook:交互式笔记本
- Anaconda:开源的Python发行版本
- Miniconda:仅仅提供conda包管理工具

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