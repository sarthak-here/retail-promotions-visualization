# Retail Promotions Analysis - Presenter Script

Approximate speaking time: 7 to 9 minutes

## Introduction

Good morning, and thank you for giving me the opportunity to present this analysis.

My name is Sarthak Sharma. In this project, I analyzed retail promotion data to understand how promotional campaigns affected sales quantity and revenue across different cities, product categories, and promotion types.

The purpose of this analysis was not only to identify which promotions generated more sales. I also wanted to understand whether those additional units resulted in higher revenue, because a promotion can increase volume while still reducing revenue through heavy discounting.

I used Python and Pandas for data preparation and analysis. I used Matplotlib and Seaborn for the exploratory visualizations, and then converted the main findings into this client presentation.

Before beginning the analysis, I joined the event data with the campaign, product, and store information. I also checked the data for missing values, exact duplicates, and unmatched records. The final analysis covered 1,500 promotional events from 50 stores.

I will now take you through the main findings.

## Slide 1 - Sales performance before and after promotion

This presentation examines sales performance before and after the promotional campaigns.

I evaluated performance from two perspectives. The first was quantity, which shows whether customers purchased more units. The second was revenue, which shows whether those additional sales produced financial value after accounting for the promotional price.

For revenue, I multiplied the applicable base price by the corresponding quantity sold. For incremental sold units percentage, or ISU%, I compared the total quantity before and after promotion. I used the same aggregate approach for incremental revenue percentage.

Using aggregated totals is important because averaging percentages from individual transactions can produce misleading results.

## Slide 2 - Executive summary

This slide summarizes the three most important findings from the analysis.

First, Grocery and Staples contributed 70.51% of all units sold after promotion during the Sankranti campaign. This shows that Sankranti sales were highly concentrated in one category.

Second, Madurai recorded the highest city-level incremental sold units percentage at 121.28%. In other words, the quantity sold after promotion was more than double its pre-promotion quantity.

Third, Bengaluru's total revenue increased by 81.34% after promotion. However, the later category analysis shows that this increase did not occur evenly across all product groups.

These findings suggest that campaign performance should be evaluated at multiple levels. A strong overall result can hide weaker categories or ineffective promotion types.

## Slide 3 - Store distribution by city

Here, I analyzed the number of unique stores in each city.

Bengaluru has the largest store network with 10 stores. Chennai follows with 8 stores, and Hyderabad has 7. Bengaluru therefore has two more stores than Chennai and three more than Hyderabad.

The remaining cities each have five or fewer stores. This means that Bengaluru has a larger physical base for testing campaigns and can naturally generate higher total sales.

This is why store count must be considered when comparing cities. Absolute sales alone can favor cities with more stores. Percentage-based metrics, such as ISU%, provide a fairer comparison of promotional effectiveness between markets of different sizes.

From a business perspective, Bengaluru is suitable for larger campaign tests, while smaller cities can be used for focused pilots before expanding a promotion.

## Slide 4 - Sankranti category contribution

This chart shows how each category contributed to the total quantity sold after promotion during Sankranti.

Grocery and Staples clearly dominated the campaign. It generated 177,724 units and contributed 70.51% of all post-promotion sales volume.

Home Appliances was the second-largest category at 14.13%. Home Care contributed 6.70%, Combo1 contributed 4.92%, and Personal Care contributed 3.74%.

I performed this analysis to identify where customer demand was concentrated. The result indicates that customers responded particularly strongly to essential grocery products during Sankranti.

For future campaigns, the business should protect inventory availability for Grocery and Staples so that stock shortages do not limit sales. The smaller categories should receive more targeted promotions based on their own customer behavior rather than receiving the same discount strategy as groceries.

## Slide 5 - Correlation between price and quantity

This slide examines whether the base price after promotion was related to the quantity sold after promotion.

The Pearson correlation coefficient is 0.269. This represents a weak positive relationship.

This means that the dataset does not show a strong pattern where lower-priced products consistently sold more units. It also does not mean that increasing price causes sales to increase.

Other factors can influence this relationship, including product category, normal demand, campaign, store location, and promotion type. For example, an expensive appliance and a low-priced grocery product have very different buying patterns.

The business should therefore avoid selecting promotions based only on product price. A better approach would analyze price sensitivity separately within each category and promotion type.

## Slide 6 - Baseline demand by category

These charts show the distribution of quantity sold before promotion for each product category.

I included the pre-promotion distribution because every category starts with a different level of natural demand. Without this baseline, a category with high normal sales could appear more successful simply because it was already popular.

Grocery and Staples had the highest baseline demand, with a median of 317 units. Its distribution was also much wider than the other categories, which indicates greater variation between sales events.

Combo1 had a median of 147 units. Home Appliances had a median of 72, Personal Care had 58, and Home Care had 43.

The important conclusion is that one sales target should not be applied to every category. Grocery products should be evaluated against their already-high baseline, while smaller categories may show meaningful growth even when their absolute sales remain lower.

Future promotional targets should therefore be category-specific and based on both baseline demand and expected incremental improvement.

## Slide 7 - Incremental sold units by city

This slide compares ISU% across cities.

I calculated this metric by subtracting total pre-promotion units from total post-promotion units, dividing the difference by total pre-promotion units, and multiplying by 100.

Madurai achieved the highest ISU% at 121.28%. Bengaluru followed at 114.70%, while Coimbatore reached 113.74% and Chennai reached 112.52%.

Visakhapatnam recorded the smallest increase at 99.07%. Although it was the lowest result, its post-promotion sales were still almost double its baseline.

The difference between Madurai and Visakhapatnam was 22.21 percentage points. This variation shows that promotions were effective across all cities, but their strength differed by market.

Before copying Madurai's strategy, I would examine which categories and promotion types were responsible for its result. This would help determine whether the performance came from a reusable strategy or simply from a different product mix.

## Slide 8 - Hyderabad promotion performance

This scatter plot compares incremental sold units with incremental revenue for each promotion type in Hyderabad.

I used both measures because the promotion that moves the most products is not necessarily the promotion that creates the most revenue.

BOGOF generated the highest increase in sales volume, adding 24,168 units. It also produced approximately 3.18 million in incremental revenue.

The 500 Cashback promotion generated fewer additional units, at 5,845, but it produced the highest incremental revenue at approximately 12.87 million.

The percentage discounts were weaker. The 33% and 50% discounts increased units but reduced revenue. The 25% discount reduced both quantity and revenue in Hyderabad.

The business implication is that BOGOF works well when the objective is volume, inventory movement, or customer acquisition. The 500 Cashback promotion is the stronger option when the objective is revenue growth. Percentage discounts should be reviewed carefully because a sales increase may not compensate for the reduced selling price.

## Slide 9 - Bengaluru revenue performance

The final slide compares revenue before and after promotion across product categories in Bengaluru.

Overall revenue increased from approximately 32.91 million before promotion to 59.68 million after promotion. This represents an increase of 81.34%.

Combo1 was the main driver. Its revenue increased from approximately 15.78 million to 38.13 million, producing an incremental gain of about 22.35 million.

Grocery and Staples, Home Appliances, and Home Care also generated higher revenue after promotion.

Personal Care was the exception. Its revenue declined by 32.39%, from approximately 576 thousand to 390 thousand.

Based on these findings, I would recommend maintaining sufficient Combo1 inventory during future campaigns and continuing to test the successful Grocery and Home category promotions. I would redesign the Personal Care offer and test a different promotion type, discount level, or product selection before using the same strategy again.

## Conclusion

To conclude, the promotions produced strong overall sales growth, but the results varied considerably across categories, cities, and promotion types.

Grocery and Staples drove Sankranti sales volume. Madurai recorded the strongest percentage growth in units. In Hyderabad, BOGOF was the strongest volume promotion, while 500 Cashback generated the most incremental revenue. In Bengaluru, Combo1 drove most of the revenue improvement, while Personal Care underperformed.

The main recommendation is to avoid using a single promotion strategy everywhere. Future campaigns should define their objective first, such as increasing volume, improving revenue, clearing inventory, or attracting customers. The promotion type should then be selected according to the category and local market.

Thank you. I would be happy to answer any questions about the analysis, calculations, or recommendations.

## Short answers for likely client questions

### Why did you use aggregated totals for ISU% and IR%?

Aggregated totals preserve the actual business impact. Averaging row-level percentages would give small and large sales events equal influence and could distort the result.

### Does the correlation prove that higher prices increase sales?

No. The correlation is weak, and correlation does not prove causation. Category, demand, location, and promotion type can influence both variables.

### Which promotion should the company use?

It depends on the objective. BOGOF produced the highest incremental volume in Hyderabad, while 500 Cashback produced the highest incremental revenue. The company should select promotions based on the desired outcome.

### Why might Personal Care revenue have declined?

Possible causes include an ineffective discount, weak product selection, low demand, or customers shifting purchases between periods. The current dataset identifies the decline but does not establish its cause, so a product-level investigation is required.

### What additional analysis would you perform?

I would compare campaign-level profitability, promotion performance within each category, average results per store, product-level outliers, and repeat-customer behavior. Cost and margin data would also allow profit analysis instead of revenue analysis alone.


