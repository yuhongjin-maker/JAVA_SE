# Stream流

## Stream流的概述

* 在Java8中，得益于Lambda所带来的函数式编程，引入了一个全新的Stream流概念
* 目的：用于简化集合和数组操作的API

### Stream流式思想的核心

1. 获取Stream流 - 创建一条流水线，并把数据放到流水线上准备进行操作
2. 中间方法 - 流水线上的操作。一次性操作完毕后，还可以继续进行其他操作
3. 终结方法 - 一个Stream流只能有一个终结方法，是流水线上的最后一个操作



## Stream流的获取

* 集合获取Stream的方式是通过调用stream()方法实现的

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 6.22.11 PM.png" alt=""><figcaption></figcaption></figure>



## Stream流的常用API

* 中间方法也称为非终结方法，调用完成后返回新的Stream流可以继续使用，支持链式编程
* 在Stream流中无法直接修改集合、数组中的数据

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 6.33.47 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 6.49.55 PM.png" alt=""><figcaption></figcaption></figure>



## 收集Stream流

* 收集Stream流的含义：就是把Stream流操作后的结果数据转回到集合或者数组中去

* Stream流：方便操作集合/数组的手段

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 7.24.06 PM.png" alt=""><figcaption></figcaption></figure>





