# Rickaby-Hardware-Analysis
Revenue and Profit Analysis for Rickaby Hardware


*Please check my [Portfolio](https://saco1621.github.io/Conerlious_Datascience_portfolio/) for more projects. *

![](https://i.imgur.com/yRjLhG4.png)

Rickaby hardware is a company which supplies the hardware peripherals to different clients such as nomad stores etc. They have a head office in Mumbai India, and they have different regional offices in different cities of India. Dumisani Sagas is the sales director of this company, and he Is managing the business from the head office. So, what is happening with this company is that sales are declining and Dumisani as a sales director is having a lot of struggle tracking where the business is failing due to the size of the company which is big. When Dumisani calls his reginal mangers asking for information on why the sales are declining, unfortunately, his reginal managers are always giving him fuzzy and unclear information which can help him understand the root cause. In addition to that, they always give him big excel files of all transactions which is very difficult for Dumisani to transform all those excel sheets into insights. However, Dumisani calls for an emergency meeting with the sales director, marketing, customer, data analysis and IT teams. 

##### To come up with a solution, Dumisani and his teams used AIMS grid focusing on four (4) components which are:_

**Purpose**

-	_The purpose is to unlock sales insights that are not visible so that the sales team can use them for decision support and automate them to reduced time spent in data gathering._ 

**Stakeholders & Data Warehousing**

Stakeholders were chosen based on each team's impact towards profit and revenue of the company. To map down stakeholder's impact, i made reference to the company's data warehousing structure. 

![](https://i.imgur.com/YJ2TL32.png)
Depicted form the diagram, stakeholders are:

_-	Sales Director._

_-	Marketing Team._

_-	Customer Service Team._

_-	Data miners and Analysis team._

_-	IT team (Software Engineers). _

**Result (what do we aim at the end of this project?)**

-	_An automated dashboard providing quick and latest sales insights to support data driven decision making._ 

**Success criteria (should be able to measure success of the project.)**

-	_Dashboards uncovering sales order insights with latest data available._
-	_Sales team able to take better decisions and prove 10% cost savings of total amount spent._ 
-	_Sales analysts stop data gathering manually to save 20% of their business time and reinvest in value added activity._ 

##### Tools to be used

Due to the amount of data available, Dumisani wants his analysis team use the following tools. 

#####  _SQL_

- _MySQL was used for ETL, aggregation and Analysis. This is so because it was easier for the team because the datasets contain a huge amounts of data which will be tidious to clean it using excel_

#####  _Tableau_

- _To share insights with stakeholders, Tableau was used. _

#### Deliverables

**Dumisani asked the data analysis team to come up with the following:**

+ Revenue breakdown by cities.

+ Revenue breakdown by years and months.

+ Show top 5 customers by revenue and sales quantity.

+ Top 5 products by revenue number.

_NB) He wants a visualized version of Revenue and Profit Analysis dashboard where he can click on different regions._

To perform the analysis, i used a [Dataset](https://github.com/codebasics/DataAnalysisProjects/tree/master/2_SalesInsightsTableau) from GitHub.This dataset has 5 tables which are:

+ Customers

+ Products

+ Transactions

+ Markets(Cities)

+ Date

### Data Modeling.

To model the data, i used a star schema whereby transactions table will the fact table referencing  the other 4 dimension tables. See the diagram below showing the relationship between all the tables. 

![](https://i.imgur.com/08UF0qT.png)

**Transactions Join with Customer table**
```{r cars}
# SELECT customer_code From Customers INNER JOIN Transactions ON Cusomers.customer_code = Transactions.customer_code
```

**Transactions Join with Products table**
```{r}
# SELECT product_code From Products INNER JOIN Transactions ON Products.product_code = Transactions.product_code
```

**Transactions Join with Markets table**
```{r}
# SELECT market_code From Markets INNER JOIN Transactions ON Markets.market_code = Transactions.market_code
```

**Transactions Join with Date table**
```{r}
# SELECT order_date From Date INNER JOIN Transactions ON Date.order_date = Transactions.order_date
```

##### Date Modeling Results


![](https://i.imgur.com/F0BjwRJ.png)

####  Revenue breakdown by cities.


![](https://i.imgur.com/YkjlOvJ.png)

####  Revenue breakdown by years and months.


![](https://i.imgur.com/Wsyw2Bl.png)

####  Show top 5 customers by revenue and sales quantity.


![](https://i.imgur.com/xSF2mCx.png)

####  Top 5 products by revenue number.

![](https://i.imgur.com/z7vUFBW.png)



## Revenue Analysis Dashboard 

For interactive experience use this link to [Revenue Analysis dashboard](https://dub01.online.tableau.com/#/site/rickabyhardwareworkbook/views/Rickaby_hardware_workbook/Dashboard1?:iid=1) 

![](https://i.imgur.com/UHxfNMf.png)

## Profit Analysis Dashboard 

For interactive experience use this link to [Profit Analysis dashboard](https://dub01.online.tableau.com/#/site/rickabyhardwareworkbook/views/RickabyhardwareProfitAnalysis/ProfitAnalysis?:iid=1) 


![](https://i.imgur.com/tq6V2oh.png)

#    I hope you enjoyed Thank You!
