# Designing Data Intensive Applications
[Book link](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321)
Sharing some thoughts of each chapter with side quests, This is not an overview or your normal notes. [click here if you want an overview](https://github.com/ahmedhammad97/Designing-Data-Intensive-Applications-Notes)


## Chapter 1: Reliable, Scalable, and Maintainable applications
| Term | Meaning |
| ------ | ------ |
| Reliability | the system continue to work when faced with hardware faults or human errors |
| Scalability | you can handle growth (traffic, data volume or complexity) |
| Maintainability | your applications can easily be adapted to new use cases |
- Applications are getting more Data-bound instead of Computing-bound and the intoroduction of internet didn't help
- Fault vs Failure 
    - A fault is usually defined as one component of the system deviating from its spec
    - Failure is when the system as a whole stops
    - You can not reduce the probability of a fault to a zero; the idea is to design fault-tolerence mechanisms that prevents faults from causing failures.
- [p95, p99, p999](https://stackoverflow.com/questions/12808934/what-is-p99-latency) 
- Good operations can often work around the limitations of bad software, but good software cannot run reliably with bad operations.
    - example by me (Good operations, bad software): If a program is leaking memory at a rate of 100MiB every day, the node memory is 1 GiB and the init memory of the application is 100MiB, then the operations team can just restart (Automated ofc) this application every 9 days and it will be fine.
    - example by me (Bad operations, good software): Your network routers gets restarted every X minutes, Proxies drop your connections unexpectedly or your application machine gets restarted every X hours
