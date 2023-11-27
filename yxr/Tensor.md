---
title: Tensor
description: 
published: true
date: 2023-11-27T10:49:48.091Z
tags: 
editor: markdown
dateCreated: 2023-11-27T10:35:46.011Z
---

# Tensors

> 张量是多维数组的泛概念。
{.is-info}

## 张量的基本操作
## 内积

对应元素相乘并求和。

$$
\left< \mathcal{X}, \mathcal{Y} \right> = \sum \limits_{i_{1}=1}^{I_{1}}\sum \limits_{i_{2}=1}^{I_{2}} \dots \sum \limits_{i_{N}=1}^{I_{N}} x_{i_{1}i_{2} \dots i_{N}} y_{i_{1}i_{2} \dots i_{N}}
$$

## 矩阵化(模n展开)

<img src='/面上/模n展开.png'>

张量$\mathcal{X} \in \mathbb{R}^{3\times4\times2}$:

$$
\mathbf{X}_{1}=\left[\begin{matrix}
1 & 4 & 7 & 10 \\
2 & 5 & 8 & 11 \\
3 & 6 & 9 & 12
\end{matrix}\right], \mathbf{X}_{2}=\left[\begin{matrix}
13 & 16 & 19 & 22 \\
14 & 17 & 20 & 23 \\
15 & 18 & 21 & 24
\end{matrix}\right]
$$

其展开为：

$$
\begin{gathered}
\mathbf{X}_{(1)}=\left[\begin{matrix}
1 & 4 & 7 & 10 & 13 & 16 & 19 & 22 \\
2 & 5 & 8 & 11 & 14 & 17 & 20 & 23 \\
3 & 6 & 9 & 12 & 15 & 18 & 21 & 24
\end{matrix}\right], \\
\mathbf{X}_{(2)}=\left[\begin{matrix}
1 & 2 & 3 & 13 & 14 & 15 \\
4 & 5 & 6 & 16 & 17 & 18 \\
7 & 8 & 9 & 19 & 20 & 21 \\
10 & 11 & 12 & 22 & 23 & 24
\end{matrix}\right], \\
\mathbf{X}_{(3)}=\left[\begin{matrix}
1 & 2 & 3 & 4 & 5 & \cdots & 9 & 10 & 11 & 12 \\
13 & 14 & 15 & 16 & 17 & \cdots & 21 & 22 & 23 & 24
\end{matrix}\right]
\end{gathered}
$$