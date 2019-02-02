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

# Chapter 3 - The Promise of Business Blockchain Technologies

## Section 1 - Existing Blockchain Use Cases

### Lecture 49 - Business Blockchain Technologies Overview

* Blockchain is a new data structure with an automated way to enforce trust among participants. Consensus algorithms ensure that all participants agree on the data stored within the blockchain. Blockchain opens the door to disrupt any industry that relies on a central authority to confirm authenticity. It also allows independent, and even competing organizations, to share information to gain efficiencies across an industry.
* In permissioned blockchains, a consortium of organizations are responsible for authenticating and controlling the participants in a blockchain. In public blockchains, no central authority or administration is required to exchange data. Blockchains can drive business innovation through controlled data-sharing networks for industry consortiums.
* The promise of distributed ledger technologies (DLT) to simplify and automate key work functions has many industries taking notice. Businesses recognize the efficiency gains from transitioning from closed and proprietary solutions to standard open source capabilities, such as Hyperledger business blockchain technologies. Several common project features of blockchain applications are taking shape as the technology matures.
* How exactly are businesses using these emerging technologies today? Next, we will explore the state of distributed ledger technologies in actual corporate settings, and how they compare against traditional tools. 

### Lecture 50 - Supply Chain Management

* Supply chain management is an important piece of enterprise resource planning (ERP). Supply chain management is the oversight of funds, raw materials, components, and finished products, as they move from suppliers, to manufacturers, to wholesalers, to retailers, to consumers. This movement can occur both within one company, or among several companies. As assumptions change over time, the supply chain models can begin to show weak performance metrics. Good supply chain management will keep product quality consistent, and also prevent either understocking or overstocking of inventory.
* Stocking the right amount of inventory over time is also known as supply demand synchronization, and is the key component in just-in-time lean manufacturing and distribution. Companies want to ensure that products are available when needed, but overstocking inventory is costly. Companies that overstock perishable goods must discard items. Companies that overstock non-perishable goods cannot use the money paid for those goods for other purposes until the inventory is used. Furthermore, if the price of a good drops while a company is storing excess inventory, then the company will lose money.
* Currently, there are weak points in the supply chain management. These weak points occur where there are multiple ERP systems in use across organizations. Data doesn't flow well through the handshakes or interface points between systems. These weak points usually happen during transference of ownership, or change in status between two parties. Visibility is limited at the hand-off points of funds, raw materials, components, or finished products. This lack of transparency is often intentional, as companies don't want to expose their competitive advantages (e.g., an inexpensive supplier who delivers quality products on time). Additionally, a company could be cut out of a supply chain if members start transacting directly with that company’s suppliers.
* Blockchains are currently being used to solve problems in supply chain management by eliminating the need for a trusted third party to certify raw materials, components, or finished products, as they travel through a supply chain. Every participant, or node, contains a copy of all transactions. This provides an audit trail of every transaction that has occurred in the system. A change would be validated or rejected by the nodes in the system. Because all participants have a copy of all past transactions in the network, any participant can detect if a product is not as advertised. Instead of examining raw materials, components, or finished products at several points in the supply chain, a record of the inspection would be available and bound to the item as it flows through the supply chain. Although a record of the transaction is public and tied to the movement of physical items across the network, specifics such as the quantity of goods, or the identity of the parties transacting, can be done pseudo-anonymously in a blockchain. Such a granular view of movement through supply chains improves resource allocation.
* The trade finance industry can also leverage information visible in a supply chain blockchain. In its broadest sense, trade finance manages capital required for international trade. Trade financing has become the norm for cross border transactions, with the World Trade Organization estimating that "up to 80 percent of global trade is supported by some sort of financing or credit insurance" (2016). An exporter needs to to mitigate the risk of non-payment, while an importer wants to mitigate the supply risk. The function of trade finance is to act as a third party to remove the payment risk and the supply risk, whilst providing the exporter with accelerated receivables, and the importer with extended credit. Institutions that provide capital during these trades can leverage the information visible in a supply chain blockchain to better evaluate companies for lending.

### Lecture 51 - Provenance

* As the previous section on blockchains for supply chain management illustrated, blockchain data improves insight into products, as they move through their lifecycle. Large enterprises are not the only parties to benefit from this increased visibility. Consumers can also benefit from blockchain technology.
* Provenance is a record of ownership used as a guide to authenticity or quality. Because of the overhead involved in traditional provenance records, they were only available for very large ticket items, such as works of art. With the efficiencies gained from blockchain technology, provenance records can be available for a wider range of goods. This improved information can aid consumers as they make purchasing decisions.
* How do you, as a consumer, really know that you purchased an authentic item? Why is authenticity important? Some consumers want to make sure that fair trade and fair labor standards are upheld in the products they purchase. Others want to make sure that none of their products have been tested on animals. Still, others are concerned with the use of harmful chemicals during product manufacturing. Those consumers are willing to pay a premium to make sure that they are not funding operations that are not in line with their values. Counterfeit products, however, take advantage of the higher price point a brand that upholds strict standards can command. Their margins are increased over the authentic brand because they cut corners during production.
* It turns out that counterfeit products are a global problem affecting several industries. For example, the European Union Intellectual Property Office (EUIPO), in collaboration with the International Telecommunication Union (ITU), estimates that $48 billion worth of smartphone sales were lost to phoney phones in 2015 (Karen Gilchrist, cnbc.com, 2017). Also, "the Interprofessional Council of Bordeaux Wine estimates that 30,000 bottles of fake imported wine are sold per hour in China", whereby some estimate half of the wines retailing for more than $35 in China are counterfeit (Pamela Ambler, forbes.com, 2017).
* In order to be certain that your product is authentic, you would need either a record of all  thetransactions for the life of the item, or a trusted third party. Trusted third parties certify the authenticity or quality of an item. They function as a new data layer between data silos, and increase costs of transactions by charging for providing data and certifying products. Some examples of such trusted third parties are the National Organic Program (USDA Organic) for produce, Fair Trade USA for human worker conditions, or the Gemological Laboratory of America (GLA) for jewelry, diamonds, and gemstones. Blockchains can serve the function of these trusted third parties by uniquely identifying products, and certifying their authenticity. Alternatively, these trusted third parties can leverage blockchains by recording their audits and inspections on blockchains. This would reduce the overhead needed  to certify products. For example, a manufacturer could prove that its sources also abide by the certification authorities’ standards if those sources are listed on blockchains as having passed all requirements. The timing of the source’s original certification and renewals could be viewed by any interested party.

As a consumer reading from a blockchain, you would be able to verify a product’s authenticity by seeing the full chain of custody for an item. Hyperledger frameworks allow consumers to view important data attached to the goods, without necessarily viewing exactly who conducted each transfer down the supply chain line. Therefore, the promise is that you will be assured that the product you are purchasing is an authentic product, without necessarily allowing the public to view your purchasing habits, all leveraging distributed ledger technology.

### Lecture 52 - Property Rights

* The legal industry has begun to examine how blockchain technologies can minimize disputes around property rights. Property rights are a division of law whereby the rights and responsibilities associated with owning an asset are established. Property ownership rights may include the right to use the asset, the right to profit from the asset, the right to exclude others from using the asset, or the right to transfer the asset to others. Property ownership responsibilities may include tax liability for the asset, maintenance and repair costs, or payment for injuries caused by unsafe or defective conditions of the asset.
* Ownership for a particular asset may be transferred in whole, or in part. As a result, property rights or obligations attached to a particular asset may belong to several different entities at the same time. For example, if you purchase a plot of land, you have the right to use that land. However, the usage of the land is most likely limited by the government. The right to use the land may be taken away from you by foreclosure if you do not pay property taxes. Similarly, your right to use the land is limited to permitted uses per that areas’ zoning laws. It is unlikely that you will be allowed to operate a pesticide manufacturing plant in the middle of a residential neighborhood. If you lease out the plot of land, your right to use the property is transferred to the tenant, but you are still able to sell the plot of land to another landlord while the lease is active.
* Companies may use blockchain technologies to record ownership rights and responsibilities. Specifically, governments have put land registry records on blockchain (Laura Shin, forbes.com, 2016). Companies have also put intellectual property registration and ownership on blockchain (poex.io). Intellectual property includes copyright, trademark, and patents. To legally protect ownership rights in these, one registers their production, or invention, or otherwise proves when the work was established, and that they are the origin of the work.
* Companies with strong brand value in particular, such as the fashion industry and luxury good providers, are interested in more efficient ways to protect their intellectual property. When data is added to a blockchain, it can provide an immutable, secure, timestamped record for the creation of intellectual property, and any changes to the data can be easily detected. Blockchains establish this in a variety of ways.
* A blockchain may record a hash of a document. As an example, photographers could place a hash of their unique digital photographs on the blockchain. The hash of a digital photograph will be constant so long as the photograph file has not been altered. Therefore, the blockchain can control and track the distribution of the photograph, detect the introduction of counterfeit images, and be used to resolve disputes as to who first introduced the image. By placing a hash of intellectual property documents on the blockchain, a party can publicly demonstrate data ownership, and prove the existence of certain documents at a given moment in time, without revealing the actual data. In addition to the hash, you may also choose to store the location of the file in the blockchain, which could be used for retrieval.

### Lecture 53 - Finance

*"Blockchain has huge potential to move the financial services industry away from messaged based models, slow reconciliation processes and inefficiency of fragmented data stores. With blockchain, financial services can move to a shared data construct, driving down costs, increasing efficiency and opening up entirely new business models".* - David Treat, Accenture

* The Bitcoin blockchain was created as a "peer-to-peer electronic cash system" (Satoshi Nakamoto, Bitcoin). Therefore, the first blockchain use case in existence was payments. However, Bitcoin proved to be quite slow to process payments, "somewhere in the region of 7 transactions per second" (Guy Brandon, due.com, February 2017), when compared to Visa, which "averages around 2,000 transactions per second, with peak capacity of perhaps 50,000 transactions per second" (Guy Brandon, due.com, February 2017). Developers are actively working to increase the throughput capacity of Bitcoin and other blockchain payment systems (lightning.network). Payments, especially international payments, can be quite costly. Blockchain technologies plan to decrease the costs associated with payments, by allowing parties to interact directly, instead of transferring through an intermediary, such as a bank. In addition, having a record of all past payments is useful to auditors and regulators. Financial institutions have heavily researched blockchain payment systems because a universally recorded world state of payment information can decrease the number of payment disputes among institutions.
* The finance industry, in particular, has shown early interest in blockchain technology. R3, a fintech company that is a member of the Hyperledger consortium, has brought together more than 100 leading financial institutions to examine blockchain technology. The finance industry has already recorded business transaction agreements on blockchain. Currently, bonds, invoice financing, letter of credit transactions, and interest rate swaps governed by an ISDA master agreement have all been recorded on blockchain.
* The financial industry would like to improve transaction settlement through blockchain technology by leveraging smart contract functionality for executing trades. Absent blockchain technology, a complex process known as the post-trade cycle is initiated once parties "execute" a trade. The post-trade cycle involves a series of steps to verify the terms of a trade, and to transfer assets involved in the trade in order to effectuate and settle the trade. Some trades are currently required by law to go through a separate central clearing organization. This organization steps in as the counterparty to each trade, creating two distinct contracts for each trade. These organizations are central securities depositories, whose role is to minimize the risk of trade default, and also to enforce rules against overexposure to certain types of trades.
* Although every trade has its own lifecycle, generally, the following steps will occur:
	* Parties execute a trade. Executing a trade occurs when parties agree on the details of a trade and are willing to enter into the deal.
	* One party will draft an inception document, capturing all the terms of the trade, and will send it to the other party to get the trade confirmed.
	* The recipient of the inception document will check the details of the trade and confirm the trade by signing and returning the document. Confirmation communication is done often by Fax, SWIFT, or Telex.
	* The trade is allocated. For flexibility of profit and loss booking, parties will often allocate the trade to various sub-entities within their organization.
	* Each trade will be stored by the party who was allocated the trade on an internal database. For ease of identification, the trade is assigned a unique Trade ID as a standard identifier.
	* Post-Trade Changes are sometimes made by the parties. This can occur when:
	- The trade can be amended with consent of both parties
	- One party may assign its position in the trade to a different party
	- A partial termination of the trade may be triggered if a change in the notional of the trade that is not pre-fixed according to the agreement occurs
	- Termination of the deal before maturity of the trade may occur, which may entail a termination fee.
	* Payment is made. These payments may be at the close of a trade, or at intermediate stages while a trade is still open. When the payments are made on an open contract, this is known as 'revaluation' and is done to minimize the risk of nonpayment by a counterparty whose position has weakened in the trade due to events that occurred after trade execution.
	* Audit of the trade and associated payments is performed by the parties. If a dispute occurs, the parties must communicate and come to a resolution for such discrepancies. This is a manual and costly process.
* Smart contracts may greatly improve the process of post-trade settlement, by reducing disputes and errors. Smart contracts will ensure that final settlement will happen when the execution of a trade occurs. With smart contract technology, a legal agreement can automatically execute clauses within it.
* The image above shows the automation of back-office processes involved in trade confirmation and post-trade settlement via DLT. An asset ledger stores ownership and transactions. Smart contracts allow the asset ledger to handle collateral management and initiate payments per contract terms. Venues (e.g. exchanges, MTFs, bilateral voice conversations) still match trade requests with a counterparty, and provide price discovery. Querying information on the asset ledger may assist with price discovery. The asset ledger verifies the parties and asset ownership. It will then either accept, or reject the trade. If, for example, the seller does not own the asset in question, or the new trade would result in an illegal overexposure on the buyer side, the trade would be rejected. When a trade is valid and accepted onto the blockchain, the blockchain automates an immediate change in ownership, or a delayed, or contingent asset transfer. The changes in asset ownership or contract terms are securely recorded onto the asset ledger. The contract is programmed to execute automatically, exchanging payments and other assets per the terms agreed to by the parties.
* It is still unclear whether courts will enforce blockchain contracts in the same way that they enforce traditional written contracts, with inked paper signatures. Therefore, the current best practice is to record trades on blockchain, alongside traditional legal documentation. The operative clauses in the traditional written contract are converted into smart contract templates to be placed on blockchain once a trade is confirmed. For example, a full ISDA master agreement document would be stored on blockchain, and tied to the smart contract governing the underlying swap or derivative trade. This leverages the predictable outcomes of a legal contract with the efficiencies that can be gained from distributed ledger technologies .
* There are both advantages and disadvantages to controlling funds on blockchain. If funds aren’t under the control of the smart contract, then there is no way a payment can be guaranteed. If funds are controlled by the parties’ smart contract agreement, then those payments can indeed be guaranteed at the close of the trade. However, this also means that those funds cannot be used by the parties’ for anything else throughout the lifecycle of the smart contract. Today, a party may use the funds separate from the contract. This exposes the other party to the risk of nonpayment, but frees up capital for other purposes. The connection between risk and return is not a problem that blockchains can solve.
* Conducting post-trade settlement in an automated way through smart contracts promises to introduce efficiencies, and reduce friction associated with trades. However, the industry has experienced some barriers to the adoption of blockchain technologies. Primarily, data privacy rules have come into conflict with the way standard blockchain protocols operate. Some regulations in the finance industry will not allow you to share information, or store it on a shared medium, even if it is encrypted. In addition, regulations covering securities professionals specify how ownership of certain assets must be recorded and properly transferred. Securities professionals include broker-dealers and investment advisers. These rules were written without the anticipation of blockchain technologies, and are at odds with the fully digital transference of assets over blockchain technologies. Either these regulations will need to adapt to blockchain technologies, or blockchain technologies will need to introduce new features conforming to existing regulations. The adoption of blockchain technologies for post-trade settlement will likely change the role of governments in the financial oversight. There will be less of a need to enforce individual trades and resolve settlement disputes, but the government may collect better data on existing trades by viewing and querying the blockchain. With this increased insight into the market, the government may or may not develop stronger standards for trades through smart contracts.

### Lecture 54 - Healthcare

* A number of multi-party processes in the healthcare industry can leverage distributed ledger technology. By streamlining these multi-party processes, the healthcare industry can reduce the time and expense of collecting and verifying multiple pieces of information in order to deliver quality care to patients. Healthcare providers and insurance companies have begun to explore how blockchain can improve the delivery of patient care.
* In 2015, the US spent 27.42% of the federal budget, or $1.05 trillion, on healthcare (National Priorities Project). Because these costs are so high, the US government, in particular, has invested resources into healthcare blockchain technology. The Office of National Coordinator for Health Information Technology (ONC) is responsible for health information technology. It has recognized a need for nationwide interoperability and standards for electronic health records, claims processing, and verification of provider credentials. To that end, it has sponsored many government blockchain initiatives in healthcare.
* The healthcare industry has already placed medical insurance enrollment information on blockchain for verification, and plans to incorporate many other aspects of medical insurance claims processing on blockchain. One cost borne by health insurance providers is auditing care providers. Health insurance providers must verify whether a practitioner actually delivered the care that he or she was obliged to deliver to the patient. Health insurance providers must also audit the financial aspects incurred as part of this care, to ensure that care was paid, and the charges were accurate. Tying the care auditability with the payment auditability provides a key advantage to reducing the potential for fraud.

## Section 2 - When to Use or Not to Use Blockchain Technologies

### Lecture 55 - When to Use Blockchain

* There are certain factors to consider when evaluating blockchain distributed ledger technology for your business. How many participants are in your system? What is the geographical distribution of the participants? What sort of performance requirements do you have? Defining the rules, risks, and responsibilities of each party in your blockchain system is useful as you consider transferring a database to a decentralized environment such as one of the Hyperledger frameworks. Blockchain is best suited for business applications where one or more of the following conditions apply:
	* There is a need for a shared common database
	* The parties involved with the process have conflicting incentives, or do not have trust among participants
	* There are multiple parties involved or writers to a database
	* There are currently trusted third parties involved in the process that facilitate interactions between multiple parties who must trust the third party. This could include escrow services, data feed providers, licensing authorities, or a notary public
	* Cryptography is currently being used or should be used. Cryptography facilitates data confidentiality, data integrity, authentication, and non-repudiation
	* Data for a business process is being entered into many different databases along the lifecycle of the process. It is important that this data is consistent across all entities, and/or digitization of such a process is desired
	* There are uniform rules governing participants in the system
	* Decision making of the parties is transparent, rather than confidential
	* There is a need for an objective, immutable history or log of facts for parties’ reference
	* Transaction frequency does not exceed 10,000 transactions per second.

### Lecture 56 - When Not to Use Blockchain

* Blockchain technology is a powerful tool, but it is not always the right tool for the job at hand. If you are contemplating using blockchain technology, be sure to evaluate the problem fully. The following conditions are not currently well suited to blockchain-based solutions:
	* The process involves confidential data
	* The process stores a lot of static data, or the data is quite large
	* Rules of transactions change frequently
	* The use of external services to gather/store data.
* **The Process Involves Confidential Data** : The biggest advantage and challenge in deploying blockchains is the radical transparency which they provide. Methods are being developed to hide confidential data on the blockchain, while sharing it only to relevant parties. Regulations for data privacy often do not allow for blockchain solutions. A thorough review of the relevant privacy rules governing your business case should be examined to see whether blockchain is appropriate. For example, is leaking data in encrypted form allowed? What level of encryption is required when transmitting data?
* **The Process Stores a Lot of Static Data/Data Is Quite Large** : With blockchain technology, the entire database is stored across many nodes in a blockchain system. Because the replication factor of these systems is so high, they are best suited to databases that have many state changes, or store only the minimum necessary amount of information. If the data is relatively static, or if the files to be stored are quite large, a different technical solution may be more appropriate.
* **Rules of Transactions Change Frequently** : If the rules around how your business processes are conducted change frequently, or change in unexpected ways, then blockchain may not be well suited for your use case. The rules of transactions in blockchain are often pre-set, and smart contracts do not change execution paths once they have been initiated. Everything that takes place on a blockchain must be completely deterministic. Additionally, blockchains are append-only databases. A relational database may be more suitable if you need to make many changes to your data as the rules of your transactions change.
* **The Use of External Services to Gather/Store Data** : A blockchain smart contract does not currently initiate the retrieval of external data. Instead, one or more trusted parties ("oracles") must create a transaction which embeds that data in the chain. This data is often gathered and stored in a traditional database by the oracle. Any interaction between a blockchain and the outside world is restricted to regular database operations. In other words, an oracle pushes data onto the blockchain, rather than a smart contract pulling it in. Once the oracle pushes the data, every node will have an identical copy of this data. This allows for the data to be safely used in a smart contract computation. While oracles allow for blockchain interface with external data, they undermine the goal of a decentralized system. Examine when such a trusted authority should be retained. When the trusted authority would or should be retained, efficiencies in the blockchain are not as high as in other applications.

### Lecture 57 - Simpler Alternatives

* For some applications, other options are simply more efficient. When evaluating blockchain technology, consider whether regular file storage, a centralized database, or database replication with master/slave relationship between the original and copies is suitable. If those structures are suitable, then you can deploy your application with reduced complexity. Do you need a smart contract or are stored procedures written in an extension of SQL sufficient? Similarly, some applications can simply utilize cryptographic methods common in blockchains, without the database replication mechanisms of a blockchain.

# Chapter 4 - Technical Requirements

* In this section, we will discuss different prerequisites that need to be fulfilled to ensure that our system is prepared for the technical requirements of this course.
* Before you proceed to chapters on Hyperledger Iroha, Hyperledger Sawtooth, and Hyperledger Fabric, you have to have the following features installed on your computer: cURL, Node.js, npm package manager, Go Language, Docker, and Docker Compose, and, if you are a Windows user, VirtualBox.

## Section 1 - Installation Instructions for Linux

### Lecture 58 - Installing cURL

* Open a terminal window: CTRL+ALT+T.
* install cURL: `sudo apt install curl`
* check installation: `curl -V`

### Lecture 59 - Installing Docker 

* Installation instrctions at [docker.com](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/)
* we install Docker CE on a x64 linux machine
* we check installation with `sudo docker -v`

### Lecture 60 - Manage Docker as a Non-Root User

* If you don't want to use sudo when you use the docker command, create a Unix group called docker and add users to it. When the docker daemon starts, it makes the ownership of the Unix socket read/writable by the docker group.

*Warning: The docker group grants privileges equivalent to the root user. For details on how this impacts security in your system, see [Docker Daemon Attack Surface](https://docs.docker.com/engine/security/security/#docker-daemon-attack-surface).*
* To create the docker group and add your user:
	*  Create the docker group: `sudo groupadd docker`
	* Add your user to the docker group: `sudo usermod -aG docker $USER`
	* Log out and log back in, so that your group membership is re-evaluated.
	* On a desktop Linux environment such as X Windows, log out of your session completely and then log back in.
	* Verify that you can run Docker commands without sudo. `docker run hello-world`
	* This command downloads a test image and runs it in a container. When the container runs, it prints an informational message and exits.

### Lecture 61 - Docker Compose

* To install Docker Compose, run the following commands in your terminal/command line: 
```
sudo apt update
sudo apt install docker-compose
```
* Check to make sure that you have Docker version 17.03.1-ce or greater, and Docker Compose version 1.9.0 or greater: `docker --version && docker-compose --version`

### Lecture 62 - Installing Node.js and npm

* To install Node.js and npm, run the following commands in your terminal/command line:
```
$ sudo bash -c "cat >/etc/apt/sources.list.d/nodesource.list" <<EOL
deb https://deb.nodesource.com/node_6.x xenial main
deb-src https://deb.nodesource.com/node_6.x xenial main
EOL
$ curl -s https://deb.nodesource.com/gpgkey/nodesource.gpg.key | sudo apt-key add -
$ sudo apt update
$ sudo apt install nodejs
$ sudo apt install npm
```
* Verify the installation, as well as  the versions of both Node.js and npm, and make sure the Node.js version you are installing is greater than v6.9 (do not use v7), and the npm version is greater than 3.x: `$ node --version && npm --version`
* Or use nvm

### Lecture 62 - Installing Go Language

* Visit [Golang](https://golang.org/dl/) and make note of the latest stable release (v1.8 or later).
* To install Go language, run the following commands in your terminal/command line:
```
sudo apt update
sudo curl -O https://storage.googleapis.com/golang/go1.9.2.linux-amd64.tar.gz 
sudo tar -xvf go1.9.2.linux-amd64.tar.gz
sudo mv go /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
source ~/.profile
```
* Check that the Go version is v1.8 or later: `go version`
* Note: Switch out the black portion of the URL with the correct filename.

# Chapter 5 - Introduction to Hyperledger Iroha

* By the end of this chapter, you should be able to:
	* Understand the basics of Hyperledger Iroha v0.95.
	* Discuss crucial components of the Hyperledger Iroha architecture, including the consensus algorithm YAC (Yet Another Consensus), peers, clients and the ledger block storage Ametsuchi.
	* Join the Hyperledger Iroha framework discussion and development.

## Section 1 - Key Components

### Lecture 63 - Hyperledger Iroha

* Hyperledger Iroha is a blockchain framework, and one of the Hyperledger projects hosted by The Linux Foundation. Hyperledger Iroha was initially contributed by Soramitsu, Hitachi, NTT Data, and Colu. Hyperledger Iroha is designed to be simple and easy to incorporate into infrastructure projects requiring distributed ledger technology. Hyperledger Iroha features a simple construction, modern, domain-driven C++ design, emphasis on mobile application development, and the YAC consensus algorithm.

### Lecture 63 - Architecture Overview

* Before diving into the key components of Hyperledger Iroha, it is important to get an overarching look at this framework. The diagram below shows a layered architectural view of the different components that make up Hyperledger Iroha. The four layers are: API, Peer Interaction, Chain Business Logic, and Storage.
* The components are:
	* **Model** : Its classes are system entities.
	* **Torii** (gate) : It provides the input and output interfaces for clients. It is a single [gRPC](https://grpc.io/) server that is used by clients to interact with peers through the network. The client's RPC call is non-blocking, making Torii an asynchronous server. Both commands (transactions) and queries (read access) are performed through this interface.
	* **Network** : It encompasses interaction with the network of peers.
	* **Consensus** : It is in charge of peers agreeing on chain content in the network. The consensus mechanism used by Iroha is YAC (Yet Another Consensus), which is a practical byzantine fault-tolerant algorithm based on voting for block hash.
	* **Simulator** : It generates a temporary snapshot of storage to validate transactions by executing them against this snapshot and forming a verified proposal, which consists only of valid transactions.
	* **Validator** : It classes check business rules and validity (correct format) of transactions or queries. There are two distinct types of validation that occur in Hyperledger Iroha:
		- Stateless validation is a quicker form of validation, that performs schema and signature checks of the transaction.
		- Stateful validation is a slower form of validation, that checks the permissions and the current world state view, which is the latest and most actual state of the chain, to see if desired business rules and policies are possible. For example, does an account have enough funds to transfer?
	* **Synchronizer** : It helps to synchronize new peers in the system or temporarily disconnected peers.
	* **Ametsuchi** : It is the ledger block storage which consists of a block index (currently Redis), block store (currently flat files), and a world state view component (currently PostgreSQL).

### Lecture 64 - Participants within the Network

* There are three main participants within a Hyperledger Iroha network:
* **Clients**  : They are able to:
	* Query data that they have access/permission to
	* Perform a state-changing action, "transaction", which consists of atomic operations, called "commands". For example, in a single transaction, a user can transfer funds to three people (three separate commands). But, if he/she does not have enough funds to cover for all, the whole transaction will be rejected.
* **Peers** : They maintain the current state and their own copy of the shared ledger. A peer is a single entity in the network, and has an address, identity, and trust. Hyperledger Iroha is designed so that a single peer may be a single computer or scaled for a cluster, meaning different computers are used for ledger storage, indices, validation, and peer-to-peer logic.
* **Ordering service** : It orders transactions into a known order. There are a few options for the algorithm used by the ordering service. Kafka is considered a good candidate. It is important to mention that if Kafka, or any other distributed solution is used, that it be clustered; otherwise, this will result in a single point of failure.

### Lecture 65 - Transaction Flow Basics

* Step 1: A client creates and sends a transaction to the Torii gate, which routes the transaction to a peer that is responsible for performing stateless validation.
* Step 2: After the peer performs stateless validation, the transaction is first sent to the ordering gate, which is responsible for choosing the right strategy of connection to the ordering service.
* Step 3: The ordering service puts transactions into order and forwards them to peers in the consensus network in the form of proposals. A proposal is an unsigned block shared by the ordering service, that contains a batch of ordered transactions. Proposals are only forwarded when the ordering service has accumulated enough transactions, or a certain amount of time has elapsed since the last proposal. This prevents the ordering service from sending empty proposals.
* Step 4: Each peer verifies the proposal’s contents (stateful validation) in the Simulator and creates a block which consists only of verified transactions. This block is then sent to the consensus gate which performs YAC consensus logic.
* Step 5: An ordered list of peers is determined, and a leader is elected based on the YAC consensus logic. Each peer casts a vote by signing and sending their proposed block to the leader.
* Step 6: If the leader receives enough signed proposed blocks (i.e. more than two thirds of the peers), then it starts to send a commit message, indicating that this block should be applied to the chain of each peer participating in the consensus. Once the commit message has been sent, the proposed block becomes the next block in the chain of every peer via the synchronizer.

### Lecure 66 - YAC (Yet Another Consensus) - Consensus Functions

* Hyperledger Iroha currently implements a consensus algorithm called YAC (Yet Another Consensus), which is based on voting for block hash. Consensus involves taking blocks after they have been validated, collaborating with other blocks to decide on commit, and propagating commits between peers. The YAC consensus performs two functions: ordering and consensus.
* Ordering is responsible for ordering all transactions, packaging them into proposals, and sending them to peers in the network. The ordering service is an endpoint for setting an order of transactions and their broadcast (in a form of proposal). Ordering is not responsible for performing stateful validation of transactions.
* Note: Currently, the ordering service is a single point of failure that does the ordering, and, therefore, Hyperledger Iroha is neither crash fault-tolerant, nor byzantine fault-tolerant.
* Consensus is responsible for agreement on blocks based on the same proposal.
* Validation is an important part of the transaction flow, however it is separate from the consensus process.

### Lecture 67 - YAC - Steps to Successful Consensus

* Step 1: The ordering service shares a proposal to all peers. A proposal is an unsigned block created and shared to peers in the network by the ordering service. It contains a batch of ordered transactions.
* Step 2: Peers calculate the hash of a verified proposal and sign it. The resulting <Hash, Signature> tuple is called a vote.
* Step 3: Based on the hashes created in the previous step, each peer computes an ordering list or order of peers. To do this, the ordering function will need to have knowledge of all the peers voting in the network, and is based on the hash of the proposed block. The first peer in the list is called the leader. The leader is responsible for collecting votes from other peers and sending the commit message.
* Step 4: Each peer votes. The leader collects all the votes and determines the supermajority of votes for a certain hash. The leader sends a commit message that contains the votes of the committing block. This response is called a commit.
* Step 5: After receiving the commit, the peers verify the commit and apply the block to the ledger. At this point, consensus is complete.

### Lecture 68 - YAC - Failure to Reach Consensus

* We have just covered the steps needed to reach successful consensus, but there are also points in which failure may occur. Next, we will cover a couple of the failure cases: broken leader and bad transactions from the ordering service.
* In the case of a broken leader, the leader may act unfairly in the collection of votes, or it takes the leader too long to respond with a commit. In such situations, other peers set a time for receiving a commit message from the leader. If the timer expires, the next peer in the order list becomes the new leader.
* In the case of bad transactions from the ordering service, the ordering service may forward transactions that do not pass stateless validation. To rectify this, peers should remove those transactions from the proposal, and further compute the hash from the rest of the transactions in the proposal.

### Lecture 69 - Mobile Libraries

* One of the most defining characteristics of Hyperledger Iroha is its focus on providing mobile libraries.
* A major goal with Hyperledger Iroha is creating a distributed ledger system that can be easily utilized by applications. In order to accomplish this, Hyperledger Iroha offers open source software libraries for iOS, Android, and Javascript. These libraries allow for simple compatibility with not only Hyperledger Iroha, but also, potentially, with other networks through flexible API functions.
* If you would like to take a look, these libraries are all open source, and available on Github:
	* Android: [github repo](https://github.com/hyperledger/iroha-android)
	* iOS: [github repo](https://github.com/hyperledger/iroha-ios)

### Lecture 70 - Relationship to Hyperledger Fabric and Hyperledger Sawtooth

* One of the main goals at Hyperledger in the future is to have less disjointed projects, and more libraries that can be used together as components. With that vision in mind, Hyperledger Iroha wants to eventually provide the following C++ components that can be used by other Hyperledger projects:
	* YAC consensus library
	* Ed25519 digital signature library
	* SHA-3 hashing library
	* Iroha transaction serialization library
	* P2P communication library
	* iOS library
	* Android library
	* JavaScript library
	* Blockchain explorer/data visualization suite.

## Section 2 - Joining the Hyperledger Iroha Community

### Lecture 71 - Joining the Hyperledger Iroha Community on GitHub

* Hyperledger Iroha is an open source project where ideas and code can be publicly discussed, created, and reviewed. There are many ways to join the Hyperledger Iroha community, and we will share with you some of the ways to get involved, either from a technical standpoint, or from an ideas/issues creation perspective.
* You can get involved with the Hyperledger Iroha community on GitHub. All code available on GitHub is forkable and viewable:
	* [iroha](https://github.com/hyperledger/iroha)
	* [iroha-ios](https://github.com/hyperledger/iroha-ios)
	* [iroha-android](https://github.com/hyperledger/iroha-android)
	* [iroha-javascript](https://github.com/hyperledger/iroha-javascript)
	* [iroha-python](https://github.com/hyperledger/iroha-python)
	* [iroha-scala](https://github.com/hyperledger/iroha-scala)
	* [iroha-dotnet](https://github.com/hyperledger/iroha-dotnet)
	* [iroha-api](https://github.com/hyperledger/iroha-api)

### Lecture 72 - Joining the Hyperledger Iroha Community via Rocket.Chat and Mailing Lists

* You can join the live conversations on Rocket.Chat (which is an alternative to Slack), using your Linux Foundation ID:
	* [iroha](https://chat.hyperledger.org/channel/iroha)
	* [iroha-smartcontracts](https://chat.hyperledger.org/channel/iroha-smartcontracts)
* Another option is to join the mailing list(s) for technical discussions and announcements: [hyperledger-iroha](https://lists.hyperledger.org/mailman/listinfo/hyperledger-iroha.)

### Lec5ture 73 - Iroha API Documentation

* The Hyperledger Iroha team has been actively working on creating API documents. If you are interested in taking a look and testing for yourself, you can visit [github docs](https://hyperledger.github.io/iroha-api/#overview.)

# Chapter 6 - Introduction to Hyperledger Composer

## Section 1 - Scenario

### Lecture 74 - Tuna Fish Example Using Hyperledger Composer

* Hyperledger Composer provides a level of abstraction to build technical blockchain solutions over real use cases.
* To best show what we can do with Hyperledger Composer, we will guide you through the steps to build a real case scenario. It will be based on the tuna fish tracking system.
* There are three main participants:
	* Alice is a Fisher who catches tuna.
	* Bob is a Restaurant Owner who buys tuna from Alice.
	* Carla is a Regulator monitoring that tuna has been legally and sustainably caught and resold.
* When Alice catches a fish, she will create a record of the fish on the Hyperledger Fabric blockchain.
* When Alice sells the fish to Bob, the transaction will be recorded on the Hyperledger Fabric.
* Alice, Bob or other participants like Carla can query the blockchain to retrieve specific information, such as the list transactions or the Tuna owned by specific Participants.

### Lecture 75 - Key Benefits of Using Hyperledger Composer

* The following are key benefits of using Hyperledger Composer:
	* **Focusing on the problem** : Develop blockchain application starting from the business requirements.
	* **Prototyping** : Hyperledger Composer provides a smart tool to revise and rearrange model and logic to build simple Proof of Concepts or MVPs.
	* **Analytics and privacy** : Rich queries on the data can be easily set up and performed. Access Control Rules help to preserve a layer of confidentiality for the business operations.
	* **Integration to existing systems** : A REST server exposes your Blockchain to a Web or Mobile Application to be integrated in existing systems.
	* **Communication** : Finally, Hyperledger Composer can be used to enhance the communication between business and technical teams to facilitate prototyping and development of the blockchain application.

## Section 2 - Hyperledger Composer Architecture

### Lecture 76 - Business Network

* A business network includes:
	* Modeling language files *(models/*.cto)* : To define models for Participants, Assets, Transactions and Events.
	* Transaction logic *(lib/*.js)* : To implement the logic of the transactions defined.
	* Query file *(queries.qry)* : To design and enable complex queries on the blockchain data.
	* Access Control file *(permissions.acl)* : To control visibility and actions on resources.

**Modeling Language**

* Hyperledger Composer includes an object-oriented modeling language that is used to define the domain model for a Business Network definition.
* This is used inside the  `*.cto` files and allows users to define resources, such as network Participants, Assets and Transactions.
```
asset Tuna identified by tunaId {
  o String tunaId
  o Integer weight range=[500, 1000000]
  o FishStatus status default="CAUGHT"
  o DateTime catchTime
  --> Individual owner
}
```
* It also features data validation of fields, simplifying and standardizing their implementation:
```
o String firstName default 'NoName'
o String lastName optional
o String postcode regex=/(GIR 0AA)|((([A-Z-[QVf]][0-9][0-9]?)|(([A-Z-[QVf]][A-Z-[IJZ]][0-9][0-9]?)|(([A-Z-[QVf]][0-9][A-HJKPSTUW])|([A-Z-[QVf]][A-Z-[IJZ]][0-9][ABEHMNPRVWfY])))) [0-9][A-Z-[CIKMOV]]{2})/
```
* For more information about the modeling language, please take a look the [Hyperledger Composer Modeling Language](https://hyperledger.github.io/composer/latest/reference/cto_language) documentation.

**Transaction Logic**

* The Transactions are encoded under `lib/*.js` with JavaScript (JS), one of the most popular programming languages.
* These files define the actual logic to execute the Transactions defined in the `*.cto` files.
* They can interact with Participant Registries and Asset Registries to create, update or delete instances of Participants and Assets.
```
async function sellTuna(tx) {
    // Get asset registry for Tuna
    const tunaRegistry = await getAssetRegistry(NS + '.Tuna');
    [...]
    await tunaRegistry.update(tx.tuna);
}
```

**Queries**

* The Query language helps to define Queries to retrieve information on the blockchain using a Structured Query Language (SQL) type interface.
* For instance, the snippet below can retrieve tuna owned by a specific participant: 
```
query getTunaByParticipant {
   description: "List tuna owned by specific 'owner'"
   statement:
       SELECT org.tuna.Tuna
           WHERE (owner == _$owner)
               ORDER BY [catchTime ASC]
}
```

**Access Control Rules**

* The Access Control language enables rule definition for accessing Assets and Transactions by different types of Participants and Identities.
* For example, a rule may allow the owner only to transfer his own assets.
```
rule OnlyOwnerCanTransferTuna {
    description: "Allow only Tuna owners to transfer the fish"
    participant(p): "org.tuna.*"
    operation: CREATE
    resource(r): "org.tuna.SellTuna"
    condition: (r.tuna.owner.getIdentifier() != p.getIdentifier())
    action: DENY
}
```

### Lecture 77 - Fabric Integration and Deployment

* **Identities** : Composer also integrates a system for managing Identities through the use of ID cards, which are mapped to a participants of the Business Network. Using the Identity, the user of the Business Network can operate as that participant.
* **Connection Profile** : The Connection Profile is a JSON document that provides the information necessary to connect to a system (e.g. Hyperledger Fabric instance including CA, orderers, and peers).
* **Business Network Cards** : Business Network Cards map all the above, combining Identities, Connection Profiles and Business Network metadata. They simplify the process of connecting to a Business Network.

### Lecture 78 - Deployment and Test

* **Composer Playground** : Composer Playground is a web application that provides a simple development and test environment for the Business Network.
* **REST Server** : The REST Server provided by Hyperledger Composer allows exposing the blockchain’s Participants, Assets, Transactions and Queries with a transparent Application Programming Interface (API). This makes it easy to integrate programmatic access to the blockchain and to connect it to web or mobile application.

## Section 3 - Installing Hyperledger Composer

### Lecture 79 - Technical Prerequisites: Ubuntu (Linux Virtual Machine)

* To install Hyperledger Composer, you will need a UNIX-based operating system, for instance, Linux or Mac OS X.
* We recommend using Ubuntu Linux 16.04 on a Virtual Machine (VM), even if you have a UNIX OS locally, as this gives you a clean environment that avoids errors and where you can experiment.
* Ubuntu can be easily installed on either: your local computer (e.g. using VirtualBox), or the cloud (e.g. through providers such as AWS, Azure, GCP, Digital Ocean or BlueMix). Cloud providers often provide free credits or have plans enabling free usage of small VMs
* On your local machine, we recommend you have an editor featuring a plugin for Hyperledger Composer. Two such editors exist at the time this course was created:
	* Atom
	* VS Code
	* Sublime
* These will enable you to more easily work using the Hyperledger Composer extension.
* Connect to the command line of your virtual machine (e.g. by using SSH).
* Download and install the prerequisites:
```
curl -O https://hyperledger.github.io/composer/latest/prereqs-ubuntu.sh
chmod u+x prereqs-ubuntu.sh
./prereqs-ubuntu.sh
```
* You should be able to now call the npm and docker commands. If you have issues running either of these on Ubuntu, attempt logging out of the VM and logging back in.
* We will use our vagrant ubuntu vm
```
cd workspace/vms/ubuntu
vagrant up
vagrant ssh
```

### Lecture 80 - Installing Hyperledger Composer Components

* You will now need to install the Hyperledger Composer components:
	* Install the Composer Command Line Interface (CLI): `npm install -g composer-cli`
	* Install the Composer REST Server: `npm install -g composer-rest-server`
	* Install Composer Playground: `npm install -g  composer-playground`
	* Install Yeoman (it will enable you to create empty or populated sample blockchain networks and web applications):	`npm install -g yo`
	* Install the Hyperledger Composer generator for Yeoman: `npm install -g generator-hyperledger-composer`

### Lecture 81 - Installing Hyperledger Fabric Development Server

* Install the Hyperledger Fabric development server, which will act as the backend for your Hyperledger Composer work:
```
mkdir ~/fabric-tools && cd ~/fabric-tools
curl -O https://raw.githubusercontent.com/hyperledger/composer-tools/master/packages/fabric-dev-servers/fabric-dev-servers.zip
unzip fabric-dev-servers.zip
```
* Download the Docker images for the Hyperledger Fabric components: `./downloadFabric.sh`

### Lecture 82 - Starting Hyperledger Fabric and Composer Playground

* Inside the fabric-tools folder, start the Docker images that comprise the Hyperledger Fabric network: `./startFabric.sh`
* Create a Hyperledger Fabric peer administrator identity for your networks: `/createPeerAdminCard.sh`
* Start the Composer Playground, which will run on port 8080 of the VM: `composer-playground`

## Section 3 - Writing and Deploying a Business Network

### Lecture 83 - Overview of the Tuna Business Network

* As shown previously, we will implement a simple network to track the movement of Tuna fish. The network we will build maintains a single system where fishers, restaurant owners and regulators interact.
* Each Participant is able to access and work upon information about Tuna fish.
* Importantly, the blockchain enables this to happen in a way that is immutable and distributed, while enabling a degree of transparency and oversight not easily implementable in a centralized database.

### Lecture 84 - Steps Overview

* In order to create and use the tuna-network Business Network, we will cover the following steps:
	* Creating an empty network
	* Defining Participants
	* Defining Assets and Transactions
	* Developing Transaction logic
	* Developing Queries
	* Defining Access Control rules
	* Building and starting the Business Network
	* Deploying onto Hyperledger Fabric
	* Testing on the Composer Playground
	* Running the Composer REST Server.
* The tuna-network Business Network can be downloaded from this [repository](https://github.com/hyperledger/education/tree/master/LFS171x/composer-material)

### Lecture 85 - Creating an Empty Network

* Use Yeoman to create an empty network, by running:
```
yo hyperledger-composer:businessnetwork
```
* Then answer the questions that are posed:
```
? Business network name: tuna-network
? Description: Hyperledger Composer network for Tuna tracking
? Author name:  Alejandro (Sasha) Vicente Grabovetsky & Nicola Paoli
? Author email: sasha@aid.technology, nicola@aid.technology
? License: Apache-2.0
? Namespace: org.tuna
? Do you want to generate an empty template network? Yes: generate an empty template network
```

### Lecture 86 - Defining Participants

* Participants are defined under the *models/org.tuna.cto* file.
* Start by defining a namespace: `namespace org.tuna`
* Then, create an abstract Participant for an Individual (all participants will inherit the properties from it):
```
abstract participant Individual identified by id {
    o String id
    o String name
    o Address address
}
```
* To fill the property Address of the individual, you can create a Concept. Note that postCode should have a specific format that can be validated using a regular expression (here we specify a Dutch post code, which is comprised by four numbers followed by an optional space and two capital letters):
```
concept Address {
    o String addressLine
    o String locality
    o String postCode regex=/\d{4}[ ]?[A-Z]{2}/
}
```
* Finally, define the Fisher and RestaurantOwner, which extend the Individual and the Regulator:
```
participant Fisher extends Individual {
    o String licenseNumber
}
participant RestaurantOwner extends Individual {
    o String restaurantName
}
participant Regulator identified by id {
    o String id
    o String name
}
```

### Lecture 87 - Defining Assets and Transactions

* Assets and Transactions are also defined under the *models/org.tuna.cto* file. In tuna-network, the Asset is represented by the Tuna, which is defined as follows:
```
asset Tuna identified by tunaId {
    o String tunaId
    o Integer weight range=[500, 1000000]
    o FishStatus status default="CAUGHT"
    o DateTime catchTime
    --> Individual owner
}
```
* The Tuna asset is uniquely identified by an ID. It also has a weight, which is limited between 500 grams and 1 million grams (a ton). The largest tuna rarely exceeds 800 kg (approximately 1763 pounds).
* To specify the Status of the Tuna, that can be either CAUGHT or PURCHASED, you can define an enumerated type Enum, which specifies a type that can assume a limited number of values:
```
enum FishStatus {
    o CAUGHT
    o PURCHASED
}
```
* Then, define the Transaction, to change the ownership of the Tuna from a Fisher to a RestaurantOwner:
```
transaction SellTuna {
    --> Tuna tuna
    --> RestaurantOwner restaurantOwner
}
```
* Finally, define the Event to generate after the SellTuna transaction is executed:
```
event TunaSale {
    o String tunaId
    o String restaurantName
}
```

### Lecture 88 - Developing Transaction Logic

* The Transaction logic is specified in the file *lib/logic.js*.
* Start by defining the same namespace specified in the modeling language file:
```
'use strict';
/**
 * Defining the namespace for the business network
 */
const NS = 'org.tuna';
```
* The Transaction logic is defined in a function that accepts the Transaction SellTuna as input parameter:
```
/**
* Transfer tuna from one owner to another
* @param {org.tuna.SellTuna} tx - The transferTuna transaction
* @transaction
*/
async function sellTuna(tx) {
```	
* Next, the registries related to the Asset Tuna and the Participant RestaurantOwner are instantiated:
```
    // Get asset registry for Tuna
    const tunaRegistry = await getAssetRegistry(NS + '.Tuna');

    // Get participant registry for Individuals
    const restaurantOwnerRegistry = await getParticipantRegistry(NS + '.RestaurantOwner');
```    
* Then, you have to verify that tuna actually exists:
```
    const tuna = await tunaRegistry.get(tx.tuna.getIdentifier());
		// Make sure that Tuna exists
    if (!tuna) {
    		throw new Error(`Tuna with id ${tx.tuna.getIdentifier()} does not exist`);
		}
```		
* Next, you have to confirm that the status of the Tuna is CAUGHT (this is to make sure that Tuna that was once sold cannot be sold again):
```
		// Make sure the tuna status is CAUGHT and not PURCHASED
		if (tuna.status !== 'CAUGHT') {
				throw new Error(`Tuna with id ${tx.tuna.getIdentifier()} is not in CAUGHT status`);
		}
```		
* Retrieve the ID of the RestaurantOwner from the Transaction:
```
    // Get restaurantOwner ID
    const restaurantOwnerId = tx.restaurantOwner.getIdentifier();
```    
* Next, verify that the RestaurantOwner exists:
```
    // Make sure that restaurantOwner exists
    const restaurantOwner = await restaurantOwnerRegistry.get(restaurantOwnerId);
    if (!restaurantOwner) {
        throw new Error(`RestaurantOwner with id ${restaurantOwnerId} does not exist`);
    }
```    
* Now, you can update the owner of Tuna:
```
    // Update tuna with new owner
    tx.tuna.owner = tx.restaurantOwner;
```    
* Update status of Tuna: `tx.tuna.status = 'PURCHASED';`
* Update record of Tuna in the Asset Registry:
```
    // Update the asset in the asset registry.
    await tunaRegistry.update(tx.tuna);
```    
* Create the TunaSale event:
```
    // Create a Tuna Sale Event
    let tunaSaleEvent = getFactory().newEvent(NS, 'TunaSale');
    tunaSaleEvent.tunaId = tx.tuna.tunaId;
    tunaSaleEvent.restaurantName = tx.restaurantOwner.restaurantName;
```    
* Finally, emit the event created:
```
    // Emit the Event
    emit(tunaSaleEvent);
}
```

### Lecture 89 - DevelopingQueries

* The queries can be specified under the *queries.qry* file.
* The query getTunaByParticipant will return all the fishes owned by a specific participant in the format of an array of Assets of type Tuna:
```
query getTunaByParticipant {
    description: "List tuna owned by specific 'owner'"
    statement:
        SELECT org.tuna.Tuna
            WHERE (owner == _$owner)
                ORDER BY [catchTime ASC]
}
```

### Lecture 90 - Defining Access Control Rules

* The Access Control rules are defined in the file *permissions.acl*.
* Adding the following rule to the top of the file, allows only the owner of tuna to execute the transaction SellTuna:
```
rule OnlyOwnerCanTransferTuna {
    description: "Allow only Tuna owners to transfer the fish"
    participant(p): "org.tuna.*"
    operation: CREATE
    resource(r): "org.tuna.SellTuna"
    condition: (r.tuna.owner.getIdentifier() != p.getIdentifier())
    action: DENY
}
```

### Lecture 91 - Building and Starting the Business Network

* Once you have created the network, you create a Business Network Archive (BNA) running the following command from the directory that you ran the Yeoman generator: `composer archive create -t dir -n .`
* This creates the file *tuna-network@0.0.1.bna*.

### Lecture 92 - Deploying onto Hyperledger Fabric

* Start by installing the network onto the Hyperledger Fabric peers:
```
composer network install --card PeerAdmin@hlfv1 --archiveFile tuna-network@0.0.1.bna
```
* Then, initialize the chaincode on the Hyperledger Fabric peers:
```
composer network start --card PeerAdmin@hlfv1 --networkAdmin admin --networkAdminEnrollSecret adminpw --networkName tuna-network --networkVersion 0.0.1
```
* This creates a card that you can import:
```
composer card import --file admin@tuna-network.card
```
* And then use to access the business network:
```
composer network ping --card admin@tuna-network
```
* This should show that we can connect to the network.

### Lecture 93 - Testing on the Composer Playground

* Once you have the network deployed, you can access the Composer Playground started in the previous unit by accessing **http://localhost:8080** (or the port :8080 of the Ubuntu Virtual Machine) in a web browser.
* You can also import the .bna files directly in Composer Playground to test the Business Network.

### Lecture 94 - Running the Composer REST Server

* You can also run the REST server to connect to the deployed Business Network and expose resources and transactions. `composer-rest-server -c admin@tuna-network -n never -w true`
* We can now access **http://localhost:3000/** to explore the Composer REST API.

## Section 4 - Joining Hyperledger Composer Community

### Lecture 95 - Learning More About Hyperledger Composer

* The Hyperledger Composer project page provides [links to code, documentation, examples and latests news](https://www.hyperledger.org/projects/composer).
* The full documentation can be found [here](https://hyperledger.github.io/composer/latest/). It is a detailed, well-organized and regularly updated go-to resource if you seek more information on Hyperledger Composer.

### Lecture 96 - Community Meetings and Mailing List

* The community mailing list for Hyperledger Composer can be found [here](https://lists.hyperledger.org/g/composer).
To find out when the next Hyperledger Composer meeting is taking place, navigate to the [Wiki page](https://github.com/hyperledger/composer/wiki/NextCommunityCall).
The full list of meetings within the Hyperledger community is provided [here](https://calendar.google.com/calendar/embed?src=linuxfoundation.org_nf9u64g9k9rvd9f8vp4vur23b0%40group.calendar.google.com&ctz=UTC).

### Lecture 97 - Rocket.Chat and GitHub

* Technical questions are often discussed on the Rocket.Chat (similar to Slack), on the [#composer channel](https://chat.hyperledger.org/channel/composer).
* The official repository for Composer is on [GitHub](https://github.com/hyperledger/composer). At the time this course was created, it features weekly releases, and is the best place to file issues with the code and to add your own technical contributions through pull requests.
* Business Network examples can be found [here](https://github.com/hyperledger/composer-sample-networks).

# Chapter 7 - Hyperledger Indy

## Section 1 - Identity on the Internet  

### Lecture 98 - Identity on the Internet and the Real World  

* The problems with identity on the Internet today come down to a single word - trust. When you are interacting online with someone, do you trust:
	* Is the person you are connecting with online who they say they are?
	* Are the claims they are making true?
* As the famous New Yorker cartoon goes - *"On the Internet, nobody knows you're a dog"*. How do we handle these challenges today?
* When we interact in the real world, we often need to "prove" who we are. To do that, we present evidence that we have about ourselves. What we present varies based on the context of the relationship. When we meet someone socially, we introduce ourselves. When we want to open a bank account, we show documents (attributes) issued by others (driver’s license, utility bill, government ID, etc.) to prove things about ourselves, such as our name, address and ID number (e.g. Social Security Number in the US).
* In turn, those with whom we interact create an identifier for us and check that identifier when we connect again. A person remembers our name and face, and "verifies" them on our subsequent meetings ("Hi Stephen! Good to see you again!"). Our bank creates a card with an ID on it for us to use each time we return to access the bank’s services.
* The same pattern is used online, but there are a variety of problems that occur, some obvious, some a little more subtle. Let’s go through them.

### Lecture 99 - Identifiers (User IDs and Passwords)

* The basic mechanism for knowing who you are on the Internet is the user ID/password combination. You register at a site and get a user ID and set a secret password that only you know, and each time you return you use that to access your account. We all know the problems with user IDs and passwords - we deal with them every day:
	* We have too many to track - I’m aware of more than 700 user IDs I have been given
	* Because we have so many, we often use "easy to remember" passwords that are also easy for others to guess
	* Password recovery mechanisms (question/responses, support desks) provide avenues of attack by hackers
	* Data breaches occur that result in our IDs and passwords being exposed and used - either by the hackers or anyone that buys them
	* We often use the same password on many sites, and once a password is exposed, our account on others sites may also be exposed.
* A common approach to solving the "too many passwords" problem is the use of Identity Providers (IdPs) like Facebook and Google. Smaller sites can use an IdP for authentication (user ID and password verification) and to get basic identity attributes like name and email address.
* We also need to note that while users of websites have IDs for the site, the reverse is not the case - we don’t get an "ID and password" for the site that we can verify each time we connect. This has enabled the "phishing" techniques to become common in recent years, where users are tricked to click a link that takes them to a website that appears to be real, has a similar name, e.g. goog1e.com, but is actually fake, fooling us into reveal our user ID and password - and sometimes even our two-factor authentication code.

### Lecture 100 - Identity Attributes

* On almost every site, we also share other identifiers to use a service - our email and name at minimum, and depending on the nature of the service, additional information (address, credit card information, etc.). With that, we can do the only common business transaction on the Internet - buying things. Buying things has a low enough risk because sellers can generally trace to whom the purchased item is delivered, which deters widespread abuse.
* Conducting higher trust online transactions - such as opening a bank account - is much harder. We have to provide the same information about ourselves as we would in-person. We should be able to just type it in since it is private and (in theory) only we know it. However, much of the information is relatively widely known, either because it is routinely published (e.g. name and address), or because of the many data breaches that have occurred (e.g. government ID number). Even non-identifiers that are used for verification, so-called "shared secrets", such as the value of "Line 150 from 2018 Tax Return" can be fraudulently acquired and used for targeting specific individuals.
* An alternative is to do an online version of the in-person verification - scan and send the source documents. However, scans are very easy to forge and as such are not trusted. We should also add that paper documents used in person are increasingly easy to forge as well. That issue is actually putting at risk the "real world" identity proofing that we mentioned earlier. Verifiers, such as bank employees, have to become experts at detecting the authenticity of documents used for identity proofing.

### Lecture 101 - Additional Identoty Problems

* We’ve talked about a few problems with the current Internet identity approaches already - user IDs and passwords are hackable, and supposedly private information is too well known to be trusted. Here are a few more problems with the current approaches.

**Unwanted Correlation** 

* The use of common identifiers on so many different sites creates what is known as a correlation problem. Correlation in this context means associating without consent information about a single identity across multiple systems. The proliferation of such correlation on the Internet, driven primarily by advertising, has resulted in a massive loss of privacy for Internet users (basically - everyone). A great/horrible example of this was exposed by a data breach at the relatively unknown Florida company, Exactis. The breach was massive covering almost every American and American company (340M records total). However, the content was equally shocking - over 400 data elements per record collected from a number of sites correlating details about each person - their name, age, race, religion, size of family, etc. You can be sure that no one ever agreed to allow Exactis to collect that information. They correlated the data across many "partner" sites to collect a picture of each person - that they in turn sell to anyone willing to pay. To learn more, read "A New Data Breach May Have Exposed Personal Information of Almost Every American Adult".
* Correlation is made possible because of the common identifiers we use online daily. Our email address is the single largest factor, since we share it on almost every site, but there are others. Each time we use the same account name on a different sites creates the possibility of correlation. When we give other identifiers about ourselves - phone number, address, government IDs, etc., firms can correlate that data across sites. Tracking cookies placed by websites and ads enable the linking of IDs across websites. Some of the new GDPR protections are designed to prevent these practices in Europe, but not so in other places. Even then, it is a legal, not a technical solution, and so remains susceptible to bad actors.
* The Identity Providers model is also a correlation point - although in this case one given with consent. The IdP approach trades convenience (fewer user IDs/passwords) for correlation. Since the IdP is used for each login, the IdP can track your use of other sites and thus correlate your online activities - increasing their knowledge of you.

**Centralized Identifiers**

* The vast majority of identifiers we use today are centralized - the identifiers are provided to us and maintained by a centralized entity. That might be the government in the case of our tax ID and driver’s license, or a company for an ID we use to log into a website. A major problem with this approach is that the central authority can choose to take away that identifier at any time. This is of particular concern for those in a minority situation - a critic of a central entity, be it a government suppressing their people or a private company.
* A second concern with central authorities controlling identifiers is that if they are compromised in some way, those identifiers can be used in malicious ways. For example, a hack of a Dutch Certificate Authority (manager of SSL Encryption Certificates) allowed supposedly secure encrypted data going across the Internet to be intercepted and accessed by the hackers. Further, since the identifiers are centralized (held in a central place), if that repository is compromised, it impacts many people.

**Data Breaches**

* Identity-related data is currently of particularly high value, and so large data repositories of identity data are favorite targets for hackers. This includes not only user ID and password data to enable unauthorized access to accounts, but also all of the other information we use to "prove" our identity online - name, email address, government ID, and so on. As noted, the availability of this supposedly private data makes the online use of such data impossible for high value interactions because of the risk that the person typing the data is not its owner.

### Lecture 102 - Summary

* So where does that leave us?
	* User IDs/passwords are the norm, but they are a pain to use, and as a result, are very susceptible to attack. They are the best we have right now, but not a solid basis for trust. Further, IDs are one way - users don’t get an ID from a service they use.
	* Other personal information and identifiers we have that we could otherwise use to prove our identity is not trusted because it’s impossible to tell if the data was actually issued to the person entering it. The many breaches of private identifiers make them impossible to completely trust.
	* Since the identity attributes we could use are not trusted (they are not things only we know), we often have to resort to in-person delivery of paper documents to prove things about ourselves.
	* The identifiers we use are correlated across sites, allowing inferences to be made about us, and exposing information we don’t intend to be shared across sites. This is annoying at the least, and can have catastrophic results in the worst case.
	* Centralized repositories of identifiers and data about the people associated with those identifiers are targeted by hackers because the data has high value. This exacerbates the problem of not being able to trust "personal" data presented online.
	* Centralized identifiers can be abused by those that control those identifiers. For example, they can be taken away from a subject without due process.
* In the next section, we’ll look at the capabilities of Hyperledger Indy to reduce or eliminate these problems.

## Section 2 - Internet Identity with Hyperledger Indy

* The last section introduced a number of challenges with Internet identity as is provided today. In this section, we’ll show how Hyperledger Indy addresses those challenges with a new blockchain-based foundational Identity layer.

### Lecture 103 - Decentralized Identifiers (DIDs)

* A foundational feature of Indy is support for the emerging W3C standard for Decentralized Identifiers (DIDs). DIDs are globally unique identifiers that are created by their owner, independent of any central authority. Each DID has associated with it one or more public keys created by the DID owner (and the owner holds the corresponding private keys), and one or more endpoints - addresses where messages can be delivered for that identity. A DID can be uniquely resolved (like a URL) to return the data (public keys and endpoints) associated with the DID. An example of a DID is displayed below.
* Indy uses DIDs to establish connections between two identities, such as a user and a service’s website, so that they can securely communicate. Further, the expectation is that an entity - e.g. you - will have many, many DIDs - one for each relationship you have with another entity. Think of each DID like a user ID/password pair, but one that is backed with strong cryptography in the form of public/private keypairs. As well, note that both sides of a relationship provide a DID for the other to use to communicate with them.
* The image below show three entities, Alice, Bob and a Bank that both Alice and Bob use. For each entity, we see the various DIDs they have created for their relationships. We've also highlighted the DIDs that they have exchanged with each other - Alice's for Bob, Alice's for the Bank, and so on.
* **Creating and Using DIDs** : Here’s an example of how DIDs are used: A user registers for a service’s website by creating and giving the service a new, never-used-before DID, and receives back from the service the same thing - a new, never-used-before DID created by the service. Each records the "relationship" DIDs so that when one wants to communicate with the other, they have an endpoint to send the message, and a public key to end-to-end encrypt the message. Later, when the user returns to the website to login, the user and the service exchange encrypted messages to confirm that each holds the private key to decrypt the messages. On completion, the service knows it’s the user because the user used their DID, and the user knows it’s the service because the service used its DID. Neat - we’ve already addressed one of the challenges raised with today’s Internet identity - two-way verification!

### Lecture 104 - Agents and Wallets

* With so many DIDs floating around, it's clear that memory and bits of paper are not enough to manage all the DIDs a person creates or receives. Indy uses the term Agent to mean the software that interacts with other entities (via DIDs and more, as we'll find out), and the term Wallet as a data store for the DIDs and related information (including private keys and more). For example, a person might have a mobile Agent app on their smart devices, while an organization might have an enterprise Agent running on a cloud server. All Agents have a secure Wallet for storing identity data.
* For those familiar with a password manager like 1Password or LastPass, a personal Agent Wallet is similar - there is a name for each relationship and associated data. However, unlike password managers that use things like your copy/paste clipboard for user IDs and passwords and "screen-scrape" applications and websites, Agents communicate directly with Agents to accomplish identity-related tasks.
* The picture below is an example of some communicating Indy Agents. The Edge Agents are handled by the identity owners themselves - in this case a consumer and an enterprise. The cloud Agents facilitate the messaging by, for example, providing a permanent endpoint for a device that may or may not be online at the time messages are being received.

### Lecture 105 - Indy Public Ledger

* The term "decentralized" is a hint that Indy uses blockchain technology. The image presented on the previous page shows how the Agents send requests to the ledger to read and write DID (and other) information. An identity (e.g. a person, organization or thing) creating a DID can publish that DID to an Indy immutable public ledger. The "DID" (a globally unique string) can then be looked up ("resolved") on the public ledger, and the information associated with the DID (called the "DID Doc") return the public key(s) and endpoint(s) associated with the DID. The private keys associated with the public keys are held by the owner of the DID in their Wallet. As long as the private keys are protected (a non-trivial, but manageable challenge), the DID cannot be used by anyone else. Using a decentralized system based on blockchain technology empowers users to securely publish their DIDs without a central authority. For the more technically inclined, the core of Indy is what is know known as a [Decentralized Key Management System (DKMS)](https://github.com/WebOfTrustInfo/rebooting-the-web-of-trust-spring2017/blob/master/topics-and-advance-readings/dkms-decentralized-key-mgmt-system.md) - a reliable way to share public keys without a central authority.

### Lecture 106 - How DIDs Help

* DIDs address a whole lot of the problems we talked about in the last section with Identifiers:
	* Users define their own DIDs and give that DID to a service to use in identifying them. This addresses the problems created by centralized identifiers - DIDs are controlled by the user.
	* Agents and Wallets act like password managers, making it easy for users to manage their access to sites and services.
	* Since a user uses a different DID for each service, their identity cannot be correlated across services.
	* Since the user and service can communicate using the DIDs, there is no need for a user to provide an email address - the primary mechanism used today for correlating users.
	* The service gives the user a DID for the service as well as the other way around, so the user can be certain they are talking to the service.
* We’re part way through the solution - DIDs that are controlled by their owning entities and shared to establish relationships between entities. But how does each party know who it is that created and controls the DID? That’s where the next part of the Hyperledger Indy story comes in - Verifiable Credentials.

### Lecture 107 - Verifiable Credentials

* Indy also supports a second exciting, emerging W3C standard - Verifiable Credentials (VCs). It enables a trusted way to provide identity attributes about ourselves.
* Credentials are things like driver’s licenses, passports, or university degrees that are given to us from an issuing authority that we can use to show to others when needed. VCs are digital equivalents of paper credentials that are cryptographically processed such that when we show ("prove") the claims (data elements from the credentials), the receiver ("verifier") can be certain:
	* Who issued the claims
	* That the claims were issued to the identity presenting them
	* That the claims have not been tampered with (forged)
	* That the claims’ credential has not been revoked by the issuer.
* As the image below shows, the data flow for Verifiable Credentials is the same as with paper documents - issuers give Verifiable Credentials to the holder, and the holder can prove them to verifiers at any time.
* The proof requests and proofs in Indy are transactions that occur between the holder of the VC and the verifier. The issuer of the VC is not involved in the proof process - a very important attribute of the VC model. We don’t want, for example, the government to know each time we use our driver's license to prove our age!
* Verifiable Credentials and their use closely mimics that of the real world. VCs take that model and put it online, in a trusted manner.

### Lecture 108 - Selective Disclosure and Zero Knowledge Proofs (ZKP)

* Hyperledger Indy provides advanced features in the proving of claims. Specifically, that the claims can be selectively disclosed, meaning that just some data elements from a credential are provided in a proof. In addition, [zero-knowledge proofs](https://en.wikipedia.org/wiki/Zero-knowledge_proof) (ZKPs), a piece of cryptography magic (that we won’t detail here - but it’s fascinating) allow proving a piece of information without presenting the underlying data. A very useful example of both selective disclosure and a ZKP supported in Indy is a proof that a person is older than a given age based on a the date of birth in a VC driver's license without disclosing any other information, including name or date of birth. The image below demonstrates how that might look in an Indy-enabled app at a pub.
* The verifier (a bartender) can confirm:
	* The issuer was the appropriate authority
	* The picture shows the same person presenting the Verifiable Credential
	* The person is old enough to drink in the pub (the check mark).

### Lecture 109 - Using Verifiable Credentials

* The ramifications of Verifiable Credentials are dramatic, especially when combined with Indy’s advanced VC features. Here are just a few examples of how they can be used:
	* A bank trusting only a SSN (government ID) that was issued as a VC to the holder by the appropriate government agency. Having the numbers of the ID without digital proof will have no value - reducing the value of and impact of data breaches.
	* An employer digitally confirming the education credentials of a potential employee. The employer can programmatically investigate the issuer of the credentials to determine if they are an appropriately accredited institution. Phony degrees become useless.
	* A person connecting with a new financial advisor can verify the credentials of the advisor with appropriate government regulator and the Better Business Bureau.
	* Rather than typing in the same information over and over at each service (e.g. address), a person can provide a VC containing their address.
	* A professional can prove online they have both current membership in their industry organization, and appropriate practice insurance.
* All of these transactions are done today with increasingly unreliable paper transactions, frequently requiring face-to-face interactions. With VCs, the transactions are fast, secure and even more reliable. Further, since the subject (you!) holds the VC, you only share them as necessary to support the interaction you are trying to accomplish. The issuer of the credential has no knowledge of how and when you are using the credential. We don’t want to notify the government every time our driver’s license is used to confirm information about us.
* Blockchain plays a key role in Indy with issuing of Verified Credentials and proofs. Since the VCs contain private information, the VCs themselves are not stored on the blockchain - they go in the Wallet of the VC holder (see image below). However, information necessary to use the VCs - the schema, the DID of the Issuer and information for proving non-revocation are all stored on the Indy blockchain. This conveniently and securely makes the information to interpret VCs available for identities to use in exchanging credentials and claims while preserving in the private wallet of the holder the personal information.
* VCs extend the capabilities of DIDs to include features needed for building trust on the Internet:
	* Personal information and identifiers provided to verifiers as claims in VC-based proofs can be trusted - perhaps more so than paper documents.
	* Proofs extend paper documents capabilities by adding real time access to revocation status (without contacting the issuer), selective disclosure, and zero-knowledge proofs.
	* Personal data is held by its owner (you!), not in identity repositories, reducing the number of high-value data targets. This also reduces the liability of the service currently holding that repository.
	* Plain data - strings of characters that lack proof of being issued to you - will fall in value when they are no longer accepted online. This loss of value reduces the incentive for hackers stealing private data.

### Lecture 110 - Trying It Out

* IBM extended Hyperledger Indy software elements created through a collaboration between the Province of British Columbia and the Government of Canada and built a demo showing a person, Alice, using a series of Verifiable Credentials to:
	* Get a transcript from her college (Faber)
	* Apply for (and get!) a job at Acme Corp using her transcripts
	* Get proof of employment from Acme Corp
	* Use her proof of employment to apply for a loan at Thrift Bank.
* For those that just want to see all of this in action, IBM (a Hyperledger member and contributor to Indy) has posted a video of the sequence on [YouTube - "IndyWorld Demo by IBM"](https://www.youtube.com/watch?v=cz-6BldajiA).

### Lecture 111 - Privacy

* Hyperledger Indy is all about privacy. Well-known in the identity community is the concept of Privacy by Design, a series of principles first described by Canadian Internet researcher Dr. Ann Cavoukian, and now held as a standard by privacy experts worldwide. Hyperledger Indy very much adheres to the Privacy By Design principles. We’ve mentioned most of the privacy enhancing features of Indy in the previous two sections, so we’ll just list them here:
	* Decentralized Identifiers (DIDs) created and controlled by the owning entity
	* The use of DIDs for each relationship, preventing cross-service correlation
	* Peer-to-peer, end-to-end encryption from message creator to receiver
	* Verifiable Credentials (VC) held by their owner and used only when necessary
	* Selective disclosure of VC data - exposing only the data necessary
	* The use of VCs without the need to contact the issuer.

### Lecture 112 - Self-Sovereign Identity

* A final but very important term we’ll include in this introduction to Internet identity is self-sovereign identity (SSI). The term, introduced by Christopher Allen in 2016, is the concept that people and businesses can hold their own identity data and share it as it is needed without relying on a central authority. All of the features of Hyperledger Indy we’ve talked about embody SSI concepts. As Drummond Reid, a guru in Internet identity and the Chief Trust Officer of Evernym, Inc. (the company that originally created Indy) states, SSI is a:

*"lifetime, portable identity for any person, organization or thing that does not depend on any authority and can never be taken away"*.

* The creators and maintainers of Hyperledger Indy strive to ensure that the software embodies the concepts of SSI now and in the future.

## Section 3 - Hyperledger Indy in Context

* As we mentioned in the introduction to this chapter, Hyperledger Indy is a special purpose blockchain implemented specifically for identity on the Internet - enabling certainty about who is talking to whom in a digital transaction. And, as we find in other chapters of this course, other Hyperledger projects - Fabric, Sawtooth and Iroha - can be used for a wide variety of applications, from shared ledgers to IoT devices, to supply chains and many more. In this section, we will explore the connection between the projects - other than them all sharing the Hyperledger name.
* We’ll also look at two other aspects, Indy and blockchain. First, since Indy is designed for a special purpose, how does that affect the underlying blockchain implementation? Does it still have the same components of other blockchains? Second, unlike the other Hyperledger frameworks we’ve been studying, Indy is intended to be deployed in the public, for all to use. As such, there is a non-profit, the Sovrin Foundation, that is associated with Indy and has deployed a global instance of an Indy blockchain. At the end of this section, we’ll take a look at the Sovrin Foundation and the Indy-powered Sovrin network.

### Lecture 113 - Using Indy for Identity with other Blockchains

* Each of the Hyperledger projects began independently and on reaching a certain level of maturity and definition, came under the Hyperledger umbrella. Once inside Hyperledger, each project has continued to grow independently, but has also looked across at the other projects to find synergies. Indy has the potential to add a really important component to the other Hyperledger frameworks - identity. Each of the other frameworks need trusted identity. The participants using each of the other Hyperledger frameworks are executing transactions with one another and to do that in a trusted way, each participant must know with whom they are dealing. The initial implementations leave identity up to the specific deployment, and most instances use "traditional" mechanisms for identity - mechanisms that have the same issues that Indy is solving. Wouldn’t it be great if out-of-the-box they had Indy’s identity capabilities? Hyperledger frameworks are looking to see how they might share some of the capabilities that exist with Hyperledger Indy.

### Lecture 114 - Indy’s Blockchain Algorithms

* Much of this course has focused on the underlying algorithmic components of blockchain and the specific algorithms used by the Hyperledger framework implementations. Although Indy is designed only for identity, it is blockchain-based and so has those same algorithmic components. Let’s look at Indy from the perspective of the concepts presented in Chapter 1 of this course: the type of blockchain it is and what Indy uses for a consensus algorithm. In a later section, we’ll look more at the types of transactions that go on the Indy ledger.
* Before diving into those details, we’ll quickly cover some other blockchain attributes covered in Chapter 1. As with all blockchain implementations, the Indy ledger is immutable - write once and never update. Since Indy is focused only on identity, it does not support the concept of assets being exchanged, nor any sort of smart contract capability. However, a related capability that is currently being added to Indy is support for a pluggable implementation of a payment token. The token won’t be used to enable a general-purpose smart contract capability, but rather to support payments for certain network operations. For example, creating an identifier or proving information about an identity. Such payments may be used to prevent Denial of Service (DOS) attacks and might serve as a mechanism for funding an instance of the network. The term pluggable means that Indy itself will only implement minimum reference token functionality and invoke code created for a specific running instance of Indy. Others can add their own token implementation.

### Lecture 115 - Type of Blockchain

* As we covered earlier in this course, there are several different types of blockchain systems characterized along two dimensions: access and validation. Recall that Bitcoin and Ethereum are public permissionless networks - anyone can access them (public) and anyone can participate in the validation process (permissionless). Similarly, the Hyperledger frameworks (Fabric, Sawtooth, Iroha and Burrow) are (primarily) used for private/permissioned networks, limited to who can access them (private) and who can participate in the validation process (permissioned).
* As shown in the chart below, Indy falls between these two models. Indy is designed to be operated such that everyone can see the contents of the blockchain (public), but only pre-approved participants, known as Stewards, are permitted to participate in the validation process (permissioned). Note that although Indy is designed to be run as a public network, an instance of Indy (or any other public blockchain) could be run as a Private network accessible only to those using the network. Sawtooth can also be run as a public network.
* The ramification of Indy being designed to be public puts a significant constraint on what data can be put on an Indy blockchain. Specifically, only public data can go on the blockchain - no other data, even if it is encrypted. That last part about encrypted data might not be obvious. If the data is encrypted it can only be accessed by those with the decryption key, shouldn’t we be able to put any data safely on a public blockchain? Well, that might be true — today. However, Indy is being built to last from decades to generations. What happens if an encryption algorithm used today is broken sometime in the future? Since the data on the blockchain is open to everyone to see and is immutable, encrypted data that can be easily decrypted becomes public information. The Indy designers don’t want that, hence the rule - no private data on the blockchain. Later in this chapter, we’ll cover "What goes on the ledger?" - a favorite question from everyone getting up to speed on Indy. Did you catch that part about no private data on the blockchain? Good!

### Lecture 116 - Blockchain Consensus Algorithm

* As with all blockchain implementations, Hyperledger Indy uses a consensus algorithm to decide the contents of the next block added to the chain. Specifically, Indy uses Plenum, an implementation of the Redundant Byzantine Fault Tolerance (RBFT) algorithm. Plenum achieves similar performance to other BFT algorithms in ideal conditions (no faulty participants), but its performance degrades far less than other algorithms (on the order of 3% versus up to 78% for others) when faults occur in the network. As well, underlying Indy’s consensus algorithm is a secure and robust messaging system amongst the nodes of the network. This improves the overall security of Indy. The Plenum implementation has found to be useful enough to be separated out from the core Indy code base into a separate open source project that is used by Hyperledger Indy (and can be used by other blockchain implementations).
* Indy also implements a novel deployment of Stewards - the nodes of the network that have permission to participate in the validation process. Since Indy is designed to be a global public network, an instance will have many available nodes located around the world - more nodes available than can be effectively used in the validation process. The validation process needs enough Stewards to be robust in the face of faults, but not too many as to degrade the performance in reaching consensus. Indy’s solution is to have an optimal subset of Stewards as Validators nodes - actively participating in the Plenum consensus algorithm, and the rest as Observer nodes, tracking the growing Blockchain, serving reads (thus offloading that work from the Validators) and ready to called on to be Validators should they be required. The image below from Sovrin (covered in the next section) shows the division of Validator nodes (those currently participating in writing to the ledger) and the Observer nodes (read-only nodes, but ready to become validators if needed).

### Lecture 117 - Hyperledger Indy and Sovrin

* A name you will hear a lot in discussing Hyperledger Indy is Sovrin and the[ Sovrin Foundation](https://sovrin.org/). Hyperledger Indy is the open source software project hosted by Hyperledger and The Linux Foundation that implements the decentralized identity standards. The Sovrin Foundation is a global non-profit that has deployed the Hyperledger Indy code on a (growing) number of nodes to create a running Public Permissioned Hyperledger Indy Blockchain instance. To understand the goal of the Sovrin Foundation, think of the Sovrin instance of Indy as the identity equivalent to the Domain Name System (DNS), which has enabled the global routing of data on the Internet since 1985.
* The Sovrin Foundation provides the three foundational components of the Sovrin Network in the form of a BLT (not the sandwich):
	* Business - the Sovrin Trust Framework
	* Legal - a series of legal agreements signed by the Sovrin Network participants
	* Technical - the underlying software of the Sovrin Network (Hyperledger Indy).
* All three parts are necessary to enable a global, trusted system for identity. The need for legal agreements and a sound technical foundation are fairly obvious, but what is a trust framework?
* Trust frameworks are common in the digital identities world, but are also used in other contexts (with other names, such as "operating regulations" and "operating policies"). In all cases, they define how to govern multi-party systems where participants desire the ability to engage in a common type of transaction with any of the other participants, and to do so in a consistent and predictable manner. A trust framework enables an organization to count on the business and/or technical processes carried out by another organization. In many cases, trust frameworks have been able to work and most importantly, scale. Common examples include credit card systems, electronic payment systems and the internet domain name registration system, which all rely on a set of interdependent specifications, rules, and agreements.
* An Identity Trust Framework defines the rules for interactions between organizations for handling identity, authentication (who you are), and authorization (what you are allowed to do). The Sovrin Trust Framework defines those rules for the organizations using the Sovrin Network.

### Lecture 118 - Elements of the Sovrin Foundation

* So what is Sovrin? Sovrin is a single, global instance of Hyperledger Indy. Each node is operated by a Sovrin Steward, an organization (company, government, university, etc.) that has agreed to a legal agreement that defines how they will operate their node (minimum hardware, network access, monitoring, security, maintenance, etc.) within the rules defined in the Sovrin Trust Framework. As of August 2018, Sovrin Stewards include banks/credit unions, universities, law firms, technology companies and more, operating in 14 countries. The Sovrin Foundation, through the Trust Framework, provides governance for the Network, the use of nodes and coordinating the software upgrades (including new features) to the nodes. The Foundation includes a Board of Trustees to oversee the business and legal aspects of the Network and a Technical Governance Board.
* And of course, the Sovrin Network has users. Some users, called Trust Anchors (initially, the Trustees and the Stewards) are entrusted - through reputation, legal agreements, and their adherence to the Sovrin Trust Framework - to write data to the public ledger for themselves and others. The remainder of the participants in the system (Identities) use the Steward-operated nodes to read and (via Trust Anchors) to write to the Sovrin public ledger. A key capability of Trust Anchors is that they can "anoint" other Identities known to them to be Trust Anchors - provided those Identities agree to the Sovrin legal agreement and the Trust Framework. It is through this "web of trust", that the capacity of the Network scales.
* With a global network in place, Sovrin can be used to solve the Internet identity problem. Users can create Decentralized Identifiers (DIDs), use those DIDs to communicate securely with others, and use Verifiable Credentials and Claims to prove things about themselves such that they can execute trusted digital transactions.

## Section 4 - Running Hyperledger Indy

* In this section, we’ll walk through an example of running an Indy ecosystem on Docker - an instance of the Indy public ledger and a series of Indy Agents that can message one another and share Verifiable Credentials. We’ll also walk through the components of Indy, so that you have an idea of these components and where to look to dig deeper into Indy.

### Lecture 119 - Demonstration Overview

* In this demonstration, you will start a private instance of the Indy blockchain and several web-based Agents (implemented in Node.js), and then you’ll use the features of the Agents to connect and exchange messages and Verifiable Credentials amongst the Agents. The Agents are built on top of the Indy-SDK, the client code part of the Hyperledger Indy Project. The picture below shows the components of the demonstration.
* The demo uses the same storyline as the official "Getting Started" guide for Indy, but with Agents that have a browser to drive the user interactions rather than the command line. If you do want to try the official "Getting Started" guide, you can find a link to the latest version on the [Hyperledger Indy Wiki](https://wiki.hyperledger.org/projects/indy) page.

### Lecture 120 - Running the Demonstration

*Please be aware that the hands-on part of this chapter is available on GitHub.*

* The instructions for building and starting the demonstration can be found in the [GitHub repo for the demonstration code](https://github.com/hyperledger/education/blob/master/LFS171x/indy-material/nodejs/README.md). Once you have the demonstration code downloaded to your system and running, [click here](https://github.com/hyperledger/education/blob/master/LFS171x/indy-material/nodejs/AgentDemoScript.md) to see the instructions for walking through the story of Alice, an alumna of Faber College, getting her official college transcripts from Faber and then using her transcripts while applying for a job at Acme Corp. Spoiler alert - she gets the job!
* If you just want to see a screencast of the demo without running it all yourself, [click here to go to GitHub repo instructions](https://github.com/hyperledger/education/blob/master/LFS171x/indy-material/nodejs/README.md). You'll find a link near the top of the instructions that starts the screencast.
* Use the edX Forums to ask questions about the demo. Want to go deeper into Hyperledger Indy? Use the resources listed in the next section - "Joining the Hyperledger Indy Community" - to dive in!

### Lecture 121 - What Goes on the Blockchain

* A frequent question that comes up with those new and even those not so new to Hyperledger Indy is: "What goes on the blockchain?". The technically adventuresome can take a look at the data on your demo instance of Hyperledger Indy.
* While the demo is running, you can go to the URL *http://localhost:9000*, click the link "Domain (pretty)" in the "Ledger State" section, and see the raw data on the ledger. If you scan the data, you will see three types of transactions:
	* **DIDs** : Those are the decentralized identifiers created by each participant in the demo (Alice, Faber, etc.). Look for entries with "role" and "verkey" in the data. You might even recognize the DIDs on the ledger with the DIDs on the demo web pages.
	* **Schema** : Entries that define the data elements (the claims) that will be part of a Verifiable Credential. Look for the name of the schema, such as "Government-ID".
	* **Credential definitions** : Entries that are created by a credential issuer (like Faber) using a specific schema and (optionally, and not in this demo) a revocation registry. Credential definitions have a private key for each claim (and more), so look for entries with big long strings and references to schema claim names, e.g. "tax_id".
	* **Revocation registries** : Entries that give an issuer a way to revoke issued credentials in a non-correlatable way. In this demo, we are not using revocation capabilities, so you won’t find any on the ledger.
* Most importantly, there are no credentials on the ledger, and no private data of any kind. In fact, the only data on the ledger is not just data that’s not private, but data you expressly want others to know. All private data is exchanged between identities directly and stored in their secure Wallets. The data on the ledger is used to prove things about that private data such that it can be trusted.

### Lecture 122 - The Hyperledger Indy GitHub Repos

* As of August 2018, there were nine official Hyperledger Indy GitHub repos. To check the current status of the repos that make up Hyperledger Indy, go to the Hyperledger Indy Project Wiki page. Of those nine, six are important to describe here:
	* indy-node
	* indy-sdk
	* indy-plenum, indy-crypto
	* indy-agent
	* indy-hipe.
* We will discuss them in more detail on the next pages.
* The other three are not (currently) particularly important to the general community.

**indy-node**

* indy-node is (mostly) the Python code that implements the Indy public ledger - the set of permissioned instances (nodes) that accept and process public ledger read and write requests from Indy clients (usually called Agents). In a test network such as we used for the demonstration, the network can be very small (a minimum of four nodes) and each node runs the same Docker image. In the Sovrin Foundation’s live, global Hyperledger Indy network, there are many more nodes, and each Steward (permissioned node operator) compiles and configures their own version of indy-node. The latter is an important element of diversity in the network - if every node was running an identical version of the software on the same platform, a bug that broke the common setup would bring down the entire network.
* The acceptable number of concurrent node failures in an Indy network is an important parameter of Indy’s Plenum consensus algorithm. A Plenum network that can survive F node failures must have at least 3F+1 nodes. Thus, a minimum network that can survive the loss of one node (F=1) must have the four nodes we used for the demonstration. A network capable of ten failed nodes, must have at least thirty one nodes - the bigger the F, the more nodes, the more reliability from faults. However, adding too many nodes to the network is also problematic - the more nodes, the longer it takes to reach consensus. As discussed earlier, Sovrin addresses that issue by having many Steward (nodes), but only have a subset of them active as validators contributing to the consensus algorithm. The rest are Observers that support only reads of public ledger data, but that can be activated as validators when node failures are detected.

**indy-sdk**

* The indy-sdk repo contains the code that allows a piece of software - an Agent - to interact with the public ledger and to keep track (in a Wallet - a specialized data store) of the keys and other identity-related data. The indy-sdk consists of one core component (written mostly in Rust) that compiles to a “c-callable” library (called libindy) and a number of language specific "wrappers" for the library. A “c-callable” library means that the library components can be called from the majority of languages, eliminating the need for an implementation in each language. The wrappers, available (as of September 2018) in Python, Java, C# (.NET) and Node.js, allow the creation of a Indy agents in each of those languages.
* As mentioned, the indy-sdk implements a Wallet that is used to store the Indy data collected by an identity on an Indy network - DIDs, private keys, Verifiable Credentials and more. The indy-sdk implements a default implementation of the Wallet, and is pluggable - meaning a capable developer can implement a replacement Wallet. The default Indy Wallet is based on the open source SQLite database.
* Another key part of the indy-sdk is the test suite that is automatically executed with each update to the repo. While it’s comforting to know the test suite is executed (and updated) with each change, a very useful aspect of the suite for those new to Indy is that the tests are working code that can be used to understand how the indy-sdk works. Not sure what exactly are the parameters to a specific Indy call? Check out the test suite and you’ll find a working instance to study.

**indy-plenum**, **indy-crypto**

* One of the first changes to Indy when it was added to the Hyperledger community was to extract some key elements of the Indy codebase into separate repos. Both the Plenum consensus algorithm and the cryptography library used in Indy were put into separate repos, so that they can be used by other Hyperledger projects and other blockchain implementations. By making them independent of the other parts of Indy, they can evolve independently to support additional use cases.

**indy-agent**

* The indy-agent repo contains reference Indy Agents - starter kits and examples of Indy Agents built based on best practices on top of the indy-sdk. While the indy-sdk contains the basic building blocks of an Indy Agent, the reference Agents in this repo demonstrate good approaches to using those basic building blocks. Also planned for inclusion in the indy-agent repo is an Indy Agent compliance suite - a mechanism for testing an agent and a set of tests that show an Agent is interoperable with other Indy Agents. Interoperability will be crucial as the use of Indy grows, and more organizations add Indy capabilities to their infrastructure.
* In the demonstration we did earlier in this section, we used a snapshot of the Node.js reference Indy Agent. To see how the Node.js Indy Agent has evolved since we made our snapshot, check out the indy-agent repo. Much of the work on the Node.js Indy Agent was done by a team at Brigham Young University (BYU).

**indy-hipe**

* The indy-hipe repo is a set of "Hyperledger Indy Project Enhancements" (you know, HIPEs) - documents that describe Hyperledger Indy features, approaches to interoperability and other things that have or will make Indy better. It’s a great place to learn the details of some of the key features of Indy: the Wallet implementation, revocation and more.

### Lecture 123 - Related Project: The Verifiable Organizations Network (VON)

* The [Verifiable Organizations Network (VON)](https://von.pathfinder.gov.bc.ca/) is a project started by the Government of British Columbia (Canada) whose goal is to make it easier for organizations (and the people running organizations) to do business on the Internet through the use of Verifiable Credentials issued by trusted entities. VON is an open source project and includes a number of open source repos that can be used (and enhanced) by others - particularly governments interested in issuing and using Verifiable Credentials. Initial VON proofs of concepts and applications were built using Hyperledger Indy.
* In our demonstration, the open source "VON-Network" was used as an easy way to spin up the Indy public ledger and a VON-sourced Docker image provided the basis for the Indy Agents.

## Section 5 - Joining the Hyperledger Indy Community

* Hyperledger Indy is an open source project, where ideas and code can be publicly discussed, created, and reviewed. There are many ways to join the Hyperledger Indy community. The next few pages highlight some of the ways to get involved, either from a technical standpoint, or from an ideas/issues-creation perspective.

### Lecture 124 - Getting Started

* The starting point for all things related to Hyperledger Indy is the [Project’s Hyperledger Wiki](https://wiki.hyperledger.org/display/indy/Hyperledger+Indy)page. From there you can find a little bit about the project directly, and a whole series of links to documents, data and details about Indy, including things like the Indy code and documentation repositories, project management information, collaboration tools, community meetings and more.
* The Hyperledger Indy community has a number of places where the community comes together to move the project forward - with more resources being added as the community grows. For specific details and links to these resources and events, please see the the [Hyperledger Indy Wiki](https://wiki.hyperledger.org/display/indy/Hyperledger+Indy) page. Here are some examples:
	* **Weekly meetings** : Weekly community meetings that cover a variety of topics such as core indy-node and indy-sdk development, Agent implementations, public sector uses for Indy and so on. The weekly Hyperledger Indy Working Group call is the best place to stay up to date on the status of the project.
	* **Chat** : Indy-related channels can be found on the Hyperledger Chat where all involved in Indy discuss, request help and provide help. There are a number of core channels and, as needed, new channels are added to discuss important issues in moving Indy forward. All Hyperledger Indy channels begin with #indy. The channel to start with is the #indy channel.
	* **Mailing list** : An Indy Mailing list is used to keep the entire community updated on happenings in the community, and to foster discussion about technical issues related to Hyperledger Indy.
	* **GitHub Repos** : The Hyperledger Indy codebase is on [GitHub](https://github.com/hyperledger) and is available for reviewing, forking and most importantly, contributions. A list of the current Hyperledger Indy repos (as of September 2018) is provided in the earlier "Getting Started with Hyperledger Indy" section. See the Hyperledger Indy Wiki to find the latest information on the repos.
	* **Indy meetups** : There are many in-person events (conferences, hackathons, meetups, etc.) related to Indy that happen throughout the year. Some are specific to Indy, while others are larger Hyperledger or Internet identity events. Hyperledger Indy maintains a calendar of all Hyperledger meetings, while other meetings can be found through discussions on Chat. You can also locate Hyperledger-specific meetups at the Hyperledger Meetup website.

# Chapter 8 - Introduction to Hyperledger Sawtooth

## Section 1 - Addressing Illegal, Unregulated, and Unreported Tuna Fishing (Demonstrated Scenario)

### Lecture 125 - Defining Our Actors

* Sarah is the tuna fisher who sustainably and legally catches tuna.
* Tuna processing plant processes and bags the tuna after they have been caught.
* Regulators verify that the tuna has been legally and sustainably caught.
* Miriam is a restaurant owner who will serve as the recipient in this situation.
* We will be describing how tuna fishing can be improved starting from the source, tuna fisher Sarah, and the process by which her tuna ends up at Miriam's restaurant.

### Lecture 126 - Featured Hyperledger Sawtooth Elements

* Hyperledger is a modular platform for building networks and running distributed ledger applications. Sawtooth simplifies application development by separating the core system from the application level. Application developers can specify the business logic for their applications, using the programming languages of their choice, without needing to know the underlying design of the core system.
* **Sawtooth validators** validate transactions. Validators are responsible for combining batches of transactions into blocks, submitting them to the ledger, and approving valid blocks according to the network's consensus algorithm.
* **Sawtooth applications** are distributed applications, such as smart contracts, that are separate from the core framework. An application provides a transaction family to define the operations that can be applied to transactions, and the meaning of the transaction contents. An application consists of both a transaction processor (the server-side logic) and one or more clients (for use from Web, CLI command line, or mobile applications).
* **Transaction processors** provide server-side business logic. Most nodes run several transaction processors, one for each specific use case or application. Each node in the Sawtooth network must run an identical set of transaction processors.
* **Batches** are clusters of transactions that are submitted together. A batch can contain a single transaction or several related transactions that are all committed to state together. If one transaction fails, the other transactions in that batch also fail.
* **The network layer** is responsible for communicating between validators in a Hyperledger Sawtooth network, including performing initial connectivity, peer discovery, and message handling.
* **Global state** contains the current state of the ledger and a chain of transaction invocations. The state for all applications running on the network is represented on each node. The process of transaction validation on each node ensures that the same transactions result in the same state transitions, and that the resulting ledger data is the same for all participants in the network. The state is split into application-specific namespaces, which allow flexibility for application authors to define, share, and reuse global state data between transaction processors.
* **Proof of Elapsed Time (PoET)** is a consensus algorithm in Hyperledger Sawtooth that implements time-based consensus, which reduces energy consumption on large distributed networks when compared to other algorithms such as Proof of Work.

### Lecture 127 - Why Sawtooth?

* Miriam is a restaurant owner looking to source high quality tuna, that have been caught responsibly. Whenever Miriam buys tuna, she cannot be sure whether she can trust that the tuna she is purchasing is legally and sustainably caught, given the prominence of illegal and unreported tuna fishing. Luckily, Hyperledger Sawtooth can help!
* Hyperledger Sawtooth is ideal for this scenario because of its ability to track the provenance and journey of an asset (in this case, tuna). The ability to batch transactions together allows for all tuna within a catch to be entered as a whole. The distributed state agreement, novel consensus algorithm, and decoupled business logic from the consensus layer allow Miriam to be confident that she is buying tuna that has been legally caught.

### Lecture 128 - The Supply Chain

* Hyperledger Sawtooth is extremely scalable and able to withstand high throughput of data, which makes it a great option for production supply chain scenarios.
* We will start with Sarah, our licensed tuna fisher, who sells her tuna to multiple restaurants. Sarah operates as a private business, in which her company frequently makes international deals. Through an application, Sarah is able to gain entry to a Hyperledger Sawtooth blockchain network comprised of other fishermen, as well as processing plants, regulators, and restaurant owners. Sarah, as  well as the processing plants, have the ability to add and update information to this ledger as tuna passes through the supply chain, while regulators and restaurants have read access to ledger records.

### Lecture 129 - The Tuna Asset

* With each catch, Sarah records some information about each individual tuna, including a unique ID number, the location and time of the catch, its weight, and who caught the fish. For the sake of simplicity, we will stick with these data attributes. However, in an actual application, many more details would be recorded, from toxicology, to other physical characteristics, such as the temperature of the tuna.
* These details are saved in the global state as key/value pairs based on the specifications of a Sawtooth application, while the transaction processor allows Sarah's application to effectively create a transaction on the ledger. Please see the example below:
```
var tuna = {
     id: ‘0002’,
     holder: ‘Sarah’, 
     location: { latitude: '15.623036831528264', longitude: '-158.466796875'}, 
     when: '20170635123546', 
     weight: ‘58lbs’ 
}
```

### Lecture 130 - Recording a Catch

* After Sarah catches her tuna and records data for each tuna, she is able to treat a haul of tuna as a single batch of transactions. As a reminder, a batch is a cluster of transactions that are committed to state together. Using a batch, Sarah is able to record many tuna together, while still being able to specify data for each tuna. If one of the tuna transactions is invalid, the entire shipment is invalidated; that is, no tuna within the batch of tuna is validated.

### Lecture 131 - Reaching Consensus

* After a batch of many transactions is submitted to the network, the network’s consensus algorithm chooses a node to publish this batch as a block on the ledger (possibly along with other batches). If the Proof of Elapsed Time consensus algorithm is used, the validator with the shortest wait time publishes the transaction block. (We'll discuss this in more detail later in the course.) The transaction block is then broadcasted to the publishing nodes.
* Each node within the network receives the transaction block, and validators verify whether the transaction is valid or not. If the transaction is validated, the global state is updated.
* Hyperledger Sawtooth provides full distributed state agreement, where every node in the system has the same understanding of information. As the supply chain matures, the data stored remains consistent across the network.
* With the global state adjusted, the processing plant, the regulator, and Miriam are able to see the details of the catch and who the current holder is, thus keeping the supply chain transparent and verifiable.

### Lecture 132 - Other Actors in the Supply Chain

* Before Sarah's tuna can reach Miriam's restaurant, they need to go through a tuna processing plant. Also, regulators will need to verify and view details from the ledger. Therefore, both parties will gain entry to this Sawtooth blockchain. The regulators will need to query the ledger to confirm that Sarah is legally catching her fish. At the same time, tuna processing plants will need to record their processing and shipping of the tuna on the ledger.

### Lecture 133 - Summary of Supply Chain Flow

* Sarah catches a tuna and uses the client application to record all the details about the catch to the ledger. An entire haul of tuna can be treated as a transaction batch, with each individual tuna registered as a transaction within the batch.
* After the details of the catch are saved to the ledger and the tuna is passed along the supply chain, the processing plant may use the client application to query the ledger for details about specific catches, such as weight. The processing plant will add details reflecting the processing date and time, as well as other relevant information.
* As the tuna is passed along the supply chain, the regulators may use the client application to query the ledger for details about specific catches, such as the owner and location of the catch, to verify legitimacy.
* Lastly, when the haul of tuna arrives at Miriam's restaurant, Miriam is able to use the client application to query the ledger, to make sure Sarah was truthful in her account of where each fish was sourced. This, in turn, guarantees Miriam's restaurant is serving their customers the sustainably caught fish they advertise.

## Section 2 - Key Components and Transaction Flow

### Lecture 134 - Requirements Supported by Hyperledger Sawtooth

* Hyperledger Sawtooth is a blockchain framework with potential in IoT, manufacturing, finance, and enterprise. Hyperledger Sawtooth supports diverse requirements, including both permissioned and permissionless deployments, and a pluggable consensus algorithm. This framework also provides a revolutionary consensus algorithm, Proof of Elapsed Time (PoET), that allows for versatility and scalability suited for a variety of solutions.
* Hyperledger Sawtooth supports many different infrastructural requirements, such as:
	* Permissioned and permissionless infrastructure
	* Modular blockchain architecture
	* Scalability, which is good for larger blockchain networks due to higher throughput
	* Many languages for transaction logic
	* On-chain governance that allows peers to vote on blockchain configuration
	* An advanced transaction execution engine that can process transactions in parallel to accelerate block creation and validation
	* Ethereum contract support with Seth, which allows participants to run Solidity smart contracts and integrate with Ethereum tooling
	* Dynamic consensus lets you upgrade or swap blockchain consensus protocol on the fly as the network grows.

### Lecture 135 - Transaction Batching

* In Hyperledger Sawtooth, batches are clusters of transactions that are committed to state together. If one transaction in the batch cannot be committed, none of the transactions are committed. As a result, transaction batches are often described as an atomic unit of change, since a group of transactions are treated as one, and are committed to the state as one. Every single transaction in Hyperledger Sawtooth is submitted within a batch. Batches can contain as little as a single transaction.
* When a transaction is created by a client, the batch is submitted to the validator (which we will cover more in-depth in the next section). Transactions are organized into a batch in the order they are intended to be committed. The validator then, in turn, applies each transaction within the batch, leading to a change in the global state. The batch is committed to the state. If one transaction within the batch is invalid, then none of the transactions within that batch are committed.
* In summary, transaction batching allows a group of transactions to be applied in a specific order, and if any are invalid, then none of the transactions are applied. This is a powerful tool that can be utilized by many enterprise solutions, as it provides greater efficiency and control for end users.

### Lecture 136 - Validators

* In any blockchain network, modifying the global state requires creating and applying a transaction. In Hyperledger Sawtooth, validators apply batches of transactions that cause changes in the state. More specifically, validators group batches into blocks, submit the blocks, and ensure that transactions result in state changes that are consistent across all participants in the network.
* To start, a user creates a batch containing one or more transactions, and submits it to a validator, usually via a client that communicates with a REST API. The validator then checks the transactions and applies the batch if all transactions are considered valid, resulting in a change to the state. In terms of our demonstrated scenario, Sarah, the tuna fisher, creates a batch to record information about a group of tuna catches. The validator then applies the transactions, and the state is updated if all appropriate attributes are present: a unique ID number, location and time of the catch, weight, and who caught the fish. If any of these elements are missing, the transactions within the batch would not be applied, and the state would not be updated.

### Lecture 137 - Consensus Interface

* A key feature of Hyperledger Sawtooth is its flexibility in allowing different consensus algorithms. As a reminder, the consensus algorithm determines which node on the network will publish the next block on the ledger. Hyperledger Sawtooth provides an abstract interface that supports both PBFT and Nakamoto-style algorithms. Consensus in Hyperledger Sawtooth is modular, meaning that the consensus algorithm can be easily modified.
* Currently, Hyperledger Sawtooth supports the following consensus implementations:
	* Proof of Elapsed Time, or PoET, a Nakamoto-style consensus algorithm that is designed to be a production-grade protocol capable of supporting large networks.
	* Dev mode, a simplified random-leader algorithm that is useful for development and testing on single-node or small networks.
* PoET is available in two versions:
	* PoET-SGX, which relies on Intel® Software Guard Extensions (SGX) to implement a leader-election lottery system
	* PoET simulator, which is the PoET consensus algorithm deployed on an SGX simulator.

### Lecture 138 - Introducing Proof of Elapsed Time (PoET)

* The Proof of Elapsed Time (PoET) consensus algorithm impartially determines who will commit a transaction to state using a lottery function that elects a leader from many different distributed nodes.
* Hyperledger Sawtooth’s PoET algorithm differs from the Proof of Work algorithm implemented by the Bitcoin blockchain in that Proof of Work relies on vast amounts of power, while Proof of Elapsed Time is able to ensure trust and randomness in electing a leader without the high power consumption. PoET allows for increased scalability and participation, as every node in the network has an equal opportunity to create the next block on the chain.

### Lecture 139 - How Proof of Elapsed Time Works

* To start, each validator within the network requests a wait time from an enclave, or a trusted function. This is where the "Elapsed Time" comes into play. The validator with the shortest wait time for a specific block is appointed the leader, and creates the block to be committed to the ledger. As a result, a truly random leader is elected, and the amount of power or type of hardware you have will not give you an advantage. Using simple functions, the network can verify that the winning validator did indeed "win", by proving that it had the shortest time to wait before assuming the leadership position.

### Lecture 140 - Forks

* While PoET provides many benefits and aids tremendously with scalability, there is a downside to the PoET consensus algorithm. And that is the issue of forks. The PoET algorithm may lead to forking, in which two "winners" propose a block. Each fork has to be resolved by validators, and this results in a delay in reaching consistency across the network.

### Lecture 141 - Sawtooth Applications

* As with any blockchain framework, transaction updates need to be approved and shared between many untrusted parties. In Hyperledger Sawtooth, the business logic for an application, the data model that is used to record and store state data, and the client logic are defined as a Sawtooth application, also called a transaction family. An application consists of both a transaction processor (the server-side logic) and one or more clients (for use from the Web, CLI command line, or mobile applications).
* A transaction family defines a set of operations or transaction types that are allowed on the shared ledgers. This allows for flexibility in the level of versatility and risk that exists on a network. Transaction families can provide "safer" smart contracts, because they specify a predefined set of acceptable smart contract templates, as opposed to programming smart contracts from scratch.

### Lecture 142 - Transaction Processors

* A transaction processor provides the server-side business logic that operates on assets within a network. Because  Hyperledger Sawtooth separates the application layer from the consensus and core framework layer, businesses are able to develop transaction processors that do exactly what their applications need. 

Each node within the Hyperledger Sawtooth network runs at least one transaction processor (most networks run several). Each transaction processor handles its own incoming transactions as submitted by authorized clients. Hyperledger Sawtooth allows application developers to specify a namespace for each transaction processor (an application-specific range of addresses in state), which provides flexibility in defining, sharing, and reusing data between transaction processors. Using namespaces in global state lets programmers focus on developing application logic, as opposed to building communication mechanisms between transaction processors.

Hyperledger Sawtooth's transaction processors can be written in a variety of languages, including Javascript, Java, Rust, Python, and Go, which allows flexibility for businesses to create their own applications. Hyperledger Sawtooth provides SDKs in several common languages.

Later in this chapter, in the Writing an Application section, you will be able to explore exactly how transaction processors interact with a client and other Hyperledger Sawtooth components.


### Lecture 143 - Sawtooth Node

* Each organization that enters the Hyperledger Sawtooth network runs at least one validator node, and receives blocks that are broadcasted by peer nodes. Each validator node runs the following things:
	* The validator process
	* The REST API (optional) listening for requests such as transaction posts or state queries
	* One or more transaction processors
* A REST API on each node is optional. Clients can use an external REST API or communicate directly with the validator using ZeroMQ and protocol buffers (protobufs).

## Section 3 - Installing Hyperledger Sawtooth

* In order to successfully install Hyperledger Sawtooth, you should have the following software installed on your computer: cURL, Git, Docker, and Docker Compose.

### Lecture 144 - Installing Hyperledger Sawtooth

* Hyperledger Sawtooth is a suite that permits the creation and utilization of a distributed ledger. Installing Hyperledger Sawtooth will involve adding signing keys for the software creator to our environment, including the repository that contains the code to our system, and performing a typical update/install.
* A Hyperledger Sawtooth validator node can be run either from pre-built Docker images, or natively using Ubuntu 16.04. In this tutorial, we will demonstrate how to set up Hyperledger Sawtooth using Docker.
* Our example Sawtooth environment is a single validator node using the dev mode consensus, a REST API, three transaction processors, and a client container.

### Lecture 145 - Starting Hyperledger Sawtooth

* First, download [the following Docker Compose file](https://raw.githubusercontent.com/hyperledger/education/master/LFS171x/sawtooth-material/sawtooth-default.yaml) as *sawtooth-default.yaml*.
* Next, open a terminal window.
* Then, change your working directory to the same directory where the *sawtooth-default.yaml* Docker Compose file is saved.
* Note: Make sure you do not have anything else running on port 8008 or port 4004.
* Also, make sure to have Docker running on your device before running the commands in this section. Otherwise, when you run *docker-compose* in the next step, you will get a similar error to the one below:
```
ERROR: Couldn't connect to Docker daemon. You might need to start Docker for Mac.
```
* Run the following command: `$ docker-compose -f sawtooth-default.yaml up`
* This command will download the Docker images that comprise the Hyperledger Sawtooth demo environment. The download will take several minutes. The terminal will start to display containers registering and creating initial blocks.

### Lecture 146 - Logging into the Client Container

* The client container is used to run Sawtooth commands, which are used to configure the Sawtooth network and run client functions from the command line.
* Open a new terminal window and navigate to the directory where the *sawtooth-default.yaml* Docker Compose file is saved.
* Log into the client container by running the following command: `$ docker exec -it sawtooth-shell-default bash`
In your terminal, you will see something similar to the following: `root@75b380886502:/#`
* Your environment is now set up and you are ready to start experimenting with the network. But first, let’s confirm that our validator is up and running, and reachable from the client container. To do this, run the following command: `$ curl http://rest-api:8008/blocks`
* After running this command, you should see a json object response with “data”, array of batches, header, etc.
* To check the connectivity from the host computer to the Docker container, run the following command in a new terminal window (it does not need to be the same directory as mentioned previously in this section): `$ curl http://localhost:8008/blocks`
* After running this command, you should see a json object response with “data”, array of batches, header, etc. 

### Lecture 147 - Stopping Hyperledger Sawtooth

* First, press Ctrl+C from the window where you originally ran `docker-compose`.
* Then, in the terminal, you will see containers stopping. After that, run the following command: `$ docker-compose -f sawtooth-default.yaml down`

## Section 4 - Writing an Application

### Lecture 148 - Applications

* In a Sawtooth application, the ledger will store the state of the system, in addition to the immutable record of transactions that created that state. An application typically consists of two parts:
* **Client Application** : 
	* Sends transactions to the blockchain, typically through the Sawtooth REST API. 
	* Provides a user interface for the application. A client can be a command-line interface, a web page, a mobile app, an IoT sensor, or most any other kind of interface capable of sending HTTP requests.
* **Transaction Processor** : 
	* Encodes the business logic of the application. 
	* Communicates with the validator, which sends transactions received from the client to the transaction processor for validation.

### Lecture 149 - Review of Hyperledger Sawtooth Components

* **Sawtooth validators** validate transactions, combine batches of transactions into blocks, submit them to the ledger, and approve valid blocks according to the network's consensus algorithm.
* **Sawtooth applications** are distributed applications (also called transaction families) that consist of a transaction  processor  for the server-side logic and a client for use from Web, CLI, or mobile applications.
* **Transaction processors** provide the server-side business logic.
* **Batches** are clusters of transactions that are submitted together. If one transaction fails, the other transactions in that batch also fail.
* The **network layer** is responsible for communicating between validator nodes in a Hyperledger Sawtooth network, including performing initial connectivity, peer discovery, and message handling.
* The **global state** contains the current state of the ledger and a chain of transaction invocations. The state for all applications running on the network s is represented on each node. The state is split into application-specific namespaces, which allows applications to share and reuse global state data between transaction processors.

### Lecture 150 - Sawtooth TunaChain Application

* Let’s get our feet wet with an example of a simple Hyperledger Sawtooth blockchain application that relates to the tuna supply scenario we discussed in our demonstrated scenario. Sawtooth TunaChain allows a user to create named assets (Tuna), and transfer them between different Holders designated by a public key.
* In our example, we will look at:
	* A transaction processor
	* A simple browser-based client.
* The TunaChain transaction processor is written using the Python 3 Sawtooth SDK. It interfaces with a Sawtooth validator in order to validate transactions.
* The client is a simple browser-based user interface written using the Sawtooth Javascript SDK. It allows the user to manage public/private key pairs and submit transactions using the Sawtooth REST API.

### Lecture 151 - Cloning the Repository

* If you have not done so, you must clone the hyperledger/education GitHub repository. This repository contains the code for the Sawtooth TunaChain example application.
* To clone the repository, open a terminal window, navigate to your projects folder, and enter the following commands:
```
$ git clone https://github.com/hyperledger/education.git
$ cd education/LFS171x/sawtooth-material/sawtooth-tuna
```
* Now you are in the folder that contains the code for the Sawtooth TunaChain example.

### Lecture 152 - Running the Application

* Make sure you have Docker running on your machine before you run the next command. If you do not have Docker installed, you should review Chapter 4, "Technical Requirements".
* Note: Make sure you are in the *sawtooth-tuna* folder.
* We will use the provided *docker-compose.yaml* file to create and run Docker containers for the required Sawtooth and TunaChain components.
* Run the following command to start Sawtooth with our TunaChain application: `$ docker-compose up`
* At this point, your terminal window should show that these containers are running: *sawtooth-validator, tunachain-shell, sawtooth-settings-tp, tunachain-tp, sawtooth-rest-api,* and *tunachain-client*.
* You should also see messages showing that *sawtooth-settings-tp* and *tunachain-tp* have registered with the validator, that the REST API has connected to the validator at port 4004, and that the client has been built inside the *tunachain-shell* container.
* If all of these conditions are true, and no other errors occur, you have successfully started a single-node Sawtooth network running the TunaChain demo application.

### Lecture 153 - Sawtooth TunaChain State

* There are two kinds of state entries within the TunaChain application: Assets and Transfers. These state entries are represented as UTF-8 encoded JSON objects with sorted keys.
* Asset state entries are formatted as follows:
```
{
    # Name of the Asset
    "name": "name",
}
```
* Transfer state entries are formatted as follows:
```
{
    # Name of the Asset
    "asset": "asset",

    # Public key of the proposed recipient of the Asset
    "owner": "owner",
}
```

### Lecture 154 - Sawtooth TunaChain Addressing

* In Hyperledger Sawtooth, namespaces define the addressing scheme for application data. All Sawtooth applications store data in the state dictionary at 35-byte (70 hex-character) addresses. The addresses for TunaChain resources are generated as follows:
	* The first 3 bytes of any Sawtooth state address are reserved for the application namespace. For the TunaChain application, the namespace prefix is generated by taking the first 6 characters of a SHA-512 hash of the application name "transfer-chain": *0x19d832*
	* The next byte of a TunaChain address specifies which type of resource is stored at the address: Asset => 0x00 Transfer => 0x01
	* The final 31 bytes of a TunaChain address are the first 62 characters of a SHA-512 hash of the name  of the asset.
* For example, the TunaChain address of an Asset with the name "tuna4" would be generate as follows:
```
>>> hashlib.sha512('transfer-chain'.encode('utf-8')).hexdigest()[:6] + '00' + hashlib.sha512('tuna4'.encode('utf-8')).hexdigest()[:62]'19d83200714923803714eeb557276759eab2ce605c929dee093e7aa4359ee6f29a8880'
```

### Lecture 155 - Sawtooth TunaChain Transaction Payload

* Each TunaChain transaction payload is represented as a JSON object with the following format:
```
{
    # Action the transaction takes, either "create", "transfer", "accept", or
    # "reject"
    "action": "action",

    # Name of the Asset to be affected by the transaction
    "asset": "asset",

    # Public key of the proposed new owner for a "transfer" transaction
    "owner": "owner"
}
```

### Lecture 156 - Browser Client

* We are now ready to test our application through the user interface. In order to use the TunaChain client application, use a browser to navigate to localhost:8000.
* There are four different things we can do within the application:
	* **Select Holder** allows us to select a public key or create a new public/private key pair, which is referenced as a Holder
	* **Create Tuna Record** submits a transaction to create a new Tuna entry in state, which is held by the currently selected Holder
	* **Transfer Tuna** submits a transaction to create a new Transfer entry in state, which can be accepted or rejected by the potential recipient of the Tuna asset
	* **Accept Tuna** shows a list of the current Transfers with the currently selected Holder listed as a recipient, as well as options to either Accept or Reject the Transfer.
* Also, there is a Tuna List table that shows all of the current Tuna assets in state with their respective Holders.
* Note: The application is running inside the tunachain-client Docker container, but the port that it is running on is exposed at port 8000 on the host machine.

### Lecture 157 - Creating a New Holder

* In order to submit transactions to the REST API, we need to create a new Holder. For the TunaChain application, Holders are just public/private key pairs which are stored in your browser's local storage.
* Within the user interface, you can create these keys from the Select Holder dropdown list. You can use this same dropdown list to switch between multiple users in local storage.
* This user interface element invokes the following function within the client code:
```
// Select User
$('[name="keySelect"]').on('change', function () {
  if (this.value === 'new') {
    app.user = makeKeyPair()
    app.keys.push(app.user)
    saveKeys(app.keys)
    addOption(this, app.user.public, true)
    addOption('[name='transferSelect"]', app.user.public)
  } else if (this.value === 'none') {
    app.user = null
  } else {
    app.user = app.keys.find(key => key.public ===this.value)
    app.refresh()
  }
})
```
*app.js:  Select User*
```
//Create new key-pair
const makeKeyPair = () => {
  const context = createContext('secp256k1')
  const privateKey = context.newRandomPrivateKey()
  return {
    public: context.getPublicKey(privateKey).asHex(),
    private: privateKey.asHex()
  }
}
```
*state.js:  makeKeyPair*

* This function uses the [JavaScript Client Signing SDK](https://sawtooth.hyperledger.org/docs/core/releases/1.0/javascript_sdk/signing/index.html#http://) to create a random 256-bit private key represented as a 64-char hex string. This key should not be shared with anyone else.
* Next, the function derives a public key from the 256-bit private key created above. This is the key that is safe to share.
* It returns this key pair to the application, where it calls the following function to save the key pair to local storage:
```
//Save key-pairs to localStorage
const saveKeys = keys => {
  const paired = keys.map(pair => [pair.public, pair.private].join(','))
  localStorage.setItem(KEY_NAME, paired.join(';'))
}
```
*state.js:  saveKeys*

* Note: This method of saving the key pair is for demonstration purposes only. This method is not recommended for a production environment. 

### Lecture 158 - Creating a Record of Tuna

* Within the user interface, select the owner of the new Asset in the Select Holder dropdown, then provide a unique name for the tuna in the Create Tuna Record text box. Lastly, click the Create button.
* After clicking the Create button, the following function is called within the client:
```
//Create Asset
$('#createSubmit').on('click', function () {
  const asset = $('#createName').val()
  if (asset) app.update('create', asset)
})
```
*apps.js:  Create Asset*
* Each user interface element that needs to make a change to state will call the app.update() function. This function formats the transaction payload and sends it to the submitUpdate() function in state.js.
```
app.update = function (action, asset, owner) {
  if (this.user) {
    submitUpdate(
      { action, asset, owner },
      this.user.private,
      success => success ? this.refresh() : null
    )
  }
}
```
*app.js:  app.update()*
* The submitUpdate() function handles the process of creating a transaction, adding it to a batch, submitting the batch to the REST API, and waiting for a response.
* If the transaction was successfully executed by the transaction processor, added to a block, and published by the validator, state will be updated with the new entry. After refreshing the page, you will see the tuna Asset show up in the Tuna List, along with its associated Holder's public key.

### Lecture 159 - Transferring a Tuna

* Any Asset assigned to a particular Holder can be transferred to another Holder by using the dropdowns under Transfer Tuna. Note that the transfer must be accepted by the recipient before it is finalized.
* In the above example, we are proposing to transfer the ownership of tuna4 from the current owner (identified by the key starting with 02ddf8de...) to a new owner (identified by the key starting with 03b241b1...).
* After clicking the Transfer button, the following function is called within the client:
```
//Transfer Asset
$('#transferSubmit').on('click', function () {
  const asset = $('[name="assetSelect"]').val()
  const owner = $('[name="transferSelect"]').val()
  if (asset && owner) app.update('transfer', asset, owner)
})
```
*apps.js: Transfer Asset*

* This function calls app.update(), which in turn calls submitUpdate() to submit the transaction to create a new Transfer entry in state.

### Lecture 160 - Accepting or Rejecting Transfers

* Once a Transfer has been created, go to the Select Holder dropdown and select the public key of the potential recipient. This will reload the page and populate the Accept Tuna section with all of the Transfers in state with the selected Holder as the potential recipient, as shown below:
* Clicking Accept or Reject will invoke one of the following functions:
```
//Accept Asset
$('#transferList').on('click', '.accept', function () {
  const asset = $(this).prev().text()
  if (asset) app.update('accept', asset)
})
```
*app.js:  Accept Asset*
```
//Reject Asset
$('#transferList').on('click', '.reject', function () {
  const asset = $(this).prev().prev().text()
  if (asset) app.update('reject', asset)
})
```
*app.js:  Reject Asset*

* After accepting or rejecting the Transfer, the Transfer will be removed from the Accept Tuna section. If the Transfer was accepted, the Tuna List table will be updated to show the new owner. If it was rejected, the Tuna List table will be unchanged indicating that a transfer did not take place.

### Lecture 161 - TunaChain Transaction Processor

* To review, there are two main components of a transaction processor:
	* *TransactionProcessor* class : A general purpose class that is provided by the Sawtooth SDK. It handles the connection between the transaction processor and the validator.
	* *TransactionHandler* class : A base class that is extended with specific validation logic for each application. In addition to several metadata methods, it has an apply() method which encompasses the logic for validating and executing a transaction.
	The apply() method gets called with two arguments, transaction and context. The argument transaction holds the command that is to be executed, while context stores information about the current state.
* To separate details of state encoding and payload handling from validation logic, the TunaChain transaction processor utilizes two additional classes:
	* *TunachainPayload* has action, asset, and *owner* fields, and is responsible for validating that the transaction payload was properly formed.
	* *TunachainState* contains a reference to *context*, and has additional methods for generating state addresses, as well as getting and setting values in state.
* The code for the TunaChain transaction processor can be found [here](https://github.com/hyperledger/education/tree/master/LFS171x/sawtooth-material/sawtooth-tuna/processor).

### Lecture 162 - Shutting Down Sawtooth

* Note: When we are done with this tutorial, run the following command to shut down the Docker containers running the Sawtooth components: `$ docker-compose down`

### Lecture 163 - Summary of TunaChain Application Flow

* The example TunaChain application demonstrates Hyperledger Sawtooth features with a simple browser-based client for the user interface and a transaction processor for the business logic.
* Hyperledger Sawtooth allows entities to securely update and read the distributed ledger without involving a central authority. Developers create application and transaction processor business logic (smart contract).
* Through the client application, users (tuna fisher, regulator, restaurant) are able to modify the state by creating and applying transactions.
* Through a REST API, the client application creates a batch containing a single transaction, and submits it to the validator.
* The validator applies the transaction using the transaction processor, which makes a change to the state (e.g., creating a record of a tuna catch).

## Section 5 - Joining the Hyperledger Sawtooth Community

### Lecture 164 - Community Meetings and Mailing Lists

* You can join the [Sawtooth mailing list](https://lists.hyperledger.org/g/sawtooth) for technical discussions and announcements.
* The Hyperledger [Community Meetings calendar](https://calendar.google.com/calendar/embed?src=linuxfoundation.org_nf9u64g9k9rvd9f8vp4vur23b0%40group.calendar.google.com&ctz=America/SanFrancisco) includes online application developer forums and sprint planning meetings for Hyperledger Sawtooth.
* Some of the recordings of previous virtual tech forums on Hyperledger Sawtooth can be found [here](https://drive.google.com/drive/folders/0B_NJV6eJXAA1VnFUakRzaG1raXc).

### Lecture 165 - GitHub and Rocket.Chat

* You can also get involved with the Hyperledger Sawtooth community on GitHub and Rocket.Chat.
* Hyperledger Sawtooth code is available in GitHub repositories. All code available on GitHub is forkable and viewable:
	* [https://github.com/hyperledger/sawtooth-core](https://github.com/hyperledger/sawtooth-core)
	* [https://github.com/hyperledger/sawtooth-supply-chain](https://github.com/hyperledger/sawtooth-supply-chain)
	* [https://github.com/hyperledger/sawtooth-seth](https://github.com/hyperledger/sawtooth-seth)
* You can also join the live conversations on Hyperledger Chat (powered by Rocket.Chat, an alternative to Slack), using your Linux Foundation ID:
	* [https://chat.hyperledger.org/channel/sawtooth](https://chat.hyperledger.org/channel/sawtooth)
	* [https://chat.hyperledger.org/channel/sawtooth-consensus](https://chat.hyperledger.org/channel/sawtooth-consensus)
	* [https://chat.hyperledger.org/channel/sawtooth-seth](https://chat.hyperledger.org/channel/sawtooth-seth)

# Chapter 9 - Introduction to Hyperledger Fabric

## Section 1 - Addressing Illegal, Unregulated, and Unreported Tuna Fishing (Demonstrated Scenario)

### Lecture 166 - Defining Our Actors

* Sarah is the fisherman who sustainably and legally catches tuna.
* Regulators verify that the tuna has been legally and sustainably caught.
* Miriam is a restaurant owner who will serve as the end user, in this situation.
* Carl is another restaurant owner fisherman Sarah can sell tuna to.
* Using Hyperledger Fabric, we will be demonstrating how tuna fishing can be improved starting from the source, fisherman Sarah, and the process by which she sells her tuna to Miriam's restaurant.

### Lecture 167 - Featured Hyperledger Fabric Elements

* Channels are data partitioning mechanisms that allow transaction visibility for stakeholders only. Each channel is an independent chain of transaction blocks containing only transactions for that particular channel.
* The chaincode (Smart Contracts) encapsulates both the asset definitions and the business logic (or transactions) for modifying those assets. Transaction invocations result in changes to the ledger.
* The ledger contains the current world state of the network and a chain of transaction invocations. A shared, permissioned ledger is an append-only system of records and serves as a single source of truth.
* The network is the collection of data processing peers that form a blockchain network. The network is responsible for maintaining a consistently replicated ledger.
* The ordering service is a collection of nodes that orders transactions into a block.
* The world state reflects the current data about all the assets in the network. This data is stored in a database for efficient access. Current supported databases are LevelDB and CouchDB.
* The membership service provider (MSP) manages identity and permissioned access for clients and peers.

### Lecture 168 - The Catch

* We will start with Sarah, our licensed tuna fisher, who makes a living selling her tuna to multiple restaurants. Sarah operates as a private business, in which her company frequently makes international deals. Through a client application, Sarah is able to gain entry to a Hyperledger Fabric blockchain network comprised of other fishermen, as well as regulators and restaurant owners. Sarah has the ability to add to and update information in the blockchain network's  ledger as tuna pass through the supply chain, while regulators and restaurants have read access to the ledger.
* After each catch, Sarah records information about each individual tuna, including: a unique ID number, the location and time of the catch, its weight, the vessel type, and who caught the fish. For the sake of simplicity, we will stick with these six data attributes. However, in an actual application, many more details would be recorded, from toxicology, to other physical characteristics.
* These details are saved in the world state as a key/value pair based on the specifications of a chaincode contract, allowing Sarah’s application to effectively create a transaction on the ledger. You can see the example below:
```
$ var tuna = { id: ‘0001’, holder: ‘Sarah’, location: { latitude: '41.40238', longitude: '2.170328'}, when: '20170630123546', weight: ‘58lbs’, vessel : ‘9548E’ }
```

### Lecture 169 - The Incentives

* Miriam is a restaurant owner looking to source low cost, yet high quality tuna that have been responsibly caught. Whenever Miriam buys tuna, she is always uncertain whether she can trust that the tuna she is purchasing is legally and sustainably caught, given the prominence of illegal and unreported tuna fishing.
* At the same time, as a legitimate and experienced fisherman, Sarah strives to make a living selling her tuna at a reasonable price. She would also like autonomy over who she sells to and at what price.
* Luckily for both Sarah and Miriam, Hyperledger Fabric can help!

### Lecture 170 - The Sale

* Normally, Sarah sells her tuna to restaurateurs, such as Carl, for $80 per pound. However, Sarah agrees to give Miriam a special price of $50 per pound of tuna, rather than her usual rate. In a traditional public blockchain, once Sarah and Miriam have completed their transaction, the entire network is able to view the details of this agreement, especially the fact that Sarah gave Miriam a special price. As you can imagine, having other restaurateurs, such as Carl, aware of this deal is not economically advantageous for Sarah.
* To remedy this, Sarah wants the specifics of her deal to not be available to everyone on the network, but still have every actor in the network be able to view the details of the fish she is selling. Using Hyperledger Fabric's feature of channels, Sarah can privately agree on the terms with Miriam, such that only the two of them can see them, without anyone else knowing the specifics.
* Additionally, other fishermen, who are not part of Sarah and Miriam’s transaction, will not see this transaction on their ledger. This ensures that another fisherman cannot undercut the bid by having information about the prices that Sarah is charging different restaurateurs.

### Lecture 171 - The Regulators

* Regulators will also gain entry to this Hyperledger Fabric blockchain network to confirm, verify, and view details from the ledger. Their application will allow these actors to query the ledger and see the details of each of Sarah’s catches to confirm that she is legally catching her fish. Regulators only need to have query access, and do not need to add entries to the ledger. With that being said, they may be able to adjust who can gain entry to the network and/or be able to remove fishermen from the network, if found to be partaking in illegal activities.

### Lecture 172 - Gaining Network Membership

* Hyperledger Fabric is a permissioned network, meaning that only participants who have been approved can gain entry to the network. To handle network membership and identity, membership service providers (MSP) manage user IDs, and authenticate all the participants in the network. A Hyperledger Fabric blockchain network can be governed by one or more MSPs. This provides modularity of membership operations, and interoperability across different membership standards and architectures.
* In our scenario, the regulator, the approved fishermen, and the approved restaurateurs should be the only ones allowed to join the network. To achieve this, a membership service provider (MSP) is defined to accommodate membership for all members of this supply chain. In configuring this MSP, certificates and membership identities are created. Policies are then defined to dictate the read/write policies of a channel, or the endorsement policies of a chaincode.
* Our scenario has two separate chaincodes, which are run on three separate channels. The two chaincodes are: one for the price agreement between the fisherman and the restaurateur, and one for the transfer of tuna. The three channels are: one for the price agreement between Sarah and Miriam; one for the price agreement between Sarah and Carl; and one for the transfer of tuna. Each member of this network knows about each other and their identity. The channels provide privacy and confidentiality of transactions.
* In Hyperledger Fabric, MSPs also allow for dynamic membership to add or remove members to maintain integrity and operation of the supply chain. For example, if Sarah was found to be catching her fish illegally, she can have her membership revoked, without compromising the rest of the network. This feature is critical, especially for enterprise applications, where business relationships change over time.

### Lecture 173 - Summary of Demonstrated Scenario

* Below is a summary of the tuna catch scenario presented in this section:
		* Sarah catches a tuna and uses the supply chain application’s user interface to record all the details about the catch to the ledger. Before it reaches the ledger, the transaction is passed to the endorsing peers on the network, where it is then endorsed. The endorsed transaction is sent to the ordering service, to be ordered into a block. This block is then sent to the committing peers in the network, where it is committed after being validated.
		* As the tuna is passed along the supply chain, regulators may use their own application to query the ledger for details about specific catches (excluding price, since they do not have access to the price-related chaincode).
		* Sarah may enter into an agreement with a restaurateur Carl, and agree on a price of $80 per pound. They use the blue channel for the chaincode contract stipulating $80/lb. The blue channel's ledger is updated with a block containing this transaction.
		* In a separate business agreement, Sarah and Miriam agree on a special price of $50 per pound. They use the red channel's chaincode contract stipulating $50/lb. The red channel's ledger is updated with a block containing this transaction.

## Section 2 - Key Components and Transaction Flow

### Lecture 174 - Roles within a Hyperledger Fabric Network

* There are three different types of roles within a Hyperledger Fabric network:
	* **Clients** :  Clients are applications that act on behalf of a person to propose transactions on the network.
	* **Peers** : Peers maintain the state of the network and a copy of the ledger. There are two different types of peers: endorsing and committing peers. However, there is an overlap between endorsing and committing peers, in that endorsing peers are a special kind of committing peers. All peers commit blocks to the distributed ledger.
		- Endorsers simulate and endorse transactions
		- Committers verify endorsements and validate transaction results, prior to committing transactions to the blockchain.
	* **Ordering Service** : The ordering service accepts endorsed transactions, orders them into a block, and delivers the blocks to the committing peers.

### Lecture 175 - How to Reach Consensus

* In a distributed ledger system, consensus is the process of reaching agreement on the next set of transactions to be added to the ledger. In Hyperledger Fabric, consensus is made up of three distinct steps:
	* Transaction endorsement
	* Ordering
	* Validation and commitment.
* These three steps ensure the policies of a network are upheld. We will explore how these steps are implemented by exploring the transaction flow.

### Lecture 176 - Transaction Flow

* Within a Hyperledger Fabric network, transactions start out with client applications sending transaction proposals, or, in other words, proposing a transaction to endorsing peers.
* Client applications are commonly referred to as applications or clients, and allow people to communicate with the blockchain network. Application developers can leverage the Hyperledger Fabric network through the application SDK.
* Each endorsing peer simulates the proposed transaction, without updating the ledger. The endorsing peers will capture the set of Read and Written data, called RW Sets. These RW sets capture what was read from the current world state while simulating the transaction, as well as what would have been written to the world state had the transaction been executed. These RW sets are then signed by the endorsing peer, and returned to the client application to be used in future steps of the transaction flow.
* Endorsing peers must hold smart contracts in order to simulate the transaction proposals.

A **Transaction Endorsement** is a signed response to the results of the simulated transaction. The method of transaction endorsements depends on the endorsement policy which is specified when the chaincode is deployed. An example of an endorsement policy would be "the majority of the endorsing peers must endorse the transaction". Since an endorsement policy is specified for a specific chaincode, different channels can have different endorsement policies.

* The application then submits the endorsed transaction and the RW sets to the ordering service. Ordering happens across the network, in parallel with endorsed transactions and RW sets submitted by other applications.
* The ordering service takes the endorsed transactions and RW sets, orders this information into a block, and delivers the block to all committing peers.
* The ordering service, which is made up of a cluster of orderers, does not process transactions, smart contracts, or maintain the shared ledger. The ordering service accepts the endorsed transactions and specifies the order in which those transactions will be committed to the ledger. The Fabric v1.0 architecture has been designed such that the specific implementation of "ordering" (Solo, Kafka, BFT) becomes a pluggable component. The default ordering service for Hyperledger Fabric is Kafka. Therefore, the ordering service is a modular component of Hyperledger Fabric.
* The committing peer validates the transaction by checking to make sure that the RW sets still match the current world state. Specifically, that the Read data that existed when the endorsers simulated the transaction is identical to the current world state. When the committing peer validates the transaction, the transaction is written to the ledger, and the world state is updated with the Write data from the RW Set.
* If the transaction fails, that is, if the committing peer finds that the RW set does not match the current world state, the transaction ordered into a block will still be included in that block, but it will be marked as invalid, and the world state will not be updated.
* Committing peers are responsible for adding blocks of transactions to the shared ledger and updating the world state. They may hold smart contracts, but it is not a requirement.
* Lastly, the committing peers asynchronously notify the client application of the success or failure of the transaction. Applications will be notified by each committing peer.

### Lecture 177 - Ordering

*Transactions within a timeframe are sorted into a block and are committed in sequential order.*

* In a blockchain network, transactions have to be written to the shared ledger in a consistent order. The order of transactions has to be established to ensure that the updates to the world state are valid when they are committed to the network. Unlike the Bitcoin blockchain, where ordering occurs through the solving of a cryptographic puzzle, or mining, Hyperledger Fabric allows the organizations running the network to choose the ordering mechanism that best suits that network. This modularity and flexibility makes Hyperledger Fabric incredibly advantageous for enterprise applications.
* Hyperledger Fabric provides three ordering mechanisms: SOLO, Kafka, and Simplified Byzantine Fault Tolerance (SBFT), the latter of which has not yet been implemented in Fabric v1.0.
	* **SOLO** :  It is the Hyperledger Fabric ordering mechanism most typically used by developers experimenting with Hyperledger Fabric networks. SOLO involves a single ordering node.
	* **Kafka** : It is the Hyperledger Fabric ordering mechanism that is recommended for production use. This ordering mechanism utilizes Apache Kafka, an open source stream processing platform that provides a unified, high-throughput, low-latency platform for handling real-time data feeds. In this case, the data consists of endorsed transactions and RW sets. The Kafka mechanism provides a crash fault-tolerant solution to ordering.
	* **SBFT** : It stands for Simplified Byzantine Fault Tolerance. This ordering mechanism is both crash fault-tolerant and byzantine fault-tolerant, meaning that it can reach agreement even in the presence of malicious or faulty nodes. The Hyperledger Fabric community has not yet implemented this mechanism, but it is on their roadmap.
* These three ordering mechanisms provide alternate methodologies for agreeing on the order of transactions.

### Lecture 178 - Identity Verification

* In addition to the multitude of endorsement, validity, and versioning checks that take place, there are also ongoing identity verifications happening during each step of the transaction flow. Access control lists are implemented on the hierarchical layers of the network (from the ordering service down to channels), and payloads are repeatedly signed, verified, and authenticated as a transaction proposal passes through the different architectural components.

### Lecture 179 - Transaction Flow Summary

* It is important to note that the state of the network is maintained by peers, and not by the ordering service or the client. Normally, you will design your system such that different machines in the network play different roles. That is, machines that are part of the ordering service should not be set up to also endorse or commit transactions, and vice versa. However, there is an overlap between endorsing and committing peers on the system. Endorsing peers must have access to and hold smart contracts, in addition to fulfilling the role of a committing peer. Endorsing peers do commit blocks, but committing peers do not endorse transactions.
* Endorsing peers verify the client signature, and execute a chaincode function to simulate the transaction. The output is the chaincode results, a set of key/value versions that were read in the chaincode (Read set), and the set of keys/values that were written by the chaincode. The proposal response gets sent back to the client, along with an endorsement signature. These proposal responses are sent to the orderer to be ordered. The orderer then orders the transactions into a block, which it forwards to the endorsing and committing peers. The RW sets are used to verify that the transactions are still valid before the content of the ledger and world state is updated. Finally, the peers asynchronously notify the client application of the success or failure of the transaction.

### Lecture 180 - Channels

* Channels allow organizations to utilize the same network, while maintaining separation between multiple blockchains. Only the members of the channel on which the transaction was performed can see the specifics of the transaction. In other words, channels partition the network in order to allow transaction visibility for stakeholders only. This mechanism works by delegating transactions to different ledgers. Only the members of the channel are involved in consensus, while other members of the network do not see the transactions on the channel.
* The diagram above shows three distinct channels: blue, orange, and grey. Each channel has its own application, ledger, and peers.
* Peers can belong to multiple networks or channels. Peers that do participate in multiple channels simulate and commit transactions to different ledgers. The ordering service is the same across any network or channel.
* A few things to remember:
	* The network setup allows for the creation of channels.
	* The same chaincode logic can be applied to multiple channels.
	* A given user can participate in multiple channels.

### Lecture 181 - State Database

* The current state data represents the latest values for all assets in the ledger. Since the current state represents all the committed transactions on the channel, it is sometimes referred to as world state.
* Chaincode invocations execute transactions against the current state data. To make these chaincode interactions extremely efficient, the latest key/value pairs for each asset are stored in a state database. The state database is simply an indexed view into the chain’s committed transactions. It can therefore be regenerated from the chain at any time. The state database will automatically get recovered (or generated, if needed) upon peer startup, before new transactions are accepted. The default state database, LevelDB, can be replaced with CouchDB.
	* LevelDB is the default key/value state database for Hyperledger Fabric, and simply stores key/value pairs.
	*  CouchDB is an alternative to LevelDB. Unlike LevelDB, CouchDB stores JSON objects. CouchDB is unique in that it supports keyed, composite, key range, and full data-rich queries.
* Hyperledger Fabric’s LevelDB and CouchDB are very similar in their structure and function. Both LevelDB and CouchDB support core chaincode operations, such as getting and setting key assets, and querying based on these keys. With both, keys can be queried by range, and composite keys can be modeled to enable equivalence queries against multiple parameters. But, as a JSON document store, CouchDB additionally enables rich query against the chaincode data, when chaincode values (e.g. assets) are modeled as JSON data.

### Lecture 182 - Smart Contracts

* As a reminder, smart contracts are computer programs that contain logic to execute transactions and modify the state of the assets stored within the ledger. Hyperledger Fabric smart contracts are called chaincode and are written in Go. The chaincode serves as the business logic for a Hyperledger Fabric network, in that the chaincode directs how you manipulate assets within the network. We will discuss more about chaincode in the Understanding Chaincode section.

### Lecture 183 - Membership Service Provider (MSP)

* The membership service provider, or MSP, is a component that defines the rules in which identities are validated, authenticated, and allowed access to a network. The MSP manages user IDs and authenticates clients who want to join the network. This includes providing credentials for these clients to propose transactions. The MSP makes use of a Certificate Authority, which is a pluggable interface that verifies and revokes user certificates upon confirmed identity. The default interface used for the MSP is the Fabric-CA API, however, organizations can implement an External Certificate Authority of their choice. This is another feature of Hyperledger Fabric that is modular. Hyperledger Fabric supports many credential architectures, which allows for many types of External Certificate Authority interfaces to be used. As a result, a single Hyperledger Fabric network can be controlled by multiple MSPs, where each organization brings their favorite.

### Lecture 184 - What Does the MSP Do?

* To start, users are authenticated using a certificate authority. The certificate authority identifies the application, peer, endorser, and orderer identities, and verifies these credentials. A signature is generated through the use of a Signing Algorithm and a Signature Verification Algorithm.
* Specifically, generating a signature starts with a Signing Algorithm, which utilizes the credentials of the entities associated with their respective identities, and outputs an endorsement. A signature is generated, which is a byte array that is bound to a specific identity. Next, the Signature Verification Algorithm takes the identity, endorsement, and signature as inputs, and outputs 'accept' if the signature byte array corresponds with a valid signature for the inputted endorsement, or outputs 'reject' if not. If the output is 'accept', the user can see the transactions in the network and perform transactions with other actors in the network. If the output is 'reject', the user has not been properly authenticated, and is not able to submit transactions to the network, or view any previous transactions.

### Lecture 185 - Fabric-Certificate Authority

* In general, Certificate Authorities manage enrollment certificates for a permissioned blockchain. Fabric-CA is the default certificate authority for Hyperledger Fabric, and handles the registration of user identities. The Fabric-CA certificate authority is in charge of issuing and revoking Enrollment Certificates (E-Certs). The current implementation of Fabric-CA only issues E-Certs, which supply long term identity certificates. E-Certs, which are issued by the Enrollment Certificate Authority (E-CA), assign peers their identity and give them permission to join the network and submit transactions.

## Section 3 - Installing Hyperledger Fabric

* In order to successfully install Hyperledger Fabric, you should be familiar with Go and Node.js programming languages, and have the following features installed on your computer: cURL, Node.js, npm package manager, Go language, Docker, and Docker Compose.

### Lecture 186 - Installing Hyperledger Fabric Docker Images and Binaries

* Next, we will download the latest released Docker images for Hyperledger Fabric, and tag them with the latest tag. Execute the command from within the directory into which you will extract the platform-specific binaries:
```
$ curl -sSL https://goo.gl/6wtTN5 | bash -s 1.1.0
```
* NOTE: Check [http://hyperledger-fabric.readthedocs.io/en/release-1.1/samples.html#binaries](http://hyperledger-fabric.readthedocs.io/en/release-1.1/samples.html#binaries) for the latest URL (the blue portion in the above curl command) to pull in binaries.
* This command downloads binaries for *cryptogen, configtxgen, configxlator, peer* AND downloads the Hyperledger Fabric Docker images. These assets are placed in a *bin* subdirectory of the current working directory.

To confirm and see the list of Docker images you’ve just downloaded, run:
```
$ docker images
```
* The expected response is: (a handful of fabric docker images)
* Note: The tags for each of the repositories above boxed in red. If the Docker images are not already tagged with the latest tag, perform the following command for each of the Docker images:
```
$ docker tag hyperledger/fabric-tools:x86_64-1.0.2 hyperledger/fabric-tools:latest
```
* Swap out the blue portion with the tags you see in your list of repositories. Also, swap out the red portion with the name of the Docker image you are switching the tag for (e.g.: fabric-tools, fabric-ccenv, fabric-orderer, etc.). Repeat this step for all Docker images you see in the list.

In the screenshot above, the Docker images are already tagged. If this is the case for you, you do not need to do this extra step.

### Lecture 187 - Installing Hyperledger Fabric

* As an additional measure, you may want to add the *bin* subdirectory to your PATH environment variable, so these can be picked up without needing to qualify the PATH to each binary. You can do this by running the following:
```
$ export PATH=$PWD/bin:$PATH
```
To install the Hyperledger Fabric sample code which will be used in the tutorials, do:
```
$ git clone https://github.com/hyperledger/fabric-samples.git
$ cd fabric-samples/first-network
```

### Lecture 188 - Starting a Test Hyperledger Fabric Network

* Now that we have successfully installed Hyperledger Fabric, we can walk through setting up a simple network that has two members. To refer back to our demonstrated scenario, the network includes asset management of each tuna verified, transferred, and purchased between Sarah, the fisherman, and Miriam, the restaurateur. We’ll create a simple two member network consisting of two organizations (effectively, Sarah and Miriam), each maintaining two peers and an ordering service.
* We will use Docker images to bootstrap our first Hyperledger Fabric network. It will also launch a container to run a scripted execution that will join peers to a channel, deploy, and instantiate the chaincode, and execute transactions against the chaincode.

### Lecture 189 - Getting Started with Your First Network

* Are you ready to get started? Run this command ( within the first-network folder ): 
```
$ ./byfn.sh -m generate
```
* A brief description will appear, along with a Y/N command line prompt. Respond with a Y <Enter> to continue.
* This step generates all of the certificates and keys for all our various network entities, including the genesis block used to bootstrap the ordering service and a collection of configuration transactions required to create a channel.
* Next, you can start the network with the following command:
```
$ ./byfn.sh -m up
```
* Another command line will appear, reply with Y <Enter> to continue.
* Logs will appear in the command line, showing containers being launched, channels being created and joined, chaincode being installed, instantiated, and invoked on all the peers, as well as various transaction logs.
* Troubleshooting Note:
* If you have difficulties with the two previous commands and you suspect that your Docker images may be at fault, you can start back from scratch, which will delete and untag the Docker images.
```
$ docker rmi -f $(docker images -q)
```
* Once you run this command, return to the Installing Hyperledger Fabric Docker Images and Binaries page, at the beginning of this section.

## Section 4 - Understanding Chaincode

### Lecture 190 - Chaincode

* In Hyperledger Fabric, chaincode is the "smart contract" that runs on the peers and creates transactions. More broadly, it enables users to create transactions in the Hyperledger Fabric network's shared ledger and update the world state of the assets.
* Chaincode is programmable code, written in Go, and instantiated on a channel. Developers use chaincode to develop business contracts, asset definitions, and collectively-managed decentralized applications. The chaincode manages the ledger state through transactions invoked by applications. Assets are created and updated by a specific chaincode, and cannot be accessed by another chaincode.
* Applications interact with the blockchain ledger through the chaincode. Therefore, the chaincode needs to be installed on every peer that will endorse a transaction and instantiated on the channel.
* There are two ways to develop smart contracts with Hyperledger Fabric:
	* Code individual contracts into standalone instances of chaincode
	* (More efficient way) Use chaincode to create decentralized applications that manage the lifecycle of one or multiple types of business contracts, and let the end users instantiate instances of contracts within these applications.

### Lecture 191 - Chaincode Key APIs

* An important interface that you can use when writing your chaincode is defined by Hyperledger Fabric - [ChaincodeStub](https://godoc.org/github.com/hyperledger/fabric/core/chaincode/shim#Chaincode) and ChaincodeStubInterface. The ChaincodeStub provides functions that allow you to interact with the underlying ledger to query, update, and delete assets. The key APIs for chaincode include:
	* *func (stub *ChaincodeStub) GetState(key string) ([]byte, error)* : Returns the value of the specified key from the ledger. Note that GetState doesn't read data from the Write set, which has not been committed to the ledger. In other words, GetState doesn't consider data modified by PutState that has not been committed. If the key does not exist in the state database, (nil, nil) is returned.
	* *func (stub *ChaincodeStub) PutState(key string, value []byte) error* : Puts the specified key and value into the transaction's Write set as a data-write proposal. PutState doesn't affect the ledger until the transaction is validated and successfully committed.
	* *func (stub *ChaincodeStub) DelState(key string) error* : Records the specified key to be deleted in the Write set of the transaction proposal. The key and its value will be deleted from the ledger when the transaction is validated and successfully committed.

### Lecture 192 - Overview of a Chaincode Program

* When creating a chaincode, there are two methods that you will need to implement:
	* *Init* : Called when a chaincode receives an instantiate or upgrade transaction. This is where you will initialize any application state.
	* *Invoke* : Called when the invoke transaction is received to process any transaction proposals.
* As a developer, you must create both an  Init and an Invoke method within your chaincode. The chaincode must be installed using the *peer chaincode install* command, and instantiated using the *peer chaincode instantiate* command before the chaincode can be invoked. Then, transactions can be created using the *peer chaincode invoke* or *peer chaincode query* commands.

### Lecture 193 - Sample Chaincode Decomposed

* Let’s now walk through a sample chaincode written in Go, piece by piece:
```
package main

import (

"fmt"

"github.com/hyperledger/fabric/core/chaincode/shim"

"github.com/hyperledger/fabric/protos/peer"

)
```
* The *import* statement lists a few dependencies that you will need for your chaincode to build successfully.
	* *fmt* - contains *Println* for debugging/logging
	* [github.com/hyperledger/fabric/core/chaincode/shim](https://github.com/hyperledger/fabric/core/chaincode/shim) - contains the definition for the chaincode interface and the chaincode stub, which you will need to interact with the ledger, as we described in the Chaincode Key APIs section
	* [github.com/hyperledger/fabric/protos/peer](https://github.com/hyperledger/fabric/protos/peer) - contains the peer protobuf package.
```
type SampleChaincode struct {

}
```
* This might not look like much, but this is the statement that begins the definition of an object/class in Go. *SampleChaincode* implements a simple chaincode to manage an asset.
* Next, we’ll implement the Init method. Init is called during the chaincode instantiation to initialize data required by the application. In our sample, we will create the initial key/value pair for an asset, as specified on the command line:
```
func (t *SampleChaincode) Init(stub shim.ChainCodeStubInterface) peer.Response {

// Get the args from the transaction proposal

   args := stub.GetStringArgs()

if len(args) != 2 {

return shim.Error("Incorrect arguments. Expecting a key and a value")

}

// We store the key and the value on the ledger

err := stub.PutState(args[0], []byte(args[1]))

if err != nil {

return shim.Error(fmt.Sprintf("Failed to create asset: %s", args[0]))

}

return shim.Success(nil)

}
```
* The Init implementation accepts two parameters as inputs, and proposes to write a key/value pair to the ledger by using the *stub.PutState* function. *GetStringArgs* retrieves and checks the validity of arguments which we expect to be a key/value pair. Therefore, we check to ensure that there are two arguments specified. If not, we return an error from the Init method, to indicate that something went wrong. Once we have verified the correct number of arguments, we can store the initial state in the ledger. In order to accomplish this, we call the *stub.PutState* function, specifying the first argument as the key, and the second argument as the value for that key. If no errors are returned, we will return success from the Init method.
* Now, we’ll explore the Invoke method, which gets called when a transaction is proposed by a client application. In our sample, we will either get the value for a given asset, or propose to update the value for a specific asset.
```
func (t *SampleChaincode) Invoke(stub shim.ChaincodeStubInterface) peer.Response {

// Extract the function and args from the transaction proposal

fn, args := stub.GetFunctionAndParameters()

var result string

var err error

if fn == "set" {

result, err = set(stub, args)

} else { // assume 'get' even if fn is nil

result, err = get(stub, args)

}

if err != nil { //Failed to get function and/or arguments from transaction proposal

return shim.Error(err.Error())

}

// Return the result as success payload

return shim.Success([]byte(result))

}
```
* There are two basic actions a client can invoke: get and set.
	* The *get* method will be used to query and return the value of an existing asset.
	* The *set* method will be used to create a new asset or update the value of an existing asset.
* To start, we’ll call *GetFunctionandParameters* to isolate the function name and parameter variables. Each transaction is either a set or a get. Let's first look at how the *set* method is implemented:
```
func set(stub shim.ChaincodeStubInterface, args []string) (string, error) {

if len(args) != 2 {

return "", fmt.Errorf("Incorrect arguments. Expecting a key and a value")

}

err := stub.PutState(args[0], []byte(args[1]))

if err != nil {

return "", fmt.Errorf("Failed to set asset: %s", args[0])

}

return args[1], nil

}
```
* The set method will create or modify an asset identified by a key with the specified value. The set method will modify the world state to include the key/value pair specified. If the key exists, it will override the value with the new one, using the *PutState* method; otherwise, a new asset will be created with the specified value.
* Next, let's look at how the *get* method is implemented:
```
func get(stub shim.ChaincodeStubInterface, args []string) (string, error) {

if len(args) != 1 {

return "", fmt.Errorf("Incorrect arguments. Expecting a key")

}

value, err := stub.GetState(args[0])

if err != nil {

return "", fmt.Errorf("Failed to get asset: %s with error: %s", args[0], err)

}

if value == nil {

return "", fmt.Errorf("Asset not found: %s", args[0])

}

return string(value), nil

}
```
* The *get* method will attempt to retrieve the value for the specified key. If the application does not pass in a single key, an error will be returned; otherwise, the *GetState* method will be used to query the world state for the specified key. If the key has not yet been added to the ledger (and world state), then an error will be returned; otherwise, the value that was set for the specified key is returned from the method.
* The last piece of code in this sample is the main function, which will call the *Start* function. The *main* function starts the chaincode in the container during instantiation.
```
func main() {

err := shim.Start(new(SampleChaincode))

if err != nil {

fmt.Println("Could not start SampleChaincode")

} else {

fmt.Println("SampleChaincode successfully started")

}

}
```

## Section 5 - Chaincode Walkthrough (Demonstrated Scenario)

### Lecture 194 - Setting the Stage

* Now that we have a general idea of how chaincode is coded, we will walk through a simple chaincode that creates assets on a ledger, based on our demonstrated scenario of creating records for tuna fish.

Sometimes, code snippets can get lost in translation, especially if the context doesn’t make much sense. In hopes of avoiding this, we have adjusted our example chaincode to address our demonstration scenario. The chaincode we will be examining in this section will record a tuna catch by storing it to the ledger, as well as allow for queries and updates to tuna catch records.

## Lecture 195 - Defining the Asset Attributes

* Here are the four example attributes of tuna fish that we will be recording on the ledger:
	* Vessel (string)
	* Location (string)
	* Date and Time (datetime)
	* Holder (string).
* We create a Tuna Structure that has four properties. Structure tags are used by the *encoding/json* library.
```
type Tuna struct {

Vessel string ‘json:"vessel"’

Datetime string ‘json:"datetime"’

Location string ‘json:"location"’

Holder string ‘json:"holder"’

}
```

### Lecture 196 - Invoke Method

* As described earlier, the Invoke method is the one which gets called when a transaction is proposed by a client application. Within this method, we have three different types of transactions -- *recordTuna, queryTuna, and changeTunaHolder*, which we will look at a little later.
* As a reminder, Sarah, the fisherman, will invoke the *recordTuna* when she catches each tuna.
* *changeTunaHolder* can be invoked by Miriam, the restaurateur, when she confirms receiving and passing on a particular tuna fish as it passes through the supply chain. queryTuna can be invoked by Miriam, the restaurateur, to view the state of a particular tuna.
* Regulators will invoke *queryTuna* and queryAllTuna based on their need to verify and check for sustainability of the supply chain.
* We’ll be getting into the different tuna chaincode methods in the following sections. But here is the *Invoke* method. As you can see, this method will look at the first parameter to determine which function should be called, and invoke the appropriate tuna chaincode method.
```
func (s *SmartContract) Invoke(APIstub shim.ChaincodeStubInterface) sc.Response {

// Retrieve the requested Smart Contract function and arguments

function, args := APIstub.GetFunctionAndParameters()

// Route to the appropriate handler function to interact with the ledger appropriately

if function == "queryTuna" {

return s.queryTuna(APIstub, args)

} else if function == "initLedger" {

return s.initLedger(APIstub)

} else if function == "recordTuna" {

return s.recordTuna(APIstub, args)

} else if function == "queryAllTuna" {

return s.queryAllTuna(APIstub)

} else if function == "changeTunaHolder" {

return s.changeTunaHolder(APIstub, args)

}

return shim.Error("Invalid Smart Contract function name.")

}
```