:Authors:
  Timo Lorenz
:Version: 0.1

What is probability?
####################

When we talk about probability, we are talking about a concept that is omnipresent in our life – from thinking about all the probabilities you have after finishing your work or the most basic of all probability examples, the ‘mother of probability’, gambling. The concept of probability is even more fundamental when we take a look at how we understand science and approach all parts of statistical methodology. Yet most of the time students cringe when the word probability is spoken.

To be fair, almost everyone´s ability to estimate probabilities in real life decision-making is very limited at best (`Fhaner, 1977`_) because we seem to be prone to deterministic instead of probabilistic causations (`Frosch & Johnson-Laird, 2011`_). This makes it even more important to spend some time with this concept. If we are that bad at estimating probabilities in our everyday life, we should at least get a better understanding of how we deal with it in science. In this chapter, we will have a look at where our idea of probability comes from, along with its two points of view – the so called ‘objective’ and ‘subjective’ probability – that are still debated in psychology (`Benjamin et al. 2018`_; `Dienes, 2011`_; `Howard, Maxwell, & Fleming, 2000`_; `Taper & Lele, 2010`_). We will try to grasp the concepts in this chapter, since much of classical statistical tests will be explained later – so we’ll try to use as few formulas as possible. Before we have a look at the two opposing schools of probability, let´s have a look at the history and maybe some reasons why one school was dominant in psychology for a long time.

A brief history of gambling and egos
************************************

While we can find thoughts and solutions on probability from great names such as Galileo and other scientists, the notion that probability has a quantitative value between 0 and 1 - and with this forming our contemporary understanding of probability, emerged somewhere in the middle of the 17th century with the work of Pascal and Fermat (`Galavotti, 2015`_). The reason why these two came up with new ideas on probability was more mundane than you might think – it was gambling. According to `Hacking (1975)`_ Pascal was asked by the Chevalier de Méré from the court of Louis XIV to solve ‘problems about games of chance’ (`Hacking, 1975`_, p. 57) – namely gambling – such as fair chances in dice tosses and how players should divide the stake when a game got interrupted. Pascal and Fermat had the idea that their concept of probability could not only be used to solve gambling problems but could also be used as a general model for reasoning under uncertainty. `Hacking (1975)`_ puts it quite frankly into the words ‘On the one side it [probability] is statistical, concerning itself with stochastic laws of chance processes. On the other side it is epistemological, dedicated to assessing reasonable degrees of belief in propositions quite devoid of statistical background’ (p.12). Et voilà, we had the birth of our modern understanding of probability and with it the problem that we have a possible epistemic (belief or subjective) and an empirical (frequencies or objective) interpretation of it.

For some time having two sides of a coin was not that much of a problem and both possible interpretations coexisted. You will find all kinds of important work on probability from all the names you can find in a typical textbook on statistics – from Huygens to the Bernoullli family, Poisson, Gauss, Borel, Markov to Kolmogorov who in 1933 showed that the mathematical results of probability follow a basic set of axioms (`Dienes, 2008`_; `Galavotti, 2015`_). But a few names stand out in this history of probability – Bayes, Laplace, Fisher, Neyman and Pearson - because they are basic to our understanding of probability in statistics and its opposing school, so let´s zoom in on them.

Thomas Bayes (1702-1761) was a minister and a member of the Royal Society with only one publication under his name during his lifetime. He became the name giver of the ‘Bayesian school’ or the subjective probability when his friend Richard Price published a manuscript of his after his death. The manuscript was on the problem of how one may obtain the probability of a hypothesis given some data – something we would later call the Bayes’ theorem. This concept was as simple as it was beautiful – We modify our opinion with objective information: Initial beliefs + recent objective data = new and improved belief (`McGrayne, 2011`_). We will have a closer look at this theorem later in this chapter.

Bayes’ ideas were picked up by Pierre-Simon Laplace (1749-1827) in the early 19th century. Laplace was a probabilist and even referred to as the “Newton of France” for his work in physics and astronomy. In his lifetime he came up with two theories of probability that showed more or less the same results with very large samples (`Galavotti, 2015`_). Just on a quick side note – Laplace despised gambling.

Times changed; politics as well as personal animosities played their part as much as a shift in the idea what ‘science’ could do, and with it crashed the idea that there is a balance between subjective beliefs and objective frequencies. The new natural science wanted a ‘route to certain knowledge’, and how could this be subjective in any way? This led to scientists treating the two points of view in probability as diametrical (`McGrayne, 2011`_). Soon mathematicians should take over the field of probability, bringing with them the frequentist approach or objective probability and most terms, concepts and techniques we use in statistics today (`Dienes, 2008`_).

The most dominant name in this upcoming approach would become Sir Ronald Fisher (1890-1962), a geneticist, who coined the terms ‘null hypothesis’ and ‘significance’, and suggested a p-value of .05 as an arbitrary level to judge a result statistically significant (`Dienes, 2008`_). After working for years on randomization, sampling theory, experimental designs, tests of significance and analysis of variance he published a revolutionary manual for non-statisticians – Statistical Methods for Research Workers (`Fisher, 1925`_). This manual was a game changer and helped to turn the frequentist approach into the state of the art for years to come.

Aside from (or maybe because of) his smart mind, Fisher was in a constant ad-hominem feud with his colleagues, especially Karl Pearson (1857-1936) – a fanatical eugenicist and name-giver of the Pearson correlation, his son Egon Pearson (1895-1980), a statistician, and his colleague Jerzy Neyman (1894-1981), a mathematician (`McGrayne, 2011`_). The last two developed the ideas of hypothesis testing and statistical inference (`Pearson & Neyman, 1928`_; `Neyman & Pearson 1933`_). Even though Pearson and Neyman had a heated and ongoing feud with Fisher, the three of them still became the ‘godfathers’ of the so called objective probability approach and with it the still most ubiquitous method in the social and behavioral sciences - null hypothesis significance testing (NHST; `Cumming et al., 2007`_, `Perezgonzalez, 2015`_).
Now that we have an idea on the who is who of probability, let´s go and have a look at the two schools of thought in detail. We will have a look at their logic and their basic concepts. Let us begin with the objective probability.

Objective probability
*********************

The so called objective probability or frequentism is still the most common logic in the social and behavioral sciences, from statistics courses to most journals in this field. There are two classical approaches to frequentism – Fisher significance testing and Neyman-Pearson hypothesis testing. Table 1 (taken from `Kline, 2013`_, p. 68) shows you the difference between the two, and that most frequentists today follow the Neyman-Pearson logic, which most people now know by the name null hypothesis testing (NHST). As you can see in the table, the Neyman-Pearson logic is in reality a hybrid of Fisher´s ideas and terms he coined and the hypothesis testing ideas of Neyman and Pearson (`Dienes, 2008`_). In this part, we will have a look at the logic and assumptions of these steps in NHST.

+------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+
|Fisher                                                                              | Neyman-Pearson                                                                                             |
+====================================================================================+============================================================================================================+
| 1. State :math:`H_0`                                                               | 1. State :math:`H_0` and :math:`H_1`                                                                       |
|                                                                                    | 2. Specify :math:`\alpha`                                                                                  |
| 2. Specify test statistic                                                          | 3. Specify test statistic                                                                                  |
| 3. Collect data, calculate test statistic, determine :math:`p`                     | 4. Collect data, calculate test statistic, determine :math:`p`                                             |
| 4. Reject :math:`H_0` if :math:`p` ist small otherwise, :math:`H_0` is retained    | 5. Reject :math:`H_0` in favor of :math:`H_1` if :math:`p < \alpha`; otherwise :math:`H_0` is retained     |
+------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------------------+

Frequencies and infinity!
=========================

The objective probability approach follows the idea that the probability of something happening is not in the mind, or a subjective belief, but rather objectively exists in the real world and needs to be discovered (`Dienes, 2008`_). A subjective interpretation of probability is not compatible with science (`Popper, 2013`_).

The objective interpretation of probability is analyzed through a long-run relative frequency (`von Mises, 1957`_)– ‘wherein probability is the relative frequency of a given attribute, that can be observed in the initial part of an indefinite sequence of repeatable events’ (`Galavotti, 2015`_, p. 748). What does that mean? The classical example is a coin toss – imagine you want to know if a coin is fair, so chances are equal between heads and tails. You flip it 10 times and it comes up with an unequal number of times between heads and tails. Does that mean the coin is not fair? No, because it is possible that a coin could show heads 3 out of 10 times. You would need an infinite number of coin tosses to determine exactly, whether the coin is fair – any number of repetitions smaller than infinity will always be an approximation.

Pretty quickly you now realize that the idea of an infinite number of observations would be impossible, and that this is an idealization of what is actually possible. So how can we manage this problem, since most of us do not have the time for an infinite number of observations? Neyman-Pearson came up with an idea for that problem – setting up a set of decision rules for accepting and rejecting a hypothesis so that in the long run we will often not be wrong (`Dienes, 2008`_).


Let´s come up with a hypothesis (and a rejection rule)
======================================================

This set of decision rules is quite strict (see Table 1 to refresh the rule set) and we will have a look at it from the beginning. The first thing we need to do is set up two hypotheses. The first one is the null hypothesis (:math:`H_0`) and the second one is the alternative hypothesis (:math:`H_1`).

The :math:`H_0` are most commonly either nil hypotheses – where the value is 0 - or point hypotheses with a numerical value of a parameter. You would use the nil hypothesis when the parameter is unknown, for example in a new field of research. When you have an idea that the parameter will be some specific value other than zero, you would use the point hypothesis.

The H1 is a range hypothesis that can be either non-directional (two-tailed), predicting any result that is not included in the H0, or directional (one-tailed), predicting a value that is smaller or greater than the one included in H0. To give you an idea, here is an example: Given that

:math:`H_0 = 0`, a non-directional :math:`H_1` would be :math:`H_1 \neq 0` and a directional :math:`H_1` would either be :math:`H_1 < 0` or  :math:`H_1 > 0`. All this is to be specified before the data is collected.

Now we need a line of rejection and this is :math:`\alpha` or the level of significance which is set at 0.05 (remember - the term significance and the convention of :math:`\alpha = 0.05` were Fisher`s ideas) by most conventions in the social and behavioral sciences. In a given observation we can now calculate the :math:`p`-value, and if this is below :math:`\alpha = 0.05`, we would speak of statistical significance. Sometimes people confuse :math:`\alpha` and :math:`p` (`Hubbard, Bayarri, Berk, & Carlton, 2003`_). `Gigerenzer (1993)`_ helps us to differentiate these two by referring to :math:`p` as the exact level of significance in the observation and :math:`\alpha` is the line that gives us the long-run probability error.

The basic idea here is that if the :math:`H_0` is true, and we would have an infinite number of observations, in the long run, we would falsely reject the :math:`H_0`. I told you above, it is a system of decision that will help us to minimize errors in the long run. So let us have a look at the two possible types of errors here.


It is about the errors...long term errors
=========================================

We have met :math:`\alpha` but there is another important possible long-term error – :math:`\beta`. Remember, :math:`\alpha` is the long-term probability error that says when :math:`\alpha = 0.05` there is a 5% long-term error chance to reject the :math:`H_0` when it is true. This type of error is called the Type I error. In the binary thinking of accepting or rejecting a hypothesis, there must be a second possible error – accepting the null hypothesis when it is in false. This type of error is called Type II error or :math:`\beta`. We can put this into a nice little ‘formula’: :math:`\alpha = P(\text{rejecting}\ H_0 | H_0\ \text{is true})` and :math:`\beta = P(\text{accepting}\ H_0 | H_0\ \text{is false})`.

In the frequentist approach, you should control for both types of long-term errors and decide on an acceptable level for both. Since Fisher suggested the :math:`\alpha = 0.05` most people and journals tend to blindly follow this rule. `Aguinis et al. (2010)`_ advise caution with that and to reflect on the desired relative seriousness of the Type I vs. Type II error, depending on your research. `Neyman (1953)`_ suggested :math:`\beta = 0.20` as the highest possible value for :math:`\beta`, and :math:`\beta = \alpha` as its lower floor. So how do we control for the Type II error? You need to

1. estimate the effect size that matches your statistical method - e.g. Cohens-:math:`d` (`Cohen, 1977`_) when looking for mean differences – and which you think would be relevant in real life, given your theory is true and
2. do a prospective (a priori) power calculation.

Power is essentially :math:`1 - \beta`. So if you decide you want to keep :math:`\beta` at .05 you need a power of 0.95. There are free calculators and programs like G\*Power (`Faul, Erdfelder, Buchner, & Lang, 2009`_; `Faul, Erdfelder, Lang, & Buchner, 2007`_) as well as good practical papers (e.g. `Howell, 2012`_; `Murphy & Myors, 2014`_) out there to help you calculate power. This will be discussed more in-depth in a later section of this volume. Interestingly, many researchers seem to spend a lot of thought on the Type I error but almost seem to ignore the possible Type II error (`Brock, 2003`_; `Kline, 2013`_; `Sedlmeier & Gigerenzer, 1989`_). Unfortunately, this is not the only problematic thing that occurs a lot – there are some serious misconceptions about the :math:`p`-value as well.

Some more errors but mostly not planned ones.
=============================================

The :math:`p`-value is essential to most statistical tests in NHST. It is the probability (where the :math:`p` in :math:`p`-value comes from) of witnessing the observed result or even a more extreme value if the null hypothesis is true (see `Hubbard and Lindsay, 2008`_; `Kline, 2013`_). Unfortunately, many psychologists – from students to professors - often have some misconceptions about the :math:`p`-value (`Badenes-Ribera, Frias-Navarro, Iotti, Bonilla-Campos, & Longobardi, 2016`_; `Badenes-Ribera, Frias-Navarro, Monterde-i-Bort, & Pascual-Soler, 2015`_; `Haller & Krauss, 2002`_, `Oakes, 1986`_). This is so common that we should have a close look at this so that you will not make these mistakes in your career. `Badenes-Ribera et al. (2016)`_ name the most common misconceptions: the ‘inverse probability fallacy', the ‘effect size fallacy', the ‘clinical or practical significance fallacy’, the 'replication fallcy’ and `Verdam, Ort, & Sprangers (2013)`_ expand this by adding the ‘proof fallacy’.

*The inverse probability fallacy* is the belief that the :math:`p`-value tells us the probability of the theory is true given the data - when really it is the other way around, and not at all interchangeable. Coming back to a basic formula - the fallacy here is to think that :math:`P(\text{theory} | \text{data})` while in truth it is :math:`P( \text{data} |\text{theory})` and one cannot infer the probability of one of these two just by knowing the inverse variant.

`Dienes (2011)`_ fills this theoretical approach with a rather bloody and graphic example which should make this seizable for you: The probability of being dead given that a shark has bitten off one`s head - or :math:`P(\text{dead}|\text{head bitten off by shark})` - is 1. The probability of a head bitten off by a shark given one is dead - or :math:`P(\text{head bitten off by a shark}|\text{dead})` – is almost 0 since most people die of other causes. Therefore, one should not mistake :math:`P(\text{data}|\text{theory})` with :math:`P(\text{theory}|\text{data})`.

*The effect size fallacy* is the false belief that the smaller the :math:`p`-value, the larger is the effect (`Gliner, Vaske, & Morgan, 2001`_). Yet the effect size is not determined by the :math:`p`-value but by its appropriate statistic and the confidence interval (`Cumming 2012`_; `Kline, 2013`_). Simply spoken, the :math:`p`-value by itself gives you very little information about the effect size.

*The clinical or practical significance fallacy* is closely related to the effect size fallacy because it links a statistically significant effect with the idea that it is an important effect (`Nickerson, 2000`_). The truth is that a statistically significant effect can be without any clinical or practical importance. Just imagine two samples of one million people each are measured in height and the statistical test shows that they have a statistically significant difference in height. But in real life, they have a mean-difference of one millimeter – no one would say that a one millimeter height difference has any practical importance. `Kirk (1996)`_ states that the clinical or practical importance of results should be described by an expert in the field, not presented by a :math:`p`-value.

*The replication fallacy* is the false belief that the :math:`p`-value gives you an exact idea about the replicability of the results. This fallacy even has people mistakenly thinking that the complement of :math:`p` (i.e. :math:`1-p`) tells you the probability of finding statistically significant results in a replication study (`Carver, 1978`_). Unfortunately ‘any :math:`p`-value gives only very vague information about what is likely to happen on replication, and any single :math:`p`-value could easily have been quite different, simply because of sampling variety` (`Cumming, 2008`_, p. 286).

*The proof fallacy* is the fallacy to think that when the null hypothesis is rejected, it proves that the alternative hypothesis is true because there can be possible alternative explanations. Furthermore, it is also a fallacy to think when the null hypothesis is not rejected, it proves that the alternative hypothesis is false because this just might be a consequence of statistical power (see `Verdam et al., 2014`_).

Conclusion
==========

As you can see, the school of objective probability or frequentism is not without some serious pitfalls and yet it is still the most dominant framework used in the social and behavioral sciences. It has its own logic that unfortunately is so often misunderstood that some researchers go so far as to call for an abandonment of significance testing (e.g. `Harlow, Mulaik, Steiger, 2016`_; `Kline, 2013`_). Other authors (e.g. `Cummings, 2013`_) or the APA manual (`APA, 2010`_) demand the reporting of confidence intervals instead of or in addition to :math:`p`-values. Strangely, this is what Neyman often did. He rarely used hypothesis testing in his own research but most of the time reported confidence limits around the estimates of his model parameters (`Dienes, 2008`_). `Oakes (1986)`_ muses that some of the confusion in frequentism is due to fact that many researchers unknowingly have a subjective probability or Bayesian understanding of research. So it is time to see have a look at this approach and see if you are one of them.


Subjective probability
**********************

Introduction and the Bayes theorem
==================================

Remember that objective probability ‘only’ tells us something about inferences about long-run frequencies and their possible error rate but not about the probability of a hypothesis being right. But most people want to have some information on that as well. Just imagine you are leaving your apartment but before you do that, you look out the window and think ‘What are the odds it might rain today?’. Would you grab an umbrella or not? You might base your decision on how you high you estimate the probability of rain to be on this day. Objective probability cannot help you in this case, because this is a single event, not a long-run frequency. The moment you make a decision thinking ‘I think it may rain today, I’d better take an umbrella with me’, you are in the realm of subjective probability.

Subjective probability is the degree of belief you have in a hypothesis (`Dienes, 2008`_). Of course it gets a little more complicated than that when we are talking about how to implement subjective probability into a statistical tool but the essence stays the same. The most basic notion here, before we get to the details, is that you have an inkling of the probability of a hypothesis. You might check some sources, collect some data – in our example, you might check the Weather Channel – but at the end of day, you have to decide if you think the probability of rain is high enough to take an umbrella with you.

Because most people are not really good at updating their personal beliefs in the light of new information (`Sutherland, 1994`_), we have to come up with a system that helps us to be more scientific. At this point we come back to Bayes and his friend Price who presented his work posthumously to the Royal Society. In this work, Bayes describes the fundamental logic to subjective probability – the Bayes` theorem (`Bayes & Price, 1763`_):

.. math::

  P(H|D) = P(D|H) \cdot \frac{P(H)}{P(D)}


Now, let us pick this apart:

- :math:`P(H|D)` is the posterior, the probability of a hypothesis given some data
- :math:`P(D|H)` is the likelihood or the probability of obtaining the data given your hypothesis
- :math:`P(H)` is the prior, your belief about the hypothesis before you start collecting data
- :math:`P(D)` is the evidence or the data

We will take a closer look at these components in a moment, but first some more general ideas: if you want to compare hypotheses given the same data, P(D) would be constant and you switch the formula above to:

.. math::

  P(H|D) \propto P(D|H) \cdot  P(H)

Your posterior is proportional to the likelihood times the prior – and this is the basic tenet of Bayesian statistics. It simply tells you that you will update the prior probability of your hypothesis when you have some data and you will form a new conclusion – the posterior. In real human words this means – from a Bayesian point of view, your scientific inference is updating your beliefs in a hypothesis when you have some new data (`Dienes, 2008`_). Before we get a more detailed look at some important concepts, let us make a short excursion into the philosophy of science and give these new concepts some time to settle in your mind. Our excursion should make it clearer why so many scientists had a hard time with subjective probability, even when most of us are using it intuitively.


A philosophical excursion to Popper & Hume
==========================================

When you think about the logic of the Bayesian approach, it is pretty close to inductive thinking – the process to come up with rules from observations. Let us take the famous swan argument here as an example. You see one white swan; and another one; and another one; and so on, and you come to the inductive conclusion that all swans are white. You have no guarantee that this rule is true but due to your observations it seems plausible to you. You can do the same thought experiment with the thought that you will wake up the next morning or that the sun will rise. The school of thought that used inductive thinking was called positivism and this thinking had two famous opponents – David Hume (1711-1776) and Sir Karl Popper (1902-1994).

David Hume was a Scottish philosopher who argued that we should never reason from experience (seeing a lot of white swans) about situations we have not experienced yet (seeing a swan of a different color). You might say that in your experience the probability increases when you see tons of white swans that the next one will be white too. Hume would disagree with that because it does not follow logically. Take the second thought experiment – you waking up in the morning. Every day you wake up in the morning and this experience should increase the probability of you waking up tomorrow – inductively speaking. Now, add age to the equation and you see at one point, it becomes less likely that you will wake up the next morning. Hume points out that ‘no matter how often induction has worked in the past, there is no reason to think it will work ever again. Not unless you already assume induction, that is’ (`Dienes, 2008`_, p.5). A historical fun fact that is closely related to the swan argument, comes from the time that the British went to Australia. Guess what they found? Of course, they found black swans.

The second interesting mind here is Karl Popper, who wrote a lot about the philosophy of science and what distinguishes science from non-science. Popper argued against positivism and with it inductive thinking and his philosophy was fallibilism. In a nutshell (because `Chapter 1.2`_ is dealing with this in a much deeper way): You cannot say something is true, you can only falsify statements. Popper agreed with Hume’s statements (e.g. `Popper, 1934`_). For him a theory would in a best case scenario always be a guess, nothing more. Maybe his reasoning had something to do with the fact that during his youth one of the most dominant theories – Newtonian physics – was replaced by relativity and quantum physics. With that, something that many people believed to be established was suddenly false (`Dienes, 2008`_).

As you can imagine, these two, especially Karl Popper, had a huge influence on how people understood science in the 20th century, and why the school of objective probability was so dominant for a long time. Of course there is more to the story – from politics to history (for an in-depth look see `McGrayne, 2011`_) – but you have an idea why it took the school of subjective probability and with it the Bayesian approach for inductive reasoning so long to be back in the game. Now it is time for us to take a deeper look into the Bayesian ideas and its concepts.

The prior
=========

Let us start at the beginning – the prior or for the formula aficionados - :math:`P(H)`. Remember, the prior is your belief about the hypothesis before you start collecting data. How can we address this? First we have to assign a number between 0 and 1. Zero means there is no chance that the hypothesis is true and one means you are certain it is true. If you ask yourself how you should deal with all the possibilities between 0 and 1, the answer you will get from most people who have something to do with Bayes will be – How much money would you be willing to bet on your statement? This is a rather unclear answer so let us see how we can establish a prior in a more formal matter.

What we need is a distribution for the prior. First ask yourself if you have any previous information on the matter. This information may vary - from a special subjective belief to previous studies. If there is no information, we can use a ‘uniform prior’ or ‘uninformed prior’ with a uniform distribution where all values are equally likely. Do you have some previous information – let us say the distribution of the construct intelligence? You know that the distribution is a normal distribution with mean of 100 and a standard deviation of 15. So you could use this as your prior. Sometimes people use different priors to see how robust their posterior distribution is after the data. Some just use uninformed prior so that the likelihood (we will come to that one soon) will dominate completely – these researchers are called ‘objective Bayesians’ (`Dienes, 2008`_).

The concept of the prior is hard to grasp in the beginning and could be a big obstacle for some people to try Bayesian methods. And of course, there are a lot of debates about possible priors (e.g. `Gelman, 2009`_; `Kruschke, 2010`_; `van de Schoot et al. 2014`_; `Vanpaemel, 2010`_; `Winkler, 1967`_) because this is the most subjective part of this school of thought. If one person chooses a prior, it does not mean another person would agree with that prior. I hope you get the idea of the prior here.


Likelihood
==========

Now that we know more about the prior :math:`P(H)` , let us now talk about the second part – likelihood :math:`P(D|H)`. The likelihood contains the information about the parameters given the data. This means that the support for our hypothesis is provided by our data by a likelihood distribution with the possible values (`van de Schoot et al., 2014`_). Remember the Bayes´ theorem from above? The posterior is proportional to the likelihood times the prior or :math:`P(H|D) \propto P(D|H) · P(H)`. The likelihood connects the prior to the posterior so all information that is relevant to inference from the data is provided by the likelihood (`Birnbaum, 1962`_). We will have a likelihood distribution that is combined with the prior distribution or :math:`P(D|H) · P(H)` to obtain our posterior distribution :math:`P(H|D)`. What does that exactly mean?

Go back to your idea of previous information on your question. If you had no information and you were using a non-informative prior with a uniform distribution, all results would be equally possible. If you combine this with the likelihood, then it will show you exactly the posterior distribution because every probability in the prior was the same. But if you have some information and you are using an informed prior with a distribution of your choice, the likelihood will be combined with that information to form a posterior distribution. In the second case it means that the hypothesis with the greatest support from the data – the greatest likelihood – might differ from the highest posterior probability distribution. Also, if you have a lot of data the influence of the prior becomes less important to the posterior distribution (`Dienes, 2008`). Let us have a look at this with an example.

Imagine you would be interested in the number of rainy days in January and you have no idea about rain (uninformed prior). You would collect data by looking out the window (data and likelihood), you would come up with an idea about how many days it would rain (posterior) and maybe use that knowledge next year in January as a new and slightly informed prior. Or in a second case, you have the belief that it rains mostly when it is grey and cloudy (informed prior). Most January days in Central Europe are grey and cloudy so according to your belief, it should rain a lot. Once again you are collecting data by looking out your window (data and likelihood) and let us assume, it does not rain much but it is grey and cloudy, and you must update your information. But still the informed prior that it should rain on days that are grey and cloudy has an influence on your posterior. If you had collected tons of data on grey and cloudy days, and at the same time there is little chance of rain, the data would provide much more information on your posterior, your new belief about rainy and cloudy days, than your prior, your initial belief.
Once again you can imagine why the prior is so important (and debated, as mentioned above) because if the prior is misspecified, the posterior results are affected due to the compromise between likelihood and prior (`van de Schoot et al, 2014`_). Now that we have an idea of how prior and likelihood interact, we need to have a look at the last piece of the puzzle – the posterior :math:`P(H|D)`. The posterior will be a distribution that is a combination of prior distribution and likelihood distribution and represents your updated belief. The posterior shows you an explicit distribution of the probability of each possible value (`Kruschke, Aguinis, & Joo, 2012`_). Now you could use your updated belief as a new prior and repeat the whole process to update your knowledge once more.

Conclusion Bayes
================

I guess this was a lot to think about so let us take a breath and revisit the concepts. Using Bayesian methods and therefore the subjective probability approach is a way to update your subjective beliefs by combining your belief about a hypothesis and the evidence, and all this with distributions or different probabilities of possible results. This is much more complex than a possible black and white answer where you reject or do not reject a hypothesis. But we have seen that the prior is a double edged sword. It helps us to use previous knowledge (and often we have knowledge on things) but it can have an influence on our results because our previous knowledge might be very wrong and so we might choose a wrong prior. Given enough data this problem might not be so relevant but still it has been opening up debates in science for quite some time (e.g. `Gelman, 2009`_; `Kruschke, 2010`_; `van de Schoot et al. 2014`_; `Vanpaemel, 2010`_; `Winkler, 1967`_). Furthermore, the distributions of posterior probabilities might give a more complex picture of reality but often we are forced to make black and white decisions (decide if we want to pay for a medication or not) because we have to act. It is a different approach to probability and now you have heard of it as well. So let us end with some final thoughts.


Conclusion chapter
******************

At this point I hope you have a better understanding of two points of view of probability that are common in the social and behavioral sciences. Of course there is much more to it; more formulas, more mathematics, and different statistical approaches but my goal was to give you a first idea of the concepts that are at the basis of so many different methods in statistics. Both points of view come with their own strengths, weaknesses and possible pitfalls. I do not want to argue for one or against the other but my hope is that you will understand that both points of view have a different aim, a different inference, and are sensitive to different things. You should be aware of your research question and the kind of probability that helps you to find an answer to this question. Do you need a black and white answer using objective probability or do you need a continuous distribution of posterior beliefs using subjective probability? Both probabilities come with a huge toolbox of applicable statistical methods (and some of them are discussed by my colleagues in this volume) and many of those methods can be used with both approaches. So chose your tool and scientific approach to each question you ask very careful and aware of the alternatives. I wish you a pleasant journey into the wonderful world of statistics.


References
**********

Aguinis, H., Werner, S., Lanza Abbott, J., Angert, C., Park, J. H., & Kohlhausen, D. (2010). Customer-centric science: Reporting significant research results with rigor, relevance, and practical impact in mind. Organizational Research Methods, 13(3), 515-539.

American Psychological Association (2010). Publication Manual of the American Psychological Association (5th Edition). Wahsington, DC: American Psychological Association.

Badenes-Ribera, L., Frias-Navarro, D., Iotti, B., Bonilla-Campos, A., & Longobardi, C. (2016). Misconceptions of the p-value among Chilean and Italian academic psychologists. Frontiers in Psychology, 7, 1247.

Badenes-Ribera, L., Frías-Navarro, D., Monterde-i-Bort, H., & Pascual-Soler, M. (2015). Interpretation of the p value: A national survey study in academic psychologists from Spain. Psicothema, 27(3), 290-295.

Bayes, T. & Price, R. (1763). An essay towards solving a problem in the doctrine of chances. By the late Rev. Mr. Bayes, F.R.S. Communicated by Mr. Price, in a letter to John Canton, A.M.F.R.S. Philosophical Transactions, 53, 370-418.

Benjamin, D. J., Berger, J. O., Johannesson, M., Nosek, B. A., Wagenmakers, E. J., Berk, R., ... & Cesarini, D. (2018). Redefine statistical significance. Nature Human Behaviour, 2(1), 6.

Birnbaum, A. (1962). On the foundations of statistical inference. Journal of the American Statistical Association, 57(298), 269-306.

Brock, J. K. U. (2003). The ‘power’of international business research. Journal of International Business Studies, 34(1), 90-99.

Carver, R. (1978). The case against statistical significance testing. Harvard Educational Review, 48(3), 378-399.

Cohen, J. (1977). Statistical power analysis for the behavioral sciences. Cambridge, MA: Academic Press

Cumming, G. (2008). Replication and p intervals: p values predict the future only vaguely, but confidence intervals do much better. Perspectives on Psychological Science, 3(4), 286-300.

Cumming, G. (2013). Understanding the new statistics: Effect sizes, confidence intervals, and meta-analysis. New York, NY: Routledge.

Cumming, G., Fidler, F., Leonard, M., Kalinowski, P., Christiansen, A., Kleinig, A., & Wilson, S. (2007). Statistical reform in psychology: Is anything changing?. Psychological Science, 18(3), 230-232.

Dienes, Z. (2008). Understanding psychology as a science: An introduction to scientific and statistical inference. New York, NY: Palgrave Macmillan.

Dienes, Z. (2011). Bayesian versus orthodox statistics: Which side are you on?. Perspectives on Psychological Science, 6(3), 274-290.

Galavotti, M. C. (2015). Probability theories and organization science: The nature and usefulness of different ways of treating uncertainty. Journal of Management, 41(2), 744-760.

Hacking, I. (1975). The emergence of probability: A philosophical study of early ideas about probability, induction and statistical inference. Cambridge, UK: Cambridge University Press.

Haller, H., & Krauss, S. (2002). Misinterpretations of significance: A problem students share with their teachers. Methods of Psychological Research, 7(1), 1-20.

Harlow, L. L., Mulaik, S. A., & Steiger, J. H. (2016). What if there were no significance tests?. New York, NY: Routledge.

Howard, G. S., Maxwell, S. E., & Fleming, K. J. (2000). The proof of the pudding: an illustration of the relative strengths of null hypothesis, meta-analysis, and Bayesian analysis. Psychological Methods, 5(3), 315.

Howell, D. C. (2012). Statistical methods for psychology. Belmont, CA: Cengage Learning.

Hubbard, R., Bayarri, M.J., Berk, K.N., & Carlton, M.A. (2003). Confusion over measures of evidence (p`s) versus errros (α`s) in classical statistical testing. American Statistician, 57, 171-178.

Hubbard, R., & Lindsay, R. M. (2008). Why P values are not a useful measure of evidence in statistical significance testing. Theory & Psychology, 18(1), 69-88.

Faul, F., Erdfelder, E., Lang, A.-G., & Buchner, A. (2007). G\*Power 3: A flexible statistical power analysis program for the social, behavioral, and biomedical sciences. Behavior Research Methods, 39, 175-191.

Faul, F., Erdfelder, E., Buchner, A., & Lang, A.-G. (2009). Statistical power analyses using G\*Power 3.1: Tests for correlation and regression analyses. Behavior Research Methods, 41, 1149-1160.

Fhaner, S. (1977). Subjective probability and everyday life. Scandinavian Journal of Psychology, 18(1), 81-84.

Fisher, R.A. (1925). Statistical Methods for Research Workers. London, UK: Oliver and Boyd.

Frosch, C. A., & Johnson-Laird, P. N. (2011). Is everyday causation deterministic or probabilistic?. Acta Psychologica, 137(3), 280-291.

Gelman, A. (2009). Bayes, Jeffreys, prior distributions and the philosophy of statistics. Statistical Science, 24(2), 176-178.

Gigerenzer, G. (1993). The superego, the ego, and the id in statistical reasoning. In G. Keren & C. Lewis (Eds.), A handbook for data analysis in the behavorial sciences: Vol. 1 Methodological issues (pp. 311-339). Hillsdale, NJ: Erlbaum.

Gliner, J. A., Vaske, J. J., & Morgan, G. A. (2001). Null hypothesis significance testing: effect size matters. Human Dimensions of Wildlife, 6(4), 291-301.

Kirk, R. E. (1996). Practical significance: A concept whose time has come. Educational and Psychological Measurement, 56(5), 746-759.

Kline, R. B. (2013). Beyond significance testing: Statistics reform in the behavioral sciences. Washington, DC: American Psychological Association.

Kruschke, J. K. (2010). What to believe: Bayesian methods for data analysis. Trends in Cognitive Sciences, 14(7), 293-300.

Kruschke, J. K., Aguinis, H., & Joo, H. (2012). The time has come: Bayesian methods for data analysis in the organizational sciences. Organizational Research Methods, 15(4), 722-752.

McGrayne, S. B. (2011). The theory that would not die: how Bayes' rule cracked the enigma code, hunted down Russian submarines, & emerged triumphant from two centuries of controversy. London, UK: Yale University Press.

Murphy, K. R., Myors, B., & Wolach, A. (2014). Statistical power analysis: A simple and general model for traditional and modern hypothesis tests. London, UK: Routledge.

Neyman, J. (1953). First Course in Probability and Statistics. New York, NY: Henry Holt.

Neyman, J., & Pearson, E. S. (1933). IX. On the problem of the most efficient tests of statistical hypotheses. Philosophical Transactions of the Royal Society of London. Series A, Containing Papers of a Mathematical or Physical Character, 231(694-706), 289-337.

Nickerson, R. S. (2000). Null hypothesis significance testing: a review of an old and continuing controversy. Psychological Methods, 5(2), 241.

Pearson, J., & Neyman, E. S. (1928). On the use, interpretation of certain test criteria for purposes of statistical inference: Part I. Biometrika. A, 20, 175-240.

Perezgonzalez, J. D. (2015). Fisher, Neyman-Pearson or NHST? A tutorial for teaching data testing. Frontiers in Psychology, 6, 223.

Popper, K.R. (1934). Logik der Forschung. Zur Erkenntnistheorie der modernen Naturwissenschaft. (Logic of scientific discvovery). Wien, AU: Springer.

Popper, K.R. (2013). Quantum theory and the schism in physics: From the postscript to the logic of scientific discovery. London, UK: Routledge.

Oakes, M. (1986). Statistical inference: A commentary fort he social and behavioural sciences. Chichester, UK: Wiley

Sedlmeier, P., & Gigerenzer, G. (1989). Do studies of statistical power have an effect on the power of studies?. Psychological Bulletin, 105(2), 309.

Sutherland, S. (1994). Irrationality: The enemy within. London, UK: Constable and Company.

Taper, M. L., & Lele, S. R. (Eds.). (2010). The nature of scientific evidence: statistical, philosophical, and empirical considerations. Chicago, IL: University of Chicago Press.

Van de Schoot, R., Kaplan, D., Denissen, J., Asendorpf, J. B., Neyer, F. J., & Van Aken, M. A. (2014). A gentle introduction to Bayesian analysis: Applications to developmental research. Child Development, 85(3), 842-860.

Vanpaemel, W. (2010). Prior sensitivity in theory testing: An apologia for the Bayes factor. Journal of Mathematical Psychology, 54(6), 491-498.

Verdam, M. G., Oort, F. J., & Sprangers, M. A. (2014). Significance, truth and proof of p values: reminders about common misconceptions regarding null hypothesis significance testing. Quality of Life Research, 23(1), 5-7.

Von Mises, R. (1957). Probability, statistics and truth. London, UK: George Allen & Unwin

Winkler, R. L. (1967). The assessment of prior distributions in Bayesian analysis. Journal of the American Statistical association, 62(319), 776-800.
