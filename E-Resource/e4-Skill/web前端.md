# web前端学习笔记 Html+Css+JavaScript
HTML骨架，CSS外貌，JavaScript行为

# HTML
## 系统架构
### B/S架构
Browser/Server（Browser对应Web前端开发：HTML、CSS、JavaScript Server服务器端：Java）  
优点：升级方便，只需要升级客户端  
缺点：速度慢、体验不好
### C/S架构
Client/Server  
优缺点相反
## HTML概述
HTML:Hyper Text Markup Language（超文本标记语言），规范标准由W3C制定
文本编辑器(.html)或专业开发工具
```htm
<!--
    注释<!DOCTYPE html> HTML5.0
-->>
<html>
    <head>
        <title>网页标题</title>
    </head>
    <body>
        网页内容
    </body>
</html>
```
HTML不区分大小写，语法松散不严格  
HTML中类相同的标签可以认为是同一类标签 一个标签可以有多个类中间用空格分开  
## HTML的基本标签
### 段落
```htm
<p>
    这是一个段落。
</p>
```
### 标题
```htm
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```
### 换行
```htm
<br> 
```
### 水平线
```htm
<hr>
<hr color="red" width="50%">
```
### 预留格式
```htm
<pre>
        ok，
        go
</pre>
```
### 删除字，插入字，粗体字，斜体字
```htm
<del>删除字</del>
<ins>插入字</ins>
<b>粗体字</b>
<i>斜体字</i>
```
### 右上角加字，右下角加字
```htm
10<sup>2</sup>
10<sub>2</sub>
```
## HTML的实体符号
当所用符号与HTML语言某些符号冲突时，用实体符号
```htm
<!--实体符号以&开始以；结束-->
b<a>c<br>
b&lt;a&gt;c
a&nbsp;&nbsp;&nbsp;&nbsp;c
```
## HTML的表格
### 插入表格
```htm
<table  align="center" border="1px" width="300px" height="150px">
    <tr>
        <td>a</td>
        <td>b</td>
        <td>c</td>
    </tr>
    <tr>
        <td>d</td>
        <td>e</td>
        <td>f</td>
    </tr>
    <tr>
        <td>g</td>
        <td>h</td>
        <td>i</td>
    </tr>
</table>
```
### 单元格合并
#### 行合并
row合并，删除下面的单元格
```htm
<table  align="center" border="1px" width="300px" height="150px">
    <tr>
        <td>a</td>
        <td>b</td>
        <td>c</td>
    </tr>
    <tr>
        <td>d</td>
        <td>e</td>
        <td rowspan="2">f</td>
    </tr>
    <tr>
        <td>g</td>
        <td>h</td>
        <!--
            <td>i</td>
        -->
    </tr>
</table>
```
#### 行合并
col合并,对删除哪个单元格没有要求
```htm
<table  align="center" border="1px" width="300px" height="150px">
    <tr>
        <td>a</td>
        <td>b</td>
        <td>c</td>
    </tr>
    <tr>
        <td>d</td>
        <td>e</td>
        <td>f</td>
    </tr>
    <tr>
        <td>g</td>
        <!--
            <td>h</td>
        -->
        <td colspan="2">i</td>
    </tr>
</table>
```
### th标签
th标签，table head,加粗居中
```htm
<table  align="center" border="1px" width="300px" height="150px">
    <tr>
        <th>编号</th>
        <th>薪资</th>
        <th>部门</th>
    </tr>
    <tr>
        <td>d</td>
        <td>e</td>
        <td>f</td>
    </tr>
    <tr>
        <td>g</td>
        <!--
            <td>h</td>
        -->
        <td colspan="2">i</td>
    </tr>
</table>
```
### thead tbody tfoot
划分表格部分，便于操作
```htm
<table  align="center" border="1px" width="300px" height="150px">
    <thead>
        <tr>
            <th>编号</th>
            <th>薪资</th>
            <th>部门</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>d</td>
            <td>e</td>
            <td>f</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>g</td>
            <!--
                <td>h</td>
            -->
            <td colspan="2">i</td>
        </tr>
    </tfoot>
</table>
```
## HTML的背景
设置背景颜色和图片
```htm
<body bgcolor="green" background="img\1.jpg">
</body>
```
## HTML的图片

```htm
src：图片源地址
alt：图片加载失败时的描述
height:高度，width:宽度，当只指定一个属性时，等比例缩放
title：鼠标悬停在图片上时显示的文字
<body>
    <img src="img/OIP-C.jpg" alt="百度" height="200" title="百度图片">
</body>
```
## HTML的超链接
超链接作用：通过浏览器向服务器发送请求，用户点击链接和在地址栏上输入URL本质上没有区别
BS结构：一个请求对应一个响应，B--请求-->S S--响应-->B
```htm
    <!--
        href:hot reference,资源地址，路径可以是绝对路径，可以是网络资源的路径或本地资源的路径
    -->
    <!--文字超链接-->
    <a href="https://image.baidu.com/">百度图片</a>
    <a href="demo1.html">demo1</a>
    <!--图片超链接-->
    <a href="https://www.baidu.com/">
        <img src="img/2.jpg" alt="百度">
    </a>
```
target属性：_blank(新窗口) _self：当前窗口 _top:顶级窗口 _parent:父窗口
## HTML的列表
列表可分为有序ol和无序ul
```htm
<!--有序列表-->
<ol type="A">
    <li>水果
        <ol type="a">
            <li>苹果</li>
            <li>梨子</li>
        </ol>
    </li>
    <li>甜品</li>
    <li>饮料</li>
</ol>
<!--无序列表-->
<ul>
    <li>中国
        <ul>
            <li>北京
                <ul>
                    <li>朝阳区</li>
                    <li>海淀区</li>
                </ul>
            </li>
            <li>上海</li>
            <li>天津</li>
        </ul>
    </li>
    <li>美国</li>
    <li>韩国</li>
</ul>  
</body>
```
## HTML的表单
表单用于收集用户信息，填写表单以提交数据给服务器。一个网页可以有多个表单。  
**表单提交格式**:HTTP协议规定action？name=value&name=value&name=value&name=value&name=value&name=value，因此超链接也可以提交信息（但只能提交固定信息 get请求）。
form标签action属性：指定服务器地址，请求路径；  
```htm
<body>
    <!--超链接和表单都可以向服务器发送请求，但是表单发送请求的同时可以携带数据-->
    <form action="https://www.baidu.com/">
        <table>
            <tr>
                <td>用户名</td>
                <td><input type="text" name="username"></td>
            </tr>
            <tr>
                <td>密码</td>
                <td><input type="password" name="userpwd"></td>
            </tr>
            <tr align="center">
                <td colspan="2">
                    <input type="submit" value="登录">
                    &nbsp;&nbsp;&nbsp;&nbsp; 
                    <input type="reset" value="清空">
                </td>
            </tr>
        </table>
    </form>
</body>
```
### 用户注册表单的实现
form表单的method属性“
    get：用户提交的信息会显示在浏览器的地址栏上  
    post:用户提交的信息不会显示在浏览器的地址栏上，提交信息敏感时使用  
```htm
    <form action="" method="post">
        用户名
        <input type="text" name="username">
        <br>
        密码
        <input type="password" name="userpwd">
        <br>
        确认密码
        <input type="password">
        <br>
        性别
        <!--单选按钮的value必须手动指定-->
        <input type="radio" name="genger" value="nan" checked>男
        <input type="radio" name="genger" value="nv" >女
        <br>
        兴趣爱好
        <input type="checkbox" name="insterest" value="smoke">抽烟
        <input type="checkbox" name="insterest" value="drink">喝酒
        <input type="checkbox" name="insterest" value="firehair">烫头
        <br>
        学历
        <select name="grade">
            <option value="gz">高中</option>
            <option value="bk">本科</option>
            <option value="ss">硕士</option>
        </select>
        <br>
        简介
        <!--文本域没有value属性-->
        <textarea name="profile" cols="30" rows="10"></textarea>
        <br>
        <!--提交 清空-->
        <input type="submit" value="注册">
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <input type="reset" value="清空">
    </form>
```
## HTML的下拉列表
select标签：multiple属性支持多选，size属性框显示条目数
```htm
<select name="sheng" multiple="multiple" size="2">
    <option value="sd">山东</option>
    <option value="hb">河北</option>
    <option value="sx">陕西</option>
    <option value="hn">湖南</option>  
</select>
```
## HTML的file控件
```htm
<input type="file">
```
## HTML的hidden控件
hidden使得提交表单的数据不在浏览器页面上显示。
```htm
    <form action="">
        <!--隐藏域-->
        <input type="hidden" name="id" value="12345">
        <!--提交-->
        <input type="submit" value="提交">
    </form>
```
## HTML readonly disabled
readonly和disable都是只读不能修改，但是readonly可以提交给服务器,disbaled不能。
```htm
    <form action="">
        用户代码<input type="text" name="usercode" value="101" readonly>
        <br>
        用户姓名<input type="text" name="username" value="LiChen" disabled>
    </form>
```
## HTML 控件的maxlength属性
```htm
<input type="text" maxlength="3">
```
## HTML元素中的id属性
HTML文档中，任何元素（节点）都有id属性，是该节点的唯一标识，同一文档中id值不能重复，提交表单数据时只和name有关，和id无关。js操作需要通过id拿到节点对象。
## HTML的div和span
div和span都可以称为“图层”，作用是用于灵活布局。div就是盒子套盒子，某认情况下div会独占行。

# CSS
## CSS是什么？有什么作用？
层叠样式表Cascading Stytle Sheet，修饰HTML页面，设置页面中元素的样式。常见会写+仿写CSS
## HTML嵌套使用Css样式的方法
### 第一种方式：标签内联
`<标签> Stytle="样式名：样式值；样式名：样式值；样式名：样式值；..."></标签>`
```htm
 <div style="width: 300px;height: 300px;background-color: darksalmon;display: block;border:1px solid black;";></div>
```
### 第二种方式：内部样式Stytle块
```htm
<head>
    <Stytle type="text/css">
    id选择器：
    #id{
        样式名：样式值；
        样式名：样式值；
        ...
    }
    标签选择器:
    标签{

    }
    类选择器：
    .类名{
        样式名：样式值；
        样式名：样式值；
        ...
    }
    ...
    </Stytle>
</head>
```
```htm
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>引入css样式的第二种方式：内部样式块方式</title>
    <style type="text/css">
        /* 注释 */
        /*--id选择器 */
        #usernameErrorMsg{
            color: aqua;

        }
        /*--标签选择器 */
        div{
            background-color: aquamarine;
            border: 1px solid red;
            width: 100px;
            height: 110px;
        }
        /*--类选择器 */
        .class1{
            color:blue;
        }
    </style>
</head>
<body>
    <span id="usernameErrorMsg">
        对不起，用户名不能为空！
    </span>
    <div></div>
    <div></div>
    <div></div>

    <input type="text" value="lichen" class="class1">

    <select name="" id="" class="class1">
        <option value="">专科</option>
        <option value="">本科</option>
    </select>
</body>
```
### 第三种方式：链入外部样式表文件，
最常用,将样式写到一个独立的.css文件当中，在需要的网页上直接引入css文件。这种方式容易维护，成本降低。  
.html  
注意使用的是href  
```htm
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>引入css样式的第三种方式:引入外部独立的css文件</title>
    <!--引入css-->
    <link rel="stylesheet" type="text/css" href="1.css">
</head>
<body>
    <a href="https://image.baidu.com/">百度图片</a>
    <span id="baiduSpan">点击！</span>
</body>
```
.css  
```css
a{
    text-decoration: none;
}

#baiduSpan{
    text-decoration:underline;
    cursor: pointer;
}
```
# JavaScript
## JavaScript概述
JavaScript是运行在浏览器上的脚本语言，使页面更具有交互性,JavaScript的“目标程序”以普通文本保存。JS是一门事件驱动型的编程语言，依靠事件去驱动，然后执行对应的程序，并且任何事件都会对应一个事件句柄，事件句柄是在事件单词前添加一个on，而事件句柄是以HTML标签的属性存在的。  
JavaScript三大块：ECMAScript DOM BOM  
- ECMAScript:JS的核心语法(ES规范)
- DOM:Document Object Model(文档对象模型)
- BOM:Browser Object Model(浏览器对象模型)
DOM和BOM的区别和联系：  
BOM的顶级对象是window,DOM的顶级对象是document，实际上BOM是包括DOM的。
![关系图](img\js结构图.jpg)

## HTML中嵌入JavaScript脚本
### 第一种方式：标签内联（加入句柄）
JS内置对象window,代表浏览器对象。JS字符串可以使用双引号，也可以使用单引号。JS语句结束可以使用分号‘;’，也可以不用。
```htm
<!--window可以省略不写-->
<input type="button" value="hello"
onclick="window.alert('hello js')">
```
### 第二种方式：内部脚本块
JavaScript脚本可以放在html文件的任意位置  
```htm
<script type="text/javascript">
    /*脚本块中的程序，页面打开时自上而下逐步执行*/
    window.alert('hello')
</script>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML中嵌入js代码的第二种方式 脚本块</title>
    <script type="text/javascript">
        /*脚本块中的程序，页面打开时自上而下逐步执行*/
        window.alert('js')
        /*alert函数阻挡代码的执行*/
    </script>
</head>
<body>
    <script type="text/javascript">
        /*脚本块中的程序，页面打开时自上而下逐步执行*/
        window.alert('hello js')
    </script>
</body>
</html>
```
### 第三种方式：链入js文件
常用 注意使用的是src  
```htm
<body>
    <script type="text/javascript" src="1.js">
        //这里写的代码不会执行
        window.alert('alert')
    </script>
    <!--同一个js文件可以被引入多次-->
    <script type="text/javascript" src="1.js"></script>
    
    <script type="text/javascript">
        /*脚本块中的程序，页面打开时自上而下逐步执行*/
        window.alert('hello jack')
    </script>
</body>
```
## JavaScript的标识符和关键字
标识符规则：字母数字下划线，不能以数字开头，不能使用关键字，严格区分大小写，理论上没有长度限制  
命名规范：见名知义；驼峰命名法
## JavaScript的变量
javascript是一种弱类型语言，没有编译阶段，变量可以随意赋值。当一个变量没有手动赋值的时候，系统默认赋值undefined  
变量声明：var 变量名  
变量复制：变量名 = 值；
### 局部变量和全局变量
全局变量  
在函数体之外声明的变量，其生命周期浏览器打开时声明，浏览器关闭时销毁，耗费内存空间。  
以下注意，当变量声明时没有变量类型，无论在哪声明的，都属于全局变量  
```javascript
function myfun() {
    mname = "ggbond"
}
myfun();
alert(mname);
```
局部变量  
函数体中声明的变量，包括形参。其生命周期在函数执行时开辟局部变量的内存空间，函数执行结束后内存空间释放。
## JavaScript的函数
javascript中的函数不需要返回值类型  
语法格式  
```javascript
//第一种方式：
function name(params) {
    body
}
//第二种方式
name = function(params{
    body   
}
```
## JavaScript的数据类型
javascript中的数据类型有原始类型和引用类型。  
原始类型：Undefined、Number、String、Boolean、Null  
引用类型：Object一级Object的子类  
ES6(ECMAScript规范)之后，新增Symbol类型。  
javascript有typeof运算符，可以在程序的运行阶段获取变量的数据类型。  
typeof使用的语法格式：typeof 变量名  
typeof的运算结果：注意字符串都是全部小写，"undefined"、"number"、"string"、"bollean"、"object"、"function"  
```javascript
function sum(a,b) {
    if(typeof a == "number" && typeof b =="number"){
        return a + b;
    }
    alert("a和b都必须为数字");
}   
var res =  sum(1,2);
alert("res"+res);

var i;
alert(typeof i);
var j = 10;
alert(typeof j);
//null显示为object类型，js的bug
var k = null;
alert(typeof k);
var h = "abc";
alert(typeof h);
var l = false;
alert(typeof l);
var m = new Object;
alert(typeof m);
```
### Undefined类型
Undefined类型只有一个值undefined，当变量没有手动赋值，系统默认赋值undefined，也可以手动赋值undefined。  
### Number类型
Number类型:数字、NaN...  
NaN:运算结果本来应该是数字，但是运算得到的不是一个数字。  
```javascript
var a = 100;
var b = "abc";
alert(a/b);
```
isNaN函数，用法：isNaN(数据)，结果是true表示不是数字  
parseInt():字符串转数字，并取整数位  
parseFloat():字符串转数字  
Math.ceil():向上取整  
### Boolean类型
布尔类型永远只有两个值:true和false。  
Boolean()函数的作用是将非布尔类型转换成布尔类型。  
if()括号中的类型为布尔类型。  
### String类型
javascript中字符串可以使用单引号也可以使用双引号。  
创建字符串对象：  
第一种方式：var s = "abc"; 注意：属于原始类型string  
第二种方式：var s = new String("abc"); 注意：String是内置的类，父类是Object。  
两种方式的属性公用  
### Object类型
Object类型是所有类型的超类，自定义的任何类型，默认继承Object。
属性：prototype,作用是给类动态地扩展属性和方法。  
定义的类默认继承object.  
定义类的语法：
    第一种方法：
    function 类名(形参){
        
    }
    第二种方法:
    类名 = function(形参){
        
    }
创建对象的语法：
    new 构造方法名(实参)，构造方法名和类名一致。
JS中类的定义和构造函数的定义是相同的，放在一起完成。  
### NaN undefined null
等同运算符==，只判断值是否相等  
全等运算符===，既判断值相等又判断数据类型是否相等  
```javascript
alert(null == NaN);//false
alert(null == undefined);//true
alert(undefined == NaN);//false

alert(null === NaN);//false
alert(null === undefined);//false
alert(undefined === NaN);//false
```
## JavaScript的常用事件
任何一个事件对应一个事件句柄，事件句柄是在事件单词前添加一个on。
```javascript
blur失去焦点  
focus获得焦点  
click鼠标单击  
dbclick鼠标双击  
keydown键盘按下  
keyup键盘弹起  
mousedown鼠标按下  
mouseover鼠标经过  
mousemove鼠标移动  
mouseout鼠标弹开  
mouseup鼠标弹起  
reset表单重置  
submit表单提交  
change下选列表选中项改变或是文本框内容改变  
select文本加载完毕  
load页面所有元素加载完毕 
```
## JavaScript回调函数的概念
由其他程序负责调用的函数称为回调函数  
## JavaScript注册事件
```javascript
<body>
    <script>
        function sayHello(){
            alert("say hello");
        }
    </script>
    <input type="button" id="mybutton1" value="1" onclick="doSome()">
    <input type="button" id="mybutton2" value="2">
    <input type="button" id="mybutton3" value="3">
    <script>
        function doSome(){
            alert("do some");
        }
        //第二种方式
        //获取对象。document为内置对象，代表整个HTML页面
        var btnObj = document.getElementById("mybutton");
        //注册事件
        btnObj.onclick = doSome;
        //获取对象。document为内置对象，代表整个HTML页面
        var btnObj1 = document.getElementById("mybutton1");
        //注册事件
        btnObj1.onclick = function(){
           alert("ok..");  
        }
    </script>
</body>
```
## JavaScript代码的执行顺序
```javascript
<body onload = "ready()">
    //等待页面加载完毕
    <script>
        function ready(){
            //获取对象。document为内置对象，代表整个HTML页面
            var btnObj1 = document.getElementById("mybutton1");
            //注册事件
            btnObj1.onclick = function(){
            alert("ok..");  
            }   
        }

    </script>
        <input type="button" id="mybutton1" value="1">
</body>
```
```javascript
<body>
    <script>
        //页面加载完毕
        window.onload = function(){
            //获取对象。document为内置对象，代表整个HTML页面
            var btnObj1 = document.getElementById("mybutton1");
            //注册事件
            btnObj1.onclick = function(){
            alert("ok..");  
            }
        }
    </script>
        <input type="button" id="mybutton1" value="1">
</body>
```
## JavaScript捕捉回车键
onkeydown事件对象存在keyCode属性  
```javascript
<script>
    function sayHello(){
        alert("Hello!");
    }
    window.onload = function(){
        var usernameElt = document.getElementById("username");
        //event传入事件对象
        usernameElt.onkeydown = function(event){
            if(event.keyCode === 13){
                sayHello(); 
            }
        }
    }
</script>
<input type="text" id="username">
```
## JavaScript的void运算符
语法：void(表达式),执行表达式但不返回任何结果。  
javascript：void(0),最常用。  
```javascript
 <a href="javascript:void(0)" onclick="alert('hello')">点击执行代码但并不跳转</a>
```
## JavaScript的控制语句
1. if
2. switch
3. while
4. do while
5. for
6. break
7. continue
8. for...in
9. with
```javascript
//i是数组的下标
for(var i in arr){

}
//for..in语句可以遍历对象的属性
User = function(username,password){
    this.username = username;
    this.password = password;
}
var user = new User();
for(var shuXingMing in user){
    //shuXingMing是字符串类型
    alert(typeof shuXingMing);
}
```
## DOM编程--获取文本框的value
```javascript
<script>
    window.onload = function(){
        var mybtn = window.document.getElementById("button");
        mybtn.onclick = function(event){
            alert(document.getElementById("text").value);
        }
        var t1 = document.getElementById("t1")
        //失去焦点时alert
        t1.onblur = function(){
            alert(t1.value);
        }
    }
</script>
```
## DOM编程--innerHTML和innerText操作div和span
innerHTML和innerText都是属性  
```javascript
<style>
    #div1{
        background-color:rgb(206, 195, 39);
        width: 600px;
        height: 600px;
        border:1px black solid;
    }
</style>
<script>
    window.onload = function(){
        document.getElementById("mybtn").onclick = function(event){
            var divElt = document.getElementById("div1");
            //divElt.innerHTML = "HTML代码";
            divElt.innerText = "文本内容";
        }
    }
</script>
<input type="button" id="mybtn" value="设置内容">
<div id="div1"></div>
```
## DOM编程-正则表达式
正则表达式：Regular Expression，主要用在字符串匹配，实际上是独立的学科  
认识常见的正则表达式符号；会写简单的正则表达式；看懂别人的正则表达式；创建正则表达式对象；学会找到自己需要的正则表达式，并测试其有效性  
### 常见的正则表达式符号
- ^：匹配字符串的开始位置
- $：匹配字符串的结束位置
- .：匹配除换行符以外的任意字符
- *：匹配前面的字符零次或多次
- +：匹配前面的字符一次或多次
- ?：匹配前面的字符零次或一次
- \d：匹配数字字符
- \D：匹配非数字字符
- \w：匹配字母、数字、下划线字符
- \W：匹配非字母、数字、下划线字符
- \s：匹配空白字符，包括空格、制表符、换行符等
- \S：匹配非空白字符
- []：匹配括号内的任意字符
- [^]：匹配除了括号内的字符以外的任意字符
- ()：分组，用于提取匹配的部分
- |：匹配多个表达式中的一个
- \：转义字符，用于匹配特殊字符本身
## 去除字符串的前后空白
trim消除前后空白.低版本的IE浏览器不支持字符串的trim函数  
```javascript
<script>

    window.onload = function(){
        var btn = document.getElementById("btn");
        btn.onclick = function(){
            var userName = document.getElementById("userName").value;
            userName = userName.trim();
            alert(">"+userName+"<");
        }
    }
</script>
```
## 复选框的全选和取消全选





