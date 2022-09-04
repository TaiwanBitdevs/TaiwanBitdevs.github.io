---
layout: post
type: socratic
title: "Socratic Seminar 6: Bitcoin and Mooncakes "
meetup: https://www.meetup.com/taiwan-bitdevs/events/287163977/
---

## Announcements

Our sixth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents. As time permits, a demo of LNURL standards will be presented by lightning network contributors of BitDevs

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. Skim the [discussion topics](https://github.com/TaiwanBitdevs/TaiwanBitdevs.github.io/pull/11) on GitHub. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Fedimint (formerly Minimint) announced

Fedimint refers to a rust implementation of a federated chaumian e-cash mint; a model for distributed custody.
Fedimint is an open source protocol to custody and transact bitcoin in a community context, built on a strong foundation of privacy.

[blog post] (https://twitter.com/fedimint/status/1564190687234506753?s=20&t=0uJ-Kwmb0LuJgLdDLHBpeQ)

### NYDIG announces Lightning Accelerator WOLF (Wolf in Wolf's clothing)

NYDIG is a bitcoin company that's fusing high tech with institutional-grade finance to usher in a new era of financial products. Wolf is meant to attract entrepreneurs, investors, and highly motivated individuals to push lightning network adoption forward. Anyone interested should apply!

[blog post] (https://bitcoinmagazine.com/business/nydig-announces-lightning-accelerator-project)

### Tornado Cash developer arrested, github suspended, services restricted/blocked

Still unknown why an open source developer was arrested, still something to watch out for

[blog post](https://cointelegraph.com/news/tornado-cash-saga-highlights-legal-issues-affecting-the-crypto-market)

### Sparrow Wallet developer proposes Wallet Label  Export format

Wallet Labels are useful to keep track of transactions/UTXOs .  NOrmally wallet labels only carry across the same wallet software. Sparrow Wallet suports the import/export of many popular Wallet Formats

[blog post] (https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2022-August/020887.html)

### LND 0.15.1 beta released

Defaut taproot addresses, database migration, short channel id aliases (scid), and zero-conf channels
[blog post] (https://github.com/lightningnetwork/lnd/releases/tag/v0.15.1-beta)

### BDK enabling connectivity to electrum and esplora for blockchain data

BDK is a collection of libraries to build bitcoin software based in rust.

[blog post] (https://github.com/bitcoindevkit/bdk/pull/705)
[blog post] (https://github.com/bitcoindevkit/bdk/pull/722)

### Core-lightning (CLN) v0.12.0 released

Blockstream implementation Core-lightning adds new default plug-ins, bookkeeper (an accounting system), and commando (remote rpc authentication)

[blog post] (https://github.com/ElementsProject/lightning/releases/tag/v0.12.0)

### DLC development - BLS signatures for oracles to make attestations

Boneh-Lynn-Shacham is a cryptographic signature scheme. This proposal would require a soft fork for bitcoin clients (in this case clients running the oracle and the users relying on it) to validate these signatures
These sort of developments are discussed in the open to see if it is worthwhile

[blog post] (https://mailmanlists.org/pipermail/dlc-dev/2022-August/000149.html)


### defendingbtc.com -- Hodlnaut's trial against Craig Wright

Donations are coming in for hodlnaught to defend against Craig Wright who has been harassing Bitcoin contributors for years. Craig Wright claims to be Satoshi Nakamoto and has been unable to prove it.

[blog post] (https://www.defendingbtc.com/)
#### How traditional money transfer work vs bitcoin/lightning network: （could help taiwanese business)

 國際外匯系統 vs 比特幣 -- 是不是可以幫助台灣的貿易公司

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">There is a widespread belief amongst financial commentators that the problem of international payments has been &quot;solved&quot; by fintechs such as <a href="https://twitter.com/Wise?ref_src=twsrc%5Etfw">@Wise</a>. <br><br>Let me show you how this isn&#39;t true.</p>&mdash; Boaz (@sobradob) <a href="https://twitter.com/sobradob/status/1546141704645971969?ref_src=twsrc%5Etfw">July 10, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

#### Canadian gas producer using old generation (17nm TSMC) miners to sell oil/gas to global market

加拿大天然氣挖礦 - 利用台灣晶片

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Each of these <a href="https://twitter.com/hashtag/bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#bitcoin</a> boxes mitigate 60,000 cubic feet of methane emissions every day (methane is 25x as potent as carbon dioxide at trapping heat)<a href="https://t.co/4y1g8goOc4">pic.twitter.com/4y1g8goOc4</a></p>&mdash; Documenting Bitcoin 📄 (@DocumentingBTC) <a href="https://twitter.com/DocumentingBTC/status/1547278900882964482?ref_src=twsrc%5Etfw">July 13, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
