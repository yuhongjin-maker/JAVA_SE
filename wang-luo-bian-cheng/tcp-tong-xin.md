# TCP通信

## TCP通信模式演示

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

```
// 一发一收客户端
//创建Socket通信管道请求有服务端的连接
Socket socket = new Socket("127.0.0.1",7777);

//从scoket 通信管道中得到一个字节输出流，负责发送数据
OutputStream os = socket.getOutputStream();

//把低级的字节流包装成打印流
PrintStream ps = new PrintStream(os);

//发送消息
ps.print("lalall");
ps.flush();

//服务端
//注册端口
ServerSocket serverSoket = new ServerSocket(7777);

//必须调用accept方法：等待客户端的Socket连接请求，建立Socket通信管道
Socket socket = serverSocket.accept();

//从socket通信管道中一个字节输入流
InputStream is = socket.getInputStream();

//把字节输入流包装成缓冲字符输入流进行消息的接收
BufferedReader br = new BUfferedReader(new InputStreamReader(is));

```
