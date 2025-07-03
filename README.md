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
1. Average discount by Category didn't vary much, althougth "Home Improvements" topped the chart with **58%**.
2. The "Electronics" Category has the highest number of products with **490**, while "Car and Motorbike", "Health and Personal Care", and "Toys & Games" has **1** each. This potentially explains why "Electronics" Category, with **14,208,406**, has the highest number of reviews, as well as total potential revenue at **₹91.324bn**.
3. Only two products had a perfect rating of **5**, three others were rated **4.8**, while six were rated **4.7**.
4. Number of products having 50% or more discount were **660**.
5. Only **307** products had less than 100 reviews.
6. The trajectory of the Average Actual Price and that of the Discounted Price were similar, showing a fair balance in discount percentage.
7. There seemed not to be any relationship between product discount and average rating seeing that the least rated products (with and average of **3.94**) were those having a discount percentage of between **80 to 90%**, while products having **less than 10%** discount had an average rating of **4.2**), ranking No 2 - though second only to products with **90 to 100%** discount (with an average rating of **4.22**).
8. Products priced **₹500 or less** accounted for **37%** of all products under review, colsely followed by those priced **between ₹1,000 to ₹5,000** which accounted for about **30%**. The least was those **between ₹5,000 to ₹10,000** at just about **6%** of the total.
9. Most high-discounting products fell into the Category of Computer & Accessories, Electronics and Home & Kitchen.
10. Products under review had a fair rating distribution. While only **6** were rated **less than 3**, **914** were rated between **4 and 4.5**, and **95** were rated between **4.5 and 5**.
