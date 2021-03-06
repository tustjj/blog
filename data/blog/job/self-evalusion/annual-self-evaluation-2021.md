---
title: 年终总结-2021
date: '2022-02-08'
lastmod: '2022-02-08'
tags: ['年终总结']
draft: true
summary: 年终总结-2021
---

# 员工自评

1. 本年度做过的最重大(花费功夫最多或最有挑战)的事情，大致说明工作内容以及成果

1.1【调用链分析】
    1.1.1 工作内容: 从 Scala 翻译成 Java、benchmark 测试、参与产品设计、Web接口开发，降级方案实现，建行上线，算法优化，Bug fix，效果调优，代码重构，标准版实现。
    1.1.2 成果: 算法最早上线测试，过程中不断迭代产品展现形式和效果，最早运行稳定，能够解决实际问题出效果，被组内作为优秀案例展示。
    1.1.3 总结:【调用链分析】属于花费功夫最多的一项工作。算法初期测试效果不太理想（技术实现简单，测试案例不足，展现形式粗糙），接手工作后，先将算法工程化，但上线时遇到了各类问题（源数据接入，数据格式，算法入参，输出报告内容，展示效果）无法达到预期效果。
    后期花费了大量精力做源数据接入，算法优化，降级方案，效果调优，完善产品展现效果，最终做到前因后果都能解释清楚，调用链图清晰易懂，形成一个完整好用可靠的算法产品。
    可以总结一下：这些花费功夫最多的工作的90%本可以在预研的时候用10%的时间快速解决掉，但实际上却在客户生产环境上花费了几倍的时间去逐个解决，既浪费了研发资源，客户也感受不好，在后续预研工作中应当汲取这些宝贵经验，用心做好一个产品后再去上线。

1.2【故障特征】
    1.2.1 工作内容: 一期方案设计，测试代码设计，二期方案展望。
    1.2.2 成果: 梳理算法的实际背景和价值输出，整理出一批故障特征及概要介绍，测试代码覆盖全部代码分支，孵化出更复杂的故障特征放在二期去做。
    1.2.3 总结:【故障特征】属于比较有挑战的一项工作。接手工作后，算法标签候选集比较少，也比较零散，很难理解算法功能的定位和价值。通过收集和理解优秀案例，逐步梳理出了产品的背景信息，
    以及期望产生的价值，然后整理现有的优秀算法报告和各部分信息，能够梳理出第一期的故障特征以及概要介绍，然后复盘优秀案例，结合算法输出的算法标签，确认能够起到提纲挈领的作用。
    结合之前的宝贵经验，我们组要求测试代码需要覆盖全部代码分支，并在dev环境迭代测试验证，充分保证了算法的可靠性和有效性。与此同时，二期等更复杂的故障特征也不断涌现出来，如此循环迭代就能够快速打磨出一个优秀的产品功能。

1.3【Anomaly】
    1.3.1 工作内容: 发数器实现，券商版适配，工程化开发，算法优化，代码重构。
    1.3.2 成果: 各流程环节自检，兼容各版本的代码实现，benchmark覆盖各类算法参数和测试数据，默认参数模板、模型训练、个性化参数选择、应用算法参数，一条龙流程都集成到算法沙箱中了。
    1.3.3 总结:【Anomaly】属于去年花费功夫最多，今年也比较有挑战的一项工作。因为Anomaly是公司的拳头产品，代码量体量大，逻辑复杂，很容易产生牵一发动全身的影响，为了达到Anomaly的高并发、高可靠、易上手的效果，我们组做了非常大的努力，也取得了非常好的结果。
    虽然还没有在客户现场大规模使用起来，但大家对它还是非常信心的。

2. 本年度对公司价值最大或者最能体现个人素质的事情(如果与第一条重复，可额外写 3 条， 注意这一项工作量不一定是很大的那种)

    2.1 【追求卓越】在必示近一年半的工作时间中，不断挑战自己，提升自我，敢担当，可依赖，努力提高编程水平，努力成为领域专家，努力交付真正有价值的算法产品功能。
    2.2 【团队管理】与小组成员沟通工作中遇到的困难和期望的收获，以交付产品价值为工作核心，设立有挑战性的工作目标，给与充分的发挥空间，帮助他们解决关键问题，引导他们快速成长。 
    2.3 【坚持学习】工作中查漏补缺，不断学习，把工作做的更好。参加了学堂在线的《疾风计划》计算机课程，目前已学完的7/12门，并取得优秀证书。
        读完了多本技术书，包括:《机器学习理论导引》。《最优化导论》、《智能运维 从0搭建大规模分布式AIOps系统》、《深入理解Java虚拟机》、《Redis深度历险》、《设计模式之禅》、《编程珠玑》、《代码整洁之道》。

3. 时间线
    2021.01-2021.02: 【Farseer】从 Scala 翻译成 Java，完成 benchmark 测试，合并到 hubble 项目中。
    2021.02-2021.03: 【Anomaly】代码重构，算法优化，需求实现。具体包括：提供默认算法参数模板，参考局部数据修正基带方法优化，重新训练策略优化。
    2021.03-2021.04: 【ES 数据清理任务】需求实现，【Anomaly】需求实现，具体包括：定时更新全局参数（全局节假日+调休日）【广发】现场部署和需求沟通。
    2021.04-2021.05: 【Anomaly】适配券商版，完成 benchmark 测试。
    2021.05-2021.06: 【发数器】需求实现，配合完成 Anomaly 各流程环节自检。
    2021.06-2021.07: 【设计模式】组内分享，【Anomaly】代码重构。
    2021.07-2021.08: 【调用链分析】从 Scala 翻译成 Java，完成 benchmark 测试，参与产品设计，Web接口开发，合并到 hubble 项目中，【业务影响分析】需求实现。
    2021.08-2021.09: 【调用链分析】【业务影响分析】建行生产环境上线，Bug fix，调试效果【多维分析】适配金科接口，Bug fix。
    2021.09-2021.10: 【调用链分析】算法优化，效果调优，异常判断逻辑优化，完善展示信息，代码重构【业务影响分析】算法优化，Bug fix。
    2021.10-2021.11: 【调用链分析】降级方案，需求讨论，需求实现，效果调优【业务影响分析】新需求实现，调试效果。
    2021.11-2021.12: 【问题交易分析】需求实现，Web接口开发，效果调优，代码重构，Bug fix，建行生产环境上线。
    2021.12-2022.01: 【调用链分析】【业务影响分析】【问题交易分析】标准版实现，【故障特征】解决方案设计。

4. 对自己的整体评价

今年刚好30周岁，去年12月刚结完婚，如今的自己褪去些许浮躁，有了更多责任和担当。工作中也是一样，追求效果和效率的同时，也要求架构清晰，代码整洁，面对不断迭代更新的需求能够快速修改测试，保质保量交付产品功能，努力让所有人都能轻松阅读并理解修改测试代码。
之前对智能运维的理解比较浅薄，参与了多个算法项目之后，开始对自己经手的算法项目有了更多的价值要求，不再满足于基本的功能需求研发，而是希望自己和团队能够为公司输出一些价值，努力做好产品功能并交付价值，毕竟客户能用起来的产品才是一个好产品，也希望自己能够为智能运维尽一点微薄之力。
今年团队调整之后感觉自己更加有冲劲儿了，不仅可以做算法工程化的工作，还参与到核心算法研发当中，团队整体氛围积极向上，促使自己不断追求卓越，实现人生价值。

5. 自评评分解释

每一分都丢在了哪里，3: 核心算法研发贡献不够，希望未来能够多做贡献。3: 核心业务理解不够深刻，需要持续加强与前场的沟通，站在业务的实用角度贡献自己的能力。1: 团队管理能力需要再锻炼，目前带梦家和则言，希望未来能够持续学习并提升管理能力。
