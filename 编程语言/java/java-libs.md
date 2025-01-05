# Java

## 命令行解析工具

| 库             | 描述                                            | 地址                                                 | 推荐指数               |
| ------------- | --------------------------------------------- | -------------------------------------------------- | ------------------ |
| `jcommander`  | Command line parsing framework for Java       | [Link](https://github.com/cbeust/jcommander)       | :star::star::star: |
| `jopt-simple` | Java library for parsing command line options | [Link](https://github.com/jopt-simple/jopt-simple) | :star::star:       |
|               |                                               |                                                    |                    |

更多解析工具,参考:[Command Parser](https://jopt-simple.github.io/jopt-simple/)

## 字节码编辑工具

| 库           | 描述                                                    | 地址                                          | 推荐指数               |
| ----------- | ----------------------------------------------------- | ------------------------------------------- | ------------------ |
| `bytebuddy` | Runtime code generation for the Java virtual machine. | [Link](https://github.com/raphw/byte-buddy) | :star::star::star: |
| `javapoet`  | `.java`文件生成工具(**生成源码**)                               | [Link](https://github.com/square/javapoet)  | :star::star::star: |
|             |                                                       |                                             |                    |

## 测试库

| 库                | 描述      | 地址                                                            | 推荐指数               |
| ---------------- | ------- | ------------------------------------------------------------- | ------------------ |
| `Jacoco`         | 单元测试覆盖率 | [Link](https://github.com/jacoco/jacoco)                      | :star::star::star: |
| `Testcontainers` | 容器测试    | [Link](https://github.com/testcontainers/testcontainers-java) | :star::star::star: |
|                  |         |                                                               |                    |

## 缓存库

| 库          | 描述                                          | 地址                                            | 推荐指数               |
| ---------- | ------------------------------------------- | --------------------------------------------- | ------------------ |
| `Caffeine` | A high performance caching library for Java | [Link](https://github.com/ben-manes/caffeine) | :star::star::star: |
|            |                                             |                                               |                    |

## 序列化框架

| 库      | 描述                                                                                    | 地址                                     | 推荐指数               |
| ------ | ------------------------------------------------------------------------------------- | -------------------------------------- | ------------------ |
| `fury` | A blazingly fast multi-language serialization framework powered by JIT and zero-copy. | [Link](https://github.com/apache/fury) | :star::star::star: |
|        |                                                                                       |                                        |                    |

## 工具库

| 库              | 描述                                                                       | 地址                                                   | 推荐指数               |
| -------------- | ------------------------------------------------------------------------ | ---------------------------------------------------- | ------------------ |
| `resilience4j` | Fault tolerance library designed for functional programming.             | [Link](https://github.com/resilience4j/resilience4j) | :star::star::star: |
| `JsonPath`     | Java JsonPath implementation. 可以通过此种方式访问json对象,例:`$.store.book[0].title` | [Link](https://github.com/json-path/JsonPath)        | :star::star::star: |
| `archaius`     | Library for configuration management API                                 | [Link](https://github.com/Netflix/archaius)          | :star::star::star: |
| `MyExcel`      | 是一个集导入、导出、加密Excel等多项功能的工具包。                                              | [Link](https://github.com/liaochong/myexcel)         | :star::star::star: |
| `OSHI`         | Native Operating System and Hardware Information.                        | [Link](https://github.com/oshi/oshi)                 | :star::star::star: |
| mustache       | 模版引擎.本身也是一套规范,已有**多语言**实现,                                               | [Link](https://mustache.github.io/)                  | :star::star::star: |
| `hutool`       | Hutool是一个功能丰富且易用的Java工具库                                                 | [Link](https://github.com/dromara/hutool)            | :star::star::star: |
| `japicmp`      | japicmp is a tool to compare two versions of a jar archive.              | [Link](https://github.com/siom79/japicmp)            | :star::star:       |
| `arthas`       | Alibaba Java诊断利器Arthas                                                   | [Link](https://github.com/alibaba/arthas)            | :star::star::star: |
| `JSch`         | JSch is a pure Java implementation of SSH2.                              | [Link](http://www.jcraft.com/jsch/)                  | :star::star::star: |

## 维护状态工具

| 库             | 描述                                            | 地址                                             | 备注             |
| ------------- | --------------------------------------------- | ---------------------------------------------- | -------------- |
| `vavr`        | Vavr *core* is a functional library for Java. | [Link](https://github.com/vavr-io/vavr)        | 作者寻找新维护人员中     |
| `reflections` | Java runtime metadata analysis                | [Link](https://github.com/ronmamo/reflections) | 项目维护不活跃,**慎用** |
|               |                                               |                                                |                |

- # 



# 待学习

| 库              | 描述                                                                                                                                                                                                                                                          | 地址                                                                |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `JavaFX`       | JavaFX is an open source, next generation client application platform for desktop, mobile and embedded systems built on Java.  <br/> `gluonhq/substrate`:Create native Java(FX) apps for desktop, mobile and embedded                                       | [Link](https://openjfx.io/)                                       |
| `Java JNA`     | Java Native Access                                                                                                                                                                                                                                          | [Link](https://github.com/java-native-access/jna)                 |
| `drools`       | 规则引擎(工具复杂度高,需**重点关注**)                                                                                                                                                                                                                                      | [Link](https://github.com/apache/incubator-kie-drools)            |
| `GraphQL`      | GraphQL是一个开源的，面向API而创造出来的数据查询操作语言以及相应的运行环境.GraphQL本身是一个规范,每种语言都有其对应实现.                                                                                                                                                                                      | [Link](https://github.com/graphql-java/graphql-java)              |
| `HATEOAS`      | HATEOAS（Hypermedia as the Engine of Application State）是一种REST架构风格中的设计原则，它强调在客户端和服务器之间通过超媒体链接（Hypermedia）来驱动应用程序的状态转换。该设计原则的java实现可参考:`spring-hateoas`                                                                                                       | [Link](https://github.com/spring-projects/spring-hateoas)         |
| antlr          | ANTLR (ANother Tool for Language Recognition) is a powerful parser generator for reading, processing, executing, or translating structured text or binary files. (可用于SQL解析)                                                                                 | [Link](https://github.com/antlr/antlr4)                           |
| Quarkus        | A Kubernetes Native Java stack tailored for OpenJDK HotSpot and GraalVM, crafted from the best of breed Java libraries and standards.                                                                                                                       | [Link](https://github.com/quarkusio)                              |
| apereo cas     | Identity & Single Sign On for all earthlings and beyond. 单点登录                                                                                                                                                                                               | [Link](https://github.com/apereo/cas)                             |
| manifold       | Manifold is a Java compiler plugin. Use it to supplement your Java projects with highly productive features.                                                                                                                                                | [Link](https://github.com/manifold-systems/manifold)              |
| teaclave       | Apache Teaclave (incubating) is an open source universal secure computing platform, making computation on privacy-sensitive data safe and simple.(通用安全计算平台)                                                                                                 | [Link](https://github.com/apache/incubator-teaclave-java-tee-sdk) |
| reactor        | 非阻塞编程                                                                                                                                                                                                                                                       | [Link](https://projectreactor.io/)                                |
| micrometer     | Micrometer provides a facade for the most popular observability systems, allowing you to instrument your JVM-based application code without vendor lock-in. Think SLF4J, but for observability.                                                             | [Link](https://micrometer.io/)                                    |
| garnet         | Garnet is a remote cache-store from Microsoft Research that offers strong performance (throughput and latency), scalability, storage, recovery, cluster sharding, key migration, and replication features. Garnet can work with existing **Redis** clients. | [Link](https://github.com/microsoft/garnet)                       |
| `johnlui/PPHC` | 《高并发的哲学原理》                                                                                                                                                                                                                                                  | [Link](https://github.com/johnlui/PPHC)                           |

:white_check_mark:  :x: :star:

# 
