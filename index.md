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


# Findings
Helicopters goes pew pew
Big development gap between countries experiencing at least one versus non CW
Economical indicators such as GDP Growth and Primary Commodity Export are greatly affected by the onsets, for both the country itself and its neighbours
Weapon trade (TIV score) to increase around the onsets, for both the country itself and its neighbours.
XXX and YYY often supply heaven weapons to country experiencing civil war

# How is a country impacted by civil war?

To study the impact of an onset, we will look at the time evolution of some relevant features. First of all, we are going to study in the long lasting effects of a Civil War; how long does it take for a country to recover and return to the values it was at before the onset?

[histogrammes  sur la durée avant recovery] avec gdp, life et une 3e feature?]

Fortunately, it seems like the infant mortality (death of a baby under the age of 1 year), despite being affected by the onsets, usually recover in less than 1 year. However, the vast majority of the countries that weren’t able to restore their pre-conflict value before 2020 are located in Africa with conflicts that occurred in the 80s or 90s such as : Algeria (1991), Central African Republic (1996), Djibouti (1991), Haiti (1991), Iran (1981), Mozambique (1976), South Africa (1976) and Democratic Republic of the Congo (1991).

On the other side, the life expectancy at birth seems to take much longer to recover in some countries. As for the countries that did not recover before 2000, 3 of the conflicts occured after 1990 (Burundi, Central African Republic and Kenya), leaving very little time for recuperation. The Civil Wars that took more than 10 years to recover on this aspect are Colombia (1949-1958, El Bogotazo), Iraq (1959-1959 Mosul Uprising and 1961-1970 First Iraqi–Kurdish War) and Republic of Vietnam (1960-1975 Vietnam War).

If we focus our attention on economical factors, we can see that they are considerably more sensible and recovery periods are more spread out. The GDP growth, the holy indicator of a country's economy and development health in a capitalist world, takes in average 3 years to return to the value observed around the civil war onset. If we take for example the three countries that took more than 15 years to recover, we have China, who, because of the Cultural Revolution started in 1966, took 18 years before experiencing a GDP growth greater than 0.14%. Similar observation for Iraq, who took 18 as well to retrieve a GDP growth greater than 0.16%. Finally Vietnam had to wait the end of the Vietnam War, 16 years later, during which the GDP growth remained below 0.001%.

Countries with high Primary Commodity Export (to which Oil belongs) were reported as likely to experience civil war according to Collier and Hoeffler, two political science researchers. Even if their conclusion is disputed, we are curious to see how this division/department of a country trade is impacted. It appears that it takes on average a little bit more than 5 years to return to “normal” levels : longer than the GDP growth! We must however consider the fact that 28 countries, almost half of the countries experiencing civil war (72), weren’t able to revert to their original export level.

With we narrow the study to countries possessing oil in their soil/on their territory (34, for 16 onsets), a slightly different trend appears : the average is now 8 years, with a median at 4 years. It’s important to outline that Indonesia accounts for almost half of the onsets in this subset, with repressions of Communist movements (1949, 1963) and Darul Islamism (1949), as well as regional independence suppression (1950, 1956, 1963, 1975).

We will now take a more global approach and take a look at the trends across all the onsets across the world. To do so, we will compute the proportion of countries which saw a noticeable change between the 3 years preceding the conflict and the 3 years after (year of the onset included). Feel free to select a threshold and see the proportion of countries which experienced a variation greater than value selectionned! (NB: if data is missing, the onset is excluded from the analysis to limit biais).

{% include proportion_country_feat.html %}

We would like to draw your attention to the fact that depending on the variable considered, an increase should not necessarily be perceived as a deterioration and vice-versa.

By using a threshold of 0.05, it becomes evident that for 20% of onsets, the country experiences a diminution of the life expectancy at birth. It corresponds to approximately XX years.


A threshold of 0.1, ie a before/after variation of 10%, let us observe trends for several features:
The infant mortality increase for 30% of the onsets. As mentioned in section [bblabla] , this indicator tends to rapidly recover but the effects of the conflict are devastating on the year of the onset. Likely to be bound to the definition of the infant mortality itself as it accounts for the mortality for babies under 1 year.
The primary commodity export decrease in approximately 70% of the onsets; this domain seems to almost systematically suffer from the conflict and we could explain it by the disruption of the transports, social and economic instabilities or increased border control/borders closing.
The military power, measured as the share of the population enrolled in military forces, also increases for the vast majority of the country. When choosing a threshold a 2, ie a doubling of the militarised population, a few onsets emerge/remains : 1988 Burundi (Tutsi Genocide), 1982 Nicaragua (Cold-War proxy, revolution), 1966 Nigeria (succession of military coups), 1984 Zimbabwe (Ndebele genocide).
Weapon import, measured as TIV units by the SIPRI (Stockholm International Peace Research Institute), increases for 40% of the onsets while it decreases for 28% of the onsets. These military equipment fluxes take in consideration the quality/grade of the material (new, refurbished, used, …) and cover illegal transactions as well.

[faire un small multiple avec les features  3 colonnes, 2 lignes]


[plots avec sélection de la feature pour 4 pays, vision over time, 2 colonnes, 2 lignes]
As we can observe, the influx of military equipment does increase around the civil war onsets. Based on the dataset found on the SIPRI website, it’s possible to analyse the transaction for heavy equipment such as planes, tanks and missiles.

# Weapon trade surrounding civil war onset

By combining the Sambanis civil war dataset and the weapon trade registry, we analyzed the trends in weapon import during years surrounding a civil war onset. We hope to find certain trends in weapon imports, either by type, or by exporting nation.

We look at the variation in the number of weapon imports for a fixed number of years before, and after the civil war onset for each event in the sambanis dataset. For all weapon types we find a median increase of about 60% in weapon import, and a mean increase of over 1025%.

## Analysis per weapon type

The trade registry contains information about weapon import for many types of military equipment. In an effort to have a more coarse grained analysis, we propose to group the weapon descriptions in multiple sub categories. We identify the following categories, which encompass many entries in our dataset:

- Aircrafts: Any type of aircraft, that could give an idea for the type of investment produced for aerial warfare. Those include transport aircrafts, bomber aircrafts, fighter aircrafts etc.. We exclude helicopters which will have a category of their own.

-Helicopters: Based on the difference in endurance and range with normal planes, we decide to give helicopters a category of their own. Indeed our reasoning is that helicopters might be favored in a context of civil war because they would not need to cover the range achievable by an aeroplane, if it is restricted to the countries borders.

- Guns: We decide to put in this category any form of artillery present in the dataset  with the exception of missiles. Our dataset containing mostly transactions of heavy weaponry this category does not include handguns of firearms. It includes weapons such as towed guns, naval guns or self propelled guns.

-Missiles: The trade registry contains many entries for missiles, all of which are described as Anti-ship or Anti-tank missiles. Those were numerous and specific enough to warrant a category of their own.


-Cars: This category regroups many descriptions which seem to designate the same kind of vehicle. In the trade registry they are described as cars, Armored Cars (ac), or Armed Personnel Carrier (APC). Those all seem to designate some type of armored vehicle for military use.

### Variations in Import for different weapons types

We analysed the variation of import for different types of weapons around periods of civil war onset. We find the following median variations:

-Aircrafts: We see a **decrease** of **21.9%** of import in aircrafts

-Tanks: We see a **decrease** of **81.25%%** of import in tanks

-Helicopters: We see an **increase** of **24.3%** of import in helicopters

-Missiles: We see a **decrease** of **88.8%** of import in Missiles:

-Cars: We see a **decrease** of **-36.4%** of import in Cars

-Guns: We see a **decrease** of **-51%** in Gun import
But these numbers represent the variation in countries who have already imported such weaponry in the 5 years prior. There is often a large number of countries which are first time buyers in 5 years. Out of the 117 countries in our dataframe there are for:

-Aircrafts: 50 first time buyers

-Tanks: 85 first time buyers

-Helicopters: 67 first time buyers

-Missiles: 99 first time buyers

-Cars: 61 first time buyers

-Guns: 83 first time buyers

Of course those results are heavily influenced by the dataset that we use, and it is difficult to conclude anything definitive about the relationship of first time import in a timespan of 5 years and civil war onset.

Furthermore if we throw statistical caution to the wind and have a look at the means values, we get a different result:

-Aircrafts: We see a **increase** of **222%** of import in aircrafts

-Tanks: We see a **increase** of **523%** of import in tanks

-Helicopters: We see an **increase** of **189%** of import in helicopters

-Missiles: We see a **decrease** of **82%** of import in Missiles:

-Cars: We see a **decrease** of **756%** of import in Cars

-Guns: We see a **decrease** of **216%** in Gun import

These results seem to imply that the data is heavily skewed. Let’s have a look at which countries have the biggest variation in imported weapons surrounding a civil war onset event.


## Who is supplying the weapons?
The trade registry contains both information about the recipient and the suppliers. An interesting question would be to see which are the prevalent weapon suppliers for countries in a state of civil war. In this regard we compiled data about the amount of military equipment supplied to countries after a civil war onset, classified by supplier. The figure below presents the top 10 suppliers of military equipment to countries who have had a civil war onset 5 years prior.

{% include top_suppliers.html %}

Keeping in mind that the plot yscale is logarithmic, the soviet union proves to be the clear biggest supplier in our dataset, with over 100 thousand registered pieces of equipment. Next comes France with 54 thousand supplied pieces of equipment, and curiously The United States comes in in third place.


// Compare avec le nombre d'armes vendues au total comparé au cas avec seulement guerres civiles

## Studying the neighbours

After diving in these instruments of destruction transaction registry, we drop our bookkeeper suit, take a step back and consider the permeability of the borders. This is critical as all entities studied in this work are not isolated from each other but share borders with each other. It would be very naive to believe that the effects of these disastrous conflicts don’t spill on the neighbouring countries.

Using a threshold approach with a similar timeframe as earlier and excluding the countries experiencing an onset within the timeframe, we can bring to the light a few trends:
for 6% of the neighbouring countries, the life expectancy decreases by more than 10%.

{% include proportion_neighbors_country_feat.html %}

##OLD, pour se donner une idée

### window of 3, thr of 0.1
- Primary Commodity Exports : 19% increase, 26% decrease (over 380)
- Military power : 35% increase, 13% decrease (over 375)
- GDP Growth : 25% increase, 61% decrease (over 380)
- Infant mortality : 16% increase, 18% decrease (over 380)
- Life expectancy : 0.5% increase, 6% decrease (over 380)
- Weapon import (TIV) : 47% increase, 42% decrease (over 285)

### window of 5, thr of 0.1
- Primary Commodity Exports : 21% increase, 27% decrease (over 380)
- Military power : 49% increase, 19% decrease (over 376)
- GDP Growth : 27% increase, 61% decrease (over 380)
- Infant mortality : 19% increase, 31% decrease (over 380)
- Life expectancy : 1% increase, 8% decrease (over 380)
- Weapon import (TIV) : 51% increase, 38% decrease (over 285)

### window of 5, thr of 1
- Primary Commodity Exports : 3% increase, 0% decrease (over 380)
- Military power : 13% increase, 0% decrease (over 376)
- GDP Growth : 15% increase, 31% decrease (over 380)
- Infant mortality : 4% increase, 0% decrease (over 380)
- Life expectancy : 0% increase, 0% decrease (over 380)
- Weapon import (TIV) : 26% increase, 0% decrease (over 307)

We have a total of 411 countries "neighbour" to a CW onset, from which only 114 are unique (in term of country name)

On a window of 5 years, it seems that the neighbouring countries are greatly affected by the CW onset on the economical aspect : more than 25% of the countries next to countries that witnessed a CW avec a decrease in commodity export and more than 61% of them experience a decrease in their GDP Growth. We can make the hypothesis that the neighbouring country was probably a commercial partner and became unable to maintain their exchanges.

On the military side, it seems that the power of armies increase overtime for almost half of the neighbouring countries. Similar trend can be observed in the import of weapons.

As its name indicate, civil wars implies armed conflicts between parties within a country. Consequently, many of the victims are civilians and it's expected to observe an impact of such conflicts on the Infant mortality and Life Expectancy. With a strict threshold, we can see that in 4% of the countries neighbouring a civil war, the infant mortality increased by more than 10% compared to the period before the onset.
On a window of 6 years around the onset, we can also see that the Life expectancy decrease for 8% of the countries; passing from 54.2 years to 54.6 in average (54.8 to 55 when removing the duplicates)

### Encore un step back et comparé les pays qui ont jamais eu de guerre civile avec les autres

Let’s take an additional step back and split the countries in two groups; those who never experienced a civil war and the others. This separation is of course very rough, and doesn’t take in account the colonialist history, the natural disaster or wars between constitutionally democratic forms of government but let us outline some difference. In order to perform this comparison, we will focus on the most recent data available (1965-2000).

First of all, let’s focus on Life Expectancy again.  As of 2000, a 5 years gap (66.78 versus 61.08 years) lies between the two groups. 35 years earlier, the difference was almost 9 years : despite the civil wars, the countries were able to reduce this difference over time. We could hope that in several decennies, despite the conflicts that might emerge in the meantime, the gap will disappear. This of course depends on many other parameters...

Similar analysis can be performed on...


# Conclusion

Civil War is not necessarily the cause of the variation highlighted in this work but seems to crystallize/indicate unstable regions, susceptible to experience brutal/violent crises.
