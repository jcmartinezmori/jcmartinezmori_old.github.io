---
layout: post-no-feature
title: The Sophie Germain Identity
description: "Marie Sophie Germain was a nineteenth century mathematician who did extensive work on the theory of elasticity and on Fermat's Last Theorem."
mathjax: true
typefix:
   indent: true
date: 2016-02-05T03:47:56-05:00
---

Let's look at this question which was first appeared in the Mathematics Magazine 1950. It was put forward
by A.Makowski, a leader of the Polish IMO team. Later it was asked for the 1978 Ku:rschak
competition. 
				

>Prove that $$n^4 + 4^n$$ is composite for all natural numbers $n>1$.
				
This question is a particular example of the Sophie Germain's Identity which states that,
\begin{align}
	a^4 + 4b^4 = (a^2 + 2b^2 -2ab)(a^2 + 2b^2 + 2ab).
\end{align}

Marie Sophie Germain was an nineteenth century mathematician who did extensive work on 
the theory of elasticity and on the Fermat's Last Theorem. Her work enabled [TODO:find name]
to prove Fermat's Last Theorem for $n= 5$. For more information about Sophie Germain go this excellent
Mactutor biography[TODO:link]. So let's use the Sohpie Germain Identity to solve this question.

##Proof

Consider the special case when $n$ is even. Then,

\begin{align}
	2 \mid (n^4 + 4^n).
\end{align}

But what if $n$ is odd? Let $n = 2k+1$. Let's apply the Sohpie Germain Identity and see what we get. Notice that $n^4 + 4^n$ can be rewritten as,
\begin{align}
	(2k+1)^4 + 4\dot (2^k)^4.
\end{align}
Which means that we can factorize the expression into,


\begin{equation}
(2k+1)^2 + 2(2^k)^2 - 2(2k+1)(2^k) \times \\\
(2k+1)^2 + 2(2^k)^2 + 2(2k+1)(2^k)
\end{equation}

So we realize that the expression can indeed be factorized.

It's not too hard too figure out why $n$ cannot be $1$.
				
