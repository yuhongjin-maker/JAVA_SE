# 打印流

## 打印流

* 作用：打印流可以实现方便、高效的打印数据到文件中去。
* PrintStream,PrintWriter两个类
* 可以实现打印什么数据就是什么数据

### PrintStream

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.17.33 AM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个打印流对象
PrintStream ps = new PrintStream("src/data.txt");

ps.println(97);

ps.close();
```

### PrintWriter

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.21.11 AM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个打印流对象
PrintWriter ps = new PrintStream("src/data.txt");

ps.println(97);

ps.close();
```

### PrintStream 和 Printwriter的区别

* 打印数据功能上是一模一样的，都是使用方便，性能高效
* PrnitStream继承字节输出流OutputStream,支持写字节数据的方法
* PrintWriter继承自字符输出流Writer，支持写字符数据出去

## 输出语句的重定向

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.27.33 AM.png" alt=""><figcaption></figcaption></figure>


