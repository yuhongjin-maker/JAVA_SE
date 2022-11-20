# XML

## XML概述

* XML是可扩展标记语言（extensible Markup Language）的缩写，它是一种数据表示格式，可以描述非常复杂的数据结构，常用于传输和存储数据

## 特点

* 一是纯文本，默认使用UTF-8编码；二是可嵌套
* 如果把XML内容存为文件，那么它就是一个XML文件
* XML的使用场景：XML内容经常被当成消息进行网络传输，或者作为配置文件用于存储系统的信息

## XML的创建和语法规则

* 就是创建一个XML类型的文件，要求文件的后缀必须使用xml，如hello\_world.xml

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## XML的语法规则

* XML文件的后缀名为：xml
* 文档声明必须是第一行

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

## XML的标签（元素）规则

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## XML其它内容

<figure><img src="../.gitbook/assets/image (6) (3).png" alt=""><figcaption></figcaption></figure>

## XML的文档约束

#### 问题:由于XML文件可以自定义标签，导致XML文件可以随意定义，程序在解析的时候可能出现问题

### 文档约束

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

### DTD的使用

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

* 可以约束XML文件的编写
* 不能约束具体的数据类型

### SCHEMA约束

* schema可以约束具体的数据类型，约束能力更强大
* schema本身也是一个xml文件，本身也受到其他约束文件的要求，所以编写的更加严谨

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
