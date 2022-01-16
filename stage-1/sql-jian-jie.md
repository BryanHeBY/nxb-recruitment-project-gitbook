# sql简介

SQL 是用于访问和处理数据库的标准的计算机语言，这里附上相关教程。

{% embed url="https://www.runoob.com/sql/sql-tutorial.html" %}

这里建议你掌握CREATE TABLE，SELECT，WHERE，ORDER BY，INSERT，UPDATE，DELETE等关键词含义以及用法。

### 使用python封装库连接现有数据库

使用以下代码，我们创建了一个SQLAlchemy类的实例（代码位于database.py中）

```python
from flask_sqlalchemy import SQLAlchemy

db = SQLAlchemy()
```

接下来，建立config.py用于配置连接远程数据库所需的信息，框架代码默认提供了一个通用测试数据库的信息。除了该通用数据库，我们为每支队伍分配了一个远程测试数据库，连接信息将由指导员提供。你需要在分配的数据库中完成本次项目的测试数据生成、存储和维护。

使用以下代码将config配置载入flask应用中，并将db实例初始化：

```python
app.config.from_object(config)
db.init_app(app)
```

Flask-SQLAlchemy是一个ORM工具，因此适用于关系型数据库，它将python的面向对象思想和sql的底层存储机制结合。简单来说，我们可以在为每张数据表创建一个模型类，用于其创建和管理。这一规则非常直观，模型python类的命名和表名相同，类成员与字段名相对应。models.py中给出了一个最简单的例子：

```python
class students(db.Model):
    name = db.Column(db.String(10))
    ID = db.Column(db.Integer, primary_key=True)
    age = db.Column(db.Integer)
    sex = db.Column(db.Integer)
```

在通用数据库和分配的数据库中，均存在一个符合该结构的表格。因此，db类能够成功创建并实行查询。一个简单的查询如下：

```python
result = models.students.query.all()
```

result被传递给render\_template后可以在模板中以类似列表的方式被使用。按照分配数据库的URI信息正确配置后，前端展示的查询结果将会变化，这标志着你成功连接了测试数据库。

### 数据库的创建

你可以调用`SQLAlchemy.create_all()`方法，结合你的数据结构设计来创建新的数据表。这里有一个优秀的Flask-SQLAlchemy指南可供参考：[Flask SQLAlchemy 中文文档 | Flask 扩展文档汇总 (gitbooks.io)](https://wizardforcel.gitbooks.io/flask-extension-docs/content/flask-sqlalchemy.html)

关于Flask-SQLAlchemy的增删查改，可参考如下页面

{% embed url="http://www.pythondoc.com/flask-sqlalchemy/queries.html" %}
