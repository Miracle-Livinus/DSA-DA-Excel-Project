# DSA-DA Excel Project
This is a documentation of the execution of the DSA Data Analysis Capstone Project on Excel.
## This Project is on "Amazon Product Review Analysis" for RetailTech Insights
The base .xslx file contains product details extracted from Amazon website on some retail products, including their name, category, price, discount and ratings.

The initial number of products was **1,465** but after applying some data cleaning approaches to put the data in a well-structured format - which included removing duplicates, the number of products reduced to **1,348**.

Excel Pivot Tables was used to extract analysis-worthy information from the .xslx file, which were further presented in a result dashboard.

Part of the information extracted include:
- Average discount percentage by Product Category
- Total number of reviews per Category
- Average "actual price" **vs** "discounted price" by Category
- Number of products having a discount of 50% or more: by applying the command ```=COUNTIF("Yes")``` on the calculated Column created with the command ```=IF(N2>=50%,"Yes","No")``` _(**N** being the Discount Percentage Column on the .xlsx file)_
- Number of unique products by Price Range Bucket: where product prices were grouped in ranges using the command
  ```=IF(J2<500, "<₹500", IF(J2<=1000, "₹500 to ₹1000", IF(J2<=5000, "₹1,000 to ₹5,000", IF(J2<=10000, "₹5,000 to ₹10,000",">₹10,000"))))```
  _(**J** being the Price Column on the .xlsx file)_
- Potential revenue by Category
- How product discount percentages affected the rating levels
- Distribution of product ratings: using the command ```=IF(Q2<3,"<3",IF(Q2<3.5,"3 to 3.5",IF(Q2<4,"3.5 to 4",IF(Q2<4.5,"4 to 4.5","4.5 to 5"))))``` _(**Q** being the Product Rating Column on the .xslx file)_
- Categories with products having the highest discounts

### Key Findings from the Analysis
1. 
