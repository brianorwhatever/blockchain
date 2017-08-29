Public key cryptography, or asymmetric cryptography, is what Bitcoin and others use in order to verify transactions.This tech is essential for cryptos to work.

Public key crypto allows **authentication** and **encryption** between parties which have never met.

Most cryptocurrencies do not actually encrypt transactions or any other data on the blockchain so we only need to worry about authentication for now.

## Authentication
**Example**

Let's say you want to send a message to your friend over an untrusted network, and your friend needs to be able to tell for sure that the message came from you.

You and your friend have never met in person to exchange a shared secret, but your public key has been publicly shared.

**Send**:

1. Generate a key-pair (a public and private key)
2. Use your private key and the message to generate a signature
3. Send the message and the signature

**Receive**:

1. Your friend sees the message and signature
2. Your friend uses your public key and message (and crypto magic) to see if the signature is correct

If the message was altered at all they will know. If the signature was produced by someone without the private key they will know.

## Bitcoin
This is how Bitcoin and other cryptocurrencies verify transactions. You sign your transaction using your private key, others then check that the signature is valid given your transaction data and your public key (your account address).
