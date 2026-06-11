# Java 生态笔记

> Java 常用库、工具与知名组织整理。

## 待学习

| 库             | 描述                                                                                                                                        | 地址                                                              |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `JavaFX`       | JavaFX is an open source, next generation client application platform for desktop, mobile and embedded systems built on Java.               | [Link](https://openjfx.io/)                                       |
| `Java JNA`     | Java Native Access                                                                                                                          | [Link](https://github.com/java-native-access/jna)                 |
| `drools`       | 规则引擎（工具复杂度高，需**重点关注**）                                                                                                    | [Link](https://github.com/apache/incubator-kie-drools)            |
| `GraphQL`      | 面向 API 的数据查询操作语言及运行环境，每种语言都有其对应实现。                                                                             | [Link](https://github.com/graphql-java/graphql-java)              |
| `HATEOAS`      | REST 架构风格中的设计原则，通过超媒体链接驱动应用状态转换。                                                                                 | [Link](https://github.com/spring-projects/spring-hateoas)         |
| `antlr`        | ANTLR is a powerful parser generator for reading, processing, executing, or translating structured text or binary files.（可用于 SQL 解析） | [Link](https://github.com/antlr/antlr4)                           |
| `Quarkus`      | A Kubernetes Native Java stack tailored for OpenJDK HotSpot and GraalVM.                                                                    | [Link](https://github.com/quarkusio)                              |
| `apereo cas`   | 单点登录（SSO）框架                                                                                                                         | [Link](https://github.com/apereo/cas)                             |
| `manifold`     | Manifold is a Java compiler plugin with highly productive features.                                                                         | [Link](https://github.com/manifold-systems/manifold)              |
| `teaclave`     | Apache Teaclave 通用安全计算平台                                                                                                            | [Link](https://github.com/apache/incubator-teaclave-java-tee-sdk) |
| `reactor`      | 非阻塞编程                                                                                                                                  | [Link](https://projectreactor.io/)                                |
| `micrometer`   | Micrometer provides a facade for the most popular observability systems. Think SLF4J, but for observability.                                | [Link](https://micrometer.io/)                                    |
| `garnet`       | Microsoft Research 的远程缓存存储，兼容 Redis 客户端。                                                                                      | [Link](https://github.com/microsoft/garnet)                       |
| `johnlui/PPHC` | 《高并发的哲学原理》                                                                                                                        | [Link](https://github.com/johnlui/PPHC)                           |

## 工具库

| 库             | 描述                                                                          | 地址                                                 | 推荐指数           |
| -------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------- | ------------------ |
| `resilience4j` | Fault tolerance library designed for functional programming.                  | [Link](https://github.com/resilience4j/resilience4j) | :star::star::star: |
| `JsonPath`     | Java JsonPath implementation. 可通过路径访问 JSON，例 `$.store.book[0].title` | [Link](https://github.com/json-path/JsonPath)        | :star::star::star: |
| `archaius`     | Library for configuration management API                                      | [Link](https://github.com/Netflix/archaius)          | :star::star::star: |
| `MyExcel`      | 集导入、导出、加密 Excel 等多项功能的工具包。                                 | [Link](https://github.com/liaochong/myexcel)         | :star::star::star: |
| `OSHI`         | Native Operating System and Hardware Information.                             | [Link](https://github.com/oshi/oshi)                 | :star::star::star: |
| `mustache`     | 模版引擎，本身也是一套规范，已有**多语言**实现。                              | [Link](https://mustache.github.io/)                  | :star::star::star: |
| `hutool`       | Hutool 是一个功能丰富且易用的 Java 工具库                                     | [Link](https://github.com/dromara/hutool)            | :star::star::star: |
| `japicmp`      | A tool to compare two versions of a jar archive.                              | [Link](https://github.com/siom79/japicmp)            | :star::star:       |
| `arthas`       | Alibaba Java 诊断利器 Arthas                                                  | [Link](https://github.com/alibaba/arthas)            | :star::star::star: |
| `JSch`         | JSch is a pure Java implementation of SSH2.                                   | [Link](http://www.jcraft.com/jsch/)                  | :star::star::star: |

## 命令行解析工具

| 库            | 描述                                          | 地址                                               | 推荐指数           |
| ------------- | --------------------------------------------- | -------------------------------------------------- | ------------------ |
| `jcommander`  | Command line parsing framework for Java       | [Link](https://github.com/cbeust/jcommander)       | :star::star::star: |
| `jopt-simple` | Java library for parsing command line options | [Link](https://github.com/jopt-simple/jopt-simple) | :star::star:       |

更多解析工具参考：[Command Parser](https://jopt-simple.github.io/jopt-simple/)

## 字节码编辑工具

| 库          | 描述                                                  | 地址                                        | 推荐指数           |
| ----------- | ----------------------------------------------------- | ------------------------------------------- | ------------------ |
| `bytebuddy` | Runtime code generation for the Java virtual machine. | [Link](https://github.com/raphw/byte-buddy) | :star::star::star: |
| `javapoet`  | `.java` 文件生成工具（**生成源码**）                  | [Link](https://github.com/square/javapoet)  | :star::star::star: |

## 测试库

| 库               | 描述           | 地址                                                          | 推荐指数           |
| ---------------- | -------------- | ------------------------------------------------------------- | ------------------ |
| `Jacoco`         | 单元测试覆盖率 | [Link](https://github.com/jacoco/jacoco)                      | :star::star::star: |
| `Testcontainers` | 容器测试       | [Link](https://github.com/testcontainers/testcontainers-java) | :star::star::star: |

## 缓存库

| 库         | 描述                                        | 地址                                          | 推荐指数           |
| ---------- | ------------------------------------------- | --------------------------------------------- | ------------------ |
| `Caffeine` | A high performance caching library for Java | [Link](https://github.com/ben-manes/caffeine) | :star::star::star: |

## 序列化框架

| 库     | 描述                                                                                  | 地址                                   | 推荐指数           |
| ------ | ------------------------------------------------------------------------------------- | -------------------------------------- | ------------------ |
| `fury` | A blazingly fast multi-language serialization framework powered by JIT and zero-copy. | [Link](https://github.com/apache/fury) | :star::star::star: |

## 知名组织

### VMware Tanzu

> 云平台，助力高价值应用快速部署发布。**Spring 母公司**

[官网](https://tanzu.vmware.com/)

### Tidelift

> Making open source software work better—for everyone.

通过订阅服务，提供安全的开源软件，降低开源软件使用风险。

- Github: [Link](https://github.com/tidelift)
- 官网: [Link](https://tidelift.com)
