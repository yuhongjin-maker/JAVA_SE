# Collection 常见API、遍历方式、存储自定义类型的对象

### Collection集合的常用API

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 7.53.52 PM.png" alt=""><figcaption></figcaption></figure>

### Collection集合的常用遍历方式

#### 方法一：迭代器

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 7.57.13 PM.png" alt=""><figcaption></figcaption></figure>

```
Collection list<String> = new ArrayList<>();
Iterator<String> it = lists.iterator();
while(it.hasNext()){
    String ele = it.next();
    System.out.println(ele);
        }
```

注意：

* 迭代器默认指当前集合的索引0
* 迭代器如果取元素越界会出现NoSuchElementException异常

#### 方法二：foreach/增强for循环

#### 方法三：lambda表达式
