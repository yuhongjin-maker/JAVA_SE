# 反射概述

* 反射是指对于任何一个Class类，在“运行的时候”都可以直接得到这个类的全部成分
* 在运行时，可以直接得到这个类的构造器对象：Constructor
* 在运行时，可以直接得到这个类的成员变量对象：Field
* 在运行时，可以直接得到这个类的成员方法对象：Method
* 这种运行时动态获取类信息以及动态调用类中成分的能力称为Java语言的反射机制

## 反射的关键

* 反射的第一步都是先得到编译后的Class类对象，然后就可以得到Class的全部成分

```
HelloWorld.java -> javac -> HelloWorld.class
Class c= HelloWorld.class;
```



