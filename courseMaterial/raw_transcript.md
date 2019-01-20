# Chapter 1 - Discovering BlockChain Technologies

## Section 1 - Distributed Ledger Technology (DLT)

### Video 1 - Blockchain Technology (Robert Schwentker)

Robert, what is blockchain technology?
A blockchain is a peer-to-peer distributed ledger, forged by consensus, combined with a system for smart contracts and other assistive technologies.
Together, these can be used to build a new generation of transactional applications that establish trust, accountability, and transparency at their core,
while streamlining business processes and legal constraints.
With all distributed ledgers, there's an initial record or, in this case, a block, or a genesis block.
Each block will include one or more transactions.
Connecting to a blockchain involves people connecting to this distributed ledger via, typically, an application.
So, an example of this would be a wallet.
One person may transfer ownership of a digital asset, like a cryptocurrency, from one person to another,
and that asset will move from one person's wallet to another person's wallet,
and then, that transaction will be shown on a blockchain.
So, this distributed ledger transaction, such as a payment, will move from peer-to-peer throughout the network,
and there's no intermediaries, like a bank, or a payment company, to process this transaction.
Can you give an example of a blockchain which has been in production since a few years?
Sure, Navroop. Blockchain is actually best known because of Bitcoin.
And Bitcoin's blockchain has been in existence since 2009.
It's a cryptocurrency, but, interestingly, people confuse the two terms.
Blockchain is actually not Bitcoin, or vice versa.
Blockchain is a distributed ledger. The blockchain then tracks various assets, other than cryptocurrencies, such as Bitcoin.
Those transactions are grouped into blocks, and there can be any number of transactions per block.
Turns out, nodes or machines on a blockchain network group up these transactions and they send them throughout the network.
So, you've mentioned how blockchains operate on peer-to-peer nodes.
How do they all sync up?
So, the process of blockchains syncing up have to do with a concept of consensus - an agreement among the network peers.
So, eventually, each machine has an exact copy of the blockchain throughout the network.

### Video 2 - What Is a Blockchain? (Dave Huseby)

So, what is blockchain?
As the Security Maven at Hyperledger, I have somewhat of a different perspective on what a blockchain is.
I'm a developer, primarily, and I look at the world in an adversarial way.
It's usually my software versus the world kind of thing.
Blockchains, to me, definitely open up the world of possibilities for solving problems that have plagued us for many years.
It breaks down to being able to create distributed consensus between mutually  distrustful parties, in many ways.
It also allows us to create an instantaneous single source of truth.
In the past, we've always had problems with trying to figure out what really happened over the course of a day.
Banks reconcile their books, inventory systems clear sales and deliveries...
With blockchains, we're recording things in real time, and it provides us with sort of an up-to-date accounting of the state of the world.
So, a lot of these old systems are going away, a lot of the work load management systems are going away. We're not doing batch processing at night anymore.
Instead, we're doing validation in real time, and we always know the state of the world.
This opens up a whole new host of applications that can be based around...
If we knew exactly where every bolt was, could we make sure that there are always  bolts at the place where they're going to be installed two minutes before they are needed... things like that...
So, like lean manufacturing is one case...
But, it also applies to every other process in the world where we have to track materials and effort, and money, things like that.
Let me think...
So, the blockchain, for me, actually is just sort of rethinking of our existing business processes around how we can be more effective when we know the state of the world as it is right now,
and we know it in two minutes, and we know it in two hours, rather than having to wait until the end of the day for everything to be reconciled.
This is actually a transition from human scale to computer scale.
This was... all of these processes were done on a daily basis, and things like that,
and with blockchain, we're now... we're doing it instantaneous, because computers have made it that way.
From a security perspective, blockchains are not a silver bullet.
They're not going to replace the existing business logic.
They're more of a log-based system, so recording what has happened, as it is happening,
rather than being the source of what to do with money from a customer, and things like that.
It's not business process type of software.
Because it is a log, and because it is the source of truth, and because a lot of other business logic will be based upon it,
the security concerns on it, related to blockchain, are roughly the same as existing business practices, or business logic.
You have to think of all the members of a distributed ledger as participating in a closed network,
because that's what they are, at least in permissioned networks,
we're not operating on the public Internet, we're not operating in a trustless environment.
It's the exact opposite. We... all the participants in the distributed ledger are known, they're permissioned,
that's where that term comes from, and they all participate as if they are in a private network.
So, when deploying blockchain software, it's typically done behind a firewall,
and, anytime you have multiple organizations participating in the distributed ledger,
we will use tunneling technology and other VPN firewall tricks to make a virtual LAN exist,
so that all of their organizations can talk over it.
Different Hyperledger projects have different trade-offs.
Fabric, for instance, has a more centralized ordering service,
and so, it makes more sense to organize one of those networks into a hub-and-spoke model,
where each peer connects to the ordering service, which is run either on one of the nodes, or on a neutral third party,
and all of the gossip messages that do the consensus mechanism go through a central hub.
Now, that sounds counterintuitive because just distributed ledgers are supposed to be distributed...
they still are, they're distributed in the sense that the blockchain itself is replicated amongst all of the nodes,
and so, your data is much more resilient to disruption...  resilient against disruption.
But, the coordination can still be done in a fairly centralized manner.
With Sawtooth, it is not so much the case, right?
The organization of the network for Sawtooth is probably more of like a star model,
where you pick some subset of nodes, and your node connects to those and, as long as all nodes are fairly well connected,
they can all eventually talk to each other, either one hop, or two hops, or three hops away, depending on the size of your network.
With Iroha, they... their topology is a lot different than the others,
because they designed their distributed ledger to function well in a mobile environment,
where a lot of the clients are intermittently connected.
So, they're mobile phones that can be connected and disconnected at random.
So, their structure is more of a layered network, where the end clients' mobile  phones submit transactions to servers,
which then, amongst the servers, do the distributed ledger.
And there's no right answer, right?
The business process dictates which one you choose, but the security is pretty much the same in all of these.
We use cryptography and digital signatures to validate all the messages.
So, tampering with messages is essentially impossible.
The immutability of the distributed ledger is guaranteed by the cryptography,
but the nature of the trusted network, of the permissioned network, means that we have to treat it like any other back-office service.
You want to deploy it behind a firewall, you want to use tunneling to connect between nodes across the Internet,
and you want to maintain it, just like any other service that deals with Internet traffic...
you have firewalls, and load balancers, and things like that.
That's all I've got to say about security. And thanks for taking our course.

### Video 3 - Peer-to-Peer Networks (Robert Schwentker)

What is a Peer-to-Peer network, and how do peers come to agreement about what is on the blockchain?
A blockchain network is a group of computers that informally are organized in a Peer-to-Peer architecture.
Consensus is a process whereby the peers synchronize the data on the blockchain.
There are a number of consensus mechanisms or algorithms.
One is Proof of Work. Another is Proof of Stake.
There's also Proof of Elapsed Time, as well as Simplified Byzantine Fault Tolerance.
Bitcoin uses Proof of Work, while Ethereum uses Proof of Work currently, but is moving towards Proof of Stake.
The Hyperledger Sawtooth uses Proof of Elapsed Time.

### Video 4 - 
