# Exploring Data Science

in layman's terms, **data science** is a pretty combination and permutations of statistical analysis, fancy yet meaningful visualisations, machine learning and all types of research on data (mining/crawling, processing, etc).

A data science task consists of deployment instructions, analytics, data-metrics and more!


**Note:**  Please go through sub-directories to see numbers and graphs! Apologies that I followed curiosity about git and not created PDF.

### Aspects Covered:
  - Trends
  - Visualisation
  - Data points

### Solutions:

* **Finding Platform specific users**:

  - There're more mobile users, iOS being first and Android being second.
  - In Laptop/Desktop platform, Windows is leading, making MacOS 1st runner up and Linux as the second.
  - There're around ~400 visits by unknown devices (could be a Bot requests containing no UserAgent)
  - SymbianOS is the list used.


 - Solution
```
SELECT  `platform` , COUNT(  `visits` )  AS  `platform_specific_visits` 
FROM  `analytics` 
GROUP BY  `platform` 
ORDER BY  `platform_specific_visits` DESC;
```

* **Finding Orders placed in each months**

  - Surprisingly there're no orders placed in March, April and May month.
  - Highest orders in December being Christmast and the lowest orders placed during July month.
  - Average orders are 2340 per month (excluding draught months)

 - Solution
```
SELECT  MONTH(`day`) AS Month , COUNT(  `orders` )  AS  `Orders_placed` 
FROM  `analytics` 
GROUP BY  MONTH(`day`)
ORDER BY  `Orders_placed` DESC;
```


* **Finding Orders placed in each site**

  - Acme leaves behind others, it's leading in sales (1172356 orders in a year, not bad)!
  - Meadian of the orders is 39306.5.
  - There're 1313764 total orders made in 2013.

 - Solution
```
SELECT  site, SUM(  `orders` )  AS  `Orders_placed` 
FROM  `analytics` 
GROUP BY  site
ORDER BY  `Orders_placed` DESC;
```


* **Finding Total Sales made by sites during 2013**

  - Acme is leading in sales doing sales of 168million, whereas Botly is least profiting doing sales of 981 grands!
  - Total sales made by 6 sites is 189,196,951.

 - Solution
```
SELECT  site, SUM(`gross_sales`)  AS  `Sales` 
FROM  `analytics` 
GROUP BY  site
ORDER BY  `Sales` DESC;
```

**Surprising Facts**

* I've worked on this in 3 hours of seating. 

**Declaimer**: I will make this solution private once the interview process is over or by a week whichever is earliest to maintain the privacy of the data given.






