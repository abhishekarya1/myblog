---
title: The Year 2038 Problem
subtitle: Y2K all over again?
date: 2018-09-21
tags: ["Technology"]
---

## Not Enough Storage
If you know about The Year 2000 problem, also known as the Y2K problem, the Millennium bug, or the Y2K bug, then you know how bad it was.

In short, only the last two digits of a year were used to store the years in computers and most electronic devices in the last century. But, as soon as we hit the year 2000, problems were anticipated, and arose, because many programs represented four-digit years with only the final two digits — making the year 2000 indistinguishable from 1900 or even 3000.

It wreaked havoc and lead to many businesses facing severe setbacks and governments too were affected. It costed around $300 billion worldwide for preparations and fixing the bug. From errors in embedded systems such as elevator chips, medical equipment, airplane autopilots, power plants, nuclear reactors, reports of the failure were coming from every part of the world at that time. A nuclear energy facility in Ishikawa, Japan, had some of its radiation equipment fail, but backup facilities ensured there was no threat to the public. This was how serious it was.

## The Year 2038 Problem
Also called the Unix Millennium bug or the Y2K38 bug. Just like the Y2K problem, it is also caused by the insufficient capacity for storing dates.

The problem is exclusive to devices using the 32-bit format to store dates. 32-bit processors can handle 2<sup>32</sup> different values or 4,294,967,295 different numbers. The systems stores dates and times in 32-bit chunks. In reality that large number of different values is halved for time keeping and other data storage applications as they range from -2,147,483,648 through 2,147,483,647 leaving only 2,147,483,647 positive values from zero.

Actually, most C programs use a library of routines called the "Standard Time Library". This library uses a standard 4-byte format for the storage of time values. The standard 4-byte format assumes that the beginning of time is 1 January 1970 at 12:00:00 a.m. This value is 0. Any time/date value is expressed as the number of seconds following that zero value. You can see the current value [here](http://www.coolepochcountdown.com/). Notice how it increments with each passing second.

The latest time that can be represented in UNIX's signed 32-bit integer(int) time format is 03:14:07 UTC on 19 January 2038, which is 2,147,483,647 seconds after 1 January 1970. Beyond that time, due to integer overflow, the time values will be stored as a negative number and the systems will read the date as 13 December 1901 rather than 19 January 2038.

A similar issue happened with YouTube, where the number of views of PSY's Gangnam Style passed 2 billion and broke the 2,147,483,647 limit of the 32-bit counter Google supposedly used.

Here is an animation showing how the bug will reset the date.

![Y2K38 Bits Animation](/img/Y2K38/y2k38.gif)

You can read more about the same in detail on [Wikipedia](https://en.wikipedia.org/wiki/Year_2038_problem).

## What can happen?



## Solutions
Modern processors that power almost every computer bought today, and are starting to make their way into smartphones and tablets too, are based on a 64-bit system and 64-bit software. They also have a maximum number of different values they can address but at 264 or 18 quintillion values within 16 Exabytes of memory, the ceiling is considerably higher at a date that is over twenty times greater than the estimated age of the universe or 292bn years from now.

## Links

- See the bug in Google Calendar [here](https://www.youtube.com/watch?v=Yg0dXH2O_tg).
-
