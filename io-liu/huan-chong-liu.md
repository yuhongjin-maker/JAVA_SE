# 缓冲流

## 缓冲流概述

* 作用：缓冲流自带缓冲区、可以提高原始字节流、字节流读写数据的性能
* 一共有四种缓冲流

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 5.48.19 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 5.52.10 PM.png" alt=""><figcaption></figcaption></figure>

## 字节缓冲流

### 字节缓冲流性能优化原理
* 字节缓冲输入流自带了8KB缓冲池，以后我们直接从缓冲池读取数据，所以性能较好
* 字节缓冲输出流自带了8KB缓冲池，数据就直接写入到缓冲池中去了，写数据性能就极高了

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 8.24.14 PM.png" alt=""><figcaption></figcaption></figure>

```
  // 创建一个字节输入流管道与原视频接通
  inputStream is =  new FileINputStream("src/data.txt");
  //把原始的字节输入流包装成高级的缓冲字节输入流
  inputStream bis = new BufferedInputStream(is);
  //创建一个字节输出流管道与目标文件接通
  OutputStream os = new FileOutputStream("src/data.txt");
  //把字节输出流管道包装成缓冲字节输出管道
  OutputStream bis = new BUfferedOutputStream(os);
 
```

## 字符缓冲输入流

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 8.39.21 PM.png" alt=""><figcaption></figcaption></figure>

```
// 创建一个文件字符输入流与源文件接通
Reader fr = new FileReader("src/data.txt");

//把低级的字符输入流包装成缓冲字符输入流
BufferedReader br = new BufferedReader(fr);

//行读
String line = br.readLine();
```

## 字符缓冲输出流

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 8.45.08 PM.png" alt=""><figcaption></figcaption></figure>

```
Writer fw=  new FileWrite("src/data.txt");
BufferedSriter bw = BUfferedWriter(fw);

// 换行
bw.newLine();
   
```

