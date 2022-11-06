# 可变参数、集合操作的工具类Collections

### 可变参数

* 可变参数用在形参中可以接收多个数据
* 可变参数的格式： 数据类型....参数名称
```
// Some cod
public static void main(String[] args){
  sums();
  sums(10);
  sums(10,20,30);
  sums(new int[]{10,20,30,40});
}

public static void sum(int...nums){

}
```

### 可变参数的作用

* 传输参数非常灵活，方便。可以不传输参数，可以传输1个或者多个，也可以传输一个数组
* 可变参数在方法内部本质上就是一个数组

### 可变参数的注意事项

1. 一个形参列表中可变参数只能有一个
2. 可变参数必须泛在形参列表的最后面

### Collections集合工具类

* java.utils.Collections是集合工具类
* 作用：Collections并不属于集合，是用来操作集合的工具类

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 1.53.41 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-06 at 1.53.13 PM.png" alt=""><figcaption></figcaption></figure>



