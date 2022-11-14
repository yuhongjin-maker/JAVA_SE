# 新增方法、注意事项

#### JDK8版本开始后，Java只对接口的成员方法进行了新增

允许接口中直接定义带有方法体的方法

### 第一种：默认方法

* 类似之前写的普通实例方法：必须用default修饰
* 默认会public修饰。需要用接口的实现类的对象来调用

<figure><img src="../.gitbook/assets/image (5) (3).png" alt=""><figcaption></figcaption></figure>

### 第二种：静态方法

* 默认会public修饰，必须有static修饰
* 注意：接口的静态方法必须用本身的接口名来调用

<figure><img src="../.gitbook/assets/image (4) (3) (1).png" alt=""><figcaption></figcaption></figure>

### 第三种：私有方法

* 就是私有的实例方法：必须使用private 修饰，从JDK1.9才开始有的
* 只能在本类中被其他的默认方法或者私有方法访问

<figure><img src="../.gitbook/assets/image (3) (1) (3).png" alt=""><figcaption></figcaption></figure>

### 注意事项

* 接口不能创建对象
* 一个类实现多个接口，多个接口中有同样的静态方法不冲突，A调用A的，B调用B的
* 一个类继承了父类，同时又实现了接口。父类中和接口中有同名方法，默认用父类的
* 一个类实现类多个接口，多个接口有同名的默认方法。冲突，这个类重写该方法即可
* 一个接口继承多个接口，是没有问题的，如果多个接口中存在规范冲突贼不能多继承
