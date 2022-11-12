# 多线程的创建

## 什么是线程

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.42.48 AM.png" alt=""><figcaption></figcaption></figure>

## 多线程是什么？
* 多线程是指从软硬件上实现多条执行流程的技术
* 再例如：消息通信、淘宝、京东系统都离不开多线程技术

## 方法一：继承Thread类

### Thread类
* Java是通过java.lang.Thread类代表线程的
* 按照面向对象的思想，Thread类应该提供了实现多线程的方式

### 多线程的实现方案一：继承Thread类
1. 定义一个字类MyThread继承线程类java.lang.Thread，重写run()方法
2. 创建MyThread类的对象
3. 调用线程对象的start()方法启动线程（启动后还是执行run方法的）

### 优缺点
* 优点：代码简洁
* 缺点：线程类已经继承Thread，无法继承其他类，不利于扩展

#### 不要把主线程任务放在子线程之前
```
//在main里面new一个新线程对象
Thtread t = new My Thread();

//调用start方法启动线程（执行还是run方法）
t.start();

```

```
//定义一个线程类继承Thread类
class MyThread extends Thread{
  //重新run方法
  
  @Override
  public void run(){
    for(int i =0; i< 5;i++){
    //some code
    }
  }
  
}
```

## 方法二：实现Runnable接口

### 多线程的实现方法二：实现Runnable接口
1. 定义一个线程任务类MyRunnable实现Runnable接口，重写run()方法
2. 创建MyRunnable任务对象
3. 把MyRunnable任务对象交给Thread处理
4. 调用线程对象的start()方法启动线程

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 11.28.30 AM.png" alt=""><figcaption></figcaption></figure>

### 优缺点
* 优点：线程任务类只是接口，可以继续继承类和实现接口，扩展性强
* 缺点：编程多一层对象包装，如果线程有执行结果是不可以直接返回的
```
//创建一个任务对象
Runnable target = new My Runnable();

//把任务对象交给Thread处理
Thread t= new Thread(target);

//启动线程
t.start();

//主线程任务
```

```
// 定义一个线程任务类，实现Runnable接口
class MyRunnable implements Runnable{
  // 重写run方法
  @Override
  public void run(){
    for(int i=0; i< 10; i++){
      // some code
    }
  }
}
```
### 多线程的实现方法二：实现Runnable接口（匿名内部类形式）
1. 可以创建Runnable的匿名内部类对象
2. 交给Thread处理
3. 调用线程对象的start()启动线程

```

Runnable target = new Runnable(){
  @Override
  public void run(){
  //some code
  }
 
 
Thread t = new Thread(target);

t.start();

//主线程任务
}
```
## 方法三：实现Callable接口

### 多线程的实现方案三：利用Callable、FuntureTask接口实现
1. 得到任务对象
* 定义类实现Callable接口，重写call方法，封装要做的事情
* 用FutureTask把Callable对象封装成线程任务对象
2. 把线程任务对象交给Thread处理
3. 调用Thread的start方法启动线程，执行任务
4. 线程执行完毕后、通过FutureTask的get方法去获取任务执行的结果

```
//创建Callable任务对象
Callable<String> call = new MyCallable(100);

// 把Callable任务对象交给FutureTask对象
//FutureTask对象的作用：是Runnable的对象可以交给Thread而且可以在线程执行完毕之后调用其get方法得到执行完结果

FutureTask<String> f1 = new FitireTask<>(call);

Thread t1= new Thread(f1);

t1.start();

//拿线程执行结果
String s = f1.get();

```

```
//定义一个任务类，实现Callable接口 应该声明线程任务执行完毕后的结果的数据类型
class MyCallable implements Callable<String>{
  private int n;
  public MyCallable(int n){
    this.n=n;
  }

  //重写call方法
  @Override
  public String call() throws Exception{
    return "";
  }
}
```
