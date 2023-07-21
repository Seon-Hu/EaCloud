# 易云开发平台(EaCloud Framework)

[![Member project of EaCloud Team](https://img.shields.io/badge/member%20project%20of-EaCloud-9e20c9.svg)](https://gitee.com/eacloud)
[![NuGet Badge](https://img.shields.io/nuget/v/eacloud)](https://www.nuget.org/profiles/Seon.Hu)
[![GitHub license](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

---

 - [EaCloud简介](#01)
 - [EaCloud特性](#02)
 - [快速开始](#03)
 - [项目进度](#04)
 - [更新记录](https://gitee.com/eacloud/back-end/releases)
 - [代码生成器VSIX插件](正在构建中...)
 - [EaCloud文档中心](https://eacloud_docs.sanqing.tech/api/)

---

## <a id="01"/>EaCloud简介

易云开发平台(Easy Cloud Framework)简称 EaCloud(EaCloud Framework)，是一个基于.Net 7开发的一个.NetCore快速开发框架。这个框架使用最新稳定版的.NetCore SDK(当前是.NET 7)，对 AspNetCore 的配置、依赖注入、日志、缓存、实体框架、WebApi、身份认证、权限授权等模块进行更高一级的自动化封装，并规范了一套业务实现的代码结构与代码编写操作流程，使的实际应用项目开发和运维更高效、更简单。

后端接口服务项目：
- AspNet版本(.Net 7): [https://gitee.com/eacloud/back-end](https://gitee.com/eacloud/back-end)。

前端中后台项目：
- Vue版本(vben): [https://gitee.com/eacloud/front-end.bg-vben](https://gitee.com/eacloud/front-end.bg-vben)，当前更新版本。
- Angular版本(ng-alain): [https://gitee.com/eacloud/front-end.bg-ng-alain](https://gitee.com/eacloud/front-end.bg-ng-alain)，已停止更新。

前端移动PDA项目：
- Vue版本(uni-app): [https://gitee.com/eacloud/front-end.app-pda](https://gitee.com/eacloud/front-end.app-pda)。

### 框架组件

![image](https://eacloud_docs.sanqing.tech/images/001.sanqing108.png)

* 【EaCloud】核心组件，封装着框架核心及数据存储，缓存，辅助操作等功能。
* 【EaCloud.AspNetCore】AspNetCore 组件，提供 AspNetCore 的服务端功能的封装。
* 【EaCloud.AspNetCore.Diagnostics】AspNetCore 性能诊断组件，提供 AspNetCore 性能诊断功能的封装。
* 【EaCloud.Authorization.Datas】数据权限组件，对应用中数据权限进行授权的设计实现。
* 【EaCloud.Authorization.Functions】功能权限组件，API功能权限的设计实现。
* 【EaCloud.AutoMapper】AutoMapper 对象映射组件，封装基于 AutoMapper 的对象映射功能实现。
* 【EaCloud.Baidu】Baidu 组件，包含百度地图开放平台接口处理功能。
* 【EaCloud.EntityFrameworkCore】数据访问组件，封装 EntityFrameworkCore 数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.Allinone】EaCloud 一体化数据访问组件，封装 Cosmos(Azure Cosmos DB 的 SQL API)、Kdbndp(人大金仓)、MySql、Oracle、PostgreSql、Sqlite、SqlServer 类型数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.Cosmos】Azure Cosmos DB 组件，封装基于 Microsoft.EntityFrameworkCore.Cosmos 的数据访问功能的实现(受限于只能使用SQL类型数据库，不建议使用)。
* 【EaCloud.EntityFrameworkCore.Kdbndp】Kdbndp(人大金仓) 数据库组件，封装基于 Kdbndp.EntityFrameworkCore.KingbaseES 的数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.MySql】MySql 数据库组件，封装基于 Pomelo.EntityFrameworkCore.MySql 的数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.Oracle】Oracle 数据库组件，封装基于 Oracle.EntityFrameworkCore 的数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.PostgreSql】PostgreSql 数据库组件，封装基于 Npgsql.EntityFrameworkCore.PostgreSQL 的数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.Sqlite】Sqlite 数据库组件，封装基于 Microsoft.EntityFrameworkCore.Sqlite 的数据访问功能的实现。
* 【EaCloud.EntityFrameworkCore.SqlServer】SqlServer 数据库组件，封装基于 Microsoft.EntityFrameworkCore.SqlServer 的数据访问功能的实现。
* 【EaCloud.Exceptionless】Exceptionless 分布式日志组件，封装基于 Exceptionless 分布式日志记录实现。
* 【EaCloud.FastReport】FastReport组件，封装 FastReport.OpenSource 的报表处理功能。
* 【EaCloud.File】文件处理组件，封装基于Web的文件资源管理服务，支持数据库、物理存储、数据存储服务三种存储方式，物理存储模式下支持静态资源URL映射。
* 【EaCloud.Hangfire】Hangfire 后台任务组件，封装基于 Hangfire 后台任务的服务端实现。
* 【EaCloud.Identity】身份认证组件，基于 AspNetCore.Identity 和 EaCloud数据仓储模型 的身份认证实现。
* 【EaCloud.Log4Net】Log4Net 日志组件，封装使用 Log4Net 框架实现的日志输出功能。
* 【EaCloud.MiniProfiler】MiniProfiler 性能监测组件，封装基于 MiniProfiler 框架实现的性能监测功能。
* 【EaCloud.NLog】NLog 日志组件，封装使用 Nlog 框架实现的日志输出功能。
* 【EaCloud.Redis】Redis 缓存组件，封装基于 Redis 客户端的缓存实现。
* 【EaCloud.Report】报表组件，封装 FastReport.OpenSource 的报表处理功能。
* 【EaCloud.SMS】短信组件，封装阿里云、逸峰信盈通验证码、通知、推广短信处理功能。目前已完成验证码短信发送、验证的处理机制。
* 【EaCloud.Swagger】Swagger API 文档生成组件，封装基于 Swagger 的 API 接口文档生成及调试功能。
* 【EaCloud.Utils】工具组件，封装着框架常用的工具类。
* 【EaCloud.Workflow】工作流引擎组件，基于BPMN模型，实现办公自动化、文件审批、业务单据、请假报销等场景的流程逻辑。

* 【EaCloud.Pack.Audit】审计模块，包含操作审计和数据审计。
* 【EaCloud.Pack.Authorization】权限模块，包含数据权限和功能权限。
* 【EaCloud.Pack.File】文件处理模块，封装基于 EaCloud 文件处理组件的功能实现。
* 【EaCloud.Pack.Identity】身份认证模块，封装基于 EaCloud 身份认证组件的功能实现。
* 【EaCloud.Pack.IM】即时通讯模块，封装即时消息收发及消息记录管理功能。
* 【EaCloud.Pack.Menu】菜单模块，封装后台动态获取菜单模式下菜单管理功能。
* 【EaCloud.Pack.Message】消息模块，封装公告讯息收发及记录管理功能。
* 【EaCloud.Pack.Report】报表模块，封装基于 EaCloud 报表组件的功能实现。
* 【EaCloud.Pack.SMS】短信模块，封装基于 EaCloud 短信组件的功能实现。
* 【EaCloud.Pack.Workflow】工作流引擎模块，封装基于 EaCloud 工作流引擎组件的功能实现。

* 【EaCloud.Api.Audit】审计模块API，封装基于 EaCloud 审计模块的WebApi实现。
* 【EaCloud.Api.Authorization】权限模块API，封装基于 EaCloud 权限模块的WebApi实现。
* 【EaCloud.Api.Baidu】百度模块API，封装基于 EaCloud 百度模块的WebApi实现。
* 【EaCloud.Api.File】文件模块API，封装基于 EaCloud 文件模块的WebApi实现。
* 【EaCloud.Api.Identity】身份认证模块API，封装基于 EaCloud 身份认证模块的WebApi实现。
* 【EaCloud.Api.IM】即时通讯模块API，封装基于 EaCloud 即时通讯模块的WebApi实现。
* 【EaCloud.Api.Menu】菜单模块API，封装基于 EaCloud 菜单模块的WebApi实现。
* 【EaCloud.Api.Message】消息模块API，封装基于 EaCloud 消息模块的WebApi实现。
* 【EaCloud.Api.Report】报表模块API，封装基于 EaCloud 报表模块模块的WebApi实现。
* 【EaCloud.Api.SMS】短信模块API，封装基于 EaCloud 短信模块的WebApi实现。
* 【EaCloud.Api.System】系统公共API，封装图形验证码、模块信息等公共WebApi实现。


### Nuget Packages
| 包名称                                                         | Nuget稳定版本                                                                                                       | Nuget预览版本                                                                                                          | 下载数                                                                                                               |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [EaCloud](https://www.nuget.org/packages/EaCloud/) | [![EaCloud](https://img.shields.io/nuget/v/eacloud.svg)](https://www.nuget.org/packages/EaCloud/) | [![EaCloud](https://img.shields.io/nuget/vpre/eacloud.svg)](https://www.nuget.org/packages/EaCloud/) | [![EaCloud](https://img.shields.io/nuget/dt/eacloud.svg)](https://www.nuget.org/packages/EaCloud/) |
| [EaCloud.AspNetCore](https://www.nuget.org/packages/EaCloud.AspNetCore/) | [![EaCloud.AspNetCore](https://img.shields.io/nuget/v/EaCloud.AspNetCore.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore/) | [![EaCloud.AspNetCore](https://img.shields.io/nuget/vpre/EaCloud.AspNetCore.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore/) | [![EaCloud.AspNetCore](https://img.shields.io/nuget/dt/EaCloud.AspNetCore.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore/) |
| [EaCloud.AspNetCore.Diagnostics](https://www.nuget.org/packages/EaCloud.AspNetCore.Diagnostics/) | [![EaCloud.AspNetCore.Diagnostics](https://img.shields.io/nuget/v/EaCloud.AspNetCore.Diagnostics.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore.Diagnostics/) | [![EaCloud.AspNetCore.Diagnostics](https://img.shields.io/nuget/vpre/EaCloud.AspNetCore.Diagnostics.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore.Diagnostics/) | [![EaCloud.AspNetCore.Diagnostics](https://img.shields.io/nuget/dt/EaCloud.AspNetCore.Diagnostics.svg)](https://www.nuget.org/packages/EaCloud.AspNetCore.Diagnostics/) |
| [EaCloud.Authorization.Datas](https://www.nuget.org/packages/EaCloud.Authorization.Datas/) | [![EaCloud.Authorization.Datas](https://img.shields.io/nuget/v/EaCloud.Authorization.Datas.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Datas/) | [![EaCloud.Authorization.Datas](https://img.shields.io/nuget/vpre/EaCloud.Authorization.Datas.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Datas/) | [![EaCloud.Authorization.Datas](https://img.shields.io/nuget/dt/EaCloud.Authorization.Datas.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Datas/) |
| [EaCloud.Authorization.Functions](https://www.nuget.org/packages/EaCloud.Authorization.Functions/) | [![EaCloud.Authorization.Functions](https://img.shields.io/nuget/v/EaCloud.Authorization.Functions.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Functions/) | [![EaCloud.Authorization.Functions](https://img.shields.io/nuget/vpre/EaCloud.Authorization.Functions.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Functions/) | [![EaCloud.Authorization.Functions](https://img.shields.io/nuget/dt/EaCloud.Authorization.Functions.svg)](https://www.nuget.org/packages/EaCloud.Authorization.Functions/) |
| [EaCloud.AutoMapper](https://www.nuget.org/packages/EaCloud.AutoMapper/) | [![EaCloud.AutoMapper](https://img.shields.io/nuget/v/EaCloud.AutoMapper.svg)](https://www.nuget.org/packages/EaCloud.AutoMapper/) | [![EaCloud.AutoMapper](https://img.shields.io/nuget/vpre/EaCloud.AutoMapper.svg)](https://www.nuget.org/packages/EaCloud.AutoMapper/) | [![EaCloud.AutoMapper](https://img.shields.io/nuget/dt/EaCloud.AutoMapper.svg)](https://www.nuget.org/packages/EaCloud.AutoMapper/) |
| [EaCloud.Baidu](https://www.nuget.org/packages/EaCloud.Baidu/) | [![EaCloud.Baidu](https://img.shields.io/nuget/v/EaCloud.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Baidu/) | [![EaCloud.Baidu](https://img.shields.io/nuget/vpre/EaCloud.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Baidu/) | [![EaCloud.Baidu](https://img.shields.io/nuget/dt/EaCloud.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Baidu/) |
| [EaCloud.EntityFrameworkCore](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore/) | [![EaCloud.EntityFrameworkCore](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore/) | [![EaCloud.EntityFrameworkCore](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore/) | [![EaCloud.EntityFrameworkCore](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore/) |
| [EaCloud.EntityFrameworkCore.Allinone](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Allinone/) | [![EaCloud.EntityFrameworkCore.Allinone](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.Allinone.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Allinone/) | [![EaCloud.EntityFrameworkCore.Allinone](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.Allinone.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Allinone/) | [![EaCloud.EntityFrameworkCore.Allinone](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.Allinone.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Allinone/) |
| [EaCloud.EntityFrameworkCore.Cosmos](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Cosmos/) | [![EaCloud.EntityFrameworkCore.Cosmos](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.Cosmos.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Cosmos/) | [![EaCloud.EntityFrameworkCore.Cosmos](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.Cosmos.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Cosmos/) | [![EaCloud.EntityFrameworkCore.Cosmos](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.Cosmos.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Cosmos/) |
| [EaCloud.EntityFrameworkCore.Kdbndp](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Kdbndp/) | [![EaCloud.EntityFrameworkCore.Kdbndp](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.Kdbndp.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Kdbndp/) | [![EaCloud.EntityFrameworkCore.Kdbndp](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.Kdbndp.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Kdbndp/) | [![EaCloud.EntityFrameworkCore.Kdbndp](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.Kdbndp.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Kdbndp/) |
| [EaCloud.EntityFrameworkCore.MySql](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.MySql/) | [![EaCloud.EntityFrameworkCore.MySql](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.MySql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.MySql/) | [![EaCloud.EntityFrameworkCore.MySql](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.MySql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.MySql/) | [![EaCloud.EntityFrameworkCore.MySql](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.MySql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.MySql/) |
| [EaCloud.EntityFrameworkCore.Oracle](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Oracle/) | [![EaCloud.EntityFrameworkCore.Oracle](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.Oracle.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Oracle/) | [![EaCloud.EntityFrameworkCore.Oracle](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.Oracle.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Oracle/) | [![EaCloud.EntityFrameworkCore.Oracle](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.Oracle.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Oracle/) |
| [EaCloud.EntityFrameworkCore.PostgreSql](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.PostgreSql/) | [![EaCloud.EntityFrameworkCore.PostgreSql](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.PostgreSql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.PostgreSql/) | [![EaCloud.EntityFrameworkCore.PostgreSql](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.PostgreSql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.PostgreSql/) | [![EaCloud.EntityFrameworkCore.PostgreSql](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.PostgreSql.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.PostgreSql/) |
| [EaCloud.EntityFrameworkCore.Sqlite](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Sqlite/) | [![EaCloud.EntityFrameworkCore.Sqlite](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.Sqlite.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Sqlite/) | [![EaCloud.EntityFrameworkCore.Sqlite](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.Sqlite.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Sqlite/) | [![EaCloud.EntityFrameworkCore.Sqlite](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.Sqlite.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.Sqlite/) |
| [EaCloud.EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.SqlServer/) | [![EaCloud.EntityFrameworkCore.SqlServer](https://img.shields.io/nuget/v/EaCloud.EntityFrameworkCore.SqlServer.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.SqlServer/) | [![EaCloud.EntityFrameworkCore.SqlServer](https://img.shields.io/nuget/vpre/EaCloud.EntityFrameworkCore.SqlServer.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.SqlServer/) | [![EaCloud.EntityFrameworkCore.SqlServer](https://img.shields.io/nuget/dt/EaCloud.EntityFrameworkCore.SqlServer.svg)](https://www.nuget.org/packages/EaCloud.EntityFrameworkCore.SqlServer/) |
| [EaCloud.Exceptionless](https://www.nuget.org/packages/EaCloud.Exceptionless/) | [![EaCloud.Exceptionless](https://img.shields.io/nuget/v/EaCloud.Exceptionless.svg)](https://www.nuget.org/packages/EaCloud.Exceptionless/) | [![EaCloud.Exceptionless](https://img.shields.io/nuget/vpre/EaCloud.Exceptionless.svg)](https://www.nuget.org/packages/EaCloud.Exceptionless/) | [![EaCloud.Exceptionless](https://img.shields.io/nuget/dt/EaCloud.Exceptionless.svg)](https://www.nuget.org/packages/EaCloud.Exceptionless/) |
| [EaCloud.FastReport](https://www.nuget.org/packages/EaCloud.FastReport/) | [![EaCloud.FastReport](https://img.shields.io/nuget/v/EaCloud.FastReport.svg)](https://www.nuget.org/packages/EaCloud.FastReport/) | [![EaCloud.FastReport](https://img.shields.io/nuget/vpre/EaCloud.FastReport.svg)](https://www.nuget.org/packages/EaCloud.FastReport/) | [![EaCloud.FastReport](https://img.shields.io/nuget/dt/EaCloud.FastReport.svg)](https://www.nuget.org/packages/EaCloud.FastReport/) |
| [EaCloud.File](https://www.nuget.org/packages/EaCloud.File/) | [![EaCloud.File](https://img.shields.io/nuget/v/EaCloud.File.svg)](https://www.nuget.org/packages/EaCloud.File/) | [![EaCloud.File](https://img.shields.io/nuget/vpre/EaCloud.File.svg)](https://www.nuget.org/packages/EaCloud.File/) | [![EaCloud.File](https://img.shields.io/nuget/dt/EaCloud.File.svg)](https://www.nuget.org/packages/EaCloud.File/) |
| [EaCloud.Hangfire](https://www.nuget.org/packages/EaCloud.Hangfire/) | [![EaCloud.Hangfire](https://img.shields.io/nuget/v/EaCloud.Hangfire.svg)](https://www.nuget.org/packages/EaCloud.Hangfire/) | [![EaCloud.Hangfire](https://img.shields.io/nuget/vpre/EaCloud.Hangfire.svg)](https://www.nuget.org/packages/EaCloud.Hangfire/) | [![EaCloud.Hangfire](https://img.shields.io/nuget/dt/EaCloud.Hangfire.svg)](https://www.nuget.org/packages/EaCloud.Hangfire/) |
| [EaCloud.Identity](https://www.nuget.org/packages/EaCloud.Identity/) | [![EaCloud.Identity](https://img.shields.io/nuget/v/EaCloud.Identity.svg)](https://www.nuget.org/packages/EaCloud.Identity/) | [![EaCloud.Identity](https://img.shields.io/nuget/vpre/EaCloud.Identity.svg)](https://www.nuget.org/packages/EaCloud.Identity/) | [![EaCloud.Identity](https://img.shields.io/nuget/dt/EaCloud.Identity.svg)](https://www.nuget.org/packages/EaCloud.Identity/) |
| [EaCloud.Log4Net](https://www.nuget.org/packages/EaCloud.Log4Net/) | [![EaCloud.Log4Net](https://img.shields.io/nuget/v/EaCloud.Log4Net.svg)](https://www.nuget.org/packages/EaCloud.Log4Net/) | [![EaCloud.Log4Net](https://img.shields.io/nuget/vpre/EaCloud.Log4Net.svg)](https://www.nuget.org/packages/EaCloud.Log4Net/) | [![EaCloud.Log4Net](https://img.shields.io/nuget/dt/EaCloud.Log4Net.svg)](https://www.nuget.org/packages/EaCloud.Log4Net/) |
| [EaCloud.MiniProfiler](https://www.nuget.org/packages/EaCloud.MiniProfiler/) | [![EaCloud.MiniProfiler](https://img.shields.io/nuget/v/EaCloud.MiniProfiler.svg)](https://www.nuget.org/packages/EaCloud.MiniProfiler/) | [![EaCloud.MiniProfiler](https://img.shields.io/nuget/vpre/EaCloud.MiniProfiler.svg)](https://www.nuget.org/packages/EaCloud.MiniProfiler/) | [![EaCloud.MiniProfiler](https://img.shields.io/nuget/dt/EaCloud.MiniProfiler.svg)](https://www.nuget.org/packages/EaCloud.MiniProfiler/) |
| [EaCloud.NLog](https://www.nuget.org/packages/EaCloud.NLog/) | [![EaCloud.NLog](https://img.shields.io/nuget/v/EaCloud.NLog.svg)](https://www.nuget.org/packages/EaCloud.NLog/) | [![EaCloud.NLog](https://img.shields.io/nuget/vpre/EaCloud.NLog.svg)](https://www.nuget.org/packages/EaCloud.NLog/) | [![EaCloud.NLog](https://img.shields.io/nuget/dt/EaCloud.NLog.svg)](https://www.nuget.org/packages/EaCloud.NLog/) |
| [EaCloud.Redis](https://www.nuget.org/packages/EaCloud.Redis/) | [![EaCloud.Redis](https://img.shields.io/nuget/v/EaCloud.Redis.svg)](https://www.nuget.org/packages/EaCloud.Redis/) | [![EaCloud.Redis](https://img.shields.io/nuget/vpre/EaCloud.Redis.svg)](https://www.nuget.org/packages/EaCloud.Redis/) | [![EaCloud.Redis](https://img.shields.io/nuget/dt/EaCloud.Redis.svg)](https://www.nuget.org/packages/EaCloud.Redis/) |
| [EaCloud.Report](https://www.nuget.org/packages/EaCloud.Report/) | [![EaCloud.Report](https://img.shields.io/nuget/v/EaCloud.Report.svg)](https://www.nuget.org/packages/EaCloud.Report/) | [![EaCloud.Report](https://img.shields.io/nuget/vpre/EaCloud.Report.svg)](https://www.nuget.org/packages/EaCloud.Report/) | [![EaCloud.Report](https://img.shields.io/nuget/dt/EaCloud.Report.svg)](https://www.nuget.org/packages/EaCloud.Report/) |
| [EaCloud.SMS](https://www.nuget.org/packages/EaCloud.SMS/) | [![EaCloud.SMS](https://img.shields.io/nuget/v/EaCloud.SMS.svg)](https://www.nuget.org/packages/EaCloud.SMS/) | [![EaCloud.SMS](https://img.shields.io/nuget/vpre/EaCloud.SMS.svg)](https://www.nuget.org/packages/EaCloud.SMS/) | [![EaCloud.SMS](https://img.shields.io/nuget/dt/EaCloud.SMS.svg)](https://www.nuget.org/packages/EaCloud.SMS/) |
| [EaCloud.Swagger](https://www.nuget.org/packages/EaCloud.Swagger/) | [![EaCloud.Swagger](https://img.shields.io/nuget/v/EaCloud.Swagger.svg)](https://www.nuget.org/packages/EaCloud.Swagger/) | [![EaCloud.Swagger](https://img.shields.io/nuget/vpre/EaCloud.Swagger.svg)](https://www.nuget.org/packages/EaCloud.Swagger/) | [![EaCloud.Swagger](https://img.shields.io/nuget/dt/EaCloud.Swagger.svg)](https://www.nuget.org/packages/EaCloud.Swagger/) |
| [EaCloud.Utils](https://www.nuget.org/packages/EaCloud.Utils/) | [![EaCloud.Utils](https://img.shields.io/nuget/v/EaCloud.Utils.svg)](https://www.nuget.org/packages/EaCloud.Utils/) | [![EaCloud.Utils](https://img.shields.io/nuget/vpre/EaCloud.Utils.svg)](https://www.nuget.org/packages/EaCloud.Utils/) | [![EaCloud.Utils](https://img.shields.io/nuget/dt/EaCloud.Utils.svg)](https://www.nuget.org/packages/EaCloud.Utils/) |
| [EaCloud.Workflow](https://www.nuget.org/packages/EaCloud.Workflow/) | [![EaCloud.Workflow](https://img.shields.io/nuget/v/EaCloud.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Workflow/) | [![EaCloud.Workflow](https://img.shields.io/nuget/vpre/EaCloud.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Workflow/) | [![EaCloud.Workflow](https://img.shields.io/nuget/dt/EaCloud.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Workflow/) |
| [EaCloud.Pack.Audit](https://www.nuget.org/packages/EaCloud.Pack.Audit/) | [![EaCloud.Pack.Audit](https://img.shields.io/nuget/v/EaCloud.Pack.Audit.svg)](https://www.nuget.org/packages/EaCloud.Pack.Audit/) | [![EaCloud.Pack.Audit](https://img.shields.io/nuget/vpre/EaCloud.Pack.Audit.svg)](https://www.nuget.org/packages/EaCloud.Pack.Audit/) | [![EaCloud.Pack.Audit](https://img.shields.io/nuget/dt/EaCloud.Pack.Audit.svg)](https://www.nuget.org/packages/EaCloud.Pack.Audit/) |
| [EaCloud.Pack.Authorization](https://www.nuget.org/packages/EaCloud.Pack.Authorization/) | [![EaCloud.Pack.Authorization](https://img.shields.io/nuget/v/EaCloud.Pack.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Pack.Authorization/) | [![EaCloud](https://img.shields.io/nuget/vpre/EaCloud.Pack.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Pack.Authorization/) | [![EaCloud.Pack.Authorization](https://img.shields.io/nuget/dt/EaCloud.Pack.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Pack.Authorization/) |
| [EaCloud.Pack.File](https://www.nuget.org/packages/EaCloud.Pack.File/) | [![EaCloud.Pack.File](https://img.shields.io/nuget/v/EaCloud.Pack.File.svg)](https://www.nuget.org/packages/EaCloud.Pack.File/) | [![EaCloud.Pack.File](https://img.shields.io/nuget/vpre/EaCloud.Pack.File.svg)](https://www.nuget.org/packages/EaCloud.Pack.File/) | [![EaCloud.Pack.File](https://img.shields.io/nuget/dt/EaCloud.Pack.File.svg)](https://www.nuget.org/packages/EaCloud.Pack.File/) |
| [EaCloud.Pack.Identity](https://www.nuget.org/packages/EaCloud.Pack.Identity/) | [![EaCloud.Pack.Identity](https://img.shields.io/nuget/v/EaCloud.Pack.Identity.svg)](https://www.nuget.org/packages/EaCloud.Pack.Identity/) | [![EaCloud.Pack.Identity](https://img.shields.io/nuget/vpre/EaCloud.Pack.Identity.svg)](https://www.nuget.org/packages/EaCloud.Pack.Identity/) | [![EaCloud.Pack.Identity](https://img.shields.io/nuget/dt/EaCloud.Pack.Identity.svg)](https://www.nuget.org/packages/EaCloud.Pack.Identity/) |
| [EaCloud.Pack.IM](https://www.nuget.org/packages/EaCloud.Pack.IM/) | [![EaCloud.Pack.IM](https://img.shields.io/nuget/v/EaCloud.Pack.IM.svg)](https://www.nuget.org/packages/EaCloud.Pack.IM/) | [![EaCloud.Pack.IM](https://img.shields.io/nuget/vpre/EaCloud.Pack.IM.svg)](https://www.nuget.org/packages/EaCloud.Pack.IM/) | [![EaCloud.Pack.IM](https://img.shields.io/nuget/dt/EaCloud.Pack.IM.svg)](https://www.nuget.org/packages/EaCloud.Pack.IM/) |
| [EaCloud.Pack.Menu](https://www.nuget.org/packages/EaCloud.Pack.Menu/) | [![EaCloud.Pack.Menu](https://img.shields.io/nuget/v/EaCloud.Pack.Menu.svg)](https://www.nuget.org/packages/EaCloud.Pack.Menu/) | [![EaCloud.Pack.Menu](https://img.shields.io/nuget/vpre/EaCloud.Pack.Menu.svg)](https://www.nuget.org/packages/EaCloud.Pack.Menu/) | [![EaCloud.Pack.Menu](https://img.shields.io/nuget/dt/EaCloud.Pack.Menu.svg)](https://www.nuget.org/packages/EaCloud.Pack.Menu/) |
| [EaCloud.Pack.Message](https://www.nuget.org/packages/EaCloud.Pack.Message/) | [![EaCloud.Pack.Message](https://img.shields.io/nuget/v/EaCloud.Pack.Message.svg)](https://www.nuget.org/packages/EaCloud.Pack.Message/) | [![EaCloud.Pack.Message](https://img.shields.io/nuget/vpre/EaCloud.Pack.Message.svg)](https://www.nuget.org/packages/EaCloud.Pack.Message/) | [![EaCloud.Pack.Message](https://img.shields.io/nuget/dt/EaCloud.Pack.Message.svg)](https://www.nuget.org/packages/EaCloud.Pack.Message/) |
| [EaCloud.Pack.Report](https://www.nuget.org/packages/EaCloud.Pack.Report/) | [![EaCloud.Pack.Report](https://img.shields.io/nuget/v/EaCloud.Pack.Report.svg)](https://www.nuget.org/packages/EaCloud.Pack.Report/) | [![EaCloud.Pack.Report](https://img.shields.io/nuget/vpre/EaCloud.Pack.Report.svg)](https://www.nuget.org/packages/EaCloud.Pack.Report/) | [![EaCloud.Pack.Report](https://img.shields.io/nuget/dt/EaCloud.Pack.Report.svg)](https://www.nuget.org/packages/EaCloud.Pack.Report/) |
| [EaCloud.Pack.SMS](https://www.nuget.org/packages/EaCloud.Pack.SMS/) | [![EaCloud.Pack.SMS](https://img.shields.io/nuget/v/EaCloud.Pack.SMS.svg)](https://www.nuget.org/packages/EaCloud.Pack.SMS/) | [![EaCloud.Pack.SMS](https://img.shields.io/nuget/vpre/EaCloud.Pack.SMS.svg)](https://www.nuget.org/packages/EaCloud.Pack.SMS/) | [![EaCloud.Pack.SMS](https://img.shields.io/nuget/dt/EaCloud.Pack.SMS.svg)](https://www.nuget.org/packages/EaCloud.Pack.SMS/) |
| [EaCloud.Pack.Workflow](https://www.nuget.org/packages/EaCloud.Pack.Workflow/) | [![EaCloud.Pack.Workflow](https://img.shields.io/nuget/v/EaCloud.Pack.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Pack.Workflow/) | [![EaCloud.Pack.Workflow](https://img.shields.io/nuget/vpre/EaCloud.Pack.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Pack.Workflow/) | [![EaCloud.Pack.Workflow](https://img.shields.io/nuget/dt/EaCloud.Pack.Workflow.svg)](https://www.nuget.org/packages/EaCloud.Pack.Workflow/) |
| [EaCloud.Api.Audit](https://www.nuget.org/packages/EaCloud.Api.Audit/) | [![EaCloud.Api.Audit](https://img.shields.io/nuget/v/EaCloud.Api.Audit.svg)](https://www.nuget.org/packages/EaCloud.Api.Audit/) | [![EaCloud.Api.Audit](https://img.shields.io/nuget/vpre/EaCloud.Api.Audit.svg)](https://www.nuget.org/packages/EaCloud.Api.Audit/) | [![EaCloud.Api.Audit](https://img.shields.io/nuget/dt/EaCloud.Api.Audit.svg)](https://www.nuget.org/packages/EaCloud.Api.Audit/) |
| [EaCloud.Api.Authorization](https://www.nuget.org/packages/EaCloud.Api.Authorization/) | [![EaCloud.Api.Authorization](https://img.shields.io/nuget/v/EaCloud.Api.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Api.Authorization/) | [![EaCloud.Api.Authorization](https://img.shields.io/nuget/vpre/EaCloud.Api.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Api.Authorization/) | [![EaCloud.Api.Authorization](https://img.shields.io/nuget/dt/EaCloud.Api.Authorization.svg)](https://www.nuget.org/packages/EaCloud.Api.Authorization/) |
| [EaCloud.Api.Baidu](https://www.nuget.org/packages/EaCloud.Api.Baidu/) | [![EaCloud.Api.Baidu](https://img.shields.io/nuget/v/EaCloud.Api.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Api.Baidu/) | [![EaCloud.Api.Baidu](https://img.shields.io/nuget/vpre/EaCloud.Api.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Api.Baidu/) | [![EaCloud.Api.Baidu](https://img.shields.io/nuget/dt/EaCloud.Api.Baidu.svg)](https://www.nuget.org/packages/EaCloud.Api.Baidu/) |
| [EaCloud.Api.File](https://www.nuget.org/packages/EaCloud.Api.File/) | [![EaCloud.Api.File](https://img.shields.io/nuget/v/EaCloud.Api.File.svg)](https://www.nuget.org/packages/EaCloud.Api.File/) | [![EaCloud.Api.File](https://img.shields.io/nuget/vpre/EaCloud.Api.File.svg)](https://www.nuget.org/packages/EaCloud.Api.File/) | [![EaCloud](https://img.shields.io/nuget/dt/EaCloud.Api.File.svg)](https://www.nuget.org/packages/EaCloud.Api.File/) |
| [EaCloud.Api.Identity](https://www.nuget.org/packages/EaCloud.Api.Identity/) | [![EaCloud.Api.Identity](https://img.shields.io/nuget/v/EaCloud.Api.Identity.svg)](https://www.nuget.org/packages/EaCloud.Api.Identity/) | [![EaCloud.Api.Identity](https://img.shields.io/nuget/vpre/EaCloud.Api.Identity.svg)](https://www.nuget.org/packages/EaCloud.Api.Identity/) | [![EaCloud.Api.Identity](https://img.shields.io/nuget/dt/EaCloud.Api.Identity.svg)](https://www.nuget.org/packages/EaCloud.Api.Identity/) |
| [EaCloud.Api.IM](https://www.nuget.org/packages/EaCloud.Api.IM/) | [![EaCloud.Api.IM](https://img.shields.io/nuget/v/EaCloud.Api.IM.svg)](https://www.nuget.org/packages/EaCloud.Api.IM/) | [![EaCloud.Api.IM](https://img.shields.io/nuget/vpre/EaCloud.Api.IM.svg)](https://www.nuget.org/packages/EaCloud.Api.IM/) | [![EaCloud.Api.IM](https://img.shields.io/nuget/dt/EaCloud.Api.IM.svg)](https://www.nuget.org/packages/EaCloud.Api.IM/) |
| [EaCloud.Api.Menu](https://www.nuget.org/packages/EaCloud.Api.Menu/) | [![EaCloud.Api.Menu](https://img.shields.io/nuget/v/EaCloud.Api.Menu.svg)](https://www.nuget.org/packages/EaCloud.Api.Menu/) | [![EaCloud.Api.Menu](https://img.shields.io/nuget/vpre/EaCloud.Api.Menu.svg)](https://www.nuget.org/packages/EaCloud.Api.Menu/) | [![EaCloud.Api.Menu](https://img.shields.io/nuget/dt/EaCloud.Api.Menu.svg)](https://www.nuget.org/packages/EaCloud.Api.Menu/) |
| [EaCloud.Api.Message](https://www.nuget.org/packages/EaCloud.Api.Message/) | [![EaCloud.Api.Message](https://img.shields.io/nuget/v/EaCloud.Api.Message.svg)](https://www.nuget.org/packages/EaCloud.Api.Message/) | [![EaCloud.Api.Message](https://img.shields.io/nuget/vpre/EaCloud.Api.Message.svg)](https://www.nuget.org/packages/EaCloud.Api.Message/) | [![EaCloud.Api.Message](https://img.shields.io/nuget/dt/EaCloud.Api.Message.svg)](https://www.nuget.org/packages/EaCloud.Api.Message/) |
| [EaCloud.Api.Report](https://www.nuget.org/packages/EaCloud.Api.Report/) | [![EaCloud.Api.Report](https://img.shields.io/nuget/v/EaCloud.Api.Report.svg)](https://www.nuget.org/packages/EaCloud.Api.Report/) | [![EaCloud.Api.Report](https://img.shields.io/nuget/vpre/EaCloud.Api.Report.svg)](https://www.nuget.org/packages/EaCloud.Api.Report/) | [![EaCloud.Api.Report](https://img.shields.io/nuget/dt/EaCloud.Api.Report.svg)](https://www.nuget.org/packages/EaCloud.Api.Report/) |
| [EaCloud.Api.SMS](https://www.nuget.org/packages/EaCloud.Api.SMS/) | [![EaCloud.Api.SMS](https://img.shields.io/nuget/v/EaCloud.Api.SMS.svg)](https://www.nuget.org/packages/EaCloud.Api.SMS/) | [![EaCloud.Api.SMS](https://img.shields.io/nuget/vpre/EaCloud.Api.SMS.svg)](https://www.nuget.org/packages/EaCloud.Api.SMS/) | [![EaCloud.Api.SMS](https://img.shields.io/nuget/dt/EaCloud.Api.SMS.svg)](https://www.nuget.org/packages/EaCloud.Api.SMS/) |
| [EaCloud.Api.System](https://www.nuget.org/packages/EaCloud.Api.System/) | [![EaCloud.Api.System](https://img.shields.io/nuget/v/EaCloud.Api.System.svg)](https://www.nuget.org/packages/EaCloud.Api.System/) | [![EaCloud.Api.System](https://img.shields.io/nuget/vpre/EaCloud.Api.System.svg)](https://www.nuget.org/packages/EaCloud.Api.System/) | [![EaCloud.Api.System](https://img.shields.io/nuget/dt/EaCloud.Api.System.svg)](https://www.nuget.org/packages/EaCloud.Api.System/) |


## <a id="02"/>EaCloud特性

### 1. 模块化的组件设计

框架设计了一个模块（[Pack](https://eacloud_docs.sanqing.tech/api/EaCloud.Core.Packs.html)）的系统，所有实现了模块基类（[PackBase](https://eacloud_docs.sanqing.tech/api/EaCloud.Core.Packs.PackBase.html)）的类都视为一个独立的模块，一个模块可以独立添加服务（AddServices），并可在初始化时应用服务（UsePack）进行模块初始化。

### 2. 自动化的依赖注入机制

框架定义了`ISingletonDependency`，`IScopeDependency`，`ITransientDependency`三个空接口对应DependencyInjection中的三种服务生命周期，系统初始化时，通过反射检索程序集的方式，检索出所有服务类型(ServiceType)与服务实现(ImplementationType)及生命周期类型(ServiceLifetime)的相关数据，对依赖注入的ServiceCollection进行全自动初始化。

### 3. UnitOfWork + Repository 模式，EFCore上下文动态构建设计

* 实体数据模块使用了`UnitOfWork + Repository`的模式来设计，设计了一个泛型的实体仓储接口`IRepository<TEntity,TKey>`，避免每个实体都需实现一个仓储的繁琐操作。设计了`IUnitOfWork`接口来管理事务，通过UnitOfWork模式管理DbContext的创建，使同上下文类型同数据库连接字符串的上下文使用**相同DbConnection**对象来创建，达到多上下文的事务同步能力。

* 基于API的`ActionFilter`的`UnitOfWorkAttribute` AOP 事务自动提交，业务中不再需要关心事务的生命周期。
* 系统初始化时，通过反射检索程序集的方式，检索出各个实体与上下文的映射关系，向上下文中动态添加实体类来构建上下文类型，以达到上下文类型与业务实体解耦的目的。通过统一基类`EntityTypeConfigurationBase<TEntity, TKey>`的FluentAPI实体映射，自由配置每个实体与数据库映射的每一个细节。

### 4. 基于AspNetCore的Identity的身份认证系统设计

* 使用AspNetCore原生的用户身份认证框架，身份认证相关操作统一使用`UserManager<TUser>`，`RoleManager<TRole>`两个入口，保持了原生Identity的体系强大性与功能完整性。

* 重新设计了用户存储`UserStore`和角色存储`RoleStore`，使用框架内设计的`IRepository<TEntity,TKey>`数据仓储接口来实现对数据的仓储操作，使Identity**身份认证系统与框架完美结合**，避免了使用官方的`Microsoft.AspNetCore.Identity.EntityFrameworkCore`造成多个上下文或者被强制使用Identity上下文作为系统数据上下文来实现业务造成的尴尬。

* 设计了组织机构存储`OrganizationStore`，使用框架内设计的`IRepository<TEntity,TKey>`数据仓储接口来实现对数据的仓储操作，使Identity**身份认证系统与框架组织机构处理完美结合**，同时支持更换登录组织后重新发放令牌，并强制原令牌过期机制。
![image](https://eacloud_docs.sanqing.tech/images/002.organization.jpg)

### 5. 强大的功能权限与数据权限的授权体系设计

* 从底层开始，自动收集了系统的所有业务点（[IFunction](https://eacloud_docs.sanqing.tech/api/EaCloud.Authorization.Functions.IFunction.html)）和数据实体（[IEntityInfo](https://eacloud_docs.sanqing.tech/api/EaCloud.Authorization.EntityInfos.IEntityInfo.html)），用于对系统的功能权限、数据权限、数据缓存、操作审计 等实用功能提供数据支持。

* 功能点`Function`与API的`Area/Controller/Action`一一对应，是功能权限的最小验证单位，基于功能点，可以配置：
    * 功能访问类型（匿名访问、登录访问、限定角色访问）
    * 功能的数据缓存时间及缓存过期方式（绝对过期、相对过期）
    * 是否开启操作审计（XX用户XX时间做了XX操作）
    * 是否开启数据审计（操作引起的数据变化详情（新增、更新、删除））

    ![image](https://eacloud_docs.sanqing.tech/images/002.function.jpg)

* 数据实体`EntityInfo`与数据库中的各个数据实体一一对应，基于数据实体，可以配置：
    * 是否开启数据审计，与`Function`上的同配置级别不同，如果指定实体未开放审计，则不审计当前实体。

    ![image](https://eacloud_docs.sanqing.tech/images/003.entityinfo.jpg)

* 设计了一个树形结构的业务模块体系（[Module](https://eacloud_docs.sanqing.tech/api/EaCloud.Authorization.Entities.ModuleBase-1.html)），对应着后端向前端开放的操作点（菜单/按钮），一个模块可由一个或多个功能点构成，模块是对外开放的特殊功能点，是进行**角色/用户功能授权**的单位。把一个模块授权给角色，角色即拥有了一个或多个功能点的操作权限。

![image](https://eacloud_docs.sanqing.tech/images/004.module.jpg)

* #### 功能权限授权流程
    * **[自动]** 创建APIC的各个`Area/Controller/Action`的功能点`Function`信息，存储到数据库
    * **[自动]** 创建树形模块`Module`信息，并创建模块与功能点（一个或多个）的分配关系，存储到数据库
    * 将模块`Module`分配给角色`Role`
    * 将角色`Role`分配给用户`User`
    * 可将模块`Module`分配给用户`User`，解决特权问题
    * 这样用户即可根据拥有的角色，自动拥有模块对应着的所有功能点的功能权限 

    ![image](https://eacloud_docs.sanqing.tech/images/005.authorization.jpg)

* #### 功能权限验证流程
    * 系统初始化时，根据每个角色`Role`分配到的模块`Module`，自动初始化每个 `角色 Role - Function[] `的权限对应关系并缓存
    * 游客进入系统时，自动请求所有可匿名访问`FunctionAccessType.Anonymouse`的模块信息并缓存到浏览器，浏览器根据这个缓存的模块集合，对前端页面的各个操作点（菜单/按钮）进行是否隐藏/禁用的状态控制
    * 注册用户登录系统时，自动请求所有可执行（包括匿名的`FunctionAccessType.Anonymouse`、登录的`FunctionAccessType.Logined`、指定角色的`FunctionAccessType.RoleLimit`）的模块信息并缓存到浏览器，浏览器根据这个缓存的模块集合，对前端页面的各个操作点（菜单/按钮）进行是否隐藏/禁用的状态控制
    * 用户`User`执行一个功能点`Function`时，验证流程如下：
        * 功能点不存在时，返回404
        * 功能点被锁定时，返回423
        * 功能点可访问性为匿名`FunctionAccessType.Anonymouse`验证通过
        * 功能点可访问性为需要登录`FunctionAccessType.Logined`时，用户未登录，返回401，已登录则验证通过
        * 功能点可访问性为需要登录`FunctionAccessType.RoleLimit`时，流程如下：
            * 用户未登录，返回401
            * 逐个验证用户拥有的角色`Role`，根据角色从缓存中取出`Role-Function[]`缓存项，`Function[]`包含要验证的功能点时，验证通过
            * 由分配给用户的模块`Module`对应的功能点，获取到`User-Function[]`（并缓存），`Function[]`包含要验证的功能点时，验证通过
            * 验证未通过，返回403

* #### 数据权限授权流程
    * 基于 角色`Role`-实体`EntityInfo` 的数据权限设计，通过配置实现 XX角色是否有权访问XX实体数据（的XX属性）

    ![image](https://eacloud_docs.sanqing.tech/images/006.datafilter.jpg)

* #### 数据权限验证流程
    * 系统初始化时，将所有`角色-实体`的数据筛选规则缓存到内存中
    * 进行数据查询的时候，根据当前用户的所有`角色 Role`和要查询的`实体 EntityInfo`，查找出所有配置的数据筛选规则`FilterGroup`，转换为数据查询表达式`Expression<Func<TEntity,bool>>`，各个角色的表达式之间使用`Or`逻辑进行组合
    * 将以上生成的`数据权限`数据查询表达式，使用`And`逻辑组合到用户的提交的查询条件生成的表达式中，得到最终的数据查询表达式，提交到数据库中进行数据查询，从而获得数据权限限制下的合法数据

    ![image](https://eacloud_docs.sanqing.tech/images/007.datafilter.jpg)

### 6. 灵活统一的数据查询筛选规则设计

数据查询筛选规则组成为 条件组`FilterGroup`和条件`FilterRule`，一个条件组 [FilterGroup](https://eacloud_docs.sanqing.tech/api/EaCloud.Filter.FilterGroup.html) 包含 一个或多个条件 [FilterRule](https://eacloud_docs.sanqing.tech/api/EaCloud.Filter.FilterRule.html) 和 一个或多个 条件组`FilterGroup`，这样就实现了条件组和条件的无限嵌套，能满足绝大多数数据筛选规则的组装需要，如下图：
    
![image](https://eacloud_docs.sanqing.tech/images/006.filter.jpg)

### 7. 集成 Swagger 后端API文档系统

EaCloud 快速启动模板的开发模式，集成了 `Swagger` API 文档生成组件，方便前后端分离的开发模式中前后端开发人员的数据接口对接工作。基于`Swagger`的工作原理，API的输入输出都需使用`强类型`的数据类型，`Swagger`才能发挥更好的作用，而EaCloud框架通过`AutoMapper`的`ProjectTo`对业务实体到输出DTO`IOutputDto`提供了自动映射功能，能有效减轻后端开发中数据对象属性映射的工作量。

![image](https://eacloud_docs.sanqing.tech/images/008.swagger.jpg)

### 8. 集成 Hangfire 后端任务管理系统

EaCloud 快速开发平台集成了 `Hangfire` 任务管理组件，方便后端针对任务自动执行的需求。基于`Hangfire`的工作原理，支持 列队任务、延时任务、后继任务、定时任务等模式，基于服务注入的模式，任务执行逻辑可以调用系统依赖模块的所有功能，更灵活的实现业务场景。

![image](https://eacloud_docs.sanqing.tech/images/009.hangfire.jpg)

## <a id="03"/> EaCloud快速启动

EaCloud框架制作了一个基于`dotnet cli`命令行工具的快速启动模板，下面演示如何来使用这个模板快速创建一个基于EaCloud框架的初始化项目。

### 1. 安装最新版本 .NET 6.0 sdk 及 runtime

EaCloud当前版本（7.0.0.5）使用了 `.NET 7.0` 当前最新版本 `7.0.4`。`.NET 7.0 sdk` 需要安装到版本 [>=v7.0.100](https://dotnet.microsoft.com/zh-cn/download/dotnet/7.0)，`.NET 7.0 runtime` 需要安装到版本 [>=v7.0.0](https://dotnet.microsoft.com/zh-cn/download/dotnet/7.0/runtime)。

### 2. 安装EaCloud的`dotnet new`项目模板

在任意空白目录，打开 `cmd`或`powershell` （<kbd>Shift</kbd>+<kbd>空白处鼠标右击</kbd>+<kbd>在此处打开Powershell窗口(S)</kbd>） 命令行窗口，执行命令

```bash
dotnet new install EaCloud.Template
```

执行后，将能看到`EaCloud.Template`命令已安装到列表中

![image](https://eacloud_docs.sanqing.tech/images/010.template.jpg)

### 3. 执行`EaCloud.Template`命令，获取项目一键项目安装脚本

```bash
dotnet new EaCloud.Template
```

执行后，将得到一个名为`eacloud.cmd`的批处理脚本文件

![image](https://eacloud_docs.sanqing.tech/images/011.eacloud.cmd.jpg)

### 4. 运行脚本文件，生成项目初始化代码

直接执行`eacloud.cmd`脚本代码，将会提示 `请输入项目名称，推荐形如 “公司.项目”的模式：`，此名称将用作后端解决方案名称、工程名称起始部分、代码中的`namespace`起始部分。

![image](https://eacloud_docs.sanqing.tech/images/012.eacloud.cmd.run.jpg)

例如输入`SanQing.Test`，然后根据提示步骤操作。当所有确认选项选择`Y`时，将生成如下结构：

![image](https://eacloud_docs.sanqing.tech/images/013.eacloud.cmd.res.jpg)

### 5. 用 Visual Studio 打开后端解决方案

注：由于 EaCloud 基于最新的 `.NET 7.0` 框架，IDE工具需要安装 [Visual Studio 2022](https://visualstudio.microsoft.com/zh-hans/) 及以上版本，否则有可能会出现未知的异常。

打开解决方案后，各个工程之间的引用关系已配置好，eacloud框架的类库已引用 nuget.org 上的相应版本，并将自动还原好。项目结构如图所示：

![image](https://eacloud_docs.sanqing.tech/images/014.back-end.vs.jpg)

#### 5.1 项目自定义Pack代码结构说明：

* Core： 业务核心工程，顶层文件夹以业务模块内聚，每个文件夹按职责划分文件夹，通常可包含传输对象`Dtos`、实体类型`Entities`、事件处理`Events`等，业务接口IXXXContract与业务实现IXXXService放在外边，如果文件数量多的话也可以建文件夹存放。
* EntityConfiguration： EFCore实体映射工程，用于配置各个业务实体映射到数据库的映射细节。文件夹也推荐按模块内聚。
* Api： 网站的Hosting项目，按常规方式使用即可

##### 注：其余项目参见各自项目内的 README.md 文件。

#### 5.2 项目启动配置

* 确认并设置`services`目录下`XXX.Svc`项目为启动项目，`XXX.Svc`中`XXX`为运行生成项目脚本文件时输入的项目名称。
* 按实际环境修改启动项目下配置文件（Debug：`appsettings.Development.json`、Release：`appsettings.json`）中的`EaCloud:DbContexts:[MySql|Oracle|PostgreSql|Sqlite|SqlServer]`中的配置信息，`ConnectionString`为数据库连接串，`AutoMigrationEnabled`为是否开启自动迁移。
* EaCloud后端ORM采用了微软的`EF Core`框架，默认`Code First`模式，需要在`nuget 控制台`执行`Add-Migration [-Name] <String>`命令生成迁移代码文件，示例如下：

```bash
add-migration -Name InitialCreate
```
##### 注：更多 EF Core 配置说明`Startups\README.EntityFrameworkCore.Migration.md`或访问 [Entity Framework Core](https://docs.microsoft.com/zh-cn/ef/core/) 。

* 若未开启`AutoMigrationEnabled`的自动迁移功能，还需要在`nuget 控制台`手动执行迁移操作，命令如下：

```bash
update-database
```
* 配置好后，即可正常启动端口号为`38062`的项目，启动后追加路由 “/swagger（名称可配置）”将进入`Swagger`的后端Api接口的文档页。

##### 注：后端.NET Core项目支持自宿主模式启动，当采用自宿主模式时，需要正确设置配置文件（Debug：`appsettings.Development.json`、Release：`appsettings.json`）下`EaCloud:Host`节点。
##### 另附上.Net Core部署至Windows服务教程：
* [使用NSSM把.Net Core部署至 Windows 服务](https://www.cnblogs.com/emrys5/p/nssm-netcore.html)
* [在 Windows 服务中托管 ASP.NET Core](https://docs.microsoft.com/zh-cn/aspnet/core/host-and-deploy/windows-service?view=aspnetcore-6.0&tabs=visual-studio)

注：后端项目参考借鉴了 `OSharp` 开源框架，详情链接 [https://github.com/dotnetcore/osharp](https://github.com/dotnetcore/osharp)。

### 6. Vue的前端项目启动

前端项目使用了`Vue-Vben-Admin`和`Ant-Design-Vue`作为UI进行开发的，需要熟悉`NodeJS`、`Vue3.0`、`Vite`、`Ant-Design-Vue`、`TypeScript`等主流技术。
[Vben Admin 官方文档](https://doc.vvbin.cn)，[Ant Design Vue 官方文档](https://2x.antdv.com/docs/vue/introduce-cn/)

#### 6.1 前端环境准备

本地环境需要安装 [Git](https://git-scm.com)、[NodeJS](https://nodejs.org/zh-cn/) 和 [pnpm](https://www.pnpm.cn)（官方目前使用方式） 或者 [Yarn](https://yarn.bootcss.com)

##### 注：1、Node.js 版本要求16.x以上。2、Pnpm 版本要求6.x以上。3、Yarn 必须使用1.x，否则依赖可能安装不上。

* **pnpm常用命令：**
  * 安装
  ```bash
  # 全局安装最新版本
  npm i -g pnpm
  # 查看版本
  pnpm --version
  ```
  * 安装第三方模块
  ```bash
  # 安装默认添加至 dependencies
  pnpm install [package]
  # 安装并添加至 devDependencies
  pnpm install [package] -D
  # 安装并添加至 dependencies
  pnpm install [package] -S
  ```
  * 更新第三方模块
  ```bash
  pnpm update
  ```
  * 卸载第三方模块
  ```bash
  pnpm uninstall [package]
  ```

* **yarn常用命令：**
  * 安装
  ```bash
  # 全局安装最新版本
  npm install -g yarn
  # 查看版本
  yarn --version
  ```
  * 安装第三方模块
  ```bash
  # 在当前的项目中添加一个依赖包，会自动更新到package.json和yarn.lock文件中
  yarn add [package]
  # 安装指定版本，这里指的是主要版本，如果需要精确到小版本，使用-E参数
  yarn add [package]@[version]
  # 安装某个tag（比如beta,next或者latest）
  yarn add [package]@[tag]
  # 不指定依赖类型默认安装到dependencies里，你也可以指定依赖类型：
  yarn add --dev/-D # 加到 devDependencies
  yarn add --peer/-P # 加到 peerDependencies
  yarn add --optional/-O # 加到 optionalDependencies
  ```
  * 更新第三方模块
  ```bash
  yarn upgrade [package]
  ```
  * 卸载第三方模块
  ```bash
  yarn remove [package]
  ```

#### 6.2 前端工具配置

如果您使用的 IDE 是 [Visual Studio Code](https://code.visualstudio.com/)(推荐，前端最好用的IDE) 的话，可以安装以下工具来提高开发效率及代码格式化：

##### 6.2.1 建议安装插件

* [Iconify IntelliSense](https://marketplace.visualstudio.com/items?itemName=antfu.iconify) - Iconify 图标插件
* [windicss IntelliSense](https://marketplace.visualstudio.com/items?itemName=voorjaar.windicss-intellisense) - windicss 提示插件
* [I18n-ally](https://marketplace.visualstudio.com/items?itemName=Lokalise.i18n-ally) - i18n 国际化插件
* [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar) - Vue3 开发必备 （也可以选择 [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur) - Vue2 不推荐）
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - 脚本代码检查
* [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - 代码格式化
* [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint) - css 格式化
* [DotENV](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv) - .env 文件 高亮

##### 6.2.2 选装插件

* [Chinese (Simplified) Language Pack](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans) - 适用于 VS Code 的中文（简体）语言包
* [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) - 可视化 git 分支和提交记录
* [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons) - 可以让 vscode 中的文件管理的树目录显示图标，显示图标后会使得文件、文件夹更加明确功能
* [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments) - 美化注释的插件，可以根据不同种类的注释，显示不同的颜色，一目了然 [使用说明](https://www.cnblogs.com/suwanbin/p/13263732.html)
* [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight) - 颜色高亮展示插件，直观的显示色值对应的颜色

##### 6.2.3 摸鱼插件

* [小霸王](https://marketplace.visualstudio.com/items?itemName=gamedilong.anes) - 基于vscode的nes游戏插件。通过劳逸结合，提升开发效率。请务必在闲暇时间使用本插件，若是上班摸鱼被发现，后果自负~

```text
注：注意存放代码的目录及所有父级目录不能存在中文、韩文、日文以及空格，否则安装依赖后启动会出错。
```

#### 6.3 使用 VS Code 打开Vue前端项目

* 定位到项目的目录`front-end\background-gui\vben-admin`，在空白处点右键，使用 VS Code 打开项目，可看到如下结构：

![image](https://eacloud_docs.sanqing.tech/images/015.vben-admin.vs.jpg)
##### 注：项目结构中功能代码存放于 src 目录。其中 api 为与后端交互的接口函数目录，assets 为本地资源目录，components 为组件目录，enums 为枚举目录，locales 为国际化多语言目录，router 为页面路由配置目录，views 为页面功能目录，其余的请查看具体目录下的代码功能。

* 按 <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>`</kbd> 调出VS Code的终端，按步骤执行以下命令：

  * 安装依赖
  ```bash
  # pnpm方式：
  pnpm install
  # yarn方式：
  yarn 
  # OR
  yarn install 
  ```

  * 依赖安装完成后，运行项目
  ```bash
  # pnpm方式：
  pnpm dev
  # yarn方式：
  yarn dev
  ```
  ![image](https://eacloud_docs.sanqing.tech/images/016.vben-admin.vs.run.jpg)

  * 构建/发布程序
  ```bash
  # pnpm方式：
  pnpm build
  # yarn方式：
  yarn build 
  ```

至此，项目启动完成，最终效果如下图所示：

![image](https://eacloud_docs.sanqing.tech/images/017.vben-admin.login.jpg)
![image](https://eacloud_docs.sanqing.tech/images/018.vben-admin.main.jpg)

注：前端项目使用了 `Vben Admin` 作为前端框架，更多资料详见 [官方文档](https://doc.vvbin.cn)。
附：[nginx下载链接](http://nginx.org/en/download.html)。

### 7. 移动端项目启动

移动端项目使用了`DCloud`的`uni-app`作为框架进行开发的，IDE工具为`HBuilder X`，需要熟悉`NodeJS`、`Vue`、`JavaScript`等主流技术。
[DCloud 官网](https://www.dcloud.io)，[uni-app 官方文档](https://uniapp.dcloud.net.cn)，[HBuilder X 官方文档](https://www.dcloud.io/hbuilderx.html)

#### 7.1 环境准备

本地环境需要安装 [Git](https://git-scm.com)、[NodeJS](https://nodejs.org/zh-cn/)

##### 注：参见 6 Vue的前端项目启动。

#### 7.2 开发工具（IDE）配置

移动端项目使用的 IDE 是 [HBuilder X](https://www.dcloud.io/hbuilderx.html)(推荐，其他IDE请自行百度)。

```text
注：注意存放代码的目录及所有父级目录不能存在中文、韩文、日文以及空格，否则可能存在未知的问题。
```

#### 7.3 使用 HBuilder X 打开移动端项目

* 打开 HBuilder X 程序，打开或导入项目`app\pda`，可看到如下结构：

![image](https://eacloud_docs.sanqing.tech/images/019.app-pda-uni-app.hbuilderx.jpg)
##### 注：项目结构中，apis 为与后端交互的接口函数目录，config 为配置目录，static 为静态资源目录，enums 为枚举目录，locales 为国际化多语言目录，pages.json 为页面路由配置文件，pages 为页面功能目录，其余的请查看具体目录下的代码功能。

* 若项目结构中不存在`node_modules`目录，请检查并删除`package-lock.json`或者`pnpm-lock.yaml`文件后执行以下命令：
  * 安装依赖
  ```bash
  # npm方式：
  npm install
  # pnpm方式：
  pnpm install
  # yarn方式：
  yarn 
  # OR
  yarn install 
  ```

* 运行项目

![image](https://eacloud_docs.sanqing.tech/images/020.app-pda-uni-app.hbuilderx.run.jpg)

* 发行/打包程序

![image](https://eacloud_docs.sanqing.tech/images/021.app-pda-uni-app.hbuilderx.build.jpg)

至此，移动端项目启动完成，最终效果如下图所示：

![image](https://eacloud_docs.sanqing.tech/images/022.app-pda-uni-app.login.jpg)
![image](https://eacloud_docs.sanqing.tech/images/023.app-pda-uni-app.profile.jpg)

注：移动端项目使用了 `uni app` 作为开发框架，更多资料详见 [官方文档](https://uniapp.dcloud.net.cn)。

## <a id="04"/>EaCloud结构概述

截止到目前，EaCloud 框架的计划中的功能点均已得到较高水准的实现，结构概述如下所示：

- [x] **易云开发平台（EaCloud Framework）**
    - [x] EaCloud
        - [x] 添加常用Utility辅助工具类
        - [x] 添加框架配置Options定义
        - [x] 定义Entity数据访问相关接口
        - [x] 定义依赖注入模块相关接口
        - [x] 定义并实现EventBus事件总线的设计
        - [x] 定义Mapper对象映射模块相关接口
        - [x] 定义实体信息EntityInfo及初始化，用于给各个实体进行数据日志审计配置及数据权限设计
        - [x] 定义功能点信息Function及初始化，用于收集各个业务功能点（API的Action），用于对功能进行缓存配置、操作日志审计、功能权限设计
        - [x] 定义实体信息Module及初始化，用于记录系统模块的树形结构信息
        - [x] 定义Audit审计功能，用于处理需要操作及数据记录的审计信息
        - [x] 定义DistributedCache分布式缓存的功能实现
        - [x] 定义数据库Function、Procedure、Trigger、View信息及初始化，用于自动管理数据库实体表之外的数据库对象
        - [x] 定义Localize本地化处理功能，实现可基于Http请求的AcceptLanguages属性获取或设置多语言消息设计
        - [x] 定义EmailSender邮件发送相关接口及默认实现
        - [x] 定义Permissions权限模块的相关接口
        - [x] 实现框架依赖注入服务启动入口，调用各个功能模块（Pack）添加各模块的服务映射
        - [x] 实现ServiceLocator服务定位模式的依赖注入对象的解析
        - [x] 实现雪花算法、自增算法、有序GUID算法等非数据库处理的主键生成逻辑
    - [x] EaCloud.AspNetCore
        - [x] AspNet
            - [x] 实现框架启动入口`app.UseEaCloud()`，调用Pack模块管理器`EaCloudPackManager`启动各个功能模块（PackBase）
            - [x] 实现基于当前请求的ServiceLocator的Scoped对象的解析
            - [x] 实现Localize本地化LocalizeHandler本地化处理程序的实例化，实现后方能正常使用本地化功能
            - [x] 实现图形验证码的相关处理功能
            - [x] 实现JSON请求的404处理中间件
            - [x] 实现JSON请求的异常信息到JSON操作结果与异常日志记录中间件
        - [x] MVC
              - [x] 添加Api专用控制器基类`ApiControllerBase`,`AreaApiControllerBase`,`ControllerBase`
              - [x] 实现MVC功能点处理器
              - [x] 实现MVC业务模块处理器
              - [x] 定义Cors跨源资源共享服务
              - [x] 定义Kestrel宿主配置处理，可通过在启动程序Program.cs --> CreateHostBuilder 方法中设置 Host.CreateDefaultBuilder(args).ConfigureWebHostDefaults --> webBuilder.ConfigureKestrel 中 加入 options.SetHost(); 实现自宿主的相关参数设置
              - [x] 实现基于MVC的功能权限AOP拦截验证
              - [x] 实现基于MVC的事务提交AOP拦截提交
        - [x] SignalR
              - [x] 实现基于SignalR Hub处理基本功能（连接、加入组、离开、发送消息、用户身份、缓存、相关事件）
    - [x] EaCloud.AspNetCore.Diagnostics
        - [x] 实现AspNetCore性能诊断功能的封装
    - [x] EaCloud.Authorization.Datas
        - [x] 实现`角色-实体`，`用户-实体`的数据权限配置
        - [x] 实现`角色-实体`，`用户-实体`的数据权限过滤
    - [x] EaCloud.Authorization.Functions
        - [x] 实现功能权限各个业务实体的数据存储
        - [x] 实现在系统初始化时，遍历反射程序集，自动初始化功能点、数据实体、业务模块等信息并持久化到数据库
        - [x] 实现系统初始化时，将功能点，数据实体，角色功能权限等信息缓存到内存中
        - [x] 实现`角色-功能点`，`用户-功能点`的功能权限验证
    - [x] EaCloud.AutoMapper
        - [x] 不同的映射类型，通过实现`Profile`来实现映射注册
        - [x] 实现通过遍历程序集，查找实现了`IMapTuple`接口的`Profile`来自动注册映射策略
        - [x] 定义`MapToAttribute`，`MapFromAttribute`类型，用以标注Mapping的Source与Target类型，使用时在要映射的类型上标注如`[MapTo(typeof(TTarget))]`或`[MapFrom(typeof(TSource))]`特性，框架初始化时自动查找相应的类型进行CreateMap映射注册
    - [x] EaCloud.Baidu
        - [x] Map
            - [x] 实现与百度地图的相关接口交互
    - [x] EaCloud.EntityFrameworkCore
        - [x] 实现运行时上下文类型初始化及自动加载相关实体类型的功能
        - [x] 实现Repository仓储的数据存储功能
        - [x] 实现UnitOfWork的多上下文管理及同DbConnection的上下文事务同步
        - [x] 实现主从结构的数据读写分离
        - [x] 实现可直接执行SQL语句，通过SQL语句返回DataTable或指定实体数据
    - [x] EaCloud.EntityFrameworkCore.Allinone
        - [x] 实现 Cosmos(Azure Cosmos DB 的 SQL API)、Kdbndp(人大金仓)、MySql、Oracle、PostgreSql、Sqlite、SqlServer 类型数据访问功能
    - [x] EaCloud.EntityFrameworkCore.Cosmos
        - [x] 实现 Azure Cosmos DB 的 SQL API 数据访问功能
    - [x] EaCloud.EntityFrameworkCore.Kdbndp
        - [x] 实现EntityFrameworkCore的Kdbndp(人大金仓)数据访问功能
    - [x] EaCloud.EntityFrameworkCore.MySql
        - [x] 实现EntityFrameworkCore的MySql数据访问功能
    - [x] EaCloud.EntityFrameworkCore.Oracle
        - [x] 实现EntityFrameworkCore的Oracle数据访问功能
    - [x] EaCloud.EntityFrameworkCore.PostgreSql
        - [x] 实现EntityFrameworkCore的PostgreSql数据访问功能
    - [x] EaCloud.EntityFrameworkCore.Sqlite
        - [x] 实现EntityFrameworkCore的Sqlite数据访问功能
    - [x] EaCloud.EntityFrameworkCore.SqlServer
        - [x] 实现EntityFrameworkCore的SqlServer数据访问功能
    - [x] EaCloud.Exceptionless
        - [x] 实现基于Exceptionless的分布式日志记录
    - [x] EaCloud.File
        - [x] 实现基于Web的文件资源管理服务，实现文件的上传、下载、删除、版本管理功能
        - [x] 实现数据库存储、物理存储、文件存储服务三种存储方式功能处理
        - [x] 实现物理存储模式下静态资源可通过URL映射
    - [x] EaCloud.Hangfire
        - [x] 实现基于Hangfire的后台定时任务
    - [x] EaCloud.Identity
        - [x] 身份认证Authentication
            - [x] 实现用户Claims提供器`IUserClaimsProvider`
            - [x] Cookie
                - [x] 实现Cookie登录，并刷新在线用户信息
            - [x] JwtBearer
                - [x] 实现 Jwt Token 的构建功能
                - [x] 实现 Jwt Token 的刷新机制
            - [x] OAuth2 
                - [x] 实现 `微信`、`钉钉`、`抖音`、`QQ`、`Microsoft`、`Github` 三方登录功能
        - [x] 身份标识Identity
            - [x] 实现用户数据管理功能，以及 `用户角色`、`用户组织机构` 的绑定管理
            - [x] 实现角色数据管理功能，以及 `用户角色`、`角色组织机构` 的绑定管理
            - [x] 实现组织机构数据树形管理功能，实现用户登录组织及部门，可用于后续的数据权限处理
            - [x] 重写UserStore，RoleStore，使用现有IRepository进行数据存储
            - [x] 实现第三方OAuth2认证系统的整合
            - [x] 在线用户信息缓存系统，实现用户信息刷新
    - [x] EaCloud.Log4Net
        - [x] 实现基于Log4Net的日志处理
    - [x] EaCloud.MiniProfiler
        - [x] 实现基于MiniProfiler的性能监测
    - [x] EaCloud.NLog
        - [x] 实现基于NLog的日志处理
    - [x] EaCloud.Redis
        - [x] 实现基于Redis客户端的缓存处理
    - [x] EaCloud.Report
        - [x] 实现基于 FastReport.OpenSource 的报表处理功能
    - [x] EaCloud.SMS
        - [x] 实现验证码短信管理功能
        - [x] 实现基于阿里云平台的短信发送、签名管理、模板管理
        - [x] 实现基于逸峰信盈通平台的短信发送、短信查询
    - [x] EaCloud.Swagger
        - [x] 实现基于Swagger的API自动生成同步的在线文档功能
    - [x] EaCloud.Workflow
        - [x] 工作流组件，基于BPMN模型，实现办公自动化、文件审批、业务单据、请假报销等场景的流程逻辑


## 交流

| <img src="https://eacloud_docs.sanqing.tech/images/QQ_863605868_256px.png" alt=" QQ" width="256px" height="256px" /> | <img src="https://eacloud_docs.sanqing.tech/images/Wechat_SeonHu_256px.png" alt=" WeChat" width="256px" height="256px" /> |
| :-: | :-: |
| QQ群号：863605868 | 微信号：SeonHu |
