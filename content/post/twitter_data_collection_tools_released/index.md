---
title: Twitter Data Collection tools released
date: 2012-08-05T15:51:23+11:00
layout: post
profile: true
aliases: 
  - /2012/08/05/twitter-data-collection-tools-released/
tags:
  - Internet
  - Science Communication
  - Social Media
---
I have released the Java programs that I've been using to collect data from Twitter for my PhD since November 2009.

It is suite of programs that use the Twitter Search API and Twitter Stream API to get tweets and then store them in a mySQL database. They have been tested on Mac OS X and Debian Linux.

The Java source is split into 9 Eclipse projects using Maven to bring in the external library dependencies.

For people who just want to use the tools, I've included the runnable Java files for the main modules and the shell scripts and a suggested cron file to run them in the Example directory. The [README.MD file in the Example directory](https://github.com/brendam/tStreamingArchiver/tree/master/Example#example-of-how-to-use-tstreamingarchiver) has instructions on how to create the mySQL databases and configuration files.

The **tStreamingArchiver** project code is available on GitHub: https://github.com/brendam/tStreamingArchiver.

Please tell me if you find it useful.
