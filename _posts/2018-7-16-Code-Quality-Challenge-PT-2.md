---
layout: post
title: Code Quality Challenge - Part 2 
---

**This is *Part 2* of Code Quality Challenge day to day post. It all [started here](http://lurraca.com/Code-Quality-Challenge-PT-1/)**

I have to be honest, I fell off the wagon for a bit. I skipped updating the post for a day, next day I missed the exercise enterily and next day was a Friday and was going out of town so I couldn't catch up or even do the exercise for that day.

But I am back, and that's what matters. Consistency, not perfection! I really need to learn how to deal with the fact that it can be good, even if it's not perfect.

# Day 11 - Run your tests with your wifi off

Run both our main repos [Cloud Foundry Cloud Controller](https://github.com/cloudfoundry/cloud_controller_ng) and [GCP Broker Proxy](https://github.com/cloudfoundry-incubator/gcp-broker-proxy) with no internet connection and just as expected all our tests are passing. It wouldn't make any sense for us to depend on a external system for our tests.

This is a nice exercise since I am sure that this has been an issue in other projects where everything is part a single system.

