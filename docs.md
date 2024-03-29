<style>
    p {
        text-align: justify;
    }
</style>

#  [DRAFT] SSI Standardisation Overview
By [Maaike van Leuken](mailto:maaike.vanleuken@tno.nl) (TNO)\
Last revision: 06-04-2023
___
## Glossary

**Standard**: a *neat* document written by a **standardisation body** in which a **technology** is defined.

**Specification**: a *neat* document in which a **technology** is defined. The difference with a standard is that the document was not written by a recognised **standardisation body**.

**Standardisation body**: W3C, DIF, OIDF, Aries, ... 

**Technology**: a technical protocol, concept, architecture, ... that can be used to achieve a certain goal.

**Revocation mechanism**

**Credential profile**

**Proof format**: the cryptographic algorithm used to make a proof in the creation of the presentation. Examples of proof formats are JWS, Ed25519, ECDSA, RSA, ... .

**Credential format**: the format along which the claims are structured, such as JSON, JSON-LD, ABC, ... .

The term **ID token** is used as defined in the [OIDC Terminology](https://openid.net/specs/openid-connect-core-1_0.html#Terminology).

The term **VP token** is used as defined in the [OIDC4VP standard](https://openid.net/specs/openid-connect-4-verifiable-presentations-1_0-07.html#name-vp_token).

The terms **credential**, **claim**, **presentation**, **verifiable credential** and **verifiable presentation** are used as defined in the [W3C VC Data Model Glossary](https://www.w3.org/TR/vc-data-model/#terminology).

The terms **credential application** and **credential response** are used as defined in the [DIF Credential Manifest Glossary](https://identity.foundation/credential-manifest/#terminology).

The terms **self-sovereign identity**, **issuer**, **holder**, **verifier**, **subject**, **party**, **delegation**, **mandate** ... are defined in the [eSSIF-Lab Glossary](https://essif-lab.github.io/framework/docs/essifLab-glossary).

The terms **self-certifying identifier** and **self-authenticated identifier** are used as defined in [tbd](#tbd).

The terms **identifier**, **link secret**, **presentation definition** and **presentation submission** are defined in the [DIF Presentation Exchange Terminology](https://identity.foundation/presentation-exchange/#terminology).

The terms **mdoc**, **mDL**, **mDL reader** and **mDL holder** are used as defined in [ISO/IEC 18013-5:2021 (mDL)](https://www.iso.org/standard/69084.html).
___

## Abbreviations

DID

DPKI

SSI

OIDC

DDIP

AIP

<!-- will be a long long list -->


___

## Introduction

There is a large amount of standardisation developed and in development within the context of **Self-Sovereign Identities (SSI)**. The **standards** and **specifications** vary from legacy technologies to new and upcoming technologies, from specifications on cryptographic signature schemes to usability and inclusivity concepts such as guardianship. Whenever looking into a standard or specification, it can be hard to place it in the bigger picture:
- What does the technology described in the standard achieve?
- What is the context of this technology and its standard?
- Is this standard $x$ compatible with standard $y$?
- Are standards $x$ and $y$ competitors?

We have made a graphical overview of the situation trying to answer these questions, which can be found [here](https://maaikevanleuken.github.io/SSI-Standardisation-Overview/). Here you see the basic model. To answer the questions above, we want to give the relation between various technologies. This becomes fuzzy quickly. To keep it uncluttered, we have made buttons on the bottom that can be used to toggle specific views.
- *General* shows the general interactions between technologies, that is, without choosing a specific technology.
- *DIDComm* shows the DIDComm-based technologies.
- *OIDC* shows the OIDC-based technologies.
- *DDIP* shows the [Dutch Decentralised Interoperability Profile](https://github.com/DutchBlockchainCoalition/DDIP).
- *AIP* shows the [Aries Interop Profile](https://github.com/hyperledger/aries-rfcs/blob/main/concepts/0302-aries-interop-profile/README.md).

<!-- ![The graphical overview of standards and specifications related to SSI.](/images/overview.png "The graphical overview of standards and specifications related to SSI.") -->

The overview graphically answers the questions above more or less. This document will describe the structure of the graphical overview and give a description for each technology mentioned in the graphical display.

### Audience
This document is made in such a manner that it is accessible to all parties working with or wanting to work with SSI. We will explain each technology in the overview on a high level. Links to the specification are given for further (more technical) reading.

### Context and Continuation
This document has been developed for the Dutch Blockchain Coalition (DBC) and has been discussed with multiple technical experts.

<!-- Relation with interop profiles such as DDIP and AIP -->

Both this document and the graphical overview are living documents. The amount of specifications is ever-growing and updates of specifications are brought out periodically. We will try our best to keep our resources up-to-date. We also welcome any input from technical experts on the standards and their context. If you have any suggestions or questions, please contact us.
___
## Description of the Model
The [Trust over IP (ToIP) model](https://trustoverip.org/toip-model/) consists of two stacks: the technology stack and the governance stack. We will here restrict ourselves to the technology stack, since we aim to give context for *technologies*. The stack consists of the following four layers:
1. *Public utilities*. This forms the basis for the other layers through defining trust anchors such that the technologies in this layer create a trusted basis.
2. *Peer-to-peer communication*. This layer defines the (private) digital wallets and agents, such that **credentials** can be stored and exchanged, via peer-to-peer protocols.
3. *Trust task protocols*. This is the *trust triangle* comes into play and the credentials are exchanged. 
4. *Application ecosystems*. This layer defined market applications built on top of the other layers.

![The two stacks in the ToIP model.](/images/toip.jpg "The two stacks in the ToIP model.")

While looking through various specifications / standards, it seemed to make sense to arrange them according to the ToIP technology stack, as they seem to fit into these layers. We have made some small alterations to the layers in the ToIP technology stack, such that the scope is broadened (wider than just DID-based methods) and renamed the layers such that the fit our purpose better. The result is displayed below.  

![The four layers from the ToIP stack used to structure the overview of the standards.](/images/stack-background.png "The four (altered) layers from the ToIP stack used to structure the overview of the standards.")

For each of these layers, we dedicate a chapter below and explain what the scope of the layer is, what technologies belong to the layer. For each of the technologies we will
- list some general information about the standard:
  - the standardisation body
  - the most recent version
  - when the most recent version was published
  - a link to the standard
  - the technologies it is competitive to
  - the technologies it is compatible with
- give a short description of what the technology does



<!-- Standardisation body: []()\
Most recent version:\
Published on:\
Link: []()\
Competitive to:\
Compatible with: -->

<!-- 
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

| Standardisation body  | Content Cell  |
| ------------- | ------------- |
| Most recent version  | Content Cell  |
| Published on  | Content Cell  |
| Link  | Content Cell  |
| Compatible with  | Content Cell  |
| Competitive with  | Content Cell  |
-->

### Layer 1: Trust Anchors
Trust anchors form the basis of the entire stack. Without a strong foundation to anchor your trust to, you cannot have trust in the information communicated on the higher layers, i.e. the credentials exchanged in layer 4. Technologies in layer 1 include [identifiers](#-id-), [decentralised public key infrastructure](#-dpki-) and [registries](#-registries-).

#### Identifier {#-id-}
An **identifier** is used to identify a party in a certain context. This identifier can be authenticated by another party. Strong identifiers must be **self-certifying**, i.e. there should be a strong binding between the key and the corresponding identifier.

##### Decentralised Identifier {#-did-}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div><a href="https://www.w3.org/">W3C</a></div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>v1.0</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>19-07-2022</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div><a href="https://w3c.github.io/did-core/">Decentralised Identifiers (DIDs)</a></div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-x509-">X.509</a>, 
    <a href="#-link-secret-">link secret</a>, 
    <a href="#-raw-public-key-">raw public key</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-did-exchange-protocol-">DID Exchange Protocol</a>, 
    <a href="#-didcomm-">DIDComm</a>, 
</div> 
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with</div> 
<div>
    <a href="#-issue-credential-protocol-">Issue Credential Protocol,</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with</div>
<div>
    <a href="#-presentation-exchange-">Presentation Exchange,</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with</div> 
<div>
    <a href="#-present-proof-protocol-">Present Proof Protocol</a>
</div>  
<br></br>

Decentralised identifiers (DIDs) allow for the authentication of decentralised digital identities of a [DID subject](https://w3c.github.io/did-core/#did-subject). A DID is a URI that associates the DID subject with a DID document, which describes the DID subject and how they can authenticate themselves using cryptographic keys. By resolving the DID Document, a sender can find the endpoint where to reach the receiver and the public key that the receiver will use in the communication with the sender. DID documents are generated using a specific [DID method](https://w3c.github.io/did-spec-registries/#did-methods). It depends on the DID method whether the DID is a **self-certifying identifier**. 

A DID can be a global unique identifier, but parties can also have multiple ([peer](https://identity.foundation/peer-did-method-spec/))DIDs to separate domains/personas. 

##### X.509

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://www.itu.int/en/Pages/default.aspx">ITU</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    10/19
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    14-10-2019
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://www.itu.int/rec/T-REC-X.509-201910-I/en">X.509</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-did-">DID</a>,
    <a href="#-link-secret-">link secret</a>,
    <a href="#-raw-public-key-">raw public key</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc-">OIDC</a>
</div>
<br></br>

X.509 certificates are very widely used to define the binding between a party's (partial) identity and a public key. This certificate can be signed by a certificate authority, such as is done for protocols like TLS in HTTPS. X.509 certificates can also be self-signed. Since you can put attributes in the certificate, X.509 certificates can also be used as [credential](#-credential-) format.

##### Link Secret

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-did-">DID</a>, 
    <a href="#-x509-">X.509</a>, 
    <a href="#-raw-public-key-">raw public key</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">AnonCred</a>, 
    <a href="#-didcomm-">DIDComm</a>
</div> 
<br></br>

A link secret is a non-correlatable secret only known to the holder. During credential issuance, the link secret is sent as a blind attribute to the issuer. The issuer thus doesn't know the value of the link secret. The issuer can then sign all claims, including the blinded link secret. The holder can prove ownership over the credentials to a verifier without disclosing a persistent identifier.

Not a standard, but a cryptographic technique.
Based on [Pedersen commitments](https://www.cs.cornell.edu/courses/cs754/2001fa/129.PDF), see [link secrets](https://www.evernym.com/blog/how-does-a-verifier-know-the-credential-is-yours/).

##### Raw Public Key
Raw public keys can be used as an identifier. 


##### Recovery

https://sovrin.org/wp-content/uploads/2019/03/What-if-someone-steals-my-phone-110319.pdf

#### Decentralised Public Key Infrastructure {#-dpki-}
As the name suggests, this is the decentralised version of the classic, centralised public key infrastructure. The decentralisation ensures that no single party can compromise the integrity and security of the system as a whole. In decentralised PKI, there is no need to have a trusted third party.

##### Key Event Receipt Infrastructure {#-keri-}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">Web of Trust</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    N.A.
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    16-07-2022
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://weboftrust.github.io/ietf-keri/draft-ssmith-keri.html">KERI</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    PKI
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-did-">DID</a>
</div> 
<br></br>

KERI is a novel technology for Decentralised Key Management Infrastructure (DKMI). It has been brought under in an informational standard.
The primary operation for key management is key rotation, that can be performed using key event receipt logs (KERL).

The trust is rooted in self-certifying identifiers. 


#### Registry {#-registry-}
A registry is used to store information that could be checked by anyone. To provide more protection against malicious modifications and a single-point of failure, this registry should be implemented in a decentralised fashion. Decentralised Ledger Technologies (DLTs), such as a blockchain, can be used for this. Note that SSI solution do not necessarily require the usage of DLTs. [IRMA](https://irma.app/) for example is a ledger-less SSI solution.

##### Distributed Ledger Technology {#-dlt-}
A blockchain is a distributed database, without a single point of failure or a single central authority that you must trust, leading to a higher level of privacy and security.

###### Hyperledger
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-"></a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-distributed-ledger-technology-">Other DLTs</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-did-">DID</a>
</div> 
<br></br>
Hyperledger is a collection of projects related to DLTs and creates open-source DLT. Hyperledger falls under guardianship of the Linux Foundation.

###### European Blockchain Services Infrastructure {#-ebsi-}

<div style="width:250px; height:auto; float:left">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-distributed-ledger-technology-">Other DLTs</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-trusted-issuer-">Trusted Issuer</a>
</div> 
<br></br>

The European Blockchain Services Infrastructure (EBSI) is a European consortium that created a blockchain for the public sector. 

##### Registry Applications
<!-- Explain in bullet points as these are not standards. -->

###### Identifier

###### Schema

###### Revocation

###### Delegation

###### Trusted Issuer
Link Oskar

In the [mDL](#-mobile-driving-license-) standard, the notion of Verified Issuer Certificate Authority List (VICAL) is introduced. This list can be used as a trust anchor for verifiers.

###### Trusted Verifier
Link Oskar

###### Trusted App

#### Revocation Method

##### Revocation List
Status List 2021
<!-- if standard &rarr; table, otherwise just listed. -->

##### Cryptographic Accumulator

https://link.springer.com/content/pdf/10.1007/978-3-642-00468-1_27.pdf

https://github.com/hyperledger/anoncreds-spec/blob/main/spec/ursaAnonCreds.pdf

https://github.com/hyperledger/indy-sdk/blob/main/docs/concepts/revocation/cred-revocation.md

#### OCA Definition
(?)
___

### Layer 2: Peer-to-Peer Connection
To exchange data, first a trusted (mutually) authenticated channel has to be set up. Peer-to-peer connections have to be established between agents of the communicating parties.

#### Peer-to-Peer Protocol
A peer-to-peer protocol establishes a secure and private communication between [](#-agent-).

##### DIDComm
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://identity.foundation/">DIF</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    v2.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://identity.foundation/didcomm-messaging/spec/">DIDComm Messaging</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-openid-connect">OIDC</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-did-">DID</a>,
    <a href="#-did-exchange-protocol-">DID exchange protocol</a>,
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div>
<div>
    <a href="#-issue-credential-protocol-">issue credential protocol</a>,
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div>
<div>
    <a href="#-present-proof-protocol-">present proof protocol</a>,
</div> 
<br></br>

By resolving the DID Document, a sender can find the endpoint where to reach the receiver and the public key that the receiver will use in the communication with the sender. 

Various message types are defined: 
- DIDComm plaintext messages
- DIDComm signed messages
- DIDComm encrypted messages

<!-- Messages are explained, where is the protocol explained? -->

##### DID Exchange Protocol
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://github.com/hyperledger/aries-rfcs">Aries RFC</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    15-04-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://github.com/hyperledger/aries-rfcs/blob/main/features/0023-did-exchange/README.md">DID Exchange Protocol 1.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-didcomm-">DIDComm</a>
</div> 
<br></br>

##### OpenID Connect {#-oidc-}
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://openid.net/foundation/">OpenID Foundation</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    08-11-2014
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://openid.net/specs/openid-connect-core-1_0.html">OpenID Connect Core 1.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-didcomm-">DIDComm</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-siop-">SIOP</a>, 
    <a href="#-oidc4ci-">OIDC4CI</a>, 
    <a href="#-oidc4vp-">OIDC4VP</a>, 
    <a href="#--">presentation exchange</a>
</div> 
<br></br>
Used in many systems. Less or no migration needed compared to moving to a DIDComm-based system


##### Self-Issued OpenID Provider {#-siop-}
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://openid.net/foundation/">OpenID Foundation</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    v2
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    18-12-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://openid.net/specs/openid-connect-self-issued-v2-1_0-06.html">Self-Issued OpenID Provider</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc-">OIDC</a>
</div> 
<br></br>

#### Agent {#-agent-}

##### Wallet

###### Wallet Rendering

###### DKMS


___
### Layer 3: Credential Exchange Protocols 
Now that a connection tunnel has been set up, credentials can be exchanged. This layer is about the trust triangle (or diamond).

#### Issuance Protocol
This section describes protocols related to the issuance of credentials. We describe to standards to do so. Additionally, we also discuss the credential manifest.

##### Issue Credential Protocol
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://identity.foundation/">DIF</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    3.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    27-10-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://github.com/decentralized-identity/waci-didcomm/blob/main/issue_credential/README.md">Issue Credential Protocol 3.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-oidc4ci-">OIDC4CI</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-did-">DID</a>, <a href="#-link-secret">link secret</a>, <a href="#-DIDComm-">DIDComm</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div> 
<div>
    <a href="#-didcomm-">DIDComm</a>,
    <a href="#-did-exchange-protocol-">DID exchange protocol</a>, <a href="#-present-proof-protocol-">present proof protocol</a>
</div>
<br></br>

This standard formalizes the protocol to issue credentials by specifying the following four messages in the protocol:
- Holder &rarr; issuer: what credential the holder would like to receive from the issuer.
- Issuer &rarr; holder: offer the credential and possibly its notify the price.
- Holder &rarr; issuer: request the credential.
- Issuer &rarr; holder: issue the credential.

The **proof type** can be JWT, JSON-LID or ZKP.


##### OpenID Connect for Verifiable Credential Issuance {#-oidc4ci-}
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://openid.net/foundation/">OpenID Foundation</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    30-12-2022
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html">OpenID for Verifiable Credential Issuance</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-issue-credential-protocol-">issue credential protocol</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc-">OIDC</a>, 
    <a href="#-siop-">SIOP</a>, 
    <a href="#-mdl-">mDL</a>, 
    <a href="#-verifiable-credential-">VC</a>
</div> 
<br></br>

This standard describes an API for credential issuance via OIDC (and OAuth2.0), by defining what the **credential offer** and **credential offer response** should look like.  
The **proof type** must be JWT.

##### Credential Manifest

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://identity.foundation/">DIF</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    0.0.1
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://identity.foundation/credential-manifest/">Credential Manifest</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    JSON-based credentials, 
    <a href="#-oidc4ci-">OIDC4CI</a>,
    <a href="#-issue-credential-protocol-">issue credential protocol</a>,
</div> 
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div> 
<div>
    <a href="#-chapi-">CHAPI</a>
</div> 
<br></br>

In order for the issuer to send the soon-to-be holder a credential, the issuer needs to know some information about the subject. This specification a data format named the **credential manifest**, describing the inputs a subject must provide to an issuer in which format, in order for the issuer to determine whether to issue the credential to the subject. The subject, i.e. the user agent, discovers the credential manifest and can then form a **credential application**, containing the information on the subject that the issuer needs. The issuer can then determine whether this application is accepted or declined and sends a **credential response**. The formats for the credential application and credential response are also specified in this standard.

We assume that the credential manifest is **claim format** and transport envelope agnostic, just like the formats in [presentation exchange](#-presentation-exchange-). However, this has not been clearly specified in this standard, but there are some hints.


The credential manifest is the issuance equivalent to the **presentation definition** specified in [presentation exchange](#-presentation-exchange-).

#### Verification Protocol

##### Present Proof Protocol
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://identity.foundation/">DIF</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    3.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    22-06-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://github.com/decentralized-identity/waci-presentation-exchange/blob/main/present_proof/present-proof-v3.md">Present Proof Protocol 3.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-openid-connect4vp">OIDC4VP</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-didcomm">DIDComm</a>,
    <a href="#-issue-credential-protocol">issue credential protocol</a>, 
    <a href="#-presentation-exchange">presentation exchange</a>
</div> 
<br></br>

This standard formalizes the protocol for presentation exchange by specifying the following three messages in the protocol:
- Prover &rarr; verifier: propose what the presentation would look like.
- Verifier &rarr; prover: request a presentation.
- Prover &rarr; verifier: provide the presentation.


##### OpenID Connect for Verifiable Presentations {#-oidc4vp-}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://openid.net/foundation/">OpenID Foundation</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    17-12-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://openid.net/specs/openid-connect-4-verifiable-presentations-1_0-07.html">OpenID Connect for Verifiable Presentations</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#-present-proof-protocol">present proof protocol</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc4ci-">OIDC4CI</a>, <a href="#-self-issued-openid-provider">SIOP</a>,
    <a href="#-presentation-exchange">presentation exchange</a>, <a href="#-vp">VP</a>
</div> 
<br></br>

OIDC for Verifiable Presentations is, as the name suggests, an extension to OIDC allowing the exchange of verifiable presentations (in a **VP token**) in addition to an **ID token**. The standard defines the protocol for this, by defining what the request and response must look like.

##### Presentation Exchange

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://identity.foundation/">DIF</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    2.0.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://identity.foundation/presentation-exchange/spec/v2.0.0/">Presentation Exchange 2.0.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    JSON-based credentials, 
    <a href="#-oidc4vp-">OIDC4VP</a>,
    <a href="#-present-proof-protocol-">present proof protocol</a>,
</div> 
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div> 
<div>
    <a href="#-chapi-">CHAPI</a>
</div> 
<br></br>

In order for the holder to send the verifier a presentation, the holder needs to know (1) the verifier's proof requirements and (2) how to formulate the proof according to the requirements. This specification defines two data formats: 
1. A **presentation definition** format for the verifier's proof requirements. A presentation definition defines which **proof formats** are allowed, and optionally a set of selection rules or a purpose.
2. A **presentation submission** format for the holder to formulate proofs. It shows how the presented inputs are in accordance with the requirements specified in the presentation definition. 

These formats are **claim format** and transport envelope agnostic, as long as the claim format can be serialized as JSON.

The presentation definition is the verification equivalent of the [credential manifest](#-credential-manifest-).

##### Device Binding Attachments
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://github.com/hyperledger/aries-rfcs">Aries RFC</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    07-04-2022
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://github.com/hyperledger/aries-rfcs/tree/main/features/0728-device-binding-attachments">Aries RFC 0728: Device Binding Attachments</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="">SECDSA</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-present-proof-protocol">present proof protocol</a>,
    <a href="#-anoncred-">AnonCred</a>
</div> 
<br></br>

#### Credential
Overview: Link to RWOT Credential Comparison Matrix + Paper.

In the next sections we will describe the credential formats that are standardised. Note that these still have a lot of degrees of freedom in there, as choices can be made in the used signature algorithm, revocation mechanism, identifiers... 

##### Verifiable Credential

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://www.w3.org/">W3C</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    v1.1
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    03-03-2022
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://www.w3.org/TR/vc-data-model/">Verifiable Credentials Data Model v1.1</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">other credential formats</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc4ci-">OIDC4CI</a>, 
    <a href="#-oidc4vp-">OIDC4VP</a>, 
    <a href="#-issue-credential-protocol-">issue credential protocol</a>,
</div>
<div style="width:250px; height:auto; float:left; display:inline; opacity:0">Compatible with:</div> 
<div>
    <a href="#-present-proof-protocol-">present proof protocol</a>
</div> 
<br></br>

The data model defines the terms **claim**, **credential** and **presentation** that form the basis for the verifiable credentials. Verifiable credentials and verifiable presentations are defined by giving a format on how to specify them.
The standard for Verifiable Credentials leaves some room for choices in **claim format** (JSON vs JSON-LD) and **proof format** (JWT vs linked data proofs).

<!-- ##### Verifiable Presentation

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

The standard for Verifiable Presentations (VPs) leaves some room for choices in credential (JSON vs JSON-LD) and proof (JWT vs linked data proofs) format. -->

##### Mobile Document {#-mdoc-}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">ISO</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    xx-09-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://www.iso.org/standard/69084.html">ISO/IEC 18013-5:2021</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">other credential formats</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#-oidc4ci-">OIDC4CI</a>, 
    <a href="#-oidc4vp-">OIDC4VP</a>,
    <a href="#-vical-mdoc-">VICAL</a>
</div> 
<br></br>

The standard specifies the implementation of a driving license in association with a mobile device, through specifying amongst others:
- the interface between the **mDL** and the **mDL reader**
- the interface between the **mDL reader** and the issuing authority infrastructure
- how to tie the **mDL** to the **mDL holder** (where the holder must be equal to the **data subject**), through the use of a portrait image of the **mDL holder**.

The credential format used for the mDL is the MDOC.
<!-- Link to MDOC? -->


##### AnonCred {#-anoncred-}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>


___
### Layer 4: Application Ecosystems
TBD

#### Delegation and Mandate
It's very useful to be able to delegate and mandate rights and duties towards a third party to for example an employee.

##### Authentic Chained Data Containers {#-acdc}

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://wiki.trustoverip.org/display/HOME/Trust+over+IP+Foundation">ToIP Foundation</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    25-04-2022
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://www.ietf.org/archive/id/draft-ssmith-acdc-01.html">Authentic Chained Data Containers (ACDC)</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

The ACDC protocol aims to provide granular provenanced proof-of-authorship of the data contained via a chain of linked ACDCs. It allows for delegation of credentials by setting up a verifiable chain-of-custody.

Variant of VC
KERI
JSON
claim formats: JSON, CBOR, MGPK, CESR

##### ZCap

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

##### Chained Credential

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

#### Guardianship
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

#### Credential Handler API {#-chapi-}
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="https://www.w3.org/">W3C</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    1.0
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    23-06-2021
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="https://w3c-ccg.github.io/credential-handler-api/">Credential Handler API 1.0</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href="#--">-</a>
</div> 
<br></br>

#### EASSI
<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>
    -
</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div>
    <a href="-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div>
    <a href="#--">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    A variety of wallets
</div> 
<br></br>

#### Accessibility

## To Research
- Sovrin governance & trust framework
- Decentralised file system?
- Timestamping
- Presentation definition and submission
- Gordian envelopes