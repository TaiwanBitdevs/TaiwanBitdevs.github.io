---
layout: post
type: socratic
title: "Socratic Seminar 5: Discrete Log Contracts with Chris Stewart "
meetup: https://www.meetup.com/taiwan-bitdevs/events/287163977/
---

## Announcements

Our fourth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion on the latest bitcoin developents for 40 minutes. Then, guest speaker Chris Stewart, founder of Suredbits, will discuss "Discrete Log Contracts: What are they and how do they work?" After the 90 minute seminar we will walk to Café Libero No. 1, Lane 243, Jinhua St, Da’an District, Taipei City, 106 to socialize.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. Skim the [discussion topics](https://github.com/TaiwanBitdevs/TaiwanBitdevs.github.io/pull/11) on GitHub. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. 

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Storm P2p arbitrary LN Messaging

LNP/BP has messaging that's working over the lightning network

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Status update: we are completing (debugging) integration of all three nodes (LNP, RGB, Storm) together required to get <a href="https://twitter.com/hashtag/RGB?src=hash&amp;ref_src=twsrc%5Etfw">#RGB</a> working over Lightning. Expect to release these three nodes by this Wednesday and present on our usual dev call. <a href="https://t.co/Dkqee0Pl45">https://t.co/Dkqee0Pl45</a></p>&mdash; LNP/BP Standards Association (@lnp_bp) <a href="https://twitter.com/lnp_bp/status/1546424964621996033?ref_src=twsrc%5Etfw">July 11, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### Wasabi 2.0 Released

- Auto CoinJoin
- Questionable algorithm

[blog post](https://blog.wasabiwallet.io/wasabi2-0-released/)

### Using routing fees to signal liquidity

Using routing fees to signal liquidity: developer ZmnSCPxj posted to the Lightning-Dev mailing list an argument for how optimally cheap and reliable payments could be obtained through game theoretic behavior between spenders and routing nodes:

- Spenders should choose paths that charge less in routing fees.

- Routing nodes should charge more to use a channel as its capacity decreases. E.g., if most of the balance in a channel is owned by Alice, she can reliably forward payments to Bob and so she shouldn’t charge much; but, as more balance is forwarded towards Bob, Alice’s ability to forward additional payments decreases, so she should charge higher fees.


### X-only workaround

Bitcoin public keys are points on a two-dimensional graph which are referenced by the intersection of an x coordinate and a y coordinate. For any given x coordinate, there are only two valid y coordinates and these can be calculated from the x value. This allowed an optimization in the design of taproot to require all public keys used with BIP340-style schnorr signatures to only use a certain one of these y coordinates, allowing any public keys included in transactions to omit including the y point entirely, saving one vbyte per signature over the original taproot design.

At the time, this technique (called x-only public keys) was thought to be an optimization with no significant tradeoffs, but later design work on OP_TAPLEAF_UPDATE_VERIFY (TLUV) revealed that x-only pubkeys required either computationally limiting the proposal or storing extra data in the block chain or UTXO set. The problem may affect other advanced uses of pubkeys as well.

This week, Tim Ruffing posted to the Bitcoin-Dev mailing list a potential workaround that only requires a slight bit of additional computation by signers—an amount that even a resource-constrained hardware signing device can probably perform without making its user wait too long.

Credit: [Bitcoin Optech Newsletter #208](https://bitcoinops.org/en/newsletters/2022/07/13/)

### Allowing deliberately slow LN payment forwarding

In a reply to a thread about recursive/nested MuSig2 (see Newsletter #204) and the latency that nodes using it would add when routing payments, developer Peter Todd asked on the Lightning-Dev mailing list whether it would “be worthwhile to allow people to opt-in to their payments happening more slowly for privacy?” For example, if Alice and Bob each sent forward-slowly payments around the same time through Carol’s forwarding node to Dan’s forwarding node, Carol would be able to forward both payments together, reducing the amount of privacy-leaking information about the participants that third parties could discover through balance probing, network activity surveillance, or other techniques. Developer Matt Corallo agreed it was an interesting idea.

Credit: [Bitcoin Optech Newsletter #208](https://bitcoinops.org/en/newsletters/2022/07/13/)

### Full RBF in Bitcoin Core

Replace by fee allows transactions to be [R]eplaced [b]y later transactions paying a higher [fee]. bitcoin core #25353 introduces `mempoolfullrbf` option which allows any transaction to be replaced. Previously, only transactions that opt-in with a flag could be replaced.

### Zero-conf channel opens in LND and Core Lightning

Core Lightning #5275 adds support for zero-conf channel opens and the related Short Channel IDentifier (SCID) aliases (see Newsletter #203). This includes updates to the listpeers, fundchannel, and multifundchannel RPCs.

Credit: [Bitcoin Optech Newsletter #208](https://bitcoinops.org/en/newsletters/2022/07/13/)


### Bitcoin Ordinals

####  What are ordinals?

Ordinals are numbers, like this: 804766073970493. Every satoshi, which is ¹⁄₁₀₀₀₀₀₀₀₀ of a bitcoin, has an ordinal, and every ordinal has a satoshi. When a satoshi changes hands, so does its ordinal. There are a lot of satoshis, and so there are a lot of ordinals. Two quadrillion ninety-nine trillion nine hundred ninety-nine billion nine hundred ninety-seven million six hundred ninety thousand, to be precise.

#### What can ordinals do?

Ordinals can be used for anything needing a public, persistent, transferable, decentralized identity. This includes NFTs, accounts, stablecoins, PKI, and more. For more ideas, see the BIP.

#### What are ordinals not?

Ordinals are not a side chain, do not require any changes to the bitcoin protocol, and are extremely simple.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">RGB: Boiling the ocean<br>Ordinals: Boiling a teaspoon of heroin<br><br>We are not the same 😤😤😤</p>&mdash; Casey Rodarmor (@rodarmor) <a href="https://twitter.com/rodarmor/status/1548810977084198912?ref_src=twsrc%5Etfw">July 17, 2022</a></blockquote>

#### How traditional money transfer work vs bitcoin/lightning network: （could help taiwanese business)

 國際外匯系統 vs 比特幣 -- 是不是可以幫助台灣的貿易公司

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">There is a widespread belief amongst financial commentators that the problem of international payments has been &quot;solved&quot; by fintechs such as <a href="https://twitter.com/Wise?ref_src=twsrc%5Etfw">@Wise</a>. <br><br>Let me show you how this isn&#39;t true.</p>&mdash; Boaz (@sobradob) <a href="https://twitter.com/sobradob/status/1546141704645971969?ref_src=twsrc%5Etfw">July 10, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

#### Canadian gas producer using old generation (17nm TSMC) miners to sell oil/gas to global market

加拿大天然氣挖礦 - 利用台灣晶片

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Each of these <a href="https://twitter.com/hashtag/bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#bitcoin</a> boxes mitigate 60,000 cubic feet of methane emissions every day (methane is 25x as potent as carbon dioxide at trapping heat)<a href="https://t.co/4y1g8goOc4">pic.twitter.com/4y1g8goOc4</a></p>&mdash; Documenting Bitcoin 📄 (@DocumentingBTC) <a href="https://twitter.com/DocumentingBTC/status/1547278900882964482?ref_src=twsrc%5Etfw">July 13, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
