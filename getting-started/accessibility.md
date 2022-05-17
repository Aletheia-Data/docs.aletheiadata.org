# Accessibility

### Desirable Characteristics of Decentralized Storage <a href="#desirable-characteristics-of-decentralized-storage" id="desirable-characteristics-of-decentralized-storage"></a>

While resiliency and efficiency are hallmarks of decentralized storage, there are a number of additional characteristics that an ideal storage system might offer:

**Accessible**

An ideal distributed system should be accessible. Participation in the network should be easy, allowing as many nodes as possible to store and distribute files on behalf of the network.

With [Filecoin](https://filecoin.io/), any relatively tech-savvy individual should be able to run a client node to interact with the network. As for running storage miner nodes (see [below](https://coinmarketcap.com/alexandria/article/what-is-decentralized-storage-a-deep-dive-by-filecoin#toc-case-study-how-filecoin-embodies-these-characteristics) for more information), it’s not something that everyone and their mom can do — you need to have hardware that meets certain specifications.

In the case of IPFS, nodes have lower hardware requirements, which means it is possible for many more users to contribute to the network by running a node (perhaps by running a web browser that came with one built in).

**Programmable**

Cloud service providers have made cheap and reliable storage easier than ever to work with. One major aspect of their success is the ability to provision and manage storage through code via APIs. Any competing system should be able to offer the same level of convenience.

**Content Addressing**

As discussed, URLs embody some inherent design tradeoffs. They describe the location of data, rather than its content.

To explain how centralized systems can make it hard to find a piece of data — imagine that you want to download a picture of a fluffy kitty. Consider these two URLs:

https://example1.com/cat.jpeg

https://example2.com/cat.jpeg

Each of these URLs references a file called cat.jpeg, but there’s no guarantee that these two files are the same. If example1.com goes offline, you can’t be sure that example2.com has what you’re looking for — its cat.jpeg could be entirely different. In fact, it could even be a picture of a dog! There’s no inherent relationship between a URL and content it references.

As a result, there’s no way for you to ask the internet of today, “Does anyone out there have this file?” because you don’t know anything about the file other than its location.

When you share files using a URL, things can go wrong. The server could start serving a different file from that URL, or someone could perform a (surprisingly not that rare) man-in-the-middle attack and alter the file. It’s very difficult to verify that everyone accessing the URL receives the file they wanted.

_Content addressing_, by contrast, finds files based on content identifiers (CIDs), which serve as files' digital fingerprints. Addressing files in this manner solves many issues with location addressing. When a client wants a file, instead of asking one server for a URL, they ask nodes in the network for a file with a particular CID. Once the client downloads the file, they fingerprint it themselves.

To revisit our previous example, it would be as if all websites had a shared understanding of what file to deliver when asked for cat.jpeg. So while it’s not a guarantee that any node has that particular cat.jpeg, the nodes will run a check for that file’s fingerprint to try to find a match.&#x20;

While a step like fingerprinting is something that would require more technical savvy than the average person would want to deal with, Filecoin and IPFS clients can easily automate this process. This lets the client guarantee that they received the file they asked for — in this system, it’s trivial to find alternate providers of a piece of data.&#x20;

The main takeaway: CIDs mean that you can find content that would otherwise be missing in a centralized system, and CIDs can also prevent man-in-the-middle attacks or a server suddenly changing a file at a particular URL.

**Trustless**

A trustless system enables cooperation between two parties without them having to know one another or look to a third party. Rather, the incentives of the system push actors towards the behavior necessary for the network to function.

**Verifiable**

An ideal storage system should make it easy to continuously prove that nodes are  storing the exact data they have promised. This type of auditability is key in achieving trustlessness. If you can always establish that data is being stored correctly, you have less need to trust the party providing the storage.

**Open**

Finally, an ideal distributed storage system is open: its code is open-source and auditable. Furthermore, the storage system should not be monolithic. Instead, it should expose an open protocol that anybody can implement and build upon, rather than encouraging lock-in.
