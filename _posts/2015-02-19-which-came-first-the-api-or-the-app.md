---
layout: post
title: Which came first, the API or the app?
date: 2015-02-19 04:44
author: irwinium
comments: true
categories: [Uncategorized]
---
The Caribbean Open Data Code Sprint took place on January 26, 2015.  It's a 24 hour coding competition.  In it, you are given access to specific Open Data datasets and asked to come up with a solution that uses one or more of those sets.  The hosts were the University of the West Indies and the main sponsor was the Caribbean Telecommunications Union.

The sets we had access to are available on <a href="http://data.tt">http://data.tt</a>

Anand &amp; I were talking about The Caribbean Open Data Code Sprint for weeks.

The conversation went like this:
<blockquote>Irwin: Code Sprint?

Anand: Yeah, why not.</blockquote>
So, we were excited, in a way.

When the day for participation came, I was already on my way to the Hyatt. We hadn't confirmed if he was going.  He called,
<blockquote>Anand: Code Sprint?

Irwin: Yeah, why not.</blockquote>
We met up with Nigel (Wallen) who came from Solution by Simulation and he joined up with us.

After discussing a few ideas we settled on the idea of a mechanism for rating secondary schools in Jamaica.  It's so specific because the data we had ready access to came from secondary school performance in Jamaica.  It was fairly comprehensive.  Data listed included:
<ul>
	<li>The number of grade 1, 2 &amp; 3 results.</li>
	<li>The number of passes and fails.</li>
	<li>Metrics were broken down according to subject.</li>
	<li>Beyond that, there was also data on teacher qualification.</li>
</ul>
Our ranking system was necessarily simple, we wanted to use the data to enable an informed discussion on what is the best school to attend.

As we discussed it, 'best school' is at best shakily determined by only using information on pass rates.  But as we said, we wanted to open the conversation.  As implied here, the conversation needed to be informed by data.

We considered on how to present this solution and came up with an application that let's you view the best schools on a map.  How to know the best school though?  We decided to go with an algorithm that computes a score of each school, based on grades.

Once we had that core idea, we approached it by building an API that brings together the school data and the calculation around the score.  As we built out the API, and spent more time crafting  it out and making it make sense, we spent less time on a demonstration app and 24 hours became 18 which became 10 and then 4.

We left the venue to go home and work from there.  That didn't quite work. Anand kept the light burning longest - til around 2am.  We did have a sound, fool-proof plan though - to reconvene very early the next morning.
The next morning there was a four-car smash up that involved one fatality and hundreds of commuters being stranded or stuck in the gridlock of the highway.

One hour before the event, we had a great API, a far less great application, and a decision to make.

Do we go with the tried and failed approach of, "well, we had this great idea for an app but we ran out of time and here is this thing"? Or, do we reexamine what we've done and understand what value that offered in that context?

We went with the latter option.  In our five minute presentation, we chose to focus on the innovation of building an API that married the existing dataset with knowledge and applied insight. We demoed the API - <a title="available here" href="http://best-school.azurewebsites.net/Help" target="_blank">available here</a> &amp; spoke to its ability to then be consumed by other developers and apps - like PowerBI  or Google Fusion Tables.

This edition's judging panel included Chief Knowledge Officer of the Congress WBN,  <a title="Bevil Wooding" href="http://en.wikipedia.org/wiki/Bevil_Wooding" target="_blank">Bevil Wooding</a> as well as lecturers from the University of the West Indies, <a title="Dr Akash Pooransingh" href="http://sta.uwi.edu/eng/electrical/staff/akash_pooransingh.asp" target="_blank">Dr. Akash Pooransingh</a> &amp; <a title="Dr. René Jordan" href="http://sta.uwi.edu/fst/dcit/rene.jordan.asp" target="_blank">Dr. René Jordan</a>.

<a href="https://irwinium.files.wordpress.com/2015/02/opendatacodesprintjudges.jpg"><img class=" size-medium wp-image-68 aligncenter" src="https://irwinium.files.wordpress.com/2015/02/opendatacodesprintjudges.jpg?w=300" alt="opendatacodesprintjudges" width="300" height="200" /></a>

The judges just asked one question and we were done.  A few more teams presented and then we waited for about an hour or so.

When Dr. Mallalieu provided closing remarks, she had this to say:

https://twitter.com/iStarr/status/563792253718495232

"The winning team hit the spot on <a class="twitter-hashtag pretty-link js-nav" href="https://twitter.com/hashtag/OpenData?src=hash"><s>#</s><b>OpenData</b></a>"

<a href="https://irwinium.files.wordpress.com/2015/02/opendatacodesprintdrmallalieu.jpg"><img class=" size-medium wp-image-69 aligncenter" src="https://irwinium.files.wordpress.com/2015/02/opendatacodesprintdrmallalieu.jpg?w=300" alt="opendatacodesprintDRMALLALIEU" width="300" height="200" /></a>

That winning team was us (Team IAN - not very imaginative, sorry). Our API captured a big part of what the Caribbean Open Data Code Sprint was attempting to accomplish and it felt like the start of something good.
