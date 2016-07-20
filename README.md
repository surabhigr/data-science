# Exploring Data Science

in layman's terms, **data science** is a pretty combination and permutations of statistical analysis, fancy yet meaningful visualisations, machine learning and all types of research on data (mining/crawling, processing, etc).

A data science task consists of deployment instructions, analytics, data-metrics and more!

### Aspects Covered:
  - Trends
  - Visualisation
  - Data points




### Solutions:

* Finding Platform specific users:

```
SELECT  `platform` , COUNT(  `visits` )  AS  `platform_specific_visits` 
FROM  `analytics` 
GROUP BY  `platform` 
ORDER BY  `platform_specific_visits` DESC;
```

* Finding Orders placed in each months

  - Surprisingly there're no orders placed in March, April and May month.
  - Highest orders in December being Christmast and the lowest orders placed during July month.
  - Average orders are 2340 per month (excluding draught months)

```
SELECT  MONTH(`day`) AS Month , COUNT(  `orders` )  AS  `Orders_placed` 
FROM  `analytics` 
GROUP BY  MONTH(`day`)
ORDER BY  `Orders_placed` DESC;
```

**Declaimer**: I will make this solution private once the interview process is over or by a week whichever is earliest to maintain the privacy of the data given.





