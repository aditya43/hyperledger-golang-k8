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
- 2 basic components of any working network are going to be the `orders` and `peers`.
- `peers` receive verify transactions in the network and then hand them off to the `orders` which process them and decide which order they are written to the block chain. `orders` then pass them back to the `peers` who write them to their `ledger`.
- Each `peer` has it's own `ledger`.