# Lambda表达式

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 6.22.46 PM.png" alt=""><figcaption></figcaption></figure>

```
// Code Example
Swimming s1 = () -> {
    System.out.println("~~~");
};

@FunctionInterface // 一旦加上这个注解代表是函数接口，只能有一种抽象方法
Interface Swimming {
    void swim();
}
```

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 6.30.42 PM.png" alt=""><figcaption></figcaption></figure>

### Lambda例子

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 6.33.51 PM.png" alt=""><figcaption></figcaption></figure>

### Lambda省略机制

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 6.34.58 PM.png" alt=""><figcaption></figcaption></figure>
