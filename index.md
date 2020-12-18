---
layout: default
---

# Introduction

A civil war is typically caused by a combination of complex factors and its effects are usually long-lasting. But does it only impact its country of origin? How do the dynamics of economical and societal metrics evolve surrounding these onsets? Does a state equip itself in suspicion of civil conflict? And what countries are the biggest export of weaponry ? These are some of the questions we will answer here.

In their [publication](https://www.cambridge.org/core/journals/political-analysis/article/abs/comparing-random-forest-with-logistic-regression-for-predicting-classimbalanced-civil-war-onset-data/109E1511378A38BB4B41F721E6017FB1), Muchlinski, Siroky, et al. seeked to predict the onset of a civil war using two different techniques : logarithmic regressions and Random Forests. While the logistic regression is widely used to develop models with binary outcomes, the use of Random Forests was original and allowed the researchers to identify features with a strong predictive power.
These metrics were for the most already considered relevant in the literature (GDP growth, Education level etc.) as explanatory variables. This data story presents itself as an extension of this paper and aims at understanding and visualizing trends in these pertinent features.

But first, what is a civil war? The dataset used comes from [Sambanis](https://web.sas.upenn.edu/sambanis/) which defines a civil war as an armed conflict, in which the government is one of the combatants, in a state recognized internationally with a population of at least half a million. The onset is declared as the year in which there are at least 500 deaths as long as there are 1000 deaths over the next three years.

Let us have a quick look at the dataset. In the map below, you can see the 117 CW onset taking place in 72 different countries. Some countries have been stricken multiple times in this dataset which ranges from 1945 to 2000. The bar plot below displays

{% include world_map_CW_over_years.html %}

{% include geographic_repartition.html %}



# How is a country impacted by civil war?

First of all, we are going to study the long lasting effects of a Civil War; how long does it take for a country to recover the values it was at for specific metrics before an onset?

{% include recovery_years_histo.html %}


Fortunately, it seems like infant mortality (death of a baby under the age of one year old), despite being affected on the year of the onset, usually recovers in less than a year. We found out that some countries never fully recovered in the time frame at hand from which the vast majority are located in Africa with conflicts that occurred in the 80s or 90s such as : Algeria (1991), Central African Republic (1996), Djibouti (1991), Haiti (1991), Mozambique (1976), South Africa (1976) and the Democratic Republic of the Congo (1991).

On the other side, the life expectancy at birth seems to take much longer to recover in several countries. Concerning the countries that did not recover before 2000, three of the conflicts occured beyond 1990 (Burundi, Central African Republic and Kenya), leaving very little time for recuperation. Civil Wars that took over ten years to recover on this aspect are Colombia (1949-1958, **El Bogotazo**), Iraq (1959-1959 **Mosul Uprising** and 1961-1970 **First Iraqi–Kurdish War**) and the Republic of Vietnam (1960-1975 **Vietnam War**).

If we focus our attention on economical factors, we can see that they are considerably more sensitive and the recovery periods spread out more. The **GDP growth**, the holy indicator of a country's economy and development health in a capitalist world, takes in average three years to return to the value observed around the civil war onset. If we take for example the three countries that took more than fifteen years to recover, we have China, who, because of the **Cultural Revolution** started in 1966, took eighteen years before experiencing a GDP growth greater than 0.14%. Similar observation for Iraq, which took eighteen years as well to retrieve a GDP growth greater than 0.16%. Finally, Vietnam had to wait the end of the Vietnam War, 16 years later, during which the GDP growth remained below 0.001%.

Countries with high Primary Commodity Export (to which Oil belongs) were reported as likely to experience civil war according to Collier and Hoeffler, two political science researchers. Even if their conclusion is [disputed](https://web.stanford.edu/group/fearon-research/cgi-bin/wordpress/wp-content/uploads/2013/10/Primary-Commodity-Exports-and-Civil-War.pdf), we are curious to see how this division of a country’s exportation is impacted. It appears that it takes on average a little bit more than 5 years to return to “normal” levels : longer than the GDP growth! We must however consider the fact that twenty-eight countries, almost half of the countries experiencing civil war (seventy-two), were not able to revert to their original export level.

We now narrow the study to countries possessing oil on their territory (34, for 16 onsets), a slightly different trend appears : the average is now 8 years, with a median at 4 years. It’s important to outline that Indonesia accounts for almost half of the onsets in this subset, with repressions of Communist movements (1949, 1963) and Darul Islamism (1949), as well as regional independence suppression (1950, 1956, 1963, 1975).

{% include recovery_years_histo_oil.html %}

We will switch to a more global approach and take a look at the trends across all the onsets across the world. To do so, we will compute the proportion of countries which saw a noticeable change between the three years preceding the conflict and the three following  years (year of the onset included). Feel free to select a threshold and see the proportion of countries which experienced a variation greater than the value selectionned! (NB: if data is missing, the onset is excluded from the analysis in order to limit biais).

{% include proportion_country_feat.html %}

We would like to draw your attention to the fact that depending on the variable considered, an increase should not necessarily be perceived as a deterioration and vice-versa (GDP growth good, infant mortality raise bad).

By using a threshold of 5%, it becomes evident that for 20% of onsets, the country experiences a diminution of the life expectancy at birth. It corresponds to approximately XX years.

A threshold of 10%, i.e. a before/after variation of at least 10%, let us observe trends for several features:
- The infant mortality increases for over 30% of the onsets. As mentioned above, this indicator tends to rapidly recover but the effects of the conflict are devastating on the year of the onset. Likely to be bound to the definition of the infant mortality itself as it accounts for the mortality for babies under 1 year.
- The primary commodity export decrease in approximately 70% of the onsets; this domain seems to almost systematically suffer from the conflict and we could explain it by the disruption of the transports, social and economic instabilities or increased border control/borders closing.
- The military power, measured as the share of the population enrolled in military forces, also increases for over half of the countries. When choosing a threshold of 200%, i.e. a doubling of the militarised population, a few onsets remains : 1988 Burundi (Tutsi Genocide), 1982 Nicaragua (Cold-War proxy, revolution), 1966 Nigeria (succession of military coups), 1984 Zimbabwe (Ndebele genocide).
- Weapon imports, measured as TIV units by the [SIPRI](https://www.sipri.org/databases/armstransfers/background) (Stockholm International Peace Research Institute), increases for 40% of the onsets while it decreases for 28% of the onsets. These military equipment fluxes take in consideration the quality/grade of the material (new, refurbished, used, …) and cover illegal transactions as well.

{% include lebanon_evolution.html %}
{% include indonesia_evolution.html %}
{% include argentina_evolution.html %}
{% include burundi_evolution.html %}

To better visualize the impact of civil war on different indicators over time 4 countries, on 4 different continents, were selected. For each one of them, a drop in GDP close to each civil war onset is visible but also additional trends such as increases in illiteracy for XXX, increase in infant mortality for YYY and or decrease in ZZZ for WWW,


As one can observe, the influx of military equipment does increase around the civil war onsets. Based on the SIPRI dataset, it is possible to analyse the transaction for heavy equipment such as planes, tanks and missiles.

# Weapon trade surrounding civil war onset

By combining the Sambanis civil war dataset and the weapon trade registry, we analyzed the trends in weapon import during years surrounding a civil war onset. We hope to find certain trends in weapon imports, either by type, or by exporting nations.

We look at the variation in the number of weapon imports for a fixed number of years before, and after the civil war onset for each event in the sambanis dataset. For all weapon types we find a median increase of about 60% in weapon import, and a mean increase of over 1025%.

## Analysis per weapon type

The trade registry contains information about weapon import for many types of military equipment. In an effort to have a more coarse grained analysis, we propose to group the weapon descriptions in multiple sub categories. We identify the following categories, which encompass many entries in our dataset:

- Aircrafts: Any type of aircraft, that could give an idea for the type of investment produced for aerial warfare. Those include transport aircrafts, bomber aircrafts, fighter aircrafts etc.. We exclude helicopters which will have a category of their own.

-Helicopters: Based on the difference in endurance and range with normal planes, we decide to give helicopters a category of their own. Indeed our reasoning is that helicopters might be favored in a context of civil war because they would not need to cover the range achievable by an aeroplane, if it is restricted to the countries borders.

- Guns: We decide to put in this category any form of artillery present in the dataset  with the exception of missiles. Our dataset containing mostly transactions of heavy weaponry this category does not include handguns of firearms. It includes weapons such as towed guns, naval guns or self propelled guns.

-Missiles: The trade registry contains many entries for missiles, all of which are described as Anti-ship or Anti-tank missiles. Those were numerous and specific enough to warrant a category of their own.


-Cars: This category regroups many descriptions which seem to designate the same kind of vehicle. In the trade registry they are described as cars, Armored Cars (ac), or Armed Personnel Carrier (APC). Those all seem to designate some type of armored vehicle for military use.

### Variations in Import for different weapons types

We analysed the variation of import for different types of weapons around periods of 5 years surrounding a civil war onset. We looked at the number of imports from both sides of an onset and derived the following results:

| Type                                            | Aircraft | Helicopter | Guns  | Missile | Tank  | Cars  |
|-------------------------------------------------|----------|------------|-------|---------|-------|-------|
| Global variation                                | +64%     | +55%       | +173% | +219%   | -34%  | +120% |
| # of first time buyers after onset (out of 117) | 50       | 67         | 83    | 99      | 85    | 61    |
| Median variation for  recurrent buyers          | -21%     | +24%       | -51%  | -89%    | -81%  | -36%  |
| Mean variation for  recurrent buyers            | +222%    | +523%      | +189% | +82%     | +757% | +150% |


We find an overall positive global variation. Regardless of weapon type there is an increase of 60% in weapon import from countries after a civil war onset. Aside from tanks, all weapons have a net positive variation across all of the civil war dataset. But this is not very telling and we would like to look at the median variation for each type.

 However there are some countries For which there are no import entries for certain types of weaponry in the years leading to the onset. The reasons could be very diverse but perhaps it could indicate some types of weapons that are rather obtained on a short notice in case of a war onset. For instance for Missiles there are 99 cases where the country did not obtain any in the years leading to the onset, while aircrafts and cars are the categories with the least amount of first time buyers, perhaps because they are more versatile.

The median variations of each category for recurrent buyers are mostly negative, with the exception of helicopter import. What could be the reason for such a trend ? First of all, if the concerned countries have already imported weaponry in the years leading to the onset, it could be that they already have a stockpile. Interestingly enough the median variation of import of helicopters is positive. An interesting hypothesis would be that helicopters could be more useful than aircrafts in a civil war situation, given their superior endurance at the cost of range, which would not be such an important factor in a conflict inside the country's territory.

However if we have a look at the means values, we get different results: The mean variation for every recurrent buyer is positively large for every category. It seems that the data is heavily skewed by some specific civil war events. We propose to visualize the events with the largest import variation for each category.

{% include Cuba_top_tank.html %}

The onset event in Cuba in 1958 sees the highest variation in tanks import in our dataset. The year suggests that this weapon import is linked to the cuban revolution. It is documented that during this conflict, the United States supplied Cuba with planes, ships and tanks, which was used against the rebels (Ernesto "Che" Guevara (World Leaders Past & Present), by Douglas Kellner, 1989, Chelsea House Publishers).

{% include Argentina_top_air.html %}



Argentina saw the biggest increase in aircraft orders in 1955. Those imports seem to occur in the years following the Revolución Libertadora coup d’état which employed the use of air bombardements by Air Force loyalists.


{% include Cambodia_top_helico.html %}


Cambodia got supplied with new helicopters during the years after 1970. Those were the years of the Cambodian campaign, which was a part of the Vietnam War


## Who is supplying the weapons?

The trade registry contains both information about the recipient and the suppliers. An interesting question would be to see which are the prevalent weapon suppliers for countries in a state of civil war. In this regard we compiled data about the amount of military equipment supplied to countries after a civil war onset, classified by supplier. The figure below presents the top 10 suppliers of military equipment to countries who have had a civil war onset 5 years prior.


{% include top_suppliers.html %}

Keeping in mind that the plot yscale is logarithmic, the soviet union proves to be the clear biggest supplier in our dataset, with over 50 thousand registered pieces of equipment. Next comes the  United States just shy of 40 thousand supplied pieces of equipment. Russia, which should be a relatively young nation in our dataset with entries only appearing after the fall of the soviet union, is third in our dataset, followed by France.


However we must remember that these supplies concern only transactions with countries in a state of civil war. Comparing the number of weapons sold in a context of civil war compared to the total supply in weapons paints a different picture.

{% include total_suppliers.html %}


By looking at the total number of weapon supplies we see a slightly altered ordering of those countries. We find that the United States is still second only to the Soviet Union. However the proportion of weapons dealt to countries associated with civil war is considerably smaller. France which was 4th in number of weapon supply to countries associated with civil war is now third. We understand how Russia managed to get third in the plot from above. An unusually large part of its weapon supply is associated with civil war. This pushes us to ponder on the question about which country is the most involved with civil war in its weapon trade.


{% include supply_ratio.html %}



{% include big_investors.html %}

From those two plots above we can see the countries with the biggest ratio of weapon supply associated with civil war compared to the rest of weapon trade for this given country. Sudan is in first place although it has only 3 recorded interactions. We can see that Russia is in both the top 10 countries in sheer number of weapons supply but also in the top 10 of countries with the biggest relative supply in weapons for civil war.

## Studying the neighbours

After diving in these instruments of destruction transaction registry, we drop our bookkeeper suit, take a step back and consider the permeability of the borders. This is critical as all entities studied in this work are not isolated from each other but share borders with each other. It would be very naive to believe that the effects of these disastrous conflicts don’t spill on the neighbouring countries.

Using a threshold approach with a similar timeframe as earlier, we study the neighbours of all the countries experiencing a civil war. We, of course, exclude the countries going through  a civil war themself to avoid biais. By doing so, we noticed a civil war hot-spot in Asia, in both 1948 with Myanmar (Ethnic war), India (Myanmar independences from India), China (Nationalist versus Communists clashes in China, Taiwainese dissidents) and 1968 with India (Repression of Naxalites), China (Mao Zedong’s Cultural Revolution), Myanmar and Thailand (Communist insurgencies), Bangladesh and Pakistan (Ethnic war, Bengali independence).

Nevertheless, when using a threshold of variation equal to 50%, we notice some very faint trends:
40% of Civil War neighbouring countries see their GDP decrease while 30% maintenant a positive growth. As these proportions cover a period of 50 years with actors dispatched across the world, it is difficult to be assertive but one could say that not every civil war has an impact on the neighbouring countries, would it be by their nature or dispositions taken by the adjacent countries.
Enrollment of the population in the military also displays something interesting; an almost perfect symmetry can be observed between the proportions of countries with increasing (28%) and decreasing (26%) military power.

For these two indicators, the variations are quite extreme; we are talking about a 50% increase from the mean of the 3 years preceding the onset of the conflict in a neighbouring country. By setting the threshold to 200%, we can see that 10% of the onsets neighbours are doubling their militarised population.

In order to differentiate the effect of civil wars to the one of international wars, we performed a similar analysis on all the countries with a neighbour at war, to see if the trends were similar.

Unfortunately, these results do not take in account the duration of civil wars and the onsets of international conflicts. Despite our best effort and the amazing resources available on the website Systemic Peace, as the beginning and ending of conflicts are not always clearly defined, it is pretty much impossible to manually correct the mismatches.

## Another step back; does a Civil War experience make you different/how marking is it/What are Civil War scars?

Let’s take an additional step back and split the countries in two groups; those who never experienced a civil war and the others. This separation is of course very rough, and doesn’t take in account the colonialist history, the natural disaster or wars between constitutionally democratic forms of government but let us outline some difference. In order to perform this comparison, we will focus on the most recent data available (1965-2000).

For one last time, let’s focus on Life Expectancy again. As of 2000, a 5 years gap (66.78 versus 61.08 years) lies between the two groups. 35 years earlier, the difference was almost 9 years : despite the civil wars, the countries were able to reduce this difference over time. We could hope that in several decades, despite the conflicts that might emerge in the meantime, the gap will disappear. This of course depends on many other parameters...

{% include life_expectancy_CW_no_CW.html %}

When put in contrast with the average life expectancy and number of civil onsets per region, we can even observe that between 1965 and 1990, the ranking of the regions by longest life expectancy is the exact opposite of the ranking by the number of civil war onsets. In 1990, with the dismantlement of the URSS, many independances wars broke out as well as numerous ethnic violences. These conflicts induce a considerable drop in the Eastern Europe life expectancy and make this region fall behind Latin America, Middle East and North Africa as well as South & East Asia and Ocenia.

# Conclusion

Civil War is not necessarily the cause of the variation highlighted in this work but seems to crystallize/indicate unstable regions, susceptible to experience brutal/violent crises.

A very limiting factor for such geopolitical studies is the robustness and extensivity of the measures; probably because of the considerable time frame covered (1950-2000) by the datasets used here, many values are either missing or not measured frequently (with the reuse of the last known measure). In addition to that, countries and borders are not static, particularly during the period covered with the fall of colonialism empires, independances wars and dissolution of the URSS. Altogether, these changements interfere with the analysis.
