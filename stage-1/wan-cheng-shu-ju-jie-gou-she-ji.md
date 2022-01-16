# 完成数据结构设计

## 数据结构设计举例

针对样题匿名提问箱，我们可以设计如下数据表。同时，为了方便管理，后端需要对相关数据交互操作进行封装。

### 用户表

| 列名       | 类型      |
| -------- | ------- |
| 用户id（主键） | int     |
| 用户昵称     | varchar |
| 用户密码     | varchar |

相关接口：

* 用户注册
* 用户登录检查
* 用户信息修改

### 用户接受匿名提问表

| 列名       | 类型      |
| -------- | ------- |
| 提问id（主键） | int     |
| 被提问用户uid | int     |
| 提问内容     | text    |
| 是否被回答    | boolean |
| 回答内容     | text    |

相关接口：

* 向某用户匿名提问
* 删除提问
* 回答提问

## 要求

请根据自己组内的项目要求，建立数据表（可以调用[`SQLAlchemy.create_all()`](https://wizardforcel.gitbooks.io/flask-extension-docs/content/api.html#flask.ext.sqlalchemy.SQLAlchemy.create\_all)方法，也可直接连接数据库使用sql create table语句），之后可以试着插入一些记录，在学习模板引擎后将结果显示出来

