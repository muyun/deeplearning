### Notes on Neural networks

#### 2018-12-28 
    * [Structure of code in python is Key](https://docs.python-guide.org/writing/structure/#)

    - Python Modules - main abstraction layers
        + keep module names short
        + the included code in Python is isolated in a module namespace
          => needn't worry that included code could have unwanted effects
        + "import modu" -> readability

    - Packages
        + "__init__.py" -> share operations, any variable, function, or class

    - Object-oriented programming
        + pure functions -> no context or side-effects
        


#### Notes on deep learning
    * ch2
    - 通过**与非门**的组合可以实现计算机 ? [The elements of computing systems](http://www1.idc.ac.il/tecs/plan.html) 
    - 与非门可以使用感知机实现 => 通过感知机的组合可以表示计算机  
    - 两层感知机就能构建计算机， 因为两层感知机可以表示任意函数

    * ch3
    - 神经网络可以**自动地从数据中学习到合适的权重参数** 
        + a = WX + b 
    - **激活函数** - y = h(a)
        + 必须使用 非线性函数 
        + 发挥叠加成所带来的优势 
    - **batch 批处理** 可以缩短处理时间
        + 因为数值计算的库都能够高效处理大型数组运算的最优化
        + 批处理一次性计算大型数组要比分开速度更快 - 数据传送成为瓶颈

    * ch4
    - 由人来驱动 - 人来设计算法解决问题，
    - 数据驱动 - 机器学习是由机器**从收集到的数据中找出规律** ->算法
    - 选 mini-batch -> 计算mini-batch的损失函数的值 - 梯度 -> 更新参数 <- loop
    - 从训练数据中随机选出一部分数据 - mini-batch - 目标是减少mini-batch的损失函数的值
        + 神经网络 **以损失函数为指标** 寻找最优权重参数
    - 以识别精度作为指标，参数的导数在绝大多数地方都会变成0
        + 识别精度**对微小的参数变化**基本上没有什么反应， 它的值是不连续，突然地 变化

    - **梯度法** - 以梯度的信息为线索，决定前进的方向 

    - **学习率** 由人工设定 - 在一次学习中，在多大程度上更新参数 

    * ch5


#### reference