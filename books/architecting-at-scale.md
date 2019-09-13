# Architecting at Scale
## Author: Lee Atchison
 
## General Quotes
- Concept of bronze, silver, gold teams.
- Bronze level - risk matrix and defined SLA's.
- Silver level - monitoring for items in risk matrix and running game days.
- Gold level - risk are mitigated, CMM level 5, were systems were self-healing and the focus was on continuous improvement.
- Build with failure in mind.
- Using design constructs and patterns, such as simple error catching deep within your application, retry logic, and circuit breakers in a way that allows you to catch errors when they have affected the smallest available subset of functionality.
- Think about whether specific pieces of dynamic content can actually be generated statically.
- Availability and risk management go hand in hand. Building a highly available system is significantly about managing risk.
- Often, for basic web applications, 3 nines is considered acceptable availability. This amounts to 43 minutes of downtime every month.

| Nines   | Percentage | Monthly Outage |
|---------|------------|----------------|
| 2 Nines | 99%        | 432 minutes    |
| 3 Nines | 99.9%      | 43 minutes     |
| 4 Nines | 99.99%     | 4 minutes      |
| 5 Nines | 99.999%    | 26 seconds     |
| 6 Nines | 99.9999%   | 2.6 seconds    |

- By tracking when your application is available and when it isn't gives you an *availability percentage* that can show how you are performing over a specific period of time.
- A tool that you can use to help manage your application availability is *service tiers*. These are simply labels associated with services that indicate how critical service is to the operation of your business.
- Finally create and maintain a *risk matrix*. With this tool, you can gain visibility into the technical debt and associated risk present in your application.
- If you continuously make one off changes to the resources such as servers, the servers will begin to *drift* and act differently from one another.
- Consistency, repeatability, and unfaltering attention to detail is critical to make a configuration management process work. And a standard and repeatable configuration management process such as we describe here is critical to keeping your scaled system highly available.
- (Losing trust from the customer) You must weigh loss against a competing aspect: what is the cost of removing the risk to prevent this from happening.
- The risk matrix can quickly become stale if you don't review it regularly. You should review your risk matrix as a team at least quarterly, but perhaps monthly for very active and highly critical systems.
- The significance of a risk is the combination of the severity of the risk happening with the likelihood of it happening. To successfully manage risk, you must consider both of these values and how they relate to each other. To reduce risk, you need to lose at least one of these two values for any given risk.
- I recommend one risk matrix per team. Because decision making on what features or issues to work on and their priority is often handled at the team level, it makes sense for the risk matrix to be managed and prioritized at the team level.
- Have a meeting with your development team. The team members will have an amazingly large number of worries on their minds about their services. Listen to their concerns, and add risk items for each one that comes up.
- Go through your feature backlog. Are there capabilities of your system that are missing that are critical to the health of your system? Look especially for monitoring and maintenance related backlog items.
- A *triggered plan* is a plan for what you are going to do if the risk actually occurs.
- The mitigation column in the risk matrix is used to show what mitigations can be, or are being used to reduce the severity, the likelihood, or both values for a given risk. It is all about taking a High/High risk and changing it to a High/Medium risk or a Medium/High risk. It is not about fixing, only mitigating the severity or likelihood of the risk.
- Risk management is understanding the play between removing risk and mitigating risk. It's knowing whether it is prudent, timely, and cost effective to remove a risk or simply reduce the impact of the risk.
- One model for testing these plans is to run *Game Days*. A game day is when you test invoking a specific failure more into your system and watch to see how your operators and engineers respond to it, including how they implement any recovery/disaster plans. After the game day, a postmortem review will uncover changes and issues with your plans that will need to be made. These changes will keep your plans fresh and updated, and ready to be used when a real problem occurs.
- Netflix takes the random failures problem to a new level. The company has a system called Chaos Monkey built into its application. The system randomly and regularly introduced random faults into the application, into the production environment, with live running customers.
- p 56.
