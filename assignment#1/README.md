# Thoughts on AOP

Google TechTalks about AOP: https://www.youtube.com/watch?v=40Q16Ix-src&t=598s&ab_channel=GoogleTalksArchive

### My thoughts:

Aspect oriented programming (AOP) is, in a shorter and simpler way to say, a programming style that aims to eliminate cross cutting throughout the code. It does that while providing a straightforward and modular way of writing tasks such as logging(the most used these days), tracing and so on. This makes refactoring, readability and debugging an easier process.

But there is a catch, I was wondering why I’m listening for the first time a term that was first introduced more than 14 years ago, and after some research i found this, quoting:

“The problem that AOP tries to solve - how to develop different concerns independently and then compose them later - is a hard problem. I don’t think anyone has really solved it. It’s basically higher-dimensional Tetris to fit multiple concerns together, even by hand. Getting a machine to do it, automatically but intelligibly, is especially tricky.
In particular, in any kind of procedural / OO language, whatever preprocessing you use to thread the aspects together disrupts your ability to read the flow of control by looking at the code. Even things like macros, Python decorators and other kinds of advice have this problem.
So, for procedural programmers, AOP adds a kind of difficulty which may be more trouble than it's worth.”

I think this is way os not broadly spoken, it’s hard to do using procedural languages, which are more common. In the video Gregor Kiczales says that may not appear, but aop actually is better for modularity, but the problem with aop is with overdue, it gets messy and complicated.

This pattern like “event driven” or “case handling” programming might handle composition of concerns better than AOP. So why not turn your program into a number of asynchronous “when” statements that react to different events, both internal and external. kotlin supports this kind of design and it’s awesome.
Thinking of programs like this, as declarative rules, without explicit flow of control, then adding new concerns is just adding new bundles of rules. 
