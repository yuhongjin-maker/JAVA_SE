# 选择排序、二分查找

### 选择排序

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 5.28.05 PM.png" alt=""><figcaption></figcaption></figure>

### 二分查找

* 二分查询性能好，二分查找的前提是必须是排好序的数据
* 二分查找等于等于每次去掉一半的查找范围
* 二分查找元素不存在 （开始位置min<= 结束位置max）

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-01 at 6.18.47 PM.png" alt=""><figcaption></figcaption></figure>

```
// Code for binarysearch
public static int binarys(int[] arr,int c1) {   
                                                
    int left =0;                                
    int right = arr.length-1;                   
                                                
    while (left<=right){                        
        int index = (left+right)/2;             
        if (arr[index] > c1){                   
            right = index-1;                    
        }else if(arr[index] < c1){              
            left = index+1;                     
        }                                       
         else{                                  
            System.out.println(left);           
            System.out.println(right);          
            return index;                       
        }                                       
    }                                           
    return -1;                                  
```
