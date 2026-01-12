---
layout: post
type: socratic
title: "Socratic Seminar 28: All the time in the world is all they've got"
meetup: https://www.meetup.com/taiwan-bitdevs/events/312842288
---

## Announcements

Our 28th Socratic Seminar event will be held at TempoHouse

Tempohouse generously offered their space to host BitDevs

This time would like to take the opportunity to go over something more Taiwan-centric alongside the usual socratic

Bitcoin is the worlds first global digital money, and money speaks all languages. To use Bitcoin is to communicate with the world which throughout history Taiwanese have been eager to do. Taiwanese also contributes to Bitcoin in a meaningful way, let's explore the unique aspects of how Taiwan is drawn to Bitcoin .

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### BIP444 Softfork Proposal
user dathonohm submitted a BIP (currently unassigned but 444 is how it is referred to at the moment) Reduced Data Temporary Softfork in response to growing adoption of Bitcoin Core v30.0.0 which relays and validates large OP_Returns that may have uninteded consequences

Blocks with a height from (TBD) until and including 987424 are checked with these additional rules:

* New output scriptPubKeys exceeding 34 bytes are invalid, unless the first opcode is OP_RETURN, in which case up to 83 bytes are valid.
* OP_PUSHDATA* with payloads larger than 256 bytes are invalid, except for the redeemScript push in BIP16 scriptSigs.
* Spending undefined witness (or Tapleaf) versions (ie, not Witness v0/BIP 141 nor Taproot/BIP 341) is invalid.
* Witness stacks with a Taproot annex are invalid.
* Taproot control blocks larger than 257 bytes (a merkle tree with 128 script leaves) are invalid.
* Tapscripts including OP_SUCCESS* opcodes anywhere (even unexecuted) are invalid.
* Tapscripts executing the OP_IF or OP_NOTIF instruction (regardless of result) are invalid.

##### Some background
[ML discussion - Limit ScriptPubkey Size >=520 Bytes Consensus](https://groups.google.com/g/bitcoindev/c/YO8ZwnG_ISs)

Precedent of invalidating blocks from uninteded consequences of bitcoin reference implementation
* Inflation Bug (Satoshi Era)
* LevelDB/BerkeleyDB Bug (2013)

##### Common Misconceptions
* Difference between hard fork and soft forks and what has happened in the past
* Bip444 is not an "airdrop"
* Signaling vs Doing Nothing vs URSF

[link](https://github.com/bitcoin/bips/pull/2017)

[mailing list discussion](https://groups.google.com/g/bitcoindev/c/nOZim6FbuF8)

### YouTube-alternative video app Rumble implements Bitcoin tipping
Rumble, a video-sharing platform with over 51 million monthly users, is partnering with Tether to roll out tipping in Bitcoin (and other crypto) by mid-December. The move aims to empower creators with additional monetisation tools beyond ads.  
[link](https://beincrypto.com/rumble-challenges-youtube-with-bitcoin-tipping/)

### Trezor quantum-ready hardware wallet
Trezor has unveiled its new hardware wallet model (Safe 7) which features a “quantum-ready” architecture—designed to support future post-quantum firmware updates and includes an auditable secure element. However, the wallet does *not* provide immediate quantum-proof on-chain protection today.  
[link](https://cryptoslate.com/what-trezors-new-quantum-ready-hardware-wallet-really-means-for-bitcoin/)

### Bitcoin-only app Relai secures EU approval
Relai, a Swiss “Bitcoin-only” investment app, has become one of the first such firms to receive a regulatory authorisation (a MiCA license via France’s regulator) enabling it to offer regulated services across the EU. This signals a milestone for regulated Bitcoin-only platforms in Europe.  
[link](https://bravenewcoin.com/insights/bitcoin-app-relai-secures-historic-eu-approval-under-mica-framework)

### Solo BTC miner secures \$347
A solo miner solved block 920,440 entirely by themselves (outside major mining pools) and earned approximately \$347,455 (≈ 3.125 BTC + fees). This win highlights the potential for smaller miners to compete and underscores the decentralisation ethos of Bitcoin.  
[link](https://cointelegraph.com/news/solo-bitcoin-miner-wins-block-self-soverignty)

### AWS outage took down Coinbase
An operational failure at Amazon Web Services (specifically in the US-EAST-1 region involving its DynamoDB/DNS infrastructure) caused widespread disruptions, including to Coinbase and various Ethereum layer-2 networks. The incident highlighted the crypto industry’s dependence on centralised infrastructure even while promoting decentralisation.  
[link](https://cryptoslate.com/aws-failure-exposes-cryptos-centralized-weak-point/)

### Nostr, zaps and stuff (always)

Taiwan BitDevs would like to explore Nostr with the audience by generating an npub with the audience present to follow along.
Nostr stands for "notes and other stuff transmitted over relays" it is a protocol designed around censorship resistance which can be used for social media. Nostr is a lot of fun and a great way to use Lightning Network (NIP-57 / zaps / LNURL)

#### NIP update - nostr marketplace (NIP-15)
Theres an LNBits extension that allows you to list and shop for goods using nostr relays and get paid through Bitcoin/Lightning

[tutorial](https://github.com/lnbits/lnbits/wiki/LNbits-Extensions)
[nip-15](https://github.com/nostr-protocol/nips/blob/master/15.md)


[github link](https://github.com/nostr-protocol/nostr)

[web client](https://snort.social)

[Amethyst android](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst&hl=en&gl=US)

[Damus iOS](https://apps.apple.com/ca/app/damus/id1628663131)
