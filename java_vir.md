# 走进java

从了解java体系历史 ，到手动编译虚拟机，从而接触java 为了能合适使用，需要对虚拟机有所了解，才能让java程序运行的更稳定，性能更好的发挥

概貌

- 是什么？
- 为什么？
- 怎么做？

理解事物就是为了解决这几个问题

# 自动内存管理机制
## 运行时数据区
- 方法区
- 虚拟机栈
- 本地方法栈
- 堆
- 程序计数器

目前内存的动态分配与内存回收技术已经相当成熟，那为什么了解GC和内存分配？
> 当需要排查各种内存溢出、 内存泄漏问题时， 当垃圾收集成为系统达到更高并发量的瓶颈时， 我
们就需要对这些“自动化”的技术实施必要的监控和调节

## 判断对象是否存活
- 引用计数算法

缺点：很难解决对象之间相互循环引用的问题

- 可达性分析算法

主流实现

对于已经判定对象是不可达的，也不能并非是‘非死不可’的。这就需要垃圾收集算法

## 垃圾收集算法

- 标记-清除算法
问题：效率问题，空间问题   效率低 会产生内存碎片

- 复制算法

- 标记-整理算法
- 分代收集算法
主流实现


> 总结：对象存活判定算法 和 垃圾收集算法

## JDK的命令行工具
jps：虚拟机进程状况工具


> 总结：随JDK发布的6个命令行工具及两个可视化的故障处理工具

# 虚拟机执行子系统

# 代码编译和代码优化


# 面试题
带着问题去找答案
1. 介绍下Java内存区域（运行时数据区）
Java虚拟机在执行Java程序的过程中会把它所管理的内存划分为以下6个运行时数据区域
- 程序计数器（Program Counter Register）
- Java虚拟机栈（Java Virtual Machine Stacks）
- 本地方法栈（Native Method Stack）
- Java堆（Java Heap）
- 方法区（Method Area）
- 运行时常量池（Runtime Constant Pool）

2. 怎么判定对象已经“死去”？

