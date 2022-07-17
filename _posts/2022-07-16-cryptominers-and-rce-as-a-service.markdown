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
 
## About the Communities
There is a large somewhat underground community of discord and telegram channels. In some cases these channels follow a personality, others are focused on specific providers with teams working towards mining on the provider, others are based around selling working tooling for mining, and there are some tight knit groups solely focused on earning profit for their group.
 
The communities aligned around a personality are usually based around an individual on platform like YouTube who is creating working configs/projects to mine with. They'll generally create these projects to disseminate to their followers. Most of the followers tend to be less sophisticated and if one of their projects stops working they'll ask the community leader to come up with something new. Since there is a large segment of RCE as a service providers the community leader will usually work on the lowest hanging fruit to get their followers mining again.
 
Communities aligned towards specific providers will generally be a group working towards mining or RDP on a specific service. Usually there will be a few people capable of making projects and getting around detection, and their friends who are along for the ride. These communities rarely stay specific to one provider. Providers actively try to combat this form of abuse, and staying on one when there's lower hanging fruit on another is a waste of effort. They may refocus on their primary target occasionally, but generally they'll become mining communities that are platform agnostic.
 
Sales communities are interesting. In my work I saw projects that were attested to work up for sale, but I wasn't going to purchase a project. It also seemed that most of the sales were conducted via DM. I didn't see as many requests for new projects in the sales communities. It's possible they weren't selling anything at all, the channels themselves were generally just advertisements for working projects for platform X.
 
The tight knit groups/single individuals focused on earning profit were generally fairly inaccessible. I learned that they existed through watching projects and styles, seeing their names come up, and opsec failures. These actors were persistent, and often skilled. They would frequently be using full automation through the entirety of their campaigns. They would run large volumes, when detected they would iterate and attempt to work around the detection. They would change tactics, they would change coins, they would change tooling. Anything to evade detection and continue mining.
 
## The Takeaway
Anywhere you can execute your own code for free, there will be cryptomining. Often it takes companies some time to realize this, usually it gets realized when they're on fire. Word of working RDP or cryptomining spreads fast through the communities. If a platform is particularly appealing then it will also attract groups/individuals with the capability to overcome many forms of automated remediation.
 
If you're running a service that allows for any type of remote code execution, then you likely have cryptomining happening. All of these services have different ways that cryptomining is executed, different platform architectures, and different acceptable loss thresholds. This means there isn't a one size fits all easy solution. Building a solution in house can take some time.
 
If you're about to build a platform where code can be executed for free by a user, you should think about how you will detect and remediate cryptomining. This should be part of your platforms architecture from the start, it will save you a lot of headaches and money down the road. If you're an older company getting caught up in attacks due to the popularity of cryptomining, you probably already have an anti-abuse team, and are writing custom software in house.