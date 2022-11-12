# 转换流

## 字符流直接读取文本内容
* 必须文件和代码编码一致才不会乱码
* 如果文件和代码编码不一致，读取将出现乱码

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 9.05.44 PM.png" alt=""><figcaption></figcaption></figure>


## 字符输入转换流

* 可以解决字符流读取不同编码乱码的问题
* 可以指定编码把原始字节流转换成字符流，如此字符流中的字符不乱码

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 10.50.13 PM.png" alt=""><figcaption></figcaption></figure>

```
//代码UTF-8 文件 GBK "src/data.txt";
// 提取GBK文件的原始字节流
InputStream is =  new FileInputStream("src/data.txt");

//把原始字节流转化成字符输入流
Reader isr = new InputStreamReader(is,"GBK"); //指定的GBK编码转换成字符输入流

BufferedReader br = new BufferedReader(isr);

```

## 字符输出转换流

* 可以指定编码把字节输出转换成字符输出流，从而可以指定写出去的字符编码

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.10.44 PM.png" alt=""><figcaption></figcaption></figure>

```
// 定义一个字节输出流
OutputStream os = new FileOutputStream(src/"data.txt");

//把原始的字节输出流转换成字符输出流
Writer osw = new OutputStreamWriter(os); //默认用UTF-8写字符出去，跟直接写FileWriter一样

Writer osw = new OutputStreamWriter(os，“GBK”); //指定GBK的方式写字符出去

//把低级的字符输出流包装成缓冲字符输出流
BufferedWriter bw = new BufferedWriter(osw);

```
