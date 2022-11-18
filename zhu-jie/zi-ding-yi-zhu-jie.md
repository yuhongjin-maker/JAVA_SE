# 自定义注解

* 自定义注解就是自己做一个注解来使用

```
public @interface 注解名称{

  public 属性类型 属性名() default 默认值
}
``` 

## 特殊属性

* value属性，如果只有一个value属性的情况下，使用value属性的时候可以省略value名称不写
* 但是如果有多个属性，且多个属性没有默认值，那么value名称是不能省略的
