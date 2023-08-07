- datastruct: redis 的各类数据结构实现
    - dict: hash 表
    - list: 链表，支持基本的添加、访问、修改和移除操作，以及遍历和范围查询。节点为页
    - lock: 用于锁定 key 的锁组件
    - set： 基于hash表的集合
    - sortedset: 基于跳表实现的有序集合
    - bitmap 用于表示一组二进制位的数据结构，通常用于进行位运算和标记等操作。
    
Redis 数据结构并不是指 String（字符串）对象、List（列表）对象、Hash（哈希）对象、Set（集合）对象和 Zset（有序集合）对象，因为这些是 Redis 键值对中值的数据类型，也就是数据的保存形式，这些对象的底层实现的方式就用到了数据结构。

数据类型与底层数据结构对应关系如下图（转载自小林coding）：
![img](https://pic1.zhimg.com/80/v2-1811a380e3f75ffdfb33869c3e359e6c_1440w.webp)

