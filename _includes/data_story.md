## Introduction

In a publication ..., Hegre and XXX tried to predict the onset of civil wars using two different techniques : logarithmic regressions and Random Forests. While the logistic regression are widely used to developed model with binary outcomes, the use of Random Forests was original and allowed the researchers to identify features/values/metrics with a strong predictive power.

These metrics were for the most already widely discussed/covered in the literature (GDP Growth, ...) a few of them were unexpected such as the roughness of the landscape or the XXX.

Since variations in these domains allowed the algorithm to perform accurate predictions, we wanted to study these trends

## Findings

- A
- B
- C

Surprisingly... Limitations (data filling with previous year, heavy weapons...)...

## Impact of the civil war on the country

To study the impact of the onset, the average over the 5 years preceding the onset was compared to the average over the 5 years after the onset (included). In data was missing for one of these year, the onset was excluded from the analysis.

[PEUT ÊTRE MIEUX DE FAIRE ANNEE AVANT + ANNEE ONSET + ANNEE APRES ONSET COMPAREE AU 3 ANS Ä PARTIR DE 4 ANS AVANT LE ONSET. POUR FAIRE COMME SI L'ANNEE QUI PRECEDE L'ONSET EST DEJA IMPACTEE PAR L'ONSET?]

### The GDP growth
- 21% (14 onsets) were followed by a position variation of the GDP growth > than 1
- 12% positive variation > than 2.

- 28% (19) were followed by a negative variation of the GDP growth greater than 1.
- 15% (10) negative variation > than 2.

### GDP per Capita
- 37% (25, window of 5 years) decrease > 0.1
- 34% (23, window of 5 years) increase > 0.1

### Military power
- 7% (5) positive increase > 2 -> 1988 Burundi, 1982 Nicaragua, 1966 Nigeria, 1984 Zimbabwe
- 18% (12) positive increase > 1
- 31% (21) positive increase > 0.5

### Life expectancy
- 0% (over 67) positive increase > 0.2 (peut-être à comparer avec la moyenne générale au fil des années?)
- 13% (9) negative variation > 0.1 -> 1991 Burundi, Indonesia, Iraq, Loas, Liberia, Rwanda, Sudan, Vietnam, Yemen

- 20% (20, window of 2 years) negative variation > 0.05
- 6% (6, window of 2 years) positive variation > 0.05

- 27% (26, window of 2 years) negative variation > 0.02
- 27% (26, window of 2 years) positive variation > 0.02

### Infant mortality

- 31% (30, window of 2 years) positive variation > 0.1
- 10% (10, window of 2 years) negative variation > 0.1

- 27% (37, window of 5 years) positive variation > 0.1
- 30% (20, window of 5 years) negative variation > 0.1

### Primary Commodity Exports

- 18% (18, window of 2 years) positive variation > 0.02
- 79% (77, window of 2 years) negative variation > 0.02

- 28% (19, window of 5 years) positive variation > 0.02
- 67% (45, window of 5 years) negative variation > 0.02

- 13% (12, window of 3 years) positive variation > 0.1
- 71% (66, window of 3 years) negative variation > 0.1

[...]

### Weapon import (TIV)

- 35% (34, window of 2 years) positive variation > 0.1
- 22% (22, window of 2 years) negative variation > 0.1

- 40% (37, window of 3 years) positive variation > 0.1
- 28% (26, window of 3 years) negative variation > 0.1

As we can observe, the influx of military equipment does increase around the civil war onsets. Based on the dataset found on the SIPRI website, it possible to analyse the transaction for heavy equipment such as planes, tanks and missiles.

## Who is supplying the weapons?

TODO :
- analyse the trade registry dataset
- analyse the TIV export of the countries mentioned in the trade registry (matching the studied CW)

[...]

In regions such as ...(Sub-Saharan Africa? Middle East?) where the frequency of civil war is considerably higher compared to other regions in the world, we wondered if the onset of a civil war in a country could destabilize its neighbours and lead to other civil wars by domino effect.

## Clashes Splashes - permeable borders

TODO :
- aggregate using geodata
- computage average/median before and after (using time windows) for each neighbour
- look for variation, trends...

## Regional vizualization of civil war onsets

TODO :
- aggregate information
- plot magic