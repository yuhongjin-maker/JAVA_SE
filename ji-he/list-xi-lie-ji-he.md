# List系列集合

### List集合特点

* ArrayList, LinkedList ：有序、可重复、有索引
* 有序：存储和取出的元素顺序一致
* 有索引：可以通过索引操作元素
* 可重复：存储的元素可以重复

### List特有方法

* List因为支持索引，所以多了很多索引操作的独特API，其他Collectioon的功能List也都继承了

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-02 at 2.30.32 PM.png" alt=""><figcaption></figcaption></figure>

#### ArrayList底层基于数组实现的，根据查询速度快，增删相对慢

#### LinkedList底层基于双链表实现的，查询元素慢，增删首尾是非常快的

### List遍历方式

1. 迭代器
2. 增强for循环
3. Lambda表达式
4. for循环（因为List支持索引）

### ArrayList集合底层原理

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-02 at 3.14.27 PM.png" alt=""><figcaption></figcaption></figure>

### &#x20;LinkedList集合底层原理

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-02 at 3.29.18 PM.png" alt=""><figcaption></figcaption></figure>

