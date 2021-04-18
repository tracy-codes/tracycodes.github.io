---
title: Coding practices you should learn now, and utilize forever
date: '2019-10-22'
tags: [Dev]
draft: false
summary: These are 5 coding practices I've come to know and love over the last few years that I thiank myself for every day.
images:
  ['https://og.tracycodes.com/**Top%205%20Coding%20Practices**.png?theme=dark&md=1&fontSize=100px']
---

![hero-banner](https://og.tracycodes.com/**Top%205%20Coding%20Practices**.png?theme=dark&md=1&fontSize=100px)

Here are 5 coding practices I've come to know and love over the last few years that I thank myself for every day.

## 1. Standard code formatting

Most codebases are ready more than written. A codebase with consistent formatting is a lot easier to read vs code with varying styles from numerous contributors on a team. Standardized formatting brings about being able to easily scan through code and pick out the bits you need without bashing your head against your desk. Prettier + ESLint + a popular linting config can do all the heavy lifting for you. Do you have a team member who absolutely refuses to use semi colons in their JavaScript? That's fine! Just have them use Prettier ESLint with a predetermined config, this will return errors if they don't follow the code guidelines. When we implemented this exact setup in our codebase, we ended a lot of discussions/heated debate during code reviews and QA.

## 2. Don't code DRY if it doesn't make sense

The DRY (Don't Repeat Yourself) principle is almost a mantra (and sometimes a great interview question) among developers. But, if it's applied without knowing why, then it will lead to some abstract code that is simply too hard to read and understand.

For me and my team, we stick to a "2-copy maximum" rule. This means any function/code can be copied two times in a codebase. If it needs to be copied any more than twice, then we refactor so that the code is completely reusable within the rest of the application without having to copy+paste code constantly. This keeps us from assuming two problems should be solved the same way, at first glance.

## 3. Debug code via logging

You should practice debugging code in your local environment via logs instead of a debugger. For us, we use [Sentry.io](https://sentry.io/) for our logger/debugger in production. Because of this, we're charged "per event", which means logging and events are very precious.

Since we treat logging and events as such, we do debugging on our local machines first to ensure that logs are added in the right place. This, in turn, makes it so that if an exception is handled via Sentry, it is super easy to track down since we don't have a crazy clutter of logging.

## 4. Don't add complication early on

Don't complicate your codebase with features that no user or stakeholder has asked for. This is a problem you need to especially avoid in early product lifecycles. I struggled with this when I first joined my new team. I tried to come out the gate swinging and going above and beyond expectations. You know what this did? Added more questions, more tickets, and even more work on my team's plate.

**This is an anti-pattern.** Adding unnecessary features makes your codebase harder to read and debug. When you onboard new developers, they will find it difficult to differentiate between imporant features and ones that were added at 4am and were backed by a caffeine overdose.

## 5. Setup a CI/CD pipeline early in your project's lifecycle

I can't say this enough. Even if you're on your own with a project, a CI/CD pipeline will reduce the overhad of remembering (and doing) the build and deployment of your codebase.

A common misconception is that CI/CD pipelines are important only for teams that push/deploy a lot of code to production every day. From my experience, even if you're pushing to production once a week, it can save hours. Recently, I introduced a CI/CD pipeline for our main project (deployment used to take several hours as a lot of it was copy+pasting code or uploading code to servers and replacing old files via diffing). After introducing CI/CD, we can run a full production deployment in under 5 miunutes and can rollback in seconds if there's an error.

P.S. having a CI/CD pipeline usually results in having an exact deployment history, linking it to a specific commit. This has helped us during postmortems to find the root cuase for an incident.
