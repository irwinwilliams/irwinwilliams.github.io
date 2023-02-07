---
title: "Time For Water: The bot edition."
date: "2017-05-02"
categories: 
  - "cui"
tags: 
  - "time-for-water"
---

Back in 2013, I built a small site that took some data that the Water and Sewage Authority released (@wasatnt on Twitter) and remixed it, to make it easier to consume.

https://twitter.com/wasatnt/status/857911550467854340

Recently, @wasatnt released a document detailing the current distribution schedule in this dry season, 2017.  It's a PDF doc, listing the data for all regions in Trinidad and Tobago. Hundreds of rows, I discovered.

It seemed  like a good idea to build a simple bot to provide information about service at a particular area. So, I did. Listed below are some  of the steps it took from prepping the data to working prototype.

- Get the data
    - It's a PDF, so this means downloading and then converting.
    - I converted using https://smallpdf.com/pdf-to-excel
- Clean the data
    - Small PDF gave me an excel workbook with 15 worksheets
    - All the worksheets contained merged cells, so I un-merged them.
    - Delete unnecessary columns
    - Then, I duplicated the row data so that every row could stand on it's own. That's important for the look-ups I'll do later on.
        - I ended up doing this [via a VBA script](https://gist.github.com/irwinwilliams/3ba02698a964d615df34b7af81585f63). I code, it's what I do.
- Convert the data
    - I was going to work with the excel file as is, but that introduced OLEDB issues. So, avoiding that, I [converted the file's contents](https://shancarter.github.io/mr-data-converter/) to JSON.
- Finally, I was able to build a bot, [Time For Water](https://www.facebook.com/Time-for-water-532875436756652/?fref=ts), that would respond to messages with look-ups of the data in the original schedule.
