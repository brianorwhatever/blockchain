Public key cryptography, or asymmetric cryptography, is what Bitcoin and others use in order to verify a transaction came from the account holder.

Public key crypto allows **authentication** and **encryption** between parties which have never met, but most cryptocurrencies do not actually encrypt transaction data or any other data on their blockchains so we only need to worry about the authentication part for now.

## Authentication

<p>Produce your key-pair &#x2012; a public key which you can share with anyone, even publish to your website, and a private key which is kept private. Now you can produce a chunk of data, maybe a will, financial transaction, or any message, and use your private key to 'sign' this chunk of data. Recipients who receive the message can be certain that it came from you. More accurately they can be sure that someone with the private key, which corresponds to the public key that you published, signed the document.</p>

So as long as your public key is published somewhere that people can trust, you can send out signed messages on an *untrusted* network and others can be sure that the message came from you, and that it wasn't altered in any way. If you cannot, or do not want to associate a public key to your identity, you can still send out signed messages and recipients can verify that the message came from someone who holds the private key corresponding to some public key.
