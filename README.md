# 🍜 即时零售系统 | ScanToOrder

## ✨ 项目简介

本项目基于前后端分离架构开发，后端采用模块化设计，涵盖门店服务、菜品服务、订单服务、支付服务、配送服务、会员营销服务、消息通知服务等核心模块，支持高并发在线下单与订单状态实时同步。
前端适配顾客点餐端（H5/小程序/APP）、商家管理端、后厨出餐端多端展示，核心实现菜品分类与规格管理、购物车与订单状态机、动态计价引擎、配送范围校验、会员积分与优惠券体系
、权限与数据隔离等能力。系统代码结构清晰、接口规范，支持 JAR 私有库依赖管理，可配合 NDA 协议进行源码交付，便于客户团队后续维护、扩展与自主上线部署。

- 📱 **顾客端**：商城下单、会员中心、订单追踪
- 💼 **商家管理端**：订单管理、菜品管理、数据统计
- ⚙️ **后端服务**：RESTful API、WebSocket 实时通知

### 🛒 下单功能
- ✅ 扫码进入商品页面
- ✅ 菜品分类浏览与搜索
- ✅ 购物车管理
- ✅ 多规格菜品选择
- ✅ 特殊要求备注

### 💳 支付功能
- ✅ 微信支付（H5/Native）
- ✅ 支付宝支付
- ✅ 聚合支付（嘉联）
- ✅ 支付方式后台可控
- ✅ 自动识别扫码环境（微信环境只显示微信支付）

### 👤 会员系统
- ✅ 手机号登录（短信验证码）
- ✅ 会员卡购买
- ✅ 优惠券系统
- ✅ 积分体系

### 📊 商家管理
- ✅ 实时订单通知（WebSocket）
- ✅ 订单状态管理（待处理/制作中/已完成）
- ✅ 菜品分类管理
- ✅ 桌台二维码生成
- ✅ 营业数据统计
- ✅ 店铺信息配置

## 🛠️ 技术栈

| 层级 | 技术                                    |
|:---|:--------------------------------------|
| **后端框架** | Spring Boot + MyBatis Plus            |
| **JDK** | Java 8+                               |
| **数据库** | MySQL 5.7+                            |
| **缓存** | Redis                                 |
| **消息队列** | RabbitMQ                              |
| **实时通信** | Netty WebSocket                       |
| **地图服务** | 高德地图                                  |
| **支付** | 微信支付 + 支付宝支付                          |
| **管理后台** | Vue 2.x + Element UI + ECharts        |
| **构建工具** | Maven 3.8+ / Vue CLI 5（webpack 5）     |

#### 4️⃣ 启动系统
- 通过git下载源码
- idea、eclipse需安装lombok插件，不然会提示找不到entity的get set方法
- 创建数据库fast_build，数据库编码为UTF-8
- 执行db/mysql.sql文件，初始化数据
- 修改application-dev.yml，更新MySQL账号和密码
- Eclipse、IDEA运行fastApplication.java，则可启动项目
- Swagger文档路径：http://localhost:8003/fast_build/swagger/index.html
- Swagger注解路径：http://localhost:8003/fast_build/swagger-ui.html


## 📁 部署包结构
```
fb-diandan-server
├── src/main/java/com/fast
│ ├── common # 公共模块（注解、切面、异常、工具类、XSS过滤）
│ ├── config # 全局配置（Shiro、Redis、MyBatis、Swagger、CORS等）
│ ├── datasource # 多数据源支持（动态数据源切换）
│ ├── modules # 业务模块
│ │ ├── app # APP端用户接口（登录、注册、Token认证）
│ │ ├── sys # 系统管理（用户、角色、菜单、字典、日志）
│ │ ├── order # 点餐订单核心业务
│ │ ├── goods # 商品/菜品管理
│ │ ├── pay # 支付模块（微信支付、支付宝、回调处理）
│ │ ├── member # 会员管理
│ │ ├── address # 收货地址管理
│ │ ├── shopSeat # 店铺座位管理
│ │ ├── banner # 轮播图管理
│ │ ├── coupon # 优惠券管理
│ │ ├── integral # 积分管理
│ │ ├── invite # 邀请奖励
│ │ ├── message # 消息推送
│ │ ├── datacentre # 数据统计中心
│ │ ├── oss # 文件存储（阿里云OSS）
│ │ ├── file # 文件上传
│ │ ├── common # 业务公共模块
│ │ └── utils # 业务工具类
│ └── FastApplication.java # 启动类
├── src/main/resources
│ ├── mapper # MyBatis XML映射文件
│ ├── static/swagger # Swagger静态资源
│ ├── weixin # 微信支付证书
│ ├── application.yml # 主配置文件
│ └── application-prod.yml # 生产环境配置
├── db # 数据库脚本
│ └── diandan.sql # 数据库初始化SQL
```

## 💬 联系我们
- 📞 电话：15596655525
- 💬 微信：15596655525（同号）

> ⚠️ 开源版仅用于学习交流，商用请购买商业版授权。


## ⭐ 支持项目

如果这个项目对你有帮助，请给一个 **Star** ⭐ 支持一下！

---

<div align="center">

**在线点餐系统** © 2024-2025

让餐饮服务更智能 🍜

</div>

