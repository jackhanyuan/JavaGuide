---
title: Java后端面试重点总结
description: Java后端面试重点总结：梳理校招/社招高频考点与复习优先级，覆盖Java基础、集合、并发、MySQL、Redis、Spring/Spring Boot、JVM与项目经验准备，帮你抓重点高效备战。
category: 面试准备
icon: star
head:
  - - meta
    - name: keywords
      content: Java后端面试,面试重点,八股文,Java基础,Java集合,Java并发,MySQL,Redis,Spring Boot,项目经验
---

<!-- @include: @small-advertisement.snippet.md -->

::: tip 友情提示
本文节选自 **[《Java 面试指北》](../zhuanlan/java-mian-shi-zhi-bei.md)**。这是一份教你如何更高效地准备面试的专栏，内容和 JavaGuide 互补，涵盖常见八股文（系统设计、常见框架、分布式、高并发 ……）、优质面经等内容。
:::

## Java 后端面试哪些知识点是重点？

**准备面试的时候，具体哪些知识点是重点呢？如何把握重点？**

先来一张图（后续会详细解读）：

![Java 后端面试重点](https://oss.javaguide.cn/github/javaguide/interview-preparation/back-end-interview-focus.png)

给你几点靠谱的建议：

1. Java 基础、集合、并发、MySQL、Redis 、Spring、Spring Boot 这些 Java 后端开发必备的知识点（MySQL + Redis >= Java > Spring + Spring Boot）。大厂以及中小厂的面试问的比较多的就是这些知识点。Spring 和 Spring Boot 这俩框架类的知识点相对前面的知识点来说重要性要稍低一些，但一般面试也会问一些，尤其是中小厂。并发知识一般中大厂提问更多也更难，尤其是大厂喜欢深挖底层，很容易把人问倒。计算机基础相关的内容会在下面提到。
2. 你的项目经历涉及到的知识点是重中之重，有水平的面试官都是会根据你的项目经历来问的。举个例子，你的项目经历使用了 Redis 来做限流，那 Redis 相关的八股文（比如 Redis 常见数据结构）以及限流相关的八股文（比如常见的限流算法）你就应该多花更多心思来搞懂吃透！你把项目经历上的知识点吃透之后，再把你简历上哪些写熟练掌握的技术给吃透，最后再去花时间准备其他知识点。
3. 针对自身找工作的需求，你又可以适当地调整复习的重点。像中小厂一般问计算机基础比较少一些，有些大厂比如字节比较重视计算机基础尤其是算法。这样的话，如果你的目标是中小厂的话，计算机基础就准备面试来说不是那么重要了。如果复习时间不够的话，可以暂时先放放，腾出时间给其他重要的知识点。
4. 一般校招的面试不会强制要求你会分布式/微服务、高并发的知识（不排除个别岗位有这方面的硬性要求），所以到底要不要掌握还是要看你个人当前的实际情况。如果你会这方面的知识的话，对面试相对来说还是会更有利一些（想要让项目经历有亮点，还是得会一些性能优化的知识。性能优化的知识这也算是高并发知识的一个小分支了）。如果你的技能介绍或者项目经历涉及到分布式/微服务、高并发的知识，那建议你尽量也要抽时间去认真准备一下，面试中很可能会被问到，尤其是项目经历用到的时候。不过，也还是主要准备写在简历上的那些知识点就好。
5. JVM 相关的知识点，一般是大厂（例如美团、阿里）和一些不错的中厂（例如携程、顺丰、招银网络）才会问到，面试国企、差一点的中厂和小厂就没必要准备了。JVM 面试中比较常问的是 [Java 内存区域](https://javaguide.cn/java/jvm/memory-area.html)、[JVM 垃圾回收](https://javaguide.cn/java/jvm/jvm-garbage-collection.html)、[类加载器和双亲委派模型](https://javaguide.cn/java/jvm/classloader.html) 以及 JVM 调优和问题排查（我之前分享过一些[常见的线上问题案例](https://t.zsxq.com/0bsAac47U)，里面就有 JVM 相关的）。
6. 不同的大厂面试侧重点也会不同。比如说你要去阿里这种公司的话，项目和八股文就是重点，阿里笔试一般会有代码题，进入面试后就很少问代码题了，但是对原理性的问题问的比较深，经常会问一些你对技术的思考。再比如说你要面试字节这种公司，那计算机基础，尤其是算法是重点，字节的面试十分注重代码功底，有时候开始面试就会直接甩给你一道代码题，写出来再谈别的。也会问面试八股文，以及项目，不过，相对来说要少很多。
7. 多去找一些面经看看，尤其你目标公司或者类似公司对应岗位的面经。这样可以实现针对性的复习，还能顺便自测一波，检查一下自己的掌握情况。

看似 Java 后端八股文很多，实际把复习范围一缩小，重要的东西就是那些。考虑到时间问题，你不可能连一些比较冷门的知识点也给准备了。这没必要，主要精力先放在那些重要的知识点即可。

## 如何更高效地准备八股文？

<img src="https://oss.javaguide.cn/github/javaguide/interview-preparation/preparation-for%20eight-part%20essay.png" style="zoom:50%;" />

对于技术八股文来说，尽量不要死记硬背，这种方式非常枯燥且对自身能力提升有限！但是！想要一点不背是不太现实的，只是说要结合实际应用场景和实战来理解记忆。

我一直觉得面试八股文最好是和实际应用场景和实战相结合。很多同学现在的方向都错了，上来就是直接背八股文，硬生生学成了文科，那当然无趣了。

举个例子：你的项目中需要用到 Redis 来做缓存，你对照着官网简单了解并实践了简单使用 Redis 之后，你去看了 Redis 对应的八股文。你发现 Redis 可以用来做限流、分布式锁，于是你去在项目中实践了一下并掌握了对应的八股文。紧接着，你又发现 Redis 内存不够用的情况下，还能使用 Redis Cluster 来解决，于是你就又去实践了一下并掌握了对应的八股文。

**一定要记住你的主要目标是理解和记关键词，而不是像背课文一样一字一句地记下来，这样毫无意义！效率最低，对自身帮助也最小！**

还要注意适当“投机取巧”，不要单纯死记八股，有些技术方案的实现有很多种，例如分布式 ID、分布式锁、幂等设计，想要完全记住所有方案不太现实，你就重点记忆你项目的实现方案以及选择该种实现方案的原因就好了。当然，其他方案还是建议你简单了解一下，不然也没办法和你选择的方案进行对比。

想要检测自己是否搞懂或者加深印象，记录博客或者用自己的理解把对应的知识点讲给别人听也是一个不错的选择。

另外，准备八股文的过程中，强烈建议你花个几个小时去根据你的简历（主要是项目经历部分）思考一下哪些地方可能被深挖，然后把你自己的思考以面试问题的形式体现出来。面试之后，你还要根据当下的面试情况复盘一波，对之前自己整理的面试问题进行完善补充。这个过程对于个人进一步熟悉自己的简历（尤其是项目经历）部分，非常非常有用。这些问题你也一定要多花一些时间搞懂吃透，能够流畅地表达出来。面试问题可以参考 [Java 面试常见问题总结（2024 最新版）](https://t.zsxq.com/0eRq7EJPy)，记得根据自己项目经历去深入拓展即可！

最后，准备技术面试的同学一定要定期复习（自测的方式非常好），不然确实会遗忘的。

## 详细面试准备计划

以下计划按**「项目经历 → 简历技术 → MySQL/Redis/Java → 框架 → 系统设计与场景题 → 计算机基础 → 分布式/高并发 → JVM」**的优先级编排，每阶段都对应到本站具体文章，便于按图索骥。

建议总周期 **4～8 周**，可根据目标公司（中小厂 / 大厂）和基础情况压缩或拉长。

### 计划总览

| 阶段                          | 建议时长              | 核心产出                            | 自测建议                               |
| ----------------------------- | --------------------- | ----------------------------------- | -------------------------------------- |
| 第 0 步 前期准备              | 1～2 天               | 简历定稿、复习节奏确定              | 简历能否 30 秒讲清项目                 |
| 第一阶段 项目与简历深挖       | 约 1 周               | 项目卡片、必会题清单、话术稿        | 能脱稿讲清每个项目背景+难点+你的贡献   |
| 第二阶段 Java + MySQL + Redis | 2～3 周               | 八股理解+关键词记忆                 | 根据网站文章自测                       |
| 第三阶段 框架                 | 1～2 周               | Spring/IoC/AOP/事务、设计模式、安全 | 能说清项目里用到的注解与设计思路       |
| 系统设计与场景题              | 按需 0.5～1 周        | 系统设计题、场景题思路与案例        | 能口述 1～2 个经典设计（如短链、秒杀） |
| 第四阶段 计算机基础           | 按需 0.5～2 周        | 计网/OS/数据结构；目标字节等加算法  | 手写经典题、能画 TCP/HTTP 过程         |
| 第五阶段 分布式与高并发       | 按需 1～2 周          | 分布式理论、RPC、MQ、高可用         | 能讲清项目中的分布式方案选型理由       |
| 第六阶段 JVM                  | 大厂/部分中厂 3～5 天 | 内存、GC、类加载、调优排查          | 能结合项目说一次 GC 或 OOM 排查        |
| 面试前冲刺                    | 1～2 天               | 总复习清单、心态稳定                | 过一遍必会题+项目话术                  |

### 第 0 步：前期准备（建议 1～2 天）

在系统刷八股前，先把「怎么准备、怎么写简历、怎么稳住心态」搞定，避免方向跑偏。

| 事项       | 说明                                | 对应文章                                                                                                                                                                                    |
| ---------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 准备方法   | 明确复习节奏、自测方式、时间分配    | [如何高效准备 Java 面试？](https://javaguide.cn/interview-preparation/teach-you-how-to-prepare-for-the-interview-hand-in-hand.html)                                                         |
| 简历       | 一页纸、项目 STAR、技术栈与岗位匹配 | [程序员简历编写指南](https://javaguide.cn/interview-preparation/resume-guide.html)                                                                                                          |
| 学习路线   | 查漏补缺，确定自己当前所处阶段      | [Java 学习路线（最新版，4w+ 字）](https://javaguide.cn/interview-preparation/java-roadmap.html)                                                                                             |
| 项目与经历 | 没有项目/实习时如何包装、怎么讲     | [项目经验指南](https://javaguide.cn/interview-preparation/project-experience-guide.html)、[校招没有实习经历怎么办？](https://javaguide.cn/interview-preparation/internship-experience.html) |
| 心态       | 减少紧张、发挥更稳                  | [面试太紧张怎么办？](https://javaguide.cn/interview-preparation/how-to-handle-interview-nerves.html)                                                                                        |

### 第一阶段：项目与简历深挖（约 1 周）

**目标**：能清晰讲出每个项目的背景、你的角色、技术选型与难点，并能推导出「可能被问的面试题」。

**产出物**：

- **项目卡片**：按简历逐条过项目，为每个项目写清——业务背景、技术栈、你负责的模块、1～2 个难点与解决方式、可量化的成果（如 QPS、耗时、节省成本）。
- **必会题清单**：根据项目用到的技术，列出「必会题」（例如：用了 Redis 限流 → Redis 常见数据结构 + 限流算法；用了 MySQL → 索引、事务、慢 SQL 优化）。可参考 [Java 面试常见问题总结](https://t.zsxq.com/0eRq7EJPy) 按项目拓展。
- **话术稿**：每个项目准备 1～2 分钟版本（自我介绍用）和 3～5 分钟版本（深挖用），能流畅讲出「为什么这么选、遇到什么问题、怎么解决的」。

**每日建议**：每天至少梳理 1 个项目 + 对应必会题，周末做一次脱稿自测（录音或对着镜子讲）。

**自测**：能脱稿讲清每个项目的背景、难点和你的贡献；必会题清单里的题能答出要点。

### 第二阶段：Java 核心 + MySQL + Redis （约 2～3 周）

**优先级**：最重要的部分，面试高频考点，MySQL + Redis ≥ Java 基础/集合/并发 > 框架知识，大厂会深挖并发与底层。

**Java 基础**

- [Java 基础常见面试题总结（上）](https://javaguide.cn/java/basis/java-basic-questions-01.html)、[（中）](https://javaguide.cn/java/basis/java-basic-questions-02.html)、[（下）](https://javaguide.cn/java/basis/java-basic-questions-03.html)：语法与面向对象、字符串与拷贝、异常/泛型/反射/SPI/序列化/注解

**Java 集合**

- [Java 集合常见面试题（上）](https://javaguide.cn/java/collection/java-collection-questions-01.html)、[（下）](https://javaguide.cn/java/collection/java-collection-questions-02.html)：List/Set/Queue、HashMap、ConcurrentHashMap

**Java 并发**（大厂必深挖）

- [Java 并发常见面试题（上）](https://javaguide.cn/java/concurrent/java-concurrent-questions-01.html)、[（中）](https://javaguide.cn/java/concurrent/java-concurrent-questions-02.html)、[（下）](https://javaguide.cn/java/concurrent/java-concurrent-questions-03.html)：线程与锁、synchronized/ReentrantLock、ThreadLocal/线程池/Future/AQS/虚拟线程
- [JMM](https://javaguide.cn/java/concurrent/jmm.html)、[线程池详解](https://javaguide.cn/java/concurrent/java-thread-pool-summary.html)与[最佳实践](https://javaguide.cn/java/concurrent/java-thread-pool-best-practices.html)
- [ThreadLocal](https://javaguide.cn/java/concurrent/threadlocal.html)、[AQS](https://javaguide.cn/java/concurrent/aqs.html)、[CompletableFuture](https://javaguide.cn/java/concurrent/completablefuture-intro.html)、[常见并发容器](https://javaguide.cn/java/concurrent/java-concurrent-collections.html)

**MySQL**（必看）

- [MySQL 常见面试题总结](https://javaguide.cn/database/mysql/mysql-questions-01.html)（基础、引擎、事务、索引、锁、优化）
- [MySQL 索引详解](https://javaguide.cn/database/mysql/mysql-index.html)、[三大日志](https://javaguide.cn/database/mysql/mysql-logs.html)、[事务隔离级别](https://javaguide.cn/database/mysql/transaction-isolation-level.html)
- [InnoDB 对 MVCC 的实现](https://javaguide.cn/database/mysql/innodb-implementation-of-mvcc.html)、[SQL 执行过程](https://javaguide.cn/database/mysql/how-sql-executed-in-mysql.html)

**Redis**（必看）

- [Redis 常见面试题总结（上）](https://javaguide.cn/database/redis/redis-questions-01.html)、[Redis 常见面试题总结（下）](https://javaguide.cn/database/redis/redis-questions-02.html)
- [Redis 延时任务](https://javaguide.cn/database/redis/redis-delayed-task.html)、[Redis 做消息队列](https://javaguide.cn/database/redis/redis-stream-mq.html)
- [5 种基本数据类型](https://javaguide.cn/database/redis/redis-data-structures-01.html)、[3 种特殊类型](https://javaguide.cn/database/redis/redis-data-structures-02.html)、[跳表实现有序集合](https://javaguide.cn/database/redis/redis-skiplist.html)
- [持久化](https://javaguide.cn/database/redis/redis-persistence.html)、[内存碎片](https://javaguide.cn/database/redis/redis-memory-fragmentation.html)、[常见阻塞原因](https://javaguide.cn/database/redis/redis-common-blocking-problems-summary.html)

### 第三阶段：框架（约 1～2 周）

**设计模式**

- [设计模式常见面试题总结](https://interview.javaguide.cn/system-design/design-pattern.html)

**Spring / Spring Boot**

- [Spring 常见面试题](https://javaguide.cn/system-design/framework/spring/spring-knowledge-and-questions-summary.html)、[SpringBoot 常见面试题](https://javaguide.cn/system-design/framework/spring/springboot-knowledge-and-questions-summary.html)
- [常用注解](https://javaguide.cn/system-design/framework/spring/spring-common-annotations.html)、[IoC 与 AOP](https://javaguide.cn/system-design/framework/spring/ioc-and-aop.html)、[Spring 事务](https://javaguide.cn/system-design/framework/spring/spring-transaction.html)
- [Spring 中的设计模式](https://javaguide.cn/system-design/framework/spring/spring-design-patterns-summary.html)、[SpringBoot 自动装配](https://javaguide.cn/system-design/framework/spring/spring-boot-auto-assembly-principles.html)、[Async 原理](https://javaguide.cn/system-design/framework/spring/async.html)
- [MyBatis 常见面试题](https://javaguide.cn/system-design/framework/mybatis/mybatis-interview.html)、[Netty 常见面试题](https://javaguide.cn/system-design/framework/netty.html)

**自测**：能说清项目里用到的 Spring 注解、IoC/AOP 在项目中的体现、事务失效场景；设计模式能举出项目或框架中的例子。

**权限与安全**

- [认证授权基础](https://javaguide.cn/system-design/security/basis-of-authority-certification.html)、[JWT](https://javaguide.cn/system-design/security/jwt-intro.html) 与[优缺点](https://javaguide.cn/system-design/security/advantages-and-disadvantages-of-jwt.html)、[权限系统设计](https://javaguide.cn/system-design/security/design-of-authority-system.html)、[SSO](https://javaguide.cn/system-design/security/sso-intro.html)、[常见加密算法](https://javaguide.cn/system-design/security/encryption-algorithms.html)

### 系统设计与场景题（建议放在框架之后）

面试官常会穿插一两道系统设计或场景题，考察整体思路和方案权衡。本模块与「框架」分开，便于单独安排时间刷题与总结。

- **系统设计 / 场景题汇总**：[系统设计常见面试题总结](https://javaguide.cn/system-design/system-design-questions.html)（付费内容在 [《后端面试高频系统设计&场景题》](https://javaguide.cn/zhuanlan/back-end-interview-high-frequency-system-design-and-scenario-questions.html) 专栏，含短链、秒杀、海量数据处理等 30+ 道）。
- **本站可参考的设计类文章**（思路可迁移到面试口述）：[定时任务](https://javaguide.cn/system-design/schedule-task.html)、[Web 实时消息推送](https://javaguide.cn/system-design/web-real-time-message-push.html)。

**自测**：能口述 1～2 个经典系统设计（如短链、秒杀、限流）的整体思路与关键取舍；场景题（如海量数据去重、第三方登录）能说出常见方案。

### 第四阶段：计算机基础（按目标公司安排）

**目标字节等重算法/基础的厂**：适当多留时间，算法与代码题要单独刷（LeetCode 热题、剑指 Offer、手写常见数据结构）；**目标中小厂**：可压缩或后置。

- **算法与代码题**（面字节、快手等必留时间）：[剑指 Offer 题解](https://javaguide.cn/cs-basics/algorithms/the-sword-refers-to-offer.html)、LeetCode 热题 100、常见手写（如 LRU、生产者消费者、单例等）。建议每天至少 1 道，保持手感。
- **网络**：[计网常见面试题（上）](https://javaguide.cn/cs-basics/network/other-network-questions.html)、[（下）](https://javaguide.cn/cs-basics/network/other-network-questions2.html)、[访问网页全过程](https://javaguide.cn/cs-basics/network/the-whole-process-of-accessing-web-pages.html)、[应用层常见协议](https://javaguide.cn/cs-basics/network/application-layer-protocol.html)、[HTTP/HTTPS](https://javaguide.cn/cs-basics/network/http-vs-https.html)、[HTTP 1.0 vs 1.1](https://javaguide.cn/cs-basics/network/http1.0-vs-http1.1.html)、[DNS](https://javaguide.cn/cs-basics/network/dns.html)、[TCP 三次握手与四次挥手](https://javaguide.cn/cs-basics/network/tcp-connection-and-disconnection.html)、[TCP 可靠性](https://javaguide.cn/cs-basics/network/tcp-reliability-guarantee.html)、[ARP](https://javaguide.cn/cs-basics/network/arp.html)
- **操作系统**：[操作系统常见面试题（上）](https://javaguide.cn/cs-basics/operating-system/operating-system-basic-questions-01.html)、[（下）](https://javaguide.cn/cs-basics/operating-system/operating-system-basic-questions-02.html)、[Linux 基础](https://javaguide.cn/cs-basics/operating-system/linux-intro.html)
- **数据结构**：[数组/链表/栈/队列](https://javaguide.cn/cs-basics/data-structure/linear-data-structure.html)、[图](https://javaguide.cn/cs-basics/data-structure/graph.html)、[堆](https://javaguide.cn/cs-basics/data-structure/heap.html)、[树](https://javaguide.cn/cs-basics/data-structure/tree.html)、[红黑树](https://javaguide.cn/cs-basics/data-structure/red-black-tree.html)、[布隆过滤器](https://javaguide.cn/cs-basics/data-structure/bloom-filter.html)

**自测**：能画访问网页全过程、TCP 握手挥手；算法题能手写常见套路；OS 进程/线程、内存、死锁能说清概念与例子。

### 第五阶段：分布式与高并发（按简历与岗位）

若简历或岗位涉及分布式/微服务/高并发，再系统过一遍；否则可只过「项目会用到的点」。

- **分布式理论**：[CAP 与 BASE](https://javaguide.cn/distributed-system/protocol/cap-and-base-theorem.html)、[Paxos](https://javaguide.cn/distributed-system/protocol/paxos-algorithm.html)、[Raft](https://javaguide.cn/distributed-system/protocol/raft-algorithm.html)、[Gossip](https://javaguide.cn/distributed-system/protocol/gossip-protocol.html)、[一致性哈希](https://javaguide.cn/distributed-system/protocol/consistent-hashing.html)
- **RPC**：[RPC 基础](https://javaguide.cn/distributed-system/rpc/rpc-intro.html)、[Dubbo](https://javaguide.cn/distributed-system/rpc/dubbo.html)
- **分布式 ID / 网关 / 锁**：[分布式 ID](https://javaguide.cn/distributed-system/distributed-id.html)、[设计指南](https://javaguide.cn/distributed-system/distributed-id-design.html)、[API 网关](https://javaguide.cn/distributed-system/api-gateway.html)、[Spring Cloud Gateway](https://javaguide.cn/distributed-system/spring-cloud-gateway-questions.html)、[分布式锁](https://javaguide.cn/distributed-system/distributed-lock.html)、[实现方案](https://javaguide.cn/distributed-system/distributed-lock-implementations.html)
- **高并发与 MQ**：[CDN](https://javaguide.cn/high-performance/cdn.html)、[读写分离与分库分表](https://javaguide.cn/high-performance/read-and-write-separation-and-library-subtable.html)、[冷热分离](https://javaguide.cn/high-performance/data-cold-hot-separation.html)、[SQL 优化](https://javaguide.cn/high-performance/sql-optimization.html)、[深度分页](https://javaguide.cn/high-performance/deep-pagination-optimization.html)、[负载均衡](https://javaguide.cn/high-performance/load-balancing.html)
- **高可用**（项目涉及再重点看）：[高可用系统设计](https://javaguide.cn/high-availability/high-availability-system-design.html)、[限流](https://javaguide.cn/high-availability/limit-request.html)、[熔断与降级](https://javaguide.cn/high-availability/fallback-and-circuit-breaker.html)、[超时与重试](https://javaguide.cn/high-availability/timeout-and-retry.html)、[幂等设计](https://javaguide.cn/high-availability/idempotency.html)、[冗余设计](https://javaguide.cn/high-availability/redundancy.html)
- **消息队列**：[MQ 基础](https://javaguide.cn/high-performance/message-queue/message-queue.html)、[Disruptor](https://javaguide.cn/high-performance/message-queue/disruptor-questions.html)、[RabbitMQ](https://javaguide.cn/high-performance/message-queue/rabbitmq-questions.html)、[RocketMQ](https://javaguide.cn/high-performance/message-queue/rocketmq-questions.html)、[Kafka](https://javaguide.cn/high-performance/message-queue/kafka-questions-01.html)

**自测**：能讲清项目里用到的分布式方案（如分布式锁、ID、MQ）及选型理由；CAP/BASE、一致性哈希等能举例说明。

### 第六阶段：JVM（大厂 / 部分中厂）

目标阿里、美团、携程、顺丰、招银等可重点看；面国企或小厂可跳过。

- [Java 内存区域](https://javaguide.cn/java/jvm/memory-area.html)、[JVM 垃圾回收](https://javaguide.cn/java/jvm/jvm-garbage-collection.html)
- [类文件结构](https://javaguide.cn/java/jvm/class-file-structure.html)、[类加载过程](https://javaguide.cn/java/jvm/class-loading-process.html)、[类加载器](https://javaguide.cn/java/jvm/classloader.html)
- 结合 [常见线上问题案例](https://t.zsxq.com/0bsAac47U) 理解调优与排查

**自测**：能说清内存区域、常见 GC 器与回收过程、类加载与双亲委派；能结合项目或案例讲一次 GC 调优或 OOM 排查思路。

**Java 新特性**（按岗位要求选读）：[Java 11](https://javaguide.cn/java/new-features/java11.html)、[Java 17](https://javaguide.cn/java/new-features/java17.html)、[Java 21](https://javaguide.cn/java/new-features/java21.html)

### 面试前 1～2 天冲刺清单

临近面试时优先做这几件事，避免临时抱佛脚方向散乱：

| 事项              | 说明                                                                                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 过一遍必会题      | 重点看你第一阶段整理的「项目相关必会题」+ 简历上写的「熟练掌握」对应的考点，能口头复述要点即可。                                                        |
| 练一遍项目话术    | 每个项目 1 分钟版、3 分钟版各讲一遍，卡壳的地方记下来再顺一遍。                                                                                         |
| 目标公司/岗位倾向 | 翻一下该公司或同类型岗位的面经，看有没有偏重（如算法、计网、项目深挖），针对性过一眼。                                                                  |
| 心态与状态        | 早睡、准备好设备（线上面试）或路线（现场），可看 [面试太紧张怎么办？](https://javaguide.cn/interview-preparation/how-to-handle-interview-nerves.html)。 |

面试结束后建议做一次简短复盘：哪些题答得不好、哪些没准备到，补充进必会题清单，下一场前重点过一遍。
