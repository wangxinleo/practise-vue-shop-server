#vueShop_Server

### 介绍

learnVue_shop 配套的服务器 API 项目

**项目所有配置代码已做详细注释，请放心食用。**

> 在食用本项目前，推荐先学习 node.js 和 express 框架，这两个东西很简单，一个下午随便找些文档和视频看就可以入门。**切勿急功近利**

<br/>

**前端 web 项目索引：[2019 黑马前端 element 课程学习的代码项目。 附全套学习资源和 vscode 配置](https://github.com/wangxinleo/learnVue_shop.git)**

<br/>

黑马前端官方课程地址：
前端项目地址：[http://shop.liulongbin.top/](http://shop.liulongbin.top/)
后端接口地址：[https://www.liulongbin.top:8888/api/private/v1/](https://www.liulongbin.top:8888/api/private/v1/)

<br/>
API 接口文档：已部署至本项目根节点
<br/>

全套课程下载：链接：[https://pan.baidu.com/s/1\_-Ve1ceCsvPuXDtieeyVEA](https://pan.baidu.com/s/1_-Ve1ceCsvPuXDtieeyVEA) ，提取码是 q8ln

<br/>

\_注：本后端服务器已设置必须带有 token 才能正常发送和接收请求。请注意请求头参数

### 鸣谢

b 站用户 : [洛天依保护协会](https://space.bilibili.com/132108522?spm_id_from=333.788.b_636f6d6d656e74.26)提供的公用后台 API 接口
<br/>
用户名 : admin 密码 : 123456
<br/>
[洛天依保护协会](https://space.bilibili.com/132108522?spm_id_from=333.788.b_636f6d6d656e74.26)的项目示例地址 : [http://gl.timemeetyou.com](http://gl.timemeetyou.com)
<br/>
**万一接口失效了或者用户被删了可以私聊其恢复数据库**

### 安装

```
# 克隆项目
git clone https://github.com/wangxinleo/vueShop_Server.git

# 进入项目目录
cd vueShop_Server

# 安装依赖
npm install

# 本地开发 启动项目
node ./app.js
```

### 目录结构说明

- `config` 配置文件目录
  - `default.json` 默认配置文件（其中包含数据库配置，jwt 配置）
- `dao` 数据访问层，存放对数据库的增删改查操作
  - `DAO.js` 提供的公共访问数据库的方法
- `models` 存放具体数据库 ORM 模型文件
- `modules` 当前项目模块
  - `authorization.js` API 权限验证模块
  - `database.js` 数据库模块（数据库加载基于 nodejs-orm2 库加载）
  - `passport.js` 基于 passport 模块的登录搭建
  - `resextra.js` API 统一返回结果接口
- `node_modules` 项目依赖的第三方模块
- `routes` 统一路由
  - `api` 提供 api 接口
  - `mapp` 提供移动 APP 界面
  - `mweb` 提供移动 web 站点
- `services` 服务层，业务逻辑代码在这一层编写，通过不同的接口获取的数据转换成统一的前端所需要的数据
- `app.js` 主项目入口文件
- `package.json` 项目配置文件

#### 项目环境

##### 本地环境

​ Node.js + Express + MySQL

##### 创建数据库

​ 数据库文件在：db -> mysdb.sql

​ 创建数据库 mydb，可通过新建查询执行 mysdb.sql 下的 SQL 语句建立数据库，数据库表

​ 数据库连接名：root 密码： 123456

​ 可在 config -> default.json 修改
