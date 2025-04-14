---
theme: seriph
background: https://cover.sli.dev
title: Diffusion Model
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true

---

对一个人说：“想象一只狗在奔跑的场景。”他立马可以想出各种各样的与之对应的图片。但是在几年之前，对于计算机来说，这仍是一个很难完成的任务。不过，随着近几年计算机视觉领域的飞速发展，各种文本到图像生成模型不断涌现，并且表现出惊人的性能。其中一个很火的概念就是扩散模型(diffusion model)。

---

其核心思想源于物理学中的扩散过程。模型通过模拟“噪声逐步破坏数据”的正向过程(Forward Process)和“从噪声中重建数据”的反向过程(Reverse Process)来学习数据分布。在正向阶段，原始图像被逐步添加高斯噪声，直至转化为纯随机噪声；反向阶段则通过训练神经网络（如U-Net）逐步预测并去除噪声，最终生成高质量数据。这个思想其实与过去的遗传算法与进化算法有相似之处。本次汇报将着重介绍这个部分。