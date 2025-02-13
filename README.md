# Google Summer of Code 2025 Ideas 🎉

This page showcases project ideas that align seamlessly with our Roadmap and are an ideal fit for GSOC '25. We aim to offer valuable insights into the necessary skillset and prerequisites, along with expectations for learning throughout the project. In addition to providing a project name and a concise descriptive abstract, we've included an assessment of general difficulty (assuming you meet the requirements) and project size. You will find the project list below. The sections represent the project titles, and the subsections are structured as follows:

| Subsection                            | Meaning                 | Values                                |
|---------------------------------------|-------------------------|---------------------------------------|
| Your Mission                          | Brief Overview             | `Free-form text` including `expected outcomes`                   |
| Skills required                       | Things you already know | `List of skills and technologies`     |
| You'll know those things after summer | Things you will learn   |  `List of skills and technologies`    |
| Difficulty                            | Difficulty ranges from a significant workload but straightforward implementation (Easy) to a research-oriented task with an unpredictable outcome (Challenging) | `Easy, Intermediate or Hard` |
| Size                                  | The size of the project, measured by the estimated hours required for completion | `90 hours, 175 hours or 350 hours` |
| Possible Mentors                      | Your mentor will guide and support you through this project | `List of names` |

For example, some projects may involve research tasks resulting in a small but significant output, categorized as both `Hard` in Difficulty and `350 hours` in Size. On the other hand, there might be projects with a well-defined vision, but requires a lot of time for implementation and testing, falling also into `350 hours` Size category but with an `Easy` difficulty level. In essence, Difficulty reflects the time spent for thinking, while Size corresponds to the overall time estimate for project completion.

---

## 👉 Proof-of-provenance for Software Artifacts

### 🚣 Your Mission

_Software Supply Chain_ attacks are becoming increasingly common, and sophisticated, with attackers targeting software forges, code & artifacts repository, or even [taking over maintenance of well-known packages to inject backdoors](https://en.wikipedia.org/wiki/XZ_Utils_backdoor). This is particularly concerning for software powering global networks like Cardano which is used to manage valuable assets.

On the other hand Cardano itself, being an extremely resilient, highly available, and decentralised network, could be a solid foundation to increase the security and traceability of software supply-chains. Providing signed and verifiable _proofs-of-provenance_ on-chain, stable identities, and tools and processes to trace and verify any software artifact to their author(s), would allow both software providers and consumers to build a strong web of trust.

Your mission will consist in building such a system, comprising of an on-chain part, e.g. _smart contracts_, to enforce rules about software releases and signatures on-chain, and an off-chain part itself divided in two sub-parts: a web API and site to provide a central point for sharing informations about published artifacts, and SDKs in at least two major languages (e.g. Java, Go, Python, JS/TS) to ease publication and verification workflows in software development lifecycle.

Some details are available [here](https://github.com/pragma-org/pop).

### 🏄 Skills required

DevOps, Web API and apps development, software forges

Note:

* We do not prescribe the language or tech stack to be used, this will be informed by the need to interact with Cardano network.
* No prior knowledge of Cardano is required as the focus of the work is on the developers' facing part

### 🐋 You'll know those things after summer

Software supply-chain attacks and mitigation, software development lifecycle, forges ecosystem and supply-chain security

### 🏋️ Difficulty

Medium

### 👕 Size

350 hours

### 🎓 Possible Mentors

[Arnaud Bailly](https://github.com/abailly)

---

## 👉 Decentralized Identity Wallet Integration with Single Sign-On (SSO)

### 🚣 Your Mission

The Cardano Foundation is actively developing an [open-source Identity Wallet](https://github.com/cardano-foundation/cf-identity-wallet) based on the principles of Self-Sovereign Identity (SSI) and the [Key Event Receipt Infrastructure (KERI)]((https://keri.one/)).

<p align="center">
  <kbd> 
      <img src="https://github.com/cardano-foundation/cf-identity-wallet/blob/main/docs/images/readme/User-Flow-Preview.png" alt="User Flow Preview" width="720"/>
  </kbd>
</p>

While the wallet already supports advanced features like secure enclaves, multi-sig identifiers, and credential exchange, there is an opportunity to bridge the gap between decentralized identity and the familiar Single Sign-On (SSO) flows used in Web2 applications (e.g., Google or social account logins).

*Your mission* is to create a system that integrates the Identity Wallet with standard SSO flows. The project will involve building a website where users can:

- Log in using Google or other social accounts.
- Connect their decentralized identity wallet (via QR code).
- Receive a verifiable credential in their wallet that proves they completed the SSO flow.
- This credential can then be used to log in to other applications, providing both authentication and additional identity information in a decentralized and privacy-preserving manner.

The project will demonstrate how decentralized identity can coexist with Web2 authentication systems, paving the way for broader adoption of SSI principles.

#### 📦 Expected Outcomes

A React-based single page application that supports:

- SSO login with Google or other social accounts.
- QR code-based connection to the Identity Wallet.
- Issuance of verifiable credentials to the wallet.
- A mechanism for applications to verify the credential and retrieve user information (with user consent).
- Documentation and a library abstraction to enable developers to integrate this system into their own applications.

### 🏄 Skills required

- ReactJS
- OAuth2 / OpenID Connect (SSO protocols)
- Decentralized identity standards (e.g., KERI, Verifiable Credentials)

### 🐋 You'll know those things after summer

- How to integrate decentralized identity systems with Web2 authentication flows.
- The principles of Self-Sovereign Identity (SSI) and Verifiable Credentials.
- Best practices for secure and privacy-preserving identity management.

### 🏋️ Difficulty

Medium

### 👕 Size

350 hours

### 🎓 Possible Mentors
[Thomas Mayfield](https://github.com/ThomasADA), [Jaime Caso](https://github.com/jimcase)

---

## 👉 Connected Goods

### 🚣 Your Mission

Counterfeit goods are a significant problem in the global economy. The Cardano blockchain can be used to track the provenance of goods, ensuring their authenticity and promoting transparency. The Cardano Foundation has collaborated with Georgia's National Wine Agency, the Bolnisi Winemakers Association, and Scantrust to develop the Georgian Wine Traceability Program. Furthermore, Cardano Foundation created a proof-of-concept hoodie with an integrated NFC chip that includes an encryption mechanism to ensure the authenticity of the product, which is linked to an asset on the Cardano blockchain. While this project is (open source)[https://github.com/cardano-foundation/cardano-store-poc-hoodies], it is currently not user-friendly for integration with other products and has a lot of manual steps.

Your mission is to create a user-friendly tool that can be used to develop NFC-enabled products that can be tracked on the Cardano blockchain.

#### 📦 Expected Outcomes

We would like you to implement an open-source tool that can flash NTAG DNA chips, automating and customizing the process of creating NFC-enabled products for use with blockchain technology. The [manual steps are described in the README](https://github.com/cardano-foundation/cardano-store-poc-hoodies?tab=readme-ov-file#instructions) of the hoodie PoC project. The tool should be platform-independent and ideally compatible with mobile devices, eliminating the need for external NFC writers and speeding up the creation process. Flutter, Ionic, or Tauri are preferred frameworks for the implementation.

<img src="https://store.cardano.org/cdn/shop/files/Diagram.png?v=1701202428&width=1000" height="360">

**Source: https://store.cardano.org/pages/authenticated-products**

### 🏄 Skills required

Python, Rust or Javascript or Dart, NFC & Cryptography (beginner level)

### 🐋 You'll know those things after summer

Cryptography, Cardano Native Assets, NFC

### 🏋️ Difficulty

Intermediate

### 👕 Size

175 hours

### 🎓 Possible Mentors

[Fabian Bormann](https://github.com/fabianbormann), [Sebastian Bode](https://github.com/cleanerm5)

---

## 👉 Ultimate Decentralized WebRTC Connector

### 🚣 Your Mission

[CIP-0045](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0045) introduces a method for setting up peer-to-peer communication between two browser windows on different devices, eliminating the need for a central signaling server to exchange their IP addresses. This technique allows for the injection of an API and making calls between the peers. To resolve their deep IPs behind different NATs, this approach uses a list of public WebTorrent trackers for peer discovery. However, in many scenarios, this method is not ideal. While https://peerjs.com/ requires a central component to establish the connection, it is more reliable and would significantly improve the user experience. This technique is currently used by mobile wallets like [Eternl](https://eternl.io/), but it would be a generic solution for any kind of API injection and peer-to-peer communication.

#### 📦 Expected Outcomes

The mission is to implement a multi-stage connection mechanism and enhance the CIP-0045 standard by adding preferred methods for the connection process. A QR code or link should include a custom PeerJS server address. If this server is unreachable or has not been provided, the community PeerJS server should be preferred as a fallback. If this also becomes unreachable, the current torrent-based approach should act as a final fallback. You can explore a demo setup using the current torrent-based approach in the open-source repository [available here](https://github.com/fabianbormann/cip-0045-demo-implementation).

### 🏄 Skills required

Typescript, PeerJS, WebRTC, WebTorrent (beginner level)

### 🐋 You'll know those things after summer

WebTorrent, WebRTC, Cardano Peer Connect

### 🏋️ Difficulty

Intermediate

### 👕 Size

175 hours

### 🎓 Possible Mentors

[Fabian Bormann](https://github.com/fabianbormann), [Jaime Caso](https://github.com/jimcase)

---

## 👉 Create a Graph-Native Query Layer

### 🚣 Your Mission

Cardano distributed ledger technology is based on the [eUTxO (Extended Unspent Transaction Output) model][eutxo-model], which in practice, generates an heterogeneous (decentralized) data lake of [un]structured data that is inherently more similar to a graph than to just a transactional ledger of balances, and doing (semantic) searches for relationships between different entities across the huge amounts of data the blockchain users produce, should be much cheaper in terms of computational resources and therefore, usually quicker, [using a graph-native database than a non-native (such as relational ones)][neo4j-native-vs-non-native]; also while crafting the queries to analyse data.

While there are currently multiple alternatives to feed Cardano events into relational databases such as `postgres`, message queues such `kafka` or virtually any data store using webhooks, and although some PoCs (using [oura][oura-dgraph-poc] and [yaci][yaci-fluree-poc]) exist to store Cardano events into [dGraph][dgraph] or [Fluree][fluree] graph-native solutions, there is no ready-to-consume API nor queries that makes use of a graph-native database as storage engine.

#### 📦 Expected Outcomes

The proposed mission would be to come up with an integrated solution that makes possible to query meaningful data for consumers like for example wallets or financial tools. *E.g.*:

* Balances (per address, per stake account, per contract...)
* Metadata events ([N]FT mints, messages, CIP events...)
* dApp interations (smart contracts executions, dApp events...)
* Financial analysis (token distributions, transactions volume...)

Graphs is where [web3][web3], maybe, meets [web3.0][web30]; as both are about linked data.

[eutxo-model]: https://en.wikipedia.org/wiki/Unspent_transaction_output#The_Extended_UTXO_(EUTXO)_Model
[oura-dgraph-poc]: https://github.com/txpipe/oura/tree/main/testdrive/cardano2dgraph
[yaci-fluree-poc]: https://github.com/cardano-foundation/cf-ledger-sync/blob/chore/test-streaming-events-to-fluree/streamer-app/README.fluree.md
[fluree]: https://flur.ee/
[dgraph]: https://dgraph.io/
[neo4j]: https://neo4j.com/developer/graph-database/#neo4j-overview
[neo4j-native-vs-non-native]: https://neo4j.com/blog/native-vs-non-native-graph-technology/
[web3]: https://en.wikipedia.org/wiki/Web3
[web30]: https://en.wikipedia.org/wiki/Web_3.0

### 🏄 Skills required

- Proficiency in at least one programming language and scripting language (bash)
- Experience with RESTful API development
- General understanding of a graph database (such as [neo4j][neo4j])
- OCI-compliant containers management

### 🐋 You'll know those things after summer

Graph databases fundamentals, at least one graph query language (graphql, sparql, dql...), Cardano entities/events, ETL

### 🏋️ Difficulty

Hard

### 👕 Size

350 hours

### 🎓 Possible Mentors

[Roberto C. Morano](https://github.com/rcmorano)

---

## 👉 SSOI Integration Platform with Identity Wallet

### 🚣 Your Mission
Self-Sovereign Onchain Identity (SSOI) represents an evolution of digital identity management that combines the principles of self-sovereign identity with the immutability and transparency of blockchain technology. This project will contribute significantly to the Cardano ecosystem by creating a bridge between traditional identity management and blockchain-based identity solutions, while also providing the necessary infrastructure for efficient SSOI data access and management. The Cardano Foundation's Identity Wallet already provides robust support for decentralized identities, and there's an opportunity to create a seamless bridge between SSOI systems and this existing infrastructure.

Your mission is to develop a comprehensive integration platform that consists of three main components:

1. An integration service that connects SSOI with the Cardano Foundation Identity Wallet, enabling seamless identity verification and credential management
2. A UTxO-based RPC service for SSOI that leverages Cardano's extended UTxO model to handle identity-related transactions
3. A high-performance indexer written in Go that monitors the Cardano blockchain for SSOI-related events and provides efficient query capabilities

#### 📦 Expected Outcomes

- A service that enables bi-directional communication between SSOI systems and the Identity Wallet
- An RPC implementation that handles SSOI operations using Cardano's UTxO model
- A Go-based indexing system that:
  - Monitors and indexes SSOI-related transactions on the Cardano blockchain
  - Provides a query API for accessing SSOI data
  - Implements efficient caching and data retrieval mechanisms
- Comprehensive documentation for all components
- Integration tests and examples showing the complete workflow

### 🏄 Skills required

- Go programming language
- Experience with blockchain indexing systems
- Understanding of UTxO-based blockchain models
- RESTful API development
- Knowledge of identity management systems and protocols
- Experience with concurrent programming

### 🐋 You'll know those things after summer

- Deep understanding of Self-Sovereign Identity principles and implementation
- Cardano's extended UTxO model and its applications
- Blockchain indexing strategies and optimization techniques
- Integration patterns for decentralized identity systems
- High-performance data processing with Go
- Best practices for building scalable blockchain services

### 🏋️ Difficulty

Hard

### 👕 Size

350 hours

### 🎓 Possible Mentors

[Nelson Kshetrimayum](https://github.com/nelson-ksh), [James Dunseith](https://github.com/workshop-maybe)

