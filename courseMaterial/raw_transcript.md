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

### Video 4 - Smart Contracts (Robert Schwentker)

What is a smart contract?
Back in 1996, a man named Nick Szabo coined the term 'smart contract'.
You can think of them as computer protocols used to facilitate, verify, or enforce the negotiation of a legal contract.
A smart contract is a phrase to describe computer code.
Today, Ethereum smart contracts are designed to run on all nodes of the Ethereum network.
Those smart contracts facilitate the exchange of value, including money, content, property, or shares between a fixed number of parties.

### Section 2 - Bitcoin and Ethereum Blockchains

### Video 5 - Bitcoin and Ethereum (Robert Schwentker)

And so, why were Bitcoin and Ethereum created? What problems do they solve?
So, Bitcoin was first launched in January of 2009, as a response to the global financial crisis at the time.
Part of the motivation for the system was to be able to transfer value over the internet, without an intermediary.
So, one of the biggest inventions and problems that it solved was that of the 'double spend' problem.
So, Bitcoin, in fact, is programmable money.
Ethereum, on the other hand, was created as a response to Bitcoin.
While Bitcoin is focused upon transferring monetary value between parties, it has a very limited programming language.
Ethereum, on the other hand, uses a more expansive set of programming languages and tools to allow for many other types of programs and applications.
The core invention of Ethereum is it's EVM, or Ethereum Virtual Machine.
The EVM runs on the Ethereum network, and it runs a Turing-complete software.
So, Vitalik Buterin is the person who wrote the white paper for Ethereum.
Some of its key features include the immutability of data, that unauthorized users cannot make changes to that data,
the Ethereum development platform is designed to make corruption and tamper proof applications,
the secure apps are sent decentralized and secured with cryptography,
and they're protected against hacking attacks and fraudulent activities,
and lastly, it's designed with zero downtime.
That is because the applications on the network are decentralized, and on many, many machines,
if some of those machines go down, the Ethereum network maintains a stable state of the Ethereum network.

### Video 6 - Ethereum (Robert Schwentker)

Can you give another example of a production blockchain system, such as Ethereum, and how is it different from Bitcoin?
Sure. Ehereum also has a public blockchain. It also groups and orders transactions into blocks.
However, Ethereum may be defined as an open source platform that enables  developers to build and deploy both smart contracts and decentralized applications, also known as Dapps.
In addition to the Ethereum public blockchain, there are numerous versions of Ethereum which are designed to be private and are permissioned.

## Section 3 - Exploring Permissionless Blockchains

### Video 7 - Exploring Bitcoin and Ethereum Blockchains

Let's take a look at a couple of public blockchains: those of Bitcoin and Ethereum,
and let's examine the genesis block, or the first block, of each one of them.
Then, we'll take a look at a couple of large transactions, including the most famous transaction in cryptocurrency history: the purchase of a pizza for 10,000 bitcoins.
So, first, we'll go to this blockchain explorer, and see that there is a Height column, which indicates the number of blocks in this particular blockchain; it's nearing a half a million.
These blocks are created approximately every 10 minutes,
and there's a Transactions column that shows how many transactions are included in each block,
as well as the Total Sent, or the amount of Bitcoin that was transferred in each of those blocks.
Finally, you can notice that there's... they relate by column, which is essentially the miner or mining pool that created that block.
So, from here, let's take a look at another blockchain explorer, and you can see here the genesis block of the Bitcoin blockchain.
Notice that the timestamp is January 3rd 2009.
So, that's the genesis block of the Bitcoin blockchain.
Now, moving on to the Ethereum  blockchain, we'll look at another blockchain explorer.
And this one shows you that there's approximately 5 million blocks in the Ethereum blockchain.
Notice that each block is created much more quickly than in the Bitcoin blockchain.
From here, we'll examine the genesis block of the Ethereum blockchain,
and notice that it was mined about two years ago,
and the mining reward for this was approximately five ether.
So, from here, we'll take a look at the very interesting transaction: that of the pizza transaction.
On Bitcoin Forum, there was somebody on May 18th of 2010 who was requesting that they would pay 10,000 bitcoins for a pizza.
They provided their address and someone in fact sent them a pizza. In fact, it was from Europe.
And you can see here that that was this transaction here: of 10,000 bitcoins.
And lastly, a very large and interesting transaction of 658 bitcoins, done recently.
Notice that the value of that is close to 3 million dollars.
So, you can examine these transactions on both the Bitcoin and Ethereum blockchains, and many other blockchains.
In Chapter 2 of this course, we'll touch upon the Hyperledger Explorer, which can be configured to examine blockchains you might develop with other of the Hyperledger frameworks.

### Video 8 - Certifying" a Document onto Blockchains Using Stamp.io
 Bookmark this page

In this screencast, we will show how we can take a document and certify it to both the Bitcoin and Ethereum blockchains.
I'm going to use the tool Stamp.io, and I will take a file and I will, in a sense, have it certified on the blockchain.
Once this is done, the output on Stamp.io will show us a certificate.
They call it the Stampery certificate, which indicates the name of the file, when it was added to Stampery,
and the person who, in a sense, signed it.
So, a particular hash of this document was stored in transactions which were placed in various blocks, on both the Ethereum and the Bitcoin blockchain.
So, if we open up this particular transaction, we'll see that there was inside of this transaction a hash of the document,
and this was done a number of days ago and added to this particular block on the Ethereum blockchain.
If we examine the Bitcoin block, a transaction into which this transaction was put,
we will also say that this here is the particular transaction that was then added to this particular block on the Bitcoin blockchain.
So, stamp.io is a tool that can be used to put and verify document hashes onto both the Ethereum and Bitcoin blockchains.

## Section 5 - Hyperledger

### Video 9 - Hyperledger (Robert Schwentker)

So, tell us about Hyperledger.
So, Hyperledger is an umbrella of open source projects, some of which are blockchain distributed ledger frameworks such as Fabric,Sawtooth, and Iroha.
Hyperledger may be thought of as an open system for marketplaces, including decentralized data sharing networks and digital communities.
In fact, there are more than a hundred and thirty organizations which comprise the Hyperledger member community [as of October 2017].

### Video 10 - 