1. *Title*

    Civil War: how does this disastrous event affect a country and its neighbours? An analysis of the impact on the international military material trade and other economical and social factors.

2. *Abstract*

    A civil war is typically caused by a combination of complex factors and its effects are usually long-lasting. But does it only impact its country of origin? In this project, we would like to analyze the particular economic and societal dynamics in a country stricken by civil war, and in its neighbors. More specifically, we aim to determine if and how a country might react to an impending threat of civil war, for instance by importing military materials. Furthermore, do neighboring countries see such events as a threat and feel the need to protect themselves as well? To do so, we will use several SIPRI datasets, on international weapon trade. Additionally, we will also analyze the recovery time of the countries affected directly or indirectly by these conflicts for several economic and social factors, such as education or GDP per capita as those features might not be affected similarly. This study could highlight sectors particularly sensitive to civil war onset, which could constitute high priority targets for NGOs.

3. *Research Questions*

*   What is the impact of the civil war onset on the economic and social metrics of a country and their neighbouring countries?
*   What about the arm trade surrounding these war onsets?
*   What are the effects of the civil war on a regional level: are there civil wars “hot spots”?
    * Are their effects cumulative if a country shares borders with several countries experiencing civil war simultaneously ?
    * Are some countries able to “permeabilize” their border and minimize the impact of the nearby ongoing conflicts?
    
*Dropped Research Question*
*   If the weapon trade presents interessant trends, add it to prediction models and see if the accuracy is improved : lack of time, wasn't integrating well to the data story
    
4. *Datasets exploited*

*   SambnisImp.csv dataset used in the original paper
    *   1945-2000
    *   civil war year onset : before/during/after analysis
    *   yearly metrics per country : assess the impact of the civil war (and the eventual relation with the onset predictive power)
*   GeoData Country-borders.csv
    *   last update in dec 2019
    *   pair of countries with common border, used to aggregate the metrics by neighbouring countries (around country experiencing the civil war)
    *   https://github.com/geodatasource/country-borders/blob/master/GEODATASOURCE-COUNTRY-BORDERS.CSV
*   SIPRI TIV tables
    *   1950-2000
    *   arbitrary unit (trend-indicator value, TIV)
    *   import/export per country and year of military material (include illegal transfert)
    *   Might be “convertible” to a monetary value but mostly used as indication of the flux intensity/fluctuation
    *   https://armstrade.sipri.org/armstrade/page/values.php
*   SIPRI Arms Transfers Database
    *   1950-2000
    *   weapon description of deliveries between countries with the order & delivery years. No monetary value information.
    *   https://armstrade.sipri.org/armstrade/page/trade_register.php
*   SIPRI Milex data
    *   1949-2019
    *   Military expenditure by country per year as % of government spending : highlight change of resources allocation (among expression of the government military expenditure)
    *   https://www.sipri.org/databases/milex
*   Systemic peace dataset
    *   1945-2019
    *   intra & inter states conflicts localization (country), start-end year, number of casualties : used to reinforce the analysis of the civil war impact on the metrics, possible interferences
    *   http://www.systemicpeace.org/warlist/warlist.htm

5. *Methods*

*   Processing of the additional datasets
    *   add a TIV column to the Sambanis dataset using the year and country name (obtainable using the COW_code)
    *   add a military expenditures column using the same variables (year & country)
    *   using the geodata, compute the average of some metrics (for example illiteracy, GPD, happiness…) for the neighbouring country of each country (if necessary, just focus on the countries that experience civil war at some point)
*   For each civil war onset, analyse metrics for neighbouring countries
    *   See if trends appear before, during or after the civil war onset. for example, how long does it take for a country experiencing civil war to restore its Education/GDP to the level it was at before the onset
    *   How badly is the neighbour country GDP affected?
*   Repeat with the weapons importation:
    *   Are the governments “sensing civil war coming” and preparing for it? 
    *   Are neighbouring countries buying weapons to protect their border from the “civil war”?
    *   How long does it take to establish the weapon influx to the “baseline” level
*   Visualize everything on a map, observe per region, civil war co-occurrence or series

6. *Proposed timeline*

<table>
  <tr>
   <td>
30 Nov
   </td>
   <td>Obtain & merge the datasets, wrangle the data
   </td>
  </tr>
  <tr>
   <td>4 Dec
   </td>
   <td>Explore the data under the light of our research questions
<ul>

<li>treat each civil war, aggregate the data around the neighbouring country (might be common to several war)

<li>treat the “other” war, see if there are overlap or interaction between these events that could “interfere” (to make our analysis more robust)
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>9 Dec
   </td>
   <td>Perform statistical tests to show if the civil war onset might explain the fluctuations of the metrics (#p value hacking)
   </td>
  </tr>
  <tr>
   <td>15 Dec
   </td>
   <td>Use visualization tool to plot the map and display values per region, with a widget to change country/metric
<p>
Start working on the video
   </td>
  </tr>
  <tr>
   <td>18 Dec
   </td>
   <td>Finalize the website + the video
   </td>
  </tr>
</table>

7. *Member contribution*

* Cindy : 
    * cowcode datasets import
    * dynamic plotting functions
    * data story website creation and maintenance
    * data story (countries & neighbours) writing
    * methodologie and thoroughness advisor
* Theophile :
    * trade registry analysis
    * trade registry related plotting
    * trade registry related data story writing
* Antoine :
    * tiv tables, trade registry, military expenses, geodata and systemic peace datasets import (#data crawling)
    * preliminary data analysis
    * helper functions
    * data story draft for onset effects on countries and neighbours
