# 集合的并发修改异常问题

### 问题引出

* 当我们从集合中找出某个元素并删除的时候可能出现一种并发修改异常问题

### 哪些遍历存在问题？

* 迭代器遍历集合且直接用集合删除元素的时候可能出现
* 增强for循环遍历集合且直接用集合删除元素的时候可能会出现 （最好不用没有办法解决并发问题 ）

```

List<String> list = new ArrayList<>();
        list.add("Java");

        Iterator<String> it = list.iterator();

        while (it.hasNext()){
            String ele = it.next();
            if("需要删除的String".equals(ele)){
                // list.remove("需要删除的String")
                //会造成并发问题
                it.remove();
                // 使用迭代器删除当前位置的元素,保证不后移
            }
        }
```

* for循环可以通过从后往前删
