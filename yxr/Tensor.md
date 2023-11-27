---
title: Tensor
description: 
published: true
date: 2023-11-27T11:04:38.065Z
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
\end{matrix}\right].
\end{gathered}
$$

## 张量积
### Kronecker积

矩阵的Kronecker积是一种矩阵运算，也被称为矩阵的张量积。给定两个矩阵A和B，它们的Kronecker积$A \otimes B$是一个大矩阵，若$A \in \mathbb{R}^{m\times n}$和$B \in \mathbb{R}^{p\times q}$,则A与B的Kronecker积是一个大小为$mp \times nq$的矩阵，其表述为：

$$
A=\left[\begin{matrix}
a_{1,1} & \ldots & a_{1, n} \\
\cdots & \ddots & \cdots \\
a_{m, 1} & \ldots & a_{m, n}
\end{matrix}\right]_{m \times n} B=\left[\begin{matrix}
b_{1,1} & \ldots & b_{1, q} \\
\cdots & \ddots & \cdots \\
b_{p, 1} & \ldots & b_{p, q}
\end{matrix}\right]_{p \times q}
$$

$$
A \otimes B=\left[\begin{matrix}
a_{1,1} B & \ldots & a_{1, n} B \\
\cdots & \ddots & \cdots \\
a_{m, 1} B & \ldots & a_{m, n} B
\end{matrix}\right]_{m p \times n q}
$$
