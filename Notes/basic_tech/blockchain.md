## Conceptualisation

A blockchain is a distributed, secure database or ledger. A blockchain can store transaction data or any other data you want.

An interesting aspect of a blockchain is that it is *ordered*. With most data structures it isn't really a sensible question to ask which part of the data structure was created first. Blockchains actually must be constructed in a particular order. Therefore they have some aspect of time encoded into them.

## Basic idea

Take some chunk or 'block' of data, compute the hash for it, now take that hash value and put it in the next block. Repeat the process for each new block. Now anyone who looks at this sequence of blocks can be sure of their order of creation, as well as the contents of each block being unaltered in any way after the chain was created.

Assuming the hash of at least the newest block is published somewhere trusted, then if an attacker tries to send you a copy of the blockchain with even a single bit changed in *any* block, no matter how far back, the hashes of all blocks following the change will not match.

In addition to the previous block's hash, a block can contain any kind of data you want. In the case of Bitcoin the blocks contain transaction data. Attackers cannot go back to an old block and change a transaction, because doing so would cause all following block hashes to change. A blockchain could be made to store contracts, records of events, patents or anything else where having an unaltered history matters.

This data structure can serve as a sort of shared database. It would be nice however, to have some way of knowing your blockchain, your database, was correct without having to trust a hash value from *anyone*. And there should be some way of knowing you have the correct blockchain that everyone else is using without having to trust some central authority to keep track of this. Bitcoin very elegantly solves both of these problems.
