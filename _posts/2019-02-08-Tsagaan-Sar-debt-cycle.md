---
layout: post
title:  The Tsagaan Sar Debt Cycle
date:   2019-02-08 00:00:00 +0800
image:  '/images/tsagaan-sar-debt-cycle/cover.jpeg'
tags:   [Tsagaan Sar, debt]
featured: 
---

The entire country mobilizes weeks ahead of time to prepare. The city government, worried about traffic, only allows cars to drive during alternate days on the weekend. The bakeries are so consumed with making _ul boov_, a traditional pastry, that bread starts to disappear from store shelves the week before the holiday.

This sounds like quite a lot, but it is just the run-up to the actual event, Tsagaan Sar, Mongolia’s lunar new year celebration. The main activity of the holiday (which goes on for three days) is where family (and extended family) visit their elders in their home. The guests traditionally bring money as a gift for their elders, and the guests are given gifts (sometimes small, sometimes large) in addition to a truly magnificent feast.

The video below shows the preparation of one of the signature dishes of Tsagaan Sar, _buuz_.

Tsagaan Sar Preparation

<iframe width="560" height="315" src="https://www.youtube.com/embed/BymB9IYd2xE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### The Cost

Each year new outlets write many articles sharing the costs of Tsagaan Sar. [News.mn estimated](https://news.mn/r/770526/) this year that cost for one family is about 1.32 million MNT (about $500 USD). To put his in perspective, more than half of those employed make less than [$200 per month](http://dnn.mn/%D1%86%D0%B0%D0%B3%D0%B0%D0%B0%D0%BD-%D1%81%D0%B0%D1%80-%D0%B1%D0%B0-%D1%86%D0%B0%D0%BB%D0%B8%D0%BD-%D1%82%D1%8D%D1%82%D0%B3%D1%8D%D0%B2%D1%8D%D1%80%D0%B8%D0%B9%D0%BD-%D0%B7%D1%8D%D1%8D%D0%BB/). A survey completed by a market research firm and reported by [BloombergTV Mongolia](http://bloombergtv.mn/%D0%B8%D1%80%D0%B3%D1%8D%D0%B4%D0%B8%D0%B9%D0%BD-62-%D1%85%D1%83%D0%B2%D1%8C-%D0%BD%D1%8C-%D0%B7%D1%8D%D1%8D%D0%BB%D1%8D%D1%8D%D1%80-%D1%86%D0%B0%D0%B3%D0%B0%D0%B0%D0%BD-%D1%81%D0%B0%D1%80-%D1%82%D1%8D%D0%BC%D0%B4%D1%8D%D0%B3%D0%BB%D1%8D%D0%B6-357-%D1%82%D1%8D%D1%80%D0%B1%D1%83%D0%BC-%D1%82%D3%A9%D0%B3%D1%80%D3%A9%D0%B3%D0%B8%D0%B9%D0%B3-%D0%B8%D0%BC%D0%BF%D0%BE%D1%80%D1%82%D1%8B%D0%BD-%D0%B1%D1%8D%D0%BB%D1%8D%D0%B3%D1%82-%D0%B7%D0%B0%D1%80%D1%86%D1%83%D1%83%D0%BB%D0%B6-%D0%B1%D0%B0%D0%B9%D0%BD%D0%B0/) concluded that 62% of those surveyed take out loans for the holiday.

I’ve thought about the cost of Tsagaan Sar for a few years now, but not in absolute costs. I’ve written before about the [growing debt](https://medium.com/mongolian-data-stories/mongolians-are-more-in-debt-now-than-ever-7f797e448f77) in Mongolia, and I wanted to see how the holiday impacted those who hold the greatest burden, the elders responsible for hosting 10’s or 100’s of guests. Phrased in a testable way:

> Do pension or salary loans issuances show an increase for Tsagaan Sar separate from the rest of the year?

### Loan Data

Luckily, MongolBank, the country’s central bank, [keeps statistics](https://www.mongolbank.mn/eng/dbliststatistic.aspx?id=02) many statistics on loans. I chose salary and pension loans because they are issued to individuals and are not (directly) used to purchase real estate. Pension loans are of particular interest because they are given using the government pension of the person as collateral.

To do the analysis I downloaded the [quarterly report](https://www.mongolbank.mn/eng/dbliststatistic.aspx?id=02) of “ Individual and SME loans issued by banks” and separated out salary and pension loans issued. The data is only available quarterly or annually. Quarterly actually suits our needs quite well as Tsagaan Sar always takes place in Q1 while the exact dates move every year.

![](/images/tsagaan-sar-debt-cycle/dataframe.png)

The head of our issued loans data. All numbers are in millions of MNT.

Let’s first take a look at the time series of both salary and pension loans.

![](/images/tsagaan-sar-debt-cycle/salary-loans-issued.png)

![](/images/tsagaan-sar-debt-cycle/pension-loans-issued.png)

Other than the obvious large increases in both, the thing to notice is when each increases during the year. It is already noticeable that pension loans have a spike at the beginning of each year while salary loans spike later.

To do a trend analysis we can use the handy [Prophet](https://facebook.github.io/prophet/) package from Facebook. There is a built-in seasonality tool that is perfect for this analysis. The tool is built on daily data analysis, so changes were made to accommodate a quarterly period (mainly reducing the [Fourier order](https://facebook.github.io/prophet/docs/seasonality,_holiday_effects,_and_regressors.html#fourier-order-for-seasonalities) for seasonality). The graphs below show the derived trends.

![](/images/tsagaan-sar-debt-cycle/salary-loans-seasonal.png)

It is important to remember when interpreting these graphs that as we only have one data point per quarter, Prophet is interpolating the trends between the quarters. For reference, quarters end March 31, June 30, September 30, and December 31.

Salary loans do show a large trend in Q1, but the largest trend appears to be in Q3. Perhaps parents trying to get enough money to pay for school tuition, clothes, etc.?

![](/images/tsagaan-sar-debt-cycle/pension-loan-seasonal.png)

Pension loans have an obvious upward trend in Q1, with Q2 and Q3 being significantly smaller. Can we answer our question?

> Do pension or salary loans issuances show an increase for Tsagaan Sar separate from the rest of the year?

Well, we certainly see a large increase in pension loans in Q1, which is when you would expect Tsagaan Sar expenditures, and therefore the need for cash. This certainly seems to fit with the narrative that the elderly are the most impacted, and are taking out loans specifically for the holiday.

Perhaps if you visit a family next year for Tsagaan Sar you may consider giving a bit more money to help offset these costs.