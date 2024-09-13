# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 11088ssm在线考试系统程序 11088ssm1

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Kp48e9EtU?p=130)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

在线考试系统工作原理图如图4-1所示：

![](/md/blog.013.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。在线考试系统的整体结构设计如图4-2所示。

![](/md/blog.014.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、教师信息实体图如图4-3所示：

![](/md/blog.015.png)

图4-3教师信息实体图

2、学生信息实体图如图4-4所示：

![](/md/blog.016.png)

`       `图4-4学生信息实体图

3、在线答疑信息实体图如图4-5所示：

![](/md/blog.017.png)

`     `图4-5在线答疑信息实体图
#########
4、发布问题信息实体图如图4-6所示：

![](/md/blog.018.png)

`           `图4-6发布问题信息实体图

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表名：token

功能：token表

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint|||`
   `主键
||
|userid|bigint||用户id|||
|username|varchar|100|用户名|||
|tablename|varchar|100|表名|||
|role|varchar|100|角色|||
|token|varchar|200|密码|||
|addtime|timestamp||新增时间||CURRENT\_TIMESTAMP|
|expiratedtime|timestamp||过期时间||CURRENT\_TIMESTAMP|




表名：xuesheng

功能：学生

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||编号|`
   `主键
||
|addtime|timestamp||添加时间||CURRENT\_TIMESTAMP|
|xuehao|varchar|200|学号|||
|mima|varchar|200|密码|||
|xueshengxingming|varchar|200|学生姓名|||
|xingbie	|int||性别|||
|touxiang|varchar|200|头像|||
|shouji|varchar|200|手机|||
|youxiang|varchar|200|邮箱|||




表名： jiaoshi

功能：   教师

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint|||`
   `主键
||
|addtime|timestamp||添加时间||CURRENT\_TIMESTAMP|
|jiaoshigonghao|varchar|200|教师工号|||
|mima|varchar|200|密码|||
|jiaoshixingming|varchar|200|教师姓名|||
|xingbie|varchar|200|性别|||
|zhaopian|varchar|200|照片|||
|zhicheng|varchar|200|职称|||
|lianxidianhua|varchar|200|联系电话|||



表名：fabuwenti

功能：发布问题

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint|||`
   `主键
||
|addtime|timestamp||添加时间||CURRENT\_TIMESTAMP|
|biaoti|varchar|200|标题|||
|leixing|int||类型|||
|tupian|date||图片|||
|wentimiaoshu|varchar|200|问题描述|||
|faburiqi|varchar|200|发布日期|||
|xuehao|varchar|200|学号|||
|xueshengxingming|varchar|200|学生姓名|||
|sfsh|varchar|200|是否审核|||
|shhf|varchar|200|审核回复|||




表名：zaixiandayi

功能：在线答疑

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint|||`
   `主键
||
|addtime|timestamp||添加时间||CURRENT\_TIMESTAMP|
|biaoti|varchar|200|标题|||
|`	`leixing	|int||类型|||
|dayineirong|varchar|200|答疑内容|||
|dayiriqi|date||答疑日期|||
|xuehao|varchar|200|学号|||
|xueshengxingming|varchar|200|学生姓名|||
|jiaoshigonghao|varchar|200|教师工号|||
|jiaoshixingming|varchar|200|教师姓名|||
#########

#########
# 5系统界面实现
## 5.1 登录
管理员输入个人的账号、密码和角色登录系统，这时候系统的数据库就会在进行查找相关的信息，如果我们输入的账号、密码和角色不正确，数据库就会提示出错误的信息提示，同时会提示管理员重新输入自己的账号、密码，直到账号密码输入成功后，会提登录成功的信息。网站管理员登录效果图如图5-1所示：

![](/md/blog.019.png)     
图5-1管理员登录界面

## 5.2  管理员功能模块     
### 5.2.1 学生管理
管理员对学生管理进行编辑填写学号、密码、学生姓名、性别、头像、手机、邮箱并进行详情、删除、修改等操作。程序成效图如下图5-2所示:

![](/md/blog.020.png)

图5-2学生管理界面图
### 5.2.2 教师管理
管理员对教师管理进行编辑教师工号、密码、教师姓名、性别、照片、职称、联系电话等操作并可以进行详情、删除、修改操作。程序效果图如下图5-3所示：

![](/md/blog.021.png)

图5-3教师管理界面
### 5.2.3 在线学习管理
管理员对在线学习管理进行编辑标题、类型、图片、内容简介、学习视频、发布日期等操作并可以进行详情、删除、修改操作。程序效果图如下图5-4所示：

![](/md/blog.022.png) 

图5-4在线学习管理界面

### 5.2.4 轮播图管理
轮播图；该页面为轮播图管理界面。管理员可以在此页面进行首页轮播图的管理，通过新建操作可在轮播图中加入新的图片，还可以对以上传的图片进行修改操作，以及图片的删除操作。程序效果图如下图5-5所示：

![](/md/blog.023.png)

图5-5轮播图管理界面
### 5.2.5发布问题管理
管理员对发布问题管理进行填写标题、类型、图片、问题描述、发布日期、学号、学生姓名、审核回复、审核状态等进行详情、删除、修改操作。程序效果图如下图5-6所示：

![](/md/blog.024.png)

图5-6发布问题管理界面
### 5.2.6在线答疑管理
管理员对在线答疑管理进行编辑标题、类型、答疑内容、答疑日期、学号、学生姓名、教师工号、教师姓名等操作并可以进行详情、删除、修改操作。程序效果图如下图5-7所示：

![](/md/blog.025.png) 

图5-7在线答疑管理界面
### 5.2.7论坛交流
管理员对论坛交流进行编辑帖子标题、用户名、状态等操作并可以进行详情、删除、修改操作。程序效果图如下图5-8所示：

![](/md/blog.026.png) 

图5-8论坛交流界面



## 5.3 前台首页功能模块
前台首页详情页面：首页、在线学习、论坛交流、试卷列表、系统公告、个人中心、后台管理等功能操作。程序效果图如下图5-9所示：

![](/md/blog.027.png)

图5-9前台首页功能界面
## 5.3.1 登录、学生注册
学生在线填写学号、密码、学生姓名、手机、邮箱等信息进行注册、登录操作。程序效果图如下图5-10所示：

![](/md/blog.028.png)

![](/md/blog.029.png)

图5-10登录、学生注册界面
## 5.3.2在线学习
学生进入在线学习可以填写标题、类型、图片、内容简介、学习视频、发布日期、点击次数等信息，并可以进行立即提交操作。程序效果图如下图5-11所示：

![](/md/blog.030.png)


图5-11在线学习界面
## 5.3.3论坛交流
学生进入论坛交流可以填写帖子标题、发布人、用户名进行立即提交操作。程序效果图如下图5-12所示：

![](/md/blog.031.png)

图5-12论坛交流界面

## 5.4 学生功能模块

## 5.4.1个人信息
学生进入个人信息可以查看学号、密码、学生姓名、性别、头像、手机、邮箱等操作。程序效果图如下图5-13所示：

![](/md/blog.032.png)

图5-13个人信息界面
## 5.4.2发布问题管理
学生进入发布问题管理可以填写标题、类型、图片、问题描述、发布日期、学号、学生姓名、审核回复、审核状态并可以进行详情、删除等操作。程序效果图如下图5-14所示：

![](/md/blog.033.png)

图5-14发布问题管理界面
## 5.4.3我的收藏管理
学生进入我的收藏管理可以填写收藏名称、收藏图片等信息，并可以进行详情、删除等操作。程序效果图如下图5-15所示：

![](/md/blog.034.png)

图5-15我的收藏管理界面
## 5.4.4考试记录
学生进入考试记录可以填写用户ID、学号、学生姓名、试卷、考试得分等信息进行详情、删除，操作。程序效果图如下图5-16所示：

![](/md/blog.035.png)

图5-16考试记录界面


## 5.5 教师功能模块
## 5.5.1个人信息
教师进入个人信息可以查看教师工号、密码、教师姓名、性别、照片、职称、联系电话等信息，并可以进行详情、删除等操作。程序效果图如下图5-17所示：

![](/md/blog.036.png)

图5-17个人信息界面

## 5.5.2试卷管理
教师进入试卷管理可以查看试卷名称、考试时长、试卷状态等信息，进行删除、详情等操作。程序效果图如下图5-18所示：

![](/md/blog.037.png)

图5-18试卷管理界面

## 5.5.3试题管理
教师进入试题管理可以查看试卷、试题名称、分值、答案、类型等信息，详情、删除等操作。程序效果图如下图5-19所示：

![](/md/blog.038.png)

图5-19试题管理界面












