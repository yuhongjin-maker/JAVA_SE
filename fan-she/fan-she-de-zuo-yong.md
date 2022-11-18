# 反射的作用

* 可以在运行时得到一个类的全部成分然后操作
* 可以破坏封装性
* 可以破坏泛型的约束性
* 适合做高级框架

## 绕过编译阶段为集合添加数据

* 反射是作用在运行时的技术，此时集合的泛型将不能产生约束了，此时是可以为集合存入其他任意类型的元素的
* 泛型只是编译阶段可以约束集合只能操作某种数据类型，在编译成Class文件进入运行阶段的时候，其真实类型都是ArrayList，泛型相当于被擦出了

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## 通用框架的底层原理

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
