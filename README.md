*项目正在持续完善，code和详细描述持续补充中*

# 项目简介

## 概述

根据专业及课程设置提问与答疑模块，结合LLM与向量数据库自动回答提问，设置活动报名功能，集成评论、点赞、关注提升社区体验，对提问与回答内容按照相关属性设置热门榜单与排序等功能。

- 前后端分离，后端使用SpringBoot+Nacos+Feign微服务架构开发，结合Redis实现单点登录与分布式session，统一处理异常与返回值，使用Restful接口。
- 使用Redis存放缓存，并使用分布式锁处理热门活动报名时产生的并发相关问题。
- 使用zSet保存热度对内容排序，使用RabbitMQ异步处理相关属性的热度分数添加。
- 使用MySQL数据库存储数据，并使用oss对象存储服务储存图片、视频等文件。
- 对课程文档解析问题与知识点生成知识库，借助LLM与向量数据库，对学生的提问自动结合知识库回答。

## 架构

- #### 总体架构

<img src="imgs\架构图.png"/>

- #### **大模型对话架构**

<img src="imgs\知识库生成.png" style="zoom: 67%;" />

<img src="imgs\推理.png" style="zoom: 80%;" />





## 功能展示

- #### **登录页**

  采用手机验证码方式登录，后端返回token保存在cookies中，登录session信息存储在redis中

  <img src="imgs\login.png" style="zoom:33%;" />

  <img src="imgs\login2.png" style="zoom:37%;" />

  

- #### **首页热榜**

  <img src="imgs\hot.png" style="zoom:38%;" />

- #### **问题提问**

  <img src="imgs\question1.png" style="zoom:33%;" />

  <img src="imgs\question2.png" style="zoom:44%;" />

- #### **问题回答**

  <img src="imgs\ans2.png" style="zoom:45%;" />

- #### **问题详情页**

  <img src="imgs\ques3.png" style="zoom: 40%;" />

- #### **回答详情（点赞、评论）**

<img src="imgs\ans3.png" style="zoom: 50%;" />

- #### **大模型智能回答**

  <img src="imgs\ans4.png" style="zoom:33%;" />

- #### **关键词页**

  <img src="imgs\key1.png" style="zoom:33%;" />

  <img src="C:\Users\Gary\Desktop\新建文件夹\imgs\key2.png" style="zoom:44%;" />

- #### **关键词详情浏览页**

  <img src="imgs\key3.png" style="zoom:33%;" />

- #### **活动报名**

  <img src="imgs\activity.png" style="zoom:38%;" />



## 开发者

郭春晓、刘宝印 东北大学

