## Task 2 :- Experimentation and uplift testing


- Julia has asked us to evaluate the performance of a store trial which was performed in stores 77, 86 and 88.

            • This can be broken down by:-
                        ♦ Total sales revenue
                        ♦ Total number of customers
                        ♦ Average number of transactions per customer
                        
-  Create a measure to compare different control stores to each of the trial stores to do this write a function to reduce having to re-do the analysis for each trial store. Consider using Pearson correlations or a metric such as a magnitude distance e.g. 1- (Observed distance – minimum distance)/(Maximum distance – minimum distance) as a measure.

- Once you have selected your control stores, compare each trial and control pair during the trial period. You want to test if total sales are significantly different in the trial period and if so, check if the driver of change is more purchasing customers or more purchases per customers etc.

    - Main areas of Focus are :-
        - Select control stores – Explore data, define metrics, visualize graphs
        - Assessment of the trial – insights/trends by comparing trial stores with control stores
        - Collate findings – summarize and provide recommendations

**Experimenting and testing :-**

- **Compile each store's monthly:**
      
      < 1 > Total sales
      < 2 > Number of customers
      < 3 > Average transactions per customer
      < 4 > Average chips per customer
      < 5 > Average price per unit

- Check significance of Trial minus Control stores TOT_SALES Percentage Difference Pre-Trial vs Trial.

Step 1 :- Check null hypothesis of 0 difference between control store's Pre-Trial and Trial period performance.
Step 2 :- Proof control and trial stores are similar statistically

Check p-value of control store's Pre-Trial vs Trial store's Pre-Trial. If <5%, it is significantly different. If >5%, it is not significantly different (similar).

Step 3 :- After checking Null Hypothesis of first 2 step to be true, we can check Null Hypothesis of Percentage Difference between Trial and Control stores during pre-trial is the same as during trial.

    -  Check T-Value of Percentage Difference of each Trial month (Feb, March, April 2019).

    -  Mean is mean of Percentage Difference during pre-trial.

    - Standard deviation is stdev of Percentage Difference during pre-trial.

    - Formula is Trial month's Percentage Difference minus Mean, divided by Standard deviation.

- Compare each T-Value with 95% percentage significance critical t-value of 6 degrees of freedom (7 months of sample - 1)

- Null hypothesis is true. There isn't any statistically significant difference between control store's scaled Pre-Trial and Trial period sales.

- There are 3 months' increase in performance that are statistically significant (Above the 95% confidence interval t-score):
  
      < 1 > March and April trial months for trial store 77
      < 2 > March trial months for trial store 86
  
- Check significance of Trial minus Control stores nCustomers Percentage Difference Pre-Trial vs Trial.

Step 1 :- Check null hypothesis of 0 difference between control store's Pre-Trial and Trial period performance.
Step 2 :- Proof control and trial stores are similar statistically
Step 3 :- After checking Null Hypothesis of first 2 step to be true, we can check Null Hypothesis of Percentage Difference between Trial and Control stores during pre-trial is the same as during trial.

- There are 5 months' increase in performance that are statistically significant (Above the 95% confidence interval t-score):
  
March and April trial months for trial store 77

Feb, March and April trial months for trial store 86

![TS 77 and CS 233 - TOT_SALES](https://user-images.githubusercontent.com/27211670/182024443-92dd6ab6-9351-4933-bca4-026d54193fd9.png)

![TS 86 and CS 155 - TOT_SALES](https://user-images.githubusercontent.com/27211670/182024457-a55adbcb-c5fe-43f6-a237-1675c93517ce.png)

![TS 88 and CS 40 - TOT_SALES](https://user-images.githubusercontent.com/27211670/182024474-cbc431d6-5f6e-4038-939c-21dbde3a945d.png)


![TS 77 and CS 233 - nCustomers](https://user-images.githubusercontent.com/27211670/182024498-b3c04c67-8a1f-47d4-8055-5e83a33c3897.png)

![TS 86 and CS 155 - nCustomers](https://user-images.githubusercontent.com/27211670/182024507-c5f80354-3c76-468c-b4d1-3bfa3249564e.png)

![TS 88 and CS 40 - nCustomers](https://user-images.githubusercontent.com/27211670/182024523-3db0cbcb-74a8-45e0-8913-339fd901d15e.png)



# Insights :-


1. We can see that Trial store 77 sales for Feb, March, and April exceeds 95% threshold of control store. Same goes to store 86 sales for all 3 trial months.

2. Trial store 77: Control store 233

3.  Trial store 86: Control store 155

4. Trial store 88: Control store 40

5. Both trial store 77 and 86 showed significant increase in Total Sales and Number of Customers during trial period. But not for trial store 88. Perhaps the client knows if there's anything about trial 88 that differs it from the other two trial.

6.  Overall the trial showed positive significant resul
