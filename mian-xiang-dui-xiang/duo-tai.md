# 多态

### 什么是多态？

同类型的对象，执行同一个行为，会表现出不同的行为特征

### 多态的常见形式

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### 多态中成员访问特点

* 方法调用：编译看左边，运行看右边
* 变量调用：编译看左边，运行也看左边（多态侧重行为多态）

### 多态的前提

* 有继承/实现关系；有父类引用指向子类对象；有方法重写

### 优势

* 在多态形式下，右边对象可以实现解耦合，便于扩展和维护

<figure><img src="../.gitbook/assets/image (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

* 定义方法的时候，使用父类型作为参数，该方法就可以接收这父类的一切子类对象，体现出多态的扩展性与便利

### 产生的问题

* 多态下不能使用子类独有功能

### 多态下引用数据类型的类型转换

#### 自动类型转换（从子到父）：子类对象赋值给父类类型的变量指向

#### 强制类型转换（从父到子）

* 此时必须进行强制类型转换：子类 对象变量 = （子类）父类类型的变量
* 作用：可以解决多态下的劣势，可以实现调用子类独有的功能
* 注意：如果转型后的类型和对象真实类型不是同一个类型，那么在转换的时候就会出现ClassCastException

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>
