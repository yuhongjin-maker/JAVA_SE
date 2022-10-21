# 案例技术：Random类、猜数字游戏

**随机数Random类**

* 作用: 用于在程序中获取随机数的技术

1. 导包: 告诉JDK的哪个包中找随机数技术 -> import java.util.Random;
2. 写一行代码代表得到随机数对象 (Random r = new Random());
3.  用随机数的功能获取0-9的随机数 (int number = r.nextInt(10));

    nextInt(n) 功能只能生成: 0至n-1之间的随机数,不包含n nextInt(a,b) 不包含b：a至b-1之间的随机数

例如：生成1-10之间的随机数 思路:(10-1) => (0-9)+1 Random r = new Random(); int number = r.nextInt(10)+1;

