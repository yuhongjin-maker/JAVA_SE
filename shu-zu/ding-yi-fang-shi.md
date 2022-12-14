# 定义方式

**数组的定义**

数组就是用来储存一批同种类型数据的内存区域（容器）

**静态初始化数组**

* 定义数组的时候给数组赋值
* 数组变量名中储存的是数组在内存中的地址，数组是引用类型
* 数组一但定义出来，执行过程中,长度、类型就固定了

**数据类型\[] 数组名 = new 数据类型\[] {元素1,元素2,元素3....};**

**数据类型\[] 数组名 = {元素1,元素2,元素3....};**

**数据访问**

数组长度: 数组名称.length

**动态初始化数组**

定义数组的时候只能确定元素的类型和数组的长度，之后再存入具体数据

**数据类型\[] 数组名 = new 数据类型\[长度]**

两种数组定义时的特点和场景有什么区别：

* 当前已经知道存入的元素值，用静态初始化
* 当前还不知道要存入哪些数据,用动态初始化
* 两种格式的写法不能混用

动态初始化数组后元素的默认值是什么样的？

* byte,short,int,char,long类型数组元素的默认值都是0
* float,double 类型数组元素的默认值都是0.0
* boolean 类型数组元素的默认值是false, String类型数组元素的默认值是null
