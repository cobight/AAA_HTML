# AAA_HTML
 前端学习，记录每一个标签，记录每一个属性

# 标签学习

## 文本标签

```html
<p>段落标签，用于显示一段内容。
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

