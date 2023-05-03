---
layout: post
type: socratic
title: "Socratic Seminar 10: May the force of Bitcoin be with you!"
meetup: https://www.meetup.com/taiwan-bitdevs/events/293166577
---

## Announcements
Welcome again Bitdevs Taiwan

Our tenth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Civ Kit: A Peer-to Peer electronic marketplace system

Proposed by Nicholas Gregory, Ray Youssef and Antoine Riard
This design builds on top of the new Nostr protocol for its peer-to-peer order book and relies on the Bitcoin blockchain as a source of truth for its Web-of-Stakes market ranking paradigm.
Market trades are locked under Bitcoin contracts to avoid reliance on trusted third parties for dispute arbitration.
[link to whitepaper](https://github.com/civkit/paper/blob/main/civ_kit_paper.pdf)

Noones appears to be the successor to paxful p2p marketplace -- based on civkit(?) 

[noones market](https://noones.com/)

### First Republic Bank collapses, acquired by JP Morgan Chase

Reminder that Bitcoin was born from the financial crisis, this is following the Silicon Valley Bank (16th largest US bank) collapse. First Republic Bank held $200b of asseets and was 13th largest US Bank

[tweet](https://twitter.com/cryptograffiti/status/1653159862594076672?s=20)
[more banks will fail](https://www.discreetlog.com/banking-crisis/)
[other small bank failure](https://twitter.com/KobeissiLetter/status/1653406861859643400?s=20)


### BlueWallet Custodial Lightning Wallet closure postponed another month, May 31st

Reminder for any BlueWallet users to move their funds off their custodial service

[link](https://www.nobsbitcoin.com/bluewallet-postpones-lightning-node-shut/)

### Shiro Web Wallet with RGB released, available on Umbrel

"Shiro at the current form is still very rough and alpha and only available on testnet for now. Nonetheless, you can issue, send and receive fungible RGB tokens, allowing you to experiment with the protocol and gain first hand experience."

[link](https://www.nobsbitcoin.com/shiro-wallet-umbrel-release/)

### Bitcoin Network Reaches New Transaction All-Time High As Fees Surge Due To BRC-20 Tokens

BRC-20 token is an experimental fungible token standard, created using Ordinals and inscriptions of JSON data to deploy token contracts, mint them, as well as transfer tokens

[link](https://thebitcoinmanual.com/articles/brc-20-tokens)

### Floresta, a utreexo-based Electrum server

Electrum is the backend for many Bitcoin wallets, electrum requires a fully indexed bitcoin core node. utreexo is a way to lessen the burden to run a Bitcoin node

[link](https://medium.com/vinteum-org/introducing-floresta-an-utreexo-powered-electrum-server-implementation-60feba8e179d)

### Country of Bhutan appears to have been mining Bitcoin

Bhutan is perfectly set up to mine digital assets. For the country’s size, it has vast amounts of green energy generated through run-of-the river hydro projects and more importantly it is cheap.

[link](https://www.nobsbitcoin.com/the-kingdom-of-bhutan-has-been-mining-bitcoin-for-years/)

[softwar theory/lecture @ MIT Bitcoin Expo](https://www.mitbitcoinexpo.org/streaming)


### Nostr, zaps and stuff (again)

Taiwan BitDevs would like to explore Nostr with the audience by generating an npub with the audience present to follow along.
Nostr stands for "notes and other stuff transmitted over relays" it is a protocol designed around censorship resistance which can be used for social media. Nostr is a lot of fun and a great way to use Lightning Network (NIP-57 / zaps / LNURL)

[github link](https://github.com/nostr-protocol/nostr)

[web client](https://snort.social)

[Amethyst android](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst&hl=en&gl=US)

[Damus iOS](https://apps.apple.com/ca/app/damus/id1628663131)

### Ordinals Broken(?) Bug or bad design

Discussion in Taiwan BitDevs LINE group about ordinals theory.  This github discussion can help explain flaws in ordinal theory

[github discussion](https://github.com/casey/ord/discussions/2015)
