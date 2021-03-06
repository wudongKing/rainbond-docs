---
title: 功能列表
describe: Rainbond功能列表
weight: 204
---

{{% button href="/quick-start/roadmap/" %}}开发计划{{% /button %}}
{{% button href="/quick-start/release-cycle/" %}}发布周期{{% /button %}}

本文档列举`Rainbond开源版`具备的重点基础功能，随着版本升级本文档列举不一定完全，如有疑问请于社区留言咨询。

#### 应用的部署

| 功能                   | 功能描述                                                     |
| ---------------------- | ------------------------------------------------------------ |
| 支持源代码持续构建     | 支持PHP源码编译，支持PHP源代码、PHP5.3~7版本运行时，apace、nginx构建应用，并支持流行的PHP开发框架 |
|                        | 支持Java源码编译，支持Java（maven）源代码、war包、jar包构建应用，并支持流行的java开发框架 |
|                        | 支持Python源码编译，支持Python源代码、Python 2.6~3.2运行时构建应用，并支持流行的Python开发框架 |
|                        | 支持Node.js源码编译，支持Node.js源代码、Nods.js 6.x~10.x运行时构建应用，流行的Node.js开发框架，包括前端类项目。 |
|                        | 支持Golang源码编译、Golang 1.8.x，1.9.x运行时构建应用，并支持流行的Golang开发框架 |
|                        | 支持dotnet源码编译、支持选择多个版本的编译和运行环境（.netcore linux运行） |
|                        | 支持Dockerfile识别和构建，支持Dockerfile源码的方式构建应用   |
|                        | 支持Helm Chart源码识别和构建（TODO）                         |
|                        |                                                              |
| Docker镜像持续构建     | 支持基于DockerRun命令识别服务运行方式构建服务组件            |
|                        | 支持解析DockerCompose文件识别服务运行方式批量构建服务组件    |
|                        | 支持从私有镜像仓库、公有镜像仓库获取Docker镜像               |
|                        | 支持镜像仓库Webhook服务的持续部署与发布                      |
|                        |                                                              |
| 支持集成Git源码仓库    | 分租户的代码仓库管理，针对不同的团队隔离代码仓库             |
|                        | 支持GitWebhook自动回调功能，实现应用的持续部署与发布         |
|                        | 支持代码分支、tag部署，支持使用不同的代码分支、tag构建应用   |
|                        |                                                              |
| 支持集成Svn源码仓库    | 支持从Svn代码仓库获取源码，支持账户授权和子目录构建          |
|                        |                                                              |
| 支持Windows应用创建    | 支持基于Dockerfile、镜像创建Windows类服务（.net或mfc架构传统应用）（TODO） |
|                        |                                                              |
| 支持第三方服务集成管理 | 支持管理运行于Rainbond集群外的服务，并与Rainbond应用网关和ServiceMesh网络无缝集成。 |
|                        |                                                              |
| 支持应用12要素原则     | 平台遵循或兼容PaaS平台应用的[12要素原则](https://12factor.net/zh_cn/) |
|                        |                                                              |
| 一键部署及回滚         | 实时显示部署及回滚过程，应用的部署与回滚过程要实时可见，方便排查问题 |
|                        | 版本构建历史可追溯，显示版本详细信息，要可以追溯到应用的各个部署版本及详细的部署信息，包括代码提交信息，操作人员等 |
|                        | 支持自动不间断滚动升级，应用部署，升级过程中不能影响现有业务，提供不间断业务的升级机制 |
|                        | 支持一键回滚，支持应用的快速回滚，且不应影响现有业务         |
|                        |                                                              |
| 支持自定义的pipeline   | 支持基于API 对接Jenkins Pipeline, Jenkins处理完成后由Rainbond完成后续CI/CD流程 |
|                        |                                                              |

#### 服务管理与运维
| 功能               | 功能描述                                                     |
| ------------------ | ------------------------------------------------------------ |
| 服务生命周期管理   | 支持对服务的启动、停止、更新、升级、持续构建管理             |
|                    | 支持无状态应用的滚动升级，升级过程不影响业务                 |
|                    | 支持有状态应用的滚动升级，集群服务升级过程不影响业务         |
|                    | 支持基于应用市场的服务升级策略                               |
|                    | 支持针对应用操作的严格的权限管理机制与审计机制               |
|                    |                                                              |
| 服务配置管理       | 支持基于环境变量的服务配置管理                               |
|                    | 直接基于动态配置文件的服务配置管理                           |
|                    | 支持基于动态注入的连接信息配置管理                           |
|                    |                                                              |
| 服务构建源管理     | 支持持续调整服务构建源设置                                   |
|                    | 支持设置服务源码构建参数，根据不同的语言设置Runtime版本，编译参数等 |
|                    |                                                              |
| 服务日志管理       | 支持实时应用级汇总，存储，分割和实时展示，能实时显示应用的日志、汇总分析日志、日志存储与下载功能 |
|                    | 支持基于插件对接ELK等日志分析服务，能够对接业界流行的日志分析工具，如ELK进行展示与分析 |
|                    |                                                              |
| 服务伸缩管理       | 支持不中断服务的的水平伸缩和垂直伸缩操作，平台应用应具备生产级（不中断业务）水平与垂直伸缩服务的能力 |
|                    | 支持基于业务级分析指标的自动伸缩策略，平台具备根据业务分析指标来达到自动伸缩服务的能力（TODO） |
|                    |                                                              |
| 服务高可用保证     | 支持便捷部署高可用分布式服务，将数据与计算分离，网关与计算分离。 |
|                    | 赋予大多数Web服务分布式部署能力                              |
|                    |                                                              |
| 服务性能分析与监控 | 支持常用应用协议的实时性能（响应时间和吞吐率）分析，支持常用应用协议，如HTTP、TCP、MYSQL的实时性能分析，如响应时间，吞吐率等功能 |
|                    | 支持请求Top实时展示，应用的性能分析以列表的形式展示，并能将影响性能最大的URL/SQL语句进行排序 |
|                    | 支持历史分析数据查询，应用的性能分析日志支持按小时与日期进行查询 |
|                    | 支持服务实例实时状态展示和 实例内存实时状态展示和监控        |
|                    |                                                              |
| 服务健康检测       | 支持基于多种策略的应用健康检测，平台对运行的不同协议类型的应用进行实时的监控检查 |
|                    | 支持不健康应用实例的自动下线，针对异常的应用，支持配置不同的处理策略 |
|                    |                                                              |
| 服务管理终端       | 支持基于web的终端管理，平台应用具备web 控制台功能，方便开发人员登录应用内部临时调试程序。 |
|                    | 支持基于命令行的终端管理，平台应支持命令行的方式进行管理，如创建应用，启/停应用，扩容应用等操作 |

#### 应用管理

| 功能               | 功能描述                                                     |
| ------------------ | ------------------------------------------------------------ |
| 应用级生命周期管理 | 支持应用级启动、停止、构建、升级操作                         |
|                    | 支持动态维护应用内部服务直接依赖关系                         |
|                    |                                                              |
| 拓扑图可视化       | 全局业务拓扑实时状态展示，能实时显示业务组的连接（网络）拓补图展示功能 |
|                    | 支持可视化编辑服务服务注册和服务发现                         |
|                    | 支持拓扑流量实时展示，具备拓扑图的流量监控及监控状态显示功能 |
|                    |                                                              |
| 应用备份与恢复     | 支持应用级整体全量备份                                       |
|                    | 支持备份跨租户、跨数据中心迁移和恢复                         |
|                    | 支持备份数据的导入和导出                                     |
|                    |                                                              |
| 应用分享           | 支持应用分享到企业或团队内部市场或企业公有云市场             |
|                    |                                                              |
| 应用升级           | 基于应用市场的应用自动化升级和回滚                           |

#### 应用网关管理

| 功能                | 功能描述                                                     |
| ------------------- | ------------------------------------------------------------ |
| HTTP应用访问策略    | 支持基于域名、访问路径、请求头、Cookie的访问路由控制         |
|                     | 支持HTTPs访问策略                                            |
|                     | 支持HTTP与HTTPs共存，HTTP Rewrite HTTPs策略                  |
|                     | 支持泛域名策略                                               |
|                     | 自定义负载均衡算法，支持轮询算法，一致性Hash算法，Session粘连算法 |
|                     |                                                              |
| TCP/UDP应用访问策略 | 默认支持基于IP+端口的TCP\UDP访问策略管理                     |
|                     | 支持内网IP和外网IP隔离的访问策略                             |
|                     |                                                              |
| TLS证书管理         | 支持导入第三方签发的TLS证书                                  |
|                     | 支持证书的状态监控和管理                                     |
|                     | 支持自动签发TLS证书（TODO）                                  |
|                     |                                                              |
| 虚拟IP池管理        | 支持集群虚拟IP资源池管理（TODO）                             |
|                     |                                                              |
| 服务测试升级策略    | 支持A/B测试控制                                              |
|                     | 支持灰度发布控制                                             |
|                     |                                                              |
| 服务安全控制        | 插件化支持JWT业务安全认证（5.2版本计划）                     |
|                     | 插件化支持白名单、黑名单控制管理（5.2版本计划）              |
|                     | 插件化支持与第三方Auth2.0认证体系对接（5.2版本计划）         |
|                     | 插件化支持WAF防火墙（5.2版本计划）                           |
|                     |                                                              |
| 网关监控            | 对接Prometheus监控域名、服务的实时访问数据                   |
|                     | 监控网关运行的实时数据                                       |
| 服务访问日志管理    | 支持与第三方日志服务对接，发送服务访问日志到第三方平台（5.2版本计划） |



#### 应用插件的管理与设计

| 功能                           | 功能描述                                                     |
| ------------------------------ | ------------------------------------------------------------ |
| 具备完善的应用高级功能扩展架构 | 服务除本身功能以外可以无侵入的扩展其他高级功能，例如防火墙，日志处理，性能分析，网络治理等，建立标准的应用插件体系规范非常关键。插件是独立存在，与应用绑定运行的程序，与应用具有相同的运行环境，可以定义插件独有的配置信息。 |
|                                | 具备插件与应用协同工作的基础运行环境，例如提供服务发现，配置发现，环境配置等。 |
|                                | 具有完善的应用插件开发，部署流程，与应用可以便捷的绑定。能够自助完成应用插件设计 |
|                                |                                                              |
| 应用插件支持标准化传播共享     | 应用插件具备标准化传播能力，可以单独或与应用绑定分享到应用市场 |
|                                | 支持从应用市场安装和使用插件                                 |
|                                |                                                              |
| 提供常用的应用插件             | 提供生产可用的插件用例，例如日志分析、MySQL数据备份、应用性能分析、网络治理等。 |

#### 微服务架构

| 功能                         | 功能描述                                                     |
| ---------------------------- | ------------------------------------------------------------ |
| 提供Service Mesh架构支持     | 支持跨语言和跨协议服务调用                                   |
|                              | 支持多种Service Mesh框架实现（envoy、linkerd等），针对不同场景可实时替换 |
|                              | 支持服务自动注册和发现                                       |
|                              | 支持透明的负载均衡，服务可以随时伸缩                         |
|                              | 支持服务治理：高级路由、限流、熔断机制                       |
|                              |                                                              |
| 支持服务拓扑显示             | 通过拓扑图显示服务之间的依赖关系                             |
|                              |                                                              |
| 支持服务动态编排             | 不需要修改配置文件，动态编排服务依赖关系                     |
|                              |                                                              |
| 支持对接其他微服务架构       | 支持对接Dubbo                                                |
|                              | 支持对接Spring cloud                                         |
|                              |                                                              |
| 支持API gateway              | 支持通过插件扩展API gateway的功能                            |
|                              | 支持对接第三方登录，对接Oauth 2.0                            |
|                              | 支持限流和熔断                                               |
|                              | 支持访问控制                                                 |
|                              |                                                              |
| 支持通过插件机制实现服务治理 | 故障处理及恢复，熔断/限流                                    |
|                              | 传输加密                                                     |
|                              | 网络策略管理                                                 |
|                              | 性能分析                                                     |
|                              | 支持tracing                                                  |
|                              | 支持内部服务A/B测试和灰度发布                                |
|                              | 支持基于域名/Path/header的业务路由                           |

#### 应用市场管理

| 功能                 | 功能描述                                                     | 说明 |
| -------------------- | ------------------------------------------------------------ | ---- |
| 应用发布和安装和升级 | 支持自助发布一组服务到应用市场，包括程序，环境与配置，数据，拓扑关系，插件扩展。 |      |
|                      | 用户可以在应用市场一键安装，不需要懂技术                     |      |
|                      | 支持跨数据中心发布应用和安装应用                             |      |
|                      | 发布新版本后，应用可以一键升级                               |      |
|                      |                                                              |      |
| 在线和离线的应用交付 | 支持应用市场间应用同步                                       |      |
|                      | 支持应用导出安装包兼容 docker-compose。                      |      |
|                      | 支持应用离线导入与导出，导入后可以一键安装使用               |      |
|                      |                                                              |      |
| 应用市场展示功能     | 支持应用多级分类显示，用户可以分类筛选                       |      |
|                      | 支持应用搜索                                                 |      |
|                      | 显示应用名、logo、简介和版本                                 |      |
|                      | 支持应用市场的审核机制                                       |      |
|                      |                                                              |      |
| 多级应用市场         | 支持三级应用市场隔离，发布应用时可选应用可见的粒度。         |      |
|                      | 支持对接公有应用市场，其他应用市场                           |      |

#### 多数据中心管理

见[企业服务支持](https://www.goodrain.com)

#### 系统运维平台

| 功能                     | 功能描述                                                     |
| ------------------------ | ------------------------------------------------------------ |
| 便捷的数据中心安装和升级 | 支持对数据中心内节点进行分类管理，例如分为：负载均衡节点，管理节点，存储节点，计算节点。实现对所有节点的统一管理 |
|                          | 支持多个管理节点的在线，离线安装与升级，例如Kubernetes服务，平台管理服务 |
|                          | 支持计算节点的安装与升级                                     |
|                          | 支持对基础环境，如系统内核、docker、网络、存储的安装和升级   |
|                          |                                                              |
| 节点管理                 | 支持基于命令行的节点管理                                     |
|                          |                                                              |

关于多租户管理，UI可视化运维，监控与报警系统等企业服务功能见[企业服务支持](https://www.goodrain.com)

#### 平台其他功能及技术架构

| 功能                                 | 描述                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| 标准RestfulAPI开放设计，支持二次开发 | 支持应用标准化管理API开放，基于用户授权的安全验证策略        |
|                                      | 平台管理API开放，支持对用户，租户，权限等管理                |
|                                      | 资源管理API开放，支持对集群节点，资源调度情况进行管理        |
|                                      |                                                              |
| 应用与资源解耦合                     | 架构思路上应用不与计算资源绑定，支持根据需要随处迁移         |
|                                      |                                                              |
| 支持多功能命令行工具                 | 命令行工具支持应用的启动，停止，调度，综合状态查询功能       |
|                                      | 命令行工具支持租户查询，批量操作功能                         |
|                                      | 命令行工具支持集群节点管理，资源调度管理                     |
|                                      |                                                              |
| 权限管理                             | 支持在租户级别自定义角色名称，自定义分配权限，用户自定义支持多种角色 |
|                                      | 支持应用级别权限精确控制，可继承租户级别权限                 |
|                                      | 控制权限严格验证，做到API级别安全控制                        |
|                                      |                                                              |
| Overlay网络架构支持                  | 支持多租户网络隔离的Overlay网络模型                          |
|                                      | 支持虚拟机、容器统一的网络资源（IP,路由）自动化分配，虚拟机与容器可以同时组成租户网络 |
|                                      |                                                              |
| 支持多种类型的存储系统对接           | 支持应用级别自助设置多种存储设备对接，包括：分布式文件系统，块设备，内存虚拟存储等 |
|                                      | 支持存储数据的备份，快照与恢复                               |
|                                      |                                                              |
| 应用调度系统                         | 基于Kubernetes的docker容器调度系统，不必要暴露过多的容器技术概念，支持平台级的应用调度参数设置 |
|                                      | 支持自定义调度策略的设置和二次开发                           |
|                                      |                                                              |
| 服务间内部负载均衡                   | 内部服务之间的访问能够自动进行服务发现和负载均衡             |
|                                      | 应用之间的负载均衡功能可插件化扩展，支持高级的服务治理       |



### 更多功能

关于SaaS化应用交付体系、企业级应用市场、企业资源管理平台、企业级监控报警系统以及更多的Rainbond企业级支持见 [企业服务支持](https://www.goodrain.com)

