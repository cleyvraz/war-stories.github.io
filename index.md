---
layout: default
---

# Introduction

A civil war is typically caused by a combination of complex factors and its effects are usually long-lasting. But does it only impact its country of origin? How do the dynamics of economical and societal metric evolve surrounding these onset? Does a state equips itself in suspicion of civil conflict? (??ADD MORE??) ? These are the questions we are going to answer here.

In their publication, Muchlinski, Siroky, et al. seeked to predict the onset of a civil war using two different techniques : logarithmic regressions and Random Forests. While the logistic regression are widely used to developed model with binary outcomes, the use of Random Forests was original and allowed the researchers to identify features with a strong predictive power.
These metrics were for the most already considered relevant in the literature (GDP growth, Education level etc.) as explanatory variables. This data story presents itself as an extension of this paper and aims at understanding and visualizing trends in these pertinent features.

But first, what is a civil war? The dataset used is from Sambanis which defines civil war as an armed conflict, in which the governement is one of the combatant, in a state recognized internationnaly with a population of at least half a million. The onset is declared as the year in which there are at least 500 deaths as long as there are 1000 deaths over the next three years. 

Let us have a quick look at the dataset. In the map below, you can see the 116 CW onset taking place in 72 different countries. Some countries have been striken mutiples times in this dataset which ranges from 1945 to 2000. In light grey are the countries for which the data is unavailable. 

{% include world_map_CW_over_years.html %}


# How is a country impacted by civil war?

To study the impact of an onset, we will look at the time evolution of some relevant features. We will first look at the proportion of country which saw a major change in relevant features. Below, you can see the proportion of countries which saw an increase bigger or equal (???) than the threshold. For exemple, ....

(ADD PLOT PROPORTION ANTOINE)

#### Indonesia
Let us now focus on some special cases, like Indonesia, which is the most striken country with in total 7 civil wars. Looking at the time evolution of some of the most relevant features, we can notice a few things. Primary and secondary education mostly follow the same trend, which is to be expected, but with different amplitudes. Overall, primary education 

{% include indonesia_evolution.html %}


{% include iraq_evolution.html %}




# Conclusion
