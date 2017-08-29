## Conceptualisation
Ultimately a blockchain is just a type of database. Like any database you can store whatever you want in it, but not all applications will benefit from the properties of a blockchain.

### Distributed
Blockchains are shared data structures suitable for distributed systems. If you just want to save your files on your computer, or store website assets on a CDN, then you are probably far better off with a regular database.

### Read
Blockchains are shared data structures. When a node joins the network they need to obtain the blockchain from their peers. They then go through the whole blockchain and verify it's validity.

The node may then scan the blockchain for data when needed, or it may have built up a 'state' of the network when it scanned through the blockchain. For example in Bitcoin the state can be thought of as how much Bitcoin each 'account' has. In order to figure this out each node must go through the whole chain.

### Write
To write to a blockchain you create a new block and append it to the end of the chain. Once blocks are part of the chain they cannot be edited. So blockchains are append only.

## Visual Explanation
The video below perfectly explains how blockchains work in a visual way.

[![Blockchain Demo](http://img.youtube.com/vi/_160oMzblY8/0.jpg)](https://youtu.be/_160oMzblY8)
