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

* Blockchain technology has some key differentiators from databases. 
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

### Lecture 24 - Hyperledger Blockchains: Permissioned or Permissionless?

* Hyperledger blockchains are generally permissioned blockchains, which means that the parties that join the network are authenticated and authorized to participate on the network. Hyperledger’s main goal is to create enterprise grade, open source, distributed ledger frameworks and code bases to support business use cases.
* If you look at permissionless blockchains, like the Bitcoin blockchain or the Ethereum blockchain, anyone can join the network, as well as write and read transactions. The actors in the system are not known, which means there could be some malicious actors within the network.
* Hyperledger reduces these security risks and ensures that only the parties that want to transact are the ones that are part of the transaction and, rather than displaying the record of the transactions to the whole network, they remain visible only to the parties involved. So, Hyperledger provides all the capabilities of the blockchain architecture - data privacy, information sharing, immutability, with a full stack of security protocols - all for the enterprise.

### Section 6 - Other Open Source Permissioned Distributed Ledgers

### Lecture 25 - [Chain Core](https://chain.com/)

* Chain Core is an enterprise permissioned blockchain system that is mostly focused on financial services, like currencies, securities, derivatives, gift cards, and loyalty points. The company partners with clients to launch and operate a network under the client's brand. Thanks to its strategic partnerships with companies such as Capital One, Citigroup, Fiserv, Nasdaq, Orange, Visa, etc., the company raised over $40 million in funding since 2014.
* Within the Chain Core network, the creation and transfer of assets is decentralized. However, as stated in the 2016 [Kudelski Security report](https://www.kudelskisecurity.com/sites/default/files/files/Kudelski_Security_Publication_Blockchain_EN.pdf),

*"the operation of the network is governed by a designated set of entities known as a federation".*

* The platform features the Chain Testnet, which allows decentralized application development on Chain Core, operated by Chain, Microsoft, and the Initiative for Cryptocurrencies and Contracts (IC3).

### Lecture 26 - Corda

* As of October 2018, R3 is a consortium of over two hundred large global financial institutions, that seeks to leverage distributed ledger technologies to record, manage, and automate legal agreements between businesses through its software solution, called Corda.

[Corda](https://www.corda.net/) is a distributed ledger platform, which features a blockchain-style P2P network; however, it is not a blockchain platform. Unlike blockchains, which involve global availability of data across the network and third party validators, Corda only allows information access and validation functions to parties actually involved in the transaction. Featuring a different software architecture, "Corda achieves consensus between firms at the level of individual deals, not the level of the system" (Richard Gendal Brown, 2016), while supporting a variety of consensus mechanisms.

### Lecture 27 - Quorum

* Created by JPMorgan, Quorum is, in fact, a fork of the Ethereum public blockchain, which uses a voting-based consensus algorithm to facilitate an enterprise-focused distributed ledger and smart contract platform. Data privacy is achieved within the network by allowing data visibility on a need-to-know basis. The platform is designed to support *"both transaction-level privacy and network-wide transparency"*. The network validates all smart contracts and overall system state through the involvement of all running nodes. As with other permissioned ledgers, regulatory compliance is front and center in the Quorum platform.

### Lecture 28 - IOTA

* The cryptocurrency IOTA has been around since 2015. According to Martin Rosulek, *"It is the first cryptocurrency that provides the whole ecosystem based on blockless blockchain"* to enable machine-to-machine (M2M) transactions.
* IOTA, however, is more than just a cryptocurrency. Essentially, the platform entails a generalization of the blockchain protocol (the technology called Tangle) that sits at the backend of the IOTA platform. 
* Instead of paying miners to validate the transactions, the architecture of the network involves peer-based validation. We can think of a simple analogy, that of a teacher grading students' homework: the students are the clients/users in the Bitcoin protocol, and the teacher is the miner/validator. Tangle technology asks students (users) to grade each other's homework, making the need for a teacher (external validator) redundant, and avoiding expenses related to the teacher's/validator's work. This allows the platform to be completely free of cost, without facing the scaling challenges that are inherent in the first generation of blockchains.
* Additionally, the use of the platform with connected devices or the Internet of Things

*"enables companies to explore new business-to-business models by making every technological resource a potential service to be traded on an open market in real time, with no fees".* - Roger Aitken, 2017

## Section 7 - Challenges in the Adoption/Deployment of Distributed Ledger Technologies  

* There are a number of challenges to the widespread use of permissioned distributed ledger technologies. Key among them are challenges around the lack of standards, regulatory challenges, and the lack of knowledge about distributed ledger technologies. These challenges are inherent to any new technological infrastructure that replaces an older infrastructure.

### Lecture 29 - Standards

* Since we are still witnessing the early days of blockchain technology, there is no agreement on standards in the developer and business community, as of yet. Standards are key in ensuring interoperability and avoiding risks associated with a fragmented ecosystem. Standards are critical not just for the distributed ledger itself, but also for supporting services, like identity, privacy, and data governance. Furthermore, the management of keys, as well as protocols and standards around key loss and theft, will be critical (Deshpande, Stewart, Lepetit, & Gunashekar, 2017).
* As a result, the International Organization for Standardization for Blockchain and Distributed Ledger Technologies was established in 2016 and has defined areas for future standardization work (Clare Naden, 2017). More about the ISO/TC 307 technical committee can be found at the ISO/TC 307 website.

### Lecture 30 - Regulation

* The lack of regulation around transactions on the blockchain creates an environment of uncertainty for all players. Highly regulated industries like financial services are treading carefully in the DLT space. The Securities and Exchange Commission of the United States has clarified its stance on Initial Coin Offerings (ICOs) in 2017. The Chinese government has, in fact, banned all ICOs, while 60 major ICO platforms are being investigated (Saheli Roy Choudhury, 2017).
* Similarly, there are no regulatory guidelines governing smart contracts, causing much anxiety among various players like lawyers, regulators, programmers, and businesses. The lack of regulatory guidelines, along with a lack of industry standards, exacerbates hindrances to rapid adoption of DLT.

### Lecture 31 - Lack of Know-How

* The lack of know-how (and know-whom and know-where) around distributed ledger technologies and the availability of experts in the area is a major challenge in the adoption of distributed ledger technologies. While there has been an exponential increase in the interest around 'blockchain', as indicated in the figure below, there is a huge lag of technical talent in the space. In fact, the origin of this course stems from the need to address this gap in know-how, both for the business and technical audiences.

# Chapter 2 - Introduction to Hyperledger

## Section 1 - Hyperledger

### Lecture 32 - [Hyperledger](https://www.hyperledger.org/)

* Hyperledger is a group of open source projects focused around cross-industry distributed ledger technologies. Hosted by The Linux Foundation, collaborators include industry leaders in technology, finance, banking, supply chain management, manufacturing, and IoT.
* As of October 2018, Hyperledger consists of ten projects, five of which are distributed ledger frameworks. The other five projects are tools that support these frameworks.
* As Arnaud Le Hors, member of the Hyperledger Technical Steering Committee, emphasized,

*"these projects show how broadly applicable blockchain technology really is. This goes way beyond cryptocurrencies".*

* Hyperledger provides an alternative to the cryptocurrency-based blockchain model, and focuses on developing blockchain frameworks and modules to support global enterprise solutions. The focus of Hyperledger is to provide a transparent and collaborative approach to blockchain development.

### Lecture 33 - Comparing Hyperledger with Bitcoin and Ethereum

* The following table explores the differences between Hyperledger's permissioned distributed ledgers and the Bitcoin and Ethereum permissionless blockchains. If you are considering blockchain solutions for your business requirements, it is important to pay attention to all these elements and weigh in on those that are most important for your use case.
	* Cryptocurrency-based: Bitcoin(V) Ethereum(V) Hyperledger(X)
	* Permissioned: Bitcoin(X) Ethereum(X) Hyperledger(V?)
	* Pseudo-anonymous: Bitcoin(V) Ethereum(x) Hyperledger(X)
	* Auditable: Bitcoin(V) Ethereum(V) Hyperledger(v)
	* Immutable ledger: Bitcoin(V) Ethereum(X) Hyperledger(X)
	* Modularity: Bitcoin(X) Ethereum(X) Hyperledger(v)
	* Smart contracts: Bitcoin(X) Ethereum(V) Hyperledger(V)
	* Consensus Protocol: Bitcoin(PoW) Ethereum(PoW) Hyperledger(Various)

* Sawtooth can be configured to be permissionless
* Key Hyperledger consensus protocols are Apache Kafka in Hyperledger Fabric, PoET in Hyperledger Sawtooth, RBFT in Hyperledger Indy, Tendermint in Hyperledger Burrow, and Yet Another Consensus (YAC) in Hyperledger Iroha. For more details, see the Hyperledger Architecture, Volume 1 paper.

### Lecture 34 - Hyperledger Goals

* Hyperledger has taken a leadership role to develop cross-industry standards and provide a neutral space for software collaboration. The financial services industry, in particular, is witnessing an unprecedented level of collaboration between institutions that have traditionally been competitors. The advent of a new foundational or infrastructural technology like the blockchain - much like the Internet - requires collaboration of various actors in order to realize the full benefits of the technology. Unless all actors use a certain standard, the pace of technological dissemination will continue to be slow. Technological adoption is characterized by network effects, where the costs decrease with the increase in use of a certain technology. Since shifting to distributed ledger technology involves significant costs, open source software, communities and ecosystems that develop around these have a significant part to play.

### Lecture 35 - Open Standards

*"Only an Open Source, collaborative software development approach can ensure the transparency, longevity, interoperability and support required to bring blockchain technologies forward to mainstream commercial adoption. That is what Hyperledger is about - communities of software developers building blockchain frameworks and platforms".* - hyperledger.org 

* As we learned in Chapter 1: "Discovering Blockchain Technologies", the non-availability of standards in distributed ledger technologies is one of the major hurdles in scaling them. One of Hyperledger's key goals is to facilitate the process of standards formation, not by promoting its own distributed ledger(s), but by providing a space for a variety of standards to co-exist simultaneously:

*"Rather than declaring a single blockchain standard, it encourages a collaborative approach to developing blockchain technologies via a community process, with intellectual property rights that encourage open development and the adoption of key standards over time".* - hyperledger-fabric.readthedocs.io 

* Hyperledger aims to adhere to "open standards", which means they are

*"(...) interoperable through open published interfaces and services".* - John Palfreyman, ibm.com

### Lecture 36 - Open Source and Open Governance

*"Today, most people understand the concept of Open Source. What many people don't get, and something we here at Hyperledger and The Linux Foundation pride ourselves on doing well, is Open Governance".* - hyperledger.org

* Open source software is software that is made freely available and may be redistributed and modified. In other words, anyone has the ability to view the code, use the code, copy the code, change the code, and, depending on the open source license, contribute back changes.
* Open governance means that technical decisions for an open source project are made by a group of community-elected developers drawn from a pool of active participants. These decisions include things such as which features to add, how, and when to add them.
* To learn more about the specifics of Hyperledger's open governance read the following article "ABCs of Open Governance".

### Lecture 37 - Blockchain for Business

* The cryptocurrency-based blockchain model, popularized by public blockchains like Bitcoin and Ethereum, currently falls short of fulfilling a host of requirements that many types of organizations would have to fulfill in order to be compliant when using blockchain and distributed ledger technologies - for instance, in the areas of financial services, healthcare, and government.
* Hyperledger is a unique platform that is developing permissioned distributed ledger frameworks specifically designed for enterprises, including those in industries with strong compliance requirements. Enterprise use cases require capabilities such as scalability and throughput, built-in or interoperable identity modules for the parties involved in a transaction or a network, or even access to regulators who can access all data in the ledger as read-only to ensure compliance. The latter is particularly important because, regardless of the innovation, it has to operate within the current regulatory framework, as well as comply with any new rules that come into place specifically targeted at blockchain technologies.
* The enterprise continues to be at the heart of this course.

## Section 2 - Hyperledger Frameworks

### Lecture 38 - Components of Hyperledger Frameworks

* Hyperledger business blockchain frameworks are used to build enterprise blockchains for a consortium of organizations. They are different than public ledgers like the Bitcoin blockchain and Ethereum. The Hyperledger frameworks include:
	* An append-only distributed ledger
	* A consensus algorithm for agreeing to changes in the ledger
	* Privacy of transactions through permissioned access
	* Smart contracts to process transaction requests.

### Lecture 39 - Hyperledger Iroha v0.95

* [Hyperledger Iroha](https://www.hyperledger.org/projects/iroha) is a blockchain framework contributed by Soramitsu, Hitachi, NTT Data, and Colu. Hyperledger Iroha is designed to be simple and easy to incorporate into infrastructure projects requiring distributed ledger technology. Hyperledger Iroha emphasizes mobile application development with client libraries for Android and iOS, making it distinct from other Hyperledger frameworks. Inspired by Hyperledger Fabric, Hyperledger Iroha seeks to complement Hyperledger Fabric and Hyperledger Sawtooth, while providing a development environment for C++ developers to contribute to Hyperledger.
* In conclusion, Hyperledger Iroha features a simple construction, modern, domain-driven C++ design, along with the consensus algorithm YAC.

### Lecture 40 - Hyperledger Sawtooth v1.0

* [Hyperledger Sawtooth](https://www.hyperledger.org/projects/sawtooth), contributed by Intel, is a blockchain framework that utilizes a modular platform for building, deploying, and running distributed ledgers. Distributed ledger solutions built with Hyperledger Sawtooth can utilize various consensus algorithms based on the size of the network. It includes the Proof of Elapsed Time (PoET) consensus algorithm, which provides the scalability of the Bitcoin blockchain without the high energy consumption. PoET allows for a highly scalable network of validator nodes. Hyperledger Sawtooth is designed for versatility, with support for both permissioned and permissionless deployments.

### Lecture 41 - Hyperledger Fabric v1.0

* [Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) was the first proposal for a codebase, combining previous work done by Digital Asset Holdings, Blockstream's libconsensus, and IBM's OpenBlockchain. Hyperledger Fabric provides a modular architecture, which allows components such as consensus and membership services to be plug-and-play. Hyperledger Fabric is revolutionary in allowing entities to conduct confidential transactions without passing information through a central authority. This is accomplished through different channels that run within the network, as well as the division of labor that characterizes the different nodes within the network. Lastly, it is important to remember that, unlike Bitcoin, which is a public chain, Hyperledger Fabric supports permissioned deployments.

*"If you have a large blockchain network and you want to share data with only certain parties, you can create a private channel with just those participants. It is the most distinctive thing about Fabric right now"* - Brian Behlendorf, Executive Director of Hyperledger, The Linux Foundation

### Lecture 42 - Hyperledger Indy

* [Hyperledger Indy](https://www.hyperledger.org/projects/hyperledger-indy) is a distributed ledger purpose-built for decentralized identity. Hyperledger Indy's goal is to achieve this by developing a set of

*"(...) decentralized identity specs and artifacts that are independent of any particular ledger and will enable interoperability across any DLT that supports them".*

* Contributed by the Sovrin Foundation, Hyperledger Indy allows individuals to manage and control their digital identities. Rather than having businesses store huge amounts of personal data of individuals, Hyperledger Indy allows businesses to store pointers to identity. Once the company verifies the other party's identity, it throws it away.
* According to Brian Behlendorf,

* "(...) identity is a toxic asset that could present a liability to organizations".*

* Indeed, since 2013, over 9 billion data records were lost or stolen. What is striking is that, out of these, only 4% were encrypted, and hence, rendered useless after being stolen (also called "secure breaches"). You can find detailed statistics at the Breach Level Index website.
* One of the key principles of Hyperledger Indy is its "privacy by design" approach. Given the immutable nature of the DLT, it is all the more important that digital identities be handled with the utmost care, keeping human values front and center.

*"Hyperledger Indy lets users authenticate identity based on the attributes they are willing to store and share themselves. This can reduce the amount of liability contained within a business because the data can be kept with the user and presented to you again in a way that you can trust and validate that what has been said really was said and is trusted by the other parties you do business with".* - Nathan George, Maintainer, Hyperledger Indy

* Further information about the history of the project can be found at the [Sovrin's website](https://sovrin.org/).

### Lecture 43 - Hyperledger Burrow v0.16.1

* Formally known as eris-db, [Hyperledger Burrow](https://www.hyperledger.org/projects/hyperledger-burrow) was released in December 2014. Currently under incubation, Hyperledger Burrow is a permissionable smart contract machine that provides a modular blockchain client with a permissioned smart contract interpreter built- in part to the specification of the Ethereum Virtual Machine (EVM). It is the only available Apache-licensed EVM implementation.
* Following are the major components of Burrow:
	* The Gateway provides interfaces for systems integration and user interfaces
	* The Smart contract application engine facilitates integration of complex business logic (maintaining the networking stack between the nodes and ordering transactions)
	* The Application Blockchain Interface (ABCI) provides interface specification for the consensus engine and smart contract application engine to connect.

## Section 3 - Hyperledger Tools

* The Hyperledger frameworks which we examined in the previous section are used to build blockchains and distributed ledgers. The Hyperledger tools, which we will look at next, are auxiliary softwares used for things like deploying and maintaining blockchains, examining the data on the ledgers, as well as tools to design, prototype, and extend blockchain networks.

### Lecture 44 - Hyperledger Cello

* For businesses that want to deploy Blockchain-as-a-Service, [Hyperledger Cello](https://www.hyperledger.org/projects/cello) provides a toolkit that fulfills this need. Particularly for lean businesses and small enterprises, who want to reduce or eliminate the effort required in creating, managing, and terminating blockchains, Hyperledger Cello allows blockchains deployment to the cloud. Operators can create and manage such blockchains through a dashboard, and users (typically, chaincode developers) can obtain a blockchain instance immediately.

As a Hyperledger module, "Cello aims to bring the on-demand 'as-a-service' deployment model to the blockchain ecosystem", thus helping in furthering the development and deployment of Hyperledger's frameworks. Hyperledger Cello was initially contributed by IBM, with sponsors from Soramitsu, Huawei, and Intel.

Application developers and system administrators using Cello can provision and maintain Hyperledger networks. For instance, you can create a group of distributed ledger networks in virtual clouds known as 'container clusters', and then, manage and monitor those networks with a configurable dashboard. Additionally, you can build a Blockchain-as-a-Service (BaaS) platform.

### Lecture 45 - Hyperledger Explorer

* [Hyperledger Explorer](https://www.hyperledger.org/projects/explorer) is a tool for visualizing blockchain operations. It is the first ever blockchain explorer for permissioned ledgers, allowing anyone to explore the distributed ledger projects being created by Hyperledger's members from the inside, without compromising their privacy. The project was contributed by DTCC, Intel, and IBM.

Designed to create a user-friendly web application, Hyperledger Explorer can view, invoke, deploy, or query:

Blocks
Transactions and associated data
Network information (name, status, list of nodes)
Smart contracts (chain codes and transaction families)
Other relevant information stored in the ledger.
The ability to visualize data is of critical importance, in order to extract business value from it. Hyperledger Explorer provides this much needed functionality. Key components include a web server, a web UI, web sockets, a database, a security repository, and a blockchain implementation.

### Lecture 46 - Hyperledger Composer

* [Hyperledger Composer](https://www.hyperledger.org/projects/composer) provides a suite of tools for building blockchain business networks. These tools allow you to:
	* Model your business blockchain network
	* Generate REST APIs for interacting with your blockchain network
	* Generate a skeleton Angular application.
* Built in Javascript, Hyperledger Composer provides an easy-to-use set of components that developers can quickly learn and implement. The project was contributed by Oxchains and IBM.
* Hyperledger Composer has created a modelling language that allows you to define the assets, participants, and transactions that make up your business network using business vocabulary. In addition, the transaction logic is then written by developers using Javascript. This simple interface allows business people and technologists to work together on defining their business network.
* The benefits of Hyperledger Composer are:
	* Faster creation of blockchain applications, eliminating the massive effort required to build blockchain applications from scratch
	* Reduced risk with well-tested, efficient design that aligns understanding across business and technical analysts
	* Greater flexibility as the higher-level abstractions make it far simpler to iterate.
* To get an overview of Hyperledger Composer watch "Introduction to Hyperledger Composer" and take a look at Chapter 6

### Lecture 47 - Hyperledger Caliper

* [Hyperledger Caliper](https://www.hyperledger.org/projects/caliper) is a blockchain benchmark tool that allows users to measure the performance of a specific blockchain implementation with a set of predefined use cases. Hyperledger Caliper will produce reports containing a number of performance indicators (e.g., transactions per second, transaction latency, resource utilization, etc.). These reports can be used in deciding what blockchain implementation is suitable for a user's specific needs, as well as by other Hyperledger projects as they build out their framework. 
* Hyperledger Caliper was initially contributed by developers from Huawei, Hyperchain, Oracle, Bitwise, Soramitsu, IBM and the Budapest University of Technology and Economics.

### Lecture 48 - Hyperledger Quilt

* [Hyperledger Quilt](https://www.hyperledger.org/projects/quilt) is a business blockchain tool that offers interoperability between ledger systems by implementing the Interledger protocol (which is primarily a payments protocol designed to transfer value across distributed ledgers and non-distributed ledgers). 
* Hyperledger Quilt was initially contributed by NTT Data and Ripple.
