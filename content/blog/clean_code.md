---
title: "The Joy of Clean Code"
date: 2022-02-11T12:00:00
description: "My first blog in my 'joy of' series"
author: "Russ Davey"
type: "post"
---

# The Joy of Clean Code

“So if you want to go fast, if you want to get done quickly, if you want your code to be easy to write, make it easy to read.”
― Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship

## Introduction
Welcome to my blog! This is hopefully the first in a series of blogs covering some of the best software engineering and ways of working practices there are in today’s modern tech world.

But with a difference, there are many very good blogs and YouTube videos out there already that cover these topics in great detail, however, to quote Albert Einstein, “If you can’t explain it to a 6-year-old, you don’t understand it yourself,”.

So my aim in these blogs is to attempt to use clear language, metaphors (and a few memes) to explain these concepts in a way that anyone, including non-techies, can understand, even if it’s only for myself.

And hopefully encourage the adoption of these great practices which can help any tech company build happy, highly efficient and effective software engineering teams.


## Working Environments
For every profession there is an environment the workers have to work in, if you’re a doctor you could be working in a hospital, or as a mechanic, you probably need a workshop.

In each environment, they have the tools and information they need to get the job done, and having a workspace that works well for them can determine how quick and effective they can be.

But the macro environment is only part of it, in each case, there’s something that needs discovery and requirements that needs working on, and each thing could be very different from the last, some easy to work on and some much harder.

For example, if you’re a mechanic and the car you’re working on has been carefully designed to allow it to be easily worked on, you’re in for a good day, however, if the part you need to work on is buried deep within the machinery and requires a lot of time and effort before you can even start, then the job becomes a lot harder.

After a quick google search, the Wrangler Jeep looks like a mechanic’s dream and the The MINI Cooper a mechanic’s nightmare.

Not only does the extra work cost time and effort, but it also has a real cost in terms of money for the customer to who it belongs, who will have to wait while the experts charge by the hour for labour.


## Now back to Software
In software engineering it’s a very similar concept, the macro environment could be your infrastructure (cloud environment) and pipelines (how your software gets shipped), all very important and will be covered in another blog.

And the customer could be anyone, another team that requires something to change or something new, or the end user who’s patiently waiting for a new feature.

In either case, the “Service” — software that runs the automated tasks, needs work done, and this can be comparable to the car mentioned above, but with one big difference. The car may have been built by someone else, or you may have been the one who built it.

There are now two elements to the story, you can be either or both the manufacturer and/or the mechanic, but mostly the problem is the same, as this meme clearly demonstrates:

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*vb13YWSR-wOWFViX.jpg)

It’s very easy to lose context about something you’ve built if you haven’t worked on it for a while, leave it long enough and you’ll be the mechanic to the very thing you’ve manufactured.


## What is Clean Code and How Does This Help?
So here we are, imagine you’re a software engineer (if you’re not already, and if not, why not?). You’ve been asked to fix a bug in the code in a service you’ve been working on, but you find the code is quite hard to read and navigate, even though you’ve written most of it yourself.

The bug has plenty of places to hide in because there’s so much code, and like the mechanic working on a difficult car, you have to shift through all the machinery until you reach the part you want to fix.

This has a cost in terms of time, not only for the engineer but also for those waiting for the bug to be fixed.

Eventually, you find the defect and start working on fixing it, but you hit more issues, fixing it requires you to rip out other parts, parts that were working fine before, and thus you hit the same issue and the problem gets bigger.

This kind of scenario can happen quite often in software engineering, and to me, the biggest cost is to the morale of the person trying to fix it… it does not spark joy.

However, imagine the code within the service has been beautifully constructed like the Jeep, it’s clear and obvious where to find the parts you want to work on, everything is written more or less in plain English, and it’s quick and easy to work with.

Fixing one thing doesn’t break another, and what’s more, if you do make a mistake there’s something to tell you that it’s broken before you put the car on the road, and if you try, the engine won’t even start (automated testing).

Sounds too good to be true, doesn’t it? Well, there’s a lot to deconstruct here as there are many practices in play, but they all have synergy and they all work to give engineers a happy place to work.


## Writing Clean Code
Clean code does pretty much what it says on the tin, the code is clean.

In software there any many languages you can choose to code in, a software language is a tool and they are all slightly different with pros and cons in each, but fundamentally they are there to translate something humans can understand into something a computer can understand.

Sometimes you can pick the best tool for the job, but also sometimes the cognitive load of learning a new language outweighs the benefits, for example, if you want something quick and easy but don’t have to worry about performance, you could pick Python.

Or if you wanted something that’s highly performant but requires a bit more investment in learning, then GoLang is a good choice.

However, the language is irrelevant when it comes to writing clean code as the principles are universal.

It’s not only computers that have to read and understand your code, it's other humans, and yourself as well.

Here are a few tips on how to write clean code:

* **Use well-named functions and variables:** a function should describe in simple terms what exactly it does and if possible what it returns, if the name is too long it can mean that your function is too long, try to break things down into smaller understandable and testable parts.
Same with variables, you should be able to read the name and understand to a degree something about the data it holds.

* **Simple code:** write the code for what you need it to do now and remove anything that isn’t used. Abstract code away into functions and chain them together (some languages are easier than others for doing this), so that on the surface you can read in plain English what it’s doing while allowing the person reading it to dig deeper into the code if they chose too.
The less verbose the code the better.

* **Use consistent naming and styles:** once a person gets used to the code it becomes very easy to navigate if the same naming conventions and design patterns are used consistently. Imagine two different cars welded together, how difficult it could be for the mechanic to move from one half to the other.
Minimalize the use of conditions: lots of if/else logic gates can be very confusing to read as you have to try and follow the different paths, it can also lead to bugs. Moving predicates into functions or using switch statements can allow you to make your code very readable. i.e. a function could be called endOfFile and your logic can sit in there, then in your code, you can call it by: if endOfFile(line, maxLines) { <do something> }, instead of an if/else statement which you’ll need to translate in head first to understand what it’s checking against.

* **Group similar functionality together:** creating a namespace, or package or class and grouping together the code you need for a particular task there can make things easier to find and maintain. Even if it’s just a place to store misc helper functions.
Reuse code: try to reuse existing functions as much as possible, even if it means expanding them to take some extra arguments, you’ll be amazed at how much less code you’ll need to write.
For a deeper dive into writing clean code I highly recommend reading Clean Code: A Handbook of Agile Software Craftsmanship by Robert C. Martin.

## But isn’t That a Lot of Work?
It can be, it takes practice and discipline and sometimes you just need to get something done without worrying about how it looks, and that’s where XP and agile software development can really enhance writing clean code.

## Test Driven Development
I would always highly recommend Test Driven Development (TDD) as a minimum or Behaviour Driven Development (BDD) if you want to take it to the next level.

My good friend Mark Bradley has an awesome YouTube channel dedicated to software testing if you would like to explore this more: https://www.youtube.com/c/TestingAllTheThings

There are many many benefits to TDD which I won’t cover in this blog, but one thing it allows you to do is the red/green/refactor approach to writing software.

RED: Write a failing test (frame the problem you want to solve but specify what you want the outcome to be, without having to think about the code or implementation)
GREEN: Get the test to pass with the minimum amount of code (even if the outcomes are hardcoded in)
REFACTOR: Now you can write the implementation and keep testing until you get to the desired outcome, and if you have the rest of your code tested, it means anything you do which breaks something else, is identified instantly.

It’s the refactor step that really allows you to get into writing clean code, for the first iteration you may write something that’s a bit hideous but is quick and does the job.

In the second iteration which can be done straight after (or say you revisit the code when you have more time) you can refactor the code, making it easier to understand and just nicer to read, but here you don’t have to worry about breaking anything or solving the problem you’ve already solved.

This gives you a lot more freedom to focus on the clean aspects, if your tests fail you know you’ve broken something and can fix it.

## Conclusion
Ok, so my aim wasn’t really to write this for 6-year-olds, as in reality there aren’t many 6-year-old software engineers in the industry at the moment, but hopefully no matter your age, experience or background you’ve found this blog post useful.

In my opinion, writing clean code can give you a really good feeling about your work, to quote an agile term “morale is a multiplier for velocity”, from what I’ve seen this couldn’t be more true.

Taking real pride and having software craftsmanship over your code will not only greatly benefit you, but your good deeds will help all those who have to follow in your footsteps.

Having a safe, clean, stress-free environment to work in is the best we can hope for and writing clean code is a huge step towards that in the software engineering world.

Thanks for reading!
