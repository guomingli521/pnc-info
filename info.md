# 移动机器人路径规划应用及其实现案例

## 行业应用

### 市场概述
新兴行业，技术初步成熟，具有想象空间

涉及领域广阔，盈利模式未知,成本控制困难,技术护城河不够深

大厂观望，小厂摸索，独角兽寥寥无几

### 送餐/迎宾机器人
场景：动态场景

多机调度 

<center> <video src="https://github.com/guomingli521/pnc-info/blob/main/video/pd.mp4?raw=true" width="400px" height="300px" controls="controls"></video> </center>

### 物流/仓储/安防/巡检机器人
场景：非结构化道路

路网 规定道路行驶

### 清洁/割草机器人
场景：室内、室外通用场景

贴边 梯控 自动覆盖 回充 回洗

<center> <video src="https://github.com/guomingli521/pnc-info/blob/main/video/gs.mp4?raw=true" width="400px" height="300px" controls="controls"></video> </center>

### 自动驾驶
场景：城市道路,封闭道路，高速

交通规则 自动泊车 车道内避障 超车

## 核心技术点

### 规划算法

在拥有感知(地图)和定位(位置)模块的基础上，通过规划算法实现任务需求

输入地图+位置 输出任务实现方法(逻辑+算法)

#### 规划算法所需要考虑的问题和要求
输入任务+地图+位置，输出安全光滑路径,保证安全性，实时性(10hz)

#### 基于搜索的规划算法
dijkstra 

![dijkstra](https://github.com/guomingli521/pnc-info/blob/main/gif/Dijkstra.gif?raw=true#pic_center =200x200)

astar 

![astar](https://github.com/guomingli521/pnc-info/blob/main/gif/Astar.gif?raw=true#pic_center =200x200)

hybridastar

![hybrid_astar](https://github.com/guomingli521/pnc-info/blob/main/image/hybrid_astart_1.png?raw=true#pic_center =200x200)
![hybrid_astar](https://github.com/guomingli521/pnc-info/blob/main/image/hybrid_astart_2.png?raw=true#pic_center =200x200)
![hybrid_astar](https://github.com/guomingli521/pnc-info/blob/main/image/hybrid_astart_3.png?raw=true#pic_center =200x200)

rs curve

![rs](https://github.com/guomingli521/pnc-info/blob/main/gif/rs.gif?raw=true#pic_center =200x200)

#### 基于采样的规划算法
rrt 

![rrt](https://github.com/guomingli521/pnc-info/blob/main/gif/RRT_2D.gif?raw=true =200x200)


dwa 

teb

#### 轨迹优化
minimumsnap

### 控制算法

#### 控制算法所需要考虑的问题和要求
输入路径+位置，输出速度控制指令，保证稳准快

#### 速度规划
横纵向速度分离控制，topp

#### pid

#### mpc

### 决策及行业特需算法

#### 调度编队
组网 状态机

#### 自动覆盖
之字清扫

回字清扫

优化方法的改进

#### 贴边与居中行驶


#### 交通规则


#### 车道内规划
跟车

超车

车道内避障

#### 强化学习的尝试
逻辑策略上的应用

### 其他延伸模块

#### 地图构建
栅格地图

距离场

#### 软件框架
ros

apollo

#### 仿真平台
gazebo

nvidia


## 挑战与展望

### 机器人与人的关系(需求）
机器人应当完成怎样的工作

### 机器人与钱的关系(成本)
时间成本 价格成本 人力成本 机器人工作效率
商业模式的探索

### 机器人与技术的关系(可行性）
技术飞速迭代
全民工程师的时代





