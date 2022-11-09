# 异常概述、分类、认识

## 异常概述

* 异常是程序在“编译”或者“执行”的过程中可能出现的问题，注意：语法错误不算在异常体系中
* 比如：数组索引越界、空指针异常、日期格式化异常，等.....
* 异常一旦出现了，如果没有提前处理，程序就会推出JVM虚拟机而终止
* 研究异常并且避免异常，然后提前处理异常，体现的是程序的安全、健壮性



## 异常体系

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-07 at 2.48.33 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-07 at 2.51.54 PM.png" alt=""><figcaption></figcaption></figure>



## 常见运行时异常

### 运行时异常

* 直接继承自RuntimeException或者其子类，编译阶段不会报错，运行时可能出现的错误

### 运行时异常示例

* 数组索引越界异常：ArrayIndexOutOfBoundsException
* 空指针异常: NullPointerException,直接输出没有问题，但是调用空指针的变量的功能就会报错
* 数学操作异常：ArithmeticException
* 类型转换异常：ClassCastException
* 数字转换异常：NumberFormatException
#### 运行时异常：一般是指程序员业务没有考虑好或者是编程逻辑不严谨引起的程序错误

### 编译时异常
* 不是RuntimeException或者子类的异常，编译阶段就报错。
* 作用：是担心程序员的技术不行，在编译阶段就爆出一个错误，目的在于提醒不要出错

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-09 at 11.40.13 AM.png" alt=""><figcaption></figcaption></figure>



## 异常的默认处理流程

1. 默认会在出现异常的代码那里自动的创建一个异常对象：ArithmeticException
2. 异常会从方法中出现的点这里抛出给调用者，调用者最终抛出给JVM虚拟机
3. 虚拟机接收到异常对象后，先在控制台直接输出异常栈信息数据
4. 直接从当前执行的异常带你干掉当前程序
5. 后续代码没有机会运行了
