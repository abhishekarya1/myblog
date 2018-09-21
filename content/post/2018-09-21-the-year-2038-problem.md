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

The problem is exclusive to devices using the 32-bit architecture to store dates. 32-bit processors can handle 2^32 different values or 4,294,967,295 different numbers. The systems stores dates and times in 32-bit chunks. In reality that large number of different values is halved for time keeping and other data storage applications as they range from -2,147,483,648 through 2,147,483,647 leaving only 2,147,483,647 positive values from zero.
