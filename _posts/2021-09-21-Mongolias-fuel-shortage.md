---
layout: post
title:  Mongolia is running on fumes
date:   2021-09-21 00:00:00 +0800
image:  '/images/fuel-shortage/cover.jpg'
tags:   [import, economy, fuel, gasoline]
featured: 
---

Just yesterday I learned that there has been a gasoline "shortage" for a few weeks in Mongolia. I put shortage in quotation marks because it seems the government and average citizens did not immediately agree on the reality of the situation. 

On September 14, 2021,  the Mineral Resources and Petroleum Authority of Mongolia  made a [statement](https://montsame.mn/mn/read/275097) via the state news agency Montsame unequivocaly stating that there is no shortage of gasoline. This is heavily contrasted by reports on social media of limitations on purchases or outages at some stations. 

<blockquote class="twitter-tweet"><p lang="ru" dir="ltr">Хил гааль дээр хэдэн сараар гацсан бараа таваараа татаж чадахгүй, хэдэн колониуд нь бензиний нөөцөө барсан, ковидоор өвдсөн хүмүүст нь эмнэлэг олдохгүй, дарга эрх мэдэлтнүүд нь эзгүй.... бид дижитал үндэстэн <a href="https://t.co/2xxAd3ha80">pic.twitter.com/2xxAd3ha80</a></p>&mdash; Seku (@ganaasel) <a href="https://twitter.com/ganaasel/status/1440021463935840257?ref_src=twsrc%5Etfw">September 20, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

So what is the actual situation currently in Mongolia? As usual, I like to go to the actual data to see what the reality is. 

## Fuel Reserves
The Mineral Resources and Petroleum Authority of Mongolia (MRPAM) reports fuel reserves on a monthly basis, and has these reports going back to 2015. Unfortunately the reports are in PDF form, requiring a bit of copy pasting on my part to collect the last two years of data. 

![](/images/fuel-shortage/92-supply.png)

We can see that the reserves of AI-92 fuel as of June 2021 are nearly 35% less than June 2020. It is also clear that during the fall reserves are reduced, most likely due to increased vehicle usage as people return to work from their summer vacations. 

As far as I can determine the government has not said anything definitive about when  imports of AI-92 slowed or stopped. The government did [release some information](https://montsame.mn/mn/read/275719) about further dwindling reserves today (September 21, 2021), stating the central region has 4 days of fuel remaining. Other than a mention that no AI-92 fuel will be imported in September, it is not clear what the current import situation is. 

Note: I chose to visualize AI-92 fuel as it is the most common fuel used in passenger vehicles in Mongolia. It is also the type of fuel nearly everyone is complaining about shortages of. 


#### Reporting Irregularity

Typically, the MRPAM posts the reserve statistics one month delayed, but it seems this year they have neglected to post any reserve statistics since July 22nd. By now we should be able to expect the reserve numbers for July and August to have been posted. As of the time of publishing, the government still has not released reserve or import statistics for July or August 2021.

In addition, an irregularity in the reporting popped up as I was going through these monthly reports. On all monthly reports, the MRPAM shows a yearly comparison on the fuel reserve chart, for example showing January 2021 vs January 2020. This allows the report reader to see how the reserves land year over year. This is a good comparison as consumer behavior follows a yearly pattern. 

The latest report for June 2021 made a departure from this. Instead of showing a year over year comparison they compared June 2021 vs May 2021. This made the numbers look better on the chart, and conveniently hid the nearly 35% reduction in reserves year over year. The screenshot below from [Page 25 of the June 2021 report](https://mrpam.gov.mn/public/pages/169/2021.06.stat.report.mon.pdf) shows this departure from the usual practice. 

![](/images/fuel-shortage/page25.png)

## Fuel Reserve Projection
Given today's announcement by the government, we know that the central region of Mongolia has only 4-5 days of fuel remaining. Nevertheless, it may be useful to understand how a fuel reserve projection could be made given imports, reserve numbers, and inferred usage. 

MRPAM releases import numbers by fuel type alongside the reserve numbers. 

![](/images/fuel-shortage/import-table.png)

A few minutes of copy pasting later I was able to create a nice table with reserves and imports for AI-92. I then took the previous months reserves, added it to the current months imports, and subtracted the current months reserves. This should give us a reasonable estimate of actual usage of AI-92 during that month.

![](/images/fuel-shortage/est_usage.svg)

We can also determine the available reserves at the end of the month given a very similar formula. 

![](/images/fuel-shortage/est_reserve.svg)

To extrapolate forward I looked at several different import scenarios where the imports are a *percentage of the values from 2020*. We will forecast forward using 75%, 85%, and 95% of the import levels from July 2020 to December 2020. We will assume the same level of fuel usage from July 2020 to December 2020. 

Stepping forward each month we can do the process listed above and get a projection of AI-92 reserves at the end of each month for each of these scenarios. Keep in mind the projection below assumes 2020 levels of consumption and are based on a percentage of imports from the corresponding month in 2020.

![](/images/fuel-shortage/projected-92-reserves.png)

At 85% of 2020 imports we see reserves emptying in September. At 95% reserves go negative in October and rise again positive in November. Only at 100% of 2020 import levels do the reserves stay above 0. The already lowered reserves from late summer seem to be exacerbating the current import issues.

It is very clear that without imports equal to or larger than 2020 Mongolia's AI-92 fuel reserve will continue to be near zero for a few months. Of course these projections aren't a guarantee of what will happen. They are merely scenarios based on past data that we can use to better understand the current situation. I hope you find them useful.


## Hiding Risk
It seems fairly clear from the analysis above that the current shortage of fuel could have been seen as early as July/August this year. Reserves were so far off their usual level that it was a clear signal of risk. Of course this was a sensitive time politically as back to school preparations began. The government seemed to clearly be trying to exhibit a sense of stability and preparation ahead of the usual fall rush in the city and around the country. 

It is important to remember that in December 2020 Mongolia had a [large opportunity](https://mongoliandatastories.com/Australias-loss-Mongolias-gain-coal) to significantly increase coal exports to China. China recently banned the import of coal from Australia, giving Mongolia an obvious advantage. Due to COVID-19 outbreaks and customs issues, Mongolia seems to have squandered that opportunity. 

You can find the code, data, and Excel spreadsheet for the projections above on the site Github page [here](https://github.com/robertritz/mongoliandatastories/tree/main/notebooks/Fuel-Shortage). 


***
#### MDS Newsletter
Thank you for reading. Mongolian Data Stories has a free newsletter! To receive new articles straight to your inbox so you never miss out, [click here to sign up](https://www.getrevue.co/profile/mongoliandatastories). 

