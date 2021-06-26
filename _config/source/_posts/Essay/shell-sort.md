---
title: 希尔排序
date: 2018-10-25 14:42:29
tags: Data Structure
---

# 希尔排序（文末附有C语言实现方法） #
写出这个主要是平常练习中经常出现希尔排序的题目，这次考试中，又出现了两次（一道选择题，一道算法题），题目我只记得要求，就是进行希尔排序时，选择不同的增量，第一趟排序的结果的怎样。看到这个，我真的是一脸懵逼，只能回来，再一次看一下书，好好复习一下，下次问到就根据这些印象，可能这些问题就可以迎刃而解了。
首先看一下，官方的表达
希尔排序的思想：先取定一个小于n的整数d1作为第一个增量，把数组R中的全部元素分成d1个组，所有下标距离为d1的倍数的元素放在同一组中，即R[1],R[1+d1],R[1+2d1],...为第一组，R[2],R[2+d1],R[2+2d1],...为第二组,...,接着在各组内进行直接插入排序；然后再取d2(d2<d1)为第二个增量，重复上述分组和排序，直到所取得增量 dt = 1(dt<dt-1<...<d2<d1),把所有得元素放再同一组中进行直接插入排序为止。

案例分析



这里我贴出C语言的代码
```C
void ShellInsert(SeqList R,int dk,int n)
{
  int i,j;
  for(i = dl + 1;i<=n;i++)
    if(R[i].key < R[i-dk].key)
    {
      R[0] = R[i];
      j = i-dk;
      while(j>0 && R[0].key < R[j].key)
      {
        R[j + dk] = R[j];
        j = j - dk;
      }
      R[j + dk] = R[0];
    }
}
void ShellSort(SeqList R,int d[],int t,int n)
{
  int k;
  for(k = 0;k<t;k++)
    ShellInsert(R,d[k],n);
}
```