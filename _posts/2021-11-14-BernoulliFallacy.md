---
layout: post
title: "Bernoulli's Fallacy"
date: 2021-11-14
published: true
---
<p style="text-align:center"><img src="/assets/BernoulliCover.png" width="200"/><br></p>

In statistics courses in undergraduate and graduate, as well as corporate statistical training, I was repeatedly 
instructed in statistical tests and null hypothesis. I was never given any hint that I was only being taught only the frequentist 
school of statistics and completely neglecting the other - Bayesean[^1]. It appears that I'm old enough now to have some of my traditional education be, if not proven wrong, at least inadequate. The book I recently finished [Bernoulli's Fallacy, Statistical Illogic and the Crisis of Modern Science](https://www.amazon.com/Bernoullis-Fallacy-Statistical-Illogic-Science/dp/0231199945) does a good job of giving the history behind why Bayes was neglected through much of the twentieth century and the flaws in frequentist statistics, and further explains why that is such a mistake.

The author starts the book with the fundamental idea that you have to work your way through to understand the flaw in frequentist statistics.

<i>The probability of the hypothesis given the data is __not equal__ to the probability of the data given the hypothesis.</i> 

This counter-intuitive statement follows directly from Bayes theorem:

<p>P(H|D) = P(D|H) * P(H)/P(D)</p>

which follows from a simple algebraic manipulation of the following identity:

<p>P(H and D) = P(H|D)*P(D) = P(D|H)*P(H)</p>[^2]

All of frequentist probability focuses on the what the probability of the data is given the hypothesis. If the data is very unlikely, one rejects the null hypothesis. But Bayes tells you you must also consider the <i>prior</i> probability P(H).

Going further requires getting into the epistemology of probability. Does probability have meaning for one time events? Frequentists say no, but Bayes's followers are more open to the idea.

After reading this book I'm going to be much more skeptical anytime I hear phrase statistically significant and attempt to incorporate my prior and Bayes when working with probabilities.

[^1]: I think it is very likely that my corporate trainers had no ideas about Bayes equation and it might even be true that my college instructors (who weren't statistics PhD's) did either.

[^2]: The "|" symbol in the equation <p>P(H|D) means the probability of H conditioned on D, or probability of H given D.