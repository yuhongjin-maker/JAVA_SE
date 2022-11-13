# 定时器

## 定时器
* 定时器是一种控制任务延时调用，或者周期调用的技术
* 作用：闹钟、定时邮件发送

## 定时器的实现方式

* 方式一: Timer
* 方式二: ScheduledExecutorService

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-13 at 12.33.12 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个Timer定时器

Timer timer = new Timer(); //定时器本身就是一个单线程

//调用方法，处理定时任务
timer.schedule(new TimerTask(){
  @Override
  public void run(){
    //some code
  }
},3000,2000);
```

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-13 at 12.41.09 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建ScheduledExecutorService线程池，做定时器
ScheduledExecutorService pool = Executors.newScheduledThreadPool(3);

//开始定时任务
pool.scheduleAtFixedRate(new TimerTask(){
  @Override
  public void run(){
    //some code
  }
},0)
```
