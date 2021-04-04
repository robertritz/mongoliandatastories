---
layout: post
title:  The Ethical Matrix of Dzud Forecasting
date:   2019-02-13 00:00:00 +0800
image:  '/images/ethical-matrix-dzud-forecasting/cover.jpeg'
tags:   [dzud, forecasting]
featured: 
---

In 2016 a pivotal book in the field of data science was released. [Weapons of Math Destruction](https://www.amazon.com/Weapons-Math-Destruction-Increases-Inequality-ebook/dp/B01LDFCP0S/ref=sr_1_1?keywords=weapons+of+math+destruction&qid=1549790280&s=gateway&sr=8-1), by Cathy O’Neil, makes the claim that the algorithms which promise to change our world for the better can also reinforce discrimination, unfair bias, and cause damage on a massive scale.

In this book and in a forthcoming research paper, O’Neil proposes that algorithms don’t just predict the future, they can also _create it._ As such she proposes the use of an “Ethical Matrix” be completed before such an algorithm is implemented. This matrix is designed to understand the real impact of an algorithm. It aims to explicitly answer _who the algorithm is impacting and how_ in the following ways:

-   Fairness: is the algorithm truly fair to all those impacted?
-   Transparency: do we have visibility as to how the algorithm is making its decisions?
-   False Negatives: how are stakeholders impacted by false negatives?
-   False Positives: how are stakeholders impacted by false positives?

Why is this matrix important? As algorithms are being applied in more areas of our lives, there is often little regard to their full impact. Here are just a few examples of algorithms and their unintended consequences.

-   In 2015 Google’s auto-tagging photo feature embarrassed the company by labeling a black person a gorilla. [Google still has this problem.](https://www.wired.com/story/when-it-comes-to-gorillas-google-photos-remains-blind/)
-   Recently a significant amount of scrutiny was placed on [algorithmic credit scoring](https://qz.com/1276781/algorithms-are-making-the-same-mistakes-assessing-credit-scores-that-humans-did-a-century-ago/). These supposedly fair algorithms show a surprising bias in areas such as race. In one example an algorithm reduced credit scores for customers that had a bank charge for “counseling”.
-   Amazon has used an algorithm to assess recruits applying for jobs at the company. [This algorithm](https://www.reuters.com/article/us-amazon-com-jobs-automation-insight/amazon-scraps-secret-ai-recruiting-tool-that-showed-bias-against-women-idUSKCN1MK08G) appeared to have a strong gender bias against women. Amazon says they never put it in production.

[**2018 in Review: 10 AI Failures**  
_Last December Synced compiled its first “Artificial Intelligence Failures” recap of AI gaffes from the previous year…_medium.com](https://medium.com/syncedreview/2018-in-review-10-ai-failures-c18faadf5983 "https://medium.com/syncedreview/2018-in-review-10-ai-failures-c18faadf5983")[](https://medium.com/syncedreview/2018-in-review-10-ai-failures-c18faadf5983)

Given these potential consequences, it’s a good idea to evaluate any potential new algorithm to better understand how it could hurt those it impacts. A recently released algorithm in Mongolia inspired me to do just this.

#### Livestock Mortality Index

In November 2018 a [research paper](https://reliefweb.int/report/mongolia/advancing-understanding-dzud-risk-livestock-mortality-model-and-multi-indicator-dzud) was released by People in Need, an international NGO, that proposes a livestock mortality index to perhaps provide an early warning for [dzud](https://en.wikipedia.org/wiki/Zud) in Mongolia. This index would assign a value from 0–5 for each aimag (province) that would describe the risk of dzud in that aimag for the next winter. As dzud is perhaps the largest natural disaster Mongolia faces, being able to accurately assess the risk of dzud is a very important step in making herding a sustainable livelihood long term.

Currently, the Government of Mongolia has a [risk map model](http://eic.mn/dzud/index.php) (at the [soum](https://en.wikipedia.org/wiki/Sum_%28country_subdivision%29) level) in place that was implemented in 2015/2016 and is updated every 10 days. The way in which the proposed index is different is the lead time it would provide to prepare areas that are at the highest risk. Instead of identifying a sudden issue up to 10 days in advance, there would be an indicator of risk months ahead of time. This would give the government and non-governmental actors time to preposition fodder or other materials long before a dzud occurred.

In the paper, the authors make clear that this index is not intended to be a forecast, but rather an indicator of risk. However, as this is essentially an algorithm that is attempting to predict the future, I thought this was the perfect time to apply the Ethical Matrix to a Mongolian case.

### Ethical Matrix

To assess the algorithm we will look at four areas: **fairness, transparency, false negatives,** and **false positives**. To quickly summarize the algorithm, it uses 7 indicators to create a score from 0–5 (ex. 0.1, 1.4, 2.3, 4, 4.4) for each aimag. The higher the number the higher the risk. The indicators are:

-   Winter temperature anomaly
-   Snowfall anomaly
-   Biomass anomaly
-   Pasture use anomaly
-   Zootechnical scores (a combination of past mortality and female reproductivity)

#### Fairness

The idea of fairness is the general question of whether the algorithm treats those impacted by it equally. In this, the algorithm does quite well. One area of concern is the metric of forage biomass (the amount of forage available). Given the disparity between the south of Mongolia and the north, this is an area where an imbalance could occur. The authors handle this by looking at the anomaly (or change in) biomass to ensure areas with disparate biomass are not treated differently.

![](/images/ethical-matrix-dzud-forecasting/biomass.gif)

#### Transparency

Transparency in an algorithm is a difficult thing to accomplish. As these are computer models, it isn’t as simple as asking the computer ‘_Why did you do that?’_. However, what we can do is understand how the inputs are related to the outputs. For example, if I change one thing how does this change the score (higher/lower). In this way, we can understand “how” the algorithm is coming to its conclusions.

The algorithm here again does this quite well. As it is a linear model, we have coefficients for each variable. These coefficients are basically weights on the variables that are combined with the variables themselves to generate a score. The model equation is given and as such we can determine how each variable impacts the final risk score.

![](/images/ethical-matrix-dzud-forecasting/page16.png)

Page 16 of the MDVI report

#### False Positives and Negatives

It’s great to have a fair and transparent algorithm, but what if it fails in certain ways that can cause harm? This is what we try to assess when looking at false positives and false negatives. A false positive in this case is a high-risk score (a “positive” result for high dzud risk) when little to no mortality occurred. The opposite situation is a false negative, where the risk score is low but high mortality results. Both are undesirable but for different reasons.

**False Positives**

A false positive is also known as “crying wolf”. The result can be similar to the fable, with an erosion of trust in the model after several attempts to prevent disaster over the long term. In the short term, a false positive can waste resources that could otherwise be used in areas that need them more. Over the long term, the larger movement to stop a dzud from happening could be undermined with herders, governments, and NGO’s withdrawing from the program.

The idea of [false dzud alarms](http://blogs.ubc.ca/mongolia/2017/crying-wolf-dzud/) was discussed in 2017 by Julian Dierkes, a professor at the University of British Columbia and a well-known observer of Mongolia. This critical look at false positives shows how not only data can undermine the system, but the perception of the situation.

**False Negative**

A false negative can have dire consequences. In this situation, high mortality would occur with the model indicating a low risk. This would mean that enough fodder or other materials may not be readily available on short notice to help in aimags falsely designated as low risk.

This would have more extreme short term consequences not only for livestock but also for trust in the model. If a model has even a few false negatives it very likely could be thrown out and labeled untrustworthy.

### Confusion Matrix

In general, when optimizing a machine learning model it is good to ask whether false positives or false negatives are worse. For this model, it is conceivable that several false positives could be tolerated, although with an erosion of trust and possibly less mobilization for each subsequent false positive. However, it would be disastrous to have even a few false negatives in the real world. Livestock could die by the hundreds of thousands and the area could be devastated economically. For this reason, I believe that false negatives for this are much less desirable and should be minimized as much as possible.

The authors of the study made available the predicted risk scores and the livestock mortality numbers for the years in question. With this data, we can create a confusion matrix that will allow us to visualize our false positives and negatives. As the authors did not give bins for the index values, we will simplify things a bit and bin them ourselves. The bins are as follows:

-   Index, Mortality %
-   0–1, \[0%-3%\]
-   1–2, (3%-6%\]
-   2–3, (6%-17%\]
-   3+, (17%+)

Here is the corresponding confusion matrix. TP = True Positive, TN = True Negative, FP = False Positive, FN = False Negative.

![](/images/ethical-matrix-dzud-forecasting/confusion-matrix.png)
*Confusion matrix derived from MVDI risk scores*

Viewing this confusion matrix we see a relatively small number of true positives or negatives (about 15% of the total). If this were a classification task this would be quite undesirable. However, the model is set up as a regression task, so this isn’t necessarily bad. Of more interest are the FP’s and FN’s.

The false positives are the large majority here. As we established that we want to minimize FN’s due to their destructive potential, this is a positive sign. However, FP’s are nearly 74% of the values. Given this, it should be known that this model will consistently overstate the risk values.

### Conclusion

One way to solve the issue with FP’s and FN’s is to restate the task as a classification one. Currently, as regression, the output plotted against real values is shown in figure 5. While it’s simple to say that higher values mean higher risk, what is one aimag has “1.5” and the other has “2.2”. Should more resources be provided to the higher risk even though we know this model has a high false positive ratio?

![](/images/ethical-matrix-dzud-forecasting/mdvi-index-chart.png)

Resulting index values from MDVI model

By changing the problem to a classification one we can allow the user of the model to make more intuitive decisions from the output of the model. Instead of numeric values, the output of the model could be “low”, “medium”, and “high”. This may in itself be too simple, but if the classes are based on actual results from real data, then they will have a higher interpretive ability in the real world.

It is an important step for any machine learning or algorithmic project to take time to understand how it’s results can impact stakeholders and the system as a whole. The authors state that this model was not designed as a dzud forecast. However, once they release it in the real world NGO’s and governments can interpret the results how they wish. As such, there is a very real responsibility to understand how these values can be interpreted.
