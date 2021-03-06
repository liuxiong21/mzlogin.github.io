---
layout: post
title: 怎样阅读一个大型项目的源代码
categories: 编程
description: 怎样阅读一个大型项目的源代码如springframework
keywords: 阅读源代码, springframework
---

对于像springframework这种级别的项目，怎么样才能阅读得下去它的源代码呢？有什么突破点？

## 怎么寻找突破点

刚工作的时候也想过要阅读一些著名项目的源代码，多次尝试都被巨量的代码给吓退。正好最近一段时间一直在阅读一些开源项目的源代码，说下我自己的体会吧。

其实项目的代码量多并不可怕，只要掌握了方法其实并不难，我的阅读习惯一般是：

1. 首先从github上下载下来一个开源项目把开发环境准备好，保证在eclipse里面能把单元测试跑起来。
2. 当然在阅读代码之前需要知道这个项目能干嘛，然后基于自己的好奇心寻找下手点，如对于Spring，到底ClasspathXmlApplicationContext是怎么初始化的，怎么去解析占位符、Bean怎么实例化的等等。
3. 其实每个开源项目都有测试用例，像netty还有一个单独的maven module里面都是example，这就是下手点了，一个个单元测试或者use case跑起来，打断点调下去，当然你需要花点时间去粗略的看下相关类及源代码，最好能把class 的UML图给画出来。
4. 最后就是要坚持下来并多想这段代码为什么要这样。

## 为什么有的代码会看不下去

其实很简单，就是因为知识储备还不够，如果有了一定的知识储备在看代码过程中遇到不明白的地方，去网上查一下其实都是能搞明白的，越到后面阅读起来就越顺畅了。
