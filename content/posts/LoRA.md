+++
title = 'LoRA'
date = 2024-01-31T14:50:41+09:00
draft = false
+++

### Reference
- https://arxiv.org/abs/2106.09685
- [Hugging Face's PEFT library](https://huggingface.co/docs/peft/v0.7.1/en/index)

Low-Rank Adaption

The concept of **`rank`** appears in Linear Algebra.  
The rank of a matrix A refers to
- the number of linearly independent columns of A
- the dimension of the vector space spanned by its columns(independent columns)

For the details, see the **Linear Algebra** posts.

I didn't know about **PEFT(Parameter-Efficient Fine-Tuning)** until I saw LoRA.  
It has several advantages.
1. Cost efficient for training
2. Less time consuming to train
3. Can save only adapter model

At first, I was perplexed by the concept of SVD(Singular Value Decomposition) since I was not and am not fully understand it. I thought I should have known it before I try to understand this LoRA. 

However, I rather focus on the a letter D(Decomposition) than SVD. There are more than one matrix decomposition method such as LU, QR etc. Anyway the point is that we can decompose a matrix into 2 or more matrices. For instance, matrix W can be decomposed into matrix A and B. Don't forget that if we interpret in reverse, it also means we can multiply 2 or more matrices into a matrix.  


In the paper, there is an equation (3).  
$\Delta W = AB$  
Without LoRA, We have to fine-tuning the whole $W$ matrix.(left-side of equation)  
With LoRA, We only need to fine-tuning matrix A and B.(right-side of equation)

*"Why do you even bother yourself since you need to adjust two matices with LoRA?"*

Let's say matrix $W$ is 100x120 matrix. Then We have to fine-tuning 12,000 parameters.  
If matrix A is 100x20(r) and matrix B is 20(r)x120, then we merely have to fine-tuning 4,400 parameters. Imagine r(rank) is less than 20 like 8. Hmm...800+960...1760 ?!  
Well, This is the beauty of Math. :heart_eyes:
