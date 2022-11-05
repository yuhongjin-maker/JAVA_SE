# Set系列集合

### Set系列集合特点

* 无序：存取顺序不一样
* 不重复：可以去除重复
* 无索引：没有带索引的方法，所以不能使用普通for循环遍历，也不能通过索引来获取元素

### Set集合实现类特点

* HashSet：无序、不重复、无索引
* LinkedHashSet: 有序、不重复、无索引
* TreeSet: 排序、不重复、无索引

#### Set集合的功能上基本与Collection的API一致

### HashSet底层原理

* HashSet集合底层采取哈希表存储的数据结构
* 哈希表是一种对于增删改查数据性能都较好的结构

### LinkedHashSet集合概述和特点

* 有序、不重复、无索引
* 这里的有序指的是保证存储和取出的元素顺序一致
* 原理：底层数据结构式依然哈希表，只是每个元素又额外的多了一个双链表的机制记录存储的顺序 
<figure><img src="../.gitbook/assets/Screen Shot 2022-11-05 at 6.36.02 PM.png" alt=""><figcaption></figcaption></figure>



### 哈希表的组成

* JDK8之前的，底层使用数组+链表组成

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-03 at 5.43.00 PM.png" alt=""><figcaption></figcaption></figure>

* JDK8开始后，底层采用数组+链表+红黑树组成

#### 当挂在元素下面的数据过多时，查询性能降低，从JDK8开始后，当链表长度超过8的时候，自动转为红黑树

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-03 at 5.50.27 PM.png" alt=""><figcaption></figcaption></figure>

### 哈希表的详细流程

1. 创建一个默认长度为16，默认加载因为0.75的数组，数组名table
2. 根据元素的哈希值跟数组的长度计算出应存入的位置
3. 判断当前位置是否为null，如果null直接存入，如果位置不为null，表示有元素，则调用equals方法比较属性，如果一样，则不存，如果不一样，则存入数组
4. 当数组存满到16\*0.75=12时，就自动扩容，每次扩容原先的两倍

### 哈希值

* 是JDK根据对象的地址，按照某种规则算出来的int类型的数值

### Object类的API

```
// Some code
public int hasCode(): 返回对象的哈希值
```

### 对象的哈希值特点

* 同一个对象多次调用hashCode()方法返回的哈希值是相同的
* 默认情况下，不同对象的哈希值是不同的

