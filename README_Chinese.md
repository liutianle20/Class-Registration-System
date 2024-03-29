## 适用人群
1. 在校学生，小白用户，想学习知识的
2. 有点基础，想要通过项目实操提高自己的开发能力的
3. 找不到完整项目跟着练的
4. 网上项目比较大，会提供资料，太大了，吃不了它
## 可以学习到的技能

1. 学会常用技术栈的使用
2. 独立开发项目
3. 学会前端的开发流程
4. 学会后端的开发流程
5. 学会数据库的设计
6. 学会前后端接口调用方式
7. 学会多模块之间的关联
8. 学会数据的处理
## 系统功能描述
### 功能模块

1. 管理员信息：用户名、密码、性别、年龄、手机号
2. 教师信息：用户名、密码、性别、年龄、职称、所属专业
3. 学生信息：用户名、密码、性别、年龄、学号、总学分、所属学院
4. 学院信息：学院名称、学院介绍、学院学分限制
5. 专业信息：专业名称、系名、所属学院
6. 课程信息：课程名称、介绍、学分、所属专业、上课教师、开班人数、上课时段、上课地点、已选人数
7. 选课信息：课程名称、介绍、学分、所属专业、上课教师、开班人数、上课时段、上课地点、学生姓名、课程状态
8. 登录注册、修改密码、个人信息管理、退出登录
### 系统角色

1. 管理员：管理员可以看到以上所有模块，管理所有模块信息。
2. 教师：教师可以看到学院信息、专业信息，但只能查看；可以查看自己的课程信息；可以查看自己课程的选课信息
3. 学生：学生可以查看学院、专业信息；可以对已有的课程进行选课，可以再选课信息模块对已选的课程进行取消。如果某个课程被删除，那么已选该课程的选课信息状态变成已取消。
## 系统技术栈

1. 后端：Springboot、MyBatis、SpringMVC
2. 前端：html、css、JavaScript、bootstrap、Vue.js
3. 数据库：MySQL 5.7 或者 MySQL 8
4. 前后端：不分离
5. 编辑器：IDEA2021
## 系统实现
### 项目脚手架的准备

### 管理员信息模块开发
#### 数据库设计

#### 用户实体类的设计

#### 登录功能的实现（前端）
```html
<form role="form">
  <hr/>
  <br/>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-tag"></i></span>
    <input type="text" class="form-control" placeholder="用户名"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" placeholder=" 密码"/>
  </div>
  <h5 style="color: white">请选择角色</h5>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-user"></i></span>
    <select class="form-control">
      <option value="" selected="">请选择</option>
      <option value="1">管理员</option>
      <option value="2">教师</option>
      <option value="3">学生</option>
    </select>
  </div>

  <div style="text-align: center">
    <a href="javascript:void(0)" class="btn btn-primary">登录</a>
  </div>
  <hr/>
  <div style="text-align: center">
    <span style="color: white">未注册 ?</span> <a href="register.html" style="color: yellow">点击这里 </a>
  </div>

</form>
```
#### 登录功能的实现（后端）
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminInfoDao">

    
</mapper>
```
#### 个人主页的实现

#### 退出登录的实现

### 教师信息模块开发
#### 数据库设计
#### 实体类的设计
#### 教师注册功能的实现（前端）
```html
<form role="form">
  <hr/>
  <br/>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-tag"></i></span>
    <input type="text" class="form-control" placeholder="用户名"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" placeholder=" 密码"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" placeholder=" 确认密码"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-male"></i></span>
    <div style="margin-left: 20px">
      <input type="radio" name="sex" value="男" title="男" checked>
      <span style="margin: 0 20px 0 5px">男</span>
      <input type="radio" name="sex" value="女" title="女">
      <span style="margin: 0 20px 0 5px">女</span>
    </div>
  </div>
  <h5>请选择角色</h5>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-user"></i></span>
    <select class="form-control">
      <option value="" selected="">请选择</option>
      <option value="2">教师</option>
      <option value="3">学生</option>
    </select>
  </div>
  <div class="form-group">
    <label class="checkbox-inline">
    </label>
    <span class="pull-right">
    </span>
  </div>

  <div style="text-align: center">
    <a href="javascript:void(0)" @click="register" class="btn btn-primary">注册</a>
  </div>
  <hr/>

</form>
```
#### 教师注册功能的实现（后端）

#### 个人主页的实现
```html
<form role="form" style="width: 300px">
  <input type="hidden" id="id" name="id" v-model="entity.id">
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" v-model="entity.password" placeholder="原密码"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" v-model="entity.newPassword" placeholder="新密码"/>
  </div>
  <div class="form-group input-group">
    <span class="input-group-addon"><i class="fa fa-lock"></i></span>
    <input type="password" class="form-control" v-model="entity.new2Password" placeholder="确认密码"/>
  </div>
  <div style="text-align: center">
    <a href="javascript:void(0)" @click="updatePassword()" class="btn btn-primary">提交</a>
  </div>
</form>
```
#### 教师信息管理的实现（前端）

#### 教师信息管理的实现（后端）


### 学生信息模块开发
#### 数据库设计

#### 实体类的设计

#### 学生注册功能的实现（前端）

#### 教师注册功能的实现（后端）

#### 个人主页的实现

#### 教师信息管理的实现（前端）

#### 教师信息管理的实现（后端）
### 学院信息模块开发

### 专业信息模块开发

### 课程信息模块开发

### 选课信息模块开发

### 课表信息模块开发



