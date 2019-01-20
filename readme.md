# edX Course: Linux Foundation LFS171x Course "Blockchain for Business - An Introduction to Hyperledger Technologies"
* [Course Link](https://www.edx.org/course/blockchain-for-business-an-introduction-to-hyperledger-technologies)
* [Course Repo]()

# Chapter 1 - Discovering BlockChain Technologies

## Section 1 - Distributed Ledger Technology (DLT)

### Lecture 1 - Background - The Rising Interest in Distributed Ledger Technologies

* Looking back to the last half century of computer technologies and architectures, one may observe a trend of fluctuation between the centralization and subsequent decentralization of computing power, storage, infrastructure, protocols, and code.
* Mainframe computers are largely centralized. They typically house all computing power, memory, data storage, and code. Access to mainframes is mainly by "dumb terminals", which only take inputs and outputs, and do not store or process data.
* With the advent of personal computers and private networks, similar computational capabilities were now housed both on the clients, as well as the servers. This, in part, gave rise to the "client-server" architecture, which supported the development of relational database systems. Massive data sets, which are housed on mainframes, could move onto a distributed architecture. This data could replicate from server to server, and subsets of the data could be accessed and processed on clients, and then, synced back to the server.
* Over time, Internet and cloud computing architectures enabled global access from a variety of computing devices; whereas mainframes were largely designed to address the needs of large corporations and governments. Even though this "cloud architecture" is decentralized in terms of hardware, it has given rise to application-level centralization (e.g. Facebook, Twitter, Google, etc.).
* Currently, we are witnessing the transition from centralized computing, storage, and processing to decentralized architectures and systems. According to Muneeb Ali, these systems aim to

*"give explicit control of digital assets to end-users and remove the need to trust any third-party servers and infrastructure".*

* Distributed ledger technology is one of the key innovations making this shift possible.

### Lecture 2 - Distributed Ledger Technology (DLT)

* A distributed ledger is a type of data structure which resides across multiple computer devices, generally spread across locations or regions.
* Distributed ledger technology (DLT) includes blockchain technologies and smart contracts. While distributed ledgers existed prior to Bitcoin, the Bitcoin blockchain marks the convergence of a host of technologies, including timestamping of transactions, Peer-to-Peer (P2P) networks, cryptography, and shared computational power, along with a new consensus algorithm. 
* In summary, distributed ledger technology generally consists of three basic components:
	* A data model that captures the current state of the ledger
	* A language of transactions that changes the ledger state
	* A protocol used to build consensus among participants around which transactions will be accepted, and in what order, by the ledger.

### Lecture 3 - Blockchains

* According to hyperledger.org,

*"A blockchain is a peer-to-peer distributed ledger forged by consensus, combined with a system for "smart contracts" and other assistive technologies".*

* Smart contracts are simply computer programs that execute predefined actions when certain conditions within the system are met.
* Consensus refers to a system of ensuring that parties agree to a certain state of the system as the true state.
* Blockchain is a specific form or subset of distributed ledger technologies (DLTs), which constructs a chronological chain of blocks, hence the name "block-chain". Examples of other DLTs are Chain Core, Corda, Quorum, and IOTA. They will be covered later in this chapter.
* A block refers to a set of transactions that are bundled together and added to the chain at the same time.
* Timestamping is another key feature of blockchain technology. Each block is timestamped, with each new block referring to the previous block. Combined with cryptographic hashes, this timestamped chain of blocks provides an immutable record of all transactions in the network, from the very first (or genesis) block.
* In the Bitcoin blockchain, the miner nodes bundle unconfirmed and valid transactions into a block. Each block contains a given number of transactions. In the Bitcoin network, miners must solve a cryptographic challenge to propose the next block. This process is known as "proof of work", and requires significant computing power. We shall discuss proof of work in more detail in the Consensus Algorithms section. For more information about blockchain technology, please read the following article: "A Brief History of Blockchain" by Vinay Gupta.
* A Bitcoin block consists of four pieces of metadata:
	* The reference to the previous block
	* The proof of work, also known as a nonce
	* The timestamp
	* The Merkle tree root for the transactions included in this block (Merkle tree is explained next).

### Lecture 4 - Merkle Tree

* The Merkle tree, also known as a binary hash tree, is a data structure that is used to store hashes of the individual data in large datasets in a way to make the verification of the dataset efficient. It is an anti-tamper mechanism to ensure that the large dataset has not been changed. The word "tree" is used to refer to a branching data structure in computer science, as seen in the image below. According to Andreas M. Antonopoulos, in the Bitcoin protocol,

*"Merkle trees are used to summarize all the transactions in a block, producing an overall digital fingerprint of the entire set of transactions, providing a very efficient process to verify whether a transaction is included in a block".*

### Lecture 5 - Transactions

* The record of an event, cryptographically secured with a digital signature, that is verified, ordered, and bundled together into blocks, form the transactions in the blockchain. In the Bitcoin blockchain, transactions involve the transfer of bitcoins, while in other blockchains, transactions may involve the transfer of any asset or a record of some service being rendered. Furthermore, a smart contract within the blockchain may allow automatic execution of transactions upon meeting predefined criteria.
* Cryptography has a key role to play both in the security, as well as in the immutability of the transactions recorded on blockchains. Cryptography is the study of the techniques used to allow secure communication between different parties and to ensure the authenticity and immutability of the data being communicated. For blockchain technologies, cryptography is used to prove that a transaction was created by the right person. It is also used to link transactions into a block in a tamper-proof way, as well as create the links between blocks, to form a blockchain.

### Lecture 6 - Differences Between Blockchains and Databases

*Blockchain technology has some key differentiators from databases. 
* A blockchain is a write-only data structure, where new entries get appended onto the end of the ledger. Every new block gets appended to the block chain by linking to the previous block's "hash" (you can check the Glossary tab for a refresher on hash functions). There are no administrator permissions within a blockchain that allow editing or deleting of data.
* In a relational database, data can be easily modified or deleted. Typically, there are database administrators who may make changes to any part of the data and/or its structure. Additionally, blockchains were designed for decentralized applications, whereas relational databases, in general, were originally designed for centralized applications, where a single entity controls the data.

### Lecture 7 - Types of Blockchains

* A blockchain can be both permissionless (like Bitcoin or Ethereum) or permissioned (like the different Hyperledger blockchain frameworks). A permissionless blockchain is also known as a public blockchain, because anyone can join the network. A permissioned blockchain, or private blockchain, requires pre-verification of the participating parties within the network, and these parties are usually known to each other.
* The choice between permissionless versus permissioned blockchains should be driven by the particular application at hand (or use case). Most enterprise use cases involve extensive vetting before parties agree to do business with each other. An example where a number of businesses exchange information is the supply chain management. The supply chain management is an ideal use case for permissioned blockchains. You would not want non-vetted companies participating in the network. Each participant that is involved in the supply chain would require permissions to execute transactions on the blockchain. These transactions would allow other companies to understand where in the supply chain a particular item is. 
* On the contrary, when a network can "commoditize" trust, facilitating parties to transact without necessarily having to verify each other's identity, like the Bitcoin blockchain, a permissionless blockchain is more suitable. Many of these instances involve the sale or distribution to the public. Cryptocurrencies and Initial Coin Offerings (which are not backed by national governments) usually involve implementations of permissionless blockchains.
* You will learn about a variety of use cases in Chapter 3, "The Promise of Business Blockchain Technologies".

### Lecture 8 - Peer-to-Peer Network Architecture

* Historically, most applications utilize a central server (or servers). For one user/client to send a message to another user/client in the network, the request has to be sent to the hub or a central server, which then directs it to the right computer.
* Peer-to-peer (P2P) networks were first made popular by Napster (and later BitTorrent) and consist of computer systems which are directly connected to each other via the Internet, without a central server. Peers contribute to the computing power and storage that is required for the upkeep of the network. P2P networks are generally considered to be more secure than centralized networks, as they do not have a single point of attack, as in the case of a server-based network, where the security of the entire network can be compromised if the central server is successfully attacked. As a result, large corporations invest significant amounts of financial resources to fortify their central servers, and yet, a total cost of $445 billion to the global economy in cyberspace crimes was estimated by the World Economic Forum's "2016 Global Risk Report".
* Permissionless P2P systems do not require a set amount of peers to be online and are generally slower. Permissioned P2P networks have to guarantee uptime and require a high level of quality of service on the communication links.

### Lecture 9 - Immutability of Data

* The immutability of the data which sits on the blockchain is perhaps the most powerful and convincing reason to deploy blockchain-based solutions for a variety of socio-economic processes which are currently recorded on centralized servers. This immutability, or "unchanging over time" feature makes the blockchain useful for accounting, financial transactions, identity management, and asset ownership, management and transfer, just to name a few examples. Once a transaction is written onto the blockchain, no one can change it, or, at least, it would be extremely difficult to change it.
* According to Antony Lewis, the Director of Research at R3,

*"When people say that blockchains are immutable, they don't mean that the data can't be changed, they mean it is extremely hard to change without collusion, and if you try, it's extremely easy to detect the attempt".*

* Let's dig into this statement a bit further. It is extremely hard to change the transactions in a blockchain, because each block is linked to the previous block by including the previous block's hash. This hash includes the Merkle root hash of all the transactions in the previous block. If a single transaction were to change, not only would the Merkle root hash change, but so too would the hash contained in the changed block. In addition, each subsequent block would need to be updated to reflect this change. In the case of proof of work, the amount of energy required to recalculate the nonce for this block and each subsequent block would be prohibitive. On the other hand, if someone did modify a transaction in a block without going through the necessary steps to update the subsequent blocks, it would be easy to recalculate the hashes used in the blocks and determine that something is amiss.
* Let's look at an example of how this works. In the following diagram, we see the original blocks and the transactions for Block 11. Specifically, we see that the Merkle root for the transactions in Block 11 is Hash #ABCD, which is the combined hash for the four transactions in this block. Now, let's say that someone comes in and attempts to change Transaction A to Transaction A'. This, in turn, modifies the hashes that are stored in the Merkle tree, and the Merkle root changes to Hash #A'BCD. In addition, the Previous Block hash stored in Block 12 also needs to be modified to reflect the overall change in the hash for Block 11.

### Lecture 10 - Blockchain Applications

* Since blockchain is a new form of digital infrastructure, applications built on top of a blockchain provide a gateway to accessing information that sits on that blockchain. In other words, clients/users interact with the blockchain through applications. Starting from the simple wallets that hold bitcoins, sophisticated applications which encompass applications addressing digital identity (e.g. UPort, KYC-Chain, Netki, etc.), and complex financial transactions are being built on the blockchain.
* A more exhaustive list of companies using blockchain technology for identity management and authentication can be found in the following article: "[21 Companies Leveraging Blockchain for Identity Management and Authentication](https://gomedici.com/22-companies-leveraging-blockchain-for-identity-management-and-authentication/)" by Elena Mesropyan.
* For more details about blockchain applications, you can refer to Daniel Palmer's article entitled "[7 Cool Decentralized Apps Being Built on Ethereum](https://www.coindesk.com/7-cool-decentralized-apps-built-ethereum)".

### Lecture 11 - Smart Contracts

* Smart contracts are simply computer programs that execute predefined actions when certain conditions within the system are met. Smart contracts provide the language of transactions that allow the ledger state to be modified. They can facilitate the exchange and transfer of anything of value (e.g. shares, money, content, property).

### Section 2 - Bitcoin and Ethereum Blockchains

### Lecture 12 - Bitcoin - A Popular Blockchain Deployment

* With the invention of the peer-to-peer (P2P) cash system known as Bitcoin in 2008, we have an example of a global decentralized payment network with a distributed and publicly-owned infrastructure, operating as a "permissionless" system. There is a persuasive case that Bitcoin is the first "killer application" of decentralized computing. One can send and receive bitcoins anywhere in the world in a completely P2P manner, without having to intermediate through a trusted third party, such as a bank.
* According to the Coin Market Capitalizations website, as of October 2018, bitcoin's market capitalization (market cap) was over $112 billion. 
* According to AngelList, nearly three thousand startups have been created to leverage Bitcoin and blockchain-related technologies since the inception of the Bitcoin payment system. Hundreds of large companies, and dozens of governments and universities have become actively involved in researching, testing, and prototyping blockchain protocols, platforms, and applications. In particular, the financial services sector has been actively investing in exploring wider applications of distributed ledger technologies (of which, blockchain is a subset) since late 2015.

### Lecture 13 - Bitcoin and Cryptoeconomics

* Bitcoin has also ushered in tremendous academic and research interest in the area of Cryptoeconomics and Cryptoeconomic security.
* According to Vitalik Buterin,

*"Cryptoeconomics is about building systems that have certain desired properties using cryptography to prove properties about messages that happened in the past while using economic incentives defined inside the system to encourage desired properties to hold into the future".*

* In other words, the field of Cryptoeconomics explores the intersection of cryptography and economic incentives. While cryptography is used for ensuring network security at various levels and functions, the built-in economic incentives provided to the participating nodes in the network ensures that, at any given point, the majority of players in the network operate in a desirable way.
* Rather than imposing barriers to entry, permissionless blockchains are public and open for anyone to join. Since such networks can reasonably expect all kind of agents - including malicious actors - the key lies in incentivizing good behavior in a critical majority of the network, such that:
	* The malicious actors cannot take over the network through an escalated attack.
	* The malicious actors cannot collude to undertake an organized majority attack on the network.
	* The payoffs of securing the network are consistently higher than the cost of attacking the network.
	* The cost of attacking the network is prohibitively high.
* You can find more about Cryptoeceonomics read "The Blockchain Economy: A Beginner’s Guide to Institutional Cryptoeconomics".

### Lecture 14 - Ethereum - An Alternative to Bitcoin

* According to Ethereum's official documentation,

*"Ethereum is an open blockchain platform that lets anyone build and use decentralized applications that run on blockchain technology".*

* The Ethereum blockchain platform facilitates scripting functionality, or "smart contracts", which are run through the nodes in the network. As a result, unlike the Bitcoin blockchain, it does not just track transactions, it also programs them. Technically, Ethereum is a Turing-complete virtual machine with its native cryptocurrency called "ether". The platform was proposed in 2013 in a white paper by the then 19-year old Vitalik Buterin.
* As of October 2018, Ethereum had a market cap of over $21 billion, making Ether the second most valuable cryptocurrency after Bitcoin.

### Lecture 15 - Dapps

* As Stephan Tual explains, Ethereum applications do not have a middleman; instead, users interact in a P2P fashion with other users through a variety of interfaces - social, financial, gaming, etc. Since the applications are developed on the decentralized consensus-based network itself, third-party censorship is virtually impossible. Malicious actors cannot secretly tamper with the application by changing the code and compromise all application users (or nodes that are actively interacting with it). These Decentralized Applications have come to be known as Dapps.
* Since they are cryptographically secured, Dapps are referred to as "secure applications". Some of the high profile Dapps built on the Ethereum platform include:
	* Augur, which is a Decentralized Prediction Market
	* Digix, which tokenizes gold on Ethereum
	* Maker, which is a Decentralized Autonomous Organization (DAO).
* The Ethereum network is a distributed global public network, which means it is not run on central servers in a certain geographical location. Instead, the computing power that runs the network is contributed by nodes that are spread across the globe. In other words, Dapps have "zero downtime" - they never go down and, in general, cannot be switched off.

### Lecture 16 - Ethereum Smart Contracts

* A hypothetical example of an Ethereum-based smart contract may involve the following transaction: in an equity raise, transfer amount X from the investor to the company upon receiving the given shares from the company. The monetary amount X, which was pre-validated by the company for the transaction (much like in a credit card purchase), is held in escrow by the smart contract, until the shares have been received by the investor. Any kind of arbitrary sophisticated business logic can be committed to the blockchain. The Ethereum blockchain only encodes these "rules of the games". The actual payoffs occur by interacting with the blockchain.
* The illustration below describes this process. The smart contract encodes the agreement between the company raising funds and its investors (Panel 1). The smart contract sits on the Ethereum public blockchain, and is run on the Ethereum Virtual Machine (EVM). Once hitting a triggering event, like an expiration date or a strike price that has been pre-coded, the smart contract automatically executes as per the business logic (Panel 2). As an added benefit, regulators are able to scrutinize the market activity on an ongoing basis, without compromising the identity of specific players in a permissionless public blockchain, as Ethereum (Panel 3).
* Note: With the advent of the Ethereum blockchain platform and the scripting functionality or smart contracts that it enables, there are ongoing attempts to do the same for the Bitcoin blockchain, which does not allow for this, due to security reasons. RSK is one such smart contract platform that seeks to achieve this "with a 2-way peg to Bitcoin". The added functionality can go a long way in making the Bitcoin blockchain useful for use cases other than cash transfers.

## Section 3 - Exploring Permissionless Blockchains

* Let's start by examining the Bitcoin and Ethereum blockchains, both of which are permissionless, public blockchains. We will examine several large transactions, and the genesis block for each blockchain. We will look at block heights, transaction times, mining pools, timestamps, and block rewards.

### Lecture 17 - "Certifying" a Document

* We have just examined the Bitcoin and Ethereum blockchains, and the key variables to pay attention to. Next, let's examine how we can "certify" a document on both the Bitcoin and Ethereum blockchains simultaneously, using Stamp.io, which is a certification tool. We will show you how to easily certify various types of files on Stamp.io, obtaining a "Stampery Certificate". We will also show you how to cross-check the hash of the transactions on the Bitcoin and the Ethereum blockchains. 
* Course of actions:
	* signup to stamp.io
	* drag-grop a file
	* get certificate (filename + timestamp + id + hash)
	* Get proof fgrom ethereum and bitcoin (the ahsh was added in the blockchain)

## Section 4 - Consensus Algorithms

* Consensus in the network refers to the process of achieving agreement among the network participants as to the correct state of data on the system. Consensus leads to all nodes sharing the exact same data. A consensus algorithm, hence, does two things: it ensures that the data on the ledger is the same for all the nodes in the network, and, in turn, prevents malicious actors from manipulating the data. The consensus algorithm varies with different blockchain implementations.
* While the Bitcoin blockchain uses Proof of Work as the consensus algorithm, other blockchains and distributed ledgers are deploying a variety of consensus algorithms, like the Proof of Stake, Proof of Burn, Proof of Capacity, Proof of Elapsed Time, and many others, depending on their unique requirements.
* Next, we will briefly explain some of these algorithms.

### Lecture 18 - Proof of Work (PoW)

* The Proof of Work consensus algorithm involves solving a computational challenging puzzle in order to create new blocks in the Bitcoin blockchain. Colloquially, the process is known as 'mining', and the nodes in the network that engage in mining are known as "miners". The incentive for mining transactions lies in economic payoffs, where competing miners are rewarded with 12.5 bitcoins and a small transaction fee.
* As described in the 2016 Kudelski Security report,

*"Proof-of-work (PoW) is the outcome of a successful mining process and, although the proof is hard to create, [it] is easy to verify".*

* For better understanding, please consider the following example provided by Ofir Beigel:

*"(...) guessing a combination to a lock is a proof to a challenge. It is very hard to produce this since you will need to guess many different combinations; but once produced, it is easy to validate. Just enter the combination and see if the lock opens".*

* Multiple criticisms exist for the PoW consensus algorithm. PoW requires a huge amount of energy to be expended, given the computationally heavy algorithm. In addition, PoW has a high latency of transaction validation, and the concentration of mining power is located in countries where electricity is cheap. In terms of the network security, PoW is susceptible to the "51% attack", which refers to an attack on a blockchain by a group of miners controlling more than 50% of the network's computing power.

### Lecture 19 - Proof of Stake (PoS)

* The Proof of Stake algorithm is a generalization of the Proof of Work algorithm. In PoS, the nodes are known as the "validators" and, rather than mining the blockchain, they validate the transactions to earn a transaction fee. There is no mining to be done, as all coins exist from day one. Simply put, nodes are randomly selected to validate blocks, and the probability of this random selection depends on the amount of stake held. So, if node X owns 2 coins and node Y owns 1 coin, node X is twice as likely to be called upon to validate a block of transactions. The specific implementation of PoS can vary, depending on the use case, or as a matter of software design. Instances include Proof of Deposit and Proof of Burn. The PoS algorithm saves expensive computational resources that are spent in mining under a PoW consensus regime.

### Lecture 20 - Proof of Elapsed Time (PoET)

* Developed by Intel, the Proof of Elapsed Time consensus algorithm emulates the Bitcoin-style Proof of Work. Hyperledger's Sawtooth implementation is an example of PoET at work. Instead of competing to solve the cryptographic challenge and mine the next block, as in the Bitcoin blockchain, the PoET consensus algorithm is a hybrid of a random lottery and first-come-first-serve basis. In PoET, each validator is given a random wait time.

*"The validator with the shortest wait time for a particular transaction block is elected the leader".* - sawtooth.hyperledger.org

* This "leader" gets to create the next block on the chain.

### Lecture 21 - Simplified Byzantine Fault Tolerance (SBFT)

* The Simplified Byzantine Fault Tolerant consensus algorithm implements an adopted version of the Practical Byzantine Fault Tolerant (PBFT) algorithm, and seeks to provide significant improvements over Bitcoin's Proof of Work consensus protocol. The basic idea involves a single validator who bundles proposed transactions and forms a new block. Note that, unlike the Bitcoin blockchain, the validator is a known party, given the permissioned nature of the ledger. Consensus is achieved as a result of a minimum number of other nodes in the network ratifying the new block. In order to be tolerant of a Byzantine fault, the number of nodes that must reach consensus is 2f+1 in a system containing 3f+1 nodes, where f is the number of faults in the system. For example, if we have 7 nodes in the system, then 5 of those nodes must agree if 2 of the nodes are acting in a faulty manner.
* The practical example would be that of ByzCoin, which seeks to make key improvements over the original Bitcoin protocol. Addressing the challenge around scalability due to high latency, ByzCoin transactions are irreversibly committed to the blockchain within seconds. The added advantage is the communication trees to "(...) optimize transaction commitments and verification under normal operations" ([2016 Kudelski Security report](https://www.kudelskisecurity.com/sites/default/files/files/Kudelski_Security_Publication_Blockchain_EN.pdf)).

### Lecture 22 - Proof of Authority (PoA)

* roof-of-Authority (PoA) is a consensus algorithm which can be used for permissioned ledgers. It uses a set of "authorities", which are designated nodes that are allowed to create new blocks and secure the ledger. Ledgers using PoA require sign-off by a majority of authorities in order for a block to be created.

### Lecture 23 - Comparing Permissioned Consensus Approaches and Standard PoW

* Consensus can be implemented in different ways, such as through the use of lottery-based algorithms (PoET or PoW), or through the use of voting-based methods (SBFT), each targeting different network requirements and fault tolerance models.
* Lottery-based algorithms are advantageous in that they can scale to a large number of nodes. Voting-based algorithms provide low-latency finality.
* The following table offers an at-a-glance view of the main considerations and pros and cons of different business blockchain approaches to reaching consensus.
* Permissioned Lottery-Based: Speed (GOOD) Sacalability (GOOD) Finality (MODERATE)
* Permissioned Voting based: Speed (GOOD) Scalability (MODERATE) Finality (GOOD)
* Standard Proof of Work (Bitcoin): Speed (POOR) Scalability (GOOD) Finality (POOR) 

## Section 5 - Hyperledger

* Hyperledger is an open source effort created to advance cross-industry blockchain technologies. Hosted by The Linux Foundation, it is a global collaboration of members from various industries and organizations. Hyperledger boasts a host of enterprise-ready solutions. Hyperledger is about communities of software developers building blockchain frameworks and platforms. We will take a closer look at some of the current Hyperledger projects in the coming chapters.

