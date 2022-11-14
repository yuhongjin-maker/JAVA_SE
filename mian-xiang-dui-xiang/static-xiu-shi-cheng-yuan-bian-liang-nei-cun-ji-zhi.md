# static: 修饰成员变量、内存机制

### static是什么:

* 是静态的意思，可以修饰成员变量和成员方法
* static修饰成员变量表示该成员变量只在内存中存储一份，可以被共享访问，修改

### 成员变量可以分成2类

* 静态成员变量（有static修饰，属于类，内存中加载一次）：常表示如在线人数信息、等需要被共享的信息，可以被共享访问

![](<../.gitbook/assets/image (13) (1).png>)

* 实例成员变量（无static修饰，存在于每个对象中）：常表示姓名name、年龄age、等属于每个对象的信息

![](<../.gitbook/assets/image (2) (1) (2).png>)

### 内存机制

<figure><img src="../.gitbook/assets/image (7) (2).png" alt=""><figcaption><p><br><br></p></figcaption></figure>
