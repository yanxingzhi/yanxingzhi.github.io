---
layout: post
title:  "技术总结"
date:   2021-05-01 10:00:00 +0800
categories: "Technologe"
author: yue.yan
tag: "Technologe"
---

## JVM
### 内存模型
> 线程私有：程序计数器、方法栈、native方法栈  
> 线程公有：方法区、堆


### 垃圾回收
> 标记清除(简单且强大，标记法)  
> 标记复制(经验：朝生夕灭，也就是需要标记是很多的，而且会造成内存碎片，所以诞生标记复制)  
> 标记整理(--)

### 工具(排查问题)
> jstack：栈快照  
> jdump：堆内存快照  

### 类加载机制(双亲委派)
> 类加载器加载机制：类加载器先委派父加载器去加载类，加载不到再由自己加载。
> 好处1：保护核心内不被串改 2：统一管理、减少冗余

### 并发与同步
#### 同步只指让多线程并发执行的更协调的过程
> 原子性  
> 可见性
> volatile 非原子性、可见性、禁止指令重排

#### 锁
> 排它锁    
> CAS无锁算法，线程先持有内存地址的值（旧值），要更改的值即新值，更改前与旧值比较，相同则替换，不同则改变不成功。    
> 锁优化
1. 自旋锁
2. 锁粗化
3. 轻量级锁（无锁）


## Java基础
### 基础数据结构
1. ArrayList    自动扩容
2. HashMap      Hash算法、解决碰撞、位运算、链表、红黑树
3. JUC
4. 线程池
5. 连接池

## Mysql数据库
### 事务隔离级别
> read uncommit  
> read commit  
> repeat read  
> serilizable  
### 事务原理
> 针对的是可重复读，MVVC  

### 索引
#### 索引结构
> Hash  
> B+Tree  
#### 索引原则
> 最左原则
> 索引失效

### 优化
> 主键为什么用自增的INT类型的ID，而不是UUID之类的  

## Redis
### 数据类型
1. String 常用redis锁，就是这种key、value
2. HashMap
3. HashSet
4. 其他（待补充）
### Redis锁
setNX + getAndSet，key设置业务+业务唯一标识；value设置时间戳

## Dubbo（预计5月12号-19号截止）

## RocketMQ（预计21号-28号截止）


