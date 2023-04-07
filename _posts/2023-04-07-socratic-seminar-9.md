---
layout: post
type: socratic
title: "Socratic Seminar 9: 好 '九' 不見"
meetup: https://www.meetup.com/taiwan-bitdevs/events/292571920/
---

## Announcements
Welcome back Bitdevs Taiwan

Our ninth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### ZeroSync and Blockstream

ZeroSync leverages zero knowledge proofs to allow bitcoin clients to validate the chainstate without downloading entire blocks
Sync Bitcoin Core from Space!

[blockstream satellite](https://twitter.com/Blockstream/status/1641897424305246224?s=20)

[Article in Chinese](https://news.cnyes.com/news/id/5134900)

### Sparrow Wallet adds Border Wallets to help with seed phrasees

Border Wallets solve a problem faced by many Bitcoiners; how to quickly, easily, securely and reliably memorise 12 or 24 (or more) seed words. The idea draws on a concept known as the Picture Superiority Effect, and employs the use of user-generated patterns applied to a randomised map of (BIP-39 compliant) seed words - offline, in a secure, air-gapped setting.

[border wallet website](https://www.borderwallets.com/)

[sparrow wallet changelog](https://github.com/sparrowwallet/sparrow/releases)

### Blockstream Jade mining (April Fools joke)

Cute april fools joke, apparently you can emulate a Jade on x86 for better performance 

[website to start mining ](https://jademiner.blockstream.com/)


### Payjoin rust implementatioon

Taiwan Bitdevs' Dan Gould introduces his payjoin toolkit end of last month. Payjoin is one of the ways to use Bitcoin in a privacy-preserving manner.

Taiwan BitDevs have some questions about

[tweet](https://twitter.com/bitgould/status/1640746521829208066?s=20)

[wasabi inputs flagged by custodial services](https://www.nobsbitcoin.com/el-salvadors-chivo-wallet-is-reportedly-flagging-and-freezing-txs-from-wasabi/)

### Taproot buried in Bitcoin Core
Welcome Andrew Chow :)

[stack exchange](https://bitcoin.stackexchange.com/questions/117569/why-isnt-the-taproot-deployment-buried-in-bitcoin-core)

### Operation Chokepoint 2.0(?)
Silvergate -> SVB bailout, Signature shutdown.  Lots of chatter about US regulators cracking down on crypto perhaps another round of bank closures like what happened in 2014 which debanked many bitcoin services.

[tweet](https://twitter.com/jimmysong/status/1641083651873206272?s=20)

### Paxful shuts down
Paxful is a P2P Bitcoin marketplace started in 2015. According to founder Ray Youseff it was shut down due to internal legal disputes. P2P marketplaces remain popular across many exchanges and services
[article](https://decrypt.co/125411/paxful-bitcoin-marketplace-closure-cofounder-lawsuit)


### Nostr, zaps and stuff

Nostr stands for "notes and other stuff transmitted over relays" it is a protocol designed around censorship resistance which can be used for social media. Nostr is a lot of fun and a great way to use Lightning Network (NIP-57 / zaps / LNURL)

[github link](https://github.com/nostr-protocol/nostr)


### Skull of Satoshi by Greenpeace USA backfires(?)

March 24th Greenpeace USA tries to start a marketing campaign to again try to disparage Bitcoin mining. Fun reactions, maybe Skull of Satoshi should come to Taiwan?

[tweet](https://twitter.com/greenpeaceusa/status/1638952445542801425?s=20)

### Invalid Block (too many sigops)
F2Pool mined an invalid block on April 1st (block 783426). More than 80,000 signature operations so not accepted by the network, block replaced by Foundry)

[tweet](https://twitter.com/BitMEXResearch/status/1642151592609607685?s=20)

[bitcointalk post](https://bitcointalk.org/index.php?topic=5447129.0)

### LND v.0.16.0 released
LND had a funky behavior where nodes miss channel updates (occurs on nodes with lots of channels). This might explain it

[pull request](https://github.com/lightningnetwork/lnd/pull/7239)

### BDK 1.0.0-alpha
BDK test release, improvements in asynchronous operations
[release notes](https://github.com/bitcoindevkit/bdk/releases/tag/v1.0.0-alpha.0)

