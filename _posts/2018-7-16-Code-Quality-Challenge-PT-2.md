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


# Day 12 - Investigate your slowest test(s)

Happily enough only #10 on the top 10 slowest tests for [Cloud Foundry Cloud Controller](https://github.com/cloudfoundry/cloud_controller_ng) is on /services. The tests doesn't seems to be doing nothing wrong, the implementation seems to be doing quite a lot. I feel that the drive to change the implementation needs to be bigger than this specific tests runs slow (1.7 seconds, which is a lot) in order to dedicate resource to make a change to the implementation specially since this is legacy code that i don't fully have context on.

# Day 15 - Improve one name

I couldn't find anything that desperately needed a change. I feel that this might be to my lack of overall context of the project. While I remember some conversations were we team members used different terms to describe the same thing, I feel that we didn't reach an agreement on the best way to call things.

**Note of the day:** Last couple of exercises have no op for me. Have to admit that in a large codebase, 20 mins might not be enough to find the issues that these exercises describe.

# Day 16 - TBD
