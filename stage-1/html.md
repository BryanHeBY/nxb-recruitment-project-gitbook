# HTML

#### 简介

**超文本标记语言**（英语：**H**yper**T**ext **M**arkup **L**anguage，简称：**HTML**）是一种用于创建网页的标准标记语言。HTML是一种基础技术，常与[CSS](https://zh.wikipedia.org/wiki/CSS)、[JavaScript](https://zh.wikipedia.org/wiki/JavaScript)一起被众多网站用于设计网页、网页应用程序以及移动应用程序的用户界面。网页浏览器可以读取HTML文件，并将其渲染成可视化网页。HTML描述了一个网站的结构语义随着线索的呈现，使之成为一种标记语言而非编程语言。

*   一个简单的页面的HTML可能看起来是这样的

    ```html
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <title>
                hello, title
            </title>
        </head>
        <body>
            hello, body
        </body>
    </html>
    ```
*   HTML 的文件后缀名是.htm 或者.html（如果电脑不显示文件后缀名， 可以百度搜索如何显示文件后缀名）。`<!DOCTYPE html>`代表文档类 型符合HTML5 标准。 观察文件，我们发现html 文件的主体是body 标签中的内容。每个html文件都是这样的:

    ```html
    <html>
    	<head>
    		<title>   </title>
    		...
    	</head> 
    	<body>
    	...
    	</body>
    	...
    </html>
    ```

    网页中包含的具体内容在body 中，浏览器、搜索引擎所需信息在head 中。
* HTML 的每个元素由标签和内容组成，在`<title> hello title</title>`这一元 素中，`<title>`是开始标签，`</title>`是结束标签，`hello title`是内容。
* 注意这里的缩进不是必须的，只是为了代码的可读性

#### HTML的常见标签

接下来讲一些常见的HTML 标签。

* `h1`-`h6`代表标题，`<h1> xx </h1>` 代表一级标题，即字体最大的 标题。
* `p` 代表段落，每个段落自动换行，需要注意的是：段落内部文字忽略连 续空格和换行。
* `<br/>` 是一个单独出现的标签，代表换行。
* `&nbsp;` 是一个特殊字符，当他出现在段落内部，代表空格，连续 的`&nbsp;`不会被当作连续空格忽略。
* `pre`: 在`pre` 标签中，文本中的空格和换行符会被保留。
* `span` 标签可以在行内添加（css 中定义好的）样式，以格式化文本。
* `<hr/> <hr/>` 是一个单独出现的标签，代表一条水平线。
* `<!--注释-->` 注释中的内容不会在浏览器中显示，用来做标记，方便我们读懂自己写的代码。
* `a` 是超链接标签。超链接可以让用户点击来跳转到其他页面，你可以创建两个html，然后互相超链接，链接写在a 的href 属性中，例如：`<a href=”https://www.baidu.com/”>百度一下，你就知道</a>`。
* `img` 标签可以插入图像，你可以复制一个图片“test.jpg”到网页目录下，然后通过`<img src="test.jpg" />`来插入图片。（你需要通过STFW弄清楚什么是绝对路径，什么是相对路径。）
* `div` 代表区域。
* `ul,li`: `ul` 代表无序列表。你可以测试以下代码：`<ul> <li> 1 </li> <li> 2 </li> </ul>`。
* `ol` 代表有序列表，你可以将上一案例中的ul 替换为ol 测试。
*   `table,tr,td`: `table` 代表表格，`tr` 代表一行，`td` 代表一列，例如:

    ```html
    <table> 
    	<tr> 
    		<td> 
    			...
    		</td> 
    		<td> 
    			...
    		</td> 
    		<td> 
    			...
    		</td> 
    	</tr>
    	<tr> 
    		<td> 
    			...
    		</td> 
    		<td> 
    			...
    		</td> 
    		<td> 
    			...
    		</td> 
    	</tr> 
    </table>
    ```

    代表一个两行三列的表格，你可以往td 中加入内容。值得注意的是，table 默认样式是无边框表格。
*   表单`<form>`

    有了上述的这些标签，在了解一些样式相关的知识之后，你就基本可以使用HTML 制作一个图文并茂的网页了。但是，在网页中我们往往还需要收集一些用户的信息，这就需要表单`<form>` 这一标签。`<form>` 标签单独出现并没有任何实际作用，我们需要在form 标签中加入`<input>`、`<select>`、`<textarea>` 这些标签。input 是一个单独出现的标签，但它的属性较为复杂。它的type 属性决定了这个标签是一个怎样的元素。`type= text` 代表这是一个普通的输入框；`type = password` 代表这是一个密码输入框（输入的内容不会明文显示）；`type = submit` 代表这是一个按钮，点击之后即可提交表单内所有标签的内容；type = reset 代表重置，会清空该表单内所有输入框的内容；`type = radio` 代表这是一个单选的按钮（表单内只能选择一项）；`type = checkbox` 代表这是一个多选的按钮（表单内可以选择多项）。`<select>` 标签是一个菜单，你可以测试这些代码：`<select> <option> 1</option> <option> 1 </option> </select>`。`<textarea>` 标签是一个可以输入多行文本的文本框。以上提到的三种标签：input，select 和textarea 都是表单元素。一个表单通常是：`<form action=” 数据处理网页”> 表单元素</form>`，当然，数据处理涉及到后端开发，仅靠html 和css 是无法实现的。

#### 学习建议

* 以上只是给大家简单介绍了一下HTML和一些常用标签，介绍不一定详尽，更多细节以及更多内容需要大家去自学
* HTML并不需要大家掌握所有东西，需要用到什么去学什么是ok的，这里推荐[w3school](https://www.w3school.com.cn/html/html5\_intro.asp)这个网站，你在里面可以看到各种HTML相关内容的介绍。当然如果你更喜欢英文文档的话可以看[这里](https://www.w3schools.com/html/default.asp). 并且请善用搜索引擎。有不会的也可以问指导员。
* HTML你需要重点学习HTML的结构，一些常用的标签、表单等。具体视项目情况而定
