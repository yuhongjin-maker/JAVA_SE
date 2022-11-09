# Logback日志框架、日志级别设置


### [官方网站](https://logback.qos.ch/index.html)

## Logback主要分为三个技术模块

* logback-core:logback-core模块为其他两个模块奠定了基础，必须有
* logback-claasic:它是log4j的一个改良版
* logback-access:与Tomcat 和 Jetty等Servlet容器集成，以提供HTTP访问日志功能


## Logback的开发步骤
1. 在项目下新建文件夹lib,导入Logback的相关jar包到该文件夹下，并添加到项目库中去
2. 必须将Logback的核心配置文件logback.xml直接拷贝到src目录下
3. 在代码中获取日志的对象
4. 使用日志对象输出日志信息



## Logback配置详解-输出位置、格式设置

#### Logback日志系统的特性都是通过核心配置文件logback.xml控制的

### Logback日志输出位置、格式设置

* 通过logback.xml中的 <append> 标签可以设置输出位置和日志信息的详细格式
* 通常可以设置2个日志输出位置：一个是控制台、一个是系统文件中
  
  
