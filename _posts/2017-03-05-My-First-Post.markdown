---
layout: post
title:  'My First Post, a rant about my professional experience'
date: 2017-03-05
categories: management development Java
---


I have always thought that writing a blog is arrogant (why my opinion should have more value than any of the 100 million blogs out there ?), and since I decided to start writing one, I will go fully arrogant (note how much the “I” will be used) and narrate my career, and especially the pitfall of a modern world career I was able to see for myself (of course I will avoid using explicit names, as ex colleagues or companies I worked for will be able to recognize themselves)

My real first job as a developer was to create some front-end carousels, improving the responsiveness of the website, and probably as many of us, I was working as a contractor. And being quite young and naïve, I went to every daily meeting (you know the thing supposed to last only 15 minutes…), and we see there that there is a real issue (actually I have seen it on every project I was asked to participate to a daily meeting), between people making jokes, people reading out loud their codes, and so on and so forth… And before you know it, it is already time to go for lunch. Amazing, if we are 16 team members, (number chosen for the ease of computation), and the meeting last 1 hour 15 minutes (unfortunately it is not as rare as we would hope), we have lost 2 days of work (with an average of 8h of work per day)… It seems that we need micromanagement everywhere, developers are little kid that if you don’t ask him (or her) to show his homework every day, then he won’t work. (probably the case for some, but I’d bet it is not the majority).  

My 2 penny suggestions to get closer to a resolution:

1.     Don’t bother and walk out of the door after 15 minutes (I’m pretty sure a manager has a ridiculous request for you to process, like modifying by 2 pixels in height the component it took you 8 hours to put in the right place…)
2.     Yell, and yes yelling appears to be the only way to get something (more on that later), to use tools such as Jira, because if you think about it for 2 seconds, Jira has everything in it for micromanagement lovers, no need to come and bother everyone, every 15 minutes asking “Did you commit? Did you commit?” or “Did you solve the issue?”…


A second pitfall are the middle managers (do we know what they are doing exactly ?), you do a perfect job, go for the “extra mile” as some like to say, do everything possible to improve the quality of the output, and then suddenly you realize that your job is not exactly what it ought to be. So being naïve again, consult with your colleagues, and then mail the (middle) manager with something like “Hey we have issue on A, B, C, can we have a meeting”. And how does it go you might ask, well here it is:

* Simple worker: ”Can we change A,B,C”
* Middle Manager: “A and B is ok, C is definitely not”
* Simple worker: “Brilliant, thanks a lot” (of course never expect to get a 100% in a negociation)

3 months later

* Simple worker: “Where are the modifications on A and B ?”

* Middle manager: “It is still in talk, we will keep you informed”
* Simple (naïve) worker: “All right cheers!”


6 months later

* Simple worker: “Still talking on A and B ?”
* Middle manager: “Yes …”
* Simple (naïve) worker: “All right here is my resignation”


Seeing that makes me think of 2 solutions:

1.  Leave the company
2.  Yell

Obviously if you stay nice and friendly, nothing happens, anyone is happy to delay any changes, however when being put under pressure (like resignation) I saw some differences: “Oh we will give you this and that, please stay!” So in the end there are really only 2 solutions, get the hell out, or fight like a maniac. And I do believe that in the tech industry, we have the chance of being needed so except if you start showing off private parts at work, there is literally 0 chances to get fired for this (perhaps there are more than 0 depending on the quality of work provided, although even in this case, I would guess it is pretty low from what I saw and see at several workplaces)

And finally (actually I wanted to make a nice first article, but go figure, ranting is easier), I am writing this last part regarding you,yes you dear developer (although if you’re not a developer I’m not sure exactly why you would be reading this article), all the things I have heard from developers, Experts as they like to be called, and that are completely preposterous (is Stackoverflow still a thing), not understanding, and even worse, not trying to understand (I also find excuses myself, to immediately regret it afterwards, and spend the rest of my day whipping myself), I just want to use an old saying RTFM, especially upon hearing:

·         “This component does not work how you described, after testing, we see that the conclusions differ from your affirmation” -> Answer: An “Expert” told us the opposite (You gotta love this argument…)
·         There is a bug? -> Answer: Oh we don’t care, it’s for later (Then why the heck you wasted your time on this and commited it….)
·         Is implementing (badly mind you) X used for something? Answer: This library needs classes implementing X (Documentation of the library is surely wrong, source code as well I suppose…)
·         Why catching an Exception and then ignoring it? Answer: Historical reasons (History does repeat itself though….)
·         Have you tested your changes? Answer: Yes it works (Jenkins is probably a big liar, there is a conspiracy… I can’t imagine you modifying your classpath locally and then commiting code that does not work with a different one…)
·         DO NOT USE SYSTEM.OUT in Production (actually don’t use it anywhere)! Answer: It’s a console application… (What can I say to that….)
·         Overriding hashcode and not equals (or vice versa)??? No need … (Again I’m speechless… Twice in a row!)
·         Why is there X here? Answer: I think it works like that (And here I thought computer sciences were rational…)


I could go on forever I think, but you got the point, if you want to have an argument, I am all for it, as long as it is rational, we are not making alcohol in a barrel hidden in the countryside, we are programming, which implies rationality is the key factor.

Of course by now you clearly see I am focused on Java development, although I do not mind other languages (too many times people are acting like a sect and dancing around a fire praising their own language, I am fortunately a complete asocial…)
