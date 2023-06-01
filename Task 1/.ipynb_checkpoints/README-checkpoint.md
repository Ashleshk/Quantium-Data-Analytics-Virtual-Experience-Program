## Task 1 :- Data preparation and customer analytics

Conduct analysis on your client's transaction dataset and identify customer purchasing behaviours to generate insights and provide commercial recommendations.

**The background information for this task :-**

- I am part of Quantium’s retail analytics team and have been approached by our client, the Category Manager for Chips, who wants to better understand the types of customers who purchase Chips and their purchasing behaviour within the region.
    
- The insights from my analysis will feed into the supermarket’s strategic plan for the chip category in the next half year.
Here is task :-

- I need to present a strategic recommendation to Julia that is supported by data which she can then use for the upcoming category review however to do so I need to analyse the data to understand the current purchasing trends and behaviours. The client is particularly interested in customer segments and their chip purchasing behaviour. Consider what metrics would help describe the customers’ purchasing behaviour.
    - Examine transaction data - check for missing data, anomalies, outliers and clean them
    - Examine customer data - similar to above transaction data
    - Data analysis and customer segments - create charts and graphs, note trends and insights
    - Deep dive into customer segments - determine which segments should be targetted
           
**Data Preparation :-**
    
•♦• Date column was in integer format. So the date column was changed to date time format.

•♦• There are 365 days in a year but in the DATE column there are only 364 unique values so one was missing. As it was a Christmas day and store was closed there was no anomaly. Value was kept as zero transaction for "TOT_SALES".
    
![Sales of December 2018](https://user-images.githubusercontent.com/27211670/182023039-abcf79bb-6c23-425a-8766-f4ba41870f1d.png)

•♦• Checked if all the products in given data are chips.

•♦• Some product names are written in more than one way. Example : Dorito and Doritos, Grains and GrnWves, Infusions and Ifzns, Natural and NCC, Red and RRD, Smith and Smiths and Snbts and Sunbites. It was cleaned thereafter.

•♦• Split and frequency of each word in "PROD_NAME" column. Removed all rows containing "salsa" in "PROD_QTY" column.

•♦• Checked for outliers and removed outliers rows in "PROD_QTY" column.

•♦• Each word value was counted in "PROD_NAME" column to extract the brand name. Combined brands written in multiple ways. Created a new column "Cleaned_Brand_Names".
    
![Brand Names](https://user-images.githubusercontent.com/27211670/182023130-68ac433a-b952-4170-85f2-fa61510b38b7.png)
    
    
**Data Analysis on Customer Segments :-**

♦ The 4 main questions answered in data analysis were:
    < 1 > Who spends the most on chips (total sales), describing customers by lifestage and how premium their general purchasing behaviour is ?
    < 2 > How many customers are in each segment ?
    < 3 > How many chips are bought per customer by segment ?
    < 4 > What's the average chip price by customer segment ?

♦ Groupby sum TOT_SALES column and identified top 3 highest total sales contributing segments.
♦ Plot the groupby into stacked bar chart with percentage text on each segment stack.

![lifestage_sales](https://user-images.githubusercontent.com/27211670/182023454-c0e11717-7a80-40ef-b63c-a9526cc2c057.png)

♦ The high sales amount by segment "Young Singles/Couples - Mainstream" and "Retirees - Mainstream" are due to their large number of unique customers, but not for the "Older - Budget" segment. Next we'll explore if the "Older - Budget" segment has: High Frequency of Purchase and, Average Sales per Customer compared to the other segment.

♦ Used p-value calculation and found statistically significant TOT_SALES difference (pval < 5%) between "Mainstream Young Midage" to "Budget and Premium Young Midage" segment.

♦ Divided groupby sum to groupby nunique to get average amount of chips bought per customer segment. Older and Young Families bought the highest average amount of chips.

♦ Unstacked the groupby and plotted it by segment:

![Average purchase quantity per segment](https://user-images.githubusercontent.com/27211670/182023522-1fb84dfa-c384-4b05-a3f3-e46ecdb68f0a.png)

**Insights from Data :-**
    Top 3 total sales contributor segment are :-

                                                i. Older families (Budget) $156,864
                                               ii. Young Singles/Couples (Mainstream) $147,582
                                              iii. Retirees (Mainstream) $145,169                                                  

•♦• Young Singles/Couples (Mainstream) has the highest population, followed by Retirees (Mainstream). Which explains their high total sales.

•♦• Despite Older Families not having the highest population, they have the highest frequency of purchase, which contributes to their high total sales.

•♦• Older Families followed by Young Families has the highest average quantity of chips bought per purchase.

•♦• The Mainstream category of the "Young and Midage Singles/Couples" have the highest spending of chips per purchase. And the difference to the non-Mainstream "Young and Midage Singles/Couples" are statistically significant.

•♦• Chips brand Kettle is dominating every segment as the most purchased brand.

•♦• Observing the 2nd most purchased brand, "Young and Midage Singles/Couples" is the only segment with a different preference (Doritos) as compared to others' (Smiths).

•♦• Most frequent chip size purchased is 175gr followed by the 150gr chip size for all segments.

**Future Recommendations :-**

•♦• Older Families: Focus on the Budget segment. Strength: Frequent purchase. We can give promotions that encourages more frequency of purchase. Strength: High quantity of chips purchased per visit. We can give promotions that encourage them to buy more quantity of chips per purchase.

•♦• Young Singles/Couples: Focus on the Mainstream segment. This segment is the only segment that had Doritos as their 2nd most purchased brand (after Kettle). To specifically target this segment it might be a good idea to collaborate with Doritos merchant to do some branding promotion catered to "Young Singles/Couples - Mainstream" segment. Strength: Population quantity. We can spend more effort on making sure our promotions reach them, and it reaches them frequently.

•♦• Retirees: Focus on the Mainstream segment. Strength: Population quantity. Again, since their population quantity is the contributor to the high total sales, we should spend more effort on making sure our promotions reaches as many of them as possible and frequent.

•♦• General: All segments has Kettle as the most frequently purchased brand and 175gr (regardless of brand) followed by 150gr as the preferred chip size. When promoting chips in general to all segments it is good to take advantage of these two points.
