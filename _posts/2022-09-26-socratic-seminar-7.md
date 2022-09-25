---
layout: post
type: socratic
title: "Socratic Seminar 7: Coin Selection, Fedimint, and DriveChains"
meetup: https://www.meetup.com/taiwan-bitdevs/events/288662252/
---

## Announcements

Our seventh Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents. As time permits, a demo of LNURL standards will be presented by lightning network contributors of BitDevs

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. Skim the [discussion topics](https://github.com/TaiwanBitdevs/TaiwanBitdevs.github.io/pull/11) on GitHub. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Coin Selection

Evan has been working on the coin selection module of `bdk_core`. What are some considerations and requirements when building a coin selection library?

[github pull-request](https://github.com/LLFourn/bdk_core_staging/pull/23)

### Fedimint

Fedimint, a federated chaumian ecash system, claims to be the "third pillar" of Bitcoin (alongside the Bitcoin blockchain and Lightning Network), but what does this all mean? How does Fedimint "solve custody" for Bitcoin?

Currently, it is harder to custody ecash than on-chain Bitcoin. Each ecash-token needs to be backed up individually, otherwise the user will lose funds permanently. How can deterministic client nonce generation solve this?

[blog post](https://bitcoinmagazine.com/culture/will-fedimints-bring-bitcoin-to-the-world)

[github issue](https://github.com/fedimint/fedimint/issues/502)

### DriveChains with `SIGHASH_ANYPREVOUT`

Jeremy Rubin proposes a way in which drivechains could be implemented with `SIGHASH_ANYPREVOUT` (APO). APO was proposed in BIP-118, while the original drivechain soft-fork proposal is in BIP-300. What are the benefits and tradeoffs between these two drivechain proposals?

[optech newsletter](https://bitcoinops.org/en/newsletters/2022/09/21/)

[mailing list](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2022-September/020919.html)

### Improve Payment Reliability in Lightning with "Valves"

Valves are an important tool for flow control in fluid and gas networks. Rene Pickhardt (BitMEX Grantee) investigates how valves on the Lightning Network can improve flow control and reduce payment failure rates.

[blog post](https://blog.bitmex.com/the-power-of-htlc_maximum_msat-as-a-control-valve-for-better-flow-control-improved-reliability-and-lower-expected-payment-failure-rates-on-the-lightning-network/)

### Bitcoin Core 24.0 Release Candidate 1

Notable changes include P2P/network improvements to address a potential denial-of-service attack, wallet support for `wsh()` descriptors, an experimental RPC call to migrate legacy wallets to descriptor wallets, and various other RPC/HTTP-API/GUI changes.

[release notes draft](https://github.com/bitcoin-core/bitcoin-devwiki/wiki/24.0-Release-Notes-draft)
