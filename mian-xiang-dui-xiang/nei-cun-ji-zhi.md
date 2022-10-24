# 内存机制

### 多个对象内存图

![](<../.gitbook/assets/image (1) (2).png>)

#### 对象放在的位置

堆内存

#### Car c = new Car(); c变量名中存储的是什么？

存储的是对象在堆内存中的地址

#### 成员变量（name,price） 的数据放在哪里，存在于哪个位置？

对象中，存在于堆内存中

### 两个对象指向同一个对象的内存图

![](<../.gitbook/assets/image (2) (3).png>)

### 垃圾回收

当堆内存中的对象，没有被任何变量引用（指向）时，就会被判定为内存中的“垃圾”

JAVA 是有自动的垃圾回收站不需要自己清理