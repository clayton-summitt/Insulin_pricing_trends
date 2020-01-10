# Insulin pricing trends and the realationship to executive team compensation

# Motivation
My wife is a recently diagnosed Type 1 diabetic. This disease currently has no cure and as such it is managed dailly with injections of insulin. [Colorado recently passed a law](https://leg.colorado.gov/bills/hb19-1216) putting a cap on the price of insulin, this was in response to a number of high profile deaths of young diabetics who while gainfully employed, could not afford the out of pocket expense insulin (estimated at $1300 month). Beyond the personal connection to this disease, I am also interested in the economics of pharmaceuticals and the effect that generic drugs have on the marketplace, corporate bottom lines and executive compensation. Insulin is unique in that there are no generic competitors in the healthcare system. Since 1946, NPH or human insulin has been available, manufatured by Novo Nordisk, with the first recombinant human Insulin being brought to the market by Eli Lilly in 1982, improvements in both solubility, stability and duration of activity have lead to a large increase in the number of analogue insulins by Eli Lilly, Novo Nordisk and Sanofi. These include Tresiba(2015), Levemir(2005) and Lantus(2000). In addition to the rate of activity, these manufactures provide insulin in multiple delivery systems from vials, pens to cartridges for insulin pumps. 
![Devices](https://github.com/clayton-summitt/Insulin_pricing_trends/blob/master/images/Insulin_Delivery_Devices.png)
Image By BruceBlaus - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=44805230
# data source
Wholesale costs for insulin were collected from the Medicaid NADAC portal, this portal provides access for monthly average wholesale prices paid by a random selection of pharmacies in the United States. These csv files were assembled into a database using postgreSQL. 
[National Average Drug Acquisition Price](https://data.medicaid.gov/Drug-Pricing-and-Payment/NADAC-Comparison/6gk3-9bxc)  
[Eli Lilly] (https://investor.lilly.com/financial-information/quarterly-results)  
[Novo Nordisk] (https://www.novonordisk.com/investors/financial-results-and-investor-events.html)  


# data analysis
A two sided t-test was done to test the hypothesis that human insulin (NPH) and new insulin analogues have different mean prices. In addition to this test, a two sided t-test was done to test the hypothesis that the mean price of long acting (basal) insulin was not equal to fast acting insulin. Both tests had extremely low Pvalues :(Human vs Analogue) P value = 6.68* 10-7, (fast acting vs rapid acting) : P value = 2.215* 10-7. There is insuffiecient evidence to reject the null hypthesis that the mean prices are equal. Eli Lilly income by drug per quarter was plotted over time to gain insight into the volatility of the insulin market.A histogram of all prices reported for all insulins was plotted. The mean prices for Human (red dash) Analogue fast acting(black dash) and Long Acting(green dash) were plotted. Prices for Humalin (human insulin) and Novolin with Novolog were plotted as a time series.  All drugs examined showed an increase in price which has been previously described in the media and in research literature. https://bmjopen.bmj.com/content/1/2/e000258#T3









![Histogram of prices from 2014-2020](https://github.com/clayton-summitt/Insulin_pricing_trends/blob/master/images/histogram%20copy.png)
![Eli Lilly](https://github.com/clayton-summitt/Insulin_pricing_trends/blob/master/images/elililly.png)
![Humulin pricing](https://github.com/clayton-summitt/Insulin_pricing_trends/blob/master/images/humulin.png)
![Novolog and Novolin](https://github.com/clayton-summitt/Insulin_pricing_trends/blob/master/images/novol.png)
## Future data analysis
Besides insulin, there are several other diabetic devices that could be examined such as glucose meters, test strips, insulin pumps and continous glucose meters. Medicaid, in addition to the I am also interested in measuring public sentiment to insulin pricing via twitter.[There is evidence that some groups are concerned about the decreased revenue from generic competiton in all drugs classes](https://www.uspharmacist.com/article/drug-patent-expirations-and-the-patent-cliff). As such It would be interesting to examine historical medicaid reimbursement data for all 50 states and the NADAC prices paid to see what if any trends can be predicted by changes in a drugs patent status.
