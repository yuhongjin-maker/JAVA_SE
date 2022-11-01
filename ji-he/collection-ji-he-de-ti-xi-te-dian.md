# Collection集合的体系特点

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 7.29.38 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 7.32.28 PM.png" alt=""><figcaption></figcaption></figure>

### Collection 集合（接口）特点

#### List系列集合：添加的元素有序、可重复、有索引

* ArrayList、LinkedList:有序、可重复、有索引

#### &#x20;Set系列集合：添加的元素无序、不重复、无索引

* HashSet:无序、不重复、无索引
* LinkedSet:有序、不重复、无索引
* TreeSet: 按照大小默认升序排序、不重复、无索引

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 7.40.43 PM.png" alt=""><figcaption></figcaption></figure>

```
// JDK7后后面类型声明可以不写
Collection<String> list2 = new ArrayList<>();
```

### 如何约定集合存储数据的类型

* 集合支持泛型
* 集合和泛型不支持基本数据类型，只支持引用数据类型
