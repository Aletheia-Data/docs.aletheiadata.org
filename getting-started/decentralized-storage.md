# Decentralized Storage

Unlike a centralized server operated by a single company or organization, decentralized storage systems consist of a peer-to-peer network of user-operators who hold a portion of the overall data, creating a resilient file storage sharing system. These can be in a blockchain-based application or any peer-to-peer-based network.

When looking at decentralized storage (dStorage) options, there are a few things a user must keep in mind.

* [Persistence mechanism / incentive structure](decentralized-storage.md#persistence-mechanism-incentive-structure)
* [Data retention enforcement](decentralized-storage.md#data-retention)
* [Decentrality](decentralized-storage.md#decentrality)
* [Consensus](decentralized-storage.md#consensus)

### Persistence mechanism / incentive structure <a href="#persistence" id="persistence"></a>

#### Blockchain-based

For a piece of data to persist forever, we need to use a persistence mechanism. For example, on Ethereum, the persistence mechanism is that the whole chain needs to be accounted for when running a node. New pieces of data get tacked onto the end of the chain, and it continues to grow - requiring every node to replicate all the embedded data.

This is known as **blockchain-based** persistence.

Platforms with blockchain-based persistence:

* Ethereum
* [Arweave](https://www.arweave.org)

#### Contract-based

**Contract-based** persistence has the intuition that data cannot be replicated by every node and stored forever, and instead must be upkept with contract agreements. These are agreements made with multiple nodes that have promised to hold a piece of data for a period of time. They must be refunded or renewed whenever they run out to keep the data persisted.

In most cases, instead of storing all data on-chain, the hash of where the data is located on a chain gets stored. This way, the entire chain doesn't need to scale to keep all of the data.

Platforms with contract-based persistence:

* [Filecoin](https://docs.filecoin.io/about-filecoin/what-is-filecoin/)
* [Skynet](https://siasky.net)
* [Storj](https://storj.io)
* [0Chain](https://0chain.net)

****[**IPFS**](https://docs.ipfs.io/concepts/what-is-ipfs/) is a distributed system for storing and accessing files, websites, applications, and data. It doesn't have a built-in incentive scheme, but can instead be used with any of the contract-based incentive solutions above for longer-term persistence. Another way to persist data on IPFS is to work with a pinning service, which will "pin" your data for you. You can even run your own IPFS node and contribute to the network to persist your and/or other's data for free!\


### Data Retention

In order to retain data, systems must have some sort of mechanism to make sure data is retained.

#### Challenge mechanism <a href="#challenge-mechanism" id="challenge-mechanism"></a>

One of the most popular ways to make sure data is retained, is to use some type of cryptographic challenge that is issued to the nodes to make sure they still have the data. A simple one is looking at Arweave's proof-of-access. They issue a challenge to the nodes to see if they have the data at both the most recent block and a random block in the past. If the node can't come up with the answer, they are penalized.

Types of dStorage with a challenge mechanism:

* 0Chain
* Skynet
* Arweave
* Filecoin

### Decentrality <a href="#decentrality" id="decentrality"></a>

There aren't great tools to measure the level of decentralization of platforms, but in general, you'll want to use tools that don't have some form of KYC to provide evidence they are not centralized.

Decentralized tools without KYC:

* 0Chain (implementing a non-KYC edition)
* Skynet
* Arweave
* Filecoin
* IPFS
* Ethereum

### Consensus <a href="#consensus" id="consensus"></a>

Most of these tools have their own version of a [consensus mechanism](https://ethereum.org/en/developers/docs/consensus-mechanisms/) but generally they are based on either [**proof-of-work (PoW)**](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/) or [**proof-of-stake (PoS)**](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/).

PoW based:

* Skynet
* Arweave
* Ethereum

PoS based:

* [The Beacon Chain](https://ethereum.org/en/upgrades/beacon-chain/)
* Filecoin
* 0Chain

\
