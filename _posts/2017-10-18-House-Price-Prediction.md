---
layout: post
title: House Price prediction by machine learning
---

![_config.yml]({{ site.baseurl }}/images/house-prices up.jpg)

To choose which kind of property to purchase is always a hard work for many potential buyers, normally, common features such as number of bedrooms, location, the closeness to the public transport are always ranked the top to consider. However, in this case, almost 80 features which includes almost every aspect of a property, and base one those features, we are here trying to predict the sales prices of them.

Key points of this project:
Knowledge to clean the date and deal with the NULL values
Knowledge to do feature engineering to get more relevant and usable data
Knowledge to choose and evaluate the model

1, In order to use linear model, the target (sales price in this case) needs to be normally distributed, however, If you look into the sales price, it is bit skewed.

![_config.yml]({{ site.baseurl }}/images/p3-1-price.png) 

So, tying to see whether the logged sales price is normally distributed:

![_config.yml]({{ site.baseurl }}/images/p3-2-logprice.png) 

The result is promising, and we can go ahead to built a linear model.

2, There are so many columns containing Nominal data (categorised date, order is not important) and Ordinal data (categorised date, order means something), so we now trying to numberise them based on the mean of the relative targeted price.

![_config.yml]({{ site.baseurl }}/images/p3-3-numberise.jpg)  

3, Last, Lasso was used as the model to train the data, and the result is promising, which is in around 87% of the time that the model can predict a correct price.

![_config.yml]({{ site.baseurl }}/images/p3-4-result-compare.png)  

(The closer the dots to the diagonal, the better the accuracy is)

The code for this project can be found at: [Link to Github](https://github.com/DavidZliu/p3-house-price/blob/master/p3-code-Nov.ipynb)

