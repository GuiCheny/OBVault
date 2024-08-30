## 定义

Lasso回归算法（Lasso Regression Algorithm），叫最小绝对值收敛和选择算子算法（least absolute shrinkage and selection operator）。

代价函数添加L1-范数作为惩罚项，L1正则化。

$$
Cost ((w) = \sum_{i=1}^{N} \left( y_i - w^T x_i \right)^2 + \lambda \left\| w \right\|
$$

训练目标为：

$$
w = \text{argmin} \left( \sum_{i=1}^{N} \left( y_i - w^T x_i \right)^2 + \lambda \left| w \right| \right)
$$

## 解法



