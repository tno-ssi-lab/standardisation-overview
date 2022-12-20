#  SSI Standardisation Overview
By [Maaike van Leuken](mailto:maaike.vanleuken@tno.nl) (TNO)\
Last revision: 12-12-2022
___
## Introduction

There is a large amount of standardisation developed and in development within the context of Self-Sovereign Identities (SSI). The standards and specifications vary from legacy technologies to new and upcoming technologies, from specifications on cryptographic signature schemes to usability and inclusivity concepts such as guardianship. Whenever looking into a standard or specification, it can be hard to place it in the bigger picture:
- What problem does this standard tackle?
- What is the context of this standard?
- Is this standard $x$ compatible with standard $y$?
- Are standards $x$ and $y$ competitors?

We have made two graphical overviews of the situation answering most of these questions:
- [Basic graphical overview](https://whimsical.com/overview-HAJbEJrV4RH5VbJ6UEURwF)
- [Graphical overview with interconnections](tbd)

<!-- ![The graphical overview of standards and specifications related to SSI.](/images/overview.png "The graphical overview of standards and specifications related to SSI.") -->

The overview graphically answers the questions above more or less. This document will describe the structure of the graphical overview and give a description for each technology mentioned in the graphical display.

### Audience
This document is made in such a manner that it is accessible to all parties working with or wanting to work with SSI. We will explain each technology in the overview on a high level. For the technically inclined and completeness, links to the specification are given.

### Context and Continuation
This document has been developed for the Dutch Blockchain Coalition (DBC) and has been verified with multiple technical experts.

<!-- Relation with interop profiles such as DDIP and AIP -->

Both this document and the graphical overview are living documents. The amount of specifications is ever-growing and updates of specifications are brought out periodically. We will try our best to keep our resources up-to-date. We also welcome any input from technical experts on the standards and their context. If you have any suggestions or questions, please contact us.
___
## Description of the Model
The [Trust over IP model](https://trustoverip.org/toip-model/) is a very useful way to give insight in how an SSI solution can be build and of which layers it is built up. While looking through various specifications / standards, it seemed to make sense to arrange them according to the ToIP technology stack. Below you see the empty model, consisting of four layers. For each of these layers, we dedicate a section below and explain what the scope of the layer is, what technologies belong to the layer and a description of that technology. 

![The ToIP stack used to structure the overview of the standards.](/images/stack-background.png "The ToIP stack used to structure the overview of the standards.")

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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>
-->


### Layer 1: Trust Anchors
<div style="text-align: justify">Trust anchors form the basis of the entire stack. Without a strong foundation to anchor your trust to, you cannot have trust in credentials that are exchanged in layer three etc. Technologies in this layer include identifiers, decentralized public key infrastructure and registries.</div>

#### Identifier
<div style="text-align: justify"> An identifier is used to identify a party and this identifier can be authenticated by another party. Identifiers in this context are usually bound to a key somehow. Strong identifiers must be self-certifying, i.e. there should be a strong binding between key and identifier.</div>

##### DID

<div style="width:250px; height:auto; float:left; display:inline">Standardisation body:</div> 
<div><a href="https://www.w3.org/">W3C</a></div>
<div style="width:250px; height:auto; float:left; display:inline">Most recent version:</div> 
<div>v1.0</div>
<div style="width:250px; height:auto; float:left; display:inline">Published on:</div> 
<div>19-07-2022</div>
<div style="width:250px; height:auto; float:left; display:inline">Link:</div> 
<div><a href="[-](https://w3c.github.io/did-core/)">Decentralized Identifiers (DIDs)</a></div>
<div style="width:250px; height:auto; float:left; display:inline">Competitive to:</div> 
<div><a href="#x509">X.509</a>, <a href="#link-secret">link secret</a></div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->DID Exchange Protocol</a>, 
    <a href=#->DID Comm</a>, 
</div> 
<div style="width:250px; height:auto; float:left; display:inline; color:white">Compatible with</div> 
<div>
    <a href=#->Issue Credential Protocol</a>,
</div>
<div style="width:250px; height:auto; float:left; display:inline; color:white">Compatible with</div> 
<div>
    <a href=#->Present Proof Protocol</a>
</div>  
<br></br>

Decentralized identifiers that allow for the authentication of decentralized digital identities of a [DID subject](https://w3c.github.io/did-core/#did-subject). A DID is a URI that associates the DID subject with a DID document, which describes the DID subject and how they can authenticate themselves using cryptographic keys. DID documents are generated using a specific [DID method](https://w3c.github.io/did-spec-registries/#did-methods). It depends on the DID method whether the DID is a self-certifying identifier.

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
    <a href="#did">DID</a>,
    <a href="#link-secret">link secret</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div>
<br></br>

X.509 certificates are very widely used to define the binding between a party's (partial) identity and a public key. This certificate can be signed by a certificate authority, or it can be self-signed. It forms the basis for protocols like TLS in HTTPS. Because you can put attributes in the certificate, X.509 certificates can also be used as credential format.

##### Link Secret

Not a standard, but a cryptographic technique.
Based on [Pedersen commitments](https://www.cs.cornell.edu/courses/cs754/2001fa/129.PDF), see [link secrets](https://www.evernym.com/blog/how-does-a-verifier-know-the-credential-is-yours/).

#### Decentralized Public Key Infrastructure
As the name suggests, this is the decentralized version of the classic public key infrastructure. This ensures that no single party can compromise the integrity and security of the system as a whole. In decentralized PKI, there is no need to have a trusted third party.

##### KERI

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
    <a href=#did>DID</a>
</div> 
<br></br>


KERI is a novel technology for Decentralized Key Management Infrastructure (DKMI). It has been brought under in an informational standard.
Primary key management operation is key rotation, that can be performed using key event receipt logs (KERL)

The trust is rooted in self-certifying identifiers. 


#### Registry
A registry is used to store information that could be checked by anyone. To provide more protection against malicious modifications and a single-point of failure, this registry should be implemented in a decentralized fashion. Examples of this are decentralized file systems or Decentralized Ledger Technologies (DLTs), such as a blockchain.

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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

##### DID Exchange Protocol
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

##### Open ID

##### Open ID Connect
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>
https://openid.net/specs/openid-connect-core-1_0.html


##### Self-Issued OpenID Provider
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

___
### Layer 3: Credential Exchange Protocols 
Now that a connection tunnel has been set up, credentials can be exchanged. This layer is about the trust triangle (or diamond).

#### Issuer Protocol


##### Issue Credential Protocol
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

##### Credential Request (?)

##### OID4CI
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

#### Verifier Protocol

##### Present Proof Protocol
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

##### Presentation Request

##### OID4VP
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

#### Presentation Exchange

#### Signature Scheme

#### Credential Profile

Link to RWOT Credential Comparison Matrix + Paper

___
### Layer 4: Application Ecosystems
TBD

#### Delegation and Mandate

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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

#### CHAPI
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
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
    <a href="#-">-</a>
</div>
<div style="width:250px; height:auto; float:left; display:inline">Compatible with:</div> 
<div>
    <a href=#->-</a>
</div> 
<br></br>

#### Accessibility
