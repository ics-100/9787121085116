## 第 1 章 温故而知新


**学习记录**

* `Tue Nov  3 15:39:22 CST 2020`


### 1.2 万变不离其宗

* 三个部件最为关键: `cpu` / `内存` / `IO控制芯片`
* 为了协调CPU、内存和高速的图形设备，人民专门设计了一个高速的北桥芯片
* 又设计了专门处理低俗设备的南桥芯片

**SMP与多核**

* 对称多处理器(SMP)
* 多核处理器(Multi-core Processor)

### 1.3 站的高，望的远

* 每个层次之间都需要相互通信，既然需要通信就必须有一个通信的协议，我们一般将其称为`接口(Interface)`
* 接口的下面那层是接口的`提供者`，由它定义接口
* 接口的上面那层是接口的`使用者`，它使用该接口来实现所需要的功能
* `系统调用接口(System call Interface)` -> `应用程序编程接口（Application Programming Interface)`


### 1.4 操作系统做什么

* `多道程序` -> `分时系统` -> `多任务系统`
* `进程` / `抢占式`


### 1.5 内存不够怎么办


**1.5.3 分页**

* 目前几乎所有的PC上的操作系统都使用4KB大小的


### 1.6 种人拾柴火焰高

* 线程，有时被称为轻量级进程(LWP), 是程序执行流的最小单位