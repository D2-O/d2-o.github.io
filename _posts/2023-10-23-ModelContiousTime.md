---
layout:     post
title:      How to Model Continuous Time
subtitle:   literature review
date:       2023-10-23
author:     D2O
catalog: true
tags:
    - 论文
    - 宏观经济
---

## DEFINITION
1. Elasticity of Intertemporal substitution (Intertemporal elasticity of substitution) 
    - measure of responsiveness of the **growth rate of consumption** to the **real interest rate**
    
$$
Qu'(c_t)=Q\beta Ru'(c_{t+1})
$$
$$
R=\frac{u'(c_t)}{\beta u'(c_{t+1})}
$$
$$
ln(R)=ln(1+r)=-ln[\frac{u'(c_{t+1})}{u'(c_t)}]-ln\beta
$$
$$
r \approx -ln[\frac{u'(c_{t+1})}{u'(c_t)}]-ln\beta
$$
$$
EIS \equiv \frac{dln(c_{t+1}/c_t)}{dr}=\frac{dln(c_{t+1}/c_t)}{dln(u'(c_{t+1})/u'(c_t))}
$$

2. Relative Risk Aversion
    - percentage of consumption in risky assets for a given consumption
$$
RRA=-\frac{d(u'(c_t))/u'(c_t)}{d(c_t)/c_t}=-u''(c_t)\frac{c_t}{u'(c_t)}
$$

3. Absolute Risk Aversion
    - actual dollar amount an individual will consume in risky assets, given a certain consumption.

$$
ARA=-\frac{u''(c)}{u'(c)}
$$
    




## Lifetime utility 
$$
U=\int_0^T e^{-\rho t}u(c_t)dt
$$
$$
EIS=-\frac{\partial{(\dot{c}/c})}{\partial{(\dot{u}'(c_t)/u'(c_t)})}=-\frac{\partial{(\dot{c}/c})}{\partial{(u''(c_t)\dot{c}/u'(c_t)})}=\frac{\partial{(\dot{c}/c})}{\partial{RRA(\dot{c}/c)}}=\frac{1}{RRA}
$$
