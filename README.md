# region_profit
**Context**

- Re-create the visual that is displayed in *region_profit_challenge*

**Task**

- Create the viz where state colors represent the average profit across the state
- Circle colours and sizes reflect the percent contribution of the respective city towards the overall profit of the state

**Techniques & Process**

- Combined *ListOfOrders* and *OrderBreakdown* with an **Inner Join**
- Created a **Hierarchy** named *Geography*
- Baseline viz:

![](https://github.com/latiful-hassan/region_profit/blob/main/region_profit_screenshots/baseline_viz.png)

- To increase granularity of this viz without losing the level of aggregation I will craete a **Level of Detail (LOD) Calculation**
**LOD Include** calculated field with formula: 
<br/>
{INCLUDE [City] : SUM([Profit])}

- The follow maps show with and without the LOD include calculation, the one with LOD averages at the city level instead of item:

![](https://github.com/latiful-hassan/region_profit/blob/main/region_profit_screenshots/lod_include.png)

- The map below is using **LOD Exclude** to show the proportion that each city contrubuted to profit of that state:

![]()

**Analysis & Insights**

-
