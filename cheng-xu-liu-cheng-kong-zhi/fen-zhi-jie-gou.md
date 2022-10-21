# 分支结构

**if 分支**

* if 在功能上远远强大与switch
* if 适合做区间匹配

**switch 分支**

* switch适合做：值匹配的分支选择、代码优雅

```
switch(表达式){
 case 值1：
  执行代码;
  break;
  ......
 default:
  执行代码n;
}
```

**switch使用的注意事项**

* case 给出的值不允许重复，且只能是字面量，不能是变量
* 表达类型只能是byte、short、int、char 不支持double、float、long

**Switch 穿透性**

不要忘记写break
