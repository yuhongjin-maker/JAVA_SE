# 字节流的使用

## 文件字节输入流：FileInputStream
### 每次读取一个字节

* 每次读取一个字节存在 1. 性能较慢 2. 读取中文字符输出无法避免乱码问题

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.24.12 PM.png" alt=""><figcaption></figcaption></figure>

```
// 创建一个文件字节输入流每次读取一个字节的数据
InputStram is =  new FIleInputStream("file/src/data.txt");

int b1 = is.read();
```


### 每次读取一个字节数组

* 性能提升但读取中文字符输出无法避免乱码问题

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.41.51 PM.png" alt=""><figcaption></figcaption></figure>

```
// 创建一个文件字节输入流每次读取一个字节数组的数据
InputStram is =  new FIleInputStream("file/src/data.txt");

// 定义一个字节数组，用于读取字节数组
byte[] buffer = new byte[3];
int len = is.read(buffer);

```

### 一次读完全部字节


<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.48.43 PM.png" alt=""><figcaption></figcaption></figure>

```
InputStram is =  new FIleInputStream("file/src/data.txt");

byte[] buffer = is.readALLBytes();
String s = new String(buffer)
```
## 文件字节输出流：FileOutputStream
### 写字节数据到文件

* 字节输出流实现写出去的数据能换行 -> os.write("\r\n".getBytes())
* flush()刷新数据 -> 让写出去的数据能成功生效
* close()方法是关闭流，关闭包含刷新，关闭后流就不可以继续使用了

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 4.29.53 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个文件字节输出流管道与目标文件接通，在文件后追加内容，如果要清空再写不加true即可
OUtputStream os = new FileOutputStram("file/src/data.txt",true);

//写数据
os.write('a');

//刷新数据
os.flush();

//释放资源，包含了刷新
os.close();
```

## 文件拷贝

* 字节流适合
## 文件拷贝

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 4.42.40 PM.png" alt=""><figcaption></figcaption></figure>

