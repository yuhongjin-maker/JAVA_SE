# 线程池

## 线程池概述

### 什么是线程池？
* 线程池就是一个可以复用线程的技术

### 不使用线程池的问题
* 如果用户每发起一个请求，后台就创建一个新线程来处理，下次新任务来了又要创建新线程，而创建线程的开销是很大的，这样严重影响系统的性能

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.49.48 PM.png" alt=""><figcaption></figcaption></figure>

## 线程池实现的API、参数说明

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.50.55 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.53.50 PM.png " alt=""><figcaption></figcaption></figure>

## 面试常见题

### 临时线程什么时候创建？
* 新任务提交时发现核心线程都在忙，任务队列也满了，而且还可以创建临时线程，此时才会创建临时线程

### 什么时候拒绝任务？
* 核心线程和临时线程都在忙，任务队列也满了，新的任务过来的时候才会开始任务拒绝

## 线程池处理Runnable任务

