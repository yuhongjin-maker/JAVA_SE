# 线程生命周期


## 线程的状态

* 线程的状态：也就是线程从生到死的过程，以及中间经历的各种状态及状态转换
* 理解线程的状态有利于提升并发编程的理解能力

## Java线程的状态

* Java总共定义了6种状态
* 6种状态都定义在Thread类的内部枚举类中


<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.29.10 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.31.56 PM.png" alt=""><figcaption></figcaption></figure>  

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.32.35 PM.png" alt=""><figcaption></figcaption></figure>  

## 线程的六种状态

* 新建状态（NEW）--> 创建线程对象
* 就绪状态（RUNNABLE）--> start方法
* 阻塞状态（BLOCKED） --> 无法获得锁对象
* 等待状态（WAITING）--> wait方法
* 计时等待（TIMED_WAITING）--> sleep 方法
* 结束状态（TERMINATED）--> 全部代码运行完毕
