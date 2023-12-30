

# Operating System



## Week1

### 1.操作系统概述

#### 1.1**Defination:**

操作系统是管理计算机硬件的程序，它还为应用程序提供基础，并且充当计算机硬件和计算机用户的中介。

An operating system acts as an intermediary between **a user** and **the computer hardware**
操作系统主要有以下操作方式：

- 管理程序的开始与结束并在程序间共享CPU
- 管理内存
- 输入输出
- 文件管理系统
- 保护



#### 1.2 计算机系统的组成成分

自下而上

![image-20220527120000171](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527120000171.png)

### 2.进程(Process)

* 进程process代表一个正在运行的程序
* 程序program代表被存储在硬盘空间内的代码，是一个被动的实体。

#### 2.1 进程的状态

As a process executes, it changes state.
当进程执行时，会改变状态，状态象征着进程当前活动：
1. new：被创建
2. running：指令正在被执行
3. waiting：进程需要用户输入或其他进程运行结果而等待
4. ready：已就绪，可以被执行
5. terminated：被终止

![image-20220405161308899](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220405161308899.png)

#### 2.2 PCB进程控制块(Process Control Block)

定义：一种在操作系统核心中的一种**数据结构**，本质上是数据结构-链表linked list。存储了**一个**进程的**相关信息**。主要用来表示进程的状态。所有进程的PCB都被包含在主存中。进程对于多道（multiprogramming  environment ）有相当重要的作用。

![image-20220405161919959](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220405161919959.png)

#### 2.3 进程调度概述

定义：进程调度一般是从某个地方选择进程，然后将其转移到另一个地方。

一般维护以下进程：

1. **作业队列**Job queue：系统内所有进程的集合
2. **就绪队**列Ready queue：处于就绪状态的进程
3. **设备队列**Device queues：等待I/O设备输入输出的进程队列

三种调度类型：

1. 长期调度（Long-Term Scheduler，Job Scheduler）也称**作业调度**,根据进程池中的所有进程进行规划并调度，选择一个或一批进程进入内存，作业完成后还需负责回收系统资源。
2. 中期调度（Medium-term scheduler）将需要等待I/O的进程移出内存，存储于磁盘上，降低多道设计的程度，需要时再换回内存中-swapping

3. **短期调度** （Short-Term scheduler，CPU scheduler）选择一个就绪队列里的进程占据CPU运行，也是常说的调度

##### 2.3.1上下文切换(Context Switch)

当CPU内的进程发生**切换Switch**（中断或系统调用）时，需要将被切换的进程的相关信息（临时变量，状态等）存储进PCB，同时，读取切进来的进程的相关信息，这个过程被称为上下文切换。

![image-20220405162903182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220405162903182.png)

#### 2.4 对进程的操作(Operations on Processes)

系统需要提供进程的<font color='red'>创建creation</font>和<font color = 'red'>终止termination</font>操作（mechanisms）。

1.创建进程：

进程可以被进程创建，例如，一个父母进程创建一个子进程。通过进程间的创建，可以形成一个进程树，进程树上的每个节点通过pid（process identifier进程标识符）来唯一地被标识。

* 三种资源策略：
  * 父母进程与子进程共享所有的资源
  * 共享部分资源
  * 不共享资源

* 执行策略：
  * 父母进程和子进程同时执行。
  * 子进程被终止后，父母进程被终止。

2.终止进程

1. 在进程执行最后一条语句，然后使用系统调用exit()让系统终止该进程。 
2. 父进程也可以用exit()终止子进程。

![image-20220527121503772](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527121503772.png)

#### 2.5 进程间的通信(Inter-process Communication)

##### 2.5.1 进程的种类

**1.独立进程(Independent Processes)**

​	<font color='red'>不与其他进程相互影响的进程</font>

**2.合作进程(Cooperating Processes)**

​	会被其他进程影响的进程。一般在以下几个方面

* 资源共享information sharing：多个用户浏览同一资源
* 计算加速computation speedup：并行计算提高速度
* 模块化modularity：按照模块化方式构造系统
* 便利性convenience：单个用户可能同时执行多个任务



##### 2.5.2 进程的通信方式（Communication Models）

分成两种方式：<font color='red'>**内存共享和消息传递**</font>

同时都使用一个叫缓冲区buffer的存储空间来存储消息。

**1.内存共享**(Shared-Memory)

processes can be able to exchange information by reading and writing all the data to the shared region
通过读写同一片缓冲区buffer的信息去达到交换信息的目的

访问同片缓冲区代表着**临界区问题**

- 当缓冲区容量有限时（Bounded capacity）：缓冲区的存储信息有上限
- 当缓冲区容量无限时（Unbounded capacity）：缓冲区存放信息没有限制

**2.消息传递(Message-Passing)**

合作进程间通过消息发送与交换共享信息，主要有两种操作：
<font color='red'>send(message)和receive(message)：发送和接收</font>

1. 消息传递方法传递的消息存储在<font color='red'>**临时队列**</font>中(邮箱）： 
   · **零容量(Zero capacity)**：临时队列中不能有未被接受的消息(每一条消息都应被接受，然后下一条消息被发送）
   · **有限容量(Bounded capacity)**：临时队列有限，至多可以存储n条消息
   · 无**限容量(Unbounded capacity)**：临时队列长度无限。
2. 如果进程P和Q想要通信，则他们之间必须要有连结。这种连结可以是直接的，也可以是间接的：
   · **直接通信（direct communication）**：将消息直接发送给另外一个进程，在这之前接受者不知道聊天对象。
   · **间接通信（indirect communication**）：设置**临时队列（temporary queue）**，合作进程将消息发送给临时队列，又能够从临时队列收取消息。
3. 消息传递可以是**同步**的，也可以是**异步**的：
   · 同步（Synchronous）：又被称为阻塞(blocking)
   Blocking send: 当消息被发送，发送者会被阻塞，直到接收者接受消息。
   Blocking receive: 接收者会被阻塞，直到接收新消息
   · 异步（Asynchronous）：又被称为非阻塞(non-blocking)
   Non-blocking send: 发送者可以发送消息然后继续运行
   Non-blocking receive: 接收者可以在任意时刻接受消息, 消息可能有效可能为空

![image-20220527121921079](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527121921079.png)

## Week2

### 1. 线程(Thread)

A thread is the smallest unit of processing that can be performed in an OS.
Thread is a fundamental unit of CPU utilization that forms the basis of multithreaded computer systems

- 线程是计算机操作系统执行的基本单元，也是<font color='red'>CPU使用的基本单元。</font>
- 线程也可以看成是简化的进程；
- 属于同一个进程的线程之间可以共享代码，数据，文件；
- 线程能够帮助程序“同时”执行多个任务。

#### 1.1线程的组成成分

<font color='red'>**线程ID，程序指针，寄存器集，栈**</font>

#### 1.2 线程状态

* 未创建的线程处于undefined状态；
* 当线程就绪时，处于ready状态；
* 同一时刻**只能有一个线程**处于running状态
* 当线程被中断运行（suspend），处于suspended状态，随后可调用resume（）回归就绪状态
* 处于中断terminated状态的进程会被释放，随后处于销毁destroyed状态
  

#### 1.3 单线程进程和多线程进程(Single and Multithreaded Processes)

1 传统讲的单线程进程，任务被分配给了一个进程，其内只有一个线程，发生错误这个任务就挂掉了。

2 多线程进程，进程其内变成了多个线程，任务被分配给了许多线程，如果一个线程挂了对其他线程没影响，it can perform more than one task at time.可以同时进行超过一个任务。

#### 1.4 并发和并行（Concurrency vs. Parallelism）

**并发和并行的区别为：意思不同、侧重不同、处理不同。**

**一、意思不同**

1、并发：并发是指两个或多个事件在同一时间间隔发生。

2、并行：并行是指两个或者多个事件在同一时刻发生。

**二、侧重不同**

1、并发：并发侧重于在同一实体上。

2、并行：并行侧重于在不同实体上。

**三、处理不同**

1、<font color='red'>并发：并发在一台处理器上“同时”处理多个任务。（伪同时，实际上只能同时处理一件事物）</font>

2、<font color='red'>并行：并行在多台处理器上同时处理多个任务。</font>

##### 1.4.1 单核系统

<font color='blue'>单核系统(Concurrent execution on single-core system)</font>并发处理任务，进程一个一个开始，中间互相穿插运行，直到结束完成。（一会吃饭一会看手机）

![image-20220527134555239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527134555239.png)

##### 1.4.2 多核系统

<font color='blue'>多核系统(Parallelism on a multi-core system)</font>并行处理任务能够同时处理多个任务（一边吃饭一边看手机）

![image-20220527134719316](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527134719316.png)

##### 1.4.3 阿姆达尔定律(Amdahl`s Law)

![image-20220405214818583](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220405214818583.png)

#### 1.5 用户线程和内核线程

##### 1.5.1 用户线程(User Threads-ULT)

<font color='blue'>用户线程</font>：由用户实现的执行单元，这些线程受内核支持但是内核不管理这些线程。用户线程比系统线程快。

用户线程管理由用户级线程库实现。主要的用户级线程库包括：POSIX Pthreads, Win32 threads, Java threads。
通过使用**线程库thread library**来调度这些线程。

###### 1.5.1.1 用户线程的优缺点

Advantages: 

1. 线程切换不涉及内核:没有模式切换
2. 速度块
3. 调度可以是特定于应用程序的:根据情况选择最佳算法。
4. 可以在任何操作系统上运行。我们只需要一个线程库

Disadvantages:

1. 大多数系统调用会阻塞进程。因此，进程中的所有线程都会被隐式阻塞

2. 内核只能将处理器分配给进程。

   同一个进程中的两个线程不能同时在两个处理器上运行。<font color='blue'>相同进程的线程不能在多个处理器上运行。</font>

##### 1.5.2 核线程(Kernel Threads- KLT)

<font color = 'blue'>核线程</font>：又被称为内核线程和系统线程。由内核安排在CPU上执行的线程。
核线程管理通过OS核控制。比如WIndows，Linux，Mac OS。**(核线程被操作系统直接管理)**

![image-20220405215214666](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220405215214666.png)

###### 1.5.2 核线程的优缺点

Advantages:

1. 内核可以在多个处理器上调度同一个进程的多个线程.

2. 线程级阻塞，而不是进程级阻塞

   1. 如果线程阻塞，则

      CPU可以分配给同一个进程中的另一个线程

3. 甚至内核例程也可以是多线程的

Disadvantages:

1. 线程切换总是涉及到内核。这意味着每个线程切换意味着2个模式切换。
2. 比用户线程更慢（但比全流程切换要快）

##### 1.5.3 ULT和KLT之间的关系

*当用户线程执行时，需要将线程到内核线程才能执行。*

##### 1.5.4 轻量级进程 （Lightweight Processes - LWP）

内核线程和用户线程之间的层。

![image-20220527141216979](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527141216979.png)

![image-20220527141304930](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527141304930.png)

#### 1.6 多线程模型

##### 1.6.1 Many-to-One Model

多对一模型将许多用户级线程映射到一个内核线程。<font color='red'>线程管理是由线程库在用户空间进行的，因而**效率比较高**。但是如果**一个线程阻塞了系统调用，那么整个线程都会阻塞**。</font>而且，因为任一时刻都只有一个线程能访问内核，多个线程不能并行运行在多处理器上。多对一模型不限制用户线程数量。
Used on systems that do not support kernel threads.
<font color='blue'>用于不支持内核线程的系统</font>.

![image-20220527141743594](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527141743594.png)



##### 1.6.2 One-to-One Model

一对一模型将每个用户线程映射到一个内核线程。<font color='red'>该模型在一个线程执行阻塞系统调用时，能允许另一个线程继续执行，所以它提供了比多对一模型**更好的并发性**。</font>同时，它也允许多个线程能并行地运行在多处理器系统上。这种模型的唯一<font color='red'>缺点是每创建一个用户线程就要创建一个相应的内核线程。由于创建内核线程的开销会影响应用程序的性能，所以这种模型的绝大多数实现**限制了系统所支持的线程数量(用户线程)**。</font>(Winodows,Linux都属于这种模型)
Used on systems that do not support kernel threads.
<font color='blue'>用于不支持内核线程的系统</font>

![image-20220527142151999](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527142151999.png)



##### 1.6.3 Many-to-Many Model

多对多模型多路复用了许多用户线程映射到**同样数量或更小数量**(因为不可能内核线程大于用户线程数量，这是一种浪费)的内核线程。**多对多模型不限制用户线程数量，可并发**。

![image-20220527142258435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527142258435.png)

##### 1.6.4 两级模型

可以理解为多对多模型和一对一模型的结合。允许多个用户线程竞争内核线程资源，也允许某些用户线程与内核线程绑定。**多对多模型不限制用户线程数量，可并发**。

![image-20220527142404239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527142404239.png)

#### 1.7 线程库(Thread Libraries)

**是个Application Programming Interface (API)接口**，程序员可以用它在应用里创建和管理线程。

##### 1.7.2 创造Thread Libraries的两种方式

* 创造一个在用户空间中提供库（Library entirely in user space）没有内核支持。意味着库的所有代码和数据存放在用户空间，调用时不会使用系统调用。

* 实现内核级别库（kernel-level library ），库和代码放在内核空间中，调用这些函数会使用系统调用

  

* 三个主要的线程库：POSIX Pthreads，Win32，Java

#### 1.8 Implicit Threading（隐式线程）

##### 1.8.1 创建线程(Thread creation)

<font color='red'>**异步**</font>：父线程创建子线程然后互不影响，几乎不需要数据共享。
<font color='red'>**同步**</font>：父线程需要等待子线程结束运行，需要较多数据共享。

##### 1.8.2 线程的种类

1. 由程序员手动创建的叫<font color='red'>显式线程（explicit threading）</font>
2. 编译器和即时库创建的线程叫<font color='red'>隐式线程（implicit threading）</font>

##### 1.8.3 设计多线程的三种方式

###### 1.8.3.1 Thread pool线程池

在进程启动时创建一些线程，并将它们放入一个池中，它们在池中等待工作。

###### 1.8.3.2 OpenMP是个指令集

OpenMP是一组编译器指令，可用于C、c++和Fortran程序.它指示编译器在适当的地方自动生成并行代码。

###### 1.8.3.3 Grand Central Dispatch (GCD) 

GCD——是C和c++的扩展，在苹果的MacOS X和iOS操作系统上支持并行。



#### 1.9 设计多线程程序/ 多线程问题

##### 1.9.1fork（）和exec（）调用

###### 1.9.1.1 fork()

当fork（）被调用，<font color='red'>会产生个线程，一个父级，一个子级；他们俩的代码段，数据和堆栈完全相同。</font>

![image-20220527144412391](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527144412391.png)

###### 1.9.1.2 exec()

当exec（）被调用，<font color='red'>当前线程执行的程序会被替换成另一个程序</font>，进程ID未变，以别的程序替代了该线程的代码段，数据和堆栈。

![image-20220527144428562](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527144428562.png)



##### 1.9.2信号处理Signal handling

<font color='red'>信号用来通知进程某个特定事件已经发生了。根据需要通知的信号的来源和事件的理由，信号可以同步或异步吸收。</font>

###### 1.9.2.1 同步信号和异步信号

Unix/Linux系统相应某个条件或操作而生成的中断或时间，由signal handler处理，且每个信号只处理一次，信号大致有以下几种：
**异步信号**asynchronous signal：发信号后不等待。

**同步信号**synchronous signal ：发送信号后死等。

##### 1.9.2.2 线程取消Thread Cancellation


在线程完成之前关闭线程（如：加载页面时点击取消）
能通过以下方式关闭：
· **Asynchronous cancellation** 异步取消：立即终止。
· **Deferred cancellation** 延期取消：允许目标线程检查然后自己终止。

## Week3

### 1.进程同步(Process Synchronization)

PS is the task of coordinating the execution of processes in a way that no two processes can have access to the same shared data and resources.
两个进程不能同时访问共享资源。PS的任务是协调进程的执行，使任何两个进程都不能访问相同的共享数据和资源。

#### 1.1竞争条件（Race condition）

当多个进程同时访问和操作统一数据，数据的结果因代码执行顺序而异，导致数据的不一致。
To prevent race conditions, concurrent processes must be synchronized
<font color='red'>为了防止竞争，必须同步并发的进程。</font>

![image-20220527160410465](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527160410465.png)

![image-20220527160447239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527160447239.png)



#### 1.2 同步

同步发生在协作进程之间，基础思想是需要一个任何形式的锁。

### 2. 临界区问题(Critical Section Problems)

**临界区**<font color='red'>即是会**访问共享资源的代码区**（改变共同变量，读写文件等）</font>，我们需要控制程序进入这段代码的时机。
	· **进入区**：控制进入临界区
	· **临界区**：这之内的代码会访问共享资源
	· **退出区**：告诉其他进程该进程退出了邻接区

<font color='red'>简单的来说，就是多个线程对同一个代码区进行访问处理，导致代码区的数据实时在变化而可能造成不同的结构</font>

![image-20220527160240227](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527160240227.png)

共享对象

1. 可以从堆中动态分配
2. 可以在全局变量中声明static而静态分配

多线程访问共享对象

1. 如果对象是动态分配的，则每个线程都需要一个指向它的指针
2. 如果对象是静态的，线程只需要通过全局变量名引用它，编译器会计算相应的地址。

#### 2.1 临界区的三个原则

##### 2.1.1.**互斥**（mutual exclusion）：

当一个进程/线程在其临界区执行时，其他进程/线程不能在其临界区执行。

##### 2.1.2.**前进**（progress）：

如果临界区中没有进程/线程在执行，并且有一些进程/线程希望进入它们的临界区，那么其中一个进程/线程将进入临界区。它必须是可能的谈判谁将继续下一个进入CS(Critical Section)

##### 2.1.3.**有限等待**（bounded waiting）：

进程做出进入临界区请求后，其他进程进入临界区的次数是有上限的，进程发出请求后等待允许的时间有限。

#### 2.2 处理临界区的两种内核

1. **抢占式(Premptive Kernel)**: 允许进程在内核模式下运行时可以被抢占。
2. **非抢占式(non-preemptive kernel)**: 进程在内核模式运行时不会被抢占，不会产生竞争。

#### 2.3 临界区问题的解决方法

每个方法都要遵循<font color='red'>互斥，前进，有限等待</font>三个原则

1. Peterson’s solution
2. Hardware solution/Synchronization Hardware
3. Mutex lock
4. Semaphores

![image-20220527161449318](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527161449318.png)

个人认为核心观点是：在某个线程对代码段进行修改时，其他线程不能同时参与。必须等现在的线程结束后再对这个代码端进行修改。



##### 2.3.1. Peterson’s solution(彼得森解法)

<font color='red'>属于Software Solution</font>

**维护 int turn 和 boolean flag[2]**
**turn表示下一张门票；flag表明现在谁在内**

1. 这一次要进去之前把自己flag设为true表示我要进去。
2. 然后把下一次进去的机会turn留给对面，对面flag是true则自己不被允许进入临界区，只有这次机会在自己这里并且对面falg为flase自己才能进去。

自己出来临界区后把自己flag设为flase表示自己出来了，这样对面就可以进入临界区。


![image-20220406232424289](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220406232424289.png)

![image-20220527161847581](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527161847581.png)

**Explation：**

1.在进入部分，进程P0首先升起一个标志，表示希望进入临界部分。

2.然后将turn设为1，如果进程P1希望，则允许其他进程进入临界区。

3.while循环是一个繁忙循环，只要进程P1有机会进入临界段，进程P0就会等待。

4.进程P0在退出部分降低标志[0]，如果进程P1一直在等待，则允许它继续。

[Peterson算法](https://blog.csdn.net/qq_41882686/article/details/112614568)





###### 2.3.1.1 Drawbacks of Software Solutions

1. 复杂的程序
2. 繁忙等待(Busy Waiting)(浪费的CPU周期)
3. 阻塞正在等待的进程(就像它们请求I/O一样)会更有效。

##### 2.3.2 Solution to CS Problem using Locks

![image-20220527163159225](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527163159225.png)

<font color='red'>每次进入后都把修改的代码段锁死。出去后再解开。</font>

##### 2.3.3.Hardware Solutions(硬件处理)

由硬件支持的同步，都是关于**锁**的

许多现代计算机系统提供了**特殊硬件指令**以允许能**原子地**检查和修改字的内容或交换两个字的内容。

###### 2.3.3.1 单处理器环境(Single-processor environment)

<font color='red'>临界区有全局变量lock，只有lock是false是可以进入。进入时检查lock是否为F，申请到了后后置为T，退出时置为F。</font>

![image-20220406232840865](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220406232840865.png)

###### 2.3.3.2多处理器环境(Multi-processor environment)

<font color='red'>全局变量lock，只有lock为0时才进入，申请成功后交换（0,1）状态，退出时置为0，适用于多处理器环境.</font>

![image-20220406232947572](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220406232947572.png)

###### 2.3.3.3 Hardware Solution的优缺点

Advantages:

1. 适用于共享主内存的单个处理器或多个处理器上的任意数量的进程.
2. 简单，易于验证
3. 可支持多个critical section;每个critical section都可以由它自己的变量定义.

Disadvantages:

1. <font color='red'>Busy-waiting </font>当进程等待访问临界区时，它会继续消耗处理器时间
2. <font color='red'>Starvation</font> 当一个进程离开临界区，并且有多个进程在等待时，就可能出现饥饿Starvation
3. <font color='red'>Deadlock</font> 如果低优先级进程拥有临界区域，而高优先级进程需要临界区域，则可能出现死锁，高优先级进程将获得处理器等待临界区域。

### 3. 互斥锁/互斥Mutex Locks/Mutual exclusion

基于软件，允许多个程序线程不同时地访问同个资源。

1. **核层面实现互斥时**，会发生中断，导致上下文切换。为了减小中断可能对数据造成的损害，尽可能做完原语再中断，原语既完成一个数据操作的最小代码。
2. **软件层面互斥**，进程处于运行状态，需要忙等或产生自旋锁busy-wait mechanism or spinlock，既一直在循环检查是否被允许。

**进程在进入前需要申请锁，退出临界区需要释放锁。**

![image-20220527170948357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527170948357.png)

![image-20220527171014097](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527171014097.png)

### 4. 信号量 Semaphores

*在看信号量时，有一个困扰我的问题。如果Peterson是利用软件实现的，硬件同步是利用特定硬件指令实现的。那信号量不也是软件吗。“基于硬件的临界区问题的解决方案，对于应用程序员而言，使用比较复杂。为了解决这个困难，可以使用称为**信号量(semaphore)的同步工具**。”*

##### 4.1 信号量的属性

 信号量S是一个**整数变量**，除了初始化外，它只能通过两个标准**原子操作**<font color='red'>wait()和signal()</font>来访问。这些操作原来被称为**P**和**V**。

###### 4.1.1 wait（）
信号量小于等于0就Busy wait(死循环)，大于0就减一，**代表申请到了锁。**

![image-20220527171710843](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527171710843.png)

###### 4.1.2.signal（）

信号量加1，**代表锁被释放**。

![image-20220527171720883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527171720883.png)

##### 4.2 两种信号量的分类

· <font color='red'>计数信号量 COUNTING SEMAPHORE</font>
· <font color='red'>二进制信号量 BINARY SEMAPHORE</font>

###### 4.2.1计数信号量

信号量S被初始化为可用资源的数量，函数wait（）和signal（）定义不变，S代表着当时剩余的可用资源的数量。

###### 4.2.2 二进制信号量

也被称为互斥锁Mutex，值只有1和0，初始化为1，函数wait（）和signal（）分别在值为1和0的情况下被合法调用。

![image-20220527172007989](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527172007989.png)

##### 4.3 信号量的相关问题

###### 4.3.1 死锁和饥饿

1. 死锁Deadlock既**每个**进程都持有一定的资源，又希望获得正在被其他进程占有的资源，这样每个进程都得不到完整资源。

2. 饥饿Starvation既进程始终得不到它想要获得的资源。

### 5. Classical Problems of Synchronization(同步的经典问题)



#### 5.1 有限缓冲问题(bounded-buffer problem)

存在一个公共且有限的缓冲空间，使用这些的进程被分为生产者和消费者，生产者只有在缓冲未满时生产，消费者只有在缓冲非空时消费，解决方案：

1. 信号量mutex=1 保证对缓冲池的访问是互斥的
2. empty=n 表示空闲缓冲区的信号量
3. full=0 表示已使用缓冲区的信号量

![image-20220527172642943](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527172642943.png)



#### 5.2 读者-写者问题(The readers-Writers Problem)

对于一个公共资源，使用资源的进程被分为读者和写者，分别只读，只写。

对于这些读者没有太多限制。要避免同一时间有多名写者访问和写者和读者都在访问的情况。要求：
· 一个写者在访问时，其他写者和读者要被阻塞
· 允许多个读者在同时访问，但此时写者全部阻塞
解决方案：

1. readcount=0 表示读者数量。
2. mutex=1 保证更新readcount时互斥，修改读者数量时的互斥
3. wrt=1 作为写者获得请求的信号量，读者和写者共用，确保读者和写者互斥，没有读者时=0

![image-20220527173303245](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527173303245.png)



#### 5.3 哲学家进餐问题(The Dining-Philosophers Problem)

5个人坐一圈，人与人之间放一只筷子，人要么思考要么吃饭。吃饭前需要依次拿起左手与右手的筷子，思考时放下筷子。
死锁问题：所有人都在思考，然后同一时刻吃饭，所有人拿起左手的筷子后都在请求右手的筷子，产生死锁。解决方案：

1. 最多允许四个人坐下
2. 一次只允许一个左右手都有筷子的哲学家拿起两只筷子。
3. 奇数位置的人先拿左手，再拿右手；偶数位置的人先拿右手，再拿左手。

![image-20220527182439721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527182439721.png)





## Week3 tutorial

### 1. 其他：

1. P operation also called as wait operation decrements the value of semaphore variable by 1

<font color='red'>P被称为等待操作，作用是将信号量变量值减1。</font>

2. V operation also called as signal operation increments the value of semaphore variable by 1

<font color='red'>V被称为信号操作，作用是将信号量变量值加1.</font>

![image-20220527200540843](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527200540843.png)

![image-20220527201644066](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527201644066.png)

当S0<0时，且P1, P2都已经运行完毕.此时P0将一直卡在wait部分，不会再向下运行。

答案：C。顺序P0-P1-P0-P2-P0

最小次数2 P0-P1-P2-P0

### 2. Practice Exercises

##### 2.1 Process Synchronization

1. **解释为什么Windows、Linux和Solaris实现多种锁定机制。描述它们在何种情况下使用自旋锁、互斥锁、信号量、自适应互斥锁和条件变量。在每种情况下，解释为什么需要这种机制。**

答:这些操作系统根据应用程序开发人员的需要提供不同的锁定机制。自旋锁对于多处理器系统非常有用，在这种系统中，线程可以在繁忙循环中运行(短时间内)，而不会产生放入睡眠队列的开销。互斥锁对于锁定资源很有用。Solaris 2使用自适应互斥锁，这意味着互斥锁是在多处理器机器上通过自旋锁实现的。当必须长时间持有资源时，信号量和条件变量是更合适的同步工具，因为在长时间内旋转效率低下

2. 忙碌等待是什么意思?在操作系统中还有什么其他类型的等待?能完全避免忙碌的等待吗?解释你的答案。

答:

忙碌等待意味着进程在一个紧密循环中等待一个条件被满足，而不放弃处理器。

或者，进程可以通过放弃处理器来等待，并在某个条件下阻塞，等待在未来的某个适当的时间被唤醒。可以避免繁忙等待，但会带来与使进程进入睡眠状态以及在达到适当的程序状态时必须唤醒它相关的开销。

3. 解释为什么自旋锁不适合单处理器系统，而经常用于多处理器系统?

## Week3 Lab 

### 1. While loop, Character strings

### 2. Functions, Recursions





## Week4 CPU的调度

### 1. CPU的调度的基本概念

CPU调度器是一种选择下一个必须执行的进程并将CPU分配给该进程的机制。调度器负责将进程从一种状态转移到另一种状态。

#### 1.1 CPU-I/O区间周期

程序由**CPU执行（CPU execution）和I/O等待（I/O wait）**组成。从CPU执行开始在上述运行状态间进行切换。程序据此也可被分成**CPU繁忙型**和**I/O等待型。**

![image-20220527205531935](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527205531935.png)

#### 1.2 CPU调度的种类

##### 1.2.1 Long-Term Scheduler

长期调度器也被称为**作业调度器**，负责控制多编程的程度，即处于<font color='red'>就绪状态</font>的进程总数。

#### 1.2.2 Short-Term Scheduler

Short-Term Scheduler也被称为**CPU Scheduler**，负责从就绪状态中选择一个进程，将其调度到运行状态。

**短期调度**既是从就绪的进程中选择一个，分配CPU给进程。
只有处于就绪ready状态的进程会被cpu调度。

![image-20220407095006560](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407095006560.png)

#### 1.2.3 Medium-term schedulers

中期调度器是那些调度器，它们的决定将对系统的性能产生中期影响。它负责将一个进程从主内存交换到辅助存储器，反之亦然。

### 2. 抢占式与非抢占式调度

#### 2.1 抢占式Premptive Scheduling

正在运行的进程会被打断，然后下一个高优先级的进程会进入。

#### 2.1 非抢占式Non-Preemptive Scheduling

正在运行的进程不会被打断，下个进程需要等待这个进程完成CPU周期。

![image-20220527213256470](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527213256470.png)

### 3. CPU的调度

#### 3.1 调度发生在四种情况下：

##### 3.1.1 From Running to Ready

进程从运行转为就绪（因为中断）

<font color='red'>from Running to Ready</font>

##### 3.1.2 From Running to Waiting

从运行转为等待（因为I/O请求或wait（）等待

<font color='red'>from Running to Waiting</font>

##### 3.1.3 From Waiting to Ready

从等待转为就绪（IO完成）

<font color='red'>from Waiting to Ready </font>

##### 3.1.4 Terminates

终止进程 <font color='red'>Terminates</font>
其中2和4是非抢占的，1和3是抢占的。

###  4.分派程序(Dispatcher module)

控制那些<font color='red'>短期调度</font>的进程，主要包括：
	· 切换上下文
	· 切换至用户模式
	· 跳转到合适的位置以重启程序

分派程序会产生延迟。

### 5.CPU的调度准则（评估参数）

![image-20220407095936940](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407095936940.png)

![image-20220407095959514](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407095959514.png)

期望一个合理的调度算法应该尽可能拥有：

1. 最大CPU效率 Max CPU utilization
2. 最大吞吐量 Max Throughput
3. 最小周转时间 Min Turnaround time–进程提交到进程完成的时间之和
4. 最小等待时间 Min Waiting time–在就绪队列中等待的时间，不包括运行时间
5. 最小响应时间 Min Response time–提交请求到产生第一个响应的时间
   

### 6.CPU的调度算法

共7个，可以移步这位博主的总结[操作系统常用调度算法](https://www.cnblogs.com/kxdblog/p/4798401.html)，这里大部分内容不再详述。

#### 6.1 First-Come, First-Served(FCFS) Scheduling- 先到先服务

Processes are executed on first come, first serve basis.

<font color='red'>一个非抢占类，遵循先到先执行的原则。</font>

![image-20220527214356922](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527214356922.png)

##### Drawback of FCFS

采用FCFS的平均等待时间较长。当执行一个大进程时，所有的进程都要等待大进程释放CPU，称为护航效果(convoy effect)，这样会导致CPU和设备的使用率变得很低。

#### 6.2 Shorttest Job First(SJF)最短作业优先调度

<font color='red'>SJF将每个进程与其下一个CPU区间段相关联。当CPU空闲时，他会赋给具有最短CPU区间的进程。如果两个进程具有同样长度，那么可以使用FCFS调度来处理。</font>

##### 6.2.1 SJF的特点

- SJF调度算法的平均等待时间是最小的，同时系统的吞吐量也增大了。
- 有利于短进程，不利于常进程，长进程可能导致**饥饿**(又叫做无穷阻塞，指可以运行但缺乏CPU的进程)。
- SJF真正的困难在于很难知道下一个CPU区间的长度，所以它很难实现。所以一般使用<font color='red'>SJF近似算法</font>预测下一个CPU区间的长度
- 使用近似算法实现的SJF经常用于长期调度。

###### 6.2.1.1 **SJF近似算法**

下一个区间通常可预测为以前CPU区间的测量长度的**指数平均**。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2021011323255952.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxODgyNjg2,size_16,color_FFFFFF,t_70)

##### 6.2.2 NO preemption (不可抢占类型SJF)

1.用最短的burst time来调用进程。

![image-20220407101244304](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407101244304.png)

burst time： CPU的请求时间

![image-20220407101429129](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407101429129.png)

![image-20220527215151331](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527215151331.png)

##### 6.2.3 preemption (抢占类型SJF)

![image-20220527215303053](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527215303053.png)

#### 6.3 Shortest Remaining Time First(SRTF)- 短剩余时间优先

抢占型 Preemption

第一个进程先来先服务，第二个进程之后根据最短剩余时间进入,第一个进程可能会被抢占。

![image-20220407101853532](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407101853532.png)

**<font color='red'>虽然名字不同但和SJF的抢占类型一样</font>**

#### 6.4Priority Scheduling-优先级优先调度

**优先级调度**： SJF算法可作为通用优先级调度算法的一个特例。每个进程都有一个优先级与其关联，具有最高优先级的进程会分配到CPU。具有相同优先级的进程按FCFS顺序调度。SJF算法属于简单优先级算法，其优先级为预测CPU区间的倒数。CPU区间越大，优先级越小。 (在笔者这一版课本中，小数字表示高优先级 )
![image-20220527221048831](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527221048831.png)



![image-20220407102706549](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407102706549.png)

##### 6.4.1 **优先级调度的缺点及解决方法**

**缺点**：和SJF算法一样，优先级调度也会导致饥饿问题，优先级低的进程可能永远也等不到CPU的分配。

**解决方法：** 低优先级进程无穷等待问题的解决之一是**老化**(aging)：<font color='red'>随着等待时长的增加，逐渐增加在系统中等待时间很长的进程的优先级。</font>

#### 6.5 Round Robin(RR) Scheduling - 时间片轮转

**抢占**

轮转法类似于FCFS，但是增加了抢占以切换进程。<font color='red'>抢占的机制是定义一个较小的时间单元称为时间片，当分配给一个进程的时间片结束时，切换进程。</font>如果进程在时间片内运行结束，那么多余的时间片回收，然后切换进程。



![image-20220527221501827](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527221501827.png)

##### 6.5.1 上下文切换问题

每一个进程获得一个小的CPU时间段位，一般在10-100毫秒。

After this time has elapsed, the process is preempted and added to the end of the ready queue Ready queue is treated as a circular queue

在此之后，进程被抢占就添加到就绪队列的末尾，准备队列被视为循环，

如果准备队列中有n个进程，并且时间量是q，那么每个进程将获得1/n的CPU时间，每次最多获得q个单位的时间块。没有进程等待的时间单位超过(n-1)q。

**时间片大了会FCFS，时间片小了上下文切换过于频繁。**

![image-20220527221624647](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527221624647.png)

#### 6.6 Multiple-Level Queues Scheduling-多级队列调度

层与层间平行，调度前进程被分配到固定某一层

**多级队列调度算法：** <font color='red'>将就绪队列分成多个独立队列。</font>根据进程的属性，比如**内存大小，优先级，进程类型**，一个进程被<font color='red'>永久</font>地分配到一个队列。每个队列有自己的调度算法

不同的进程类别：

![image-20220407103715714](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407103715714.png)

#### 6.7 Multilevel Feedback Queue Scheduling-多级反馈队列

与多级队列调度算法不同的时，进程在多级反馈队列中被分配到一个队列之后，还可以转移到其它队列。在队列之中转移也是一种<font color='blue'>**老化**</font>的实现方式。

![image-20220527222009721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527222009721.png)



## Week4 Tutorial

### 1. CPU scheduling Algorithms- Practice1

#### 1.1 Length of Next CPU Burst

![image-20220418190812033](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418190812033.png)

**根据不同的调度算法，同一个值会有不同的结果**

![image-20220527223541852](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223541852.png)

![image-20220527223601537](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223601537.png)

#### 1.2 Shortest-Job-First (SJF) Scheduling (Ex.1-3)

![image-20220527223642550](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223642550.png)

![image-20220527223733194](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223733194.png)

![image-20220527223746600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223746600.png)

#### 1.3 Priority Scheduling (Ex.1-2)

![image-20220527223905934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223905934.png)

![image-20220527223914250](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527223914250.png)

#### 1.4 Round Robin (RR) Scheduling (Ex.1-3)

![image-20220527224033486](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527224033486.png)

![image-20220527224054798](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527224054798.png)

![image-20220527224106081](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527224106081.png)

### 2. CPU scheduling Algorithms- Practice2

#### 2.1 FCFS-Ex.1-2

![image-20220527231615956](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527231615956.png)

![image-20220527231727283](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527231727283.png)

#### 2.2 SJF-Ex

![image-20220527232220484](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527232220484.png)

![image-20220527232242852](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527232242852.png)

#### 2.3 各种时间代表的意义

##### 2.3.1 Burst time

Burst time是进程在CPU上执行所花费的总时间。

##### 2.3.2 Arrival time

到达时间是进程进入就绪状态并准备执行的时间

##### 2.3.3 Exit time

退出时间是指进程执行完成并退出系统的时间

##### 2.3.4 Response time

响应时间是流程处于就绪状态并获取首次使用CPU。

![image-20220527232752864](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527232752864.png)

**<font color='red'>Response time = Time at which the process gets the CPU for the first time - Arrival time</font>**

##### 2.3.5 Waiting time

等待时间是进程在就绪状态下等待CPU的总时间。(进入并执行完成所用的总时间)

**<font color='red'>Waiting time = Turnaround time - Burst time</font>**

##### 2.3.6 Turnaround time（轮转时间）

周转时间是过程从第一次进入就绪状态到完成所花费的总时间。

![image-20220527233530769](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220527233530769.png)

##### 2.3.7 Throughput（吞吐量）

吞吐量是一种发现CPU效率的方法。它可以定义为CPU在给定时间内执行的进程数。

<font color='blue'>例如，假设流程P1的执行时间为3秒，P2的执行时间为5秒，P3的执行时间为10秒。因此，吞吐量，在这种情况下，吞吐量将是(3+5+10)/3 = 18/3 = 6秒。</font>

## Week4 Lab

### Memory, Address, Pointer



## Week5

### 1. CPU线程调度

#### 1.1线程调度 Thread Scheduling

##### 1.1.1进程本地调用(Process local scheduling)

##### 1.1.1.1 进程竞争**（process-contention scope, PCS）

适用于many-to-many和many-to-one。
**进程竞争竞争**（process-contention scope, PCS）：<font color='red'>指**CPU竞争发生在同一进程下的线程之间**.</font>

##### 1.1.2 系统全局调度(System global Scheduling)

##### 1.1.2.1 系统竞争（system contention scope，SCS）

适用于one-to-one，
属于系统竞争（system contention scope , SCS）：<font color='red'>**指CPU竞争发生在映射的内核线程之间。**</font>

### 2. 多处理器调度(Multiple-Processor Scheduling)

Depends on how the multiple processors are configured within the system.
调度策略的选择取决于多个处理器的配置方式

*与单处理器调度相比，多处理器的调度更为复杂，目前，与单处理器中的CPU调度算法一样，没有最好的解决方案。*

#### 2.1 非对称 Asymmetric (master/slave-AMP)

大哥带小弟，大哥处理器需要处理整个系统的调度，IO等，其他处理器只处理用户的代码.

#### 2.2 对称 Symmetric (SMP)

 每个处理器自我调度。所有进程可能处于一个共同的就绪队列中，或每个处理器有自己的私有就绪进程队列。

<font color='red'>各个CPU各司其职</font>

![image-20220528125617392](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528125617392.png)

#### 2.3 Separate Kernel Configuration(分离内核配置)

每个处理器都有自己的I/O设备和文件系统。处理器之间几乎没有相互依赖关系。在一个进程上启动的程序只在该处理器上运行到完成。

![image-20220528122333343](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528122333343.png)

##### 2.3.1 Drawback of 分离内核配置

这种组织的缺点是不可能并行执行。单个任务不能被分解成多个子任务分布在多个处理器上，从而失去了计算速度提升的优势

#### 2.4 处理器亲和力 Processor affinity

特定的进程只在一个特定的处理器上运行，减少进程在不同处理器上的跳跃，既重复利用缓冲区

###### 2.4.1 Soft affinity 

操作系统试图让一个进程运行在相同的处理器上。

###### 2.4.2 Hard affinity

允许进程指定一个它可以运行的处理器子集。

#### 2.5 负载平衡 Load Balancing

操作系统检查并验证（checks and validates）就绪队列中进程数设法让工作负载平均地分配到SMP系统中的所有处理器上。

##### 2.5.1 负载移出 Push migration

如果该处理器过载，将过载的进程push到空闲处理器分配负载

##### 2.5.2 负载移入 Pull migration

pulls a waiting task from a busy processor
处理器空闲会从别的处理器转移进来进程

#### 2.6 多核处理器问题

1. SMP：多核会复杂化调度
2. 存储停顿 memory stall：核心为了等待数据可用而停顿
3. 硬件层面解决 - 实现多线程处理器内核（**multithreaded processor cores**）： 硬件的线程被分配给每个内核，如果一个线程停顿，核心切换至另一个线程。

###### 2.6.1 粗粒度多线程 Coarse-grained multithreading

只有线程阻塞时发生线程切换

###### 2.6.2 细粒度多线程 Fine-grained multithreading

线程按照时间片轮转切换

### 3. 实时CPU调度

在实时系统中，时间起着至关重要的作用

#### 3.1 硬实时系统 Hard real-time systems：

指必须在最后期限前完成任务;否则，将对系统造成不可接受的损害或致命的错误。

#### 3.2 软实时系统 Soft real-time systems：
适当但不必要的期限;即使已经超过了截止日期，安排并完成任务仍然是有意义的。

#### 3.3 Aperiodic Tasks非周期性任务

非周期性任务(随机时间)具有<font color='red'>不规律的到达时间</font>和软期限或硬期限

#### 3.4 Periodic tasks 周期性任务

周期性任务(**重复任务**)，需求可以表述为"每周期T一次"或者"正好间隔T个单位"

#### 3.5 Issues in Real-time Scheduling

##### 3.5.1 中断延迟 interrupt latency：
····**中断响应时间，中断请求到中断服务之间的时间**

![image-20220528131024954](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528131024954.png)

##### 3.5.2 调度延迟 dispatch latency：
····**停止一个进程到开始下一个进程之间的时间**

![image-20220528131039638](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528131039638.png)

##### 3.5.3 静态调度 Static scheduling：
····**程序开始前调度并处理相关资源，周期和DDL。**  <font color='red'>准备一张确定的时间表</font>

##### 3.5.4 优先级调度 priority-based scheduling：
···· **实时分析程序，为进程分配优先级**

##### 3.5.5 动态调度 dynamic scheduling：
···· **创建进程时请求调度决策**

##### 3.5.6 优先级调度（Priority-based Scheduling）

···· 分配给任务的优先级取决于任务响应事件的速度

#### 3.6 相关时间

![image-20220528131432229](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528131432229.png)

### 4. 实时调度算法 real-time

![image-20220528133324684](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528133324684.png)

#### 4.1 单调速率优先调度RMS（Rate Monotonic Scheduling ）

<font color='red'>对于周期性进程的高静态优先级抢占，目前是最优静态调度算法</font>
**优先级：周期period越短，静态优先级越高**

该算法假定每个周期中，<font color='red'>周期性进程处理的时间相同（既第一次周期，第n个周期中进程p需要执行的时间固定不变）</font>，不会随着时间推进各个周期内出现因处理时间偏差产生的误差

1. 根据静态优先级开始依次运行。
2. 每个进程开始它的一个新的周期时抢占CPU，同一时刻多个线程开启新周期，按照优先级抢占。
3. 每个进程在它的一个周期内只会完成一次task。

**以所需处理时间t / 周期period 可表示系统利用率**，系统利用率之和小于1代表目前系统可以在大周期截止前完成全部任务，甚至还能留下空闲时间。

![image-20220407113955333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407113955333.png)

![image-20220528143013060](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528143013060.png)





#### 4.2 早截止早优先(Earliest-Deadline-First Scheduling)EDF

**抢占**，根据动态优先级抢占。
优先级：<font color='red'>**根据距离DDL时间越早截止，优先级越靠前**</font>

1. 每个线程的新的周期开始时计算优先级，高优先级的抢占低优先级的

![image-20220528142817148](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528142817148.png)

#### 4.3 比例分享调度（Proportional Share Scheduling）

CPU享有T个门票，把门票下发给程序，程序持有多少比例的门票就占CPU多久比例

### 5. 算法评估

#### 5.1 Deterministic evaluation

算平均等待时间

#### 5.2 Queueing Models

算cpu利用率，平均队列长度，平均等待时间

进程离开队列和进入队列相抵

![image-20220407114448329](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220407114448329.png)

**平均队列长度 = 到达速率 * 单个进程在队列内的平均等待时间 = 出去速率 * 单个进程在队列内的平均等待时间**

#### 5.3 Simulations

![image-20220528135004768](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528135004768.png)



## Week5 -Tutorial

### 1. Practice- Ex

1. cpu调度算法决定其调度进程的执行顺序。给定一个处理器上要调度n个进程，可能有多少种调度?给出一个关于n的公式。

![image-20220528135147418](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528135147418.png)

2. 解释抢占式和非抢占式调度的区别

答:

抢占式调度允许进程在执行过程中被中断，占用CPU并分配给另一个进程。

非抢占式调度确保进程只有在当前CPU爆发结束时才放弃对CPU的控制。

3. 假设以下进程在指定的时间到达并执行。每个进程将按照列出的时间运行。在回答问题时，使用非抢占式的安排，并基于你在必须做出决定时所拥有的所有信息做出所有决定。

![image-20220528135411411](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528135411411.png)



4. 在多级排队系统的不同级别上拥有不同的时间量子大小有什么好处?

需要更频繁服务的进程(例如，编辑器等交互式进程)可以在一个时间量很小的队列中。

不需要频繁服务的进程可以在一个具有更大数量的队列中，需要更少的上下文切换来完成处理，从而更有效地利用计算机。

5. ![image-20220528140805561](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528140805561.png)

6. 假设一个调度算法(在短期CPU调度级别上)倾向于最近使用最少处理器时间的进程。为什么这个算法会倾向于I/ o限制的程序，而不会永远饿死cpu限制的程序?

这将有利于I/ o限制的程序，因为它们的CPU突发请求相对较短;但是，CPU绑定的程序不会饿死，因为I/O绑定的程序会相对频繁地放弃CPU来做I/O。

7. Distinguish between PCS and SCS scheduling.

PCS调度是在过程中本地完成的。它是线程库将线程调度到可用lwp上的方式。SCS调度是操作系统调度内核线程的情况。在使用多对一或多对多的系统上，这两种调度模型是完全不同的。对于一对一的系统，PCS和SCS是相同的。

8. 假设操作系统使用多对多模型将用户级线程映射到内核，并且通过使用lwp完成映射。此外，该系统允许程序开发人员创建实时线程。是否有必要将实时线程绑定到LWP吗?

是的，否则用户线程可能必须在实际调度之前竞争一个可用的LWP。通过将用户线程绑定到LWP，在等待可用LWP时没有延迟;实时用户线程可以立即调度。

![image-20220528141200674](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528141200674.png)

![image-20220528141503944](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528141503944.png)



## Week6

### 1. 死锁问题

什么是死锁：

Deadlock can be defined as the **permanent blocking** of a set of processes that compete for system resources

<font color='red'>由于争抢资源导致永久性的堵塞，一些列进程持有资源并且想要别的进程持有的资源。</font>

#### 1.1 死锁的四大特征

同时保持这四种特征就会形成死锁。

##### 1.1.1 互斥Mutual Exclusion

资源同一时刻只能被一个进程访问。

##### 1.1.2 占有并等待 Hold And Wait

进程持有一些资源，又等待获取一些资源。

##### 1.1.3 非抢占 No Preemption

进程不能抢占那些持有部分资源的进程

##### 1.1.4 循环等待 Circular Wait

a等b，b等c，c等a

#### 1.2 资源分配图（resource allocation grath）

圆P代表进程
块R代表资源，里面的点代表资源实例
P->R箭头（request edge）：P申请R的实例instance，request
Ri->P箭头（assignment edge）：R的实例 i 被分配给P，granted或者allocated

![image-20220528152156471](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528152156471.png)

1. 当图中没有环代表不存在死锁。

如果存在环：

1. 一**个资源只有1个实例，形成死锁**
2. **一个资源有多个实例，可能死锁**

![image-20220418143651137](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418143651137.png)



### 2. 处理死锁(Handing DeadLocks)

处理死锁问题的三个方法：

1. DeadLock prevention
2. DeadLock avoidance
3. DeadLock detection and recovery

<font color='red'>死锁预防</font>： 因为产生死锁需要四个必要条件，只要使任一条件不成立，死锁就不会发生，称为死锁预防。

<font color='red'>死锁避免</font>： 要求操作系统事先得到有关进程申请资源和使用资源的额外信息。有了这些信息，系统可以确定，对于一个进程的资源申请，进程是否应该等待。所以，系统必须考虑现有可用资源、已分配给每个进程的资源、每个进程将来申请和释放的资源。

<font color='red'>死锁检测</font> 提供一个算法来检查系统状态以确定死锁是否发生。

<font color='red'>死锁恢复</font>： 提供一个算法使操作系统从死锁中恢复。

<font color='red'>死锁忽略</font>： 未检查死锁会导致系统性能下降，因为资源被不能运行的进程所占有，越来越多的进程会因为申请资源进入思索。最后，整个系统会停止工作，并且需要进行人工启动（如果死锁很少发生，比如一年一次，那么死锁忽略就是可行的，因为这种方法更为经济）。

#### 2.1 DeadLock Prevention（死锁预防）

*死锁预防便是打破形成死锁的四个必要条件之一，有四种策略：*

##### 2.1.1 死锁预防的四种策略

###### 2.1.1.1 互斥

非共享资源必须互斥，共享资源不要求互斥所以不会死锁。无法从互斥条件下手避免死锁

###### 2.1.1.2 占有并等待

1. 可以是进程循序**拥有不等待**，即要求一个进程在执行前获得所有资源。
2. **等待不拥有**，进程在申请其他资源的时候必须释放已分配的资源。

**缺点：**

1. 资源利用率低。比如一个进程需要三个资源，它必须一开始就申请。如果需要100个时间单元，但其中一个资源可能只需要被占有10个时间单元，那么剩余的90个时间单元就被浪费了。
2. 可能会产生饥饿。如果一个进程需要多个资源，可能会永久等待

###### 2.1.1.3 非抢占

解决方法（抢占）：如果一个进程占有一些资源并在申请一些无法立刻分配到的资源，那么它占有的资源就可以被抢占。

###### 2.1.1.4 循环等待

确保此条件不成立的条件是对所有资源类型进行<font color='red'>完全排序</font>，且要求每个进程按递增顺序来申请资源。举个例子，比如有1,2,3,4四种类型的资源。不管进程使用资源的顺序如何，都必须按编号从小到大申请。



#### 2.2 DeadLock Avoidance(死锁避免)

**死锁避免原理：** 死锁避免算法动态地检测<font color='red'>资源分配状态</font>以确保循环等待条件不可能成立。资源分配状态是由可用资源和已分配资源，以及最大需求决定的。

达成Deadlock Avoidance的两种方法：

1. 如果一个进程的要求可能导致死锁，那么就不启动它。
2. 如果进程新的资源请求可能导致死锁，那么就拒绝该请求。

##### **2.1.2 Safe State（安全状态）**

安全状态指的是至少有一个给进程分配资源的分配器不会导致死锁。

所谓安全状态，是指<font color='red'>系统能按某种进程推进顺序( P1, P2, …, Pn)，为每个进程Pi分配其所需资源，直至满足每个进程对资源的最大需求，使每个进程都可顺序地完成。此时称 P1, P2, …, Pn 为安全序列。</font>如果系统无法找到一个安全序列，则称系统处于不安全状态。

![image-20220418151249997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418151249997.png)。

**相关定义**

1. **Max needs** = total amount of each resource in the system系统需要的总资源量。
2. **Available resources** = total amount of each resource not allocated to any process. 当不分配给进程时，总资源量。
3. **Need / Resources needed** = future requests of the process i for resource j进程i今后对资源j的要求。
4. **Allocation / Current allocated resources** = the resources allocated presently to process i. 当前分配给进程i的资源。

![image-20220418155948398](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418155948398.png)

##### 2.2.2 银行家算法（Banker’s algorithm）

![image-20220418161254269](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418161254269.png)

![image-20220418161905676](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418161905676.png)

![image-20220418162209104](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418162209104.png)

https://blog.csdn.net/qq_33414271/article/details/80245715?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165026942716780274175778%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165026942716780274175778&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-2-80245715.142

详细信息如上

注意：在进行安全性算法时，每执行完一个进程需要释放它的资源使得闲置空间增加。

#### 2.3 DeadLock Detection(死锁检测)

很像银行家算法中的安全性算法，简直一样。

Two parts：

1. Detection of single instance of resource.检查单个资源的单个实例。
2. Detection for multiple instances of resources. 检查多个资源的复数实例。

![image-20220418164624160](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418164624160.png)

![image-20220418164704365](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220418164704365.png)

**算法：** 与资源分配图算法一样，当且仅当等待图中存在一个环，系统中存在死锁。为了检测死锁，系统需要维护等待图，并周期性地调用在图中进行搜索的算法。

**死锁检测的时机：**

1. 关乎死锁可能发生的频率
2. 关乎死锁发生时会影响到的进程数量

#### 2.4 Recovery from DeadLock（死锁恢复）

修复死锁问题的具体措施

##### 2.4.1 进程终止

1. 终止（abort）一个或多个发生死锁的进程以终止循环等待
2. ·一次全部终止（环上的进程全部终止），或挨个终止直到循环等待(资源分配图里的环）消失。
   从一个或多个死锁进程抢占（preempt）资源
   1. ·选择受害者victim–根据拥有资源数量和运行时间
   2. ·回滚Rollback–返回安全状态，重启进程
   3. ·饥饿starvation–需要避免同个进程一直被选为受害者

##### 2.4.2 资源抢占

通过抢占资源以取消死锁，逐步从进程中抢占资源给其他进程使用，直到死循环被打破。

###### 2.4.2.1  **资源抢占要处理的问题**

- 选择一个牺牲品，使代价最小化。
- 回滚：被抢占的进程需要回滚到安全状态。
- 饥饿：必须保证不会发生饥饿，因为有可能被抢占的总是同一个进程。



### week6错题

![image-20220419174101644](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174101644.png)

![image-20220419174149666](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174149666.png)

![image-20220419174305479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174305479.png)

![image-20220419174433179](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174433179.png)

![image-20220419174538402](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174538402.png)

![image-20220419174624597](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419174624597.png)

![image-20220419175412049](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419175412049.png)

* 为了保证在应用程序、数据库或系统出现错误后，数据库能够被还原，以保证数据库的完整性，所以需要进行回滚。

  回滚([rollback](https://so.csdn.net/so/search?q=rollback&spm=1001.2101.3001.7020))就是在事务提交之前将数据库数据恢复到事务修改之前数据库数据状态。

## Week6 Tutorial

### 1. Pratice Ex

1. List three examples of deadlocks that are not related to a computersystem environment.

答:

•两辆汽车从相反的方向穿过单车道桥。

•一个人从梯子上下来，而另一个人在梯子上爬。

•两列火车在同一轨道上相向而行

2. 假设系统处于不安全状态。说明进程可以在不进入死锁状态的情况下完成它们的执行。

答:

不安全的状态不一定会导致死锁，它只是意味着我们不能保证死锁不会发生。因此，处于不安全状态的系统可能仍然允许所有进程完成而不发生死锁。

3. 考虑一个系统![image-20220528175044099](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528175044099.png)

*用银行家的算法回答以下问题:*

​	*a.矩阵Need的内容是什么?*

​	*b.系统是否处于安全状态?*

​	*c.如果来自进程P1的请求到达(0,4,2,0)，这个请求可以立即被批准吗?*

a.进程P0到P4的Need值分别为(0, 0, 0, 0)、(0、7、5,0)、(1 0 0 2),(0 0 2,0)和(0、6 4 2)。

b.是的。可用等于(1,5,2,0)，进程P0或P3都可以运行。一旦P3进程运行，它将释放其资源，从而允许所有其他现有进程运行。

c. 不行。这个请求能立即得到批准吗?这样，Available的值为(1,1,0,0)，可以完成的进程顺序为P0, P2, P3, P1, P4。

4. 防止死锁的一种可能的方法是，必须在任何其他资源之前请求单个更高阶的资源。例如，如果多个线程试图访问同步对象A···E，则可能出现死锁。(这种同步对象可能包括互斥量、信号量、条件变量等。)我们可以通过添加第六个对象f来防止死锁。每当一个线程想要获取任何对象a···E的同步锁时，它必须首先获取对象f的锁。这个解决方案被称为包容:对象A···E的锁包含在对象f的锁中。将该方案与7.4.4节中的循环等待方案进行比较。

答:

这可能不是一个好的解决方案，因为它产生了太大的范围。

最好定义一个范围尽可能窄的锁定策略。

5. a.安装死锁避免算法的理由是什么?

   b.反对安装死锁避免算法的理由是什么?

答:

在系统中安装死锁避免的一个论点是，我们可以确保死锁永远不会发生。此外，尽管周转时间增加了，所有5000个工作仍可运行。

反对安装死锁避免软件的一个理由是，死锁发生的频率很低，即使发生，成本也很低。

6. 系统能否检测到它的一些进程饿了?如果你的回答

   “是的，”解释它怎么能。如果你的回答是“不”，请解释系统如何处理饥饿问题。

答:

饥饿是一个很难定义的主题，因为它对不同的系统可能意味着不同的东西。出于这个问题的目的，我们将饥饿定义为这样一种情况:在接收到请求的资源之前，进程必须等待超过一段合理的时间(可能是无限的)。检测饥饿的一种方法是首先确定一个时间T，这个时间T被认为是不合理的。当进程请求资源时，计时器启动。如果运行时间超过T，则认为进程处于饥饿状态。处理饥饿的一种策略是采用一种策略，将资源只分配给等待时间最长的进程。例如，如果进程Pa等待资源X的时间比进程Pb更长，那么来自进程Pb的请求将被延迟，直到进程Pa的请求得到满足。另一种策略可能没有刚才提到的那么严格。在这种情况下，可以将资源授予等待时间少于另一个进程的进程，前提是另一个进程没有饥饿。但是，如果另一个进程被认为处于饥饿状态，那么它的请求将首先得到满足。

7. a.会发生死锁吗?如果你回答“是”，举个例子。如果您回答“否”，请指定哪些必要条件不能发生。

   b.会发生无限期阻塞吗?解释你的答案

答：

a.由于存在抢占，所以不会发生死锁。

b。是的。一个进程可能永远不会获得它需要的所有资源，如果它们被一系列请求(比如进程C的请求)持续抢占。

8. 假设您已经编写了避免死锁安全算法，现在要求实现死锁检测算法。你可以通过简单地使用安全算法代码并重新定义Max[i] = Waiting[i] + Allocation[i]，其中Waiting[i]是一个向量，指定进程i正在等待的资源，而Allocation[i]的定义在7.5节中。解释你的答案。

答:

是的。Max向量表示进程可能发出的最大请求。在计算安全算法时，我们使用Need矩阵，它表示最大分配。另一种理解方法是Max = Need + Allocation。根据问题，等待矩阵的作用类似于需要矩阵，因此Max =等待+分配

9. 是否可能有一个死锁只涉及一个单线程进程?解释你的答案。

No. This follows directly from the hold-and-wait condition.



## Week8

### 1.Memory Management(内存管理)

<font color='red'>*内存是现代计算机运行的中心。*</font>

**Memory**：The memory is where the programs are kept when they are running; it also contains the data needed by the running programs. 内存是程序用来保存和运行的地方，它同时储存着运行程序需要的数据。

#### 1.1 内存管理的需求(Memory Management Requirements)

##### 1.1.1 Protection

##### -从用户进程中保护OS；用户进程之间的保护，通常是由硬件支持的

##### 1.1.2Relocation

**-在内存中移动而不影响其运行**

##### 1.1.3 Sharing

**-既要保护，又要分享**

##### 1.1.4 Logical Organization of memory

**-逻辑上地址被认为是一个一维的线性的由比特组成的序列**

##### 1.1.5 Physical Organization of memory

**-物理上地址有：主存访问速度快但是贵；二级存储慢但是便宜；大容量存储放的东西多，时间长。**

#### 1.2 内存管理的基本硬件

**背景：** CPU所能直接访问的存储器只有内存和处理器内的寄存器。**机器指令可以用内存地址作为参数，而不能使用磁盘地址作为参数。** 因此，执行指令以及指令使用的数据必须在这些直接可访问的存储设备上。如果数据不存在内存中，那么在CPU使用前先把数据移动到内存中。

**中心问题：** 如何确保CPU可以正确、高效地从内存中提取指令.

**确保每个进程有独立的内存空间**：

我们需要确定进程可访问的合法地址的范围，并确保进程只访问其合法地址。
我们可以通过基地址寄存器(base register) 和 界限地址寄存器(limit register) 实现。
基地址寄存器含有最小的合法物理内存地址，界限地址寄存器决定了范围的大小。

![image-20220528212513828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528212513828.png)



#### 1.3 地址绑定

**背景：** 通常，程序以二进制可执行文件的形式存储在磁盘上。为了执行，程序被调入内存并放在进程空间内。根据所使用的内存管理方案，进程在执行时可以在磁盘和内存之间移动。在磁盘上等待调入内存以便执行的进程形成输入队列。

![image-20220528202009528](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528202009528.png)







**Random Access Memory(随机存储器) RAM** : RAM consists of a number of integrated circuits mounted on one or more circuit boards (memory modules) that plug into specialised slots on the mainboard.

#### 相关概念：
·**逻辑地址Logical address**：又叫虚拟地址virtual address，是CPU执行时处理的地址。逻辑地址空间由基地址寄存器（base registers）和限制寄存器（limit registers）组成。逻辑地址由CPU生成, 通过**内存管理单元**（MMU, memory management unit）转换成物理地址
![image-20220419191230003](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419191230003.png)

·**物理地址Physical address**：由物理内存条介质认为的地址，可以定位到物理内存中的地址。

一个程序内的逻辑地址可以在三个阶段与物理地址绑定：

1. 编译（compile time）时期：将绝对地址编译进程序，但首地址改变时就会出错
2. 加载（load time）时期：加载程序时将逻辑地址与物理地址绑定，但不支持虚拟内存
3. 运行时期（execution time）时期：执行时映射逻辑地址到物理地址，这种绑定方式需要硬件支持，支持虚拟内存。
   

#### 1.4 Memory Management Unit(MMU)

1. Each memory reference is passed through the MMU
2. The OS (hardware MMU) translates the virtual address into the physical RAM address. （操作系统将虚拟内存转换为物理内存）

![image-20220419191928732](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419191928732.png)

![image-20220419192554223](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419192554223.png)

* Memory Protection（to prevent memory overlaps）**is usually supported by the hardware (limit registers)**, because most languages allow memory addresses to be computed at run-time.

* CPU registers = high speed memory area inside the processor and used during the program execution.（进程中的告诉存储空间并且在程序执行中使用。）
* ![image-20220419193301831](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419193301831.png)

----

### 2. 交换Swapping

**交换：** 进程需要在内存中以便执行。不过，进程可以暂时从内存中交换到备份存储中上，当需要再次执行时再调回到内存中，称为**交换**

![image-20220419194924694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220419194924694.png)

### 3. Dynamic relocation using a relocation register（动态定位）



**重定位relocation既是把一个逻辑地址映射成物理存储地址。**

用户程序看到的地址都是逻辑地址（0 ~ M），当这些地址被使用时经过重定位即可映射到物理地址（R ~ R+M)。

内存管理单元(memory-management unit , MMU)方案中，映射时所用的**重定位寄存器（relocation register）就是基地址寄存器（base register）**，将CPU逻辑地址加上重定位寄存器内地址完成对数据的重定位
![image-20220421092709229](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421092709229.png)

### 4. Logical Organization of Memory - Allocation(逻辑内存分配)

#### 4.1 Contiguous memory allocation(连续内存分配)

assigns consecutive memory blocks to a process.（进程获得的内存块是连续的）

![image-20220528213521822](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528213521822.png)

##### 4.1.1内存分配

###### 4.1.1.1固态/静态 分区(Fixed/Static Partitioning)

**固态分区**：是最简单的内存分配方法，将内存分为多个大小固定的分区。并且每个分区只能容纳一个进程。

**可变分区：** 在可变分区方案里，操作系统有一个表，用于记录哪些内存可用和哪些内存已经被占用。一开始，所用内存都可用于进程，因此可以作为一大块可用内存，称为**孔(hole)**。

**分配过程：** 当有新进程需要内存时，为该进程查找足够大的孔并分配。剩余为分配的内存空间会形成新的孔或者外部碎片。

###### 4.1.1.2 常用的分配算法

- **首次适应first-fit：** 分配一个足够大的孔。需要遍历整个列表，找到第一个足够大的孔。
- **最佳适应best-fit：** 分配最小的足够大的孔。也需要遍历整个列表。
- **最差适应worst-fit：** 分配最大的孔。也需要遍历整个列表

##### 变量/动态 分区(VAriable/Dynamic Partitioning)

##### 4.1.2 碎片fragmentation

首次适应方法和最佳适应方法都有外部碎片问题(external fragmentation)。

**外部碎片：** 随着进程装入和移出内存，空闲内存空间被分为小片段。当所有总的可用内存之和可以满足请求，但并不连续时，这就出现了外部碎片问题。

**50%规则：** 假定有N个可分配块，那么可能有0.5N个块为外部碎片。即1/3的内存可能不能使用。

###### 4.1.2.1 **解决外部碎片的方法：**

- **紧缩(compaction)**: 解决外部碎片的方法之一，移动内存内容，以便所有空闲空间合并成一整块。紧缩仅在重定位是动态并且运行时才可以采用。
- 允许物理地址空间非连续。下面的分页和分段技术，就是讲的这个。

#### 4.2 Non- Contiguous memory allocation(非连续内存分配)

**以非连续方式为进程分配内存块**
逻辑地址空间可以看成书店，资源可以看成书。
**分段**可以看成把相同类型的书的分到一个集合，段表既是记录了这些集合在店里哪个地方的清单。
**分页**可以看成把店里划分为许多等大的区域，书的清单上也被划分了同样大小的等大表格，每个表格记录一个区域的位置，通过查找清单可以查找到相应的区域，再通过偏移地址可以知道在该区域内具体什么位置。

##### 4.2.1 Segmentation(分段)

按照程序的逻辑给程序分段，每段由**段名**与**段长**构成。

![image-20220421094436887](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421094436887.png)

逻辑地址由段地址segment和偏移地址offset组成。
逻辑地址空间看成是由段组成的集合。

###### 4.2.2 段表 Segment table

将两个维度的逻辑地址组合成一维的物理地址。
每个**段表元素**包含**基地址base和段长度limit**
下面的段表两行，查找的是第二行：

![image-20220421095328028](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421095328028.png)



##### 4.2.3 Paging分页

首先明确三个<font color='red'>大小相等</font>的概念，**帧(frame)**、**页(page)**、**备份存储中的块**

**帧frames**：<font color='red'>将物理内存</font>分为固定大小的块。当进程运行时，将其调入可用的帧中。

**页page**：<font color='red'>逻辑内存</font>也分为同样大小的块。包含页号和页偏移。

**备份存储中的块：** <font color='red'>备份存储</font>中你的固定大小的块

![image-20220528215035251](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528215035251.png)

上图为**逻辑地址**的组成，其中包括页号和页偏移。

**页号page number**：页在页表里的下标。

**页大小page size**：一页的大小为2的次方，between 512 bytes and 1GB per page.

**分页**可以映射连续虚拟页到不连续物理帧，通过分页可以减少内存的外部碎片external fragmentation（对于一个页而言），但是其页内部internal会产生碎片，因为页是分配的最小单位，最后一页的页内会有剩余部分。
![image-20220421101017130](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421101017130.png)



###### 4.2.3.1 分页的基本方法

Page Table 页表

<font color='red'>**页表**记录了物理地址的起始地址（基地址）。</font>

**页号page number**：页表的号码(索引)，通过页号在页表里找到物理地址的基地址。
**页偏移page offset**：页偏移加上上述基地址构成精确的物理地址。
<font color='red'>**页表长度=页的总数=逻辑地址空间大小除以页大小。**</font>
**帧的总数**：物理地址空间大小除以帧大小。

![image-20220528215211758](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528215211758.png)

![image-20220528215457753](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528215457753.png)

**具体例子**

![image-20220421101616164](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421101616164.png)

**<font size=5 color='red'>m是逻辑地址空间，进程容量，n是page的容量</font>**

![image-20220421103452452](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421103452452.png)

![image-20220421104006044](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421104006044.png)

* page size = page offet的位数

<font size = 3 color = "red">非常重要！！！！！</font>

![image-20220421175936551](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421175936551.png)

![image-20220421110645932](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421110645932.png)



###### 4.2.3.2 相关例题提醒：

![image-20220421181949798](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421181949798.png)

![image-20220421182222741](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421182222741.png)

![image-20220421182235207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421182235207.png)

###### 4.2.3.3 硬件支持

*不同的操作系统有自己的方式来保存页表。页表的指针与其他寄存器的值一起存入进程控制块中。*

**页表的硬件实现有多种方法：**

* 用<font color='red'>**一组专用寄存器**</font>来实现：寄存器的访问速度快，所以地址变换的过程也快。但是只适用于页表比较小的时候。如果页表较大，则开销太大。
* **将页表放入内存，使用页表基寄存器**(page-table base register <font  color='red'>PTBR</font>)指向页表，页表基寄存器长度记录页表长度。采用这种方法的问题是访问用户内存为止需要额外时间。访问一个字节需要两次内存访问(一次用于页表条目，一次用于字节)。这样，内存访问速度就减半。在大多数情况下，这种延迟还不如采用交换机制。
* 使用<font color='red'>转换表缓冲区</font>(translation look-aside buffers,<font color='red'>TLB</font>)： 类似于高速缓存，是一种快速内存。可以理解为寻找地址时的cache。
  ![image-20220528220646067](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528220646067.png)





###### 4.2.3.4 TLB 和有效访问时间

**双内存访问问题可以通过使用一种称为Translation Look-aside Buffers (TLB)**的特殊快速查找硬件缓存来解决，专门存放页表。

使用高速缓存尝试映射物理地址时，首先

1. E: 访问高速缓冲TLB里查找页号，找到页号得到基地址后就转到第3步
2. 如果没有，M: 就访问内存用页表基寄存器寻找页表。
3. 找到页号对应的物理基地址后，M：访问内存的物理地址。
   ![image-20220421111828445](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421111828445.png)

![image-20220528220700927](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528220700927.png)

![image-20220528221615428](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528221615428.png)

![image-20220531202958593](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531202958593.png)

###### 4.2.3.4 共享页

*以分时环境为例，如果5个用户都打开了浏览器，那么不一定需要在内存中执行五个完整的浏览器进程代码，因为代码会有一大部分是相同的。这5个用户可以共享那些相同的代码，前提是代码是可重入代码。*

**可重入代码：** 多次运行，内容不变。

![image-20220528220825744](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528220825744.png)

不仅要保护，还要共享一些资源以节约运算。
· Efficient communication：进程通过写入共享页达到交流
·Memory efficiency：在进程间共享一份只读数据
以下进程的页表间看出共享了3，4，6帧
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210522152648733.png)

###### 4.2.3.5 Protection

每个进程间都有独立的内存空间和内存空间保护。
在页表上对每个帧设置有效或无效
有效位代表相关页在进程的逻辑空间内
无效位代表相关页不在进程逻辑空间内



##### 4.2.4 页表结构

*我们刚才提到有各种各样的页表结构，这里我们了解三种。*

###### 4.2.4.1  层次页表（Hierarchical Paging ）

<font color='red'>页表再分页。</font>

**简单的说，设计一个页表来作为目录存储其他链表的信息。**



不妨先按照单级页表做计算
假如：
一页的页面大小为4kB（2^12B）
页表项(entry size,也就是页表一行的大小)大小为4B(2^2B)。
操作系统32位（2的32方B），也就是虚拟地址空间为2的32方B，
则可有以下计算结果：

1. **单个页能装下2^12B/2^2B=210个页表项**
2. **一个进程有 2^32B/2^12B = 220页，意味着页表共有2^20行，也就是2^20个页表项**
3. **页表需要占2^20/2^10=2^10页去存放**
4. **这存放页表的2^10页占了2^10 * 4kB=2^12kB=4MB空间**

我们需要2^10个页去存放页表，这意味着页表被分散开来了，**所以需要一个类似于一张记录书目清单的纸一样的一个页表，记录这些存放了页表的页，**这个书目页大小也是4kB（2^12B）正好可以放下2^12B/2^2B=2^10个记录了页表的页。

![image-20220421143553468](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421143553468.png)

![image-20220528222211283](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528222211283.png)



![image-20220421144104637](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421144104637.png)



###### 4.2.4.2 哈希页表（Hashed Page Tables）

*哈希页表的原理哈希，是数据结构中的部分。处理超过32位地址空间的常用方法是使用哈希页表(hashed page table)，并以**虚拟页码**作为哈希值。*

![image-20220528222712918](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220528222712918.png)

<font color='red'>感觉上和二级页表一模一样。</font>

###### 4.2.4.3 反转页表（Inverted Page Table）

以上的讨论，都是基于每一个进程拥有一个页表。该进程所使用的每一个页，在页表中都有一项。而反向页表则不同，反向页表需要我们反向的视角来理解。

反向页表： ** 反向页表对于每个真正的内存页或帧才有一个条目。每个条目包含保存在真正内存位置的页的虚拟地址以及拥有该页的进程信息**。整个系统只有一个页表
![image-20220421144236763](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220421144236763.png)

### Week8 tutorial

看课件，全是例题

#### 1. 计算碎片

![image-20220531200246209](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531200246209.png)

![image-20220531202900211](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531202900211.png)

#### 2. 计算logical 和 physical 地址

![image-20220531200306971](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531200306971.png)

#### 3.计算EAT

![image-20220531200809475](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531200809475.png)

#### 4.计算page的各个关系

![image-20220531201637626](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531201637626.png)





#### 5.用逻辑地址求解偏移地址

![image-20220531202434703](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531202434703.png)

![image-20220531202456123](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531202456123.png)

#### 6.计算逻辑地址的位数

![image-20220531202808917](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531202808917.png)

#### 7. TLB

![image-20220531203105254](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531203105254.png)

![image-20220531203226983](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531203226983.png)

#### 8.利用页表计算内存

![image-20220531203741906](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531203741906.png)

![image-20220531203756958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531203756958.png)

![image-20220531203906160](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531203906160.png)

##### 8.1 计算page table size的大小

![image-20220531204328024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531204328024.png)

#### 9.段表

![image-20220531205958279](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531205958279.png)

![image-20220531210643686](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531210643686.png)

![image-20220531210713503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531210713503.png)

![image-20220531211909119](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531211909119.png)

![image-20220531211934536](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531211934536.png)

#### 10. 多级链表

https://www.learningmall.cn/pluginfile.php/321588/mod_resource/content/2/Multilevel%20Paging.pdf



#### 11. Main Memory Practice

1. 指定逻辑地址和物理地址的两个差异。

答:逻辑地址不指向实际存在的地址;相反，它指的是抽象地址空间中的抽象地址。与此相反，物理地址引用内存中的实际物理地址。逻辑地址由CPU生成，并由内存管理单元(MMU)转换为物理地址。因此，物理地址由MMU产生

2. 考虑一个系统，其中一个程序可以被分为两部分:代码和数据。CPU知道它是需要一条指令(取指令)还是需要数据(取数据或存储数据)。因此，提供了两个基限制寄存器对:一个用于指令，一个用于数据。指令基限制寄存器对是自动只读的，因此程序可以在不同的用户之间共享。讨论该方案的优缺点。

答:

该方案的主要优点是它是一种有效的代码和数据共享机制。例如，一个编辑器或编译器只需要在内存中保存一个副本，并且这个代码可以被所有需要访问编辑器或编译器代码的进程共享。另一个优点是保护代码不被错误修改。唯一的缺点是代码和数据必须分离，这在编译器生成的代码中通常是这样做的。

3. 为什么页面大小总是2的幂?

答:

还记得分页是通过将地址分解为页和偏移量来实现的吗?最有效的方法是将地址分成X页位和Y偏移位，而不是在地址上执行算术运算来计算页码和偏移量。因为每个位的位置表示2的幂次，所以在位之间分割地址将导致页面大小为2的幂次。





### Week8 Lab- Inter Process Communication

Linux提供了一组丰富的进程间通信(IPC)机制，包括以下内容：

1. signals 表示一个事情已经发生
2. pipes 用于两个进程间传递数据
3. sockets, 可用于在同一主机或通过网络连接的不同主机上从一个进程到另一个进程传输数据。
4. file locking , 允许某个进程锁死某个文件以防止其他进程读取或更新文件内容。
5. message queues, 用于进程之间交换信息
6. semaphores, 用于同步进程间的操作
7. shared memory, 允许进程间分享信息

管道是一种进程间通信的机制;一个进程写入管道的数据可以被另一个进程读取。数据按照先进先出(FIFO)的顺序处理

![image-20220505115000379](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505115000379.png)

![image-20220505115354055](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505115354055.png)



![image-20220505120309540](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505120309540.png)

![image-20220505115506545](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505115506545.png)

![image-20220505120354370](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505120354370.png)

![image-20220505115737496](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505115737496.png)

* 解释一下pid!=0的问题， 因为fork创建的pid会返回两个值，一个是父进程的一段数字，代表子进程的ID地址，一个是0，代表子进程创建成功。

## Week9 Virtual Memory

### 1.Defination of VM

Virtual Memory(VM): 虚拟内存是一种管理大于内存可用空间的较大进程的大小的方法。

Virtual memory： 用户逻辑内存与物理内存的分离。

* 只有部分程序需要在内存中执行
* 出现在内存中的进程组件称为进程的常驻集（<font color='blue'>resident set of the progress</font>）
* 需要允许页面/段进行交换。

Condition of the VM: 1. hardware: 支持CPU的硬件管理单元。 2. Software: VM handler.

#### 1.1Swap space/ Swap partition

为了让虚拟内存管理一个或多个大于物理进程，<font color = 'blue'>交换空间（Swap Space）</font>被保留在了磁盘内。

### 2.Demand Paging

Demand Paging: <font color = 'red'>只在内存中加载进程需要的的部分程序（页）</font>。对于按需掉页的虚拟内存，只有在程序执行时才需要载入页（这被称为<font color = 'blue'>懒惰交换（Lazy Swapper）</font>）

#### 2.1 Issues related to the implementation of Demand Paging

##### 2.1.1 How to recognize whether a page is present in the memory?

* " valid "→关联的页面既合法又在内存中。
*  “invalid” → 页面要么无效(不在进程的逻辑地址空间中)，要么有效但当前在磁盘上。

##### 2.1.2 What happens if the process tries to access a page that is not in the memory?

* 当所引用的页不在内存中→**页错误**。
* 当通过页表转换地址时，注意页表项有一个无效的位。它**会向操作系统发出一个陷阱**(页错误陷阱)，以便能够注意到页面错误。

##### 2.1.3 What happens if there is no free frame?

* the existing page in the memory needs to be <font color = 'red'>**paged-out**</font>.
* which page will be replaced? → <font color = 'red'>**page-replacement algorithms.**</font>

##### 2.1.4 Steps in Handling a Page Fault(处理页错误的流程)

![image-20220525151450835](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525151450835.png)

![image-20220525151510126](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525151510126.png)

#### 2.2 The Effective Access Time(EAT)

在没有页错误的情况下：

 the effective access time = the memory access time

![image-20220525151904713](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525151904713.png)

![image-20220525151913755](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525151913755.png)



### 3.Copy-on-Write in Operating System(COW)

Defination : 那些从未写过的页面不需要复制。只有写好的页面需要复制

![image-20220525152647626](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525152647626.png)

如果任何父进程或子进程修改了共享页，则只复制该页。

![image-20220525152739403](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525152739403.png)



### 4. Page Replacement

Defination: 当在进程执行期间发生页面错误时，需要将页面从磁盘分页到内存中。

#### 4.1 Basic Page Replacement

1. 找到所需页面在磁盘上的位置

2. 找一个自由的框架:

   -如果有一个自由帧→使用它

   - 如果没有自由帧→使用<font color = 'blue'>页面替换算法(page replcaement algorithm)</font>选择一个受害帧。

   

3. 将想要的页面放入(新的)自由框架;更新页面和框架表。
4. 重新启动导致该告警的指令，继续该进程

![image-20220525154351168](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525154351168.png)

![image-20220525154304327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525154304327.png)

#### 4.2 Page-Replcaement Algorithms

![image-20220525154505632](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525154505632.png)

![image-20220525155223650](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525155223650.png)



##### 4.2.1 First-In First-Out Algorithm(FIFO)先进先出

当必须替换某个页时，将选择最旧的页。

![image-20220525155115182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525155115182.png)

Solution:

![image-20220525155158801](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525155158801.png)

##### 4.2.2 Optimal Alogrithm

又称理想淘汰算法、最佳页面算法等。其基本思想是：<font color='red'>总选择那些以后不再需要的或将来最长时间之后才会用到的页面进行淘汰。</font>

![image-20220525160924167](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525160924167.png)

##### 4.2.3 Least Recently Used (LRU) Algorithm

是最佳置换算法的一种近似算法。<font color='red'>该算法淘汰的页面是在最近一段时间里较久未被访问的那一页。</font>它的基本思想是根据程序执行时所体现出的局部性来考虑的，即那些刚被使用过的页面，可能马上还要被使用，而那些在较长时间里未被使用的页面，一般说可能不会马上使用到。

![image-20220525161145178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525161145178.png)

* <font color='red'>中断次数和page fault不是一个东西！！！</font>



###### 4.2.3.1 How to implement LRU replacement?(计数器实现和栈实现)

如何找到一个长时间没有使用过的页面?

Two implementations are feasible:

1. Counter implementation(计数器实现)
2. Stack implementation(栈实现)

1.Counter implementation(计数器实现)

![image-20220525161755182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525161755182.png)

2.Stack implementation(栈实现)

![image-20220525162045847](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525162045847.png)

![image-20220525162108639](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525162108639.png)

###### 4.2.3.2 LRU Approximation Algorithms（LRU近似算法）

![image-20220525162410186](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525162410186.png)

###### 4.2.3.3 Second-Chance (Clock) Page-Replacement Algorithm

**在内存中保存一个循环的页列表，“指针”(迭代器)指向列表中最后检查的页框架。**

类似于FIFO，添加硬件支持：
页表中加一个reference bit=0，表明该页是否被使用过。每当页被进程访问，bit位被置为1。

维护一个页的换入循环队列c-queue，每次从旧到新遍历队列，如果bit为1，将其置为0，跳过；如果bit=0，将其移出。循环遍历直到找到第一个bit为0的页被置换，置换进来的页放入队列尾部，bit位初始化为0。

![image-20220525162851356](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525162851356.png)

##### 4.2.4 Counting Algorithms

记录每页的引用次数

1. **Least Frequently Used (LFU) Algorithm** （最近最不常用算法）：
   选访问次数最少的页移除
2. **Most Frequently Used (MFU) Algorithm** （最常使用算法）：
   移除访问次数最多的页

### 5. Frames Allocation(帧分配)

#### 5.1 固定分配 Fixed allocation

##### 5.1.1 平均分配 Equal allocation

100个帧，5个进程，每个进程分20个

##### 5.1.2 按比例分配 Proportional allocation

根据进程规模分，10个帧，两进程一个2成一个8成，那么一个进程分2个另一个进程分8个

#### 5.2 优先级分配 Priority allocation

考虑了进程的优先级，如果进程抛出页错误，既可以从自己已分配的页更换，又可以去抢低优先级的页。

#### 5.3 Thrashing 系统颠簸

由于分配帧不够，进程频繁地换页导致换页时间多于执行时间。

## Week9 Tutorial

### 1. EAT的计算

![image-20220531224614219](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531224614219.png)

![image-20220531224625178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531224625178.png)

#### 1.1. 在多级分页中的TLB的EAT问题（基于页面故障）

##### 2.1 多级页表的EAT不存在页面故障

![image-20220531231427399](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531231427399.png)

##### 2.2 多级页表的EAT存在页面故障

![image-20220531231504944](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531231504944.png)

![image-20220531232758288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531232758288.png)

![image-20220531232808469](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531232808469.png)

#### 1.2.EAT基于页面替换的问题（计算如FIFO算法的正确率）

![image-20220531233238900](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531233238900.png)

![image-20220531233415692](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531233415692.png)

![image-20220531233448170](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531233448170.png)

一样，只是算法变化了

![image-20220531233529961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531233529961.png)





## Week10 Lecture Mass-Storage Systems

### 1.Secondary  Storage (二级存储系统)

#### 1.1 Defination of Secondary Storage

“二级存储（secondary storage，auxiliary storage）是计算机主存储器或内存之外的所有可访问数据存储器，是程序和数据长期保存的地方，常见的二级存储设备有（固定/移动）硬盘、光盘、等”

* Save data permanently.永久保存数据
* Slower than memory
* Cheaper and greater than memory.

#### 1.1 Types of Secondary Storage

**Sequential access devices(顺序访问设备):** - 按顺序存储记录，一个接一个。

* 相对永久，并保存大量数据
* 访问时间慢

**Direct access devices（直接访问设备）**：- 将数据存储在具有唯一地址的独立位置。

* 像硬盘一样使用的非易失性存储器
* 容量较小，但比HDD（硬盘驱动器）快得多

### 2. Moving-head Disk Mechanism(磁盘)

![image-20220525183114276](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525183114276.png)

* **Transfer Time（传输时间）= 数据传输的时间/从开始传输到完成传输的时间**

* **Seek time（搜寻时间）= 磁头从一个磁柱移动到另一个磁柱所花费的时间/到达磁道所花费的时间。**

* **Rotational Latency(旋转延迟)=旋转盘片并将所需的磁盘扇区置于读写磁头下所花费的时间**

* **Positioning time / Random access time = seek time + rotational latency**

* **Disk Access Time = the time to perform any operation on the disk.** 

  <font color='red'>seek time + rotational latency + transfer time.</font>

### 3. Disk Structure(磁盘结构)

磁盘作为逻辑扇区的一维数组寻址。

![image-20220525190753073](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525190753073.png)



### 4. Disk Attachment 磁盘连接

**Computer systems can access disk storage in two ways:**(计算机访问磁盘的方式)

#### 4.1 **via I/O ports and this is common on small systems**

**Host-attached storage**：

最常见的接口是

集成驱动电子IDE，先进技术

附件ATA, USB每个允许最多两个驱动器每个主机控制器。

#### 4.2 via a remote host in a distributed file systems

**Storage Area Network(存储区域网):**

光纤通道是最常见的互连，以及InfiniBand(高速连接)

**Network-Attached Storage(网络连接存储)**

通过TCP / IP连接, UDP/IP或主机连接协议，如ISCSI)

### 5. Disk Scheduling(磁盘调度)

<font color = 'red'>Goal: minimize the positioning time最小化定位时间</font>

磁盘调度即对于一个I/O操作序列，如何调度才能尽可能的**减少寻道时间**。

![image-20220525203527453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525203527453.png)

#### 5.1 FCFS调度（First Come First Served）

- **优点：** 实现简单，易于理解，较为公平
- **缺点：** 通常不是最快的算法。磁臂摆动幅度大，导致平均寻道距离大，效率低

![image-20220525203924005](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525203924005.png)

![image-20220525205156596](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525205156596.png)

**===640**

**FCFS在轻负载下工作良好;但一旦负荷增加，服务时间就会长得令人无法接受。**



#### 5.2  SSTF调度（shortest-seek-time-first）

- **算法原理：** 每次都选择处理距离当前磁头位置最近的待处理请求
- **优点：** 大大提高了性能，但不是最优的。
- **缺点：** 因为新请求可能随时抵达，可能导致饥饿。

![image-20220525204243284](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525204243284.png)

**SSTF非常受欢迎，直观上很吸引人。它在中等载荷下工作良好，但在重载下存在局部化问题。**

#### 5.3 SCAN(Elevator)

* 算法原理： 又称电梯调度算法。磁臂从磁盘的一端向另一端移动，磁头经过每个柱面时处理位于该柱面上的请求。到达另一端时改变移动方向继续处理。<font color='red'>(先向左再向右)</font>
* 优点： 避免了饥饿现象。性能较好。
* 缺点： 当磁头到达一端折返往回移动时，在该端等待服务的请求可能很少，因为该区域的请求刚刚被访问过。而另一端请求可能很密集，等待的时间较长。

![image-20220525204616891](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525204616891.png)

**SCAN在轻到中等负载下工作良好，消除了无限期延迟的问题。SCAN在吞吐量和平均服务时间上与SSTF相似。**

#### 5.4 C-SCAN调度

- **算法原理：** SCAN算法的变种。与SCAN算法的不同**是当到达另一端时，会立即返回磁盘扫描开始处**，返回时并不处理请求。
- **优点：** 与SCAN相比更公平，提供了更为均匀的等待时间。
- **缺点：** 移动的柱面较SCAN稍多

![image-20220525204835722](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525204835722.png)

**C-SCAN在中等到重型负载下工作良好，并且在服务时间上有非常小的变化。**

#### 5.5 LOOK调度

- **算法原理：** 是SCAN的变种，区别是磁头不在整个磁盘宽度内移动，而是**只移动到一个方向上的最远**请求为止。
- **优点：** 与SCAN相比提高了效率。

![image-20220525205332817](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525205332817.png)

#### 5.6 C-LOOK调度

- **算法原理：** 是C-SCAN的变种，区别是磁头不在整个磁盘宽度内移动，而是只移动到一个方向上的最远请求为止。
- **优点：** 与C-SCAN相比提高了效率。

![image-20220525205645495](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525205645495.png)



### 6. Disk Management(磁盘管理)

**在空白盘片上创建扇区**

#### Low-level formatting, or physical formatting低级格式，或物理格式

- 分成扇区以便磁盘控制器能读和写(一般在工厂进行)。
- 将磁盘分成由一个或多个柱面组成的扇区。

**自举程序(bootstrap):** 

一般在ROM中

### 7. Swap-Space Management

#### 7.1 交换空间的使用

- 不同操作系统根据实现的内存管理算法，可按不同的方式来使用交换空间。
- 对交换空间数量的高估要比低估安全。这是因为如果系统使用完了交换空间，那么可能会中断进程或使整个系统死机。

#### 7.2 交换空间位置

- 可以在普通文件系统上加以创建。
- 在一个独立的磁盘分区内进行。



#### 7.3 Swap-space management(交换管理)

内核使用**交换映射**来跟踪交换空间的使用

#### 7.4 Swap-space 

-- Virtual memory uses disk space as an extension of main memory (**虚拟内存使用磁盘空间作为主存的扩展**)

### 8. RAID Structure（独立磁盘冗余阵列）

RAID：**Redundant Arrays of Independent Disks.**

* RAID是一种**数据存储系统**，使用多个硬盘驱动器来存储数据。
* RAID是一组**物理驱动器**，在操作系统中被视为一个逻辑驱动器。
* 有几种不同的存储方法，称为级别。

#### 8.1 RAID controller

RAID控制器用于控制RAID。它可能是基于硬件或软件的。

#### 8.2  三个用在RAID的方法

##### 8.2.1 Mirroring

**Mirroring：将数据复制到多个驱动器**

##### 8.2.2 Striping 

**Striping :**将数据分成“块”，并将其连续写入不同的磁盘。

##### 8.2.3 Error correction

**Error correction**: 存储冗余数据，允许检测并可能修复错误。

#### 8.3 The level of RAID级别

![image-20220525234825857](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525234825857.png)

![image-20220525234858060](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525234858060.png)

![image-20220525234916594](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525234916594.png)

7.**RAID 0+1**： 指RAID级别0和RAID级别1的组合。RAID 0提供了性能，而RAID 1提供了可靠性。通常，它比RAID 5有更好的性能和更昂贵的价格。

8.**RAID 1+0**： 也是RAID级别0和RAID级别1的组合。不过是先镜像，再分散。与RAID 0+1相比，它如果单个磁盘不可用，但其镜像仍如其他磁盘一样可用。但RAID 0+1如果单个磁盘不可用，那么整个条就不可访问

![image-20220525235117441](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525235117441.png)

##### 8.3.1 RAID级别的选择

- **RAID 0：** 适用于性能要求高但可靠性要求不高的应用。
- **RAID 1：** 适用于可靠性要求高和快速恢复的应用。
- **RAID 0+1和1+0：** 适用于性能和可靠性要求都高的应用。
- **RAID 5：** 用于存储量大的数据。
- **RAID 6：** 较少有支持，但比RAID 5更可靠。

#### 8.4 RAID Conclusion

RAID是安全的，因为镜像复制了所有的数据。

RAID速度快，因为数据是跨多个磁盘进行条带化;可以同时对不同的磁盘读取和写入大量的数据。

RAID不是<font color='red'>(backup备份)</font>。备份是数据的副本，它存储在其他地方，在空间和时间上都与原始数据分离。

### Week10 Tutorial

### 1.CHS（扇区）

Cylinder-head-sector为硬盘驱动器上的每个物理数据块提供地址的一种早期方法。

<font color='red'>计算方法：在知晓C，H，S的情况下将三者相乘。并乘以每节的字节长度。</font>

![image-20220531235020128](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235020128.png)

**CHS寻址被线性寻址方法——逻辑块寻址(LBA)所取代，LBA通过扇区进行寻址。**

### 2.Transfer Time(传递时间)

<font color='red'>字节块的长度/每秒传递的速度=Transfer Time</font>

![image-20220531235245333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235245333.png)

### 3. IO流在磁盘队列上的移动

#### 3.1 SCAN调度算法

![image-20220531235709870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235709870.png)

![image-20220531235744338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235744338.png)

#### 3.2 FCFS调度算法

![image-20220531235805620](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235805620.png)

![image-20220531235817982](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235817982.png)

#### 3.3 SSTF调度算法

![image-20220531235850460](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235850460.png)

![image-20220531235859876](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235859876.png)

#### 3.4 C-SCAN调度算法

![image-20220531235932685](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235932685.png)

![image-20220531235943803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220531235943803.png)





## Week12 Lecture File System

### 1文件属性 Attribute：

Name-使用者可以看到的名字
Identifier-由文件系统特殊标识的标签
Type-该文件是一个目录、一个程序映像、一个用户文件、一个链接等
Location-指向文件位置
Size-文件大小·protection-控制用户权限
Time，data and user identification-记录文件创建，最后编辑时间，最后使用时间等

Position: 当前next-read/next-write 的指针位置。**只在内存中**

Usage：公开计数。 **只在内存中**

### 2.文件操作 Operations

·create创建-OS必须能够使用空闲空间创建文件
·write写-通过写指针
·read读-通过读指针
·save保存-保存文件到磁盘上的空间空间
·reposition within file文件重定位
·delete删除
·truncate截断-删除文件内容但是保留属性
·open打开-在进程操作文件之前，文件必须被打开，以加载入内存
·close关闭-不需要的时候移出内存。

Open File Table：因为打开操作会获取相应文件的基础属性，用一个表来记录这些已打开的文件的属性。


### 3. 文件逻辑策略 logical categories：
#### 3.1 共享文件shareable files

：可以被本地访问和网络共享

#### 3.2非共享文件unsharable files

：只能本地访问

#### 3.3 变量文件variable files

：可以在任意时刻改变

#### 3.4静态文件static files

：如果没有系统管理员操作，则不能改变

### 4. 访问文件的方法 Access Methods

##### 4.1 顺序访问 Sequential Access

模拟磁带操作，文件里的内容按顺序被以字节形式访问。

##### 4.2 直接访问 Direct Access

直接跳转到相应记录然后读取

##### 4.3 下标访问 Indexed Access

使用多个下标，每个下标对应一个文件属性，通过这些索引筛选并搜索主文件中的记录

### 5.目录和磁盘结构 Directory and Disk Structure

一个磁盘既可以一整个作为文件系统提供服务，也可以被划分成多个**分区，片或小磁盘**（multiple partitions, slices, or mini-disks）各自拥有自己的文件系统。

磁盘/分区（Disk/partition）划分为“块”或“扇区”

* 现代磁盘有512字节或更多扇区
* 文件系统通常以4 KB的块大小工作

![image-20220509145924920](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509145924920.png)

#### 5.1 Directory 目录

##### 5.1.1 对目录的操作

![image-20220601011746071](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601011746071.png)

##### 5.1.2 目录逻辑结构 Logical Structure of a directory

###### 5.1.2.1 **single-level directory**单级目录

单一目录，根据目录下记录所有的文件

![image-20220509150143024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509150143024.png)

###### 5.1.2.2 **two-level directory**二级目录
为每个用户指定各自的目录，形成<font color='blue'>主目录和用户目录</font>

![image-20220509151248207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509151248207.png)

###### 5.1.2.3**hierarchical/tree-structured directories**目录树状结构

分层目录，<font color='blue'>绝对路径absolute path和相对路径relative path</font>

![image-20220509151341956](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509151341956.png)

###### 5.1.2.4 **acyclic-graph directories（非循环目录）**

文件目录支持对同一个文件的共享操作，既**多个用户操作同一文件**
文件被删除后仍然保留指向文件位置的悬挂指针

![image-20220509151552022](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509151552022.png)

##### 5.1.3 依靠目录可以完成的操作

1. 文件查找 2 文件创建 3. 删除文件 4. 建立目录 5. 重命名文件 6. 遍历文件系统。

#### 5.2 系统挂载 File-System Mounting

挂载Mounting=<font color='red'>将文件系统的各个部分挂载到目录结构中。</font>

1. 装载mounting：将设备添加到用户设备上，如：插入U盘
2. 装载位置mounting point：附加设备的目录在原文件环境的附加位置，如：U盘在电脑文件目录的位置

### 6. 文件分享 File Sharing

#### 6.1 分享必须通过保护方案

1. <font color = "red">通过保护方案protection scheme进行共享</font>
   1. • Manually via programs like FTP or SSH (手动)
   2. • Automatically, seamlessly using **distributed file systems**（自动）
   3.  • Semi automatically via **the world wide web**（半自动）

##### 6.1.2 分布式系统（Distributed information Systems）

1. 在分布式系统（Distributed information Systems）中，使用网络共享

##### 6.1.3 Client-server model (客户-服务器模型)

1. Client-server model (客户-服务器模型)
   1. Network File System (NFS)通常是可行方法
   2. Common Internet File Systems CIFS
   3. Distributed Information Systems分布式信息系统实现了对远程计算所需信息的同一访问。

![image-20220601012505122](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601012505122.png)



#### 6.2 多用户分享

在多用户系统中，使用访问权限access rights和同时访问管理the management of simultaneous access。
拥有者owner和组group的概念：
其中user ID区分用户，group ID区分群组，各自有各自的权限范围。

#### 6.3 远程共享的问题

可能会产生网络或服务器故障，导致文件系统需要应对的故障变多，
复原信息时涉及到了每个远程请求的状态
无状态协议（如NFS）在每个请求中明文展示信息，安全性低，但可以轻松恢复文件



### 7. Protection 保护

<font color='red'>通过限制可以访问的文件类型控制访问文件.  创建者应当设定文件操作权限和用户访问权限</font>

访问类型：Read， Write，  Execute， Append， Delete， List

![image-20220601012728021](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601012728021.png)

#### 7.1 访问控制链表 Access-Control List (ACL)

<font color='red'>记录了每个文件的有权限的用户名和每个用户允许的访问类型。</font>
访问模式分为：读read, 写write, 运行execute

· 写包括了打开，读取，编辑等一系列权限。

访问用户分为：拥有者owner，组group，访客public access / universe

![image-20220509154001324](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509154001324.png)



### 8. 文件的系统结构

![image-20220509154221774](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509154221774.png)



#### 8.1文件系统的应用 File System Implementation

##### 8.1.1 On disk Structure

On-disk: <font  color='red'>在磁盘上，文件系统可能包含关于如何引导存储在那里的操作系统、块的总数、空闲块的数量和位置、目录结构和单个文件的信息</font>

1. Boot control block：引导控制块，位于每个卷的第一块，负责引导操作系统所需要的核心
2. File Control Block：文件控制块，包含文件的信息，如大小，所有者，访问权限，创建日期等。
3. Volume control block：卷控制块，包含卷的信息，如分区块数，块大小，空闲块数量等。
4. Free list：记录未被分配的块
5. Files and directories
   

###### 8.1.1.1 通过FCB进行文件映射

文件系统使用<font color='red'>FCB存储的文件中的逻辑位置将其映射到磁盘上的物理位置。</font>

FCB包含一个文件的块列表及其对应的磁盘块地址。要在文件中的某个位置检索数据，文件系统首先将逻辑位置转换为磁盘中的物理位置。

![image-20220601013213306](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601013213306.png)

##### 8.1.2 In memory

In memory: <font color='red'>内存中的信息用于文件系统管理和通过缓存提高性能。</font>

1. mount table：安装表，包含文件系统安装指针，文件系统类型等。
2. system-wide open-file table SOFT：打开文件表，记录每个已打开文件的FCB副本
3. per-process open-file table POFT：打开文件表，记录被进程打开的文件信息，每个条目还指向SOFT
4. Buffers：缓存，保存访问过的目录信息

##### 8.1.3 打开文件步骤

在SOFT中查询，该文件是否已经被其他进程所使用
如果是，将会在POFT中创建一个指向SOFT的指针
如果不是，遍历所有FCB，找到该文件的FCB，将该文件的FCB移入内存中读取
FCB在内存中被复制给SOFT，POFT里创建一个指向SOFT的指针
文件系统返回指向POFT元素的指针，这个指针被称为file descriptor or file handle

### 9. Directory Implementation 目录实现

A directory is a container which contains file and folder. 目录是包含文件和文件夹的容器

![image-20220509164605839](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509164605839.png)

#### 9.1[线性](https://so.csdn.net/so/search?q=线性&spm=1001.2101.3001.7020)列表

最为简单的目录实现方法是使用存储文件名和数据块指针的线性列表。这种方法编程简单但运行较为费时。

#### 9.2 哈希表

哈希函数易于查找，但是会出现冲突，降低效率。但是仍要优于线性列表

#### 9.3 分配方法 Alocation Methods

将文件分配给物理磁盘的不同策略

##### 9.3.1 连续分配 Contiguous

文件会被分配给**连续**的块
优点：简单，可顺序，可随机
缺点：得找合适的空闲区域，产生碎片fragmentation，
解决方法：

1. compaction off-line(downtime) ：用一个额外盘转移全部文件清理碎片
2. on-line：本地移动文件清理碎片

![image-20220509164842262](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509164842262.png)

##### 9.3.2 链接分配 Linked  

 文件被分配给分散的块，块与块之间以链表形式相连。
优点：简单，没有碎片，文件可以轻松拓展
缺点：存放指针占空间，只能挨个读取，容易断链子
解决：

将块聚合成簇（cluster）减少指针数量
采用文件分配表File Allocation Table, FAT：将链表间关系存储为一维链表，放在簇的开头。
File Allocation Table: FAT, used by MS-DOS operating system is a variation of linked allocation, where all the links are stored in a separate table at the beginning of the disk
![image-20220509165105697](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509165105697.png)

![image-20220509165126085](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509165126085.png)

##### 9.3.3 索引分配indexed

相比于FAT更灵活，把每个文件分散给分散的块，文件系统指向的索引块记录了所有这些分散块的索引和顺序
索引块index block的实现：通过链表（一个索引块连一个索引块），通过多层（第一个索引块连多个索引块）
优点：支持顺序，随机访问，文件大小可变，没有碎片
缺点：小文件也会占据一个完整的块作为索引块，小文件数量多时浪费空间

![image-20220509165232333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220509165232333.png)

#### 9.4 空闲空间管理Free-Space Management
使用空闲空间列表free-space list 记录可用块，五种方法

1. bit vector：1表示块可用，0表示块已用
2. Linked List：用链表链接所有空闲块
3. Grouping：在第一个空闲块内存储其余空闲块索引
4. Counting：记录每一个空闲块之后连续空闲块数量
5. Space Maps：建立位图，块的使用状态改变时修改位图。
   

## Week11 Tutorial

 #### 1. 系统和进程的分配问题

![image-20220601014937671](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601014937671.png)

![image-20220601014959987](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601014959987.png)

#### 2.使用relocation register计算物理和逻辑地址

![image-20220601015116619](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601015116619.png)

![image-20220601015128187](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601015128187.png)

#### 3. 磁盘移动问题

![image-20220601015249845](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601015249845.png)

![image-20220601015304103](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601015304103.png)

#### 4. 多级分页地址的虚拟内存系统

![image-20220601020310905](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601020310905.png)

![image-20220601020321634](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601020321634.png)

#### 5. 虚拟内存和物理内存的转换

![image-20220601020204326](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601020204326.png)

因为题目要求所有的地址和虚拟代码编号都以16进制表示、page size=1mb=2^20=十六进制下的16^5, page size=5=offset 

![image-20220601020212149](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601020212149.png)

## Week13 I/O系统

### 1. IO硬件 I/O Hardware

#### 1.1 Port端口

：设备之间的连接点。

#### 1.2 Bus总线

：daisy chain or shared direct access
····PCI：PC中常见的总线
····expansion bus：连结相对较慢的设备

#### 1.3 Controller主机适配器

：操作端口，总线和设备的集成电子器件或额外电路板。包含处理器和私有内存，能够通过总线控制器和内存与各种控制器对话。
![image-20220516144841816](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220516144841816.png)

##### 1.3.1 Controller的工作原理:

**处理器如何向控制器发送命令执行IO传输：**

1. 每个**控制器**中有用于通话CPU的寄存器
2. 此外，许多设备还有操作系统可以读写的**缓冲区**（打印机）

##### 1.3.2 **控制器中的寄存器种类**：


###### 1.3.2.1 data-in register <font color='red'>**数据输入寄存器**</font>
###### 1.3.2.2 data-out register <font color='red'>**数据输出寄存器**</font>
###### 1.3.2.3 status register 状态寄存器

-提供任务相关信息（是否完成，是否故障）

###### 1.3.2.4 control register **控制寄存器**

-接受主机发送的命令

##### 1.3.3 **CPU如何与控制寄存器和设备缓存交流：**

1. 直接IO指令-Direct I/O instructions
   每个寄存器被分配一个8bit或16bit的端号，然后CPU通过IO指令读写控制寄存器
2. 内存映射IO-Memory-mapped I/O
   把寄存器映射到内存空间，CPU通过内存访问的方式读写

### 2. IO通信技术：处于用户请求和设备之间的交流模式

#### 2.1 Polling轮询

CPU忙等并定期检测通道状态位，如果通道繁忙，CPU执行其他处理任务直到通道空闲。

#### 2.2 Interrupt-driven I/O 中断

CPU使用中断与设备交流，当设备有数据要传输或操作完成时抛出中断请求给CPU，CPU在每个指令周期后会检测中断，随后CPU将控制转到中断处理程序，开始IO传输。
Non-maskable：非屏蔽中断用于严重错误情况
Maskable：可屏蔽中断又设备控制器发起请求

![image-20220516150140774](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220516150140774.png)

与设备交互的基本协议：
·Wait for drive to be ready
·Write parameters to control registers
·Start the I/O
·Data transfer
·Handle interrupts-简单方法是块中断，更灵活的方法是当传输完成时抛出结束中断
·Error handling

### 2.3 Direct Memory Access 直接内存访问(DMA)

需要硬件支持（**DMA controller**），适合数据较大的情况，一次读取一个字符块，IO设备和内存间直接传输数据，中断请求由DMA在传输完成时发出。
如果知道虚拟内存，可以更加高效-Direct Virtual Memory Access DVMA

处理IO由DMA完成，通知处理操作又CPU向DMA通知，CPU需要告知DMA以下内容：
· type of request：请求类型（读/写）
· address of the IO device：需要IO的设备地址
· the start address of the data：需要写入或读取的数据在内存中的空间

![image-20220601080335831](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601080335831.png)

### 3. IO的应用接口

#### 3.1 块与字符设备Block and Character Devices

##### 3.1.1 **块设备：**

- 命令包括read, write, seek。
- 访问方式包括生I/O,直接I/O和内存映射。

##### 3.1.2 **字符设备：**

- 命令包括get，put。
- 可以构造库以提供具有缓冲和编辑功能的按行访问。

#### 3.2 网络设备（Network Devices）

* 比如Socket接口。

#### 3.3 阻塞与非阻塞IO流（Blocking and Non-blocking I/O）

阻塞IO: 指的是需要内核IO操作彻底完成后，才返回到用户空间执行用户的操作。阻塞指的是用户空间程序的执行状态。传统的IO模型都是同步阻塞IO。在Java中，默认创建的socket都是阻塞的。

**非阻塞IO：**指的是用户空间的程序不需要等待内核IO操作彻底完成，可以立即返回用户空间执行用户操作，即处于非阻塞的状态，与此同时内核会立即返回给用户一个状态值。

简单来说：阻塞是指用户空间（调用线程）一直在等待，而不能干别的事情；非阻塞是指用户空间（调用线程）拿到内核返回的状态值就返回自己的空间，IO操作可以干就干，不可以干就去干别的事情。

#### 3.4 时钟与定时器（Clocks and Timers）

- 可以获取当前时间，逝去的时间。
- 可以设置定时器，在T是触发操作X。
- 测量逝去时间和触发操作的硬件称为可编程间隔定时器，它可被设置为等待一定时间，然后触发中断。

- 可以获取当前时间，逝去的时间。
- 可以设置定时器，在T是触发操作X。
- 测量逝去时间和触发操作的硬件称为可编程间隔定时器，它可被设置为等待一定时间，然后触发中断。



### 4. IO内核子系统Kernel I/O Subsystem

#### 4.1 IO调度

调度一组I/O就是确定一个合适的顺序来执行这些请求。应用程勋发布的系统调用顺序不一定总是最佳选择，调度能改善系统整体性能，如磁盘调度，重新安排服务顺序增加性能就是I/O调度的核心。

操作系统开发人员通过为每个设备维护一个请求队列来实现调度

#### 4.2 缓冲Buffering

![img](https://img-blog.csdnimg.cn/20210123134503896.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxODgyNjg2,size_16,color_FFFFFF,t_70)

![image-20220601081721487](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220601081721487.png)





#### 4.3 高速缓存

#### ![img](https://img-blog.csdnimg.cn/20210123134514950.png)



#### 4.4 假脱机

**目的：** 解决独占设备的并发访问问题以提高设备利用率。

假脱机是用来保存设备输出的缓冲区，这些设备不能接收交叉的数据流。比如，应用程序的输出先是假脱机到一个独立的磁盘文件上，当应用程序完成打印时，假脱机系统将对应的待送打印机的脱机文件进行排队。

## Week13 Tutorial

1. 说明将功能放置在设备控制器而不是内核中的三个优点和三个缺点。

答:三个优点:

a. bug不太可能导致操作系统崩溃

b.使用专用硬件和硬编码算法可以提高性能

c.将算法移出内核简化了

三个缺点:

a.新的固件版本更难修复bug，或者需要新的硬件

b.改进算法同样需要硬件更新，而不仅仅是内核或设备驱动程序更新

c.嵌入的算法可能与应用程序使用的设备冲突，导致性能下降。

2. 13.2节中的握手示例使用了2位:一个繁忙位和一个命令就绪位。是否有可能实现这个握手只有1位?如果是，请描述协议。如果不是，请解释为什么1位不够。

这是可能的，使用以下算法。让我们假设我们简单地使用了繁忙位(或命令就绪位;这个答案无论如何都是一样的)。位断开时，控制器处于空闲状态。主机写入data-out，并设置该位以表示操作已经就绪(相当于设置命令就绪位)。当控制器完成时，它清除繁忙的部分。然后主机启动下一个操作。

这种解决方案要求主机和控制器对同一位具有读写权限，这可能会使电路复杂化，并增加t的成本

3. 为什么系统可能使用中断驱动的I/O来管理单个串口，并使用轮询I/O来管理前端处理器(如终端集中器)?

轮询可能比中断驱动的I/O更有效。这是I/O频繁且持续时间短的情况。尽管单个串口执行I/O的频率相对较低，因此应该使用中断，但是串口的集合(比如终端集中器中的那些串口)可以产生大量短的I/O操作，并且对每个串口进行中断可能会在系统上造成沉重的负载。一个定时轮询循环可以减轻负载，而不会因为循环而浪费太多资源，因为不需要I/O。

4. 如果处理器在I/O完成之前多次迭代繁忙等待循环，那么轮询I/O完成可能会浪费大量CPU周期。但是，如果I/O设备已经准备好服务，轮询可能比捕获和调度中断更有效。描述一种混合策略，结合了轮询、休眠和中断的I/O设备服务。对于这三种策略(纯轮询、纯中断、混合)中的每一种，都描述了一种计算环境，在这种环境中，该策略比其他任何一种策略都更有效。

答:混合方法可以根据I/O操作等待的长度在轮询和中断之间切换。例如，我们可以轮询和循环N次，如果设备在N+1时仍处于繁忙状态，我们可以设置中断和睡眠。这种方法可以避免长时间的繁忙等待周期。这种方法适用于很长或很短的繁忙时间。如果I/O在N+T(其中T是少量的周期)完成，那么效率将会很低，这是由于轮询加上设置和捕获中断的开销。纯轮询的最佳等待时间非常短。对于已知的长等待时间，中断是最好的

5. 为什么随着CPU速度的提高而提高系统总线和设备速度是很重要的?

答:

考虑一个执行50% I/O和50%计算的系统。将该系统上的CPU性能翻倍只会使总体系统性能提高50%。将系统两个方面都加倍将使性能提高100%。一般来说，重要的是要消除当前的系统瓶颈，并提高整体系统性能，练习练习49，而不是盲目地提高单个系统组件的性能。

6. 区分STREAMS驱动程序和STREAMS模块

答:

STREAMS驱动程序控制一个可能涉及到STREAMS操作的物理设备。STREAMS模块修改磁头(用户界面)和驱动程序之间的数据流。

