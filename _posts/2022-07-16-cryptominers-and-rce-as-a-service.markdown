---
layout: post
title:  "Cryptomining and RCE as a Service"
date:   2022-07-16 12:47:34 -0700
categories: engineering security threats
author: wolfshirts
---
I just spent a year writing tooling to fight cryptomining at a CI/CD company. It was definitely an exciting opportunity and I enjoyed the time I spent there. I also learned a lot about cryptomining on CI/CD and other RCE as a service type platforms. Some
of it is fairly obvious and other parts aren't.

## Background
Cryptocurrency is big, and it seems to be even bigger in developing nations. Mining for cryptocurrency can be expensive,
not everyone wants to front the cost themselves. Sometimes the cost is more than the currency is worth. Luckily for
cryptominers there's plenty of platforms that offer RCE (remote code execution) as a service, often with a free tier.

Miners will frequently abuse these free tiers. They will run as many tasks as possible, for as long as possible, with the
largest resource classes possible until caught. This costs companies a lot, and most RCE as a service companies actively combat
this abuse.

## Is it worth it?
The first thing people usually ask me when I talk about this is "how much money do they make?" The answer to this is more nuanced than it initially appears, it's relative. 

Cryptocurrency is a global phenomenon, this means it's also a global market. What would be considered low value in the US might be worth a decent amount in a place with a lower cost of living. This means that a software engineer in the US might look at the time investment and decide it's not worth the effort. An engineer in Indonesia might look at the time investment and decide it's definitely worthwhile.

At the time of writing the cost of an inexpensive restaurant meal is around 1.67 dollars in Indonesia, and 15 dollars in the United States. Given this perspective and the global nature of cryptocurrency it becomes apparent that RCE as a service platforms can be very profitable for lower cost of living regions.

## About the Community and Actors
There is a large somewhat underground community of discords, telegram channels. In some cases these channels follow a personality, others are focused on specific providers with teams working towards mining on the provider, others are based around selling working tooling for mining.

The communities aligned around a personality are usually based around an individual on platform like YouTube who is creating working configs/projects to mine with. They'll generally create these projects to disseminate to their followers. Most of the followers tend to be less sophisticated and if one of their projects stops working they'll ask the community leader to come up with something new. Since there is a large segment of RCE as a service providers the community leader will usually work on the lowest hanging fruit to get their followers mining again.

