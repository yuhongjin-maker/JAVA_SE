# IO 流概述

* I便是input，是数据从硬盘文件读入到内存的过程，称为输入，负责读
* O表示output,是内存程序的数据从内存到写出到硬盘文件的过程，称之输出，负责写

## IO流的分类

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.16.06 PM.png" alt=""><figcaption></figcaption></figure>

## 四大类

* 字节输入流：以内存为基准，来自磁盘文件/网络中的数据以字节的形式读入到内存中去的流称为字节输入流
* 字节输出流：以内存为基准，把内存中的数据以字节写出到磁盘文件或者网络中去的流称为字节输出流
* 字符输入流：以内存为基准，来自磁盘文件/网络中的数据以字符的形式读入到内存中去的流称为字符输入流
* 字符输出流：以内存为基准，把内存中的数据以字符写出到磁盘文件或者网络介质中去的流称为字符输出流

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.21.59 PM.png" alt=""><figcaption></figcaption></figure>


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


