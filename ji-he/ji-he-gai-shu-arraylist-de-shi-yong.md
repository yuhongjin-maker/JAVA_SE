# 集合概述、ArrayList的使用

#### 集合与数组类似，也是一种容器，用于装数据的

### 数组的特点

* 数组定义完成并启动后，类型确定、长度固定
* 问题：在个数不能确定，且要进行增删数据操作的时候，数组是不太合适的
* 适合做数据个数和类型确定的场景

### 集合的特点

* 集合的大小不固定，启动后可以动态变化，类型也可以选择不固定
* 集合非常适合做元素个数不确定，且要进行增删操作的业务场景
* 集合的提供了许多丰富、好用的功能，而数组的功能很单一
* 适合做数据个数不确定，且要做增删元素的场景

### ArrayList集合

ArrayList是集合的一种，它支持索引

![](<../.gitbook/assets/image (7) (1).png>)

### ArrayList类如何创建集合对象的，如何添加元素？

* ArrayList list = new ArrayList();
* public boolean add(E,e);
* public void add(int index,E element);

### 泛型概述

#### ArrayList\<E>:其实就是一个泛型类，可以在编译阶段约束集合对象只能操作某种数据类型

注意：集合中只能存储引用类型，不支持基本数据类型

### 如何统一ArrayList集合操作的元素类型？

* 使用泛型：<数据类型>
* ArrayList\<String>list1 = new ArrayList();

![](<../.gitbook/assets/image (8) (1).png>)

