# 日期时间：Data、SimpleDataFormat、Calendar

### Date

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 2.54.37 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 2.57.14 PM.png" alt=""><figcaption></figcaption></figure>

#### 日期对象如何创建、如何获取时间毫秒值？

* Date date = new Date();
* Long time = date.getTime();

#### 日期对象如何恢复成时间毫秒值？

* Date d = new Date(time);
* d.setTime(time)

### SimpleDateFormat

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.10.46 PM.png" alt=""><figcaption></figcaption></figure>

<div>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.12.34 PM.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.12.39 PM.png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.12.55 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.13.03 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.15.42 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.25.48 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.30.47 PM.png" alt=""><figcaption></figcaption></figure>

### Calendar

#### 概述

* 代表了系统此刻日期对应的日历对象
* 是一个抽象类，不能直接创建对象

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 3.45.37 PM.png" alt=""><figcaption></figcaption></figure>

#### 注意：日历是可变对象，一旦修改后其对象本身表示的时间将产生变化
