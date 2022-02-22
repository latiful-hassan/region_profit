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

- To increase granularity of this viz without losing the level of aggregation I will create a **Level of Detail (LOD) Calculation**
**LOD Include** calculated field with formula: {INCLUDE [City] : SUM([Profit])}

- The follow maps show with and without the LOD Include calculation, the one with LOD averages at the city level instead of item:

![](https://github.com/latiful-hassan/region_profit/blob/main/region_profit_screenshots/lod_include.png)

- Now to find the proportion that each city ocntributed to the profit for its respective state we can use **LOD Exclude**: {EXCLUDE [City]: SUM([Profit])}

![](https://github.com/latiful-hassan/region_profit/blob/main/region_profit_screenshots/lod_exclude.png)

- Finally, here is both maps combined:

![](https://github.com/latiful-hassan/region_profit/blob/main/region_profit_screenshots/region_profit_map.png)
