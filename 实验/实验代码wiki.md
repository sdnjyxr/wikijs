---
title: 240105实验
description: 
published: true
date: 2024-01-08T13:18:36.111Z
tags: 
editor: markdown
dateCreated: 2024-01-05T07:29:52.774Z
---

# 240105实验

## 总览

<center><img src='/240105/总览.jpg' width=60%>   <img src='/240105/目标位置.jpg' width=16.5%></center>

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
	<div class='tz'>（左）上通道成像结果（中）中通道成像结果（右）下通道成像结果</div>
</center>
<br>

> 上下通道成像模糊不一致，中通道遮光不干净。
{.is-warning}

## 3.PSF定标实验

### 3.1 边缘通道棋盘格图像

<center><img src='/240105/2-1.jpg' width=50%></center>

> 可见边缘通道的像差严重到无法识别角点了，这个问题有可能是目标距离太近了：目标近，前置大透镜的入射光线角度就大，大透镜因为它口径大，引入的像差就很大，入射光线角度再大，像差就更难说了。
{.is-warning}

> 再实验时，目标还是按照仿真的条件，放到1500mm的位置。
{.is-info}

### 3.2 中间通道PSF定标尝试

<center>
  <img src='/240105/2-2.jpg' width=40%>
  <br>
  <div class='tz'>中间通道的棋盘格图像</div>
</center>
<br>

<center>
  <img src='/240105/2-3.jpg' width=40%> <img src='/240105/2-4.jpg' width=40%>
  <br>
  <div class='tz'>（左）10倍密集的噪声 （右）15倍密集的噪声</div>
</center>
<br>

<center>
  <img src='/240105/2-5.jpg' width=40%> <img src='/240105/2-6.jpg' width=40%>
  <br>
  <div class='tz'>（左）黑屏 （右）白屏</div>
</center>
<br>
