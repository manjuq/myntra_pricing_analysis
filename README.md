The goal is to understand how discount depth and product persistence (stable vs transient listings) relate to customer trust over time.
# Myntra Women's Dresses Pricing & Discount Analysis

I scraped around 3,000 women's dress listings from Myntra every day for 20 consecutive days across three sort modes: Popularity, Discount, and Recommended. 
The goal was to understand whether the discounting on this platform is genuine or manufactured. At 72% median discount across 54,000 rows, something is clearly 
structural rather than promotional.

## Findings

1. **Discounting is structural, not promotional.** Median discount is 72% and over 
   half of all products are discounted more than 70% off MRP. MRP functions as a 
   fictional anchor, not a real price.

2. **Sort mode is a real signal.** The Discount sort averages 88.8% discount and a 
   3.88 rating vs 4.10 for Popularity. 70 brands appear exclusively in the Discount 
   sort and never in the other two, meaning they have no organic platform presence. 
   The difference is statistically significant with a large effect size (r ≈ 0.33, p ≈ 0).

3. **Higher discounts do not move more inventory.** Products with 75%+ discounts have 
   the lowest sell-through rate at 36.6%. The 40-60% discount bucket sells through the 
   most. Higher discounts are a symptom of low demand, not a solution for it.

4. **Quality products last longer on the platform.** Stable listings (15-20 days) rate 
   consistently higher than transient ones (Cohen's d = 0.117). The effect is small but reliable.

5. **Brands that discount the most reprice the least.** Spearman r = -0.44 (p < 0.001). 
   Fake-MRP brands set their discount once and never touch it. Brands like MANGO and 
   SASSAFRAS actively manage pricing around demand signals and platform events.

6. **Pricing explains very little of rating variance.** Random Forest R² = 0.185. 
   A product's rating cannot be predicted from price and discount alone, which says 
   something about what platform data can and cannot tell you.


## Stack

Python, pandas, matplotlib, seaborn, scikit-learn, scipy