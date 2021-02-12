## KOB Association Wallet(KOBAW)
The KOB Association Wallet is an association/organisational wallet for the city of Kochi. This holds the verifiable credentials about registered entities (organisations) under a particular jurisdiction. And this is a Web Application hosted on the Community Cloud for the City of Kochi.

The term "Wallet" is a data store for the DIDs and related information. For example, a person might have a mobile Agent app on their smart devices, while an Organization might have an enterprise Agent running on a Cloud Server. All Agents have a secure Wallet for storing identity data.

Every agent is paired with a digital wallet which is a key management system. This can be anything from a very simple static file on an embedded device to a highly sophisticated enterprise-grade key server. Regardless of the complexity, the job of a wallet is to safeguard sensitive data: key pairs, zero-knowledge proof blinded secrets, verifiable credentials, and any other cryptographic material needed to establish and maintain technical trust.

  ![wallet image](https://github.com/mariyachris/KOBAW/blob/master/wallet%20img.JPG)

# Understanding wallet

* A wallet is a mechanism of convenient control, not an exhaustive repository. 
* A wallet is portable. 
* A wallet is worth safeguarding. 
* Good wallets are organized so we can find things easily. 

# Implementation

The implementation of wallets guarantees proper encryption and secret-handling. It also provides some query features. Records (items) to be stored in a wallet are referenced by a public handle if they are secrets. This public handle might be a public key in a key pair, for example. Records that are not secrets can be returned directly across the API boundary.

With a technology that provides persistence and query features which could be a file system, an object store, an RDBMS, a NoSQL DB, a Graph DB, a key~value store, or almost anything similar is registered with the wallet by providing a series of C-callable functions (callbacks). The storage doesn’t have to worry about encryption at all; by the time data reaches it, it is encrypted robustly, and takes care of translating queries to and from encrypted form for external consumers of the wallet.

Searchability in wallets is facilitated with a tagging mechanism. Each item in a wallet can be associated with zero or more tags, where a tag is a key=value pair. Items can be searched based on the tags associated with them, and tag values can be strings or numbers. With a good inventory of tags in a wallet, searching can be robust and efficient.

# Benefits

* No single point of failure.
* Interoperability. 
* Portability. 
* Resilient trust infrastructure. 
* Key recovery. 

# Challenges

* This includes the difficult challenge of recovery after a device is lost or stolen or a wallet is hacked or corrupted. This is the province of decentralized key management.

* Since wallets are a major vector for hacking and cybersecurity issues, casual or fuzzy wallet requirements are a recipe for frustration or disaster. Divergent and substandard implementations could undermine security more broadly. This argues for as much design guidance and implementation help as possible.
 
* Wallets are also a unit of identity portability–if an identity owner doesn’t like how her software is working, she should be able to exercise her self- sovereignty by taking the contents of her wallet to a new service. This implies that wallets need certain types of interoperability in the ecosystem, if they are to avoid vendor lock-in.

* The wallets may need to manage hundreds of millions of relationships (in the case of large organizations)
