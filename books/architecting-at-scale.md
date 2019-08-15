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
p 30.
