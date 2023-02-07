---
title: "The Mark of a Good Programmer"
date: "2016-12-11"
---

"[_The mark of a mature programmer is willingness to throw out code you spent time on when you realize it's pointless. (Bram Cohen)_](https://bugzilla.xamarin.com/quips.cgi)"

I saw that quip on the Xamarin bug list.

I'm building an IoT solution using a Raspberry Pi 3 device. It's been a while since I looked at the solution, so I ran, "[sudo apt-get update](http://askubuntu.com/questions/222348/what-does-sudo-apt-get-update-do)" to refresh the OS and various utilities on the Pi. After the slew of upgrades, things seemed to be faster and amazing.

Included in those upgrades was one that moved my version of mono (I use C# on the Pi) from 4.0.something to 4.6.2. Which led me to exceptions like listed [here](https://bugzilla.xamarin.com/show_bug.cgi?id=27169). Problems with SSL authentication. I spent a few days digging around for solutions. I went from [custom SSL handler code](http://stackoverflow.com/a/33391290/27483), to setting up a reverse proxy with [nginx](https://bugzilla.xamarin.com/show_bug.cgi?id=26658#c7), to trying to use [libcurl](https://github.com/masroore/CurlSharp).

When I have a solution that worked and then "suddenly" stops working, I generally find myself trying to find a quick approach that lets me move on to what I actually want to build. This strategy is very breadth-first. After all, that thing that stopped working, as far as I'm concerned, **worked**, so I'm about to make the next big thing. I don't want to redo that which I've already covered. So searching gets frantic sometimes. And I get distracted more easily.

Which brings me to that quote above. I just kind of caught me in that place between distraction and frustration. As I thought about it, a big part of what I was doing on the Pi and that bug was tied to a strong desire to keep my solution working in C# even though there was a likely better approach with some other stack on the device. So, I switched, used Node.js for where the communication pathway was breaking down and I could move on.

I don't expect this is the final architecture for what I'm building, but it lets me build out higher priority areas, while that bug gets resolved or I understand with a bit more depth what broke between versions. Either way, here's to realizing pointlessness.
