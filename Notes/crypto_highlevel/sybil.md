## Sybil Attacks in Bitcoin
The mining process of Bitcoin and other cryptocurrencies can be viewed as a lottery where one of the nodes in the network is randomly selected to put forth the next block in the blockchain.

But if you simply randomly select one of the nodes, what is to stop some attacker from spinning up thousands/millions of nodes (using virtual machines with different IPs or something) in order to have a much higher chance of winning the lottery?

This is a sybil attack in the context of cryptocurrencies.

If you were able to reliably win the lottery you could double-spend and do all kinds of other nefarious things. This is a really tough problem because in the digital world practically everything can be arbitrarily copied.

## Bitcoin Solution
The solution that Satoshi came up with for Bitcoin was basically to, rather than allocate one 'lottery ticket' per node, instead allocate one lottery ticket per unit of computation.

Since doing a computation uses electricity, hardware and time resources you can't just arbitrarily replicate these lottery tickets - they cost you in the real world.

This is implemented in the Proof of Work mining algorithm.
