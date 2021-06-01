---
title: "Just what is ‘minimum’ in an MVP?"
slug: "just-what-is-minimum-in-an-MVP"
date: 2021-05-28T17:00:00+01:00
authors: ["Mark Weber"]
draft: false
tags:
- product management
---

The term ‘MVP’ or 'minimum viable product' is one that you can’t escape from in the modern digital age, and in our work in designing the new Royal Opera House TV streaming app its definitely a useful term. As a bit of background, the need for a TV app became apparent when we find that large numbers of our users were struggling to get casting to work. I find that a pretty easy to understand problem - I’ve been using Apple TV since they started, and Apple are meant to get these things right, but even trying to get an iPhone to cast reliably to an Apple TV is a bit of a hit and miss experience. Lately they seemed to have got it a bit better but it's still something I wouldn’t want to rely on - especially not for a live performance. And then when you get to the wild-west of Smart TVs with random bits of tech thrown together - a true nightmare!

![MVP car](https://blog.crisp.se/wp-content/uploads/2016/01/mvp.png)

Anyhow, the big need we identified was ‘I want to watch this stream really easily on a big screen’, and so a TV app seemed the best way. Research has shown us that Fire TV is probably the most used device by our target users, and so we’ve started with that - but we know we’ll need to support other platforms and so are using React Native to build the app to help it to be as portable as possible. 

This week we conducted remote user testing over Zoom calls, which is surprisingly effective. Our lead tester, Deborah doubled up as a TV remote control :-). We’ve gone for a fairly simple design approach and tried to follow things that feel familiar. What was interesting though was how our test users assumed functionality which we’d hoped to be able to avoid as part of our MVP. We found they assumed they would be able to add an item to a watch list, they assumed they could continue on from where they left off, etc. And even though our test mockup didn't illustrate these capabilities, the users didn't actually see they weren’t there - they just assumed it. And that really struck home - that the more a sector matures the less minimum is the ‘minimum’ of an MVP. There are things that users come to expect, and to deliver without them is to deliver a product that is basically not good enough. No matter how much we as developers may promote the idea of MVP as a great way of getting a product to market, we can not escape the reality of user expectations… and that’s the moral of this short story!
