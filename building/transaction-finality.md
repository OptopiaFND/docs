# Transaction Finality

The status of transactions on Optopia varies based on their inclusion process in the blockchain. It's crucial to understand the different stages of transaction finality for accurate and informed interaction with the Optopia network.

## Pending

Transactions are categorized as "pending" immediately after being sent to the Sequencer. This initial state indicates that the transaction has not yet become part of the blockchain and cannot be guaranteed to be included.

To retrieve a list of all pending transactions, you can utilize the standard JSON-RPC method `eth_getBlockByNumber` and set the block number parameter to "pending."

## Sequencer Confirmed / Unsafe

Generally within 2-4 seconds

Once a transaction is included in a block by the sequencer but the block has not been published to Ethereum, the transaction is marked as "sequencer confirmed" or "unsafe." Despite being in a block, if the sequencer does not immediately publish the block, there's a possibility that the transaction could be excluded from the final blockchain. Applications should account for this possibility when providing information about transactions in this state.

To obtain the latest "sequencer confirmed" block, employ the standard JSON-RPC method `eth_getBlockByNumber` with the block number parameter set to "safe." Compare it with the block returned as the "latest." If the "safe" block lags behind the "latest" block, the earliest "sequencer confirmed" block is the "safe" block plus one.

## Published to Ethereum / Safe

Generally within 5-10 minutes, up to 24 hours

When a transaction is included in a block by the sequencer and the block has been published to Ethereum but has not yet been finally determined, the transaction is considered "safe." Once a block is published to Ethereum, it is highly likely to be included in the final blockchain. However, the possibility of reorganization still exists.

To retrieve the latest "safe" block, use the standard JSON-RPC method `eth_getBlockByNumber` with the block number parameter set to "safe."

Transactions usually transition to the "safe" state within a few minutes after "sequencer confirmation."

## Finally Determined

Generally within 15-20 minutes, up to 24 hours

When a transaction is included in a block by the sequencer, it has been published to Ethereum, and the block has been finally determined, the transaction is considered "finally determined."

You can retrieve the latest "finally determined" block by calling the standard JSON-RPC method `eth_getBlockByNumber` with "finalized" as the block number parameter.
