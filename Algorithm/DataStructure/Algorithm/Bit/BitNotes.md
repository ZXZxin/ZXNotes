## 位运算可以实现

1、状态压缩

 用二进制的思想，表示某个数存不存在，1表示存在，0表示不存在

2、成对的思想

```java
0 ^ 1 = 1, 1 ^ 1 = 0
4 ^ 1 = 5, 5 ^ 1 = 4
```

3、lowbit运算

lowbit是得到最后一个1以及后面的数，例如` lowbit(1110010000) = 10000`

```java

n       : 1110010000
~n      : 0001101111
~n+1    : 0001110000
(~n+1)&n: 0000010000 (答案)    
而 (~n+1) = -n
所以
int lowbit(n){
    return (-n) & n ; // (~n + 1) & n;  取反+1 & n 
}
```

