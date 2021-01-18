---
title: "HTTP协议"
date: 2021-01-18T16:25:17+08:00
lastmod: 2021-01-19T19:01:05+08:00
draft: false
tags: ["HTTP"]
categories: ["技术"]

weight: 10
contentCopyright: MIT
mathjax: true
autoCollapseToc: true

---

## TCP/IP协议分层

- 应用层
- 传输层
- 网络层
- 数据链路层



> 如果某些地方需要改动，只需要把变动的层修改逻辑。各层对外接口部分规划好，内部设计就比较灵活了。分层好处之一。



### 应用层

应用层决定了向用户提供应用服务时通信的活动。TCP/IP 协议族内预存了各类通用的应用服务。比如，FTP（File Transfer Protocol，文件传输协议）和 DNS（Domain Name System，域 名系统）服务就是其中两类。 HTTP 协议也处于该层。、

### 传输层

传输层对上层应用层，提供处于网络连接中的两台计算机之间的数据传输。__TCP__（Transmission Control Protocol，传输控制协议）和 __UDP__（User Data Protocol，用户数据报 协议）。

### 网络层

网络层用来处理在网络上流动的数据包。数据包是网络传输的最小数据单位。与对方计算机之间通过多台计算机或网络设备进行传输时，网络层所起的作用就是在众多的选项内选择一条传输路线。

### 链路层

处理连接网络的硬件部分（网卡，光纤）。