## Sharing Blocks in Bitcoin
A distributed system like Bitcoin has a bunch of nodes scattered all over the world with no central leader. When a new block is created by a given node, it needs to be able to propagate this info to all other nodes.

But how can some random node trust that the block info that it receives wasn't just made up by some attacker?

This is essentially the **Two Generals Problem**, or in the more general case **Byzantine Generals Problem**.

## The Problem
Suppose an army splits into two in order to surround a city. Each army is controlled by a general. The generals must decide on what day they will attack.

If they attack on the same day they will take the city. If they attack on different days they will be defeated.

Since they are spread out they must communicate via messenger. Unfortunately the messenger cannot be trusted. He could be bribed by the city to alter his message.

So there is a consensus problem. How do the general arrive at consensus about when to attack when they must use an unreliable communication channel?

## The Solution
It has actually been proved that there is no solution that will guarantee perfect coordination. But there are solutions that offer a high probability of coordination in certain situations.

So general A writes a message 'attack Monday' and sends it to general B. The problem is that since this message is just a simple string, it can easily be changed to 'attack Tuesday' by an attacker.

But suppose that the generals agreed ahead of time that each message would include a nonce (a random number) and that they would only accept messages where the hash of the message and nonce started with X number of zeroes.

So to create a message you write your message, include a nonce, then hash it to see if the hash starts with X zeroes. If it doesn't, which it probably won't, increment your nonce and hash it again. Repeat until the hash starts with X zeroes.

When a general receives a message the first thing they do is hash it to verify the hash starts with X zeroes. If it doesn't they just ignore it.

So if an attacker wants to alter your message, they will also need to find a new nonce such that the message plus nonce hashes to something starting with X zeroes.

This is certainly not impossible to do, but now the attacker needs to put in a huge amount of work if they want to falsify the message.

If the armies have a great deal more computing power than the attacker then they can agree on a high number of zeroes that the message must hash to. Then it will be infeasible for an attacker with much less computing power to alter a message and find a valid nonce for it.

## Bitcoin
So in Bitcoin the Bitcoin nodes are the generals/armies and the untrusted messenger is the Internet.

To simplify things a bit, an attacker needs to have more computing power than the rest of the network combined in order to reliably falsify blocks.

For more details see the Bitcoin page [in progress].

**Source**

Most of the info on this page was based on the very good video linked below. I've attempted to summarize as much as possible but check it out for more detail.

[![Byzantine Generals](http://img.youtube.com/vi/kE51N84hBxU/0.jpg)](https://youtu.be/kE51N84hBxU)
