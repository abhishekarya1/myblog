---
title: The Year 2038 Problem
subtitle: Is it the Y2K bug all over again?
date: 2018-09-21
tags: ["Technology", "Programming", "Security"]
---

## Not Enough Storage
If you know about The Year 2000 problem, also known as the Y2K problem, the Millennium bug, or the Y2K bug, then you know how bad it was.

In short, only the last two digits of a year were used to store the years in computers and most electronic devices in the last century. But, as soon as we hit the year 2000, problems were anticipated, and arose, because many programs represented four-digit years with only the final two digits — making the year 2000 indistinguishable from 1900 or even 3000.

It wreaked havoc and lead to many businesses facing severe setbacks and governments too were affected. From errors in embedded systems such as elevator chips, medical equipment, airplane autopilots, power plants, nuclear reactors, reports of the failure were coming from every part of the world at that time. A nuclear energy facility in Ishikawa, Japan, had some of its radiation equipment fail, but backup facilities ensured there was no threat to the public. This was how serious it was.

![Y2K](/img/Y2K38/y2k.jpg)

It cost around $300 billion worldwide for preparations and fixing the bug.

## The Year 2038 Problem
Also called the Unix Millennium bug or the Y2K38 bug. Just like the Y2K problem, it is also caused by the insufficient capacity for storing dates.

The problem is exclusive to devices using the 32-bit format for storage. A 32-bit processor can handle 2<sup>32</sup> different values or 4,294,967,295 different numbers. The systems stores dates and times in 32-bit chunks. In reality, that large number of different values is halved for timekeeping and other data storage applications as they range from -2,147,483,648 through 2,147,483,647 leaving only 2,147,483,647 positive values from zero.

Actually, most C programs use a library of routines called the "Standard Time Library". This library uses a standard 4-byte format for the storage of time values. The standard 4-byte format assumes that the beginning of time is 1 January 1970 at 12:00:00 am. This value is 00:00:00 UTC, referred to as the epoch. Any time/date value is expressed as the number of seconds elapsed since that zero value. You can see the current value [here](http://www.coolepochcountdown.com/). Notice how it increments with each passing second.

The latest time that can be represented in UNIX's signed 32-bit integer(int) time format is 03:14:07 UTC on 19 January 2038, which is 2,147,483,647 seconds after 1 January 1970. Beyond that time, due to integer overflow, the time values will be stored as a negative number and the systems will read the date as 13 December 1901 rather than 19 January 2038.

A similar issue happened with YouTube, where the number of views of PSY's Gangnam Style passed 2 billion and broke the 2,147,483,647 limit of the 32-bit counter Google supposedly used. Most time critical systems today use that C code and are prone to failure. For systems working with future dates, we should have fixed that by now, if these systems deal with dates 20 years ahead or more.

Here is an animation showing how the bug will reset the date.

![Y2K38 Bits Animation](/img/Y2K38/y2k38.gif)

You can read more about the same in detail on [Wikipedia](https://en.wikipedia.org/wiki/Year_2038_problem).

## What can happen?
The biggest problem are the embedded systems as we cannot provide software updates to those systems, we have to manually replace them. Automobile systems like the anti-lock braking systems, aircraft using inertial guidance systems and GPS receivers, mobile phones and Internet appliances are the ones which we have to look out for and fix within time.

![xkcd: 2038](https://imgs.xkcd.com/comics/2038.png)


## Solution
At the moment, there's no universal solution for the Year 2038 bug. Modern processors are starting to make their way into smartphones and tablets too, are based on 64-bit architecture and use 64-bit to store data. They also have a maximum number 2<sup>64</sup> or 18 quintillion values, the ceiling is considerably higher at a date that is over twenty times greater than the estimated age of the universe i.e. 292 billion years from now.

Apple’s OS X desktop software has been exclusively 64-bit since the release of Mac OS X 10.7 "Lion" in 2011.

We can also recompile programs with the new C standard time library, upgraded to store time in 8-bytes (64-bits) format.

The changes are being done, and according to the experts, the Year 2038 problem shouldn't be much hard to fix. And we've learned a lot form the Y2K problem, this issue is well known about and studied, but the devices which won't be receiving any updates will surely be bricked after 3:14:07 UTC on 19 January 2038.

## Links

- See this video to learn about the Y2K38 bug - [Numberphile](https://www.youtube.com/watch?v=QJQ691PTKsA).
- The Y2K38 bug in [Google Calendar](https://www.youtube.com/watch?v=Yg0dXH2O_tg).
- A real-time [UNIX Clock](http://www.coolepochcountdown.com/).
