# 注解解析

## 注解的解析

* 注解的操作中经常需要进行解析，注解的解析就是判断是否存在注解，存在注解就解析内容

## 与注解解析相关的接口

* Annotation: 注解的顶级接口，注解都是Annotation类型的对象
* AnnotatedElement: 该接口定义了与注解解析相关的解析方法

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-18 at 4.10.22 PM.png" alt=""><figcaption></figcaption></figure>

## 解析注解的技巧

* 注解在哪个成份上，我们就先拿哪个成分对象
* 比如注解作用成员方法，则要获得该成员方法对应的Method对象，再来拿上面的注解
* 比如注解作用在类上，则要该类的Class对象，再来拿上面的注解
* 比如注解作用再成员变量上，则要获得该成员变量对应的Field对象，再来拿上面的注解
