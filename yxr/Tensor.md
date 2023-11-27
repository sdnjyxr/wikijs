---
title: Tensor
description: 
published: true
date: 2023-11-27T11:43:09.150Z
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

张量$\mathcal{X} \in \mathbb{R}^{3\times 4\times 2}$:

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
\vdots & \ddots & \vdots \\
a_{m, 1} & \ldots & a_{m, n}
\end{matrix}\right]_{m \times n} B=\left[\begin{matrix}
b_{1,1} & \ldots & b_{1, q} \\
\vdots & \ddots & \vdots \\
b_{p, 1} & \ldots & b_{p, q}
\end{matrix}\right]_{p \times q}
$$

$$
A \otimes B=\left[\begin{matrix}
a_{1,1} B & \ldots & a_{1, n} B \\
\vdots & \ddots & \vdots \\
a_{m, 1} B & \ldots & a_{m, n} B
\end{matrix}\right]_{m p \times n q}
$$

#### Kronecker积性质
1. Kronecker积满足线性叠加
给定$\alpha \in \mathbb{R}$：
$$
A \otimes(\alpha B)=\alpha(A \otimes B) \\
(\alpha A) \otimes B=\alpha(A \otimes B)
$$

2. Kronecker积满足加法的分配律: 
$$
(A+B) \otimes C=(A \otimes C)+(B \otimes C)
$$

3. Kronecker积是满足结合律: 
$$
(A \otimes B) \otimes C=A \otimes(B \otimes C)
$$

4. 一般情况下，Kronecker积不满足交换律: 
$$
A \otimes B \neq B \otimes A
$$

5. 转置运算在Kronecker积中满足分配律，但不满足倒序律: 
$$
(A \otimes B)^T=A^T \otimes B^T
$$

6. 当矩阵的维度适合相乘时，可以使用矩阵乘法:
$$
(A \otimes B)(C \otimes D)=A C \otimes B D
$$

7. 当A和B是方阵且满秩时，可以使用矩阵乘法进行乘法运算:
$$
(A \otimes B)^{-1}=A^{-1} \otimes B^{-1}
$$

> 如果A是一个n×n的方阵，B也是一个n×n的方阵，并且它们都是满秩的，那么它们的乘积AB也是一个n×n的方阵，可以用矩阵乘法计算。这种情况下，矩阵乘法的性质包括结合律、分配律和对换律。
{.is-info}

8. Kronecker积的行列式等于其每个矩阵的行列式的乘积:
$$
\operatorname{det}\left(A_{n \times n} \otimes B_{m \times m}\right)=\operatorname{det}(A)^m \cdot \operatorname{det}(B)^n
$$

9. $\operatorname{trace}(A \otimes B)=\operatorname{trace}(A) \cdot \operatorname{trace}(B)$

### Khatri-Rao积

Khatri-Rao积是一种张量乘积的运算符，用于计算两个张量的列向量的外积。它由两个列向量矩阵（张量）的列向量的外积构成，其中第一列向量在两个矩阵中是相同的。Khatri-Rao积通常用符号$*$表示，形式化地定义为：
$$
A * B=\left(A_{i j} \otimes B_{i j}\right)_{i j}
$$
例如，如果$A$和$B$都是$2\times 2$的分块矩阵，例如：
$$
\mathbf{A}=\left[\begin{array}{l|l}
\mathbf{A}_{11} & \mathbf{A}_{12} \\
\hline \mathbf{A}_{21} & \mathbf{A}_{22}
\end{array}\right]=\left[\begin{array}{cc|c}
1 & 2 & 3 \\
4 & 5 & 6 \\
\hline 7 & 8 & 9
\end{array}\right], \quad \mathbf{B}=\left[\begin{array}{l|l}
\mathbf{B}_{11} & \mathbf{B}_{12} \\
\hline \mathbf{B}_{21} & \mathbf{B}_{22}
\end{array}\right]=\left[\begin{array}{c|cc}
1 & 4 & 7 \\
\hline 2 & 5 & 8 \\
3 & 6 & 9
\end{array}\right],
$$
可以得到：
$$
\mathbf{A} * \mathbf{B}=\left[\begin{array}{c|c}
\mathbf{A}_{11} \otimes \mathbf{B}_{11} & \mathbf{A}_{12} \otimes \mathbf{B}_{12} \\
\hline \mathbf{A}_{21} \otimes \mathbf{B}_{21} & \mathbf{A}_{22} \otimes \mathbf{B}_{22}
\end{array}\right]=\left[\begin{array}{cc|cc}
1 & 2 & 12 & 21 \\
4 & 5 & 24 & 42 \\
\hline 14 & 16 & 45 & 72 \\
21 & 24 & 54 & 81
\end{array}\right]
$$

#### Khatri-Rao积性质
1. $(\mathbf{A} \bullet \mathbf{B})(\mathbf{C} * \mathbf{D})=(\mathbf{A C}) \odot(\mathbf{B D})$, $\odot$为Hadamard积。

2.$(\mathbf{A} \odot \mathbf{B}) \bullet(\mathbf{C} \odot \mathbf{D})=(\mathbf{A} \bullet \mathbf{C}) \odot(\mathbf{B} \bullet \mathbf{D})$
