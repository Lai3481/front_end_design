###  1.什么是JavaScript

- JavaScript 是世界上最流行的语言之一，是一种运行在客户端的脚本语言 （Script 是脚本的意思）

1995年，Netscape（网景）公司的 Brendan Eich（布兰登·艾奇，用了10天就把JavaScript搞了出来。原名LiveScript，为了蹭蹭当红明星Java热度，就改成JavaScript了（瞬间就火了），事实上他们两没啥关系。 

![](https://pic.baike.soso.com/ugc/baikepic2/10608/20220507075706-1889073100_jpeg_249_314_10556.jpg/300)

### 2.JavaScript的组成

**JavaScript 包括 ECMAScript、DOM、BOM**

![JavaScript组成部分](https://img-blog.csdnimg.cn/a9331f588aa54d43b22ae207249f0e1f.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0F1Z2Vuc3Rlcm5fUVhM,size_16,color_FFFFFF,t_70#pic_center)

- #### 🔥**ECMAScript**

**ECMAScript** 是由ECMA 国际（ 原欧洲计算机制造商协会,European Computer Manufacturers Association）进行标准化的一门编程语言，这种语言在万维网上应用广泛，它往往被称为 JavaScript 或 JScript，但实际上后两者是 ECMAScript 语言的实现和扩展。

- #### 🔥DOM

**文档对象模型**（Document Object Model，简称DOM），是W3C组织推荐的处理可扩展标记语言的标准编程接口。通过 DOM 提供的接口可以对页面上的各种元素进行操作（大小、位置、颜色等）。

- #### 🔥BOM

**BOM** (Browser Object Model，简称BOM) 是指浏览器对象模型，它提供了独立于内容的、可以与浏览器窗口进行互动的对象结构。通过BOM可以操作浏览器窗口，比如弹出框、控制浏览器跳转、获取分辨率等。

### 3.JavaScript引入方式

##### 3.1 ✨行内式JS

把JavaScript代码写在html标签当中，这种方式称为行内式js

```html
<input type="button" value="点我试试" onclick="javascript:alert('芜湖起飞~')" />
```

注意: 可读性差，html代码和js代码耦合性过高；一般不推荐使用。

##### 3.2 ✨内联式JS

把页面的js代码写在script标签当中，称为内联式js

```html
<script>
     alert('芜湖起飞~');
</script>
```

1.可以将多行js代码写到script标签中

2.内联式js是学习时常用的方式

##### 3.3  ✨外联式JS

使用:  a.新建js文件
          b.在页面通过script标签引入 js文件

```html
<script src="my.js"></script>
```

1. 利于HTML页面代码结构化，把单独JS代码独立到HTML页面之外，既美观，又方便
2. 引用外部JS文件的script标签中间不可以写代码
3. 适合于JS代码量比较大的情况

### 4. JavaScript基本语法

##### 🔥4.1 注释

###### 4.1.1 单行注释

```javascript
// 单行注释
```

- 快捷键: ctrl + / 

###### 4.2.2 多行注释

```javascript
/*
  多行注释   
*/
```

- 快捷键: shift + alt + a 

### 🔥4.2 变量

定义: 变量是用于存放数据的容器，我们通过变量名获取或者是修改数据。

本质:变量的本质实在内存申请的一块存放数据的空间。

##### 🔥4.3 变量的初始化

1.通过**var**(variable变量)关键字，可以声明一个变量，使用该关键字声明变量后，计算机会自动在内存申请一块空间。

2.var后面跟上一个变量名，相当于对刚刚申请的空间起名，我们可以通过这个变量名来访问或者修改变量的值。

```javascript
var a; // 声明一个变量a
a = 10;// 变量a赋值为10
console.log('----------------------------------------------------------------')
var a = 10 ; // 声明变量a同时赋值为10,这个过程叫变量的初始化
```

注意: 

变量的命名规范: 1.由字母(A-Z,a-z)，数字(0-9)，下划线(_)，美元符号($)组成，不能以数字开头，如:usrAge,num01,__name

​                           2.严格区分大小写，如:var a 和 var A 是两个不同的变量

​                           3.不能是关键字 ，如 var ，for等                             

​                           4.遵循驼峰命名法。首字母小写，后面单词的首字母需要大写

#####  4.4🔥JavaScript数据类型

JS 把数据类型分为两类： 1.基本数据类型(Number,String,Boolean,Undefined,Null)

​                                          2.复杂数据类型(Object)

######  4.4.1 基本数据类型🔥

<img src="img/image-20231215152412241.png" alt="image-20231215152412241" style="zoom:150%;" />

##### 4.5 🔥 运算符

###### 4.6 算术运算符 🔥

概念：算术运算使用的符号，用于执行两个变量或值的算术运算。

<img src="img/image-20231215152659692.png" alt="image-20231215152659692" style="zoom:150%;" />

###### 4.7 关系运算符🔥

关系运算符是**两个数据进行比较时所使用的运算符**，比较运算后，会**返回一个布尔值**(true / false)作为比较运算的结果。

<img src="img/image-20231215153905036.png" alt="image-20231215153905036" style="zoom:150%;" />

###### 4.8 赋值运算符🔥

<img src="img/image-20231215154508243.png" alt="image-20231215154508243" style="zoom:150%;" />

##### 4.9 逻辑运算符🔥

逻辑运算符是用来进行布尔值运算的运算符，其返回值也是布尔值

<img src="img/image-20231215154721256.png" alt="image-20231215154721256" style="zoom:150%;" />

1.🎈逻辑与：两边都是 true才返回 true，否则返回 false

<img src="img/image-20231215154831944.png" alt="image-20231215154831944" style="zoom:150%;" />

2.🎈逻辑或：两边都为 false 才返回 false，否则都为true

<img src="img/image-20231215154937110.png" alt="image-20231215154937110" style="zoom:150%;" />

3.🎈逻辑非：逻辑非（!）也叫作取反符，用来取一个布尔值相反的值，如 true 的相反值是 false

```javascript
var isOk = !true;
console.log(isOk);  // false
//逻辑非（!）也叫作取反符，用来取一个布尔值相反的值，如 true 的相反值是 false
```

### 5.1 流程控制🔥

流程控制主要有三种结构，分别是顺序结构、分支结构和循环结构，这三种结构代表三种代码执行的顺序

##### 5.2 分支结构🔥

 1.if语句🔥

```javascript
if(条件表达式) {
    //条件表达式成立执行的代码
}
//否则什么也不干
```

```javascript
var usrAge = prompt('请输入您的年龄:');
if(usrAge >= 18)
{
      alert('您的年龄合法，欢迎来到老子网吧享受学习的乐趣！');
}
```

2.if else 语句🔥

```javascript
// 条件成立，执行if里面代码，否则执行else里面的代码
if(条件表达式)
{
    //[如果]条件成立执行的代码
}
else
    {
        //[否则]执行的代码
    }
```

3.if else if 语句🔥

```javascript
if(条件表达式1)
{
    语句1;
}
else if(条件表达式2)
{
    语句2;
}
else if(条件表达式3)
{
    语句3;
}
else
{
    //上述条件都不成立执行此处代码
}
```

##### 5.3 循环🔥

1.for循环🎈

在程序中，一组被重复执行的语句被称之为**循环体**，能否继续重复执行，取决于循环的**终止条件**。由循环体及循环的终止条件组成的语句，被称之为**循环语句**

```javascript
for(初始化变量;条件表达式;操作表达式)
{
    //循环体
}
```

```javascript
//求1-100所有整数的和
var sum = 0;
for (var i = 1; i <= 100; i++) {
    var sum = sum + i;
}
console.log(sum);
```

### 6.数组🔥

数组(Array)是指一组数据的集合，其中的每个数据被称作元素，在数组中可以存放任意类型的元素。数组是一种将一组数据存储在单个变量名下的优雅方式。

```javascript
//普通变量一次只能存储一个值
var num = 10;
//数组一次可以存储多个值
var arr =[1,2,3,4,5];  // arr[0]  1
//索引 (下标) ：用来访问数组元素的序号（数组下标从 0 开始）
//长度:使用“数组名.length”可以访问数组元素的数量（数组长度） // arr.length  5
```

我们可以通过 for 循环索引遍历数组中的每一项

```javascript
// 数组索引访问数组中的元素
var arr = ['red','green', 'blue'];
console.log(arr[0]) // red 
console.log(arr[1]) // green
console.log(arr[2]) // blue

// for循环遍历数组
var arr = ['red','green', 'blue'];
for (var i = 0; i < arr.length; i++){
    console.log(arrStus[i]);
}

//数组的长度 
arr.length 

//数组的下标
从0开始，最大下标为arr.length-1
```

### 7.对象🔥

在 JavaScript 中，对象是一组无序的相关属性和方法的集合，所有的事物都是对象，例如字符串、数值、数组、函数等。

`{ }` 里面采取键值对的形式表示

- 键：相当于属性名
- 值：相当于属性值，可以是任意类型的值（数字类型、字符串类型、布尔类型，函数类型等）

```javascript
var star = {
    name : '韩金龙',
    age : 18,
    sex : '男',
};
```

***对象的调用***：

- 对象里面的属性调用 : 对象.属性名 ，这个小点 . 就理解为“ **的** ”
- 对象里面属性的另一种调用方式 : 对象[‘属性名’]，注意方括号里面的属性必须**加引号**
- 对象里面的方法调用：对象.方法名() ，注意这个方法名字后面**一定加括号**

### 8.函数🎈

函数：就是封装了一段**可被重复调用执行的代码块**。通过此代码块可以实现大量代码的重复使用。

##### 8.1 函数的使用🎈

函数在使用时分为两步：**声明函数**和**调用函数**

1.声明函数🎈

```javascript
//声明函数，通过function关键字
function 函数名(){
    //函数体代码
}
def 函数名():
```

2.调用函数🎈

```javascript
//调用函数
函数名(); //通过调用函数名来执行函数体代码
//注意:函数只有被调用才会执行
```

##### 8.2 函数的参数🎈

**在声明函数时**，可以在函数名称后面的小括号中添加一些参数，这些参数被称为**形参**，而在**调用该函数**时，同样也需要传递相应的参数，这些参数被称为**实参**。

<img src="img/image-20231215161352625.png" alt="image-20231215161352625" style="zoom: 150%;" />

```javascript
//利用函数求任意两个数的和
// 声明函数
function getSum(num1,num2){
    console.log(num1+num2)
}
// 调用函数
getSum(1,3) //4
getSum(6，5) //11
```

##### 8.3 return关键字🎈

有的时候，我们会希望函数将值返回给调用者，此时通过使用 return 语句就可以实现。

eturn 语句的语法格式如下：

```javascript
// 声明函数
function 函数名（）{
    ...
    return  需要返回的值;
}
// 调用函数
函数名();    // 此时调用函数就可以得到函数体内return 后面的值
```

- 在使用 return 语句时，函数会停止执行，并返回指定的值
- 如果函数没有 return ，返回的值是 undefined

### 9. DOM🎈

文档对象模型（Document Object Model，简称 DOM），是 W3C 组织推荐的处理可扩展标记语言（HTML或者XML）的标准编程接口

W3C 已经定义了一系列的 DOM 接口，通过这些 DOM 接口可以改变网页的内容、结构和样式。

<img src="img/image-20231215162655636.png" alt="image-20231215162655636" style="zoom:150%;" />

##### 9.1 获取页面元素DOM🎈

```html
<div>芜湖起飞~</div>
<script>
    // 1.因为我们文档页面从上往下加载，所以得先有标签，所以script写在标签下面
    // 2.get 获得 element 元素 by 通过 驼峰命名法
    // 3.参数 id是大小写敏感的字符串
    // 4.返回的是一个dom节点对象
    var ts = document.querySelector('div');
    // 5. console.log 打印我们的dom节点对象
    console.log(timer);
</script>
```

##### 9.2 页面元素添加点击事件🎈

```javascript
//鼠标单击
// dom节点
node.onclick = function()  {
    //元素被点击时要执行的操作
}
//鼠标双击
node.ondblclick = function()  {
    //元素被双击击时要执行的操作
}
//鼠标移入
node.onmouseenter = function() {
    //元素被鼠标移入时要执行的操作
}
.....
```

##### 9.3 修改页面样式🎈

###### 9.3.1 方式一: node.style.xx 的✨

``` html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
        <style>
            div {
                width: 200px;
                height: 200px;
                background-color: violet;
                position: relative;
            }
        </style>
    </head>
    <body>
        <div>测试div</div>
        <button>点我试试</button>
        <script>
            document.querySelector("button").onclick = function () {
                document.querySelector("div").style.backgroundColor = "red";
                document.querySelector("div").style.left = "100px";
            };
        </script>
    </body>
</html>
```

###### 9.3.2 方式二:node.classList.add('类名')✨

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
        <style>
            div {
                width: 200px;
                height: 200px;
                background-color: violet;
                position: relative;
            }
            .ts {
                background-color: red;
                left: 100px;
            }
        </style>
    </head>
    <body>
        <div>测试div</div>
        <button>点我试试</button>
        <script>
            document.querySelector("button").onclick = function () {
                document.querySelector("div").classList.add("ts");
            };
        </script>
    </body>
</html>
```

