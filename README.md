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

