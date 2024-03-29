---
layout: post
type: socratic
title: "Socratic Seminar 13: Hungry Ghost Festival"
meetup: https://www.meetup.com/taiwan-bitdevs/events/295581262/
---

## Announcements
Welcome again Bitdevs Taiwan

Our thirteenth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Electrum Security Update

Lightning Security issues were fixed in this update.  Electrum uses trampoline routing with the Electrum node along with some other hardcoded lightning nodes.  Trampoline routing allows for the pathfinding to occur on the trampoline nodes so the client application itself (which may not have the resources to analyze the entire channel graph) doesn't have to calculate routes. Nature of the security issue will be disclosed 9-11-2023.
[link]([https://nitter.at/ElectrumWallet/status/1693950020028903685?ref=nobsbitcoin.com])

### Fork(?) of Zap Android called Bitbanana

Bitbanana takes over the no longer maintained Zap Wallet. Zap was one of the first LND remote control wallets for Android.  It uses lndconnect which encodes the authentication macaroons to make REST API calls to a remote LND node
[article]([https://github.com/michaelWuensch/BitBanana])

### Oman starts to mine bitcoin, declares Bitcoin Sharia Law compliant

The Sultanate of Oman is a country in the Arabian Peninsula with a population of 5.4 Million.

H.E Sheikh Mansour Bin Taleb Bin Ali Al Hinai, Chairman of Oman's Authority for Public Services Regulations, publicly commented in a press statement about his nation’s government support of privately-owned bitcoin mining facilities, which are set to attract a total investment of over $1.1 billion, "this initiative aligns with our goal to diversify our economy, integrating modern technologies while upholding our commitment to ethical and sustainable practices."
Apple forced Damus remove the "Zap" feature which enabled Lightning-tipping for posts.  Here is a work-around by replacing the "shaka" with a Zap.  This is possible because nostr is open

Some cultures/religions do not allow for usury, it has been argued that Bitcoin suits those cultures.  This is a great example of how the incentives of Bitcoin can align with ethics.

[forbes article]([https://www.forbes.com/sites/irinaheaver/2023/08/24/omans-bold-bitcoin-play-11-billion-investment-on-bitcoin-mining-infrastructure/?sh=4c6255742709])

### Bitaxe Ultra - Open Source miner based on BM1366 chips

Since Taiwan BitDevs was so enamored with the NerdMiner, its also fun to point out the other options in the market.  While these likely wont be able to compete at scale, could be a fun project to pursue for those interested in mining

Bitaxe is a fully open source hardware Bitcoin ASIC miner. Ultra is the 3rd major revision of the bitaxe that now includes the BM1366 ASIC from the S19XP.

[github link]([https://github.com/skot/bitaxe/tree/ultra?ref=nobsbitcoin.com])

### LNURLp - proposal to remove metadata decription hash from validation on invoices

LNURL is a set of specifications which allow lightning apps to communicate with the nodes on the lightning network through webservers. For example, LNURLp allows for static invoices by having lightning wallets request invoices from a node through a webserver.  A popular implementation of LNURL is lightning address, which is the standard of using e-mail like names for lightning wallets.

This proposal attempts to simplify the current spec by removing one of the validation checks, the goal appears to be to increase interoperability of lightning implementation.  At current Lightning wallets that implement LUD-06(LNURL Pay) are expected to validate fields in "metadata" provided by the LNURL provider with the description hash in a generated invoice.  This requirement made it so CLN nodes had difficulty implementing LNURLp because it doesn't include a description hash in the invoices it generates.

[tweet]([https://twitter.com/callebtc/status/1695346828584047085?s=20])

### Zaprite introduces payment links
Software service to allow businesses to accept Bitcoin payments integrating with current processes, includes invoicing for products and subscriptions using URL links

[link]([https://twitter.com/ZapriteApp/status/1695120846774288738?s=20])
[blog post]([https://blog.zaprite.com/zaprite-platform-upgrades/])

### SBW Wallet to shutdown Lightning functionality, will retain on-chain wallet

(Another reminder)
Simple Bitcoin Wallet is one of the early lightning wallets using a "hosted channel" model called IMMORTAN.  It looks like the developer no longer wishes to continue. Be sure to move out any funds if used

[link](https://twitter.com/SimpleBtcWallet/status/1680801928295456769?s=20)

### DriveChain Drama -- some articles and discussions to dive into

BIP300/BIP301 is proposed change to allow nodes to store additional messages on the blockchain, commonly believed to enable the Bitcoin network to secure sidechains.
Disputes mostly surround its effect on mining incentivves and lack of activation method

[paul sztorc tweet]([https://twitter.com/Truthcoin/status/1695804825307410790?s=20])

[brian trollz tweet]([https://twitter.com/brian_trollz/status/1694389929822814355?s=20])

[adam back tweet]([https://twitter.com/adam3us/status/1696185360571826247?s=20])


[tweet about incentives]([https://twitter.com/MrHodl/status/1696138004408963203?s=20])

[messing with incentives]([https://twitter.com/bergealex4/status/1695215070333018497?s=20])

### CTV Drama -- some articles and discussions to dive into

CTV refers to BIP119. CheckTemplateVerify is an OP code to interchangeably use UTXOs under certain conditions.  CheckTemplateVerify can enable things like channel splicing/channel factories
CTV has been criticized for its activation method, wanting to go the route of miner activation (like Taproot)


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
