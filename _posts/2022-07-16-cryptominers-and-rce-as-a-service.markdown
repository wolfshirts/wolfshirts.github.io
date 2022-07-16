---
layout: post
title:  "Cryptomining and RCE as a Service"
date:   2022-07-16 12:47:34 -0700
categories: engineering security threats
author: wolfshirts
---
I just spent a year fighting cryptomining at a CI/CD company. It was definitely an exciting opportunity and I enjoyed the
time I spent there. I also learned a lot about cryptomining on CI/CD and other RCE as a service type platforms. Some
of it is fairly obvious and other parts aren't.

## Background
Cryptocurrency is big, and it seems to be even bigger in developing nations. Mining for cryptocurrency can be expensive,
not everyone wants to front the cost themselves. Sometimes the cost is more than the currency is worth. Luckily for
cryptominers there's plenty of platforms that offer RCE (remote code execution) as a service, often with a free tier.

Miners will frequently abuse these free tiers. They will run as many tasks as possible, for as long as possible, with the
largest resource classes possible until caught. This costs companies a lot, and most RCE as a service companies actively combat
this abuse.

## Is it worth it?
The first thing people usually ask me when I talk about this is "how much money do they make?". The answer to this is more nuanced than it initially appears, it's relative. Cryptocurrency is a global phenomenon.