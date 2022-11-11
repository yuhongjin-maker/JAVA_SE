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

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.56.27 PM.png" alt=""><figcaption></figcaption></figure>


