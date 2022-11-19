# 注解应用

模拟Junit框架

#### 需求

* 定义若干个方法，只要加了MyTest注解，就可以在启动时被触发执行

#### 分析

1. 定义一个自定义注解MyTest，只能注解方法，存活范围是一直都在
2. 定义若干个方法，只要有@MyTest注解的方法就能在启动时被触发执行，没有这个注解的方法不能执行

```
// Example code
@MyTest
    public void test1(){
        System.out.println("===test1=====");
    }
    
    public void test2(){
        System.out.println("======test2======");
    }

    public static void main(String[] args) {
        AnnotationDemo4 t =new AnnotationDemo4;
        
        //获取类对象
        Class c = AnnotationDemo4.class;
        //提取全部方法
        Method[] methods = c.getDeclaredMethods();
        //遍历方法。看如果有MyTest注解，有就跑它
        for(Method method: methods){
            if(method.isAnnotationPresent(MyTest.class)){
                
                method.invoke(t);
            }
        }
    }
```
