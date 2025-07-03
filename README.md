# DSA-DA Excel Project
This is a documentation of the execution of the DSA Data Analysis Capstone Project on Excel.
## This Project is on "Amazon Product Review Analysis" for RetailTech Insights
The base .xslx file contains product details extracted from Amazon website on some retail products, including their name, category, price, discount and ratings.

The initial number of products was **1,465** but after some data cleaning approaches to put the data in a well-structured format which included removing duplicates, the number of products reduced to **1,348**.

Excel Pivot Tables was used to extract analysis-worthy information from the .xslx file, which were forther presented in a result dashboard.

Part of the information extracted include:
- Average discount percentage by Product Category
- Total number of reviews per Category
- Average "actual price" **vs** "discounted price" by Category
- Number of products having a discount of 50% or more: 
- Number of unique products by Price Range Bucket: where product prices were grouped in ranges using the syntax
  ```=IF(J2<500, "<₹500", IF(J2<=1000, "₹500 to ₹1000", IF(J2<=5000, "₹1,000 to ₹5,000", IF(J2<=10000, "₹5,000 to ₹10,000",">₹10,000"))))```
  _(J2 being the Price Column on the .xlsx file)_
- 
