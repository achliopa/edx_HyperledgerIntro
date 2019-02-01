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

# Chapter 3 - The Promise of Business Blockchain Technologies

### Video 29 - Introduction (Nathalie Salami)

This chapter is designed to help people evaluate whether blockchain tech, including the Hyperledger frameworks, are right for their business,
and where best to implement this new technology.
We will cover the ways industry is using  blockchain technology today, and show you some common features of blockchains that can provide efficiencies in business.
The finance industry, in particular, put a lot of resources behind blockchain tech early on.
They have created blockchains and distributed ledgers for transferring assets and recording trade agreements.
Many types of transactions, such as private company stock sales, bonds, options, and cash transactions have all been recorded on permissioned blockchains.
Blockchains are very good at recording state transitions.
And just as the finance industry uses it to record who owns an asset at any given moment in time,
the legal industry has also implemented blockchain technology to record property rights and the transfer of those rights.
It will be interesting to see how the courts adapt to recording contractual agreements on both public and permissioned blockchains going forward.
Insurance companies act as a trusted intermediary, pooling funds from unaffiliated individuals.
By holding these funds, they spread the risk of catastrophe amongst all clients.
Clients of these insurance companies trust that, when something happens, the insurance company will pay them.
Blockchain tech may be able to disrupt the insurance industry, as they may leverage the Hyperledger frameworks as a nexus of trust that controls claim payouts.
The healthcare industry has also found distributed ledger technology to be useful to record and share data,
such as patient health records, or pharmacy information.
Finally, several industries that deal with materials and product supply chains have began using blockchain and the Hyperledger frameworks for improved resource, sourcing, and allocation.

## Section 1 - Existing Blockchain Use Cases

### Video 30 - Hyperledger Advantages for Businesses (Brian Behlendorf)

Technologists are studying the Hyperledger protocol and applications.
What should business professionals know about the Hyperledger project?
So, business professionals who should... when they see the word 'hyperledger', right,
they should associate that with a set of principles that have to do with the creation of high-quality, trustworthy software, right?
First of all, they should associate it with open source development practices,
they should know that any project that carries the term 'hyperledger', 'hyperledger foobar', 'hyperledger rhubarb', right,
that these are projects that have been collaboratively built,
that have been vetted by multiple developers working in concert on the technology,
that it's as secure as we can make it, because the code is out there.
We try to hire folks to vet it, but we also... fundamentally, you shouldn't trust software that you can't see the source code to, right?
So, that brand association, that trademark should really come to be associated with open source, with security, as well as with a sense of process,
like something that can't just show up one day and become a Hyperledger project.
The Technical Steering Committee has to approve any new proposed submission, and they have a pretty high bar.
Our goal, again, is not to be the GitHub of projects, even in the distributed technology, or distributed ledger, or smart contract space,
but to really have a high quality portfolio of these different efforts.
Finally, they should realize that they can build their business on top of Hyperledger technologies,
they can use it all day long, they don't owe anybody a fee, a license fee, a patent license, nothing,
and, if they feel like it, if they want to contribute, there should be an easy glide path to having their technical teams get  deeper into the code,
become contributors, and even help set the direction for the technology.

### Video 31 - Blockchain Use Case (Brian Behlendorf)

What is your favorite blockchain use case?
So, you know, what gets me up in the morning isn't so much making Wall Street, you know, a few milliseconds faster or...
I mean, to some degree, it's nice to be able to talk about, you know, bank payments taking five minutes, rather than three days, okay?
That's kind of a win! But, I'd say, the use cases that wake me up in the morning have more to do with positive social impact, alright?
Projects that, at the same time, is making a difference in fighting slave labor, say, fighting the conflict diamond problems in the diamond supply chain,
or fighting the illegal fish catching and the slave labor practices that happen in the fishing industry, by providing better provenance tracking for the fish supply chain...
But, I'm also very much intrigued by identity projects out there, and the potential for distributed ledger applications to take something like India's Aadhar, which is their national ID system,
and reinvent that as a decentralized privacy-protecting national ID system, rather than as a centralized, potentially privacy-invasive central ID system.
So, lots of companies are starting to figure this out,
lots of companies with large amounts of customers are starting to figure this out,
and we certainly could do with fewer privacy breaches out there, and less surveillance capitalism,
which, you look at all these businesses... many of them have business models based on learning too much about people.
I think through distributed ledger technology, ironically enough,
we can actually come up with systems that make management of the distribution of personal data much easier to put in the hands of the individuals themselves.
And so, that's really what gets me excited.

### Video 32 - Business Interest in Hyperledger (Brian Behlendorf)

Where have you seen the most industry activity in Hyperledger, to date? (October 2017)
So, much of the interest in distributed ledger technology has come from the finance industry, much of the initial early interest, right?
This is an industry that has long had not just ledgers, but a need to reconcile those ledgers across organizations.
Like, when you route a payment from one bank to another, there's a little message that says, you know, this person is routing that payment to that account.
But those banks have a reconciliation process to go through that can take days, right?
That's why a payment takes days to clear, so to speak.
And, with a distributed ledger such as those implemented by projects at Hyperledger, that confirmation step, that synchronization step can be instantaneous, right?
So, the financial sector has all sorts of really easy to imagine, easy to transpose applications and needs for which distributed ledgers make sense.
If they can perform quick enough, if they can be made flexible enough, that sort of thing.
But, pretty early on, people started to realize there are these other applications, for which, you know, the need for a distributed ledger, a system of record,
to record things like the movement of goods through a supply chain, right, or potentially use it as a way to denote, say, your education record, right,
you know, what are the schools you attended... if you're a doctor, what are the certifications that you've been awarded, the licenses to practice, and where...
So, for example, the medical industry, the healthcare industry is really interested in the use of distributed ledgers for doctor certifications, provider directories, as they call them,
potentially, as well for looking at payment flows of claims, and maybe, even patient medical records.
Now, those last few are kind of, you know, more of a moonshot, because they involve a substantial amount of confidential data,
and we're still learning the best techniques for ensuring the confidentiality of transactions, and the confidentiality of data flowing across these networks.
But, I think we're gonna figure that out.
So, healthcare is big, finance has been big, and then, every sector has a supply chain components somewhere in them, right?
The food sector, the jewelry sector...
So, there's a supply chain project around diamonds to help keep conflict diamonds out of circulation,
and help make sure that, when you buy a diamond at the retail market, it actually is, you know, both the quality and from the location that it claims to be from, right?
So, there's lots of these different use cases bubbling up, and frankly, at this point, I can't imagine a sector that doesn't have a need somewhere for a system of record,
a distributed ledger, a way to record transactions...
And indeed, the kind of interest we're seeing at Hyperledger comes from so many different sectors.
Even our own membership reflects that, with members like Airbus, and Daimler, and Change Healthcare, which is a part of McKesson,
those are companies that, not only are saying "Hey, we're interested!", but have actually made a financial commitment to being a part of Hyperledger,
and to playing with that technology within their own enterprises.Where have you seen the most industry activity in Hyperledger, to date? (October 2017)
So, much of the interest in distributed ledger technology has come from the finance industry, much of the initial early interest, right?
This is an industry that has long had not just ledgers, but a need to reconcile those ledgers across organizations.
Like, when you route a payment from one bank to another, there's a little message that says, you know, this person is routing that payment to that account.
But those banks have a reconciliation process to go through that can take days, right?
That's why a payment takes days to clear, so to speak.
And, with a distributed ledger such as those implemented by projects at Hyperledger, that confirmation step, that synchronization step can be instantaneous, right?
So, the financial sector has all sorts of really easy to imagine, easy to transpose applications and needs for which distributed ledgers make sense.
If they can perform quick enough, if they can be made flexible enough, that sort of thing.
But, pretty early on, people started to realize there are these other applications, for which, you know, the need for a distributed ledger, a system of record,
to record things like the movement of goods through a supply chain, right, or potentially use it as a way to denote, say, your education record, right,
you know, what are the schools you attended... if you're a doctor, what are the certifications that you've been awarded, the licenses to practice, and where...
So, for example, the medical industry, the healthcare industry is really interested in the use of distributed ledgers for doctor certifications, provider directories, as they call them,
potentially, as well for looking at payment flows of claims, and maybe, even patient medical records.
Now, those last few are kind of, you know, more of a moonshot, because they involve a substantial amount of confidential data,
and we're still learning the best techniques for ensuring the confidentiality of transactions, and the confidentiality of data flowing across these networks.
But, I think we're gonna figure that out.
So, healthcare is big, finance has been big, and then, every sector has a supply chain components somewhere in them, right?
The food sector, the jewelry sector...
So, there's a supply chain project around diamonds to help keep conflict diamonds out of circulation,
and help make sure that, when you buy a diamond at the retail market, it actually is, you know, both the quality and from the location that it claims to be from, right?
So, there's lots of these different use cases bubbling up, and frankly, at this point, I can't imagine a sector that doesn't have a need somewhere for a system of record,
a distributed ledger, a way to record transactions...
And indeed, the kind of interest we're seeing at Hyperledger comes from so many different sectors.
Even our own membership reflects that, with members like Airbus, and Daimler, and Change Healthcare, which is a part of McKesson,
those are companies that, not only are saying "Hey, we're interested!", but have actually made a financial commitment to being a part of Hyperledger,
and to playing with that technology within their own enterprises.Where have you seen the most industry activity in Hyperledger, to date? (October 2017)
So, much of the interest in distributed ledger technology has come from the finance industry, much of the initial early interest, right?
This is an industry that has long had not just ledgers, but a need to reconcile those ledgers across organizations.
Like, when you route a payment from one bank to another, there's a little message that says, you know, this person is routing that payment to that account.
But those banks have a reconciliation process to go through that can take days, right?
That's why a payment takes days to clear, so to speak.
And, with a distributed ledger such as those implemented by projects at Hyperledger, that confirmation step, that synchronization step can be instantaneous, right?
So, the financial sector has all sorts of really easy to imagine, easy to transpose applications and needs for which distributed ledgers make sense.
If they can perform quick enough, if they can be made flexible enough, that sort of thing.
But, pretty early on, people started to realize there are these other applications, for which, you know, the need for a distributed ledger, a system of record,
to record things like the movement of goods through a supply chain, right, or potentially use it as a way to denote, say, your education record, right,
you know, what are the schools you attended... if you're a doctor, what are the certifications that you've been awarded, the licenses to practice, and where...
So, for example, the medical industry, the healthcare industry is really interested in the use of distributed ledgers for doctor certifications, provider directories, as they call them,
potentially, as well for looking at payment flows of claims, and maybe, even patient medical records.
Now, those last few are kind of, you know, more of a moonshot, because they involve a substantial amount of confidential data,
and we're still learning the best techniques for ensuring the confidentiality of transactions, and the confidentiality of data flowing across these networks.
But, I think we're gonna figure that out.
So, healthcare is big, finance has been big, and then, every sector has a supply chain components somewhere in them, right?
The food sector, the jewelry sector...
So, there's a supply chain project around diamonds to help keep conflict diamonds out of circulation,
and help make sure that, when you buy a diamond at the retail market, it actually is, you know, both the quality and from the location that it claims to be from, right?
So, there's lots of these different use cases bubbling up, and frankly, at this point, I can't imagine a sector that doesn't have a need somewhere for a system of record,
a distributed ledger, a way to record transactions...
And indeed, the kind of interest we're seeing at Hyperledger comes from so many different sectors.
Even our own membership reflects that, with members like Airbus, and Daimler, and Change Healthcare, which is a part of McKesson,
those are companies that, not only are saying "Hey, we're interested!", but have actually made a financial commitment to being a part of Hyperledger,
and to playing with that technology within their own enterprises.

## Section 2 - When to Use or Not to Use Blockchain Technologies

### Video 33 - What Enterprises Look for When Evaluating Whether or Not to Use Hyperledger (Brian Behlendorf)

What should an enterprise look for when evaluating whether or not to use Hyperledger?
So, I always try to start... suggest that people start with the business need, right,
trying to look at what are you doing in your enterprise, and probably, it will mean
what are you doing with your business partners, with your suppliers, with your customers, maybe even with your competitors, right?
What is it... what are some business processes, or some provenance tracking problems,
or a registry somewhere that, you know, you're putting too much trust in a central org somewhere,
where is there an opportunity to take a decentralized ledger approach, and a smart contract approach to solving those issues?
Start with the need, right?
In fact, one way to explore that is, you know, every industry has a consortium somewhere in that industry talking about technical standards,
talking about common business processes, and those are often the right kinds of organizations to look at doing a proof of concept with, right?
Because they often have kind of this overarching kind of view of the industry,
and they tend to be trusted by the participants in that industry.
So, often, they could come up with what's the right kind of proof of concept, or maybe even a Minimum Viable Product kind of project,
because there really is no blockchain of one, right?
It's really hard just to think about solving your own problems with a block, with a distributed ledger.
You really need to think about an industry-wide kind of approach, even from the earliest day.
Once you've identified like that kind of opportunity, you should start to ask yourself what are the characteristics of that need,
is it from a transaction rate perspective, from a number of nodes, from how geographically distributed those nodes might be,
and then, also ask yourself who are the developers that I'm expecting to be able to tap, to bring this technology to bear,
and have they started to investigate distributed ledger technology,
have they started to learn how Fabric works, how Sawtooth works...
So, I think that that's another important side of it.
As the business side of the house is trying to understand the use cases, you should really let your technology teams explore this technology,
allow them to get their hands dirty, to go to a hackathon, to take this course, to start playing with these technologies to get a more intuitive sense for what they do,
and what they can't do, right, what their limitations might be.
This is still very early days, and you still need to be smart about how do we apply these and how do we use them.
So, at some point, those two teams should meet up, right, and say "Here's what we think is really the MVP [Minimum Viable Product] or a proof of concept",
and the other team should... that comes from the technology side of the house, should say "Okay, we understand how to build this, you know,
if we, you know, shave these corners, we can do something in a week", right?
and let's just see that, you know, cheap and dirty, what it looks like.
And then, over time, start to promulgate that amongst the other partners that you think you'd involve in a distributed ledger project.

# Chapter 5 - Introduction to Hyperledger Iroha

### Video 34 - Introduction to Hyperledger Iroha (Alexandra & Arianna Groetsema)

Hi everyone! We are the content creators for the Hyperledger Iroha chapter.
In this chapter, you will learn about Hyperledger Iroha version 0.95, what makes it unique, and how to get started with this framework.
This framework is a blockchain platform implementation, designed to be easily incorporated into other distributed ledger technologies.
Hyperledger Iroha features an architecture written in C++, an emphasis on mobile and web development, and a new consensus algorithm.
Hyperledger Iroha offers many reusable C++ components, that can be used by many different blockchain platforms.
Hyperledger Iroha is dedicated to compiling a library of reusable modular components that enhance existing distributed ledger frameworks.
Now, as you go through this chapter, if you're interested in becoming more involved with Hyperledger Iroha,
there are some resources you can check out, like Rocket.Chat, which is similar to Slack, GitHub repos, and others.
Those specific links can be found at the end of this chapter.
Good luck!

## Section 1 - Key Components

### Video 35 - Hyperledger Iroha Key Components (Alexandra & Arianna Groetsema)

Hyperledger Iroha seeks to contribute three main goals:
1. Provide an environment for C++ developers to contribute to Hyperledger.
2. Provide infrastructure for mobile and web application support,
and 3. Provide a framework to introduce APIs and a new consensus algorithm that can potentially be incorporated into other frameworks in the future.
The core architecture of Hyperledger Iroha was inspired by Hyperledger Fabric, which we will cover in Chapter 7.
Hyperledger Iroha's creators have emphasized the importance of this framework in fulfilling the need for user-friendly interfaces.
In doing so, they've created a framework with many defining features,
including a simple construction, a modern C++ design, with an emphasis on mobile application development,
and a new chain-based Byzantine Fault Tolerance consensus algorithm, called Sumeragi.
Perhaps the most defining characteristic of Hyperledger Iroha is its ability to be freely interoperable with other Hyperledger projects.
The open source iOS Android and JavaScript libraries allow for developers to conveniently create functions to perform common operations.
Good luck, and let's get into it!

### Video 36 - Discussing Hyperledger Iroha with Makoto Takemiya

Hi! I'm Robert Schwentker, and this is "Introduction to Hyperledger".
Today, we'll be talking about Iroha.
Hi! I'm Makoto Takemiya, the Co-CEO and Co-Founder of Soramitsu. We are the original developers for Iroha.
We created Iroha last summer, in 2016,
and then, in 2016 in the fall, we presented it to the Hyperledger Project.
It was accepted in October as an incubation project.
What is Iroha?
Iroha is a distributed ledger platform.
We created it to be as simple as possible for developers to use, and also, to be highly responsive for mobile and other user-facing applications.
So, other projects under the Hyperledger umbrella, they focus on enterprises or enterprise systems.
We're focused more on the user-facing applications.
What distinguishes Iroha from Fabric?
So, Fabric is a really large and complex system, and it's great for enterprises that want to manage many applications on a distributed ledger, or even conglomerates of many companies.
Iroha, it's really focused much more on companies or consortia creating applications that users can use.
So, really, it's focused on the end-user, and creating applications that are as fast and responsive as possible.
Can I use Iroha with Fabric?
In the future, we really want to make that happen.
So, there's lots of research being done in the field of inter-ledger transactions, and two way pegs, and things like that, sidechains,
and there's a lot of really interesting research being done in that field, so we want to eventually incorporate that into Iroha.
Hopefully, by the end of this year, 2017, we will see.
What are some of the interesting libraries you have for Iroha?
So, we have the core system. This is called Iroha on GitHub.
We also have different libraries to help application developers.
So, we have an Android library, we have an iOS library, and a Javascript library.
Actually, someone recently made a Scala library.
And we also have a Python library, as well.
So, these are different libraries, or SDKs, that developers can use to quickly make applications,
and just to take out some of the guess work, so they don't make basic mistakes.
What do you think is one of the most interesting applications built on top of Iroha?
Right now? At this point, there's not too many applications built.
We did have a hackathon at the beginning of March in 2016, where, you know, six teams kind of built different applications,
and one of the cool applications was a kind of decentralized library, like book lending type, and the cool thing about that was,
you don't have to return a book to the library every time, you can just do a peer-to-peer, and give the book to your friend, your friend scans the QR code,
and then, the library can keep track of who has this book at any time.
And those are really interesting use cases, I think.
What do you think is a use case that could scale up, would be very interesting for a group to build on Iroha?
So, we're really interested in things like digital currencies and settlement.
So, actually, just recently [December 2016], we started a project at the University of Izu, to create a campus currency, that's useful in the cafeteria on campus and also at the store,
and, right now, it's just in the test phase, but it's really... if we could build something where we can expand that to the surrounding economic around all this...
so if we can do that, you know, it can scale to something that thousands, or tens of thousands of people can use every day.
From a business person's perspective, what's most compelling about Iroha?
What's most compelling is probably, I think, our permission model.
So, a lot of the systems, up to this point, haven't really given too much thought into assistive administration or to the different realities associated with that.
Yet, the concept of the root user group, and then, also, domains, that manage who can create assets, who can transfer assets, different things like that,
so, that's something that can allow you to fine-tune the administration and guarantee security of asset management.
If you look a couple of years into the future, how would you imagine Iroha has evolved?
So, yeah, in two years... I think what we'll see is in the Hyperledger Project, instead of having many different, you know,  monolithic silos of different projects,
like Fabric, or Iroha, or Sawtooth Lake, I think we'll see much more collaboration between them.
So, Iroha will probably be a system that kind of has a protocol that, you know, carries on our philosophy of making things really simple, and be responsive,
but, at the same time, can operate with the other projects in the systems, as well, or even systems like Bitcoin, for instance.
Bitcoin is successful in its use case, being an open system that anyone can join, so it makes sense to try to build protocols to interoperate with it.
So, interoperability is, I think, the main go within the next two years.
Great! Thanks very much, Makoto!
Thanks!

## Chapter Summary

### Video 37 -  Conclusions (Alexandra Groetsema)

Congratulations! You've reached the end of the Hyperledger Iroha chapter.
We hope you feel more comfortable with Hyperledger Iroha and are interested in implementing this in your own distributed ledger solution.
If you would like to get more involved with this open source project, feel free to join the discussions on Rocket Chat, and create issues on GitHub.
Stay tuned for another course that will give a more in-depth look at Hyperledger Iroha in the near future.
See you in the next chapter.

# Chapter 6 - Introduction to Hyperledger Composer

### Video 38 - Introduction

Hello Everyone! I'm Nicola and I'm Sasha. We are the content creators for the Hyperledger Composer chapter.
In this chapter, we will guide [you] through a demo scenario to highlight the key components of Hyperledger Composer.
Hyperledger composer is a toolset and framework that has been designed to make it easier to prototype and integrate blockchain applications with existing business systems.
In Hyperledger Composer you can develop and deploy a full-fledged blockchain network,
and use most of the functionality available to frameworks like Hyperledger Fabric.
Hyperledger Composer provides domain-specific languages for modeling, quering, and access control that simplify the development.
Also, visual components like Playground are helpful to communicate and visualize a structure, and to test the interactions over the network.
Then, starting from the actual business requirement, technical and business individuals can work together to build blockchain applications using Hyperledger Composer.
Today Composer works with a Hyperledger Fabric blockchain framework.
However, it has been designed with a view to support other frameworks down the road, such as Sawtooth or Iroha.
As you work through this section, you may want to think more about Hyperledger Composer.
There are resources you can check out like GitHub, Rocket Chat and others.
You will find the links at the end of the chapter.
Let's get into it.

## Section 2 - Installing Hyperledger Composer

### Video 39 - Technical Prerequisites for Mac OS

In this video, we will install the prerequisites on a Mac.
Let us open a terminal window.
We first check if Xcode is installed; in our case, it is.
If it is not installed on your computer, you will be prompted to install it in the next step.
Now, we install the Node Version Manager, or NVM.
You may need to reload your bash shell configuration file.
Now, we can install the LTS version of Node.js and activate it.
We now download and install the Docker Community Edition.
You may need to make an account.
We drag Docker into our Applications folder.
Now open it...
And login with your account.
Check that it works by running the "hello-world" image.
We now download the VS (Visual Studio) Code editor.
We drag it to our Applications folder.
And open it.
We go to the "Extensions" section and search for "Hyperledger".
We then install the Hyperledger Composer extension.
Let us switch back to the terminal.
In our bash configuration file, we tell NVM to use the LTS version of node.
And we can now use the node package manager to install the Hyperledger Composer tools.
After this, we download the Hyperledger Fabric development server scripts.
We extract the files and we run downloadFabric.sh to fetch the Docker images.
We can then start the Hyperledger Fabric development server and create a PeerAdmin identity card.
Finally, we start the Hyperledger Composer Playground which we will use in a subsequent video.

## Section 3 - Writing and Deploying a Business Network

### Video 40 - Deploying onto Hyperledger Fabric

In this video, we will set up a basic Hyperledger Composer business network running on Hyperledger Fabric.
We start by creating a business network with Yeoman and the Hyperledger Composer generator.
We fill in the required details, paying special attention to the network name and namespace.
We also ask to generate an empty network.
You can now create your own network or fill in the relevant files as shown in the course slides.
For simplicity, we will simply download the network from the official Hyperledger education repository.
Let's look at the files we have there.
For instance, the package.json file defines the network name and version.
It also specifies the node.js packages used.
The org.tuna.cto file contains the modeling language definitions for Assets, Participants, and Transactions.
And the logic file contains the Transaction Logic using Node.js.
We also have a test script where we hold the unit tests [that] we define for our network.
We can use the Composer CLI to create a Business Network Archive, or BNA file.
We can then install the chaincode of the BNA onto the peers.
To enable the chaincode, we use the "start" command in the Composer CLI.
Then, we import the network card which will enable us to connect to our business network.
The simplest operation we can do is to ping the network to ensure it is operational.

### Video 41 - Testing on the Composer Playground

In this video, we will learn about the Hyperledger Composer Playground.
Let's check out the Playground we started in the prerequisites video by navigating to localhost:8080 in a web browser.
You can connect to the business network we created.
Here, you can browse a readme.md file, the model file, logic file, permission file, and query file.
Let's switch to the test tab to run some transactions.
We start by creating a new Fisher participant - Alice.
Notice the field validation of working on the postal code.
Now, we can create Bob, our Restaurant Owner.
And Karla, our Regulator.
We can also create a Tuna Fish Asset.
Notice the range validator for the tuna weight.
Also note that we specify its owner to be Alice, the Fisher.
Having our Participants and Assets, we can run a "SellTuna" transaction to transfer it to Bob.
As you can see, the tuna now has a new owner.
Finally, we can browse all the transactions we have performed.

### Video 42 - Running the Composer REST Server

In this video, we will learn about the Hyperledger Composer REST server.
Let's start the Composer REST server.
We specify our tuna business network card and press "ENTER" to select the default options for the remaining arguments.
We navigate to localhost:3000 in a web browser to access the REST server explorer.
Here, we can view the actions for a participant, such as a Fisher.
These include typical HTTP verbs, such as "GET", "POST", "PUT", and "DELETE".
Let us retrieve a list of Fisher objects.
Naturally, we see Alice who we created when using the Playground.
We can do the very same thing with our Regulators, and with our Restaurant Owners, and with Assets like tuna.
Importantly, we can also run queries on the data.
For instance, let us find all the tuna that is owned by Bob, our Restaurant Owner.
Finally, the "System" tab contains API paths related to identity, the Historian, and allows us to ping the network.
Let's try it out.

## Chapter Summary

### Video 43 - 

Congratulation! You've reached the end of the Hyperledger Composer chapter.
You should now have a solid basis to try out Hyperledger Composer to mock-up a Proof of Concept or build a project of your own.
We hope that you will get involved in the community, either on Rocket Chat or the mailing lists, or contribute to the codebase on GitHub.
Do stay tuned for another course that will give you an in-depth look at all advanced feature of Hyperledger Composer in the future.
This is Nicola and Sasha signing out.
See you later!

# Chapter 7 - Introduction to Hyperledger Indy

## Chapter Introduction

In this chapter, you will learn about Hyperledger Indy; a blockchain-based system that is quite different from the other Hyperledger projects we discuss in this course. Where the other projects are general purpose blockchain systems (they can be used in many situations), Hyperledger Indy is used for just one purpose - and it’s a big one! Indy is all about identity on the Internet. It’s about being able to prove to others who you are and you being certain who they are.

What’s the big deal about identity? Well, when the Internet was first created, all of the computers that were connecting to one another were "trusted". The number of systems was small and the people running those systems knew each other so they didn’t need mechanisms to know who was sending what data between the systems. As the number of systems on the Internet grew (and grew and grew…), that trust quickly diminished and the first of many mechanisms were added to systems to identify who is contacting whom. Unfortunately, the problem has never really been solved. The most common (and universally hated) system, that of user IDs and passwords, is fraught with problems. The resulting lack of certainty of who is on the other keyboard has led to the loss of billions from hacks, data breaches, identity theft, scams and more. Further, that same lack of certainty has made many types of business transactions on the Internet impossible - the risk is just too high.

Hyperledger Indy has been created to add an identity layer to the Internet using a mechanism that is easy to use, enables online trust, and enhances privacy. It’s a big goal that is of vital importance to everyone on the Internet. And, it’s a goal that has recently become realizable with the advent of blockchain.

In this chapter, we’ll look in more detail at the identity problem and how Hyperledger Indy uses Decentralized Identifiers (DIDs) and Verifiable Credentials to add identity as a core component of the Internet. We’ll look at the blockchain elements of Hyperledger Indy, comparing Indy’s approach to blockchain with the other systems we’ve looked at in this course.

With that background, we’ll go through a couple of Indy demonstrations - a video showing DIDs and Verifiable Credentials being used, and running a local instance of Indy that demonstrates Indy’s software Agents communicating to prove who’s who on the Internet. In doing that, we’ll dig into to a question that is important to everyone that looks into Indy (and other blockchains) - what goes on the ledger?

After covering all of that, we’ll wrap up with information on how you can learn more, and possibly contribute, to the Hyperledger Indy project.

# Chapter 8 - Introduction to Hyperledger Sawtooth

### Video 44 - Introduction to Hyperledger Sawtooth (Alexandra & Arianna Groetsema)

Hi, all! Arianna and I have put together the content in the Hyperledger Sawtooth chapter.
We are so excited to share with you how this distributed ledger works, and its defining characteristics.
We will take you through how to set up a sample Hyperledger Sawtooth network, while introducing transaction processors, and walking you through writing your own.
Hyperledger Sawtooth is an enterprise distributed ledger contributed by Intel, and was one of the first projects to join Linux Foundation's Hyperledger umbrella.
We will be working with version 0.8.
This framework is modular, scalable, with an innovative consensus model, unique support for permissioned and permissionless infrastructure,
and the potential for incredibly large network sizes.
Hyperledger Sawtooth allows for confidential transactions, without passing information through a central authority.
If at any point in this chapter you want to join the Hyperledger Sawtooth community,
there's some resources you can check out, like RocketChat, which is similar to Slack,
a dedicated wiki page, GitHub repos, and others.
Links to these resources can be found at the end of this chapter.
So let's jump into this chapter!

## Section 1 - Addressing Illegal, Unregulated, and Unreported Tuna Fishing (Demonstrated Scenario)

### Video 45 - About the Demonstrated Scenario (Alexandra & Arianna Groetsema)

Hi, everyone! I hope you guys are making a big splash!
Yeah, let's ride this wave.
Globally, three trillion dollars are spent every year on marine coastal resources and industries.
Marine fisheries employ over 200 million people, from fishing, to processing, to shipping, and sales.
As much as 40% of our oceans are heavily affected by human activities such as illegal fishing.
Every year, five million tons of tuna, with an estimated value of 40 billion dollars, are sold.
This is a huge industry, and one that could benefit greatly from innovation and transparency.
With the tuna 20/20 traceability declaration in mind, our goal is to eliminate illegal, unreported, and unregulated fishing.
We will use Hyperledger Sawtooth to bring transparency and clarity to a real world example: the supply chain of tuna fishing.
We will be describing how tuna fishing can be improved, starting from the source, fishermen Sarah, and the process by which her tuna ends up at Miriam's restaurant.
In between, we'll have other parties involved, such as the tuna processor and regulators, who will verify the validity of the data, and sustainability of the tuna catches.
We will be using Hyperledger Sawtooth framework to keep track of each part of this process.
Now, as you read through this demonstrated scenario, pay attention to  the hierarchy of actors within the network, and how these actors interact with one another.
When Sarah catches tuna from a designated ocean area, she labels each and takes note of its provenance, and passes that along.
In a Sawtooth network, regulators, processors, and restaurateurs can confirm whether a particular shipment of tuna was sustainably and legally sourced.
So, I hope this gives you a great start. Let's go fishing!

## Section 2 - Key Components and Transaction Flow

### Video 46 - Hyperledger Sawtooth Key Components (Arianna Groetsema)

Hello, everybody!
We will now be going over the architecture for Hyperledger Sawtooth.
Like many Hyperledger frameworks, Hyperledger Sawtooth is exceptional due to its flexibility and modularity, and support for many different programming languages.
For example, applications can bring their own consensus modules and revert to Hyperledger Sawtooth's Proof of Elapsed Time consensus algorithm when scaling,
because, rather than relying on the capabilities of hardware, Proof of Elapsed Time is a truly random lottery system.
that stochastically elects individual peers to execute transactions.
Since this consensus method relies on trusted computing, as opposed to manual labor,
Proof of Elapsed Time allows nearly limitless network scalability.
Another modular feature is Hyperledger Sawtooth's transaction logic.
Transaction families encapsulate business logic for the network and help define architectural differences between data control logic and application logic.
If you're more interested in learning about what distinguishes Hyperledger Sawtooth from other frameworks,
look to the transaction families, how to reach consensus, batching, and transaction flow modules.
Good luck, and I'll see you next section!

## Section 3 - Installing Hyperledger Sawtooth

### Video 47 - Change Bringing Up a Sample Hyperledger Sawtooth Network

Hi, everyone! Today, I will be walking through how to install Hyperledger Sawtooth.
To start, if you haven't gone over Chapter 4, you might want to go back and download all the necessary technical prerequisites.
Just to review, you will need cURL, which should be a default, if you have a Mac or Linux.
You should have Node.js and npm, as well as Go language. And lastly, Docker and Docker Compose.
If you are uncertain whether you have any of these, I will show you some commands to check which version you have.
So, "node --version && npm --version".
And, just to confirm, this will show... these commands will show whether you have it installed. It won't install it for you.
So, we have versions for those. So, that's good.
Now, we're going to check for Go language [go version]. Great!
And lastly, we'll check for Docker version and Docker Compose version [docker --version && docker-compose --version].
Great! So, we've got versions for both of those, and, if you get errors on any of these, go back to Chapter 4, and make sure you've installed everything correctly.
So, moving on, within our GitHub repo, under Hyperledger, there's a 'sawtooth-default.yaml' file that we will need to download and run to start our example network.
So, make sure that you have Docker running. I already have Docker running before I started this video,
but go ahead and make sure you have that started, and work within this terminal window, and change your working directory to the same directory where your 'docker-compose' file is.
So, to do that, and this could be different for you, but this is just where I have it, on my machine...
Okay, so I have it in this directory [sawtooth-material], and just to make sure, I'm going to 'ls', and yes, in fact, here's our yaml file that we will be working with.
Now, an important note: make sure you don't have anything else running on port 8080 or port 4004.
If you do, you will get a couple of errors on some of our commands.
Ok, now, we're ready to run 'docker-compose -f sawtooth-default.yaml up'.
And this might take a second.
Great! So, we see a lot of things popping up in our terminal window.
We see 'sawtooth-validator' was created, 'sawtooth-client' was created,
and a lot of other great stuff that you can go through on your own.
But, this means we're in good shape.
So, now, let that keep running, and we will open another tab, and,
you should redirect to the same directory, which I've already done so.
And we're gonna run the following command 'docker exec -it sawtooth-client-default bash'
and we will see this pop up in a window [root@65e6e6681382:/#]
You'll get a different number here, but, if you see 'root', you're in good shape.
This means that your environment is now set up and you're ready to start experimenting with the network.
But, let's first confirm that our validator is up and running and reachable from the client container.
So, within this root, we're gonna run 'curl http://rest-api:8080/blocks'.
And, hopefully, you should see this. It's a JSON object with 'data', 'batches', 'header', 'header_signatures'.
So, this is a good sign.
Now, lastly, let's check the connectivity from the host computer. And you can open up yet another tab in terminal.
And, just in... whatever directory... default directory, you can run 'curl http://localhost:8080/blocks',
and you should get the same JSON object, which means we are in good shape.
Okay. So, we've demoed how to install, and, just for continuity sake, let's...
So, I just CTRL+C, let's bring down our network, which is good practice.
So I CTRL+C in our original terminal window, and, just as good practice,
let's run the following command 'docker-compose -f sawtooth-default.yaml down'.
That operation may have taken a little bit of time, but we can see here, all the containers were stopped and removed, and we are done.
And, we're ready to move on to the next section.

## Section 4 - Writing an Application

### Video 48 - Designing an Application (Alexandra Groetsema)

So far, in this chapter, we've covered the components of Hyperledger Sawtooth framework,
including the Proof of Elapsed Time consensus algorithm, transaction families, and batches.
We've also installed and spun up our very own test network, and gone through a demonstrated example detailing how Sawtooth is unique.
Now, it's time to combine what we've learned into a coded example.
Sawtooth SDKs offer transaction family developer support for Javascript, Python, C, C++, Java, and Go.
To create our simple application, we'll use the Javascript SDK,
which provides client functionality and supplies the process of making changes to the blockchain.
If you'd like to delve more into these heavy details, technical details, stay tuned for a future course on Sawtooth.
Now, before we dig into this section, I'd like to give a brief overview.
Building an application requires a few important steps:
first, defining assets that will reside in the distributed ledger,
as well as transactions that will act on these assets to change their state;
second, designing transaction logic that operates on these assets.
Now, as transactions are received by a Sawtooth node, they are forwarded to other nodes.
A node is selected by a consensus model to publish a block.
The block will contain any transactions that have been received and executed successfully.
The block is then broadcasted to the publishing nodes.
Each sawtooth node receives a published block and verifies that that block is valid.
It then notifies our application of any state changes.
By the end of this section, we'll be familiar with how to use the Javascript SDK to interact with a Sawtooth network,
and  write code logic to create transactions holding information about physical objects.
Now you are ready to start this section!

## Chapter Summary

### Video 49 - Conclusions (Arianna Groetsema)

Congratulations! You've reached the end of the Hyperledger Sawtooth chapter.
Moving forward, we hope you feel more confident with using Hyperledger Sawtooth in your own distributed ledger solution.
We have given you a great foundation in Hyperledger Sawtooth, but stay tuned for another course that will give you a more in-depth look at this framework in the near future.
This is Arianna signing up, and I'll see you all next time.

# Chapter 9 - Introduction to Hyperledger Fabric

### Video 50 - Introduction to Hyperledger Fabric (Alexandra & Arianna Groetsema)

Hi, everyone! We are the content creators for the Hyperledger Fabric chapter.
In this chapter, you will be learning about Hyperledger Fabric version 1.0, its key components, and a little bit about how it works.
By the end of this chapter, you will be able to set up a sample Hyperledger Fabric network,
along with a simple application using the Fabric Node.JS SDK.
We will also be introducing chaincode, and walk you through writing a smart contract of your very own.
Hyperledger Fabric was the first proposal to The Linux Foundation's Hyperledger Project, contributed in part by IBM.
Version 1.0 was released just recently, in July of 2017.
This framework is modular, scalable, secure.
It's specifically formulated for industries such as manufacturing, agriculture, healthcare, and capital markets.
Hyperledger Fabric is revolutionary in its ability to allow entities to conduct confidential transactions without passing through a central authority.
Now, as you go through the chapter, if you are interested in becoming more involved with Hyperledger Fabric,
there are many resources you can turn to, such as Rocket.Chat, which is very similar to Slack, GitHub repos, there's meet ups that you can go to, and a dedicated wiki page, as well.
And there are many others. Those specific links you can find at the end of the chapter.
Let's get into it.

## Section 1 - Addressing Illegal, Unregulated, and Unreported Tuna Fishing (Demonstrated Scenario)

### Video 51 - About the Demonstrated Scenario (Alexandra & Arianna Groetsema)

Hey, everyone! I hope things are going swimmingly!
Yeah, let's just keep swimming right through this chapter.
Globally, three trillion dollars are spent every year on marine coastal resources and industries.
Marine fisheries employ over 200 million people, from fishing, to processing, to shipping, and sales.
As much as 40% of our oceans are heavily affected by human activities like illegal fishing.
Every year, five million tons of tuna, with an estimated value of forty billion dollars, are sold.
This is a huge industry, and one that could benefit greatly from innovation and transparency.
With the Tuna 2020 Traceability Declaration in mind, our goal is to eliminate illegal, unreported, and unregulated fishing.
We will use Hyperledger Fabric to bring transparency and clarity to a real-world example: the supply chain of tuna fishing.
We will be describing how tuna fishing can be improved, starting from the source, fisherman Sarah, and the process by which her tuna ends up at Miriam's restaurant.
In between, we'll have other parties involved, such as the regulator who verify the validity of the data and the sustainability of the tuna catches.
We will be using Hyperledger Fabric's framework to keep track of each part of this process.
Now, as you read through the demonstrated scenario section, there are two main ideas to pay attention to:
1. There are many actors within the network, and you will see how these actors interact, and how a transaction is conducted.
2. Private channels allow Sarah and Miriam to privately agree on the terms of their interaction,
while still maintaining transparency, so other actors can corroborate and confirm their transaction.
Using private channels, regulators and restaurateurs can confirm whether a particular shipment of tuna was sustainably and legally sourced,
without needing to see the details of the entire journey.
Only the fisherman and the restaurateur are privy to such specific details.
Good luck and let's dive right on into it!

## Section 2 - Key Components and Transaction Flow

### Video 52 - Introduction to Hyperledger Fabric Architecture (Arianna Groetsema)

Hello, everybody!
We'll now be going over the architecture of Hyperledger Fabric.
Hyperledger Fabric is so unique, because it allows for modular consensus and membership service.
This means that algorithms for consensus, identity verification are plug-and-play,
resulting in a universal blockchain architecture, that can be applied to most industries or business models.
Channels are another unique feature.
They allow transactions to be private between two actors, while still being verified and committed to the blockchain.
You will also learn about the different roles within a network, how consensus is reached, and other special features.
By the end of this section, you will understand how a transaction is performed between two actors and what exactly occurs within a network during a transaction.
Good luck, and I'll see you in the next section!

### Video 53 - Ordering Service (Chris Ferris)

The ordering service is actually something that we conceived of as a function of the initial rollout of Fabric 0.6, last year,
in the sense that... we determined that, in order to improve the performance of the consensus computation,
that, if we separated out the ordering aspects of consensus, where typically, whether it's Bitcoin or Ethereum, the minors are determining the order of transactions in a block,
if we instead make that in an independent service, and apply the fault tolerance to the ordering service itself,
we can actually get a significant improvement in performance and throughput of the overall system.
And so, we've implemented, to date, two ordering services.
One is called SOLO - it's really a toy; I mean, it's intended to be used for development purposes, or initial testing of new functions, and so forth.
And then, another one is based on an implementation of Kafka.
And, over time, as we go forward, we plan on introducing various forms of fault tolerance too to that ordering service.
And so, the initial one is going to be based on RAFT consensus, which isn't byzantine fault tolerant, but it is crash fault tolerant,
and then, there is ongoing work on something we call Simplified Byzantine Fault Tolerance,
and that, we should have probably in the first half of 2018.

### Video 54 - 

