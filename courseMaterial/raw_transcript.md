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

### Video 10 - Hyperledger vs. Other Permissioned Ledgers (Brian Behlendorf)

What makes Hyperledger so unique, compared to other permissioned ledgers?
So, Hyperledger is a really unique community in the open source landscape of different blockchain technologies.
We kind of model ourselves a little bit after Apache, and some of the other organizations out there that really are communities of communities, right?
Within Hyperledger, we have eight different technology code projects, essentially (as of October 2017).
Projects like Fabric and Sawtooth, and a lot of the others that all of you will be finding out about,
but, what these projects have in common is a set of development principles around working in the public,
around, you know... even from the earliest ideas, you know, developers should be sharing that with other developers, right,
not just something they build privately, then throw over the wall, and release this open code,
but that starts out from day one as a public process, right, and multi-stakeholder as well.
So, while projects do often start out as the work of one company or one small set of developers,
we really come to trust technologies when we see that there's lots of people both using it and contributing to it.
And so, that way, we know this is actually a project that will likely outlast any one company's commitment to it, right?
That's a good basis for deciding what open source technologies to build on.
So, at Hyperledger, we're trying to make sure that each of these projects fulfills that goal of being multi-stakeholder,
of being active software development projects that get as quickly as possible to a production release,
something that organizations can actually use in real production environments, and yet, still has the flexibility to explore a new concept,
to explore a new consensus mechanism, a new way of writing smart contracts, right?
So, that balancing act is really what we're trying to strive for inside of Hyperledger.

## Section 6 - Other Open Source Permissioned Distributed Ledgers

### Video 11 - Other Distributed Ledger Technologies (Robert Schwentker)

What are some examples of other blockchain and distributed ledger technology systems, and what are their benefits?
Chain Core, created by chain.com, has initially been designed for financial service institutions,
and for things like securities, bonds, and currencies.
Their company has strong ties with Visa, Citigroup, and Nasdaq.
The Corda distributed ledger platform is designed to record, manage, and automate legal agreements between businesses.
It was created by the R3 company, which is a consortium of over a hundred global financial institutions.
Quorum is a permissioned implementation of Ethereum, which supports data privacy.
Quorum achieves this data privacy through allowing data visibility on need-to-know basis by a voting-based consensus algorithm.
Interestingly, Quorum was created and open sourced by JPMorgan.

## Chapter Conclusions 

For a new technology to realize its full potential, a lot of pieces need to exist before network effects can be realized. Moreover, in order for the technology to bring in systemic efficiencies, a critical mass needs to be attained. As an infrastructure technology, all major players in the market need to collaborate to define standards in a democratic manner. The blockchain community is indeed witnessing unprecedented levels of industry collaboration between players who are otherwise competitors in the space. Because of the cost of moving from one infrastructure technology to the next, an open source collaborative approach is the most promising way forward. As you will learn in Chapter 2, "Introduction to Hyperledger", Hyperledger's mandate is to develop and nurture this ecosystem to develop the future of business blockchain technologies.

# Chapter 2 - Introduction to Hyperledger

## Section 1 - Hyperledger

### Video 12 - Hyperledger (Navroop Sahdev)

Hyperledger is an open source effort created to advance cross-industry blockchain technologies.
It's a global collaboration hosted by The Linux Foundation that encompasses various industries and organizations worldwide.
You may think of Hyperledger as an operating system for marketplaces, data sharing networks, microcurrencies, and decentralized digital communities.
A shared goal is to significantly reduce the cost and complexity of doing business.
Hyperledger blockchains are permissioned blockchains, which means that the parties that join the network are generally authenticated via an identity module.
Essentially, Hyperledger blockchains are specifically designed to be enterprise solutions.
If you look at permissionless blockchains, like the Bitcoin blockchain or the Ethereum blockchain, anyone can join the network,
which means there would invariably be some malicious actors within the network.
Hyperledger reduces these security risks, and ensures that only the parties that want to transact are the ones that are part of the transaction.
Rather than displaying the record of the transactions to the whole network, they remain within the parties involved.
So, Hyperledger provides all the capabilities of blockchain architecture, data privacy, information sharing, immutability,
with a full stack of security protocols, all for the enterprise.

### Video 13 - The Birth of Hyperledger (Brian Behlendorf)

It's amazing how quickly Hyperledger has developed and evolved so quickly over the past few years.
I was wondering if you could tell me a bit about the journey of how Hyperledger has come to be.
So, the Hyperledger Project began when a set of companies who were starting to pay attention to this Bitcoin space, this cryptocurrency space, this blockchain space,
approached The Linux Foundation and said "Let's do a project together".
The Linux Foundation, for 15 years, has been at the heart of the Linux ecosystem,
bringing together companies and developers to try to, you know, serve, say, air traffic control to the development of a common technology platform.
And, over the last few years, it has grown into other related technology spaces: software-defined networking, cloud computing,
all these kinds of things... the mains that also needed this focused effort to bring these two kinds of communities together.
So, it's very natural when companies like IBM, or even new ones, that had never worked with The Linux Foundation before,
like JPMorgan, or startups in this space, like Digital Asset, when they started to talk with each other, and tried to figure out where a good home for this would be,
they approached The Linux Foundation, right?
So, some conversations got started, and there was a sense that what was interesting about this space wasn't so much the cryptocurrencies, and, you know, the make-money-fast kind of mentality,
but the underlying distributed ledger and smart contract technology platforms, right?
And there's still a lot of hard work to do to figure out the right approaches to this.
So, in December of 2015, The Linux Foundation, in conjunction with those companies, and about 30 more, announced the launch of the Hyperledger effort.
alright, the Hyperledger Project, which we really just call Hyperledger now.
The first code drop, meaning the first release of software, happened just two months later, in February of 2016,
when the Fabric codebase came over.
Initially, it had been built inside of IBM, but, when it came over, it was now part of the community, right, followed soon after by Sawtooth Lake.
And it wasn't just code; the community started to meet face to face on a pretty regular basis, about once every two months.
And this was because there was a lot to sort out, a lot of knowledge to share.
I joined in May of 2016, so, a little bit of a late comer, I guess, to the launch of it.
But, I joined partly because I saw how transparent, and how engaging, even from day one, all of these processes have been.

### Video 14 - The Importance of Open Source (Brian Behlendorf)

So, you had mentioned before how Hyperledger is different from other consortiums because of its focus on creating an open community, not just open sourcing code.
Can you tell us a little bit about why this is important?
So, open source communities, I believe, live and breathe on not just, you know, reporting bugs or, you know, downloading code,
but, actually, live and breathe on true collaboration, on saying not just, you know, "I have a bug and somebody needs to fix it",
but, instead, saying "Here's how I'd like to solve this", right? What do people think?
"Here is a design for implementing a new feature." What do people think?
And I think the evidence shows that that creates higher quality code. It also creates more long lasting code.
I don't think you have a project like the Linux kernel, which has now been around for 26 years, right, without having a mechanism for a community to develop an institutional memory, right?
Why were certain decisions made? What were some ideas that were proposed and, ultimately, found to either be shot down or not really good enough, right,
so that we don't end up changing things back and forth, right, we don't end up making mistakes that we could have avoided before or learning from previous...
how do we make sure we learn from previous mistakes, right?
And that's only possible in an open source community if, on top of just releasing code, you're also engaging in the creative process itself, and making that public facing.
And I think, really, we found out over 25 years of open source that that's the best way to build trustworthy software.
I believe it leads to higher security software and higher quality software, but really, the question is trust.
This is code that sits... At Hyperledger, this is code that will sit at the heart of these enterprises.
This will be their system of record, right? So, it's essential that we develop this code in a trustworthy way and, while we do all sorts of things to help them trust the data in the system,
ultimately, they have to trust the software, as well.
And what I hope is that, through these processes, they can rest assured that, when they pick up Hyperledger, anything, right, that anything will be software that they can trust.

### Video 15 - Software Governance of the Hyperledger Projects (Brian Behlendorf)

How does the software governance of all of the Hyperledger projects work?
So, in open source projects you do... it's not a free-for-all, right? It's not just everybody throwing in every line of code,
hoping that what, you know, it sticks to the wall, and that everything is fine, right?
There actually is a development process that involves decision-making about what comes in and what doesn't, right?
At the core of each of the projects at Hyperledger is a set of maintainers.
These are individuals who either were with the project when it came in, as initial maintainers, right,
because they had been working on the code before, or were invited in by that initial set of maintainers to become maintainers,
after demonstrating, you know, a history of contributions to the project, alright?
These are now individuals who are trusted.
Once you're in that group, obviously, everything those maintainers do is public.
If they commit to the source code repository, approve a a patch, a commit request, or pull request,
everything they do is public anyway, so there's always that accountability for their actions.
If somebody does something wrong, anybody can always say "I think that's wrong",
and the set of maintainers can sometimes come to a decision to reverse a commit, right?
That's within their power.
But, it's really up to those maintainers to also chart the path forward: what's the roadmap, when will we do the next release, right,
the next minor point released, the next major release.
But, obviously, they do that in a public way.
Sometimes, they'll use a phone call, sometimes, they'll use chat on Rocket Chat, sometimes, they'll use email,
but they know that their job is to be accountable and responsible to the broader development community.
Now, from a Hyperledger perspective, if we leave it up to the projects to really decide the roadmap of what they're trying to solve,
there's a group called the Technical Steering Committee, though,
that is elected by all the contributors across all the projects, not even just the maintainer...
anybody who has contributed a line of code, contributed to the wiki in some substantial way,
they elect a group of eleven developers who form this Technical Steering Committee.
And the TSC is kind of an oversight body.
They make sure that the projects are growing, and that they're healthy.
They review activity in those projects, they also approve new projects when they come in, and they approve the graduation from the Incubator, right?
What they don't get to do is, you know, tell us, tell a project "Hey, you're working on the wrong thing. Go work on this, instead", right?
They really have to depend on this kind of decentralized governance, right, to aim in the right direction.
By and large, we try to make sure though that every project has some sort of relation to distributed ledgers and smart contracts.
Our goal is not to be the GitHub of distributed ledgers and smart contracts projects.
There's already a GitHub for that, alright?
We want these projects to be a curated, you know, coherent portfolio of different projects that might even compete with each other, right?
In many ways, Fabric and Sawtooth and Iroha do overlap, and you can build an implementation of something in all three of those. That's okay, right?
We're going to discover over time how these projects differentiate with each other,
and it's the role of the Technical Steering Committee, and a bunch of other committees we have around identity, and architecture, and white papers, and things,
to try to weave these different efforts together in something that looks coherent, something that makes sense for developers.

### Video 16 - Why Businesses Choose to Use Hyperledger? (Brian Behlendorf)

And, as a follow-up, why are businesses choosing to use Hyperledger over other distributed ledger technologies?
So, companies, when they decide what open source technologies to use, right, they should evaluate an open source project based on a number of factors,
not just, you know, is the code available, does it run, how mature is it, right, have they released a 1.0, and a 1.1, and a 1.2...
You want to see a kind of a regular stream of these things.
We also believe companies make decisions... I believe companies make decisions about what open source technologies to choose based on the health of the community, right?
And how many other companies are embedding this technology inside of their own solutions, right, inside of other products and services,
how many people out there are using it... that sort of thing.
And so, at Hyperledger, what we're trying to do is not just build a very healthy developer ecosystem around our technologies.
We also do a lot to try to talk with our members and others who are using Fabric, or using Hyperledger Sawtooth, or these other technologies,
to understand where are they using it and what's the value that they're getting from it.
And can we talk about that to the outside world, alright, which is hard.
Sometimes, people don't want to talk about their behind-the-scenes projects, right?
But, when we can talk about the application of that in music licensing, or food supply chain projects, alright,
and start to talk about kind of a higher level impact that these projects can have,
then, that I think gets companies really interested.
But, they don't make the decision to jump in, unless they can see that this is not just a piece of code, that this is a movement.
So, that's really what we're trying to build, and that's why we believe companies can confidently decide to pull down and start using Hyperledger Fabric, Hyperledger Sawtooth, and any of these projects.
And hopefully, become contributors to them, as well.

## Section 2 - Hyperledger Frameworks

### Video 17 - Incubated Hyperledger Projects (Brian Behlendorf)

What are the projects currently being incubated by Hyperledger?
So, at Hyperledger, we have a total of eight different projects, actually, as of this week [October 2017].
Because we always have the door open to new projects joining.
And we evaluate those projects on, you know, how do they fit with the portfolio of other projects,
are they mature enough to really understand, you know, where they're  going to go and who the developers are around them...
But, every new project that comes in, comes in through something called the Incubator, right?
Because we figured there's a period of time where we need to do a number of things:
we need to make sure that all of the intellectual property associated with that code is actually being contributed correctly,
and, more importantly, we need to make sure that the development team that is coming along with that code understands how to use the tools,
but also understands how to work collaboratively and publicly. Alright?
This is sometimes a new thing for many of these types of projects.
So, Fabric has graduated from the Incubator, to be an ordinary full-fledged project in Hyperledger.
Sawtooth has graduated as well. [Iroha has also graduated from the Incubator.]
The other projects are still working through that process, and the goal is to get every one of the projects through.
We don't try to apply a flamethrower to, like, nudge them through too strongly, right?
But, you know, the hope is that, over time, that they do become that,
and that becomes yet another trademark, a signal to the public that this is now code that they can trust, right?
That this is now something they can build upon.
And so, that's one of these stages. Another one is, for example, releasing as 1.0, which the Fabric community did a few months ago.
So, we have all these signals that we hope to be able to send to the public, and these other projects are still on that path.

### Video 18 - Introduction to Hyperledger Sawtooth (Courtesy of Sawtooth)

Meet Rich: he owns a popular seafood restaurant in Boston, Massachusetts.
Rich strives to serve only the freshest, highest quality fish to his patrons,
but he often has difficulty knowing exactly where it was caught, how it got to his restaurant, or if it's even the right species of fish.
From ocean to table, the  fish supply chain is difficult to track, and usually follows this pattern:
the fish is caught by a commercial fisherman in the ocean,
the fisherman then sells the fish to a market, processor, or broker,
a distributor then transports the fish to a restaurant or grocery store for a consumer to purchase.
Rich typically only buys from one or two fish distributors that he has built a foundation of trust and personal history with.
He'd like to expand his menu by adding some different kinds of seafood from other distributors,
but he worries about integrity, and for good reason.
He recently read a study by Oceana, which showed that 33% of fish purchased from retail outlets is incorrectly labeled,
and that illegal fishing represents losses between 10 to 23 billion dollars worldwide.
Rich knows that mislabeled and illegally sourced fish could hurt his customers,
his restaurant's reputation, and the environment of our planet.
Fortunately for Rich and others in the seafood industry,
Sawtooth Lake  blockchain technology can provide an immutable record of the provenance and  lineage of various goods, like fish.
In combination with Internet of Things-enabled sensors, Sawtooth Lake can manage the ownership and journey of fish from ocean to table.
Sensors can be attached to fish the moment they are harvested,
immediately and continuously recording data such as the location and  temperature of the fish.
Now, Rich can validate when and where his fish was caught, and that it was stored properly on ice while it was transported.
The Sawtooth Lake platform can also manage the Chain of Custody fish,
enabling ownership to be transferred and traded on the blockchain according to smart contracts.
With Sawtooth Lake as a traceability blockchain, Rich can easily see which fishermen meet his quality standards and feels comfortable doing business with new tradesmen.
When he serves up a new special to a  cherished customer, he can confidently and accurately assure her
it's the type of fish she ordered, it was stored at safe temperatures, when and where it was caught, how long it took to get to her plate, and the fish's name... just kidding.
Sawtooth Lake blockchain technology can be used for a wide variety of applications,
from capital markets to international trade.
The Internet of Things ties the physical world to the digital world,
with Sawtooth Lake recording the generated data in a way that all parties can trust its accuracy and completeness.
This is extremely useful for tracking perishable goods, like fish.
These sensors can track many key parameters, such as location, temperature, humidity, motion, shock, and tilt.
This technology could be added to any package or sensitive good you're entrusting to other parties.
The blockchain will ensure the data is secure and tamper-proof, so that you know what you're getting, and that you get what you pay for.
Sawtooth Lake creates a digital platform enabling physical traceability in a trustless world.

### Video 19 - Unique Characteristics of Hyperledger Sawtooth (Dan Middleton)

Some unique characteristics of Hyperledger Sawtooth are:
one, I think we are the only Hyperledger project that provides distributed state agreement, and that's a mouthful.
But what it means is that you can trust that every node in the system has the same understanding of information,
that you don't have nodes that are, say, computing interest differently than a different computer on the network,
and are gradually changing their database so that it's no longer really in agreement with the rest of them.
Something else that's unique about Sawtooth is we thought a lot about our transaction processing interface,
and we're now able to create adapters for any kind of transaction logic.
This was evidenced recently by our integration with Hyperledger Burrow.
And you can now run any kind of Ethereum Virtual Machine code, like Solidity, for example, you can compile that and run that on Sawtooth.
So, when you think about where is a home for things inspired by Ethereum or Solidity code created for Ethereum,
how would you deal with that in an enterprise environment,
you think Sawtooth and Burrow is the answer for that.

### Video 20 - Hyperledger Sawtooth Characteristics Relative to Use Cases (Dan Middleton)

So, unique characteristics of Sawtooth... There's several, but one that comes to mind for a provenance or supply chain use case,
is that that network will probably grow over time.
The reason that a lot of us are starting blockchain networks, a lot of companies are invested in looking at blockchain networks,
because we think that we're going to be in them for a long time and they're going to continue to grow.
Sawtooth is designed so that you can grow the size of the network,
you can actually change the consensus mechanism on the fly...
I think this is a unique characteristic of Sawtooth amongst all of the other ledgers...
you can submit as a transaction and then have a policy within your network to accept that new consensus,
and then, your network can move from say a PBFT-style consensus to something like PoET, or some sort of random leader election consensus...
It allows you to have tens, or hundreds, or potentially thousands of different nodes on your network,
and you really can't beat that kind of availability and integrity guarantees, or that kind of flexibility for a network that needs to be up for years.

### Video 21 - What Is Unique About Hyperledger Fabric? (Chris Ferris)

Well, I think, again, the primary distinction that we have with Hyperledger Fabric is that it is an implementation of a permissioned blockchain distributed ledger technology.
And this is independent, or distinguished from implementations such as Bitcoin and Ethereum,
and various others, that are essentially public, permissionless networks, where everybody can join anonymously.

### Video 21 - Hyperledger Indy (Nathan George)

The Hyperledger consortium has many different projects that focus on different aspects of how ledgers can work and what use cases they can be applied for.
Hyperledger Indy is a distributed ledger purpose-built for doing distributed identity,
and what that means is, it allows you to have a route of trust to manage the keys, schemas, proofs, and other information that you need to,
in order to enable trusted peer interactions between different identities, as stored on a Hyperledger Indy blockchain instance.
So, if you have an identity it belongs to you, and only you, and no one can pull the plug on you.
And you can use that identity to manifest different correlatable pieces of data between you and other identities you want to interact with,
without leaking private information or disclosing information that you don't want shared across all those different aspects of who you are.
And when you control your identity, it makes it so that you are also a party to  the kinds of data sharing, claims, and proofs that can be made about you,
as information is shared across all the different interactions you might do online.
One of the main use cases of Hyperledger Indy is to create a global public utility for identity that's being created by the Sovrin Foundation,
which allows us to take these identifiers, and to anchor them on a public ledger,
so that different pieces of truth or pieces of information can be trusted and shared with other people across the world,
and they can be trusted and validated, so that self-attested data can be shared, as well as third-party attestations can be shared across all kinds of interactions and across all kinds of data silos,
and what this makes possible is the ability to no longer have to function as an identity provider as a business,
but to rather let users authenticate based on the attributes that they're willing to store and share themselves,
which allows for GDPR-compliant use cases, where you're expressing consent on behalf of the user, and also reducing the amount of liability contained within a business,
because the data can be kept with the user and presented to you again in a way that you can trust and validate,
that what has been said, really was said, and is trusted by the other parties you do business with.

### Video 22 - Hyperledger Composer (Simon Stone & Kathryn Harrison)

So, Hyperledger Composer includes a set of components that will be familiar to a wide range of Javascript developers,
whether you are a frontend developer, working on UIs, or a backend developer working on service or code.
And these components should make it really familiar and easy for Javascript developers to get going building blockchain applications.
We've got a data modeling language, that allows you to quickly describe your blockchain business network.
You can implement your business logic using standard Javascript code.
We have a web-based playground for learning the concepts of Composer, trying it out, testing it,
looking at our set of sample business networks and extending them,
we have some client libraries for building Javascript applications, editor plugins for your favorite editor, whether it's Atom or Visual Studio Code,
we have some command line utilities for your administrative system, to create scripts to automate tasks within the blockchain.
We can also generate skeleton applications.
So, once you have taken the time to model your blockchain business network, model the assets and participants,
in a couple of minutes, we can generate a UI application for you.
All you have to do is run one command, answer a set of simple questions,
and then you have a fully functional UI app that you can start tailoring to your user experience.
And finally, we are big on APIs.
We really want to make it easy to expose your blockchain applications via RESTful APIs that you can use in your client applications, or for integrating with your existing systems.
And so, again, we provide a simple command, you run it, you connect it to your blockchain  business network, and out pops this REST API that you can start building against.
Hyperledger Composer is a developer tool that makes it very easy to create applications on blockchain.
If you think about the blockchain world, you have multiple organizations that need to come together and agree on what types of participants, assets, and transactions are taking place.
And so, Composer allows developers to very quickly and easily model out the key components of their business use case,
in a way that both business and technical teams can align around, to create APIs that make developing applications very simple.
Not only does it make it easy to create applications for blockchain,
but it also makes frontend and full stack developers that have Javascript skills into blockchain developers.

## Section 4 - Q/A with Brian Behlendorf, Executive Director of Hyperledger

### Video 23 - Reasons Why Developers Would Become Interested in Open Source Software

So, many of the students taking this course are more familiar with working  with Devs within the same room.
But why do you think developers would be excited in becoming involved with open source projects, such as Hyperledger?
Well, open source software represents, generally, the largest software development classroom ever, right?
When I was learning about software development as an undergraduate at the University of California at Berkeley,
I was taking classes, you know, I was learning kind of the formal bits about, you know, data structures and algorithms,
but the biggest education came from sitting on development mailing lists around the standards around HTTP and HTML,
and, eventually, the software development mailing lists and open source communities for the early days of the web.
And seeing, really, how software gets built, right, what are the trade-offs, what are the negotiations, the back-and-forths, the messiness of software development,
which doesn't look that different than, say, how Congress, you know, works on the bills sometimes, right?
Sometimes, it can be, you know, not very pretty, but you realize that software engineering is as much a technical pursuit, as it is a social pursuit.
And, in open source projects, I think we've figured out how do we have technical differences of opinion and work through them,
how do we create the best software, the software with the greatest longevity, right? why should we document our code...
Well, it's because we don't want to have to answer silly questions from the next person trying to understand what we wrote, right?
So, all of this is a really great education, I think, in understanding how to write higher quality code, whether that ends up being open source code or not...
That's one reason, I think, for developers to participate in open source projects, whether at Hyperledger or any place else.
The other is that open source projects are a really good way for you, as a software engineer, to understand what are the kinds of companies I want to work for, right?
The ones that are actively involved in open source projects, right?
How do I get to know people at those companies, right? And also, make them aware of my own skills, right?
And start to develop my own public history of my contributions.
These days, if you're a software engineer, if you're a software engineer and you're applying to any place interesting, they're going to look at your GitHub repository, right?
They're going to want to know about your history of contributions to open source projects as a way to evaluate your skills,
and not just technical, but also your communication skills, your collaboration skills...
So, all of that means working on open source projects can be tremendously beneficial to your own ongoing education, as well as your ability to build your career.

### Video 24 - Hyperledger vs. Apache

While at Apache, you were able to successfully build an open software developer community.
What are some similarities and differences between Hyperledger and Apache in its evolution as an open source project?
Right...  Well, on the Apache web server project, which later became the Apache Software Foundation,
a lot of what happened was due to luck, was due to inheriting a tradition that had been established since the beginning of the internet,
of technologists working together on common standards and common code.
And so, there was kind of a DNA that was built-in and, you know, the web was not that complicated at that point in time, either.
These standards were pretty simple, right?
So, we just kind of did what seemed natural. We started a mailing list.
We started an issue tracking system, a version control system, and we just started working together, very ad hoc, very informally.
And we became a non-profit about three years after we got started, when we realized we wanted a little more formalism, and a little more protection for the developers.
But it was all very informal, ad hoc, and many developers took on roles beyond development, such as marketing, such as legal, such as accounting, right?
And so, Apache's culture has been very much almost like a guild, right? Almost like a user community... a very community-driven kind of thing,
where there's this validity that comes from that grassroots-kind-of-sense, right?
Which is great for the kinds of projects that Apache was interested in.
And Apache has become a home for over 300 different individual software development projects, beyond the web server, right?
But it has always grown by happenstance, and it's always been open to whatever technology project wanted to come in.
So, there are some upsides and downsides to that all, right?
One of the downsides is, by not having a full time staff, it's hard for Apache to really take advantage of all the opportunities out there, to get the word out about who they are.
It means that developers, you know, have to do these non-developer activities, right?
And it's hard to do things like police your trademark usage, right, when people are working as volunteers.
So, The Linux Foundation took a slightly different approach.
The Linux Foundation said "We don't..." You know, just like with Apache, "we don't want to write software, we don't want to have to pay all the software developers",
because there's actually a lot to the validity that comes from all of the software development happening by volunteers,
but there's a lot of non-software development things: marketing, legal, PR, and even the hosting of meetings, the hosting of phone calls,
all of the logistics of helping these communities operate that perhaps can be taken on, right, by a full-time staff.
Now, how do you pay that staff, right? You could ask for, you know, cutting charity contributions, right?
But, a better, more scalable approach is to ask companies to join as corporate members of an organization, right?
And, they don't get any special privileges on the code, right?
Well, they don't get their patches in by default, they don't get to veto anyone else's work.
If you're a developer from IBM, there's no special status.
You have to still prove your worth, and to which, you would, you know, and be seen as a peer to, say, a 15 year old kid in Romania, who also is really eager to work on distributed ledgers and smart contract systems.
And so, but what members do get is some help in marketing their activities, building on top of Hyperledger projects, ways to participate at the events that we do.
When a journalist calls us and asks us for a story about somebody doing something interesting with Hyperledger, we've got a set of members that we... whose stories we can draw from, right?
So, this balancing act of, you know... as I mentioned, there's a developer community, and there's a commercial community, a corporate community...
That's the balancing act... that The Linux Foundation has really developed a process for, a template for, and a real science around, and that's what we're bringing to bear on the Hyperledger project.

### Video 25 - A Key Feature of Hyperledger Fabric, Hyperledger Sawtooth, and Hyperledger Iroha

Could you highlight a key feature for each of the three Hyperledger frameworks: Hyperledger Fabric, Sawtooth, and Iroha?
So, Fabric, is one of the most mature technology projects in Hyperledger.
It was the first to hit a 1.0 release, and that release, the architecture, the version 1 architecture reflects a tremendous amount of trial, proof of concept and pilot trial, of Fabric,
with a lot of different companies out there.
And they discovered things like, for scalability reasons, you wanted to separate out the ordering service into a separate set of nodes.
Or, you might want to be able to support subsets of exchanges, so that is why there is a feature called private channels, right?
And so, those are some of the distinctive parts of Fabric.
For Sawtooth, there is a number of distinctive features, but the two that stand out are a consensus mechanism called Proof of Elapsed Time,
which takes advantage of some special features on Intel's chips, and then, an approach to smart contracts called transaction families,
where you essentially predefine a set of acceptable templates for smart contracts that, then, the rest of the network can use.
And that is a safer approach to doing smart contracts than a fully programmable, general purpose programming language.
Finally, Iroha, Hyperledger Iroha, the really distinctive thing about that is it's written in C++, it's very tiny and tightly coded,
and it's got a terrific set of mobile libraries, as well.
These are all slight differences.
Our hope is that, over time, as the projects evolve and mature, and all of them get to a 1.0,
that we find ways to bring them even closer together, and make them more compatible and modular and find ways for them to work with each other.

### Video 26 - Interoperability Between Hyperledger Frameworks

What do you think will help foster interoperability between these three  different Hyperledger frameworks?
So, there's a number of things that we can do to assist in the interoperability between the different projects at Hyperledger.
One thing we're working on is kind of an overall architectural view of all the different projects, right?
What are the technologies that sit at kind of the DLT layer, at the smart contract layer, where does identity sit in, right?
And then, we can start to look at these projects and go, "Okay, could we put Fabric down here, could we put Burrow up here?"
Maybe we start to tease apart the distributed ledger part of Fabric from the smart contract part of Fabric, right,
into separate components, so that, when somebody new arrives at the project, or they take a training course like this,
they can start to pick and choose, you know, as building blocks, as appropriate for whatever use case that they want to target, right?
And so, that's something over time, this kind of modularity approach... Along with that, defining standardized APIs between these different levels, right,
so that we can get to an ideal, where you could pick the Ethereum virtual machine from Burrow, and run that on top of Fabric or on top of Sawtooth,
and, in fact, the Sawtooth and Burrow communities have now actually progressed, and you can now run Ethereum smart contracts on top of Sawtooth, which is pretty cool.
So, I think we'll see more activity like that.

## Section 5 - Learning Objectives (Review) and Conclusions

### Video 27 - Blockchain Security at Hyperledger (David Huseby)

So, security with distributed ledgers really begins here at Hyperledger with our culture of secure software development.
Every aspect of the software, from development, through testing, through bug fixing, and vulnerability resolution, it's done in a completely open process.
It's open to anybody to participate.
We have maintainers that do all the code reviews.
Changes to code is driven by requirements, and patches come in to implement those requirements...
They're reviewed... we have requirements for tests to be written before it's accepted, and we have pretty rigorous testing infrastructure in place.
We use continuous integration, so, it's always building,
and we have also initiated security reviews outside security audits of all our projects as they approach 1.0.
And it's that culture that really builds the foundation of trust for the Hyperledger projects.
Because we're radically transparent, and because we do the correct things from a software engineering perspective,
we deserve the trust that consumers of our products put in our hands.
And then, building on top of our process, comes all of the cryptography and the data resiliency that you get with a distributed ledger.
So, once we can ship a product, a piece of software that's been built to the best of our ability,
then the guarantees provided by the cryptography really carry weight, or really, are ironclad.
So, it's a very holistic approach to security here at Hyperledger: everything, from the way we write software to the way the software works.

### Video 28 - How Will Hyperledger Change the Blockchain Ecosystem? (Brian Behlendorf)

How do you think Hyperledger will change the industries that adopt the technology?
So, in the Internet era, we, as technologists, have gotten really good at building big central databases and big central services, right?
Think about the move to the cloud. The move to the cloud wasn't a move to, you  know, a really dispersed, diffused, decentralized kind of system.
It often meant a move to one company's servers, right, or one company's products, right?
And I feel like, today, the Internet is more decentralized... more centralized than it used to be, right?
And that decentralized systems tend to grow quicker, they tend to be more adaptable, that nature looks a little bit more decentralized, right?
And, for businesses, I think you often don't want to be just sitting on the outside as a satellite on another centralized business, right?
Everyone would want to be the Uber of this, or the Uber of that.
Well, that's great for Uber and its investors. It's not so great when you're sitting on the outside, right?
So, a lot of industries kind of want... don't want to see their own industry move into that centralized approach.
And, typically, today, to be able to facilitate that, they have lots of point-to-point integrations, right?
Something like Hyperledger offers the potential for integration of an industry at a time, right,
into a system that can not only become a system of record for recording transactions between parties in a network, in a marketplace,
but also allow for the automation of a whole bunch of business processes through the use of smart contracts, right?
And, in a permissioned ledger, you still have an organization that acts somewhat like the referee on a football field, right,
sets the rules of the game, watches how players play and, if somebody acts out of turn, even if the technology allows it, if they violate the spirit of the contract so-to-speak, or the human conditions,
then, the referee can kick them out. And, by the way, if the referee does their job poorly, the two teams can kick the referee out, right?
So, this type of governance mechanism for something like a football game, right, is actually not too far from the kind of governance mechanisms that many industries deploy today, right?
With distributed ledger technologies like Hyperledger, we can actually have the information systems work and look a lot more like the way that the business processes look and work,
especially in a more decentralized setting.
We can avoid the over-centralization of industries, and the over-centralization of society through the use of these technologies.

### Video 29 - 