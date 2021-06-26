---
title: 动态规划（背包问题）
date: 2019-01-16 10:46:54
tags: Data Structure
---
# 两招掌握最基本的解题思路 #
动态规划的相关算法基本问题，老师讲了两个主要大块：动态规划算法求解10背包和最长公共子序列过程图解问题
背包问题，我在最近的程序员面试推文中，阅读过一名前端的程序员面试过程中遇到面试官问的背包问题，他没有解出来，只是说了过程。
摘取推文内容如下：
Q5 我现在有一个背包，容量为m，然后有n个货物，重量分别为w1,w2,w3...wn，每个货物的价值是v1,v2,v3...vn，w和v没有任何关系，请求背包能装下的最大价值。
这个我也没写出来，也给了个思路，首先使用Q4的方法得到货物重量数组的全组合（包括拆分成小数组的全组合），然后计算每一个组合的价值，并进行排序，然后遍历数组，找到价值较高切刚好能装进背包m的组合。
[作者：_杨溜溜][来自：https://segmentfault.com/a/1190000017049146]

好了，下面说我在学校听课收获的内容和总结。
## 一、动态规划算法求解10背包 ##

## 二、最长公共子序列过程图解 ##