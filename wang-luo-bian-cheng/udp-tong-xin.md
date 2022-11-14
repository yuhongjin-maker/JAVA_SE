# UDP通信

## UDP协议通信模型演示

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

## 一发一收

```
//实现一发一收
// 发送端
// 创建发送端对象：发送端自带默认的端口号
DatagramSocket socket = new DatagramSocket();

//创建一个数据包对象封装数据
byte[] buffer = "啊啦啦啦".getBytes();
DtagramPacket packet = new DatagramPacket(buffer,buffer.length,IntetAddress.getLocalHost(),8888);

//发送数据出去
socket.sned(packet);

socket.close（）；

//接收端
//创建接收端对象：注册端口
DatagramSocket socket = new DatagramSocket(8888);

//创建一个数据包对象接收数据
byte[] buffer = new byte[1024*24];
DatagramPacket packet = new DatagramPacket(buffer, buffer.length);

//接受数据即可
socket.receive(packet);

//取出数据
//接收多少读多少
String s = new String(buffer,0,packet.getLength());

socket.close();
```

## 广播、组播

### UDP的三种通信方式

* 单薄：单台主机与单台主机之前的通信
* 广播：当前主机与所在网络中的所有主机通信
* 组播：当前主机与选定的一组主机的通信

### 如何实现广播

* 使用广播地址：255.255.255.255

#### 具体操作

1. 发送端发送的数据包的目的地写的是广播地址，且指定端口。(255.255.255.255,9999)
2. 本机所在网段的其他主机的程序只要匹配端口成功就可以收到消息了。(9999)

### 如何实现组播

* 使用组播地址：224.0.0.0 \~ 239.255.255.255

#### 具体操作

1. 发送端的数据包的目的地是组播IP （例如：224.0.1.1，端口：9999）
2. 接收端必须绑定该组播IP(224.0.1.1)，端口还可以对应发送端的目的端口9999,这样可接受到该组消息
3. DatagramSocket的子类MulticastSocket可以在接收端绑定组播IP
