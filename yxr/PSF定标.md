---
title: PSF定标
description: 
published: true
date: 2023-12-25T09:18:57.827Z
tags: 
editor: markdown
dateCreated: 2023-12-25T09:07:59.815Z
---

# PSF定标

## 1.Camera Intrinsic Blur Kernel Estimation: A Reliable Framework

这篇论文介绍了一个空变PSF定标的过程。

用相机拍摄高分辨率的电脑屏幕。

电脑屏幕有四种显示模式，分别是合成棋盘格、伯努利模式分布、黑屏、白屏。

流程大致是：

1. 拍摄合成棋盘格图像；
2. 通过角点检测将屏幕分成若干个棋盘格；
3. 切换显示伯努利随机图片，识别棋盘格区域；
4. 通过扭曲变换将目标变换为矩形；
5. 通过双立方插值提高探测图像锐度；
6. 根据清晰图像和拍摄的模糊图像和伯努利分布的均匀谱分布特性计算模糊核k'；
7. 考虑到噪声影响，通过优化目标函数得到最终的模糊核估计。