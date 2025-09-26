---
layout: post
title: "ReDo in RL: notes"
date: 2025-09-26 12:00:00 +0400
categories: [research, rl]
tags: [iqm, replay]
excerpt: "Quick notes and figures about dormant neurons and reinitialization."
---


Вступление… Формулы рендерятся как `$E=mc^2$` или блочно:


$$
\mathcal{L}(\pi,\lambda)=\mathbb{E}_\pi\Big[\sum_t \gamma^t (r_t-\sum_j \lambda_j(g_{j,t}-c_j))\Big].
$$


Код:


```python
import numpy as np
print("hello RL")
```