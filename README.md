Java高并发秒杀系统
# seckill
Java高并发秒杀系统
## 秒杀业务

秒杀主要包括两个主要业务：减库存、记录购买明细

两者组成完整的事务。

## 功能

- 秒杀接口暴露
- 秒杀操作
- 相关查询
## 难点

秒杀商品竞争：事务+行级锁

如何过滤重复：使用秒杀id和手机号做联合主键

- 如何处理竞争是关键

### 事务
- Start Transaction
- update库存
- insert购买明细
- commit
