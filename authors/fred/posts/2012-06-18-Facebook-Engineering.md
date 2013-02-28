---
layout : post
title : Engineering at Facebook
author : fred
published : true
date : 2012-06-18
slug : engineering-facebook
category : [technology]
tags : [facebook, engineering, big data]
---
A few years back 90% of the coders at Facebook were PHP engineers and 10% C++. Now the numbers shifted and up to 90% of employees are writing C++. I'm wondering how many people were fired. 

>The Facebook source code is largely written in the PHP programming language. PHP is conducive to rapid development, but it lacks the performance of lower-level languages and some more modern alternatives. In order to improve the scalability of its PHP-based infrastructure, Facebook developed a special transpiler called HipHop.

About HipHop

>HipHop converts PHP into heavily optimized C++ code, which can then be compiled into an efficient native binary. When Facebook unveiled HipHop to the public in 2010 and began distributing it under an open source software license, the company's engineers reported that it reduced average CPU consumption on Facebook by roughly 50 percent.

I always wondered how big the Facebook site really was.

> Because Facebook's entire code base is compiled down to a single binary executable, the company's deployment process is quite different from what you'd normally expect in a PHP environment. Rossi told me that the binary, which represents the entire Facebook application, is approximately 1.5GB in size. When Facebook updates its code and generates a new build, the new binary has to be pushed to all of the company's servers.

Most of it are ressources though 

>The binary executable is just one part of the Facebook application stack, of course. Many external resources are referenced from Facebook pages, including JavaScript, CSS, and graphical assets. Those files are hosted on geographically distributed content delivery networks (CDNs).

Like World of Warcraft, they are using BitTorrent for deployment.

>Moving a 1.5GB binary blob to countless servers is a non-trivial technical challenge. After exploring several solutions, Facebook came up with the idea of using BitTorrent, the popular peer-to-peer filesharing protocol. BitTorrent is very good at propagating large files over a large number of different servers. Rossi explained that Facebook created its own custom BitTorrent tracker, which is designed so that individual servers in Facebook's infrastructure will try to obtain slices from other servers that are on the same node or rack, thus reducing total latency. Rolling out a Facebook update takes an average of 30 minutes—15 minutes to generate the binary executable and another 15 minutes to push the executable to most of Facebook's servers via BitTorrent.

About the frequency of updates

>Facebook typically rolls out a minor update on every single business day. Major updates are issued once a week, generally on Tuesday afternoons. The release team is responsible for managing the deployment of those updates and ensuring that they are carried out successfully. Frequent releases are an important part of Facebook's development philosophy. During the company's earliest days, the developers used rapid iteration and incremental engineering to continuously improve the website. That technical agility played a critical role in Facebook's evolution, allowing it to advance quickly.


*[Source](http://arstechnica.com/business/news/2012/04/exclusive-a-behind-the-scenes-look-at-facebook-release-engineering.ars)*