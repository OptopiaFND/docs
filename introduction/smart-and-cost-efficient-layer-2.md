# Smart and Cost-Efficient Layer 2

## Preface

In the rapidly evolving landscape of blockchain technology, scalability and efficiency are paramount for achieving widespread adoption, Optopia’s mission is to establish new AI standards and explore AI application scenarios.

Optopia innovatively adopt a Layer 2 solution, directly addressing the scalability challenges faced by Ethereum and other blockchain networks. We emphasize empowering AI applications and promoting the implementation and adoption of artificial intelligence. By harnessing the power of [4EVERLAND’s Rollups as a Service (RaaS)](https://docs.4everland.org/raas-beta/4ever-rollup-stack), Optopia offers a smart and cost-effective approach to scaling decentralized AI applications.

## How Optopia works

Optopia seamlessly integrates with the Ethereum ecosystem, providing full compatibility and interoperability with the Ethereum Virtual Machine (EVM). Built on the Op Stack—a standardized, shared, and open-source development framework—Optopia aims to enhance both user and developer experiences without disrupting the familiar cryptocurrency landscape.

* **Efficient Layer 2 Solution**: Leveraging the Op Stack, Optopia achieves efficiency, security, and scalability. By moving computationally intensive tasks off-chain, it significantly reduces gas fees and enhances transaction throughput.
* **EIP-4844 Integration**: Optopia adopts Ethereum’s EIP-4844, introducing a new transaction type that accepts ‘binary large object’ (Blob) data. This innovation further reduces fees and increases overall efficiency.
* **Arweave Blob Archiver**: Data permanence and accessibility are guaranteed through integration with Arweave, a decentralized storage solution.

## Technical Architecture

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
### OP Stack

OP Stack serves as a standardized, shared, and open-source development stack. It acts as a software component that defines specific layers within the Optopia ecosystem while also functioning as a module in the existing layers.

* [Design Principles](https://docs.optimism.io/stack/protocol/design-principles)
* [Components Overview](https://docs.optimism.io/stack/components)

### Ethereum DA

Ethereum DA is currently the most widely used data availability module within OP Stack. When utilizing the Ethereum DA module, source data can be extracted from any information accessible on the Ethereum blockchain. This includes Ethereum calldata, events, and 4844 data Blobs.

* [Specifications](https://specs.optimism.io/protocol/derivation.html#batch-submission-wire-format)

### Arweave backup

Arweave functions as a blockchain infrastructure designed to address the permanence and accessibility of data. Its “permanent file storage” technology, distinct from traditional blockchain data storage methods, ensures the permanent preservation of data.

* [The Arweave server and App Developer Toolkit](https://github.com/ArweaveTeam/arweave)
{% endhint %}
