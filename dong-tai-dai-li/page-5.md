# 动态代理

## 什么是代理？

代理指：某些场景下对象会找一个代理对象，来辅助自己完成一些工作

代理主要是对对象的行为额外做一些辅助操作

## 如何创建代理对象

* Java中代理的代表类是：java.lang.reflect.Porxy
* Proxy提供了一个静态方法，用于对对象产生一个代理对象返回

<figure><img src="../.gitbook/assets/image (3) (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (5) (2).png" alt=""><figcaption></figcaption></figure>

## Java中实现动态代理的步骤

* 必须存在接口
* 被代理对象需要实现接口
* 使用Proxy类提供的方法的对象的代理对象

<figure><img src="../.gitbook/assets/image (7) (2).png" alt=""><figcaption></figcaption></figure>

## 执行流程

* 先走向代理
* 代理可以为方法额外做一些辅助工作
* 开发真正触发对象的方法的执行
* 回到代理中，由代理负责返回结果给方法的调用者

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

## 动态代理的优点

* 可以在不改变方法源码的情况下，实现对方法功能的增强，提高了代码的复用
* 简化了编程工作、提高了开发效率，同时提高了软件系统的可延展性
* 可以为被代理对象的所有方法做代理
* 非常的灵活，支持任意接口类型的实现类对象做代理，也可以直接为接口本身做代理
