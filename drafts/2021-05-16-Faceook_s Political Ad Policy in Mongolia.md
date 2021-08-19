---
layout: post
title:  Does Facebook Ad Policy Work in Mongolia?
date:   2021-05-17 00:00:00 +0800
image:  '/images/'
tags:   [Facebook, politics, advertising, election]
featured: true
---

During last years Parliamentary election in Mongolia I was very interested to learn more about how parties and campaigns would use Facebook advertising to get their message out. It was [reported](https://montsame.mn/en/read/226189) that social media advertising during the 2020 Parliamentary election would be closely monitored by the General Election Commission, the Communications Regulatory Commission, and even Facebook itself. Even more exciting, in January 2020, [Facebook said](https://news.mn/en/790500/) they would set up a "war room" during the 2020 election to combat misinformation and tackle fake accounts. 

All of these signals told me that election advertising during the 2020 Parliamentary election would be closely monitored. Indeed, I heard several anecdotal reports that pages violating election regulations were taken down. However, to my knowledge, there has been no published statistics or data on posts or pages taken down during this period. 

So, as an inquisitive data scientist I went looking for data. I knew that Facebook launched their [Ad Library](https://www.facebook.com/ads/library/) in May 2018 as a response to the "dark ads" of the 2016 election in the United States. The Ad Library, according to it's home page:

> "...provides advertising transparency by offering a comprehensive, searchable collection of all ads currently running from across Facebook apps and services, including Instagram."

The Ad Library allows you to see ads a Facebook page (or Instagram page) is running during a limtied time period. However, if the ads are about social issues, elections or politics, the ads are retained in the Ad Library forever. In addition, these political ads are available via Facebook's Ad Library API, where the data can be downloaded and analyzed.

Obviously, this data source seemed like a perfect fit for what I wanted! After researching several candidates for Parliament I discovered a troubling fact. Only a few ads out of the over 600 candidates were properly marking their ads as political. To be clear, Mongolian election law does not require candidates to mark their ads in this way on Facebook. 

In response, I made a Tweet calling out the disparity between the statements and reality of Facebooks statement.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr"><a href="https://twitter.com/Facebook?ref\_src=twsrc%5Etfw">@Facebook</a> says they are working with <a href="https://twitter.com/gecmongolia?ref\_src=twsrc%5Etfw">@gecmongolia</a> for this election. Hard to believe as <a href="https://twitter.com/ArdiinNam?ref\_src=twsrc%5Etfw">@ArdiinNam</a> are running ads on Facebook without flagging them as &quot;political&quot;. Result: researchers and journalists can&#39;t use the API to monitor campaigns, instead must use manual searches. /1 <a href="https://t.co/JyYQAlgjiZ">pic.twitter.com/JyYQAlgjiZ</a></p>&mdash; Robert Ritz (@RobertERitz) <a href="https://twitter.com/RobertERitz/status/1272523321343651840?ref\_src=twsrc%5Etfw">June 15, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Eventually I discovered the reason for the almost complete lack of ads being marked political. Facebook simply [had not started](https://twitter.com/george\_chen/status/1272776100729372674?s=20) enforcing authorization for political and election ads in Mongolia! 

## Political Ad Tracking Begins

Recently I started looking into Facebook political ads again because of the upcoming Presidential election in June 2021. Imagine my surprise when I find that ads are now being tagged and tracked in large quantities! Facebook turned on authorization for ads about social issues, elections or politics in August 2020. Since then over 7,000 ads have been added to the library and over $130,000 has been spent on these ads (as of May 17, 2021).

- visualization of number of ads since August 2020.

Since August 2020 





## Testing Facebook's Authorization Process



Ad text:
> Монгол улс гуравдагч хөршийн бодлогоо тогтвортой барьж чадах эсэхийг энэ жилийн Ерөнхийлөгчийн сонгууль хариулж чадна. Гадаадын хөрөнгө оруулалтыг дэмжих үү? Гадны хөрөнгө оруулагчдыг гаргах уу? Хамтын түншлэлээ өргөжүүлж чадах уу гэдэг гагцхүү таны сонголтоос хамаарна! Өмнөх Ерөнхийлөгчид, Засгийн Газруудын хүчин чармайлтаар АНУ-ын Конгрессд Монголд зориулсан "Гуравдагч Хөршийн Худалдааны Баримт Бичиг" батлагдсан байна. Гадаад худалдааг улстөржүүлэн гацаах уу, эсвэл энэ боломжийг ашиглаж дараагийн түвшинд гарах уу гэдгийг сонгогч таны мэргэн ухаан шийдэг.

Translations:
This year's presidential election will determine whether Mongolia can sustain its third neighbor policy. Will we support foreign investment? Or will foreign investors be seen out? Whether you can expand your partnership depends only on your choice! Through the efforts of previous presidents and governments, the "Third Neighbor Trade Document" for Mongolia was approved by the US Congress. It is up to the electorate to decide whether to politicize foreign trade or take this opportunity to the next level.


## What's Next?



<blockquote class="twitter-tweet"><p lang="en" dir="ltr">.<a href="https://twitter.com/george\_chen?ref\_src=twsrc%5Etfw">@george\_chen</a> according to TheGuardian Facebook detected politically manipulative behaviour in <a href="https://twitter.com/hashtag/Mongolia?src=hash&amp;ref\_src=twsrc%5Etfw">#Mongolia</a> during last elections and yet this network was never investigated. Care to comment? <a href="https://t.co/DREIaxzGsH">https://t.co/DREIaxzGsH</a> <a href="https://t.co/w4jUW5yQeS">pic.twitter.com/w4jUW5yQeS</a></p>&mdash; Zaya C Bulag (@Zaya\_CB) <a href="https://twitter.com/Zaya\_CB/status/1389208684044165123?ref\_src=twsrc%5Etfw">May 3, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

