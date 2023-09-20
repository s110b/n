---
title: github aciton 简单使用
date: 2022-09-20 21:00:30
categories:
- tech/tech
tags:
---

## 是什么？
这玩意准备了几个环境，你可以在这个环境上编译，提交，部署代码。
对简中的好处就是，github的环境天然就是墙外的，解决各种依赖不费力

## 如何用？
官方提供了很多样例，什么都不了解也可以拿来就用，但是出现问题可能就会卡住。
所以还需要简单了解些语法，比如目录位置，日志打印。每一步都做什么。

## 下面是初学者常见的问题。

1. 目录问题， 权限问题 。

## 有趣玩法

###  同步到其他的网站部署
有很多免费提供静态网站部署的大站。

比如：

* render       https://vip-20y5.onrender.com/
* cloudflare   https://vip-coi.pages.dev/
* vercel       https://vip-puce.vercel.app/
* netlify      https://aesthetic-sprite-d13736.netlify.app/

利用action可以实现，在编译后同步部署到这些网站。这些静态网站有些提供cdn，访问可能会快点。
参考示例：s110b/vip中的workflow action


### 源码和编译在不同分支存储。

jekyll 默认的部署工具看不到编译后的代码，这样其实也无所谓，但是如果你想看到这些编译后的代码，
action中提供一些提交组件可以把编译后的代码提交到另一个分支上。参考示例："s110b/n" workflow action。

###  利用现有docker编译

action还有一个功能，就是利用docker编译项目，有些项目依赖的东西较多，自己搭建环境很烦，直接利用
docker 镜像去编译，节省时间。参考： "s110b/n" workflow action 

