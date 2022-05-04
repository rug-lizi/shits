# DeFi Week 2 Blockchain

| Course Information | Info                                                        |
| ------------------ | ----------------------------------------------------------- |
| Course             | Decentralized Finance (DeFi) Infrastructure                 |
| Institution        | Duke University                                             |
| Instructor         | [Cam Harvey](https://www.coursera.org/instructor/~46121307) |


- [DeFi Week 2 Blockchain](#defi-week-2-blockchain)
  - [Blockchain](#blockchain)
  - [Hashing](#hashing)
  - [How do proof of work blockchains work?](#how-do-proof-of-work-blockchains-work)
  - [Advantages and Disadvantages](#advantages-and-disadvantages)


## Blockchain

Blockchain is a fundamentallly software protocols that allows you operate under shared assuptions without trusting each other.

These data can be anything.

[Blockchain is technology](http://www.placeholder.com)

## Hashing

Hash is cryption.

e.g. SHA-256 (Secure Hashing Algorithm)<https://emn178.github.io/online-tools/sha256.html>

1. Hashing is a one-way function.

>_Bitcoin uses SHA-256_
>_Ethereum uses Keccak-256_

2. Hashing is unique.
3. Is Hashing another way to full security, just like the function of quantum information?
4. It's called "chechsum" when the transmittion of information is achieved.


## How do proof of work blockchains work?

What do miners do?

- Miners are computing powers that secures the blockchain by adding a special number to the verified transactions on the blockchain.
- The special numbers are called "nonce", abbreviation of "numbers only once", which a series of additional numbers that make the transaction hashing output begins with "0"s.

> ## Mining
> 
> - The computational lottery involves cryptographic hashing. 
> - Miners group transactions together, make sure they are valid, and add a small piece of metadata called a nonce. They run a hashing function (SHA256 in Bitcoin and Keccak-256 in Ethereum) and try to get a very small value of the hash by cycling through different nonces.
> - This task is computationally burdensome. However, when a miner wins it is very fast to verify that the transactions + nonce = winning hash. Whenverified, a new block is added.

Impact of mining

- Well, mining requires enourmous amount of computing power that renders corruption of a blockchain infeasible for a single person, or even for a nation state.
- On the other hand, the power uses so much fuel, lots of which are fossil-fuel based, that is going to impact the environment unprecedentedly.

Questions

- Why do miners have to pack transactions to a special hashing series? Simplicity

## Advantages and Disadvantages

What can blockchain do?

- Verifaction of ownership
- Instant transfer

Why are blockchains special?

- They're just special for now, as they are evolving and the energy consumption rockets, they won't be regareded as special.

Proof of work

- Ethereum currently relies on Proof of Work (PoW) consensus protocol.
- An attacker needs amass 51% of the network computational power. This is the boundary of PoW security.

[Mining](#Mining)

How difficult is it to find the winning cash?

1. Shuffle 13 decks of cards
2. Look for 13 cards of 2 of Clubs with one shuffle
3. Duke University, Harvey's group Antminer S17 does _53 Trillion_ hashes per second. That represent 0.002% of the hashing power of the network.

<img src="/DeFi/Images/Duke-Fuqua%20Lab%20Mining%20Machines.png " width=50%>

Strength and Weekness

- Strength is security
- Weekness is the energy consumption
- Ethereum will move from `Proof of Work` to `Proof of Stake`[^1][^2] mechanism. That will likely happen in 2022. That will solve the environmental problem for Ethereum. But Bitcoin is a different story, it's likely stuck in the PoW mode.






[^1]: https://www.technologyreview.com/2022/03/04/1046636/ethereum-blockchain-proof-of-stake/
[^2]: https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/#the-beacon-chain

