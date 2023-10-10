---
layout: post
type: socratic
title: "Socratic Seminar 14: Happy Birthday to the Republic of China"
meetup: https://www.meetup.com/taiwan-bitdevs/events/296527753/
---

## Announcements
Welcome again Bitdevs Taiwan

Our fourteenth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### BITVM Arbitrary computation -- without softfork

Announced by developer Robin Linus of ZeroSync, an association founded to help scale Bitcoin by using zero-knowledge proofs, BitVM is a design that enables arbitrary computation in Bitcoin script, and use that computation to enforce what happens to bitcoin on-chain.  This idea requires no softfork, it could enable proposals that had previously required soft forks to add new op-codes  

"logic gates" are expressed in transactions using tapscript using tapleafs to represent possible states. two parties exchange the state of the computation by sharing the proof/commitment to each gate. due to the immense amount of computation, this will happen off-chain

can there be more than two parties?

[white paper] ([https://bitvm.org/bitvm.pdf])

[annoucement] ([https://twitter.com/robin_linus/status/1711378768059584723])

[article] ([https://bitcoinmagazine.com/technical/the-big-deal-with-bitvm-arbitrary-computation-now-possible-on-bitcoin-without-a-fork])

### BIP-324 Encrypted P2P and AssumeUTXO merged to Bitcoin Core

BIP-324 will allow Bitcoin nodes to communicate with each other over encrypted connections, while AssumeUXTO option is set to allow instant UTXO set bootstrapping for Bitcoin nodes.

[link]([https://github.com/bitcoin/bitcoin/pull/28331])

### UTXOracle.py daily Bitcoin price using blockchain data

Introducing http://UTXOracle.py - Get the price of bitcoin without any exchange or third party. 

Everyone who runs this will get the same price independently.

Open source, 100% on-chain data, no external libraries, no cookies. Works offline. 

[link]([https://utxo.live/oracle])

### MARA (Marathon Digital Holdings) mines invalid Bitcoin Block 809478

While validating this block, Bitcoin Core reported:

ERROR: ConnectBlock: Consensus::CheckTxInputs: 66dfefcdc3eeec2745c11f511f6068d62f34c34c767ba0feed47f63f01ccc2d8,
bad-txns-inputs-missingorspent, CheckTxInputs: inputs missing/spent
This means, there was a problem validating the transaction 66dfefcd[..]1. Specificially, a previous output refferenced in an input wasn’t found in the UTXO-set during block verification. This is usually either caused by a transaction ordering problem (output is being spent before it’s created) or a corrupt UTXO set. Problems like this always raise the question where the problem originates from and who else might be affected. Is this a bug only on the mining pool side? Or is this a bug in some version of Bitcoin Core possibly affecting the whole network?

[blog post]([https://b10c.me/observations/07-invalid-block-809478/])

### Phoenix Wallet channel splicing update live on iOS and Android

Channel splicing allows for flexible channel capacities without increasing on-chain footprint
Note that existing swap addresses should no longer be used!

[github link]([https://nitter.net/PhoenixWallet/status/1708055031398711478)

### LND v0.17.0 released -- P2TR Channels

LND v0.17 features Simple Taproot Channels that enable a lower cost and more private LN, faster Neutrino syncs for mobile development, more efficient Watchtowers, and more.

[blog post]([https://lightning.engineering/posts/2023-10-03-lnd-0.17-launch/])

### Fedimint v0.1.0 release
Fedimint is a federated Chaumian e-cash mint backed by bitcoin with deposits and withdrawals that can occur on-chain or via Lightning.

[link]([https://fedimint.org/])

### Bitmain releases Antminer S21 series 

(Bitmain has launched its new series of Antminer bitcoin mining devices. 

They’re a huge improvement in hashrate and efficiency over existing devices. 

S21 - 200 TH/s hashrate and 17.5 J/T efficiency. 

S21 Hydro - 335 TH/s hashrate and 16 J/T efficiency.

[article]([https://hashrateindex.com/blog/what-is-the-antminer-s21-everything-to-know-about-bitmains-latest-asic-miner/])

### Diamond Hands announces partnership with Boltz to provide lightning liquidity swap services for Bitcoin and Liquid

Diamond Hands released a new and improved DH Swap service for better Lightning liquidity management in partnership with Boltz.

[article]([https://www.nobsbitcoin.com/diamond-hands-partners-with-boltz-to-improve-dh-swap-service/])

### UK High Court orders that anonymous Bitcoin.org operator Cobra must identify themselves

The U.K. High Court has rejected an appeal that aimed to protect the anonymity of the pseudonymous operator behind Bitcoin.org, known as Cøbra, stating that allowing them to participate in post-judgment costs proceedings would be an 'infringement on open justice.'
This follows ongoing legal harassment of Bitcoin contributors

[link]([https://www.nobsbitcoin.com/bitcoin-org-operator-loses-appeal-to-craig-wright/])

### Drivechains (BIP300) - a Miners perspective

The bitcoin mining business is operationally complex and labor intensive. But that is a natural consequence of the narrow and well defined role they have been playing since Bitcoin’s inception. Asking miners to adjudicate disputes on a sidechain, potentially many of them at once, doesn’t just add additional business complexity, it changes the fundamentally neutral role miners play in validating transactions. Disputes are inevitable and the complexity around power, incentives, and rules becomes uncertain from a miners point of view. As of now, the power of miners is checked, and extends only to ensuring transactions satisfy consensus rules, which all parties know and agree to. While drivechains can drive additional revenue to Bitcoin miners, this addition of judgment to the protocol is deeply risky, and is trading short-term revenue for potential long-term consequences which remain largely unknown. This is simply not a wise trade off."

[article] ([https://bitcoinmagazine.com/business/drivechains-from-a-bitcoin-miners-perspective?ref=nobsbitcoin.com])


###US Gov argues that disclosing ChainAnalysis heuristics would jepordize investigations

US govt argues that disclosure of Chainalysis heuristics information in the case US vs Sterlingov would “jeopardize numerous law enforcement investigations and impact the effectiveness of law enforcement tracing tools” by enabling the development of “criminal countermeasures to blockchain analysis.”

[article] ([https://bitcoinmagazine.com/legal/us-government-frames-bitcoin-privacy-as-criminal?ref=nobsbitcoin.com])


### Chainanalysis criticisms

Roman Sterlingov is currently being prosecuted for operating bitcoin centralized coinmixer Bitcoin Fog on evidence collected by US investigators using data from chain/data analysis company ChainAnalysis

Elizabeth Bisbee, head of investigations at Chainalysis Government Solutions, testified she was “unaware” of scientific evidence for the accuracy of Chainalysis’ Reactor software used by law enforcement, an unreleased transcript of a June 23 hearing shows.

The fact that Chainalysis’ blockchain demystification tools have become so widespread is a serious threat to the crypto ecosystem. Although industry insiders have raged against Chainalysis since it was founded, often accusing it of violating people’s financial privacy, there may be a better argument to make against the company and analysis firms like it: it’s within the realm of possibility that these surveillance machines don’t work as well as advertised.


[article]([https://bitcoinmagazine.com/technical/chainalysis-investigations-lead-is-unaware-of-scientific-evidence])

[podcast about Roman]([https://www.podpage.com/citadeldispatch/cd100-the-disturbing-chainalysis-led-prosecution-of-roman-sterlingov-with-mike-hassard-and-tor-ekeland/])

### Bitcoin Spot ETF Applications Refiled To Bring Coinbase Surveillance to Next Level

Asset management giant BlackRock took the first steps Thursday to launch a spot bitcoin exchange-traded fund, which has long been a point of contention between crypto advocates and federal regulators.

The firm filed an application with the U.S. Securities and Exchange Commission to launch the iShares Bitcoin Trust. If approved, the ETF would allow easy access for investors to get exposure to crypto in a product from one of Wall Street’s largest companies.

As exciting as it is to have BlackRock enter the space so thaat Grayscale is no longer the only game in town, it is important to remember that Larry Fink once called Bitcoin an "index of money laundering", and this product does not have any form of gurantee for actual Bitcoin redemption/settlement

[updated news article](https://www.nobsbitcoin.com/spot-etf-coinbase-surveillance-agreement/)

[news article](https://www.cnbc.com/2023/06/15/blackrock-files-for-spot-bitcoin-etf-with-coinbase-as-a-crypto-custodian.html)

[criticism: Allan Farrington - Just trust me, bro](https://allenfarrington.medium.com/trust-me-bro-fb5a25964634)

[Fidelity also joins in the fun?](https://twitter.com/BitcoinMagazine/status/1670762619677085697)

### Liquid Federation open sources functionary code

The Liquid Network is a federated network with certain members of the network being able to "peg-out" L-BTC to on-chain Bitcoin.  To access the Liquid Network anyoneone can run Elements which is the Liquid Node software to "peg-in" Bitcoin to the Liquid Network. Until now there is only one Liquid Network, by open-sourcing the functionary code used by the federation members perhaps there will be more

[announcement]([https://blog.liquid.net/expanding-transparency-the-liquid-networks-functionary-code-is-now-open-source/?ref=nobsbitcoin.com])

### Serverless Payjoin

Payjoin is a technique for both sender and receiver to contribute inputs and outputs to the same transaction. This preserves the privacy of the sender and gives the receiver the opportunity to consolidate UTXOs.

Current implementations of payjoin require the receiver to run a centralized server. How do we make it possible to perform payjoin when both parties cannot be online at the same time?

[blog: Serverless Payjoin Gets its Wings](https://payjoin.substack.com/p/serverless-payjoin-gets-its-wings)

[bip pull request](https://github.com/bitcoin/bips/pull/1483)

[mailing list](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2023-August/021868.html)

### Silent Payments

Silent Payments is a new static address protocol that makes it impossible to create transactions that reuses spks, and makes it impossible for an outside observer to associate a payment with a payment address.

[bip pull request](https://github.com/bitcoin/bips/pull/1458)

[mailing list](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2022-March/020180.html)

### CoinGrinder coin selection algorithm

This is a new metric for coin selection that minimizes the weight of the input set while creating change? WHYYYYYY?

[bitcoin core pull request](https://github.com/bitcoin/bitcoin/pull/27877)

### Civkit and BOLT12

Roadmap uploaded for Civkit, a permission-less marketplace built around nostr and lightning.  Looks like BOLT12 is something they are interested in

[github repo](https://github.com/civkit/documentation/blob/main/roadmap.md)

### LN Markets Increased Trading Limits, Hit A Record $50M Trading Volume In June

LNMarkets is a derivative trading platform that does deposits and withdrawals using the lightning network, no token necessary.

[substack](https://lnmarkets.substack.com/p/63-roy-sheinfeld-lnm-fam-and-lightning)

### IMF Paper on Taxing Bitcoin Sees 'Quasi-Anonymity' as Greatest Challenge

"Policymakers are struggling to accommodate cryptocurrencies within tax systems not designed to handle them; this paper reviews the issues that arise. The risks, for now, appear more latent than real. But this can change."

[link](https://www.nobsbitcoin.com/imf-paper-on-taxing-cryptocurrencies/)

### SEC charges NFT issuer Impact Theory for offering unregistered securities

Not Bitcoin related, but general reminder that speculative tokens have regulatory risk

[SEC announcement]([https://www.sec.gov/news/press-release/2023-163])

### Tornado Cash Developers charged with Money Laundering and sanctions violation

Not Bitcoin related, Tornado Cash is a non-custodial mixer for crypto.  Going after developers of privacy software brings concerns to those who work in the space, it is important to point out that projects surrounding Tornado Cash have at times attempted to work with surveillance companies,yet regulators will still go after them

According to the indictment, Storm and Semenov designed Tornado Cash with various privacy features despite knowing that their service would be used for illicit purposes.
"Moreover, the DOJ alleged they maintained control over Tornado Cash, which they could have used to implement transaction monitoring or other anti-money laundering features, despite publicly saying they could not actually control it."
"The indictment also makes frequent references to Alexey Pertsev, another co-founder, who was arrested last year in the Netherlands, where he currently awaits trial on money laundering allegations."

Bitcoin privacy projects (coin mixers with centralized coordinators) may also fall under the same scrutiny

[article]([https://www.nobsbitcoin.com/tornado-cash-developers-charged-with-money-laundering-and-sanctions-violations/])

### Blockstream Greenlight announced

Greenlight is a set of software tools to utilize Blockstream's infrastructure to utilize the lightning network in a self-custodial way

[blog post](https://blog.blockstream.com/greenlight-by-blockstream-scalable-non-custodial-lightning-infrastructure-now-open-to-developers/)

### Floresta, a utreexo-based Electrum server

Electrum is the backend for many Bitcoin wallets, electrum requires a fully indexed bitcoin core node. utreexo is a way to lessen the burden to run a Bitcoin node

[link](https://medium.com/vinteum-org/introducing-floresta-an-utreexo-powered-electrum-server-implementation-60feba8e179d)

### Lightning HTLCs, in detail!

A very nice explanation on the HTLCs that traverse the lightning network
This post will walk through the different operations of a Lightning channel by following a long-running example with plenty of explanatory diagrams. First, we explore how Hash Time Locked Contracts (HTLCs) are added to a channel and how channel peers commit to a new state including these HTLCs. Next, we discuss how a channel’s normal flow is re-established after a disconnection. And finally, we finish with how a cooperative channel closure happens. These topics are all covered in Bolt 2 for those interested in learning more. Note that some of these operations will change with Taproot channels, which will be detailed in a future post.

[link](https://lightning.engineering/posts/2023-06-28-channel-normal-op/?ref=nobsbitcoin.com)

### Blockstream Simplicity

Simplicity is a smart contracting language, similar in spirit to Bitcoin Script or EVM. Like Hacspec (or TLA+, or Alloy), Simplicity is also a specification language, meaning its semantics have a precise mathematical model that allows formally proving statements about programs. If the contract is written in Simplicity, you can prove correctness properties directly. For instance, you can prove that the coins cannot move without signature X, or that the program cannot exceed Y memory threshold.

[link](https://blog.blockstream.com/building-blocks-of-simplicity-values-and-types)

[whitepaper](https://blockstream.com/simplicity.pdf?ref=blog.blockstream.com)

### Nostr, zaps and stuff (always)

Taiwan BitDevs would like to explore Nostr with the audience by generating an npub with the audience present to follow along.
Nostr stands for "notes and other stuff transmitted over relays" it is a protocol designed around censorship resistance which can be used for social media. Nostr is a lot of fun and a great way to use Lightning Network (NIP-57 / zaps / LNURL)

[github link](https://github.com/nostr-protocol/nostr)

[web client](https://snort.social)

[Amethyst android](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst&hl=en&gl=US)

[Damus iOS](https://apps.apple.com/ca/app/damus/id1628663131)
