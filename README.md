# Distributed Key-VaLue Database using Raft algorithm - RaftDB


<img src="https://ariskk.com/static/e332d369be6f66aae7e3da60c0e07eb1/18e3b/raft-arch-2.jpg"/>


## About this project
In this project a Key-Value distributed database like Redis, Voldermort and DynamoDB was implemented in Go. There is no doubt that fault-tolerance and availability are the major concerns when a modern system is designed. The ability to keep your business 24/7 available when it is scaled up is the most crucial part of nowadays applications. In this project we have developed a reliable and fault-tolerant key-value database using Raft consensus algorithm. The project was implemented according to [Raft extended paper](https://web.stanford.edu/~ouster/cgi-bin/papers/raft-atc14). Since we didn't have enough servers to implement such distributed algorithm, we borowed the network simulator, created by MIT, to simulate unstable network and servers. We used the [MIT's lab code](https://pdos.csail.mit.edu/6.824/) as code base and we implemented on top that the Raft algorithm.

## What RaftDB can do ?
- Append/Put Key-Value pairs
- Get Value by Key
- Guarantees scalability, availaiblity, fault-tolerance when the minority of replica servers are down.

## About Raft algorithm 
  Raft is a consensus algorithm designed as an alternative to the Paxos family of algorithms. It was meant to be more understandable than Paxos by means of separation of logic, but it is also formally proven safe and offers some additional features. Raft offers a generic way to distribute a state machine across a cluster of computing systems, ensuring that each node in the cluster agrees upon the same series of state transitions. It has a number of open-source reference implementations, with full-specification implementations in Go, C++, Java, and Scala. It is named after Reliable, Replicated, Redundant, And Fault-Tolerant. Raft is not a Byzantine fault tolerant algorithm: the nodes trust the elected leader.


## Run RaftDB via unittests
```bat
cd kvraft
go test
```
## Future Work
Implementation of the sharded version of the RaftDB.
