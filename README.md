# AAA_HTML
 前端学习，记录每一个标签，记录每一个属性

# 标签学习

## 文本标签

```html
<p>段落标签，用于显示一段内容。</p>
<b>粗体</b>
<big>大号字</big>
<em>着重字</em>
<i>斜体</i>
<small>小号字</small>
<strong>加重语气</strong>
<sub>定义下标字</sub>
<sup>定义上标字</sup>
<ins>定义插入字</ins>
<del>定义删除字</del>
<font>字体标签，用户设置字体大小，类型，颜色。</font>
<hn>标题标签，n越小，字体越大<hn>
```

## 图片标签

```html
<img title="鼠标移上图片的提示文字" src="图片位置" />图片标签，单标签。
```

## 超链接标签

```html
<a href="跳转的网址 或 跳转的锚点位置 或 指定网址的锚点位置">用于被点击的文字或其他内容。</a>
<a name="top mid bottom"></a>设置锚点，后续可以再用超链接来跳转过来。
```

## 列表

### 有序列表ol：order list

```html
类型有默认的数字类型1，有英文类型A或a，有罗马计数类型I或i
<ol type="1">
    <li>list item列表项</li>
</ol>
```

### 无序列表ul：unorder list

```html
类型有默认的disc黑点，circle空心黑点，square方框黑点，还有none无黑点。
<ul type="disc">
	<li>list item列表项</li>
</ul>
```

## 表格

```html
由table标签定义表格
caption表格标题
thead与tbody构成了上下部，配合tr/td架构表格，必须配合tr/td，否则会结构混乱，内容跑到表格头上
tr设置行，必须配合td，否则会结构混乱，内容跑到表格头上
td单元格默认字体，靠左
th单元格黑色粗体，剧中，性值是td


<table border='1' bgcolor='red #000 rgb(255,255,255)' cellspacing='0' cellpadding='0'>
		    <caption>表格标题</caption>
		    <thead>
		    	<tr>
		        	<td rowspan='2'>
		            	头部
		            </td>
					<td>nr </td>
		        </tr>
				<tr>
					<td>单元格</td>
					
				</tr>
		    </thead>
		    <tbody>
		        <tr>
		            <td colspan="2">
		            	身体
		            </td>
		        </tr>
				<tr>
					<td>1</td>
					<td>2</td>
				</tr>
				
		    </tbody>
		    <tr>
		    	<td>
		        	其他内容
		        </td>
		    </tr>
		</table>
```

### 属性特效

```html
table标签的style属性加了text-align:center;  就会表格里所有文字居中。
option标签的style属性加了text-align:center; 就会标题内容剧中。
设置td列所占的百分比：不管在哪里，只会使最大的td的width有效，不论是百分比还是固定值，所以一列的宽度受最大的td的width值影响thead/tbody不会分割。
rowspan占多行
colspan占多列
```

### 输入框

```html
<input type="text" value="显示内容" placeholder="提示内容"/>
<textarea cols="200" rows="10" readonly>输入框,一行200个字符，高度显示10行内容，多余的出现滚动条</textarea>
```

### 选择框

```html
下拉选择框
selected是确定当前选中项
<select>
    <option>郑州</option>
    <option selected>南阳</option>
    <option>洛阳</option>
</select>
```

### 表单

```html
form设置action为#表示当前页面，或者网址路径，或本地路径
<form method="get/post" action="#">
	账号：<input type="text" value="内容" maxlength="5"  /><br />
	密码：<input type="pasword" value="密码内容"/><br />
	隐藏字段：<input type="hidden" value="" /><br />
	邮箱：<input type="email" value="" /><br />
	只读<input type="text" value="123" readonly  /><br />
	submit时不能为空<input type="text" value="" required /><br />
	input宽度限字符为11：<input type="text" value="" size="10" /><br />
	爱好： 
	男孩<input type="radio" name="sex" value="boy"  checked/>
	女孩<input type="radio" name="sex" value="girl" />
	<br />
	兴趣：
	听音乐<input type="checkbox" name="hobby" value="music" checked />
	读书<input type="checkbox" name="hobby" value="read"  />
	喝<input type="checkbox" name="hobby" value="drink" />
	<br />
	文件：
	<input type="file" value="文件" accept="image/x-png" /><br />
	功能：
	<input type="submit" value="提交" />
	<input type="reset"  value="重置" />
</form>
```

# 样式学习

层叠*样式表*（英文全称：Cascading Style Sheets）

## 样式选择器种类

### 类选择器：

```html
.自定义名{ key:value;key:value;}
<p class='自定义名'></p>
```

### id选择器

```html
#自定义名{ key:value;key:value;}
<p id='自定义名'></p>
```

### 标签选择器

```html
标签{ key:value;key:value;}
这样就能直接使标签获得效果
```

### 组合选择器

```html
.name1,#name2,p,a{ key:value;key:value;}
```



### 子代选择器

```html
.name1 #name2 name3{ key:value;key:value;}
类名为name1的标签下的id名为name2的标签下的标签名为name3的标签设置

.name1 #name2 #name3{ key:value;key:value;}
类名为name1的标签下的id名为name2的标签下的id名为name3的标签设置

.name1>#name2>a{ key:value;key:value;}
子代选择器
```

### 伪类选择器

```html
选择器:动作
.p:hover{...}
#p:hover{...}
p:hover{...}
例子：
a:link {color: #FF0000}		/* 未访问的链接 */
a:visited {color: #00FF00}	/* 已访问的链接 */
a:hover {color: #FF00FF}	/* 鼠标移动到链接上 */
a:active {color: #0000FF}	/* 选定的链接 */
```



## 样式选择器的使用

### 行内样式

```html
在标签中直接添加属性来达到效果
<p style="font-size:20px;">
	文字
</p>
```

### 内部样式

```html
html文件中通过head部分添加样式
<style>
    p{
        background-color: #00FFFF;
    }
</style>
```

### 外部样式

```html
通过在html的head部分添加链接，引入css文件，加载样式
<link rel="stylesheet" type="text/css" href="css/css.css" />
```

# 位置调控

## margin：标签的外部距离

```html
margin:10px; /* 四周都是10px */
margin:10px 15px; /* 上下为10距离，左右为15距离 */
margin：5px 10px 15px; /* 距上5px，左右距离为10px，距下15px */
margin：5 10 15 20;  /* 分别是上右下左，单位px */

元素居中：
宽度不为100%
使用margin：0 auto
```

### padding：标签的内部距离

```html
padding:10px; /* 内部距离四周都是10px */
padding:10px 15px; /* 内部距离上下为10距离，左右为15距离 */
padding：5px 10px 15px; /* 内部距离距上5px，左右距离为10px，距下15px */
padding：5 10 15 20;  /* 内部距离分别是上右下左，单位px */
```

# 边框

border边框

```html
border="1px solid red"
solid单实线
dotted单虚线
```

# 浮动

## 特点

1、元素在水平方向上靠左或靠右。

2、行内元素浮动会变成块状，块状元素浮动会失去独占一行的特征。

3、一旦元素浮动，后续的元素会受到浮动效果的影响。

## 浮动塌陷

如果是在没有设置高度的容器内的元素浮动，导致容器浮动塌陷为0

## 如何消除浮动（浮动塌陷）带来的影响

1、在浮动元素后面添加一个块状标签（div），添加清除浮动的属性

```html
.clear{
	/* 清除浮动:left | right | both */
	clear:left;
}
```

2、在父容器设置overflow属性，溢出属性通过设置，能解决对应问题



```
overflow：超出、溢出；作用：如何去处理超出容器范围的部分
```

```html
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			#d1 {
				border: 1px solid red;
                /* 控制子元素如果超出父容器的范围如何去处理 
				auto: 自动
				hidden:超出部分隐藏
				scroll:总是显示滚动条
				*/
				overflow: auto;
			}

			#d1 a {
				float: left;
			}
		</style>
	</head>
	<body>
		<div id="d1">
			<a href="#">新闻1</a>
			<a href="#">新闻2</a>
			<a href="#">新闻3</a>
			<a href="#">新闻4</a>
			<a href="#">新闻5</a>
			<a href="#">新闻1</a>
			<a href="#">新闻2</a>
			<a href="#">新闻3</a>
			<a href="#">新闻4</a>
			<a href="#">新闻5</a>
			<a href="#">新闻1</a>
			<a href="#">新闻2</a>
			<a href="#">新闻3</a>
			<a href="#">新闻4</a>
			<a href="#">新闻5</a>

		</div>
		<img src="img/11.jpg"/>
		
	</body>
</html>
```

栗子：

```html
<html>
	<head>
		<meta charset="utf-8">
		<title>新乡旅游网</title>
		<style>
			body {
				margin: 0px;
				padding: 0px;
			}

			.container {
				width: 1024px;
				border: 1px solid black;
				margin: 0px auto;
			}

			.center {
				overflow: auto;
				height: 400px;
			}

			/* 在使用浮动时,如果内容超出容器范围会换到下一行 */
			.center .left1 {
				float: left;
				background-color: #FAEBD7;
				width: 20%;
				height: 100%;
				/* border:1px solid blue; */
			}

			.center .center1 {
				float: left;
				background-color: aliceblue;
				width: 60%;
				height: 100%;
			}

			.center .right1 {
				float: left;
				background-color: #FAEBD7;
				width: 20%;
				height: 100%;
			}

			.top {
				background-color: beige;
				height: 100px;
				border: 1px solid black;
			}

			.top img {
				width: 100%;
				height: 50%;
			}

			.bottom {
				background-color: #F5F5DC;
				height: 100px;
			}

			/* 一般使用无序列表：将margin,padding:0 */
			.menu {
				margin: 0px;
				padding: 0px;
				list-style: none;
				/* border: 1px solid red; */
				overflow: auto;
			}

			.menu li {
				float: left
			}

			.menu li a {
				display: block;
				width: 90px;
				height: 50px;
				line-height: 50px;
				text-align: center;
				background-color: cadetblue;
				margin-left:8px;
			}
			
			.menu li a:hover{
				background-color: #F0F8FF;
				color:red;
			}
		</style>
	</head>
	<body>
		<div class="container">
			<div class="top">
				<img src="img/01.jpg" />
				<ul class="menu">
					<li><a href="#">首页1</a></li>
					<li><a href="#">首页2</a></li>
					<li><a href="#">首页3</a></li>
					<li><a href="#">首页4</a></li>
					<li><a href="#">首页5</a></li>
					<li><a href="#">首页6</a></li>
					<li><a href="#">首页7</a></li>
					<li><a href="#">首页8</a></li>
					<li><a href="#">首页9</a></li>
					<li><a href="#">首页10</a></li>
				</ul>
			</div>
			<div class="center">
				<div class="left1">
					左
				</div>
				<div class="center1">
					中
				</div>
				<div class="right1">
					右
				</div>
			</div>
			<div class="bottom">
				下
			</div>
		</div>
	</body>
</html>
```

# 定位

## 绝对定位

```html
绝对定位的元素的位置相对于最近的已定位祖先元素，如果元素没有已定位的祖先元素，那么它的位置相对于最初的包含块body。
position:absolute;
你甚至可以在html页面用1000个div拼出一幅画。

如果需要设定父位置,在父框架内设定位置，那就把父标签的position:relative
```

## 相对定位

```html
在使用相对定位时，无论是否进行移动，元素仍然占据原来的空间。因此，移动元素会导致它覆盖其它框。
position:relative;
相对于原来的位置进行移动，但是还占用原来位置，会导致原来位置是一片空白，其他元素却被覆盖。
left:10px;       ==     right:-10px
top:10px;        ==     bottom:-10px
```



# 伪类选择器的功能

## hover

```html
#name:hover 子代tag/.name{k:v}全影响
tag:hover 子代tag/.name{k:v}全影响
.name:hover 子代tag/.name{k:v}单影响

```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<style type="text/css">
			.top{
				width: 80%;
			}
			.menu,.menu>li>ul{
				background-color: aqua;
				width: 100%;
				margin: 0px;
				padding: 0px;
				list-style: none;
			}
			.menu{
				position: relative;
			}
			.lf{
				display: none;
				position: absolute;
				border: 10px black solid;
				border-left: 10px red solid;
				top: 0px;
				left: 0px;
			}
			.rt{
				position: absolute;
				display: none;
				border: 10px black solid;
				border-right: 10px red solid;
				top: 0px;
				right: 0px;
			}
			.menu>li{
				float: left;
				width: 20%;
				text-align: center;
				background-color: aliceblue;
			}
			.menu>li>ul{
				position: absolute;
				
				display: none;
			}
			.menu>li:hover ul{
				width: 100%;
				position: relative;
				display: block;
			}
			.menu>li:hover ul>li{
				position: relative;
				height: 30px;
			}
			.menu>li:hover ul>li>span{/* 
				position: relative; */
				display: block;
			}
			a:hover span{
				/* position: absolute; */
				display: block;
			}
		</style>
	</head>
	<body>
		<div class="top">
			<ul class="menu">
				<li>金
					<ul>
						<li><a><span class="lf"></span>金1<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>金2<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>金3<span class="rt"></span></a></li>
					</ul>
				</li>
				<li>木
					<ul>
						<li><a><span class="lf"></span>木1<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>木2<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>木3<span class="rt"></span></a></li>
					</ul>
				</li>
				<li>水
					<ul>
						<li><a><span class="lf"></span>水1<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>水2<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>水3<span class="rt"></span></a></li>
					</ul>
				</li>
				<li>火
					<ul>
						<li><a><span class="lf"></span>火1<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>火2<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>火3<span class="rt"></span></a></li>
					</ul>
				</li>
				<li>土
					<ul>
						<li><a><span class="lf"></span>土1<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>土2<span class="rt"></span></a></li>
						<li><a><span class="lf"></span>土3<span class="rt"></span></a></li>
					</ul>
				</li>
			</ul>
		</div>
	</body>
</html>

```

# 脚本学习

javascript

## 构成

1、ECMAScript:语法标准：变量、数据类型、分支语句、循环、数组、对象、函数

2、BOM:浏览器对象模型：js操控浏览器的（一系列对象）

3、DOM:文档对象模型：用来操控HTML/XML文件中的各种文档元素（一系列对象）

## 变量的定义

```javascript
var name;
var age = 18;
变量的命名规则：

1、使用$ 、字母、数字 或者 下划线来命名

2、首字母：只能是字母或者是$或者是下划线

3、不能使用关键字、保留字...

4、区分大小写

命名规则：

	1、驼峰命名法：小驼峰（变量）、大驼峰（模拟类）
```

## 数据类型

- number: 数字（ 整数 、小数 ）
- string:字符串，用引号（单，双）引起来的：字符串
- boolean:布尔类型：true/false
- null: 空引用，空地址，不存在的地址，对象的默认值
- undefined: 未定义；声明了变量没有赋值，默认存的的是：undefined

## 注释

单行注释：//

多行注释: /* 内容  */

## 输出语句

document.write("0.0");

## 运算

+= -= *= /= %=

优先级：* / % > + - 

## 关系运算符

```javascript
> 大于 < 小于  >= <= ==  !=不等
```

​	关系运算返回的: true/false

## 逻辑运算符

当有多个条件需要进行组合的时候就要使用逻辑运算符

- 与：并且 ：&& 解释：当多个条件同时满足时使用，只要有一个false，最终的结果是:false

- 或：|| 解释：只需要满足其一的时候使用，只要有一个true，最终的结果是：true

- 非：! 解释：相反的条件 ;非真即假，非假即真;

  优先级：

  非 > 与 >或

() > 算术运算符 > 关系运算符> 逻辑运算符  > 赋值

## 类型转换

- parseInt("字符串") ：将字符串转换成整型
- parseFloat("字符串")：将字符串转换成浮点型 （小数）
- Number(object) : 将任意类型转换成数字

```javascript
<script>
    var inputmsg = prompt("标题栏", 2);
	console.log("输入的inputmsg类型是："+typeof inputmsg);
    inputmsg = inputmsg * 1;
    console.log("乘以1后inputmsg类型是："+typeof inputmsg);
    if (typeof inputmsg == "string"){
    console.log("string");
    }else if(typeof inputmsg == "number"){
    console.log("number");
    }
    var outmsg = "" + inputmsg;
    console.log("最后类型变为："+typeof outmsg);
</script>
```

```javascript
// 第一题：输入三个数字：三条边，判断能不能构成三角形？
// var Triangle = prompt("请输入三个数字，用空格隔开：");
// var length = Triangle.split(" ");
// if (length[0] * 1 + length[1] * 1 > length[2] && length[0] * 1 + length[2] * 1 > length[1] && length[1]*1 + length[2] * 1 > length[0] * 1){
// 	console.log("是三角形！");
// }else{
// 	console.log("不是三角形！");
// }
//第二题：输入一个三位的数字，倒着输出；比如：256 ； 输出：652
// var numbers = prompt("请输入三位数字：", 654) * 1;
// a = Math.floor(numbers / 100), b = Math.floor(numbers / 10 % 10), c = numbers % 10;
// console.log(''+c+b+a);
//第三题：输入一个三位数字判断是不是水仙花数
// var numbers = prompt("请输入三位数字：", 153) * 1;
// a = Math.floor(numbers / 100), b = Math.floor(numbers / 10 % 10), c = numbers % 10;
// if (Math.pow(a,3)+Math.pow(b,3)+Math.pow(c,3) == numbers){
// 	console.log(numbers+":是水仙花!");
```

## 循环

### while循环

```html
while(表达式){
	dosomething;
}
```

### do...while循环

```html
do{
	dosomething;
}while(表达式);
```

### for循环

```
for (条件初始化;条件表达式;条件迭代){
	dosomething;
}
```

## break与continue

break跳出循环语句。

continue跳过本次循环，开始下次循环。

# 脚本调试

通过开发者工具，我们可以可以进入调试模式，Sources功能区是调试得主要界面。

## 调试流程

选择断点，刷新网页，进入断点。

通过点击跨越F10或者下一步F11进行断点测试。

## 变量监视

调试界面右侧得Watch中，点击加号，输入变量名来监视变量得值。

# js得object数据类型

## 列表

```javascript
var lis = [1,2,3];
console.log(typeof lis);
for(var i in lis){
    console.log(i);
}
```

## 字典

key是string字符串

```javascript
var dic = {"a":"b"};
console.log(typeof dic);
for(var i in dic){
	console.log(i+dic[i]);
}
var dic = {1:2};
console.log(typeof dic);
for(var i in dic){
    console.log(typeof i+typeof dic[i])
    console.log(i*1+dic[i]);
}
```

# 操作框

## prompt输入框

参数一提示文本，参数二默认值（文本）

返回string

## confirm确认框

参数一提示文本

返回确定是true，返回时false

# 超时与定时

### setTimeout超时单次执行

### setInterval定时循环执行

### clearsetTimeout清除

### clearsetInterval清除

# window对象

## window.location

```js
window.location.href="http://跳转的网址";

window.reload();//页面刷新
```

# history对象

使用前提，操作过后退，可用前进；操作过前进，可用后退

### forward前进

#### back后退

### go()

参数1，2，3，就是forward

参数-1，-2，-3，就是back

# 数组

## 定义的方法

```javascript
var arr1 = [];//定义空数组
var arr2 = [1,2,3];//定义并初始化数组
var arr3 = new Array();//定义数组
var arr4 = new Array(100);//定义数组，开辟空间100个元素位置
var arr5 = new Array(1,2,3);//定义数组，初始化内容，没设定空间
arr4[0]=123;//开辟好的空间可以直接写值
```

## 增删改查

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [concat()](http://www.w3school.com.cn/jsref/jsref_concat_array.asp) | 连接两个或更多的数组，并返回结果。                           |
| [join()](http://www.w3school.com.cn/jsref/jsref_join.asp)    | 把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。 |
| [pop()](http://www.w3school.com.cn/jsref/jsref_pop.asp)      | 删除并返回数组的最后一个元素                                 |
| [push()](http://www.w3school.com.cn/jsref/jsref_push.asp)    | 向数组的末尾添加一个或更多元素，并返回新的长度。             |
| [reverse()](http://www.w3school.com.cn/jsref/jsref_reverse.asp) | 颠倒数组中元素的顺序。                                       |
| [shift()](http://www.w3school.com.cn/jsref/jsref_shift.asp)  | 删除并返回数组的第一个元素                                   |
| [slice()](http://www.w3school.com.cn/jsref/jsref_slice_array.asp) | 从某个已有的数组返回选定的元素                               |
| [sort()](http://www.w3school.com.cn/jsref/jsref_sort.asp)    | 对数组的元素进行排序                                         |
| [splice()](http://www.w3school.com.cn/jsref/jsref_splice.asp) | 删除元素，并向数组添加新元素。                               |
| [toSource()](http://www.w3school.com.cn/jsref/jsref_tosource_array.asp) | 返回该对象的源代码。                                         |
| [toString()](http://www.w3school.com.cn/jsref/jsref_toString_array.asp) | 把数组转换为字符串，并返回结果。                             |
| [toLocaleString()](http://www.w3school.com.cn/jsref/jsref_toLocaleString_array.asp) | 把数组转换为本地数组，并返回结果。                           |
| [unshift()](http://www.w3school.com.cn/jsref/jsref_unshift.asp) | 向数组的开头添加一个或更多元素，并返回新的长度。             |
| [valueOf()](http://www.w3school.com.cn/jsref/jsref_valueof_array.asp) | 返回数组对象的原始值                                         |



## 长度

| 属性   | 描述                     |
| ------ | :----------------------- |
| length | 返回number类型的数组长度 |

## slice方法

a是起始位置，0是第一个位置

b是结束位置

区间表达式为  [ a , a+b )

```javascript
var retn = arr.slice(a,b)

案例
var arr = [1,2,3,4,5,6,7,8,9];
var get = arr.slice(1,4);
console.log(get);
console.log(arr);
```

## splice方法

a是起始位置，0是第一个位置

b是删除的数量

“c” , 1 , 2 , 3后续加的值会插入到刚才删除的位置

```
var get = arr.splice(a, b, "c" ,1 ,2, 3);

案例
var arr = [1,2,3,4,5,6,7,8,9];
var get = arr.splice(1,4);
console.log(get);
console.log(arr);
```



## 数组排序详解

自带方法  arr.sort();

sort方法有一个参数，传递一个回调方法，这个方法返回正负值，或者0（什么都不做）。

```javascript
function funcsort(a,b){
    // console.log(a,b,a-b);//获取回调执行流程，参数，返回结果
    return (a-b);//确认过眼神，负数会导致排序从大到小 ，但是返回0 ，啥都不干
}
```

## 代码模拟

```javascript
<script type="text/javascript">
    var arr= [1,5,9,2,10,3];
    function funcsort(a,b){
        // console.log(a,b,a-b);//获取回调执行流程，参数，返回结果
        return (a-b);//确认过眼神，负数会导致排序从大到小 ，但是返回0 ，啥都不干
    }
    // arr.sort(funcsort);

    // console.log(arr);
    /*    通过加回调方法，使得实现数字排序

                    // 15	  15     
                    // 59	  159
                    // 29	  1529
                    // 25    1259
                    // 12	  1259
                    // 9 10  1259 10
                    // 3 10  1259 3 10
                    // 39   12539 10 
                    // 35	  12359 10
                    // 23    12359 10
                */


    //模拟回调
    var ar=[];
    function textsort(回调){
        for(var item in arr){
            ar.push(arr[item]);
            srt(回调); 
        }
        console.log(ar);//排序完毕
    }
    function srt(回调){
        for(var i = ar.length;i>1;i--){
            if(ar.length==1){//防止最初只输入一个值的时候因为undefined导致不可描述的异常
                break;
            }else{
                // console.log(ar[i-1],ar[i-2]);
                if(回调(ar[i-2] , ar[i-1]) > 0){//a-b>=0,前者大后者小，换位
                    // if(ar[i-2] < ar[i-1]){ //前者小与后者==>换位==>数字大的往前走，小于号是小的往前走
                    var a = ar[i-1];
                    ar[i-1] = ar[i-2];
                    ar[i-2] = a;
                }
            }
        } 
    }
    textsort(funcsort);
</script>
```



# foreach遍历

```javascript
for(var index in arr){
	console.log(index, arr[index]);
}
```



# 回调

传入回调方法名，加括号就可以调用。