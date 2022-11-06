# Map系列集合

### Map 集合概述和使用

* Map集合是一种双列集合，每个元素包含两个数据
* Map集合的每个元素的格式： key = value (键值对元素)
* Map集合也被称为“键值对集合”

### Map 集合整体格式：

* Collection集合的格式:[元素1，元素2，元素3....]
* Map集合完整格式：{key1=value1,key2=value2,key3=value3,...}

### Map集合体系

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 3.39.11 PM.png" alt=""><figcaption></figcaption></figure>

### Map集合体系特点

* Map集合的特点都是由键决定的
* Map集合的键是无序、不重复的，无索引的，值不做要求（可以重复）
* Map集合后面重复的键对应的值会覆盖前面重复键的值
* Map集合的键值对都可以为null

### Map集合实现类特点

* HashMap:元素按照键是无序，不重复，无索引，值不做要求（与Map体系一致）
* LinkedHashMap:元素按照键是有序，不重复，无索引，值不做要求
* TreeMap：元素按照键是排序，不重复，无索引的，值不做要求

### Map集合常用API

* Map是双列集合的祖宗接口，它的功能是全部双列都可以继承使用的

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 3.48.30 PM.png" alt=""><figcaption></figcaption></figure>

### Map集合的遍历方式一：键找值

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 3.56.57 PM.png" alt=""><figcaption></figcaption></figure>

### Map集合的遍历方式二：键值对

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 4.06.36 PM.png" alt=""><figcaption></figcaption></figure>

### Map集合比那里方式三：lambda表达式

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 4.38.40 PM.png" alt=""><figcaption></figcaption></figure>

### HashMap特点

* HashMap是Map里面的一个实现类。特点都是由键决定的：无序、不重复、无索引
* 没有额外需要学习的特定方法，直接使用Map里面的方法就可以了
* HashMap跟HashSet底层原理是一模一样的，都是哈希表结构，只是HashMap的每个元素包含两个值而已

#### 实际上Set系列集合的底层就是Map实现的，只是Set集合中的元素只要键数据，不要值数据而已

```
// Some Code
public HashSet(){
  
  map = new HashMap<>();
  
}
```
### LinkedHashMap集合概述和特点

* 由键决定：有序、不重复、无索引
* 这里的有序指的是保证存储和取出的元素顺序一致
* 原理：底层数据结构式依然哈希表，只是每个键值对元素又额外的多了一个双链表的机制记录存储的顺序

### TreeMap集合概述和特点

* 由键决定特性：不重复、无索引、可排序
* 可排序：按照键数据的大小默认升序（由小到大）排序。只能对键排序
* 注意：TreeMap集合一定要排序的，可以默认排序，也可以将键按照指定的规则进行排序
* TreeMap跟TreeSet一样底层原理是一样的

#### TreeMap集合自定义排序规则有两种

* 类实现Comparable接口，重写比较规则
* 集合自定义Comparator比较器对象，重写比较规则









