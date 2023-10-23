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

在动态模型中，宏观政策要完成两项基本任务：确定价格水平和稳定债务。主动的货币政策与被动的财政政策可实现通常所谓的新凯恩斯模式，即货币政策盯住通胀，财政政策此时会展现出"Ricardian Equivalence"。主动的财政政策与被动的货币政策会导致通货膨胀源于财政政策，因为货币政策疲于应付债务稳定问题。

在熨平经济周期的过程中，看似货币政策与财政政策并没有产生实际交互作用，但是实际上，在货币政策为主导的背景下，货币政策冲击导致价格水平变化，从而影响当期经济主体的财富水平，在基本盈余不变的情况下，根据政府预算，即使利率不变的情况下，未来政府实际债券价值降低，导致总需求下降，总需求的下降将抵消货币政策带来的通胀影响。另一方面，如果政府调整债务政策，并超过实际利率时，预算盈余的调整额等于家庭初始债务存量的调整额，这将抵消财富效应，造成货币政策扩张。货币政策影响家庭财富的第二条路径为较低的价格，提高了债券到期的预期利息收益。

## A General Maturity Structure

Government's flow budget identity:
$$
\frac{1}{R_t}\frac{B_t}{P_t}+s_t=\frac{B_{t-1}}{P_t}
$$

*LHS为当期政府能拿到的全部资源，RHS为政府需要偿还的全部资源*

- 加入期限结构

$B_t(t+j)$表示$t$期未偿还，$t+j$期到期的零息债券的名义数量，在constant-endowment economy中以美元计价表示为$Q_t(t+j)$，政府$t$期的预算为
$$
B_{t-1}(t)-\sum_{j=1}^{\infty}Q_t(t+j)[B_t(t+j)-B_{t-1}(t+j)]=P_ts_t
$$
In a constant-endowment economy, the bond-pricing equations are
$$
Q_t(t+k)=\beta^kE_t \frac{P_t}{P_{t+k}}
$$
Rewrite
$$
Q_t(t+k)=E_t[Q_t(t+1)Q_{t+1}(t+2)...Q_{t+k-1}(t+k)]
$$
Define the portfolio of bonds outstanding at the end of period $t-1$
$$
B_{t-1} \equiv B_{t-1}(t)+\sum_{j=1}^{\infty}Q_t(t+j)B_{t-1}(t+j)
$$
Government budget identity as
$$
\frac{B_{t-1}}{P_t}=Q_t(t+1)\frac{B_t}{P_t}+s_t
$$



$t-1$期末未偿债组合

$$
B_{t-1} \equiv B_{t-1}(t)+\sum_{j=1}^{\infty}Q_t(t+j)B_{t-1}(t+j)
$$

$t$期政府预算可重写为

$$
\frac{B_{t-1}}{P_t}=Q_t(t+1)\frac{B_t}{P_t}+s_t
$$

- **Fisher relation**

$$
\frac{1}{R_t}=\beta E_t\frac{P_t}{P_{t+1}}=\beta E_t\frac{1}{\pi_{t+1}}
$$
其中$R_t$为短期名义利率，$\pi_t$为总通胀率

- **Taylor Rule**: 使名义利率偏离稳态的程度与通货膨胀率偏离稳态的程度成比例
$$
\frac{1}{R_t}=\frac{1}{R^*}+\alpha_{\pi}(\frac{1}{\pi}-\frac{1}{\pi^*})-\epsilon^M_t
$$

$\epsilon_t^M$是货币政策的外生冲击

The elasticity of intertemporal substitution is defined as the percent change in consumption growth per percent increase in the net interest

## New Keynesian Model

- a representative consumer and firm
- monopolistic competition in final good
- calvo(1983) sticky price in which a fraction $1-\phi$ of goods suppliers sets a new price each period
- a cashless economy with one-period nominal bonds $B_t$, that sell at price $1/R_t$
    - $R_t$ is the monetaru policy instrument
- an exogenous primary government surplus $s_t$ with lump-sum taxes
- shocks only to monetary and fiscal policy
    - shocks have no effects on the natural rate of output, there is no difference between deviations in output from steady state and the output gap.
- **log-linearized around the deterministic steady state with zero inflation**

$\hat{x_t} \equiv ln_(x_t)-ln(x^*)$ denote log deviations of a variable from its steady-state value.

- private-sector behavior reduces to a **consumption-Eular** equation
$$
\hat{\gamma_t}=E_t\hat{\gamma_{t+1}}-\sigma(\hat R_t-E_t\hat{\pi_{t+1}})
$$
- Phillips Curve
$$
\hat{\pi_t}=\beta E_t \hat{\pi_{t+1}}+\kappa \hat{\gamma_t}
$$