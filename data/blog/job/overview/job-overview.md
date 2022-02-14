---
title: 工作目标
date: '2021-12-02'
lastmod: '2022-01-04'
tags: ['工作目标', '工作计划']
draft: true
summary: 为人工智能行业的进步，为国际智能运维领域的突破，为公司价值的实现，也会自己成为一个更好更优秀的人！
---

## 大目标

为人工智能行业的进步，为国际智能运维领域的突破，为公司价值的实现，也会自己成为一个更好更优秀的人！

1. 深入理解智能运维领域，整理行业痛点，了解客户需求，明确产品部的价值输出
2. 深入探索人工智能行业，以无监督的机器学习算法为出发点，深入理解算法原理，应用场景
3. 熟练掌握算法工程化，把握问题定义，设计解决方案，高质量编码，开源项目
4. 反思自己哪些方面做的好，哪些做的不好，怎么改进

### 小目标

手头上的工作内容为第一要义，辅以客户需求，问题痛点，梳理得到工作价值。

#### 上周工作内容

1. 二期线索
   a. 问题交易分析：标准化开发（可配置交易表和明细表的字段名称，交易明细展示列表可灵活配置），增加业务失败判断逻辑（响应量/交易量 > 成功量），增加大于阈值判断和线索改造，完成光大测试。
   b. sketcher：适配响应时间数字型字符串的情况，完成光大测试。
   c. quoridor2.0：增加前端设计优化项 10+ 等待前端排期；解决独立节点展示问题；优化算法入参，发送线索，增加任务和算法执行描述。
   d. 故障标签：开会讨论故障标签算法的设计方案。
2. 案例收集
   a. 光大：问题交易分析测试案例，调用链测试案例
   b. 建行：收集了三个案例

#### 本周工作内容

故障标签：综合故障自身的内容和各算法分析报告，分析得到更丰富更有价值的标签信息，帮助运维人员快速发现故障级别的线索和特征和沙里淘金。

1. 梳理若干个 good case
2. 根据 good case 选取有价值的故障标签
3. 代码实现

#### 下周工作计划

1. 二期线索
   a. quoridor2.0：算法优化，光大测试。
   b. 故障标签：收集案例，设计解决方案，后端接口开发。
   c. 问题交易分析，sketcher，业务影响分析：等其他组更新完代码周三周四的时候在广发做测试。
1. 简单标签：

   1. 根因推荐（5 个标签：业务问题、性能问题、资源不足问题、中间件问题、数据库问题）
   2. 调用链根因定位（2 个标签：源头问题、非源头问题）

   3. 业务指标画像（3 个标签：流量突增，业务成功率已恢复，业务成功率未恢复）
   4. 告警摘要（3 个标签：主要告警总量突增、告警设备数突增、告警应用系统数突增）

   5. 业务影响分析（1 个标签：严重业务影响）
   6. 全局告警摘要（1 个标签：全局性影响）
   7. 相似疑似故障（5 个标签：非频繁问题、非周期性问题、罕见问题、频繁问题、周期性问题）

1. 复杂标签：

   1. 调用链——业务影响分析——问题交易分析——业务多维分析——三方能力（1 个标签：无充足分析数据）
   2. 业务指标画像——业务影响分析（1 个标签：发展型问题）

   3. 相似疑似故障——随着时间变化每个相似历史故障的告警指标越来越严重（1 个标签：预兆性问题）

6. 二期线索
   a. quoridor2.0：算法测试调优 bug 修复，前端优化，光大测试（算法执行没问题，后端查不出算法报告）。
   b. 故障标签：收集优秀案例，梳理疑似故障算法标签候选集，产品形态和价值讨论。
   c. sketcher：支持图节点展示字段可配置。
   下周计划:
7. 二期线索
   a. 故障标签：解决方案设计，产品设计，前后端开发。
   b. 问题交易分析，sketcher，业务影响分析，quoridor2.0：广发测试。

7+1，,6+1，,7+1

3. 挑战标签：
   1. 真实故障
   2. 可汇报
   3. 无需关注
   4. 需优化
   5. 待验证

## 重要节点

1. 2021-12-02，经过过去半年的努力，终于把调用链分析、业务影响分析、问题交易分析上线了，稳定输出算法效果。成果满满。^[[202112 算法总结](https:www.tustjj.top/blog/job/2021-12-algotithm-summary)]

2. 2021-12-31，调用链，业务影响分析，标准化开发完成，在光大完成上线

3. 2021-01-07，问题交易分析，标准化开发完成，在光大完成上线