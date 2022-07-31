---
layout: page
title: 技术支持 
---

欢迎同大家一起交流 

## Pytorch深度学习环境搭建

一般常见的是**Anaconda/miniconda+Pytorch**+ (Pycharm) 的工具，我们的安装分为以下几步

1. Anaconda的安装，创建虚拟环境。 [参考该文章]([Anaconda超详细安装教程（Windows环境下）_菜鸟1号！！的博客-CSDN博客_windows安装anaconda](https://blog.csdn.net/fan18317517352/article/details/123035625))

2. 检查有无NVIDIA GPU

   - 在`cmd/terminal中`输入`nvidia-smi`（Linux和Win命令一样）、使用NVIDIA控制面板或者使用任务管理器查看自己是否有NVIDIA的独立显卡及其型号）
   - 看下版本号，看自己可以兼容的CUDA版本，等会安装Pytorch时是可以向下兼容的（本人11.6）![shipei](C:\use\E\桌面\annn\leopardpan.github.io-master\images\support\01.png)

3. PyTorch的安装

   - 登录官网[Pytorch官网](https://pytorch.org/)，点击Install按钮，进入相关界面![image-20220730092126708](C:\use\E\桌面\annn\leopardpan.github.io-master\images\support\02.png )

   - 复制 ` run this command `,在Anaconda虚拟环境中输入指令

   - 检验是否安装成功

     进入所在的**虚拟环境**，紧接着输入`python`，在输入下面的代码。

     ```
     import torch
     
     torch.cuda.is_available()
     ```

     这条命令意思是检验是否可以调用cuda，如果**安装的是CPU的小伙伴们会返回False，GPU的小伙伴会返回true**。一般这个命令不报错的话就证明安装成功。

4. Pycharm的安装 ( Windows系统上更为常用）
