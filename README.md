# Venezuela Economic Recovery Simulator 

Repository for a [Tableau Public](https://public.tableau.com/app/discover) and [RShiny](https://shiny.posit.co/) project with pedagocical purposes that simulates the estimated time to recovery for the Venezuelan economy depending on user imput of base year and compound yearly growth rate. Probability of scenario is approximated based on the country's hostrical yearly growth for the period 1830-2024. There is a standard and per capita version of the simulator.

Basic instructions for the simulator:
1. Select a base year that will fix a real gdp reference "target".
2. Select yearly compounding growth rate to calculate how long it takes for the proyected gdp to reach the target.
3. Restrict the reference period to see how (un)common the selected growth rate is when compared to historic yearly gdp growth. 

# Release V.1 (Spanish)

[Tableau Dashboard](https://public.tableau.com/views/Escenariosderecuperacion/Story?:language=es-ES&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

For both standard and per capta (ppc) versions there are the following pages and modules:

1. Yearly real gdp gorwth rate (1830-2024) with historical events for context: See period of expansion and contraction for the Veneuzelan economy, with the 2013-2020 collapse noted as the largest and most severe. 
   
2. Dashboard with simulator:
   
   2.1 Controllers for base year, compunding growth rate, and period selector: Located at the bottom. Period selector only affects histogram.
   
   2.2 Historic GDP index with proyected GDP index from 2024 onwards: Dynamic range based on selected base year and grwth rates: Dynamic extendends period up to the point the proyected GDP passes the target.

   2.3 Histogram of yearly growth rate split by selected compunding growth rate. Histogram of yearly growth rates shown in 2.1, color coded to see if they beat selected growth rate for proyected gdp. Year range can be edited with controller.
   
   2.4 Moving yearly compunding growth rate dynamically adjusted by the length of the "time to recovery estimate". Will calculate the accumulated growth rate for a period of legth matching the time to recovery estimate, calculate the implicit compound yearly growth rate, and compare it to the target growth rate. This in essence sees if there is historicall precedent of Venezuela growing in magnitudes that matches or exceeds its recovery target.
