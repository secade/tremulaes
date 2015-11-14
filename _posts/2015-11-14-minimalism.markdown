---
layout: post
title:  Minimalism in Software
date:   2015-11-14 12:51:00
categories: blog
---

When writing software, it's easy to want to plan for the future. We have to plan for edgecases of all varieties, build our applications to be scalable and resilient enough to operate under every scenario that we can imagine. Software servicing hospitals, for example, need to be available 100% of the time and the solutions to providing that level of uptime are complex and expensive, but it's essential that these services are available without fail for the hospital to run efficiently. Lives depend on it.

But what happens when we start to plan out for things that *aren't* strictly necessary? What happens when we start pumping in additional complexity because we likely will need to handle it in the future, or simply think that we will? Or when we use tools that aren't appropriate for the use case at hand? What happens when considering extensibility of a codebase crosses into the territory of trying to predict the future?

We waste time. On the surface, bits of time wasted here and there may not seem like they're too concerning, but time is perhaps our rarest resource of all. Minecraft is a beautiful lesson in understanding that no capital is more valuable than time itself. Neil Fiore says it best:

> There’s a myth that time is money. In fact, time is more precious than money. It’s a nonrenewable resource. Once you’ve spent it, and if you’ve spent it badly, it’s gone forever.

Approaching software and application development from a minimalistic mindset can, in the end, save yourself and your team a great deal of stress, money, and even better, time itself.

## The Second Expression of Minimalism

There are two primary ways in which minimalism can be achieved: first, in doing no more than necessary, and second, using tools that best suit the situation, or choosing to build one if no such tool exists.

Laziness is often lauded as one of the chief personality traits of a software engineer, and it's perhaps one of the most important. Writing no more lines of code than the situation at hand demands, adding in no additional features, and allowing the core concept shine through are important at any stage of product development, regardless of the domain. Be minimal, be small.

Just because you know a feature is coming down the pipeline later on doesn't mean you should begin building a place for it in your codebase. Plans change, pieplines are disrupted and roadmaps are set on fire *every day* for all sorts of reasons, and when you've made room for a feature that is never implemented, you're left with a gaping hole of dependencies and anti-patterns that can leave your spaghetti code leaky. This is a commonly taught and understood principle in software design.

But even beyond "Be lazy and do as little as possible", choosing inappropriate tools to solve your problems can lead to much of the same waste. I recently had the pleasure of working on a codebase in a Perl MVC framework called Catalyst. Originally designed as a scripting interpreter, Perl grew in popularity due to it's core tenets of "There's more than one way to do it" and "Easy things should be easy and hard things should be possible." In it's original conception, Perl was a great solution for a wide variety of problems due to its flexibility.

But then it grew too flexible. As new versions came out, it gained features and paradigms from other frameworks, until Object Oriented Programming was slapped on top of the otherwise procedural language. Eventually, frameworks were built out of the core language, and thus the Catalyst MVC web framework was born, and years later I found myself frustrated.

Perl was not originally intended for this use case at all, and it's strengths and weaknesses no longer lined up with its use case as an MVC framework. When compared with languages much more suited for web development (Ruby and Python are great examples), Perl feels unwieldy *because* it is unwieldy. Regardless of what made sense in the past, the reality is that better tools exist now to solve the problems that Catalyst use to solve. The issue isn't that Perl was designed to solve all of these problems, is that we are continuing to try to use it to solve problems that it is no longer the best tool to solve.

Even Rails provides a good illustration of tools not suiting needs as they change. It is often stated that "Rails doesn't scale well", and Twitter is held up as an example of why Rails fails after a certain load breakpoint. Older versions of Rails likely *weren't* very scalable; it's original use case was nowhere near the scale of where web applications like Facebook and Twitter are at today. However, Rails has responded and, in line with other technological advancements, now can provide fast, scalable ecosystems that works for many use cases in modern web applications. In this case, the tool evolved to continue solving the problems as they themselves changed over time.

As more and more ground in the technical space is exposed and explored, companies like Facebook, Microsoft, Amazon and Google are finding that existing tools are no longer sufficient to solve their problems. Instead, they build out their own internal solutions and often share their solutions with the world with some form of OSS. Sometimes they adopt and improve on existing tools, but other times they build out new languages, frameworks or ecosystems, all to solve the problem *at hand*.

## Reading the future

Minimalism will likely always be a core tenet in software. So long as knowing the future is impossible, building expectations for the future beyond core extensibility remains impractical. As plans change, people change, the domain changes and requirements change, sometimes in very rapid succession, the sure-to-be-needed feature may get tossed aside for other more pressing concerns. 

As people writing software, it's not our job to be clairvoyant; it's simply to solve problems. Let's make sure we're solving the problem at hand.
