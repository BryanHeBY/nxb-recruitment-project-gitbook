# Python与Flask环境搭建

## Python环境

关于Python环境的搭建，可以参考以下文档

{% file src="../.gitbook/assets/SCIP2020-lab00-python环境搭建.pdf" %}
python环境搭建
{% endfile %}

这里建议从JetBrains官网下载pycharm专业版

{% embed url="https://www.jetbrains.com/zh-cn/pycharm" %}
下载pycharm
{% endembed %}

专业版会有30天试用期，长期使用需要在使用JetBrains教育用户许可证，通过[该网址](https://www.jetbrains.com/zh-cn/community/education/#students)进行注册。由于某些原因，南大学生只能使用学信网官方认证文档申请。

![](<../.gitbook/assets/image (18).png>)

并根据[该页面](https://www.chsi.com.cn/xlcx/rhsq.jsp)申请学信网在线验证报告。

安装成功后，建议安装中文插件，具体可参照[该页面](https://blog.csdn.net/weixin\_47244001/article/details/120796712)

## Flask环境搭建

### 安装Flask

我们使用flask的Flask-SQLAlchemy扩展来操作mySQL数据库。它使得你可以在flask中轻松地使用SQLAlchemy工具，你可以使用python语句来操作数据库而无需关心底层实现或编写基础的SQL语句（事实上，在后端开发中使用原始sql语句是应当被避免的）。这可能涉及到以下几个python库： &#x20;

* PyMySQL
* Flask-SQLAlchemy
* SQLAlchemy

请结合你的运行环境，使用pip安装（cmd/powershell , shell）：

```bash
pip install PyMySQL Flask-SQLAlchemy SQLAlchemy -i https://pypi.tuna.tsinghua.edu.cn/simple
```

若需要永久切换pip的镜像源，请[STFW](../za-xiang/chang-jian-wen-ti-faq.md#shen-me-shi-stfw)

{% hint style="info" %}
使用pip安装只对全局python解释器有效。

你也可以通过File>>Settings>>Project>>Python Interperter中install不同的python库。这个方法对虚拟环境python解释器也适用。

&#x20;![](<../.gitbook/assets/image (2).png>)

如果你不满于每次缺少外部库都需要手动添加，这里推荐Anaconda来更好的进行环境管理，在本次实验中并不强求，有需要可以参考[这里](https://www.jianshu.com/p/f5f07ac800d8)。
{% endhint %}

### 在PyCharm中新建Flask项目

如果你使用的是pycharm专业版，可以参照如下页面新建一个Flask项目

{% embed url="https://blog.csdn.net/weixin_44291381/article/details/115523290" %}

这里只需要了解如何新建项目即可，其他内容可以一览flask的风采
