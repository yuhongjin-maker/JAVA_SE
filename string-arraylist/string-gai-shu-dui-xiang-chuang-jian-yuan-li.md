# String概述，对象创建原理

### String概述

* Java.lang.String类代表字符串，String类定义的变量可以用于指向字符串对象，然后操作该字符串
* Java程序中的所有字符串文字（例如 "abc"）都为此类对象
* 字符串类型，可以定义字符串变量指向字符串对象

### String类的特点

String其实常被称为不可变字符串类型，它的对象在创建后不能被更改

#### 原因

* String变量每次的修改其实都是产生并指向了新的字符串对象
* 原来的字符串对象都是没有改变的，所以称不可变字符串

![](<../.gitbook/assets/image (2) (4) (2).png>)

![](<../.gitbook/assets/image (3) (2) (2).png>)

### 有什么区别？

* 以 "" 方式给出的字符串对象，在字符串常量池中存储，而且相同内容只会在其中存储一份
*

    ![](<../.gitbook/assets/image (6) (2) (1).png>)
* 通过构造器new对象，每new一次都会产生一个新对象，在堆内存中分开储存
*

    ![](<../.gitbook/assets/image (2) (5).png>)
