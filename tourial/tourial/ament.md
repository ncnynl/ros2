# 简介
这篇文章会简要介绍如何快速配置和使用一个ament工作空间。
这是一个比较实际的操作教程，并不是为了替换核心文档而写。

## 背景

Ament是catkin编译工具的优化迭代版本。
关于Ament的设计上的信息可以看[这个文档](http://design.ros2.org/articles/ament.html)

ament的源代码可以在[这里](https://github.com/ament)找到

## 开发环境

确保你已经按照之前从源代码编译文档的要求配置好你的开发环境。

## 基础知识

一个Ament工作空间，是一个有着特定目录结构的文件夹。
通常会有一个src子文件夹。
在这个子文件夹下是各个软件包的源代码。
通常这个文件夹初始情况下是空的。

Ament脱离源代码进行编译。
默认情况下它会在src文件夹旁创建一个build和一个install文件夹。
build文件夹会用来存放编译过程中产生的中间文件。
对于每个软件包都会创建一个对应的文件夹，然后cmake在对应的文件夹下运行。
install文件夹是软件包的安装位置

注意:和catkin相比这里没有devel文件夹

## 创建目录结构

下面在 ~/ros2_ws 下创建一个基本的工作空间目录结构

```bash
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws
```

下面就是你所预想的目录结构
```
.
└── src

1 目录, 0 文件
```

## 添加一些源代码