
| Title | KOB Association Wallet |
|--- | ---|
| Version | TBD |
| License | [Apache-2.0](https://github.com/asa1997/KochiOrgBook/blob/master/LICENSE), [Open Source](https://github.com/mariyachris/KOBAW/blob/master/LICENSE)|
| Author |  Christin Mariya  |


<br />

# The KochiOrgBook Association Wallet 

## Abstract   

KochiOrgBook Association Wallet(KOBAW) is an online directory that makes finding authentic and authoritative data about associations faster and easier. Association Wallet is a  searchable database, where the verifiable credentials of associations under the jurisdiction of Kochi are stored in a decentralized manner. The KOBAW provides all the services offered by a Association authorized to work in Kochi. If a citizen want to be part in an association then, a request for enrolling is moved from the KOB Connect App to KOB Association Wallet. KOBAW process various claim requests.

A claims holder (Association or KOBAW) would be expected to contain the following requirements:

* DIDs (references to decentralized IDs) that make up the wallet owner's identity, and context of those DIDs - e.g. for pair-wise DIDs, the connection to which that DID applies.
* The DIDs of your connections (e.g. your banks, stores, government services and so on)
* Verifiable credentials issued to you.
* Cryptographic materials - public and private keys associated with your DIDs, and possibly other materials such as (in the HL-Indy world) your Master Secret for requesting claims (to issuers) and providing proofs (to verifiers)

The KOBAW hold pieces of data(Veriable credentials of Associations) to be used for the  operations like accessing the services offered by various associations in the jurisdiction of Kochi. All the association are part of the KOB Verifiable Organization Network(KOB VON). These informations are stored in the KOB verifiable Credential Registry(KOB VCR). 

<br />

## Dependent Projects

* [KOB PIU](https://github.com/hyperledgerkochi/KOBPIU)
* [KOB VCR](https://github.com/hyperledgerkochi/KOBVCR)
* [KOB Search](https://github.com/hyperledgerkochi/KOBSearch)
* [KOB VON](https://github.com/hyperledgerkochi/KOBVON)

<br />

## Motivation

There are many associations working under the jurisdiction of Kochi. If one citizen / organization wants to access the services provided by these associations, they have to undergo a series of verification processes. Or if someone has to get membership from any of these associations, it is a problem to prove their identity. To get an association to be established they also have to go through many paperwork thus consuming much time and effort. The traditional way of storing all information about these associations is also a problem. Our aim is to streamline all the services provided by the associations working under the jurisdiction of Kochi, and to build transparency in accessing these services. KochiOrgBook (KOB) is a Digital Trust Ecosystem project for the city of Kochi
<br />

## Solution

The KOB Association Wallet is an online directory for Associations. It uses DIDs that enables peer-to-peer, secure messaging between two parties without a centralized authority. VCs are unforgeable digital versions of paper documents that we receive today. Using Identity Registry verifiers do not need to go to the original issuer to verify the information, instead we can use the proof provided by the holder combined with public cryptographic keys provided by an identity registry, which is usually implemented as a public blockchain. The KOB Association Wallet is designed for enterprises to store the identity information in a decentralized way. The users can access the services from anywhere at any time, making the wallet a user compatible facility. The Association wallet safeguard sensitive data: key pairs of associations, zero-knowledge proof blinded secrets, verifiable credentials of the associations, and any other cryptographic material needed to establish and maintain technical trust. 

<br />

## Workflow of Kochi OrgBook
<br />

![workflow](docs\img\context_diagram.png "CONTEXT DIAGRAM")<br />

The service defines and publishes any pre-requisite authorizations/credentials an association must have before applying for a credential from the service. For example, an association might need to prove they are a registered entity, have a tax number, and insurance. An association applies for the credential, typing information about the pre-requisites and any other data needed by the service before reviewing the application. Normally, the association would also pay a fee for the application process and/or for the authorization itself. The person submitting the application might also need to prove they have the authority to act on behalf of the applying association. The service validates the application information provided and makes a decision to issue (or not) the authorization to the association. If the authorization is approved, the service provides the association with a document - a permit/ licence/ registration - that they can use to prove to others that the association has that authority. The association might display the authorization on the wall and/or might take it to others to prove it was issued. For example to a bank for use in a business loan application process. 
 
All these authorized associations are stored in the association wallet, and each association is a part of the KOB verifiable Organization Network. If a citizen want to be part of an association, first he establishes a connection to KOBAW through the KOB Connect App. Citizen will have all their proofs in their KOBConnect Wallet. Satisfying the required proofs will allow the citizen to be part of an association and these are done by the approving authority. All the details of these verifiable credentials and proofs are stored in the KOB VCR(Verifiable Credential Registry).
 
The KOB Association wallet, KOB Verifiable Credential Register, KOB Verifiable Organization Network and other services are hosted in the Community Cloud Of Kochi OrgBook (KOBCC) 



## Usecase of KOB Association Wallet
<br />

![Usecase of KOBAW](docs\img\usecase.png "USECASE DIAGRAM")

The KOB Association Wallet is a searchable database. The search is implemented using Solr. KOBAW provides all the services offered by the associations. They are accessed through a service provider. A request to service provider is passed by the approving authority which is the officials from the associations. The main services include :

* Requesting Membership
* Requesting Approval
* Request association services
* Communication with associations
* Association Administration

<br />

## Sequence Diagram

![Sequence-diagram](docs\img\sequencediagram.png "SEQUENCE DIAGRAM")<br />

The sequence diagram of KOB Associations wallet explains about the interaction between various projects in the KOB. The request from the user is first moved to the interface. If it is a request for credential then it is moved to the credential issuer. They verify the credentials or they can generate the credential. Then the issued credential is then moved to the interface. All the verifiable credentials are stored in the KOB VCR. Whenever a request from the web application has occurred they show the list of credentials using the Association Wallet.

## Target audience of KOBAW

The main target audience of Association Wallet are the Registered organisations/ associations in the city of Kochi such as:
* Bar Councils
* Cultural Societies
* Universities
* RTO
* Management Associations
* Medical Associations
* Drivers Associations


## Works completed

* BC OrgBook case study
* Understand the workflow of OrgBook
* Install Docker, Docker compose. S2I
* Run reference project in local system
* Started UI design
  

## Works to be done

* Database connection
* Connect with Public Utility Identity (KOB PIU)
* Integrate search using Solr (KOB Search)
* Accessing VC from Verifiable credential Registry (KOB VCR)
* Establish connection with Approving authority


## Status of the project

Active

## Contributors

[Christin Mariya](https://github.com/mariyachris)

## Testing the project

*TBD*

# References

* [OrgBook BC](https://www.orgbook.gov.bc.ca/en/home)
* [Edx Course - Introduction to Hyperledger Sovereign Identity Blockchain Solutions](https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS172x+3T2019/home)
