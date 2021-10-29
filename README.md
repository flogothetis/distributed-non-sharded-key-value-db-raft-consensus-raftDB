# Distributed Key-VaLue Database using Raft algorithm - RaftDB


<img src="https://ariskk.com/static/e332d369be6f66aae7e3da60c0e07eb1/18e3b/raft-arch-2.jpg"/>


## About this project
In this proejct a Key-Value distributed database like Redis, Voldermort and DynamoDB was implemented in Go. There is no doubt that scalability and availability is the major concern when a modern system is designed. The ability to scale up and down according to business needs and demands is the most crucial part of nowadays applications. In this project we have developed a realiable and scalable key-value database using Raft consensus algorithm. The project was implemented according to [Raft extended paper](https://web.stanford.edu/~ouster/cgi-bin/papers/raft-atc14). Since it is not common to have enough servers to implement such distributed algorithms, we borowed the network simulator, created by MIT, to simulate unstable network and servers. We used the [MIT's lab code](https://pdos.csail.mit.edu/6.824/) as base and we coded up the Raft's actual algorithm. 


## What RaftDB can do ?
- Append/Put Key-Value pairs
- Get Values by Key
- Guarantees scalability, availaiblity, fault-tolerance when the minority of replica servers are down.

## About Raft algorithm 
  Raft is a consensus algorithm designed as an alternative to the Paxos family of algorithms. It was meant to be more understandable than Paxos by means of separation of logic, but it is also formally proven safe and offers some additional features. Raft offers a generic way to distribute a state machine across a cluster of computing systems, ensuring that each node in the cluster agrees upon the same series of state transitions. It has a number of open-source reference implementations, with full-specification implementations in Go, C++, Java, and Scala. It is named after Reliable, Replicated, Redundant, And Fault-Tolerant. Raft is not a Byzantine fault tolerant algorithm: the nodes trust the elected leader.


## Raft DB overview
![Raft overview](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.semanticscholar.org%2Fpaper%2FARC%253A-Analysis-of-Raft-Consensus-Howard%2F3665b13932eea50cf9ef5d32b85efc8a06a92b79&psig=AOvVaw0RskMkPB_MILIJOkWxUg1a&ust=1635538605807000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCIj8iqb27fMCFQAAAAAdAAAAABAd)

## Run RaftDB via unittests
```bat
cd kvraft
go test
```
