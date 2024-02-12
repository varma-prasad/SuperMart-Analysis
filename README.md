# SuperMart-Analysis

## Table of Contents

  * [Overview](#overview)
  * [Problem Statement by Marketing Manageer](#marketing-manager)\
    	* [SQL](#sql-output)\
    	* [Power BI](#power-bi-report)
  * [Problem Statement by SupplyChain Manageer](#supplychain-manager)


### Overview

   * The DataBase has details of the sales transaction of the SuperMart.
   * All the details is distributed across these tables Customer, Product and Sales.
   * Customer table has all the relevant information about customer and similary product table is aout product details. 
   * Slaes table has all the transaction details and it is linked with customer and product tables with the Foreign keys.
   * With the help of Analytical tools, Solve problem statements and help the stakeholders involved in the business to make strategic decisions backed by the Data.
 
 The Data Model of the SuperMart Database is as follows:

![MixCollage-12-Feb-2024-08-51-PM-4040](https://github.com/varma-prasad/SuperMart-Analysis/assets/108605375/8f023d46-83ec-4ab1-91a7-da174e39fcd5)

### Marketing Manager

Problem Statement:
Lisa Wants to plan new marketing campaign. She has two modes of Campaign:
1. Social Media for Younger people
2. Print advertisemetns in News paper for Older people.

She needs data about the customers who belong to three age categories in all four regions:
1. Less than 36 years.
2. Between 36 to 54 years.
3. Above 54 years.

SQL Qury to fetch the required Data

```
Select
	Region, 
	case 
	when age < 36 then 'Young'
	when age between 36 and 54 then 'Middle'
	else 'old' 
       	end as age_category, 
	count(customer_id)
from
	customer
group by
	Region, age_category
order by
	 region asc, age_category desc
```
#### SQL Output

![image](https://github.com/varma-prasad/SuperMart-Analysis/assets/108605375/8bf4ce68-5d5f-4ba4-a28d-047d429f4228)

#### Power BI Report

![image](https://github.com/varma-prasad/SuperMart-Analysis/assets/108605375/c4d7636d-7df2-4e8f-b875-9f4710ed0ffb) 

### SupplyChain Manager

Problem Statement:
Sam facing Issues in Managing inventory in South(Over utilised) and East regions(Under Utilised). He needsd information about these products:
1. Top 5 selling Products in the East Region.
2. Least 5 selling Products in the South Region.

### Finance Manager

Problem Statement:
To Manage the revenues, he needs more detail about the Discounts given for the products.
1. Total Revenue loss due to Discounts.
2. Total Revenue and Discount for Each product.

      

   
 
