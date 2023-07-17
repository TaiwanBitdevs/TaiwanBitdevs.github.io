---
layout: post
type: socratic
title: "Socratic Seminar 12: Lightning Strikes Again!"
meetup: https://www.meetup.com/taiwan-bitdevs/events/294778654/
---

## Announcements
Welcome again Bitdevs Taiwan

Our twelveth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Phoenix Wallet Splicing

Splicing changes the game. Phoenix now manages a single dynamic channel, no more 1% fee on inbound liquidity, better predictability and control, trustless swaps. The new fee schedule is detailed here.

[annoucement]([https://acinq.co/blog/phoenix-splicing-update])

### Binance adds Lightning (finally!)

Binance adds Lightning network support after 5 years! Better than being last!

[Binance Announcement](https://www.binance.com/en/support/announcement/binance-completes-integration-of-bitcoin-btc-on-lightning-network-opens-deposits-and-withdrawals-eefbfae2c0ae472d9e1e36f1a30bf340?ref=AZTKZ9XS)

[article](https://www.nobsbitcoin.com/binance-completed-integration-of-the-lightning-network/)

### Zapple Pay, get around the Damus Zap block from iOS

Apple forced Damus remove the "Zap" feature which enabled Lightning-tipping for posts.  Here is a work-around by replacing the "shaka" with a Zap.  This is possible because nostr is open

[Zapple Pay Guide](https://habla.news/tony/zapplepay)

### Zeus Wallet announced adding a node-less option

Zeus is a Mobile App that can connect to a lightning node. This new feature will allow a wallet to be able to make payments without a node


[Link](https://primal.net/thread/note1pxpd0vedg90xsylsxgcx72ajjp975stgxddy5hfhl28jngua2ulstg7aja?ref=nobsbitcoin.com)

### SBW Wallet to shutdown Lightning functionality, will retain on-chain wallet

Simple Bitcoin Wallet is one of the early lightning wallets using a "hosted channel" model called IMMORTAN.  It looks like the developer no longer wishes to continue. Be sure to move out any funds if used

[link](https://twitter.com/SimpleBtcWallet/status/1680801928295456769?s=20)

### Bitcoin Spot ETF Applications Refiled To Bring Coinbase Surveillance to Next Level

Asset management giant BlackRock took the first steps Thursday to launch a spot bitcoin exchange-traded fund, which has long been a point of contention between crypto advocates and federal regulators.

The firm filed an application with the U.S. Securities and Exchange Commission to launch the iShares Bitcoin Trust. If approved, the ETF would allow easy access for investors to get exposure to crypto in a product from one of Wall Street’s largest companies.

As exciting as it is to have BlackRock enter the space so thaat Grayscale is no longer the only game in town, it is important to remember that Larry Fink once called Bitcoin an "index of money laundering", and this product does not have any form of gurantee for actual Bitcoin redemption/settlement

[updated news article](https://www.nobsbitcoin.com/spot-etf-coinbase-surveillance-agreement/)

[news article](https://www.cnbc.com/2023/06/15/blackrock-files-for-spot-bitcoin-etf-with-coinbase-as-a-crypto-custodian.html)

[criticism: Allan Farrington - Just trust me, bro](https://allenfarrington.medium.com/trust-me-bro-fb5a25964634)

[Fidelity also joins in the fun?](https://twitter.com/BitcoinMagazine/status/1670762619677085697)

### Civkit and BOLT12

Roadmap uploaded for Civkit, a permission-less marketplace built around nostr and lightning.  Looks like BOLT12 is something they are interested in

[github repo](https://github.com/civkit/documentation/blob/main/roadmap.md)

### LN Markets Increased Trading Limits, Hit A Record $50M Trading Volume In June

LNMarkets is a derivative trading platform that does deposits and withdrawals using the lightning network, no token necessary.

[substack](https://lnmarkets.substack.com/p/63-roy-sheinfeld-lnm-fam-and-lightning)

### IMF Paper on Taxing Bitcoin Sees 'Quasi-Anonymity' as Greatest Challenge

"Policymakers are struggling to accommodate cryptocurrencies within tax systems not designed to handle them; this paper reviews the issues that arise. The risks, for now, appear more latent than real. But this can change."

[link](https://www.nobsbitcoin.com/imf-paper-on-taxing-cryptocurrencies/)

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
