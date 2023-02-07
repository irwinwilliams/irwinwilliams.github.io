---
title: "Basket of (open data) goods"
date: "2016-04-22"
categories: 
  - "advocacy"
  - "trinidadandtobago"
tags: 
  - "finance"
  - "opendata"
coverImage: "screen-shot-2016-04-22-at-12-31-19-am.png"
---

[Last year](https://irwinium.wordpress.com/2015/02/19/which-came-first-the-api-or-the-app), Anand, Nigel and I won the Trinidad and Tobago leg of the Caribbean Open Data Sprint. (woohoo!) It was Anand and my second or third time at the event. We didn't expect to do so well, we largely went for the vibes, bounced up Nigel there and it was nice.

This year, there apparently won't be a Trinidad and Tobago leg for the first time since the thing started.[![Screen Shot 2016-04-22 at 12.38.46 AM](https://irwinium.files.wordpress.com/2016/04/screen-shot-2016-04-22-at-12-38-46-am.png?w=600)](https://www.facebook.com/developingcaribbean/photos/a.275308042533860.65565.266464596751538/1031481413583182/?type=3&theater) However, getting involved in Open Data projects never needs invitation or formalities. If the data's there, people will try to make magic.

Trinidad and Tobago [is in a recession](http://www.guardian.co.tt/business/2016-02-26/deep-recession). So, people have been more price conscious than usual. Not just people but even ministries in government and their units.

One such unit, the Consumer Affairs Division, released [a booklet](http://tradeind.gov.tt/Portals/0/Supermarket%20Prices%20Booklet.pdf) that tracks the cost of goods across a range of grocery stores around the country.

The data was locked in a PDF-formatted file, across 32 pages.

I grabbed the file and spent sometime thinking about how it could be liberated and what could be done after that.

Fortunately, because the PDF itself was structured fairly well, an online service was able to render it as excel. From there, we converted it to a more app and website friendly format - json.

A small site was built which provided a view of the data, and works fine in a desktop browser. The site can be seen here:

[http://irwinwilliams.github.io/price-range/#/prices](http://irwinwilliams.github.io/price-range/#/prices)

I was motivated to do this because it was a good demonstration of the innovation possible as more and more data becomes available.

Edit (April 30, 2016) \[and super-technical note\]:

I really wanted to start some sort of basket functionality on this PoC, and so I just added the start of that functionality into price range.  Ideally, it should do a version of what "Knapsack" does, which is, for a given set of items in the basket, what is the best place to get all the items? #KnapsackInRealLife
