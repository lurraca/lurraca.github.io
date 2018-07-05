---
layout: post
title: Code Quality Challenge - Part 1 
---

Yep! Is that time of the year again! You know, we are already in the second part of the year, that feeling of the year slipping by you, and you try to get a hold of it by doing more, and for me, this time, doing more means coding outside work hours and writing more.

So that's how this blog post was born. I stumbled upon Ben Orenstein's [30-Day Code Quality Challenge](https://www.codequalitychallenge.com/) and decided that it was something that I wanted to do. The commitment is only 20 minutes a day, and while I that very little can be accomplished during that time, at least it will get me into the habit of doing more which is my goal right now. Just hope that the habit sticks.

Since I will be documenting my journey through the 30-day challenge here in my blog, let's talk about the format of it. It will be a 3 part post (this is part 1), and each part will contain my notes for each of the 10 days.

Now that we know what all this is about let get down to business!

# Day 1 - Clean up your README

The gist of this challenge is to take a project where you are a contributor/maintainer/owner, and apply some house keeping on the README. The idea is that a good README will save time for new comers while trying to use/contribute to the project.

I have to say that this one was a bit tricky for me since at the moment, I am working on [Cloud Foundry](https://github.com/cloudfoundry) and [Cloud Foundry Incubator](https://github.com/cloudfoundry-incubator) Open Source Projects and the projects that I work on have very detailed README.md files.

However, I did went on and added a couple of details to the README.md og a project that I worked for a bit a couple of months ago. [This was the result of it.](https://github.com/cloudfoundry-incubator/gcp-broker-proxy/pull/6/files)

*Note of the day:* 20 mins is not much time. I spent much of the time, looking for something meaningful to add. Got distracted by a question on my team slack, and barely had time to complete a very simple change. Will make an effort on blocking external distractions tomorrow.

# Day 2 - Nuke TODO comments

The logic behind this challenge is that code is not meant to track future work, that there are tools suited for that and your team is most likely already using them (if you aren't, then you should, check out [Pivotal Tracker](https://www.pivotaltracker.com/dashboard)).

I started by running ```ag 'TODO|FIXME'``` on the root of one the repo that I work on. The quantity of "TODO's" and "FIXME's" were surprisingly low for a 6 years old project, with 3000+ files, not counting dependencies and vendor files with a relatively high cadence of developers rotation.

My team focus is only on a specific section of [Cloud Foundry Cloud Controller](https://github.com/cloudfoundry/cloud_controller_ng) which is **Services**, so I decided only to tackle the "TODO's" that affected that section for the moment. There was surprisingly just one, that was not even added by our team, yay!. The commit that introduce it it's 7 months old, so clearly it's been forgotten about.

So I went in, deleted the comment and created a chore in our Pivotal Tracker backlog to do the work that the 'TODO' is describing. There was an specific TODO that caught my eye, is on one of the oldest migrations, that would need a deeper look. Something that hopefully I would tackle in another time. I didn't delete that comment, since is on a part of the product that we don't own, so it will be weird to add stuff to someone else's backlog.

*Note of the day:* Time flew! Didn't do much, but glad that I took out the time to do something, even if small. I will talk to the team about "TODO's" in standup tomorrow, even we are doing an excellent job of not about already. 

*Extra tip:* To count files recursively in a directory 
```find . -type f | wc -l```
List all files in the current dir, and then count each line.

# Day 3 - July 4th? Seriously?!

There were no challenge today since it's the 4th of July... I mean, who cares? According to Google, American are just 4.4% of the world population... get real! And then they ask they rub people the wrong. /rantover

Anyway my quest of 30 days of doing something outside of work hours won't be stopped. I decided to start little project. A CLI tool that wraps around [Ngrok](https://ngrok.com/), and display the host user the exact command other people needs to execute in order to ssh into the host's machine.

I am calling it [ssh-ngrok](https://github.com/lurraca/ssh-ngrok). 

Something like:

```
ssh-ngrok <host-machine-username>

-> ssh <host-machine-username>@ngrok-url.io -p 22
```

I know. I know... it's not rocket science, and barely useful at all. But I just want to learn some Go and keep myself busy after work hours, and it's something simple enough that it won't be hard to finish.

**Note of the day:** 20 mins? More like 2.5 hrs. Oh well!

# Day 4 -  Get rid of a warning

Alright! I had my eye on warning for a while, here on this blog. Every time I pushed to github and that triggered a new a build I got an email from Github Pages alerting me that I the code highlighting library that I had set on my configuration of jekyll was deprecated.

```
The page build completed successfully, but returned the following warning for the `master` branch:

You are attempting to use the 'pygments' highlighter, which is currently unsupported on GitHub Pages. Your site will use 'rouge' for highlighting instead. To suppress this warning, change the 'highlighter' value to 'rouge' in your '_config.yml' and ensure the 'pygments' key is unset. For more information, see https://help.github.com/articles/page-build-failed-config-file-error/#fixing-highlighting-errors.

For information on troubleshooting Jekyll see:

  https://help.github.com/articles/troubleshooting-jekyll-builds

If you have any questions you can contact us by replying to this email.
```
So I went on and did that change, no more warning.In the source code that I contribute to at work don't throw any warning at all, but will definitely keep at eye on it.

**Note of the day:** This challenge took me like 15 minutes, including updating this posts. 
t
