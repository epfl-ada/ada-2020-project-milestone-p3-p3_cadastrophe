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

Analysis :
On a window of 5 years, it seems that the neighbouring countries are greatly affected by the CW onset on the economical aspect : more than 25% of the countries next to countries that witnessed a CW avec a decrease in commodity export and more than 61% of them experience a decrease in their GDP Growth. We can make the hypothesis that the neighbouring country was probably a commercial partner and became unable to maintain their exchanges.

On the military side, it seems that the power of armies increase overtime for almost half of the neighbouring countries. Similar trend can be observed in the import of weapons.

As its name indicate, civil wars implies armed conflicts between parties within a country. Consequently, many of the victims are civilians and it's expected to observe an impact of such conflicts on the Infant mortality and Life Expectancy. With a strict threshold, we can see that in 4% of the countries neighbouring a civil war, the infant mortality increased by more than 10% compared to the period before the onset.
On a window of 6 years around the onset, we can also see that the Life expectancy decrease for 8% of the countries; passing from 54.2 years to 54.6 in average (54.8 to 55 when removing the duplicates)

On a higher level, if we compare the Life Expectancy of countries that never experienced a civil war onset versus those that experienced one in 2000 for example, we notice a 5 years difference (66.78 versus 61.08 years). 

Similar analysis

## Regional vizualization of civil war onsets

TODO :
- aggregate information (focus south america or middle east)
- plot magic