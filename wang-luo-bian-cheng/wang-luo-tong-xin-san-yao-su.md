# 网络通信三要素

## 网络通信基本模式

* 常见的通信模式有如下2种形式：Client-Server(CS), Browser/Server(BS)

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

## 三要素概述

* IP地址：设备在网络中的地址，是唯一的标识
* 端口：应用程序在设备中唯一的标识
* 协议：数据在网络中传输的规则，常见的协议有UDP协议和TCP协议

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

## 要素一：IP地址

* IP（Internet Protocol）：是分配给上网设备的唯一标志
* 常见的IP分类：IPv4和IPv6

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### IP地址形式

* 公网地址、和私有网址（局域网使用）
* 192.168.开头的就是常见的局域网地址

### IP常用命令

* ipconfig:查看本机IP地址
* ping IP地址：检查网络是否连接

### 特殊IP地址

* 本机IP：127.0.0.1或者localhost:称为回送地址也可称本地回环地址，只会寻找当前所在本机

## IP地址操作类-IntetAddress

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

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
