- database: 存储引擎核心
    - server.go: redis 服务实例, 支持多数据库, 持久化, 主从复制等能力
    - database.go: 单个 database 的数据结构和功能
    - router.go: 将命令路由给响应的处理函数
    - keys.go: del、ttl、expire 等通用命令实现
    - string.go: get、set 等字符串命令实现
    - list.go: lpush、lindex 等列表命令实现
    - hash.go: hget、hset 等哈希表命令实现
    - set.go: sadd 等集合命令实现
    - sortedset.go: zadd 等有序集合命令实现
    - pubsub.go: 发布订阅命令实现
    - geo.go: GEO 相关命令实现
    - sys.go: Auth 等系统功能实现
    - transaction.go: 单机事务实现

核心路线：Exec -》execNormalCommand 各个命令通过init方法初始化对应的prepare与executor方法
   
数据类型与底层数据结构对应关系如下图（转载自小林coding）：
![img](https://pic1.zhimg.com/80/v2-1811a380e3f75ffdfb33869c3e359e6c_1440w.webp)
