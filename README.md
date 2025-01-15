# Google Summer of Code 2025 Ideas 🎉

This page showcases project ideas that align seamlessly with our Roadmap and are an ideal fit for GSOC '24. We aim to offer valuable insights into the necessary skillset and prerequisites, along with expectations for learning throughout the project. In addition to providing a project name and a concise descriptive abstract, we've included an assessment of general difficulty (assuming you meet the requirements) and project size. You will find the project list below. The sections represent the project titles, and the subsections are structured as follows:

| Subsection                            | Meaning                 | Values                                |
|---------------------------------------|-------------------------|---------------------------------------|
| Your Mission                          | Brief Overview             | `Free-form text` including `expected outcomes`                   |
| Skills required                       | Things you already know | `List of skills and technologies`     |
| You'll know those things after summer | Things you will learn   |  `List of skills and technologies`    |
| Difficulty                            | Difficulty ranges from a significant workload but straightforward implementation (Easy) to a research-oriented task with an unpredictable outcome (Challenging) | `Easy, Intermediate or Hard` |
| Size                                  | The size of the project, measured by the estimated hours required for completion | `90 hours, 175 hours or 350 hours` |
| Possible Mentors                      | Your mentor will guide and support you through this project | `List of names` |

For example, some projects may involve research tasks resulting in a small but significant output, categorized as both `Hard` in Difficulty and `350 hours` in Size. On the other hand, there might be projects with a well-defined vision, but requires a lot of time for implementation and testing, falling also into `350 hours` Size category but with an `Easy` difficulty level. In essence, Difficulty reflects the time spent for thinking, while Size corresponds to the overall time estimate for project completion.

## 👉 Untyped Plutus Core Viewer, AKA Understandable Decompiled Smart Contracts

### 🚣 Your Mission

UPLC (Untyped Plutus Core) is executed on-chain and serves as the foundational layer for Cardano smart contracts. High-level languages like Aiken or Helios compile to UPLC. While it's possible to decode the binary (flat) encoded UPLC contract into its text representation, the resulting tree structure is not particularly readable. The objective of this project is to discover a more user-friendly representation of the decoded structure. We welcome rule-based or machine learning solutions that not only transform the binary form into text but also render it in a readable format, making it accessible for e.g. TypeScript developers to comprehend the actual functionality of a contract. 

#### 📦 Expected Outcomes

We would like you to implement the viewer within a standalone React (Vite.js) app and also export the viewer component itself as a reusable component to npm. This allows other applications within the Cardano ecosystem to utilize its features.

<img src="https://github.com/cardano-foundation/cf-gsoc-ideas-page-2024/assets/1525818/37084b72-2340-4a58-82e6-da34870fed37" height="360">

**Source: https://aiken-lang.org/uplc**

### 🏄 Skills required

Typescript, React.js, General understanding of Compliers and Decompliers

### 🐋 You'll know those things after summer

Cardano Smart Contracts, Plutus Core, Aiken

### 🏋️ Difficulty

Intermediate

### 👕 Size

175 hours

### 🎓 Possible Mentors

Fabian Bormann, Satya Ranjan

## 👉 Cardano Peer Connect (CIP-0045) Improvements

### 🚣 Your Mission

[CIP-0045](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0045) introduces a method for setting up a peer-to-peer communication between two browser windows on different devices, eliminating the need for a central signaling server to exchange their IP addresses. This technique allows for the injection of an API (CIP-0030) from one browser (a wallet) to another (a DApp), enabling seamless and lightweight mobile support. To resolve their deep IPs behind different NATs, this approach uses a list of public WebTorrent trackers for peer discovery. However, in many scenarios, when the user is on a mobile device and aims to connect a wallet to a DApp in a browser on the same device, or in another situation where the user is on the same local network and wants to link the wallet on a phone to a DApp on the PC, the use of a torrent tracker becomes unnecessary due to the absence of NAT involvement. Furthermore, there's currently a bit of a hassle in switching between a browser-based wallet and a website, for instance, to sign a message. 

#### 📦 Expected Outcomes

The mission of this project would be to investigate both topics: situation-dependent peer discovery and enhanced usability. You can explore a demo setup in the open-source repository [available here](https://github.com/fabianbormann/cip-0045-demo-implementation). At the end of this project you should have implemented the new (local) peer discover method and the enhanced usabulity features (intents, nofitfications, ...) into [this repository](https://github.com/fabianbormann/cardano-peer-connect).

### 🏄 Skills required

Typescript, React.js, Ionic, Node.js

### 🐋 You'll know those things after summer

WebTorrent, CIP-0030 (Cardano dApp-Wallet Web Bridge), Firebase Cloud Messaging SDK

### 🏋️ Difficulty

Hard

### 👕 Size

175 hours

### 🎓 Possible Mentors

Fabian Bormann, Jaime Caso

## 👉 Smart Contract Classificator

### 🚣 Your Mission

At the moment, figuring out the purpose of a smart contract on Cardano only based on hashes and binary data is quite challenging. However, there are always identifiable patterns. Have you ever wondered how many smart contracts are actually being utilized for financial purposes? Is Cardano positioning itself as the go-to blockchain for gaming? What about smart contracts in supply chain scenarios, voting mechanisms, or even for distributing art and music? The truth is, no one really knows... yet.

This mission involves developing a smart contract classifier using a combination of machine learning, statistics, and various conditions. From Convolutional Networks to Gradient Boosting Decision Trees, and even manual feature engineering – everything is on the table. The goal is to design an algorithm capable of taking a smart contract transaction and providing probabilities for different use-case labels.

Whether it's addresses, reference scripts, or reference datums, we are confident that you'll create a tool that can answer the questions mentioned above. To support you in this venture, we'll assign you a mentor with previous experience as a machine learning engineer. This mentor will provide you with ground truth data, guide you on how to find it, and offer deeper insights into the world of Cardano. Towards the end of this journey, our plan is to apply your algorithm to all the on-chain contracts to create a meaningful report.

### 🏄 Skills required

Python, Scala, Statstics, Machine Learning (basics), Smart Contracts under Cardano (beginner level)

### 🐋 You'll know those things after summer

Classification algorithms, Data Science, Cardano Smart Contracts, deep insights in how Cardano actually works

### 🏋️ Difficulty

Hard 

### 👕 Size

350 hours

### 🎓 Possible Mentors

Satya Ranjan, Thomas Kammerlocher, Giovanni Gargiulo

## 👉 Enhanced Cardano Asset API Service

### 🚣 Your Mission

Your challenge is to elevate the utility of the Cardano testnet by developing a versatile API service. This service will automate the minting and distribution of a diverse range of Cardano blockchain assets, including NFTs and native tokens, to specified payment addresses. This project is a significant step beyond the current capabilities of the [**Cardano faucet**](https://docs.cardano.org/cardano-testnet/tools/faucet/), which is limited to dispensing Ada. By integrating various asset types defined in the Cardano Improvement Proposals (CIPs), such as [CIP-25](https://cips.cardano.org/cip/CIP-0025) (Media Token Metadata Standard) and [CIP-54](https://cips.cardano.org/cip/CIP-0054) (Cardano Smart NFTs), you will be creating a tool that is indispensable for developers. This API will serve as a critical resource, providing them with a variety of test assets to enhance the development, testing, and optimization of wallets, blockchain explorers, and other applications/dApps. Your work will play a pivotal role in simulating real-world asset handling, crucial for the rigorous testing and preparation of applications before their deployment in production environments.

#### 📦 Expected Outcomes

The project's output will be a fully functional API service capable of handling multiple asset types, requiring significant coding and testing.

### 🏄 Skills Required

- Proficiency in Javascript(recommended) or Java, for minting assets.
- Experience with RESTful API development.
- Familiarity with blockchain technology, specifically Cardano's ecosystem. 
- Understanding of Cardano's native tokens and NFTs as per CIPs (like CIP-25, CIP-54, CIP-27, CIP-60, CIP-68).

### 🐋 You'll Know Those Things After Summer

In-depth knowledge of Cardano's blockchain and asset standards
Experience in developing and deploying scalable blockchain APIs
Expertise in integrating diverse blockchain assets into applications

### 🏋️ Difficulty

Intermediate – This project involves not only the technical aspects of API development and blockchain integration but also requires a deep understanding of the Cardano blockchain's native asset standards.

### 👕 Size

350 hours

### 🎓 Possible Mentors

Jaime Caso

### 🌍 Importance of Testnets in Blockchain Development

The importance of testnets in blockchain development cannot be overstated. Testnets provide a sandbox environment where developers can experiment and test their applications without risking real funds or impacting the main blockchain. They are crucial for:

- Ensuring the security and stability of new features before they are deployed on the mainnet.
- Allowing developers to test the integration of different asset types and ensure compatibility with various wallet and explorer applications.
- Facilitating the development and testing of smart contracts under real-world conditions without the associated risks.
  
This challenge, therefore, not only enhances the capabilities of the Cardano testnet environment but also significantly contributes to the broader development ecosystem, enabling developers to build more robust, diverse, and secure applications on the Cardano blockchain.

## 👉 DApp End-2-End Testing Framework

### 🚣 Your Mission

A decentralized App (dApp) mainly consists of a frontend application that has the feature to connect itself to a wallet, but at the same time, it interacts with the blockchain. Although many Cardano dApps can utilize frameworks like Playwright or Cypress to test their click flow or business logic using mock data, testing end-to-end functionality is currently not as straightforward. The use of a public testnet in a continuous integration (CI) pipeline necessitates the dApp to maintain a test wallet with sufficient tADA or native test tokens, ensuring consistent preconditions for each run. Testing edge cases would not be that easy, as they often involve a complex set of requirements that developers must create and maintain on the public testnet.

#### 📦 Expected Outcomes

With yaci-devkit, we have a local testnet that developers can easily set up on a local machine or in a CI pipeline. Given our close collaboration with wallet providers in the ecosystem, your primary objective for this project will be to create and implement an architecture that seamlessly integrates a local testnet (devnet) into wallets, providing a developer-friendly experience for wallet providers and developers. Ideally, this should involve a test container with a pre-configured wallet plugin on a headless Chromium browser, along with Yaci-devkit, which expects a configuration file for managing top-ups and "genesis" amounts in wallets. A library that automates the click-flow for signing, transaction submission, etc., would be a game-changer for Cardano developers worldwide looking to test transactions, minting operations, or even smart contracts within their dApp in their CI pipeline.

### 🏄 Skills Required

TypeScript, Docker, Bash, Cypress or Playwright, GitHub Actions, CICD, Cardano (beginner level)

### 🐋 You'll Know Those Things After Summer

Cardano fundamentals, such as eUTXO and dApp & Wallet communication, How to provide a test automation framework for an extensive ecosystem

### 🏋️ Difficulty

Hard

### 👕 Size

175 hours

### 🎓 Possible Mentors

Satya Ranjan, Thomas Kammerlocher, Giovanni Gargiulo, Fabian Bormann

## 👉 Create a graph-native query layer for Cardano

### 🚣 Your Mission

Cardano DLT is based on the [eUTxO (Extended Unspent Transaction Output) model][eutxo-model], which in practice, generates an heterogeneous (decentralized) data lake of [un]structured data that is inherently more similar to a graph than to just a transactional ledger of balances, and doing (semantic) searches for relationships between different entities across the huge amounts of data the blockchain users produce, should be much cheaper in terms of computational resources and therefore, usually quicker, [using a graph-native database than a non-native (such as relational ones)][neo4j-native-vs-non-native]; also while crafting the queries to analyse data.

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

Roberto C. Morano
