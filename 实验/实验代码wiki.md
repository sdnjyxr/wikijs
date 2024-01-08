---
title: 240105实验
description: 
published: true
date: 2024-01-08T11:55:10.551Z
tags: 
editor: markdown
dateCreated: 2024-01-05T07:29:52.774Z
---

# 240105实验

## 1.棋盘格显示

> 在chessboard.py程序中设置
{.is-info}


| 变量名 | 变量含义 | 变量名 | 变量含义 |
|:-:|:-:|:-:|:-:|
|**dpi**|显示器DPI，匹配像素大小|**chess_size_cm**|棋盘格大小|
|**square_size_cm**|伯努利分布格大小|**display_mode**|（1）棋盘格<br>（2）伯努利分布<br>（3）黑屏<br>（4）白屏|

## 2.成像实验

### 2.1 上中下三个通道的成像结果

<center>
<img src='/240105/1-1.jpg' width=50%>
</center>
  
> 不能完美合像，原因如下：
>	1.边缘通道和中间通道的模糊程度不同
> 2.大透镜中心和后续系统不共轴
> 3.笼式系统不平
> 4.CCD靶面倾斜
{.is-warning}

### 2.2 单通道成像结果

<center>
<img src='/240105/1-2.jpg' width=30%><img src='/240105/1-4.jpg' width=30%><img src='/240105/1-3.jpg' width=30%>
  <br>
  <tz> （左）上通道成像结果（中）中通道成像结果（右）下通道成像结果 </tz>
</center>

> 上下通道成像模糊不一致，中通道遮光不干净。
{.is-warning}

## 3.PSF定标实验

### 3.1 边缘通道棋盘格图像

<img src='/240105/2-1.jpg' width=50%>
