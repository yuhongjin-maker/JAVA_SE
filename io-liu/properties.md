# Properties

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.29.19 AM.png" alt=""><figcaption></figcaption></figure>

## Properties属性集对象

* 其实就是一个Map集合，但是我们一般不会当集合使用，因为HashMap更好用

## Properties核心作用

* Properties代表的是一个属性文件，可以把自己对象中的键值对信息存入到一个属性文件中去
* 属性文件：后缀是.properties结尾的文件。里面的内容都是key=value,后续做系统配置信息的

## Properties的API

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-12 at 12.32.36 AM.png" alt=""><figcaption></figcaption></figure>

```
//使用Properties把键值对信息存入到属性文件中去
Properties properties= new Peoperties();

properties.setProperty("admin","12345");

properties.store(new FileWriter("src/users.properties"),"");

```

```
// Properties读取属性文件中的键值对信息
Properties properties = new Properties();

//加载属性文件的键值对数据到属性properties中去
properties.load(new FilerReader("src/users.properties"));
```
