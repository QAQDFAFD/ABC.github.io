# 目录

## 第一章 绪论

### 1.1 基本概念

## 第二章 控制系统的数学模型

### 2.1 控制系统的时域数学模型

#### **数学模型的类型**

时域数学模型 -> **微分方程**、差分方程、状态方程

复数域数学模型 -> **传递函数**、结构图与**信号流图**

频域数学模型 -> 频域特性

#### **数学模型之间的转换**

频域和复数域之间的转换：

在频域中令 jw = s 即可将数学模型变为复数域模型

在复数域中令 s = jw 即可将数学模型变为频域模型

下面**重点**来看时域数学模型：

时域数学模型一般用微分方程来描述

微分方程的动态样式：

![image-20220429220201730](https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429220201730.png)

![image-20220429220234142](https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429220234142.png)

我们就是要在不同的环境中使用不同的数学模型

#### ==重点：关于线性常微分方程的求解==

<span style="color:#0000FF">拉式法：</span>

**step one：**

考虑初始条件，对微分方程的每一项分别进行拉氏变换，将微分方程转化成变量s的代数方程；

![](https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/20220913100320.png)

**step two：**

由代数方程求出输出量的拉式变换表达式；

![image-20220429220350988](https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429220350988.png)

**step three:**

通过反拉氏变换得到输出量的表达式；

#### <span style="background-color:#C1FFC1">具体的因式分解的方式</span>

真分式的情况下，对分式的分母进行因式分解

一般情况下分为三种情况处理：

* 单根
* 共轭复根
* 重根

### 2.2 控制系统的复数域数学模型

一般用传递函数、结构图、信号流图描述复数域模型

典型环节及其数学模型

#### **结构图与信号流图**

##### 结构图

##### 信号流图

#### ==梅森增益公式==



### 2.3 控制系统的结构图与信号流图

### 2.4 闭环传递函数与误差传递函数

## 第三章 线性系统的时域分析方法

### 3.1 线性系统的稳定性

### 3.2 时间响应的性能指标与一阶系统的时域分析

### 3.3 二阶系统的时域分析

### 3.4 二阶系统的性能改善

### 3.5 线性系统的稳态误差计算

#### 终值定理求稳态误差

**例题：**

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220428215512961.png" alt="image-20220428215512961" style="zoom: 33%;" />

**答案：**这里的第二部分的问题中无法使用终值定理来求解稳态误差，因为极点在虚轴上，不在**左半开平面**

#### 系统类型Type与静态误差系数

根据不同的输入，可以得到不同的**静态误差系数**

| 类型\误差系数 | 静态位置误差系数 Kp | 静态速度误差函数  Kv | 静态加速度误差系数  Ka |
| :-----------: | :-----------------: | :------------------: | :--------------------: |
|      0型      |          K          |          0           |           0            |
|      Ⅰ型      |          ∞          |          K           |           0            |
|      Ⅱ型      |          ∞          |          ∞           |           K            |

| 类型\e~ss~\输入 |  1   |  2   | 3    |
| :-------------: | :--: | :--: | ---- |
|       0型       |      |  ∞   | ∞    |
|       Ⅰ型       |  0   |      | ∞    |
|       Ⅱ型       |  0   |  0   |      |

**例题：**

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220428220152627.png" alt="image-20220428220152627" style="zoom:33%;" />

**答案：**二阶系统，K = 1，0型系统

## 第四章 线性系统的根轨迹法

### 4.1 根轨迹法的基本概念

#### 根轨迹的基本概念

**根**：极点

**根轨迹**：开环系统某一个参数从零变到无穷时，极点在s平面的轨迹

一个根就会有一个轨迹

**根轨迹法**：利用图解法求根轨迹

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429180955069.png" alt="image-20220429180955069" style="zoom: 50%;" />

根轨迹提供的信息：

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429181419991.png" alt="image-20220429181419991" style="zoom: 33%;" />

#### 根轨迹法的基本法则（作根轨迹）

##### 法则一：根轨迹的分支数，对称性和连续性

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429182019690.png" alt="image-20220429182019690" style="zoom: 67%;" />

##### 法则二：根轨迹的起点与终点

根轨迹起始于**开环极点**

终止于**开环零点**

有n条根轨迹，只有 n-m 条根轨迹是终止在开环零点的

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429182501065.png" alt="image-20220429182501065" style="zoom:67%;" />

##### 法则三：根轨迹的渐近线

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429182941190.png" alt="image-20220429182941190" style="zoom:67%;" />

以下为 **n-m 为1、2、3、4**的情况

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429183358175.png" alt="image-20220429183358175" style="zoom:67%;" />

##### 法则四：根轨迹在实轴上的分布

数右侧**零、极点之和**

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429184105622.png" alt="image-20220429184105622" style="zoom:67%;" />

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429184407997.png" alt="image-20220429184407997" style="zoom:67%;" />

##### 法则五：根轨迹的分离点与分离角

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429185043059.png" alt="image-20220429185043059" style="zoom:67%;" />

凭借以下的特点可以帮助判断分离点的位置

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429185232659.png" alt="image-20220429185232659" style="zoom:67%;" />

**例题：**

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429185543404.png" alt="image-20220429185543404" style="zoom:67%;" />

##### 法则六：根轨迹的起始角与终止角

先看有无是负数的零点或者极点

起始角：从起点触发时的角度

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429190532039.png" alt="image-20220429190532039" style="zoom:67%;" />

终止点：进入开环零点的角度

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429190732640.png" alt="image-20220429190732640" style="zoom:67%;" />

**例题：**

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191022811.png" alt="image-20220429191022811" style="zoom:67%;" />

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191127441.png" alt="image-20220429191127441" style="zoom:67%;" />

##### 法则七：根轨迹与虚轴的交点

（根轨迹与虚轴相交了 -> 出现了纯虚根）

从渐近线判断：根轨迹会沿着渐近线趋于无穷远，所以如果渐近线与y轴相交，一般根轨迹就会有纯虚根

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191929375.png" alt="image-20220429191929375" style="zoom:67%;" />

* 方法一：劳斯表
* 方法二：代数法

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191416479.png" alt="image-20220429191416479" style="zoom:67%;" />

例题：

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191626647.png" alt="image-20220429191626647" style="zoom:67%;" />

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429191657182.png" alt="image-20220429191657182" style="zoom:67%;" />

##### 法则八：闭环特征根的和与积

和一定、积一定

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429192641053.png" alt="image-20220429192641053" style="zoom:67%;" />

### 4.2 利用根轨迹分析系统的性能

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429194838186.png" alt="image-20220429194838186" style="zoom:67%;" />

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429195034083.png" alt="image-20220429195034083" style="zoom:67%;" />

根轨迹向右偏移，导致系统的不稳定

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429195310049.png" alt="image-20220429195310049" style="zoom:67%;" />

## 第五章 线性系统的频域分析

### 5.1 频域特性的基本概念

#### 频域特性的几何表示

##### 幅相 频率特性曲线图 --- 奈奎斯特图

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429201818075.png" alt="image-20220429201818075" style="zoom: 67%;" />

##### 对数 频率特性曲线图 --- 伯德图

（幅频+相频）

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429202414951.png" alt="image-20220429202414951" style="zoom:67%;" />

对数 频率特性曲线的意义：

<img src="https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429202645836.png" alt="image-20220429202645836" style="zoom:67%;" />

![image-20220429203222566](https://picgo-use-images.oss-cn-shanghai.aliyuncs.com/images/image-20220429203222566.png)
