# JavaScript

#### 简介

* 有了HTML和CSS，你就能做出来一个好看的静态网页了。但如果想写出能在浏览器或者客户端运行的代码，你还需要一种新语言JavaScript
*   JavaScript的基本结构的语法跟C或者python是有几分相似的

    ```js
    let counter = 0;
    ```

    ```js
    counter = counter + 1;
    counter += 1;
    counter++;
    ```

    ```js
    if (x < y)
    {

    }
    ```

    ```js
    if (x < y)
    {

    }
    else
    {

    }
    ```

    ```js
    if (x < y)
    {

    }
    else if (x > y)
    {

    }
    else
    {

    }
    ```

    ```js
    while (true)
    {

    }
    ```

    ```js
    for (let i = 0; i < 3; i++)
    {

    }
    ```
* 用JavaScript我们可以在浏览器中实时改变HTML的内容。可以用`<script>`标签直接包含代码，或者通过一个`.js`文件
*   下面我们来看一个例子：

    ```html
    <!DOCTYPE html>

    <html lang="en">
        <head>
            <script>

                function greet()
                {
                    alert('hello, body');
                }

            </script>
            <title>hello</title>
        </head>
        <body>
            <form onsubmit="greet();">
                <input id="name" type="text">
                <input type="submit">
            </form>
        </body>
    </html>
    ```

    这里我们有一个`onsubmit`属性，它会调用我们在JS中定义的函数。现在如果打开这个页面并点击submit，就可以看到浏览器显示`hello, body`
* JavaScript还有更多广泛的用法。比如监听事件（鼠标点击、鼠标悬停等等）[`EventTarget.addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)从而做出某些反应，或者通过ID或者名字获取DOM元素（HTML结构中的标签等等） [`document.querySelector`](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) or [`document.querySelectorAll`](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll)然后对其做相应的事
*   在JavaScript中也会经常用到匿名函数：

    ```js
    <script>

        document.addEventListener('DOMContentLoaded', function() {
            document.querySelector('form').addEventListener('submit', function() {
                let name = document.querySelector('#name').value;
                alert('hello, ' + name);
            });
        });

    </script>
    ```

    我们可以用`function()`语法来传入一个匿名函数

#### 学习建议

* 以上只是一个简单的介绍，你可以到[w3school](https://www.w3school.com.cn/js/index.asp)上学你认为需要用到的js用法。[这里](https://www.w3schools.com/js/)也有个英文版的Tutorial
* 对于JavaScript，你需要重点学习如何监听事件，如何获取DOM元素，从而实现动态的页面。
