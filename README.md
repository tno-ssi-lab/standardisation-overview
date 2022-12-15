<!-- <style>H1{color:blue; font-weight:700}</style> -->
<!-- <style>H4{color:mediumblue; font-size:15px; font-weight:900}</style>
<style>H5{color:mediumblue; font-weight:900}</style> -->
<style>
      /* Whatever that is inside this <style> tag is all styling for your markup / content structure.
      /* The . with the boxed represents that it is a class */
      .boxed {
        background: #F2F2F2;
        color: black;
        border: 3px solid #535353;
        margin: 0px auto;
        width: 456px;
        padding: 10px;
        border-radius: 10px;
      }
    </style>

#  SSI Standardisation Overview
By [Maaike van Leuken](mailto:maaike.vanleuken@tno.nl) (TNO)\
Last revision: 12-12-2022

## Introduction

There is a large amount of standardisation developed and in development within the context of Self-Sovereign Identities (SSI). The standards and specifications vary from legacy technologies to new and upcoming technologies, from specifications on cryptographic signature schemes to usability and inclusivity concepts such as guardianship. Whenever looking into a standard or specification, it can be hard to place it in the bigger picture:
- What problem does this standard tackle?
- What is the context of this standard?
- Is this standard $x$ compatible with standard $y$?
- Are standards $x$ and $y$ competitors?

We have made a graphical overview of the situation giving an answer to most of these questions. See the image below.

![The graphical overview of standards and specifications related to SSI.](/images/overview.png "The graphical overview of standards and specifications related to SSI.")

The overview graphically answers the questions above more or less. This document will describe the structure of the graphical overview and give a description for each technology mentioned in the graphical display.

### Audience
This document is made in such a manner that it is accessible to all parties working with or wanting to work with SSI. We will explain each technology in the overview on a high level. For the technically inclined, links to the specification are given.

### Context and Continuation
Both this document and the graphical overview are living documents. The amount of specifications is ever-growing and updates of specifications are brought out periodically. We will try our best to keep our resources up-to-date. We are also very welcoming of input from technical experts on the standards and their context. If you have any suggestions or questions, please contact us.


### Outline and Structure of the Document
This document has been developed for the Dutch Blockchain Coalition (DBC) and has been verified with multiple technical experts.

## Description of the Model
The [Trust over IP model](https://trustoverip.org/toip-model/) is a very useful way to give insight in how an SSI solution can be build and of which layers it is built up. While looking through various specifications / standards, it seemed to make sense to arrange them according to the ToIP technology stack. Below you see the empty model, consisting of four layers. For each of these layers, we dedicate a section below and explain what the scope of the layer is, what technologies belong to the layer and a description of that technology. 

![The ToIP stack used to structure the overview of the standards.](/images/stack-background.png "The ToIP stack used to structure the overview of the standards.")

___
Standardisation body: []()\
Most recent version:\
Published on:\
Link: []()\
Competitive to:\
Compatible with:
___


### Layer 1: Trust Anchors
Trust anchors form the basis of the entire stack. Without a strong foundation to anchor your trust to, you cannot have trust in credentials that are exchanged in layer three etc. Technologies in this layer include identifiers, decentralized public key infrastructure and registries.

#### Identifier
An identifier is used to identify a party and this identifier can be authenticated by another party. Identifiers in this context are usually bound to a key somehow. Strong identifiers must be self-certifying, i.e. there should be a strong binding between key and identifier.

##### DID
- Standardisation body: [W3C](https://www.w3.org/)\
- Most recent version: v1.0\
- Published on: 19-07-2022\
- Link: [Decentralized Identifiers (DIDs)](https://w3c.github.io/did-core/)\
- Competitive with: other identifiers (X.509, link secrets)\
- Compatible with: DID Exchange Protocol, DID Comm, Present Proof Protocol, Issue Credential Protocol 


Decentralized identifiers that allow for the authentication of decentralized digital identities of a [DID subject](https://w3c.github.io/did-core/#did-subject). A DID is a URI that associates the DID subject with a DID document, which describes the DID subject and how they can authenticate themselves using cryptographic keys. DID documents are generated using a specific [DID method](https://w3c.github.io/did-spec-registries/#did-methods).

##### X.509
Standardisation body: [ITU](https://www.itu.int/en/Pages/default.aspx)\
Most recent version: (10/19)
Published on: 14-10-2019\
Link: [X.509](https://www.itu.int/rec/T-REC-X.509-201910-I/en)

##### Link Secret
Not a standard, but a cryptographic technique.
Based on [Pedersen commitments](https://www.cs.cornell.edu/courses/cs754/2001fa/129.PDF), see [link secrets](https://www.evernym.com/blog/how-does-a-verifier-know-the-credential-is-yours/).
#### Decentralized Public Key Infrastructure

##### KERI

#### Registry

#### Revocation Method

#### Attribute Schema

#### Credential Definition

#### OCA Definition
(?)
___

### Layer 2: Peer-to-Peer Connections
To exchange data, first a trusted (mutually) authenticated channel has to be set up. Peer-to-peer connections have to be established.

#### Protocols

##### DIDComm

##### DID Exchange Protocol

##### Open ID

##### Open ID Connect

##### Self-Issued OpenID Provider

___
### Layer 3: Credential Exchange Protocols 
Now that a connection tunnel has been set up, credentials can be exchanged. This layer is about the trust triangle (or diamond).

#### Issuer Protocol

##### Issue Credential Protocol

##### Credential Request (?)

##### OID4CI

#### Verifier Protocol

##### Present Proof Protocol

##### Presentation Request

##### OID4VP

#### Presentation Exchange

#### Signature Scheme

#### Credential Profile

Link to RWOT Credential Comparison Matrix + Paper

___
### Layer 4: Application Ecosystems
TBD

#### Delegation and Mandate

#### Guardianship

#### CHAPI

#### EASSI

#### Accessibility
