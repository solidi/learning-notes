# Trade-offs List

Thanks to [nderflow](https://www.reddit.com/user/nderflow/) in [this Reddit thread](https://www.reddit.com/r/SoftwareEngineering/comments/igbwsa/software_architecture_tradeoffs/).

## Here's a selection of trade-offs:

1. The all-time classic: (quality, cost, time) [this is not specific to software, but it's very important]
1. Buy vs. build (most obviously with system components, but also with staffing and with orgs).
1. Integrate best-of-breed versus already-integrated products
1. Dividing systems into services (whether to do it, and how)
1. How much technical debt to take on, when to do it and at what rate to pay it off.
1. Latency versus both of (cost, complexity)
1. Throughput versus both of (cost, complexity)
1. Design for higher probabilities of partial failure versus lower probabilities of total failure
1. Cost of implementation versus cost of support (e.g. how much to spend on observability, manageability, serviceability)
1. When to hold hard on scope, when to flex on scope; the balance between these changes across the lifetime of a project.
1. Which features should be in the MVP and which in later releases? Too much in the MVP and the project may not survive long enough to ship. Too little and nobody wants a 2.0 release because 1.0 was so useless.
1. When to slip the schedule, how to do it. Slip too early? May slip twice. Slip too late? May seriously trash other teams' plans, attract extra-org downsides (e.g. bad reputation).
1. When to refuse to slip. How to not look like a dumb-ass when you chose this option.
1. When to spend your political capital, when so save it (in other words: how to pick your engineering battles)
1. The difference between motivating the team to do more and being an asshole
1. Empowerment versus predictability (e.g. how much should the team self-direct, how much direction should come from within the team versus be imposed from without)
1. Skills development versus predictability For example, when there is a hard problem to solve, who do you give it to? Give it to a junior team member, it may not be done quickly or perfectly, but they will build their skills. Give it to a senior team member, it will likely be done quickly/well, but the capabilities of your team are unchanged.
1. How much team mobility to allow/encourage/force? Too little and no new ideas come into your team. Too much and nobody knows how to do anything. If your team member is long-serving in the team, is this because they're very happy here, or is it because they have imposter syndrome and are worried they would not succeed in another team?
1. Another old saw: rewrite versus iterate
1. Basically the same saw with different spelling: retrofit automated tests to an old design, or make a new design for testability
1. How much effort to assign to (documentation, roadmapping, design, coding, testing, production support)
1. When to redefine your success criteria (too infrequently and the existing criteria are not relevant, too frequently and you can't compare this $time_period to last $time_period).
1. Which features of this thing should be internal versus externally visible/usable (this trade-off occurs at every scale, from the individual module up to the application and service level)?


## Engineering and Product Conversation

Thanks to [dan-jat](https://www.reddit.com/user/dan-jat/) for below:

### Product

> Product: We would like to have our solution run with 99.99999% uptime, and scale up and down based on load so we can land customers A and B who have inquired about this functionality.

> Engineering: Ok, we can do that but we need to get 4 additional datacenters, a new monitoring solution of some kind, likely worth about triple the one we are running currently, and re-architect our solution to work in an automatically scaling environment. The most popular one currently is Kubernetes, but its also quite far away from the monolith that we are currently running. Would those customers bring us in enough additional revenue to justify an early estimate cost of $y?

> Product: Well, that's way to much...what could we do for $x?

> Engineering: Initial estimate would be that we would be able to get to 99.999% uptime for that, and allow manual scaling up but not down, by the addition of new hardware into the site(s). Would that be enough to get us those customers?

> Product: Let me talk to them and we'll meet up again afterwards.

### Engineering

> Engineering: We need to decide between 2 different options that from a technical perspective have equal pros and cons to each other, and we're hoping that you can help us swing the vote in favor of one or the other.

> Product: Ok, but I'm not very technical so I'm not sure how I can help.

> Engineering: You know the customers though, and what they want. Would you rather have faster response times for searches and lower bandwidth usage, or a more responsive data input screen with additional customizable branding?

> Product: Customers spend far more time on the input screen that searching, because we've reports that show everything they want most of the time, so the data screen being more responsive would be nice, and anything that can drive more customization we can have professional services bill for always gets my vote.

> Engineering: Ok, so continuing along a semi-similar track would they rather be able to have more historical data available for those reports, or have the ability to easily create new formats for those reports

> Product: I thought we couldn't store any more historical data because of that other feature we did, but if that's back on the table we definitely still want it.

> Engineering: Thanks, you've been a big help.
