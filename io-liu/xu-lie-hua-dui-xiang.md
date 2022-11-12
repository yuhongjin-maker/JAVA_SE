# 序列化对象

## 对象序列化

* 含义：把对象数据存入到文件中去
* 序列化对象的要求是对象必须实现序列化接口

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.17.13 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.19.51 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.29.52 PM.png" alt=""><figcaption></figcaption></figure>

```
//对象要序列化必须实现Serializable序列化接口
//创建学生对象
Student s = new Student("minnie","h245yu","123456",21);

//对象序列化：使用对象字节输出流包装字节输出流管道
ObjectOutputStream oos = new ObjectoutputStream(new FileOutputStream("src/data.txt"));

//直接调用序列化方法
oos.writeObject(s);

//释放资源
oos.close();

```

## 对象反序列化

* 含义：把磁盘中的对象数据恢复到内存的Java对象中
* transient修饰的成员变量不参加序列化
* 序列化的版本号和反序列化的版本号必须一致 （private static final long serialVersionUID = 1;）

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.31.47 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-11 at 11.32.26 PM.png" alt=""><figcaption></figcaption></figure>

```
//创建对象字节输入流管道包装低级的字节输入流管道
ObjectInputStream is = new ObjectInputStream(new FileInputStream("src/data.txt"));

// 调用对象字节输入流的反序列化方法
Student s = (Student) is.readObject();
```
