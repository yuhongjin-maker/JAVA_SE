# 网络通信三要素

## 网络通信基本模式

* 常见的通信模式有如下2种形式：Client-Server(CS), Browser/Server(BS)

<figure><img src="../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>

## 三要素概述

* IP地址：设备在网络中的地址，是唯一的标识
* 端口：应用程序在设备中唯一的标识
* 协议：数据在网络中传输的规则，常见的协议有UDP协议和TCP协议

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

## 要素一：IP地址

* IP（Internet Protocol）：是分配给上网设备的唯一标志
* 常见的IP分类：IPv4和IPv6

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (6).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (6).png" alt=""><figcaption></figcaption></figure>

### IP地址形式

* 公网地址、和私有网址（局域网使用）
* 192.168.开头的就是常见的局域网地址

### IP常用命令

* ipconfig:查看本机IP地址
* ping IP地址：检查网络是否连接

### 特殊IP地址

* 本机IP：127.0.0.1或者localhost:称为回送地址也可称本地回环地址，只会寻找当前所在本机

## IP地址操作类-IntetAddress

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

```
// Some code
// 获取本机地址对象
InterAddress ip1 = InetAddress.getLocalHost();

//获取域名ip对象
InterAddress ip2 = InetAddress.getByName("www.baidu.com");

//获取公网IP对象
IntetAddress ip3 = InterAddress.getName("112.80.248.76");

//判断是否能同: ping 5s 之前测试是否1可通
ip3.isReachable(5000);
```

## 要素二：端口二

### 端口号

* 标识正在计算机设备上运行的进程，被规定为一个16位的二进制，范围是0\~65535

### 端口类型

* 周知端口：0\~1023，被预先定义的知名应用占用
* 注册端口：1024\~49151，分配给用户进程或某些应用程序
* 动态端口：49152\~65535，之所以称为动态端口，是因为它一般不固定分配某种进程，而是动态分配

#### 注意：我们自己开发的程序选择注册端口，且一个设备中不能出现两个程序端口号一样，否则出错

## 要素三：协议

### 通信协议

* 链接和通信数据的规则

<figure><img src="../.gitbook/assets/image (2) (1) (3).png" alt=""><figcaption></figcaption></figure>

### 传输层的2个常见协议

* TCP(Transimission Control Protocol)：传输控制协议
* UDP(User Datagram Protocol): 用户数据报协议

### TCP协议特点

* 使用TCP协议，必须双方先建立连接，它是一种面向连接的可靠通信协议
* 传输前，采用”三次握手“方式建立连接，所以是可靠的
* 在连接中可进行大数据量的传输
* 连接、发送数据都需要确认，且传输完毕后，还需释放已建立的连接，通信效率低

### TCP协议通信场景

* 对信息安全要求较高的场景

### TCP三次握手确立连接

<figure><img src="../.gitbook/assets/image (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

### TCP四次挥手断开连接

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### UDP协议

* UDP是一种无连接、不可靠传输的协议
* 将数据源IP、目的地IP和端口封装成数据包，不需要建立连接
* 每个数据包的大小限制在64KB内
* 发送不管对方是否准备好，接收方收到也不确认，所以是不可靠的
* 可以广播发送，发送数据结束时无需释放资源，开销小，速度快

### UDP协议通信场景

* 语音通话，视频会话等
