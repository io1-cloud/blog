# Basics of container based applications

## The primary unit
In a modern infrastructure containers are the primary unit. It's what your developers ship, it's what your ops monitors and your providers hosts. Without containers deployment could mean keeping dozens or sometimes hundreds of files and scripts synchronized between your development and production.

Many tasks become homogenic across containers. A good example is logging. In a container world this can be done by simply capturing the output of the container. The container itself remains oblivious to any form of log capturing while a log aggregation tool can get all output from all containers.

This is a situation where something 'simple' as wrapping your app into a container changes everything!

## Persistence
Containers have often been deemed unfit for databases. This is not true of course and there are different strategies to dealing with databases in a container environment (e.g. deploy & migrate or shared storage). We prefer the pragmatic option of fully managed databases which have backups, failover and upgrades all sorted out.

## Works on my machine
We recommend shipping immutable containers. This means that the application, its dependencies (on other containers) are all fixed and what the developer sees is also what will be in production. A caviat here is the settings that are unique for production. The 'canary deployment' and extensive health checks will be the final 

## Application design
If you want to move fast you need to be able to ship working software into production quickly. But if every release of any application needs a full blown integration test of all your applications, you're not reaping the benefits of containers. Loose coupling, 'canary deployment' and resiliance are the main ingredients to keep your software flowing to production.