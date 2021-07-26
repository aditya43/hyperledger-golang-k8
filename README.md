# Hyperledger Using Golang
Hyperledger Fabric, Kubernetes, GoLang, VueJS, CouchDB

## Author
Aditya Hajare ([Linkedin](https://in.linkedin.com/in/aditya-hajare)).

## Current Status
WIP (Work In Progress)!

## License
Open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

-----------

## What is Hyperledger Fabric:
- Hyperledger is a set of tools that allows us to run a distributed database that scales utilizing blockchain technologies.
- It also allows us to have much greater flexibility with our data sharing across multi tenant systems.
- Hyperledger is essentially a shared database.
- 2 basic components of any working network are going to be the `orders` and `peers`.
- `peers` receive verify transactions in the network and then hand them off to the `orders` which process them and decide which order they are written to the block chain. `orders` then pass them back to the `peers` who write them to their `ledger`.
- Each `peer` has it's own `ledger`.

-----------

## What is ordering:
- Many distributed blockchains, such as Ethereum and Bitcoin, are not permissioned, which means that any node can participate in the consensus process, wherein transactions are ordered and bundled into blocks.
- Because of this fact, these systems rely on probabilistic consensus algorithms which eventually guarantee ledger consistency to a high degree of probability, but which are still vulnerable to divergent ledgers (also known as a ledger “fork”), where different participants in the network have a different view of the accepted order of transactions.
- Hyperledger Fabric works differently. It features a node called an orderer (it’s also known as an “ordering node”) that does this transaction ordering, which along with other orderer nodes forms an ordering service.
- Because Fabric’s design relies on deterministic consensus algorithms, any block validated by the peer is guaranteed to be final and correct.
- Ledgers cannot fork the way they do in many other distributed and permissionless blockchain networks.
- In addition to promoting finality, separating the endorsement of chaincode execution (which happens at the peers) from ordering gives Fabric advantages in performance and scalability, eliminating bottlenecks which can occur when execution and ordering are performed by the same nodes.