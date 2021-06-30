0000 此节介绍runtime数据存储的设计。包括区块链存储的不同点和约束，substrate存储单元的类型，存储的初始化，最佳实践。

0035 区块链存储的不同点和约束

0250 substrate存储单元类型  
0335 回顾上节课所学的storage宏  

0357 单值类型  
0542 以数值u8类型举例  
0700 单值类型常用api  
0708 数值类型的安全操作  
0815 大整数类型的定义和api  
0850 bool 布尔类型定义  
0924 集合类型 Vec<T> vector 定义。api  
1037 定点小数 percent，permill，perbill类型定义  
1228 Moment 时间类型定义，获取链上时间  
1334 AccountId 账户类型定义  
1400 struct类型定义  
1444 enum类型定义，类似于struct

1500 以上是单值类型，这里介绍简单映射类型。StorageMap 类型，用来保存键值对，之前说的单值类型都可以用作key或value使用。  
1629 StorageMap 常用api

1720 双键映射类型 StorageDoubleMap，使用两个key索引一个value，用于快速删除或遍历key1对应的所有记录。  
1823 不同情形的hash算法选择  
1854 api  

1943 存储的初始化

2110 最佳实践

2236 其它tips