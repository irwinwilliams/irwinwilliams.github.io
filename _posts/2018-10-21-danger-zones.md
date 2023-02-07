---
title: "Danger Zones"
date: "2018-10-21"
categories: 
  - "open-data"
  - "trinidadandtobago"
coverImage: "danger-zones-the-start.png"
---

## TL; DR

I've built a map of the location updates from the Ministry of Works and Transport of Trinidad and Tobago based on flooding and where was/is impassable. You van view it [here](https://little-reaction.glitch.me/).

## "Technical" details

https://twitter.com/iStarr/status/1053284383052972038?ref\_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1053284383052972038&ref\_url=https%3A%2F%2Firwinium.wordpress.com%2F2018%2F10%2F21%2Fdanger-zones%2F

That tweet above is kind of how I got the idea in my head to build out an example of the approach.

When I sat down to do create a version of a good approach, I had all kinds of options in my mind. Should it be rendered on the client or server side? React or Angular? Should I use Google Maps, Leaflet & MapBox or something else? How would I generate the data?  Should I try and parse some tweets? What's the fastest way to get data? Who has the data?

Since I didn't want to spend all evening in analysis paralysis, I just dove in and began pulling things together. I had recently set up a new dev environment, so my regular tools for some ideas weren't restored yet. No node, npm or React was set up. So I started downloading packages, installers and tools.

https://twitter.com/iStarr/status/1054100325941067781

And then I remembered glitch! I literally paused mid environment setup and jumped onto searching in [glitch](https://glitch.com/). Glitch is like online development environment that comes prepackaged with the resources you need to get up and running with with minimal fuss. Now, you have to have a sense of what you want to build and what tech to use. Which I did. A few searches later, I found a great starting point, something that already had the Leaflet stuff built in.

Having the base I wanted, I needed to get the content of these tweets represented as geojson:

https://twitter.com/mowtgovtt/status/1053758911327670272

Again, numerous options, parsers to write and just ideas swirling around. But while spelunking online for stuff to use, I found [geojson.io](http://geojson.io) - a WYSIWIG for generating geojson. I had to handcode the stuff, switching between Google Maps, Open Streetmaps and Waze but I just wanted an early result.

And I got it: [a map](https://little-reaction.glitch.me/) that presents the information that @mowtgovtt tweeted about the state of impassable regions in the country.
