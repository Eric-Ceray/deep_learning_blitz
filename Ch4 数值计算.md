# Ch4 数值计算

机器学习算法需要大量的数值计算：即通过迭代过程更新解的估计值来解决数学问题的算法。

数值计算的常见操作：优化、线性方程组的求解。

对于数字计算机来说：实数无法在有限内存下精确表示。

## 4.1 上溢和下溢

连续数学在数字计算机上的根本困难是，我们需要通过有限数量的位模式来表示无限多的实数。

一种极具毁灭性的舍入误差是下溢（underflow）。

另一种极具破坏力的数值错误形式是上溢（overflow）。

softmax函数：
$$
\text{softmax}(\pmb x)_i = \frac{\exp(x_i)}{\sum_{j=1}^n\exp(x_j)}
$$
一个典型的例子，可以用$softmax(z)$来解决：
$$
\text{softmax}(\pmb z)= \text{softmax}(\pmb x-\max(\pmb x))
$$
另外，还要实现一个单独的函数，以数值稳定的方式计算$logsoftmax$。

## 4.2 病态条件

条件数指的是函数相对于输入的微小变化而变化的快慢程度。

## 4.3 基于梯度的优化方法

梯度下降：gradient descent。

学习率的选择：线搜索。

### 4.3.1 梯度之上：Jacobian和Hessian矩阵

## 4.4 约束优化

## 4.5 实例：线性最小二乘

