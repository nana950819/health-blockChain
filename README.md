# Blockchain
Blockchain using Golang.

### Keys

The Blockchain uses ECDSA (224 bits) keys. 
When a user first joins the blockchain a random key will be generated.

Keys are encoded using base58.

Given x, y as the components of the public key, the key is generated as following:

```
	base58(BigInt(append(x as bytes, y as bytes)))
```

### Proof of Stake
In order to sign a transaction and send it to the validator, proof of stake is required. 

### Protocol

The blockchain runs on port `9750` and uses TCP to handle connections among peers.

##### Message

