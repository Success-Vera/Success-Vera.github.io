---
layout: post
title:  "Probably Approximate Correct (PAC) Learning Framework"
categories: "learning theory"
tags: "machine learning"
comments: true
# categories: coding
# tags: linux

---

* TOC
{:toc}

![](images/hlf/main.JPG)
<p align="center">My Picture</p>

## Introduction
PAC means Probably Approximate Correct. It is a computational learning framework that was introduced by Leslie Valiant in 1984. It considers the computational cost of making representations and the time complexity of
a learning algorithm. This learning framework requires that with high probability, a learning algorithm makes small errors.

In machine learning, we talk a lot about what it means to say that a machine has <em>learned </em>. But what does it really mean when you say that a machine has learned in the PAC framework?

According to Valiant (2013), learning is the ability to <em>generalize</em>.

But what does it mean to generalize?

Think about how you learned to read in English. You were taught two-lettered words, then three, then four, and so on. Maybe you were also taught phonetics. But I am very sure that you were not taught all the three-lettered words or all four-lettered words in the English dictionary nor were you taught all the words in the English dictionary. Somehow, you were able to pronounce new words you came across. Almost certainly, you made some mistakes in your pronunciations but almost surely, all the words you know now are not words that you were taught consciously.

How were you able to do that? Why were you able to do that?

I think a neurologist may be able to give an in-depth explanation of the <em>hows</em> and the <em>whys</em> 😊.

However, this capability of being able to read out a new word after seeing some words in the past even when you had not seen them previously is what is referred to as generalization.

We want a learning machine to have this special capability possessed by humans.  We want this machine to see only a few examples and be able to pronounce a new word. 

Just like humans, we do not require that the machine be correct all the time. We just want the machine to be correct most of the time.
However, we also have the requirement that any new example shown to the learning machine must not be different from the example from which it was shown previously. This means that if the machine has learned words in English, it shouldn't be expected to pronounce words in French or any other language. Think about it: do you require that a master in English must be a master in French? I wouldn't. I know you wouldn't too. This requirement means that we want the examples and the new words to come from the same distribution. Valiant (2013) refers to it as The Invariance Assumption. 

Furthermore, we require that there exist some regularities in the examples given to the learning machine. Think about this: how do we pronounce a new word or even a long word? We just think about a similar word we had come across and try to pronounce this new word the same way. How about a long word? We break down the word syllable by syllable, right? We were able to pronounce these words because of the regularities that exist in the English Language. Valiant (2013) refers to it as The Learnable Regularity Assumption.

Hence, we make the above assumptions about the examples given to the learning machine. We assume that the examples are invariant and regular.
The PAC-Learning framework also requires that a learning algorithm is efficient, with respect to space and time. 
Bringing all the above points together, we can define what it means to be PAC-learnable.

I think it is time to pause and talk about hypothesis classes which is a core idea in PAC-Framework. 

A hypothesis class $\mathcal{H}$ is a set that contains hypotheses. A hypothesis is a learning algorithm's prediction.

Bringing all the above points together, we can define what it means to be PAC-learnable.

## Definition 

We say that a hypothesis class $\mathcal{H}$ is PAC-learnable if there exists a learning algorithm $\mathcal{L}$ and a polynomial $p(\cdot,\cdot,\cdot,\cdot)$ such that for any $\epsilon,  \delta \in (0,1)$, for any distribution $\mathcal{D}$ on $X$ and for any concept $c$, if the algorithm $\mathcal{L}$ is given  $m \ge p(\frac{1}{\epsilon}, \frac{1}{\delta}, g,\text{cost}(c))$ examples, it returns a hypothesis $h$ such that with high probability of at least $1-\delta$ (over the choice of the examples $S$), we have small error $\epsilon$. This inequality
	\begin{equation}
	\underset{S \sim \mathcal{D}^{m}}{\mathbb{P}}[R(h) \le \epsilon] \ge 1-\delta \ \ \ \  \ \label{eq:pac}
	\end{equation}


I think it is time to pause and talk about hypothesis classes which is a core idea in PAC-Framework. 
A hypothesis class H is a set that contains hypotheses. A hypothesis is a learning algorithm's prediction.
Bringing all the above points together, we can define what it means to be PAC-learnable.