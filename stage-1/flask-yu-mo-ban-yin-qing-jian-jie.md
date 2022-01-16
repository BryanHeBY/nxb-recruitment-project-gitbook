---
description: flask
---

# Flask与模版引擎简介

Flask是一个用Python编写的轻量级web应用框架。

我们从框架代码来分析一下这个“最小”的Flask应用。

```python
from flask import Flask, render_template
import config
from database import db
import models

app = Flask(__name__) 
# 我们创建一个Flask类的实例。第一个参数是应用模块或者包的名称。 __name__ 是一个适用于大多数情况的快捷方式。有了这个参数， Flask 才能知道在哪里可以找到模板和静态文件等东西。
app.config.from_object(config)
# 从config模块中配置我们的Flask应用
db.init_app(app)
# 数据库初始化


@app.route('/') # 我们使用 route() 装饰器来告诉 Flask 触发函数 的 URL
def homepage():  # put application's code here
    result = models.students.query.all()
    # models中的students类封装对数据库的操作，这里调用
    return render_template('homepage.html', list=result) 
    # 模板引擎从模版文件夹templates中呈现给定的模板上下文，其中将result传给list变量，在模板中使用


if __name__ == '__main__':
    app.run() # 运行

```

以下是Flask手册`快速上手`部分

{% embed url="https://dormousehole.readthedocs.io/en/latest/quickstart.html" %}

其中，你需要着重了解“路由”和“渲染模板”部分。

同时，你可能需要自学http请求、json等相关知识

快速入门中的关于Jinja2模板引擎的介绍较少，跟多介绍可以参考Jinja2手册

{% embed url="https://docs.pythontab.com/jinja/jinja2/templates.html" %}

最后，附上CS50入门Flask的课堂内容，你可以看课程笔记，也可以观看视频来学习。链接在[这里](https://cs50.harvard.edu/x/2021/notes/9/)。如果你从未接触过Flask并且学习时间较充足，推荐去看一看

