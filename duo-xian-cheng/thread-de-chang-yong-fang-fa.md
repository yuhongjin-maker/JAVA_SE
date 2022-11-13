# Thread的常用方法

## Thread常用API说明

* Thread常用方法：获取线程名称getName()、设置名称setName()、获取当前线程currentThread()
* 至于Thread类提供的诸如:yield、join、interrupt、不推荐的方法stop、守护线程、线程优先等线程的控制方法，在开发中很少使用

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 9.38.30 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 9.43.33 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 9.46.32 PM.png" alt=""><figcaption></figcaption></figure>

## Thread类的线程休眠方法

 ```
 //方法名称
 public static void sleep(long time);
 //说明
 让当前线程休眠指定的时间后再继续执行，单位为毫秒

 ```
