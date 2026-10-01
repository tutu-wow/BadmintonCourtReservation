# BadmintonCourtReservation
羽毛球预约小程序 亮点：Websocket智能沟通、Echarts数据分析、会员闭环管理、灵活运营规则、全流程预约； 角色：用户、工作人员、管理员；

所有源码均本人开发，项目是前后端分离的，所有的项目都具备了完整的业务逻辑，不仅仅局限于基础的增删改查（CRUD）操作，系统亮点众多。

本文注重于计算机毕业设计选题指导，列出题目均有源码， 大家可以去【公众号】(毕业终点站)获取或者加我【qq】(2112698948)提意见(别忘记Star哟)。备注：git

声明：仅用于学习使用，请勿用于任何商业行为！

1.系统非商用，非开源，非无偿。

2.由本人开发，如需源码，请联系以下方式，qq:2112698948。

3.项目有很多，并未全部上传，如果未找到想要的，可直接咨询。

# 羽毛球预约小程序

> 基于 uni-app 小程序 + Vue 3 管理后台 + Spring Boot 3 服务端的羽毛球馆预约管理系统，覆盖场馆查询、可视化选时段、在线下单、会员卡消费到经营数据分析的完整链路。

**系统亮点**：Websocket智能沟通 · Echarts数据分析 · 会员完整链路管理 · 灵活运营规则 · 全流程预约


## 一、项目简介

羽毛球预约小程序面向球馆的日常经营场景，用微信小程序解决「找场地—选时段—下单—到店—评价」这一串事。场馆、场地、日期、时段全部做成可视化选择，用户下单时系统会自动标出已被占用的时段，避免重复预约；球馆一侧可以配置最短预约时长、最远可预约天数和取消截止时间，并对频繁取消做限制，让场地资源用得更公平。

平台划分普通用户、工作人员、管理员三类角色，各管一摊：用户负责浏览场馆、下单预约、会员卡消费与评价；工作人员负责会员开户充值、订单处理和客户沟通；管理员负责场馆场地、价格规则与平台数据。


## 二、技术架构

| 类别 | 说明 |
| :--- | :--- |
| 架构 | B/S、MVC、前后端分离、微信小程序端+管理后台、管理员+工作人员+普通用户多角色权限管理 |
| 系统环境 | Windows |
| 开发环境 | IDEA、JDK17、Maven、MySQL、Node.js、微信开发者工具 |
| 后端技术 | Java、Spring Boot 3.3、Spring MVC、MyBatis-Plus、MySQL、JWT、WebSocket、微信小程序授权登录 |
| 后台技术 | Vue 3、Vite 5、Element Plus、Vue Router、Pinia、Axios、ECharts |
| 小程序技术 | uni-app、Vue 3、Pinia、微信小程序 API、腾讯地图定位 |

系统采用 B/S 架构与 MVC 分层，前后端分离；小程序端加管理后台双端并行，通过管理员、工作人员、普通用户三类角色做权限划分。


## 三、功能亮点

- 全流程预约：支持场馆、场地、日期、时段的可视化选择，自动标记已占用时段，减少重复预约。
- 灵活运营规则：可配置最短预约时长、最远可预约天数及取消截止时间，并限制高频取消，保障场地资源公平使用。
- 会员完整链路管理：集成会员卡余额支付、充值与消费记录，订单取消可按规则处理退款。
- Echarts数据分析：提供订单量、营业额、会员数、场地利用率、充值趋势等统计，同时为用户展示个人预约偏好和消费数据。
- Websocket智能沟通：内置在线客服与员工沟通，支持文字、图片及语音输入；结合语音识别提升咨询效率。


## 四、界面展示

以下截图均存放于仓库 `images/` 目录，不依赖外部图床。


### 4.1 系统总览

<p align="center"><img src="images/01-system-overview.png" width="78%" alt="系统总览"></p>

**图 01 · 系统总览**：系统整体功能与模块全景。


### 4.2 用户端（小程序）

面向普通球友，完成「浏览场馆 → 选择场地时段 → 下单预约 → 查看订单 → 会员卡消费 → 评价场地」的整个流程。

<p align="center"><img src="images/02-home.png" width="78%" alt="首页"></p>

**图 02 · 首页**：首页聚合场馆推荐、快捷预约入口与资讯位。

<p align="center"><img src="images/03-venues.png" width="78%" alt="场馆"></p>

**图 03 · 场馆**：场馆列表结合定位展示可预约场馆，进入后查看场地与时段。

<p align="center"><img src="images/04-my-orders.png" width="78%" alt="我的订单"></p>

**图 04 · 我的订单**：我的订单跟踪预约状态，支持按规则取消订单。

<p align="center"><img src="images/05-member-card.png" width="78%" alt="会员卡"></p>

**图 05 · 会员卡**：会员卡余额、充值与消费明细一览。

<p align="center"><img src="images/06-customer-service.png" width="78%" alt="客服"></p>

**图 06 · 客服**：在线客服会话，支持文字、图片与语音输入。

<p align="center"><img src="images/07-profile.png" width="78%" alt="个人中心"></p>

**图 07 · 个人中心**：个人中心维护资料、查看我的预约与账户信息。


### 4.3 工作人员端

面向场馆一线人员，处理会员开户充值、订单跟进与客户沟通，并通过数据看板了解当日经营情况。

<p align="center"><img src="images/08-staff-dashboard.png" width="78%" alt="数据分析"></p>

**图 08 · 数据分析**：工作人员视角的数据看板，汇总订单量、营业额与场地利用率。

<p align="center"><img src="images/09-member-recharge.png" width="78%" alt="会员开户及充值"></p>

**图 09 · 会员开户及充值**：为会员办理开户、充值与余额调整。

<p align="center"><img src="images/10-order-manage.png" width="78%" alt="订单管理"></p>

**图 10 · 订单管理**：预约订单查询与到店、取消等状态处理。

<p align="center"><img src="images/11-member-consumption.png" width="78%" alt="会员消费查询"></p>

**图 11 · 会员消费查询**：会员消费明细查询与统计。

<p align="center"><img src="images/12-staff-chat.png" width="78%" alt="客户聊天"></p>

**图 12 · 客户聊天**：工作人员与用户的实时沟通窗口。


### 4.4 管理员端

面向场馆管理者，负责场馆场地、价格规则、订单评价、会员卡与资讯内容的统一维护，并掌握平台整体数据。

<p align="center"><img src="images/13-venue-list.png" width="78%" alt="场馆列表"></p>

**图 13 · 场馆列表**：场馆基础信息维护。

<p align="center"><img src="images/14-court-manage.png" width="78%" alt="场地管理"></p>

**图 14 · 场地管理**：场地与场地类型的配置管理。

<p align="center"><img src="images/15-price-config.png" width="78%" alt="价格配置"></p>

**图 15 · 价格配置**：分时段价格与预约规则配置。

<p align="center"><img src="images/16-booking-orders.png" width="78%" alt="预约订单"></p>

**图 16 · 预约订单**：全平台预约订单统一管理。

<p align="center"><img src="images/17-court-reviews.png" width="78%" alt="场地评价"></p>

**图 17 · 场地评价**：用户对场地的评价内容及回复管理。

<p align="center"><img src="images/18-member-card-manage.png" width="78%" alt="会员卡"></p>

**图 18 · 会员卡**：会员卡类型与权益配置。

<p align="center"><img src="images/19-news-articles.png" width="78%" alt="资讯文章"></p>

**图 19 · 资讯文章**：场馆资讯与公告文章的发布维护。

<p align="center"><img src="images/20-admin-dashboard.png" width="78%" alt="数据分析"></p>

**图 20 · 数据分析**：管理员视角的平台整体经营数据看板。


## 五、说明

- 本文所展示的系统界面与数据均为演示环境下的测试内容，仅用于说明系统功能与设计思路。
- **本项目仅用于学习交流，非商用、非开源、非无偿。**
- 文档展示 20 张截图，需要了解更多，请联系我。
