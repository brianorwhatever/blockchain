Hash functions are the fundamental tools used to create blockchains and are critical to other aspects of cryptocurrencies including mining (for some cryptos).

## Overview

Cryptographic hash functions are one-way functions that map data of arbitrary size to some fixed-size output. So whether your input is 1 bit or 1 billion bits the output will be the same size.

For example given the input: 
```
hello
```
SHA-256 will output
```
0x2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824
```
Given the entirety of Wikipedia as input, the output would be the same size. The output, in the case of SHA-256, is an apparently random string of 256 bits.

A given input will always map to the same output, and the output should appear completely random. The SHA-256 hash algorithm for example produces a 256-bit output. Therefore any given hash value is one of 2<sup>256</sup> possible outputs. There are something like 2<sup>260</sup> atoms in the universe so the chance of finding another input that produces that hash is basically zero.

### Properties of an Ideal Hash Function

* **Determinism**: the same message always produces the same output
* **Quickness**: it is quick to compute the hash for some input
* **Irreversibility**: given some hash you can't figure out what the input was except by randomly guessing it and hashing the guess to see if it matches the target hash
* **Avalanche effect**: even a small change to the input completely alters the output
* **Collision resistance**: it is infeasible to find two messages that hash to the same value

So given these properties, what good are they?

### Digital Fingerprinting

The simplest application is **digital fingerprinting**. Take some chunk of data and hash it. The hash value will be (for all practical purposes) unique to that document.

A website can then publish just the hash of a file and users can download the file, hash it themselves, and check that their hash matches the published hash. If their copy of the file has been altered in any way, even if just one bit is flipped, the hash value will not match. If the hash matches however, then the user can be sure their file is legit.

This sort of independent integrity check is much better than going through the file chunk by chunk and asking the server if each chunk is correct.

### Hash lists

This concept can be extended to **hash lists** to allow trustless peer to peer file sharing.

Take a file, break it up into many small pieces. Hash each piece. Publish this relatively small hash list somewhere trusted. Now a peer in the network can accept a file piece from anyone, hash it; if the hash is found in the list then keep the piece, else discard.

An attacker cannot create a malicious file piece that matches a hash in the list. This technique is used by Bittorrent.

Even better we could hash the hash list itself to get a master hash or 'top hash'. We can then just publish the top hash and allow the peers to share hash lists. When a peer sends you the hash list, hash it, check if it matches the published top hash. If it matches then the hash list is legit and you can use it to start accepting blocks.

Hash functions have many other applications (like hash tables!), but the most relevant to cryptocurrencies is the blockchain.
