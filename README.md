# glusterfs-book
作为国内第一本glusterfs的书籍，方便大家学习了解
## 为什么写这本书? 
  &nbsp; &nbsp; 对于这个问题，萌生这种想法是从2020年下半年，因为转变方向开始接触glusterfs开始的。对于glusterfs，一开始在网上搜了很多资料，但是大部分资料的内容都是残缺不全的，并且没有一本专业系统的技术书来专门讲述glusterfs。而glusterfs作为世界上与ceph、hdfs齐名的分布式存储系统，但是资料却完全无法和这两者相比，这是不应该的。因此在2021年五月下旬的时候，和朋友一起聊天时，激起了想专门写一本glusterfs书的想法，抱着尝试的心态，通过阅读源码资料，还有国内外的一些信息，慢慢不断地整合学习，才有了这本书的诞生。当然这本书作为本人工作生涯的第一本书，写下这本书的时候，恰好也是工作第三年了，对于程序员的职业生涯来说，这算是迈向了一个新的阶段了，给自己一个新的礼物吧。

## 目录大纲
 ```
 前言	
1. 第一章让集群先跑起来	
  1.1. 我们为什么要用glusterfs	
  1.2. 先让glusterfs跑起来	
    1.2.1. 简单概念介绍	
    1.2.2. 一些有趣的volume	
    1.2.3. 仲裁节点arbiter	
    1.2.4. 集群的相关日志文件	
  章节语:
2. 第二章 文件系统的那些事	
  2.1. 文件系统的层次结构	
    2.1.1. 有趣的VFS和文件系统	
    2.1.2. page cahe的作用	
    2.1.3. Fuse block	
  章节语:
3. 第三章 glusterfs的核心概念	
  3.1. 有趣的扩展属性gfid	
    3.1.1. 文件的gfid属性	
    3.1.2. 目录的gfid属性	
  3.2. 数据内存模型	
    3.2.1. loc_t结构	
    3.2.2. inode_t结构	
    3.2.3. dentry_t 结构	
    3.2.4. fd_t 结构	
  3.3. posix接口的那些事	
    3.3.1. posix_lookup	
    3.3.2. posix_open	
    3.3.3. gluster fop	
    3.3.4. posix_mkdir	
    3.3.5. posix_create	
  3.4. 一些重要的概念与进程	
    3.4.1. 代码模块功能xlator	
    3.4.2. glusterfs的几个重要进程	
    3.4.3. graph和volfile	
    3.4.4. 异步回调STACK_WIND	
    3.4.5. inode相关问题	
  3.5. 内存跟踪调用	
    3.5.1. mem_acct	
    3.5.2. xlator_init	
    3.5.3. GF_CALLOC	
    3.5.4. GF_FREE	
    3.5.5. statedump	
    3.5.6. io thread	
  3.6. index模块	
    3.6.1. dirty目录	
    3.6.2. xattrop目录	
    3.6.3. entry-changes目录	
    3.6.4. heal 连接数	
    3.6.5. AFR	
  章节语:	
4. 第四章 glusterfs的特性	
  4.1. quota容量限制	
    4.1.1. 开启quota功能	
    4.1.2. quota对不同volume的使用	
    4.1.3. quota真的能限制大小吗？	
    4.1.4. quota监控	
  4.2. 偷懒的快照snapshot	
    4.2.1. lvm2原理	
    4.2.2. lvm2命令的使用	
    4.2.3. snapshot创建	
    4.2.4. 快照回滚	
    4.2.5. 删除快照	
  4.3. 防止误删数据的trash	
  4.4. 简洁的客户端coreutils	
  4.5. 强大的webhook event	
  4.6. 麻烦的扩缩容	
    4.6.1. add-brick操作	
    4.6.2. remove-brick操作	
    4.6.3. replace-brick操作	
    4.6.4. rebalance很重要	
  4.7. 性能管家profile和top	
  章节语:
5. 第五章 参数与性能优化	
  5.1.   那些有趣的参数	
    5.1.1. rebalance相关	
    5.1.2. 服务和性能相关	
    5.1.3. 日志相关	
    5.1.4. heal相关	
  5.2. linux系统优化	
  章节语:
6. 第六章 运维之路	
  6.1. 难受的运维经历	
  6.2. 周边生态项目	
  6.3. 未来还能做什么	
  章节语:	
 ```
