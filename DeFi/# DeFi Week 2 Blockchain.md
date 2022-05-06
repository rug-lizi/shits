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

<img src="/DeFi/Duke-Fuqua%20Lab%20Mining%20Machines.png " width=50%>

Strength and Weekness

- Strength is security
- Weekness is the energy consumption
- Ethereum will move from `Proof of Work` to `Proof of Stake`[^1][^2] mechanism. That will likely happen in 2022. That will solve the environmental problem for Ethereum. But Bitcoin is a different story, it's likely stuck in the PoW mode.

[^1]: https://www.technologyreview.com/2022/03/04/1046636/ethereum-blockchain-proof-of-stake/
[^2]: https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/#the-beacon-chain

## Cryptocurrency

What is cryptocurrency?

- Cryptocurrency is a digital token that is cryptographically secured and transferred.
- `Asymmetric key cryptography` is a crucial component. Owners of cryptocurrency have a private key which is essentially a long random number.
- A public key is mathematically derived from the private key. This is a one way operation (you cannot – using today’s technology) derive the private key from the public key)
- Public addresses are derived from the public key which are derevied from the private key.

How crpytocurrency is transferred?

- It's transferred when the sender uses a digital signature algorithm to sign the token over to someone else’s address. Then the receiver's key will link to more cryptocurrency, thus the transfer.

What if you lose your private key?

- Somebody else owns the right to spend your money?
- If you show your private key to the public, you expose the resevoir to stealth.
- Here is an reported example. [Lost Passwords Lock Millionaires Out of Their Bitcoin Fortune](https://www.nytimes.com/2021/01/12/technology/bitcoin-passwords-wallets-fortunes.html)

## Smart Contracts/Gas/Oracles

Smart Contract

- ETH is sometimes called a small contract machine
- A `smart contract` is code that can creat and transform arbitrary data or tokens on top of the blockchain of which it is a part
- These contracts are run on every node of ETH
- Supply chain are another good example. Smart contract scheme is a much more general idea than cryptocurrency

Gas

- Users of smart contracts need to pay a fee, called `gas`
- The gas price is as a fee for using a cloud computing platform
- `Halting Problem`: Infinite loop on the system

E.g. Car

- If a car is on autopilot and an err occured and the car cannot stop.
- Only thing is gonna halt the car is gas.
- This a `Turing Complete` mechanism.

Gas/Gas Price/Gas Limit

- A transfer ETH from one address to another requires 21,000 gas
- Each unit of gas has a gas price, which is denoted in `gwei`(giga-wei). 1 gwei = 1 billionth of an ETH. Gas prices increase as users outbid one another during times of higher network congestion
  - If your gas price is much lower than the average gas price, your transaction will likely not be accepted
- The `gas limit` is the maximum amount of gas a user is willing to use for a transaction. A transaction can include multiple operations

Problems of Gas/Gas Price/Gas Limit

- Assume the average gas price is 150 gwei and we call a function in a smart contract that
  - transfers ETH
  - checks the balance of an account
  - load 2 bytes of memory from storage
  - The total amount of gas required= 21000+400+200=21600, that translate to 0.00324 ETH
- _What if the gas required doesn't reach the gas limit?_ Then we will be refunded the difference
- _What if the gas required exceeds the gas limit?_ Then the miners will be unable to excute the entire transaction. However, we will not be refunded any gas money since we still must pay for the computation
- Such a mechanism sets up problem
  - Gas prices vary from 50 gwei to up to 700 gwei in times of high net work congestion
  - 700 gwei/gas = $ 27.3/transaction, thus totally refutes the premise that ETH provide free transaction
- ETH has a `first price auction` mechanism, allowing miners to select transactions with the highest gas fees.

Ethereum Improvement Proposal (EIP)

- EIP 1559
  - change the gas fee to a base fee
  - increase the base fee
  - the base fee is adjusted according to the congestion
  - the base fee is burned after the transaction, so it doesn't envolve anyone's interest
  - Users can add tips to a miner

> Base Fee
>
> - The base fee is adjusted on the amount of gas included in a single block. If the amount of gas in a block is over 12.5 million, then the base fee will increase and vice versa
> - To accommodate the base fee, the current gas limit in a block will be increased to a hard cap of 25 million. The average target is 12.5 million gas
> - Burning the base fee puts downward pressure on the supply of ETH. If the ETH Issue: Burn ratio is below 1, then the supply of ETH is decreasing
> - Miners/Validators will earn money from proposing blocks and transaction tips. Their expected returns are lower and a few ETH mining pools oppose the update
> **How ETH include so many man-made quantities is ugly**

Ethereum Request for Comment (ERC)

- ERC-20 [^3]
- ERC-721 [^4]

[^3]: https://www.investopedia.com/news/what-erc20-and-what-does-it-mean-ethereum
[^4]: https://www.youtube.com/watch?v=_rxHurlszUE

Oracles

- A blockchain is a closed space. An oracle is to include outside information into said chain
- Say, you want ETH to be linked to the NASDAQ index in a certain way

Oracle Problem

- How can we create an oracle that can authoritatively speak about off-chain information in a trust-minimized way?
- One Ethereum-based platform known as [Chainlink](https://chain.link/) is designed to solve the oracle problem by using an aggregation of data sources. The Chainlink whitepaper includes a reputation-based system that is decentralized

## Stablecoin and dApps

Big Problem

- Bitcoin and ETH are extremely volatle

Stablecoin

- is backed by an stable currency
- collateral: gold, silver, public stocks or government bonds
- Fiat collateralized( to be side by side with sth, good word) stablecoins

Fiat[^5] collateralized stablecoins

- backed by an off-chain reserve of target asset
- Tether:USDT, larger, complicated history
- USDC: second largest, backed by Coinbase and Circle[^6]
- These stablecoins has been banned by NY state for false statements about their financial position and losees

[^5]: Fiat money (from Latin: fiat, "let it be done") is a type of currency that is not backed by any commodity such as gold or silver, and typically declared by a decree from the government to be legal tender. https://en.wikipedia.org/wiki/Fiat_money
[^6]: Both USDT and USDC are centralized

Crypto collateralized stablecoins

- MakeDAO DAI: most poplular, smaller market cap than USDC and Tether
- sUSD: Backed by Synthetix network token, SNX

Non-collateralized stablecoins

> These are not backed by any underlying asset, and use algorithmic expansion and contraction of supply to shift the price to the peg. 
> They often employ a seigniorage model where the token holders in the platform receive the increase in supply when demand increases. 
> When demand decreases and the price slips below the peg, these platforms would issue bonds of some form which entitle the holder to future expansionary supply before the token holders receive their share

Open problem

- decentralized stablecoin which both scales efficiently and is resistant to collapse in contractions
- regulatory issues
- Fei Protocol[^7], new initiative that suffice both

[^7]: https://learn.bybit.com/crypto/fei-protocol/

dApps

- your cryptowallets

Decentralized Autonomous Organization (DAO)

- a new form of organiztion that is essentially a computer program
- a DAO sets rules of operation encoded in smart contracts that determine who can execute what behavior or upgrade
- think of DAO as a company that inherintally without a board of memebers or a CEO
