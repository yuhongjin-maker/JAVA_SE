# File类概述

## File类概述

* File类在包java.io.File下，代表操作系统的文件对象（文件、文件夹）
* File类提供了诸如：定位文件，获取文件本身的信息、删除文件、创建文件（文件夹）等功能
* 创建对象定位文件，可以删除、获取文件信息等。但不能读写文件内容。



## File类创建对象

* File对象可以定位文件和文件夹
* File封装的对象仅仅是一个路径名，这个路径可以是存在的，也可以是不存在的

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 2.24.56 PM.png" alt=""><figcaption></figcaption></figure>



## 绝对路径和相对路径

* 绝对路径：从盘符开始

```
File file1 = new File("D:\\ithema\\a.txt");
```

* 相对路径：不带盘符，默认直接到当前工程下的目录寻找文件

```
File file3 =  new File("模块名\\a.txt");
```


