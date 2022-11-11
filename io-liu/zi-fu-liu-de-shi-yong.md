# 字符流的使用

## 文件字符输入流：Reader
### 一次读取一个字符

* 好处：读取中文字符不会出现乱码
* 坏处：性能比较慢

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 5.25.19 PM.png" alt=""><figcaption></figcaption></figure>

```
//每次读取一个字符
//创建一个字符输入管道与源文件接通

Reader fr = new FileReader("src\\data.txt");

//读取一个字符返回，没有可读的字符返回-1
int code = fr.read();
```


### 一次读取一个字符数组

* 性能得到了提升

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 5.30.30 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个字符输入管道与源文件接通
Reader fr = new FileReader("src\\data.txt");

// 用循环，读取一个字符数组的数据
char[] buffer = new char[1024]; // 1K字符
int len;
while ((len = fr.read(buffer))!= -1){
  String rs = new String(buffer,0,len);
}
```

## 文件字符输出流

* 字符输出流实现写出的数据能换行 -> fw.write("\r\n");

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 5.41.26 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建一个字符输出流管道与目标文件接通
Writer fw = new FileWrite("src/data.txt");

//写一个字符出去
fw.write('a');

//写一个字符串出去
fw.write("啦啦啦")；

//写字符串的一部分出去
fw.write("啦啦啦"，0，2)；

//关闭流
fw.close();

```

## 字节流、字符流如何选择使用

* 字节流适合做一切文件数据的拷贝（音视频、文本）
* 字节流不适合读取中文内容输出
* 字符流适合做文本文件的操作（读，写）
 
