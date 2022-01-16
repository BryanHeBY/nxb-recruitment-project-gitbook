# CSS

#### 简介

* **层叠样式表**（英语：**C**ascading **S**tyle **S**heets，缩写：**CSS**）是一种用来为结构化文档（如[HTML](https://zh.wikipedia.org/wiki/HTML)文档或[XML](https://zh.wikipedia.org/wiki/XML)应用）添加样式（字体、间距和颜色等）的计算机语言

1.  我们可以在HTML的标签当中直接引用CSS，例如：

    ```html
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <title>css</title>
        </head>
        <body>
            <header style="font-size: large; text-align: center;">
                anything
            </header>
            <main style="font-size: medium; text-align: center;">
                Welcome to my home page!
            </main>
            <p style="font-size: small; text-align: center;">
                ....
            </p>
        </body>
    </html>
    ```

    在标签中，我们可以添加`style`参数，它的值是一系列CSS属性，用分号分隔开
2.  也可以将CSS与HTML分开来。我们可以将其放在`<head>`标签下：

    * 对于每个\*类型(type)\*的标签，这里用了\*\*类型选择器（type selector）\*\*来定义样式

    ```html
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <style>

                header
                {
                    font-size: large;
                    text-align: center;
                }

                main
                {
                    font-size: medium;
                    text-align: center;
                }

                footer
                {
                    font-size: small;
                    text-align: center;
                }

            </style>
            <title>css</title>
        </head>
        <body>
            <header>
                homepage
            </header>
            <main>
                Welcome to my home page!
            </main>
            <p>
                say something.
            </p>
        </body>
    </html>
    ```

    * 也可以用**类选择器(class selector)**：

    ```html
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <style>

                .centered
                {
                    text-align: center;
                }

                .large
                {
                    font-size: large;
                }

                .medium
                {
                    font-size: medium;
                }

                .small
                {
                    font-size: small;
                }

            </style>
            <title>css</title>
        </head>
        <body>
            <header class="centered large">
                homepage
            </header>
            <main class="centered medium">
                Welcome to my home page!
            </main>
            <p class="centered small">
                hello
            </p>
        </body>
    </html>
    ```

    * 也可以用\*\*id选择器(ID selectors)\*\*来为标签定义样式，在HTML中需要在标签后定义一个ID，在CSS中以`#`打头

    ```html
    <html>
    	<head>
    	<style type="text/css">
    		#test1{
    			color:red;
    		}
    		#test2{
    			color:green;
    		}
    	</style>
    	</head>
    	<body>
    		<p id="test1"> 这段文字是红色的</p>
    		<p id="test2"> 这段文字是绿色的</p>
    	</body>
    </html>
    ```
3.  最终我们可以将所有的CSS属性内容写进另一个文件中，并在HTML中用`<link>`标签来链接它：这样我们的CSS文件长这样:

    ```css
    /*styles.css*/
    .centered
    {
    text-align: center;
    }

    .large
    {
    font-size: large;
    }

    .medium
    {
    font-size: medium;
    }

    .small
    {
    font-size: small;
    }
    ```

    我们的HTML文件长这样：

    ```html
    <!--homepage.html-->
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <link href="styles.css" rel="stylesheet">
            <title>css</title>
        </head>
        <body>
            <header class="centered large">
                homepage
            </header>
            <main class="centered medium">
                Welcome to my home page!
            </main>
            <pr class="centered small">
               hello
            </p>
        </body>
    </html>
    ```

#### 学习建议

* 注意我们上面讲了CSS嵌入HTML的方式（3种）和选择器的语法（3种），是混在一起讲的，但是两个知识。
* 上面只是介绍了你应该如何使用CSS，对于CSS具体有哪些属性, 可以定义哪些样式，需要你在使用时去自学。你可以在[w3school](https://www.w3school.com.cn/css/index.asp)里找到各种CSS属性与用法。同样也有英文文档。我们建议可以先简单了解CSS能干什么，具体的怎么干可以在你有需求的时候再去看具体的语法。
* 对于CSS，你主要需要学习**颜色**、**背景**、**框模型**、**文本**、**定位**等内容。具体内容视项目情况而定
