# 字符集

## 字符集基础知识

* 计算机底层不可以直接存储字符的。计算机中底层只能存储二进制（0,1）
* 二进制是可以转换成十进制的
* 结论：计算机底层可以表示十进制编号。计算机可以给人类字符进行编号存储，这套编号规则就是字符集


## ASCII字符集

* ASCII(American Standard Code for information Interchange，美国信息交换标准代码)：包括了数字、英文、符号
* ASCII使用1个字节存储一个字符，一个字节是8位。总共可以表示128个字符信息，对于英文，数字来说是够用的

```
01100001 = 97 => a
01100010 = 98 => b
```

## GBK

* window系统默认的码表。兼容ASCII码表，也包含了几万个汉字，并支持繁体汉字以及部分日韩文字
* 注意：GBK是中国的码表，一个中文以两个字节的形式存储。但不包含世界上所有国家的文字

## Unicode码表：

* unicode是计算机科学里的一项业界字符编码标准
* 容纳世界上大多数国家的所有常见文字和符号

注意

* Unicode是万国码，以UTF-8编码后一个中文一般以三个字节的形式存储
* UTF-8也要兼容ASCII编码表
* 技术人员都应该使用UTF-8的字符集编码
* 编码前和编码后的字符集需要一致，否则会出现中文乱码
* 英文和数字在什么体系下都不会乱码

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.00.10 PM.png" alt=""><figcaption></figcaption></figure>

## 字符集的编码、解码操作

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 10.02.42 PM.png" alt=""><figcaption></figcaption></figure>

```
//编码：把文字转成字节（用指定的编码）
String name  = "abc我爱你";
byte[] bytes = name.getBytes("UTF-8")

//解码：把字节转换成对应的中文形式（编码前和编码后字符集必须一致，否则乱码）
String rs = new String(bytes);//默认的UTF-8
```

