---
layout:     post
title:      How to Model Bonds
subtitle:   literature review
date:       2023-10-16
author:     D2O
catalog: true
tags:
    - 论文
    - 宏观经济
---
# Nominal vs Real Bonds
[Leeper(2016)](https://ideas.repec.org/p/gla/glaewp/2016_01.html)写道:
> Central to the fiscal theory is the distinction between real and nominal government debt.

- Real Debt可以是与通货膨胀挂钩的债券，是对实际商品的债券，政府必须通过征税获得这些商品，这就形成了预算约束。如果政府没有足够的税收能力来获得未偿债务融资所需的商品，最终只能违约。
- Nominal Debt很像政府发行的货币：只是对未来新货币的一种要求。政府可以选择增加税收来获取所需的货币，也可以选择印制新货币。由于名义债务取决于价格水平和债券价格，实际上政府并不面临预算约束
- 欧洲货币联盟成员发行以欧元计价的债务，但由于货币政策由欧洲央行而非各国控制，所以站在成员国的角度，这些债务实际上是真实的。

在动态模型中，宏观政策要完成两项基本任务：确定价格水平和稳定债务。

## A General Maturity Structure

$B_t(t+j)$表示$t$期未偿还，$t+j$期到期的零息债券的名义数量，则以美元计价表示为$Q_t(t+j)$，政府$t$期的预算为
$$
B_{t-1}(t)-\sum_{j=1}^{\infty}Q_t(t+j)[B_t(t+j)-B_{t-1}(t+j)]=P_ts_t
$$
美元计价为
$$
Q_t(t+k)=\beta^kE_t \frac{P_t}{P_{t+k}}
$$