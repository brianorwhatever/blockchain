Hash functions are a fundamental tool for blockchains, and are used in many other areas of cryptocurrencies. They are also used all over the place in computer science, and are pretty amazing little pieces of digital machinery.

## Definition
Cryptographic hash functions are one-way functions that map data of arbitrary size to some fixed-size output. So whether your input is 1 bit or 1 billion bits the output will be the same size.

A hash function can be viewed as a black box, where given some input like the example below, the output is fixed-size, and random looking.

**Example**

Given the string:
```
hello
```
The SHA-256 hash algorithm will output:
```
0x2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824
```
Given the entirety of Wikipedia as input, the output would be the same size, but the characters would be different.

Note: Bitcoin uses SHA-256 in it's mining algorithm. Also, it's called SHA-256 because it outputs 256 bits.

### Properties of an Ideal Hash Function
* **Determinism**: the same message always produces the same output
* **Quickness**: it is quick to compute the hash for some input
* **Irreversibility**: given some hash you can't figure out what the input was except by randomly guessing it and hashing the guess to see if it matches the target hash (the universe would end before you succeeded)
* **Avalanche effect**: even a small change to the input completely alters the output
* **Collision resistance**: it is infeasible to find two messages that hash to the same value (sun explodes before you succeed)

So given these properties, what good are they?

## Applications
### Digital Fingerprinting

The simplest application is **digital fingerprinting**. Take some chunk of data and hash it. The hash value will be unique to that document.

**Example**

Suppose the Ubuntu website wants to let people download the Ubuntu image file.

They can offer the download on the site, but also publish the hash of it.

Users can then download the file, and hash it themselves using the same algorithm. If their hash matches the published one then every single bit in their file matches exactly the official file.

That way the user knows the file wasn't altered in transit, or some virus on their computer didn't inject anything after it downloaded. The user could also download the file from any site, even an untrusted one. If they hash it and it matches the published hash then their file is legit.

### Hash lists
This concept can be extended to **hash lists** to allow trustless peer to peer file sharing.

**Example**

1. Take a file, perhaps a movie, break it up into many small pieces.
2. Hash each piece.
3. Publish this relatively small list of hashes somewhere trusted. 
4. Now a peer in the network can accept a file piece from anyone, hash it; if the hash is found in the list then keep the piece, else discard.

An attacker cannot create a malicious file piece that matches a hash in the list. It's just too hard to find something that hashes to one of those hashes in the list, except the actual file piece. 

This is basically what Bittorrent does.

#### Improvement
Even better we could hash the *hash-list itself* to get a master-hash or 'top-hash'.

We can then just publish the top-hash and allow the peers to share hash-lists. When a peer sends you the hash-list, hash it, check if it matches the published top-hash. If it matches then the hash-list you were given is legit and you can use it to start accepting blocks.

### Blockchains
The most relevant application of hash functions to cryptocurrencies is of course the blockchain. Watch the video on the blockchain page for a visual explanation.
