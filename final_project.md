

```python
"""
Is it really a truth that coupon can improve purchasing power of customers?

                                                                                                    Xintong Guan

Introduction

Economic incentives have been seen as an effective way to get positive effects on improving purchasing power of 
customers. For example, coupons. We are a coupon nation. According to a survey conducted by RetailMeNot, which is a 
company that maintains a collection of coupon website, 96% Americans are coupon users and New York, Boston and 
Philadelphia reign supreme as top couponing cities. In 2013, 329 billion coupons for Consumer Packaged Goods (CPGs) 
were distributed in the U.S., and 2.9 billion of those were redeemed by people.

However, compared to “one-size-fit-all” programs, loyalty program which is one of the common economics incentives, is 
more often offered by retailers to customers who frequently make purchases, and it is seen as an very effective way 
to give customers access to new products and stimulate future purchasing. Marketers and a lot of past studies have 
paid attention to loyalty research. They used data from loyalty programs, such as demographics or transaction 
histories to study customers’ purchasing habits or pattern or predict their future buying behavior. For example, 
Sears once used their service and warranty card database to conduct a very successful direct marketing campaign,
which increased store traffic and sales of Kenmore appliances.



Hypothesis

Because of the truth of coupon, past researches have been working on how coupons improve customers purchasing. But 
to date little research exists to inform the difference effects of targeted coupons during different coupon period. 
For example, does targeted coupon work well only during coupon period, or it also has long-term effects on the 
promotion of purchasing even after the coupon period? This is leading to the following hypotheses:
 
H1: Coupon exposure increases purchasing during and after coupon period.

Different people have different reactions to coupons. Some people use them but some don’t. Therefore, are there any 
differences of future purchase between customers who used coupons before and customers who were exposed to some but 
did not use them? If people once were exposed to coupons but didn't use them, will they still increase their 
purchase? These questions lead to the second hypothesis:

H2: Coupon exposure will affect customers who ever used such coupon more than those who never used before.


Panel Data

This study is based on an existing panel data from the retail analytic firm, Dunnhumbuy. It is a de-identified, 
household-level, data. This data contains 2-year information about grocery transaction histories, and coupon 
information (exposure and redemption). During the 2 years, there are 21900 transactions among 2500 households, 92339 
products and 780 coupon exposures.


Method

I am going to draw two graphs to show the purchasing difference of before, during and after coupon period, and also 
to show purchasing difference between the situation when households were exposed to coupons and situation when 
households were not exposed to coupons. By comparing mean purchase rate among different times and among different 
coupon usage situations, we will clearly see whether coupon exposure significantly increase food purchase, whether 
the effects last for a long time and whether there are differences when households were exposed to coupons or not. 
I created independent variables coupon time and coupon exposure to describe whether transactions happened before, 
during or after coupon period, and to describe whether households were exposed to coupons were not. 


Results

The estimates of the purchasing pattern and its goodness of fit appear in these two graphs. The first bar graph 
clearly shows that coupon exposure improved food purchase during coupon period and the effect lasts for a while. The 
second graph, which demonstrates the difference between people using coupons were not, shows that when people got 
coupons and used them, the increase of food purchase was significantly greater than the occasion when they didn’t use 
coupons. I also ran regression models though SAS and got same results. Positive coefficients for coupon time when it 
represent during and after (p<. 0001), suggesting that during and after coupon period, each week, households purchase 
more than before coupon period. Therefore, my first hypothesis got supported. Consistent with second graph, when 
households once received coupons and used them, they purchased more than those who never use the coupons (p<. 0001). 
Therefore, the second hypothesis also got supported. 


Conclusion

This study examines the impact of coupons on customer’s purchasing behavior over a two-year period. It enriches prior 
studies by grouping customers and grouping coupon time. Compared to the “one-size-fit-all” strategy, targeted 
financial incentives are more effective at improving purchase. The results of this study provide powerful evidence to 
retailers and marketers that coupon is an effective way to promote people purchasing, either in the short run or in 
the long run. Furthermore, logic dictates that individual differences, such as dietary patterns, really matter on 
effectiveness of targeted incentives. For example, the shopper who regularly purchases milk would use but may not need 
a coupon to continue purchasing this product. In the future, one possible study is to adding demographic information 
as a possible covariate and could interpret when, how and how much to use targeted incentives to improve eating 
pattern among different households. 


Reference

(1)Meyer-Waarden, L. (2008), "The Influence of Loyalty Program Membership on Customer Purchase Behavior," European 
Journal of Marketing, 42, 87-114
(2)Yuping Liu. (2007), “The Long-Term Impact of Loyalty Programs on Consumer Purchase Behavior and Loyalty” American 
Marketing Association, 1547-7185
(3)Wilma E Waterlander. (2013), “Effects of different discount levels on healthy products coupled with a healthy 
choice label, special offer label or both: results from a web-based supermarket experiment”, International Journal of 
Behavior Nutrition and Physical Activity.
(4)Berry, Michael J.A (1997). Data Mining Techniques For Marketing, Sales and Customer Support. Wiley. p. 10.
(5)Bertrand, M.; Duflo, E.; Mullainathan, S. (2004). "How Much Should We Trust Differences-in-Differences Estimates?".
Quarterly Journal of Economics. 119 (1): 249–275.  


"""
```


```python
"""
data and graphs part
"""
import pandas as pd
data=pd.read_csv('bigdata.csv')
data.head()
%matplotlib inline
#first graph
plot = data.groupby(['time']).rate.mean()
plot_= plot.plot(kind = 'bar', stacked = True, 
                  title = "rate")
plot_.set_xlabel("time")
plot_.set_ylabel("rate")
```




    <matplotlib.text.Text at 0x10e251d30>




![png](output_1_1.png)



```python
#second graph
plot2= data.groupby(['exposure']).rate.mean()
plot2_= plot2.plot(kind = 'bar', stacked = True, 
                  title = "rate")
plot2_.set_xlabel("exposure")
plot2_.set_ylabel("rate")
```




    <matplotlib.text.Text at 0x10b9cfe10>




![png](output_2_1.png)



```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

            
```


```python

```
