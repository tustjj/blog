---
title: 相似报告发现
date: '2021-12-02'
tags: ['算法总结']
draft: true
summary: 比对当前报告与历史报告的多种特征，快速检索历史报告，帮助管理员了解其历史中的分布情况及特征，结合历史报告的发生情况及处置经验快速得到初步排查思路。
---

# 报告相似性计算方法

先提取报告的关键字，然后用关键字集合之间的相似程度来计算报告之间的相似度

## 相似度计算，取值范围：0 ~ 1

报告A，报告B

3. similarity = similarityScore - dissimilarityScore
4. weightScores = similarity * weight(featureSize)
6. max(weightScore) * maxScoreRate + sum(weightScores) / weightScores.size

## 相似度计算

关键字集合：Set

1. commonSet = ASet & BSet  
2. diffSet = ASet - BSet

关键字集合重合度越高，则相似度越高，相似度取值范围为 0 ~ 1
    similarityScore = jaccard(ASet, BSet)
    
### Jaccard index、并交比、Jaccard similarity coefficient

度量有限样本集合的相似度，其定义为两个集合交集大小与并集大小的比例。如果A和B完全重合，就有J(A,B)=1

更多：Jaccard Distance，用于度量样本集之间的不相似度，其定义为1 - J(A,B)
    
## 不相似度计算
    
告警数量：alertCount
    
A告警数量比B告警数量越多，不相似度越高，不相似度取值范围为 0 ~ 0.25
    dissimilarityScore = Math.min(Math.abs(AAlertCount - BAlertCount) / BAlertCount, 1) * 0.25
   
## 分数权重计算，weight

当前特征约多，则权重越高，取值范围为 0.5 ~ 1

featureSizes = [1, 1, 2, 2, 0, 3, 1]
minSize = 1
maxSize = 3

如果 (maxSize - minSize) <= 1 则权重为1
否则 log(featureSize) / log(maxSize * maxSize) + 0.5，输出范围为 0 ~ 1
注：log(n) / log(n * n) = 0.5，这就意味着最大长度的特征的权重为1，其他权重依次递减，最低为0.5

## 规律性

仅相似度大于0.5的，才认为是相似报告，才会去计算出现的规律

### 周期性

搜索范围内，以故障时间为基准，按照周期性间隔往前推7个时间，如果大于周期性阈值，则认为具有周期性。

### 频繁性

搜索范围内，相似报告的个数大于阈值，则认为具有频繁性。

### 罕见性

查询时间单位内，没有相似报告，则认为是罕见的。

## 算法参数

1. 查询时间范围：7天
2. 相似度阈值：0.75

4. 周期性搜索范围：7天
5. 周期性阈值：5天
3. 周期性间隔：1小时，4小时，1天

6. 频繁性搜索范围：2小时
7. 频繁性阈值：5次

8. 告警数量影响因子：0.1
9. 最大分数占比：0.5