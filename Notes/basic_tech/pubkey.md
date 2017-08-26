Public key cryptography, or asymmetric cryptography, is what Bitcoin and others use in order to verify transactions.This tech is essential for cryptos to work.

Public key crypto allows **authentication** and **encryption** between parties which have never met.

Most cryptocurrencies do not actually encrypt transactions or any other data on the blockchain so we only need to worry about authentication for now.

## Authentication

### Bitcoin Example
Let's say you want to create a Bitcoin 'account' and send some Bitcoin to someone. Here is a simplified explanation of what happens:

1. Use wallet software to generate a key-pair. A key-pair consists of a public and private key. The public key is your 'account number', or address, and can be shared. The private key is the key that unlocks your money.
2. Get some Bitcoin in that account.
3. Use your wallet softare to create a transaction. This transaction will say 'send X BTC to <your address>'. The transaction will include your address.
4. Sign the transaction. To sign it take the message and your private key and do crypto magic to produce a signature. The sig is unique to that transaction. The sig is a big number.
5. Now other nodes can see the message (send X BTC to whoever), see your address (your pub key) and see your signature for that transaction. They can then check for themselves that given that message and your pub key, someone with the private key **must** have created that signature. And that signature was made for this exact transaction. 

That is what public key crypto can do.

### Trust

So as long as your public key is published somewhere that people can trust, you can send out signed messages on an *untrusted* network and others can be sure that the message came from you, and that it wasn't altered in any way. If you cannot, or do not want to associate a public key to your identity, you can still send out signed messages and recipients can verify that the message came from someone who holds the private key corresponding to some public key.
