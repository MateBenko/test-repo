author:Brandur Leach;
date:February 22, 2017;
pic:/assets/img/ben-144x144.png;
topic:Board;
title:Designing robust and predictable APIs with idempotency
===

Networks are unreliable. We’ve all experienced trouble connecting to Wi-Fi, or had a phone call drop on us abruptly.

![alt text](/assets/img/blog-illustration.png "blog illustration")

The networks connecting our servers are, on average, more reliable than consumer-level last miles like cellular or home ISPs, but given enough information moving across the wire, they’re still going to fail in exotic ways. Outages, routing problems, and other intermittent failures may be statistically unusual on the whole, but still bound to be happening all the time at some ambient background rate.

To overcome this sort of inherently unreliable environment, it’s important to design APIs and clients that will be robust in the event of failure, and will predictably bring a complex integration to a consistent state despite them. Let’s take a look at a few ways to do that