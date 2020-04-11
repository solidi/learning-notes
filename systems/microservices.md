# Microservices

## Philosophy

Scalability and distribution. Building a system on an average load day.

## Concepts

1. Distribution tax.
    1. Distributability
    1. The enemny is latency
    1. Well-defined service boundaries
    1. Scability
1. Tradeoffs
    1. Scability and deployments
    1. Large number of moving parts
    1. Manage the strengths, control the weaknesses
1. Strong contracts and well-defined boundaries allow for self-discovery
1. Versioning strategy, passivity stance?
1. Use edge services to abstract inbound and outbound and isolate changes

## Shaping the Service

1. Investigate working system
1. Determine the domains (bounded context)
    1. Reduce the connection calls
1. Break up service accordingly
1. No distributed transactions!

## Others

1. Durable - guaranteed to be in the datastore until modified
1. API Layer - aggregated proxy of all of your service offerings
1. Recommend a unified logging strategy with traceID
1. Managing the risks to maximize the reward

## Trivia

1. Microservices are not always designed to be run in a cloud platform even if they aren't deployed to one.
1. The stages of evolution in modern software service architectures, from oldest to most modern are N-Tier, SOA, Microservices.
1. Tight coupling was a common problem in software development that was often more apparent in monoliths?
1. A pain point of monoliths that impedes speed to market is Long Deployment Cycles.
1. 500 is the error response code for SOAP webservice calls.
1. One of the issues with BPEL is that the workings were often abstracted from the webservices code.
1. What is true of Protocol Aware Heterogeneous Interoperability for microservices? All communications within the service boundaries are solved via ReST.
1. Microservices tend to be more complex than monoliths because of the moving parts.
1. The cost associated with remote calls for most operations in microservices architectures is often called the Distribution Tax.
1. There are no hard and fast boundaries on the size of the microservice.
1. The communication dance in microservices is primarily an effect of the ability of a service to call any other service.
1. The ability to globally distribute a microservice comes from the fact that every call is a remote call.
1. The ability to scale in a microservices architecture comes from the fact that artifacts are single purpose and separated.
1. The fact that all calls are remote and cascading is the risk of latency in a microservices architecture.
