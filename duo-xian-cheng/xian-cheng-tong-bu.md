# 线程同步

## 同步思想概述

* 加锁，把共享资源进行上锁，每次只能一个线程进行访问完毕后解锁，然后其他线程才能进来

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 10.36.00 PM.png" alt=""><figcaption></figcaption></figure>


## 方式一：同步代码块

* 作用：把出现线程安全问题的核心代码使用synchronized进行加锁
* 原理：每次只能一个线程进入，执行完毕后自动解锁，其他线程才可以进来执行

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 10.38.01 PM.png" alt=""><figcaption></figcaption></figure>

### 锁对象要求

* 理论上：锁对象只要对于当前同时执行的线程来说是同一个对象即可

### 锁对象的规范要求

* 规范上：建议使用共享资源作为锁对象
* 对于是例方法建议使用this作为锁对象
* 对于静态方法建议使用字节码（类.class）对象作为锁对象

## 方法二：同步方法

* 作用：把出现线程安全问题的核心方法给上锁
* 原理：每次只能一个线程进入，执行完毕以后自动解锁，其他线程才可以进来执行

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 10.46.50 PM.png" alt=""><figcaption></figcaption></figure>

### 同步方法的底层原理

* 同步方法其实底层也是有隐式锁对象的，只能锁的范围是整个方法代码
* 如果方法是实例方法：同步方法默认用this作为锁的对象。但是代码要高度面向对象
* 如果方法是静态方法：同步方法默认用类名.class作为的锁对象
* 同步

