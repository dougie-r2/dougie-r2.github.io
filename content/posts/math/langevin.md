---
title: "Langevin"
date: 2025-06-18T02:03:00+00:00
draft: false
tags: 
  - "Langevin"
categories: 
  - "math"
math: true
toc: false
---

Diffusion model 에 대해 공부하다가 Langevin sampling이 정확히 무엇인지 궁금하여 이것 저것 찾아보고 LLM한테도 물어보고 있었다. 
Stationary distribution 이라고 몇 번 말하기에 나는 그게 무엇인지 물어보았고 시간이 지남에 따라 변화는 하지만 결국에는 변화하지 않고 평형을 이루는 상태로 수렴하는 것을 stationary라고 LLM이 설명하였다. 
문득 나는 이전에 선형대수학 공부했을 때 Markov matrix와 eigen vector가 생각이 났고 이것을 말하니 놀랍게도 2개가 서로 연관되어 있었다. 
다음은 내가 LLM과 대화한 내역이다.

[claude sonnet 대화내역](https://claude.ai/share/b3276f3b-409f-4161-b899-c80e6aaf9706)

Discrete 경우에는 Markov matrix이고 continuous 경우에는 $\nabla \ln P(x)$ 를 쓴다고 이해하였다. 
MCMC 와 Metropolis-hastings도 이전에 공부했던 기억이 나는데 벌써 잊어버려 기억이 잘 안 난다...😅