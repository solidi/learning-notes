# Philosophy Of Software Design
# Author: John Ousterhout

## Quotes
- The most fundamental problem in computer science is problem decomposition: how to take a complex problem and divide it up into pieces that can be solved independently. Problem decomposition is the central design task that programmers face everyday and yet other than the work described herem I have not been able to identify a single class in any university where the problem decomposition is a central topic.
- Many people assume that software design skills is an innate talent that cannot be taught. However there is scientific evidence that outstanding performance in many fields is related more to high-quality practice that innate ability.
- Students work best by writing code, making mistakes and then seeing how their mistakes and the subsequent fixes relate to the principles.
- This book is an opinion piece so some readers will disagree with some of the suggestions. If you disagree, try to understand why.
- All programming requires is a creative mind and the ability to organize your thoughts. If you can visualize a system, you can probably implement it in a computer program.
- The first approach is to eliminate complexity by making code simpler and more obvious. For example complexity can be reduced by eliminating special cases or using identifiers in a consistent fashion.
- If software developers should always be thinking about design issues, and reducing complexity is the most important element of software design, then software developers should also be thinking about complexity. This book is about how to use complexity to guide the design of software throughout its lifetime.
- Your job as a developer is not just to create code that you can work with easily, but to create code that others can also work with easily.
- Sometimes an approach that requires more lines of code is actually simpler, because it reduces cognitive load.
- One of the most important goals of good design is for a system to be obvious. This is the opposite of high cognitive load and known unknowns. In an obvious system, a developer can quickly understand how the existing code works and what is required to make a change.
- Complexity comes from an accumulation of dependencies and obscurities. As complexity increases, it leads to change amplification, a high cognitive load and unknown unknowns. As a result, it takes more code modifications to implement each new feature.
- This chapter discusses why the strategic approach produces better designs and is actually cheaper than the tactical approach over the long run.
- Almost every software development organization has at least one developer who takes tactical programming to the extreme: a tactical tornado. The tactical tornado is a prolific programmer who pumps out code faster than others but works in a totally tactical fashion. When it comes to implementing a quick feature nobody gets it done than the tactical tornado. However, tactical tornadoes leave behind a wake of destruction.
- Your primary goal is to produce a great design, which also happens to work. This is strategic programming.
- Try to imagine a few ways in which the system might need to be changed in the future and make sure that will be easy with your design. Writing good documentation is a good example of a proactive investment.
- Your initial projects will thus take 10-20% longer than they would in a purely tactical approach. The extra time will result in a better software design and you will start experiencing the benefits in a few months. It won't be long before you're developing at least 10-20% faster than you would if you had programmed tactically.
- Currently: P 15.
