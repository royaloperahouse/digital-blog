---
title: "AWS Game Day"
slug: "aws-game-day"
date: 2021-09-23T17:00:00+01:00
authors: ["Thomas Meehan"]
draft: false
tags:
- work training aws
---

![AWS Gameday](/images/aws-gamedays.png)

On Friday last I was given the chance to take part in an AWS Game Day by my team here in the ROH.

Well that sounds a bit grand for something that basically involved skipping stand up to play around on AWS.

What it involved was watching an intro on Twitch with some very enthusiasitc representatives who explained that we would be acting as employees of a Unicorn rental business whose CEO had recently drawn the ire of Keanu Reeves fans by publicly trash talking him.

This resulted in some rather strange behaviour on the site namely:

```
1) Our database has been getting sudden bursts of traffic erratically, and from places
that are not our web servers. This never happened before. Can you stop these connections?

2) Someone keeps deleting the .css and background image from our S3 bucket. Can you put 
these back so our website looks right? If you want to see the website, go check out the 
DNS record in the application load balancer.

3) We are getting some really weird requests to our application (like whatever this is: 
"/Users.php?uid=1%20or%201=1"). We think this is the result of why some users are 
reporting strange changes in their accounts.
```

We were then assigned to 3 person teams composed of randomly assigned participants and given three hours to debug and fix the situation. The gameday dashboard and link to a dummy AWS console where available to us and we discussed the problem on a Chime call. My team was composed of another UK based dev and a woman in India. 

The first issue was the easiest to fix as it was obviously an issue of an overly permissive security group attached to the database instance in RDS. 

The second had us stomped as we figured it was permissions on the S3 bucket but it took a bit of googling and some help from the occasional AWS helpers to get right. There was also a bonus question on this one which required us to find the AWS account number of the user who was removing the missing assets. This was done by exporting Cloudtrail logs to Athena and then invistigating what account was deleting objects in the bucket.

The third we figured was an attempt at SQL injection but it took awhile to get to the root of it. The solution was to implement a condition in AWS WAF attached to the load balancer in front of our application. This then caught all the suspicious traffic which also allowed us to answer a bonus question of identifying the recipent of attempted malicious payments. We managed to figure that the main benificary was one Neo Anderson.  

So we managed to answer all the questions and got our unicorn business back on line. We did get full marks but we finished 8th overall based on who reached full marks first. As an experince it was enjoyable. 

So if you get a chance I'd recommend taking part in a Game day you get the chance to use some unfamialar AWS services but also spending the morning chatting with some interesting people from around the world not to successfully debugged the issues with a group of stangers.