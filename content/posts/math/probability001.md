---
title: "Probability001"
date: 2024-04-18T01:08:51+09:00
draft: false
toc: false
images:
tags: 
  - probability
---

### Probability

This probability series are based on the book `Introduction to Probabilty` by Prf.Joe Blitzstein and his Harvard lectures on Youtube.
I try to summarize essential parts as easily as possible and explain some paramount concepts for me and those who struggle to understand math like me :grinning:

Why we need probability?  
It is important to ask the reason whenever I study a concept, I always want to know why do I need this in my life? and what is the purpose of it?  
Well, you often can hear the words like 'bet', 'likely', 'uncertainty' etc in all the places. These words are related to probability.  
The origin of probability is from gamble. A study from Gamble! What a study it is!!

The book often take examples from poker game. Better to know what made of it. 52 cards with 4 different shapes(spade, heart, diamond, club). so each shape has 13 cards(Ace to King).

Let's start with **Sample Space** and **event**.  
>Sample Space $S$ of an experiment is the set of all possible outcomes of the experiment.  
An event is a subset of the sample space $S$

table image page17


### Naive definition of probability

$$
P_{naive}(A) = \frac{\# \enspace of \: outcomes \: favorable \: to \: A}{\# \enspace of \: all \: possible \: outcomes \: in \: S}
$$

### How to count


### Binomial coefficient

You need to know first about factorial `n!`. $n! = n \times (n-1) \times (n-2)\times \cdots \times 2 \times 1$ <br />
Let's say you want to pick **K** sports players from a set of **n** players. There are ${n \choose k}$ ways. Basically ${n \choose k}$ says, we are counting the number of ways to choose k objects out of n, without replacement and without distinguishing between the different orders. eg.{3, 1, 4} = {4, 1, 3}. For example, There are 4 players and we need to choose 2 players for a game. 

For any nonnerative integers k and n, the *binomial coefficient* ${n \choose k}$, read as "n choose k", is the number of subsets of size k for a set of size n.

