---
layout: post
type: socratic
title: "Socratic Seminar 21: Forever 21 (million)"
meetup: https://www.meetup.com/taiwan-bitdevs/events/302650155/
---

## Announcements
Welcome again Bitdevs Taiwan

We are at a our T7 location this month again, thanks to Evan!

Our special *21st* Socratic Seminar event will be held at No. 563, Section 4, Zhongxiao E Rd, 新仁里 · Xinyi District

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Disclosure of vulnerabilities affecting Bitcoin Core versions before 0.21.0

Update your nodes!
 Niklas Gögge posted to the Bitcoin-Dev mailing list a link to announcements of two vulnerabilities affecting versions of Bitcoin Core that have been past their end of life since at least October 2022. This follows a previous disclosure last month of older vulnerabilities (see Newsletter #310). We summarize the disclosures below:

* Remote crash by sending excessive addr messages: before Bitcoin Core 22.0 (released September 2021), a node that was told about more than 232 other possible nodes would crash due to exhaustion of a 32-bit counter. This could be accomplished by an attacker sending a large number of P2P addr messages (at least 4 million messages). Eugene Siegel responsibly disclosed the vulnerability and a fix was included in Bitcoin Core 22.0. See Newsletter #159 for our summary of the fix, which was written without us knowing that it patched a vulnerability.

* Remote crash on local network when UPnP enabled: before Bitcoin Core 22.0, nodes that enabled UPnP for automatically configuring NAT traversal (disabled by default due to previous vulnerabilities, see Newsletter #310) were vulnerable to a malicious device on the local network repeatedly sending variants of a UPnP message. Each message could result in the allocation of additional memory until the node crashed or was terminated by the operating system. An infinite loop bug in Bitcoin Core’s dependency miniupnpc was reported to the miniupnpc project by Ronald Huveneers, with Michael Ford discovering and responsibly disclosing how it could be used to crash Bitcoin Core. A fix was included in Bitcoin Core 22.0.

Additional vulnerabilities affecting later versions of Bitcoin Core are expected to be disclosed in a few weeks.

[mailing list](https://mailing-list.bitcoindevs.xyz/bitcoindev/bf5287e8-0960-45e8-9c90-64ffc5fdc9aan@googlegroups.com/)

### RFK Speech at Bicoin Conference 2024

Robert F. Kennedy Jr. delivers a groundbreaking speech Bitcoin 2024, outlining his vision for integrating Bitcoin into America's economic and national security strategies. As an independent presidential candidate, RFK Jr. proposes bold initiatives including making the US government a major Bitcoin holder, eliminating taxes on Bitcoin transactions, and using Bitcoin mining to incentivize green energy production.

[youtube](https://www.youtube.com/watch?v=ssYCRVpzcxc)
[中文翻譯](https://btczh.tw/posts/a8961609)

### Taiwan FSC Publishes Guidelines and Q&A for the Management of VASPs

Taiwan Regulators publishes guidelines for platforms offering virtual assets.  Surprisingly these guidelines are specific to not include Bitcoin.  This could be a start of interesting developments on how Taiwan treats Bitcoin.


[Announcement](https://www.crowe.com/tw/en-us/insights/insight-article_1130611)

### Full RBF enabled

Peter Todd announced that his pull request was merged. Default behavior for nodes will be mempoolfullrbf=1

Default settings are important (datacarrier changes are still not in Core)

[github](https://github.com/bitcoin/bitcoin/pull/30493#event-13769240409)

### Bitcoin Core v27.1: Bug Fixes & Performance Improvements

Another release of Core

"Bitcoin Core version v27.1 is now available from: https://bitcoincore.org/bin/bitcoin-core-27.1/ or through BitTorrent (magnet link)," announced the project.
"This release includes various bug fixes and performance
improvements, as well as updated translations. Please report bugs using the issue tracker at GitHub."

note: I think some of Taiwan BitDevs traditional chinese transaltions made it in
[github](https://github.com/bitcoin/bitcoin/releases/tag/v27.1)


### Bitcoin Optech #306: Disclosure of Vulnerabilities Affecting Older Versions of Bitcoin Core

This issue announces an upcoming disclosure of Bitcoin Core vulnerabilities, and describes: a draft BIP for testnet4, functional encryption covenants, proposed updates to 64-bit arithmetic in Bitcoin Script, looks at OP_CAT script to validate proof of work, as well as proposed update to BIP21.

"Several members of the Bitcoin Core project discussed on IRC a proposed policy for disclosing vulnerabilities that affected older versions of Bitcoin Core..."
"After this policy has a chance to be further discussed, it is the intention of the project to begin disclosing vulnerabilities affecting Bitcoin Core 24.x and below. It is strongly recommended that all users and administrators upgrade to Bitcoin Core 25.0 or above within the next two weeks."

[Ava Chow post](https://x.com/achow101/status/1799972733092294814)
[Newsletter](https://bitcoinops.org/en/newsletters/2024/06/07/)

### Senator Cynthia Lummis announces BITCOIN Act

U.S. Senator Cynthia Lummis introduced the Boosting Innovation, Technology, and Competitiveness through Optimized Investment Nationwide (BITCOIN) Act' in the U.S. Senate.

The Act proposes establishing a decentralized network of secure Bitcoin storage facilities managed by the U.S. Department of Treasury, ensuring compliance with statutory requirements for high levels of physical and cybersecurity.
The program aims to acquire up to 1 million Bitcoins over five years, purchasing no more than 200,000 Bitcoins annually, similar in size and scope to U.S. gold reserves. The bill specifies a minimum holding period of 20 years, during which no Bitcoins held in the reserve may be sold or auctioned.

[full bill](https://www.lummis.senate.gov/wp-content/uploads/BITCOIN-Act-FINAL.pdf)

### Electrum Plugin for Joinstr Tutorial

In this tutorial I will share the steps to use electrum plugin for joinstr on Ubuntu. First step is to get the latest version of electrum. Run the below commands so that electrum can be used:

[tutorial](https://uncensoredtech.substack.com/p/tutorial-electrum-plugin-for-joinstr?ref=nobsbitcoin.com)
[article](https://www.nobsbitcoin.com/how-to-use-electrum-plugin-for-joinstr/)

### BDK v1.0.0-beta1 released

congrats to Evan!

[Case Documents (Dutch)](https://uitspraken.rechtspraak.nl/details?id=ECLI%3ANL%3ARBOBR%3A2024%3A2069&ref=nobsbitcoin.com)
[News Article](https://www.dlnews.com/articles/regulation/tornado-cash-dev-alexey-pertsev-guilty-of-money-laundering/?ref=nobsbitcoin.com)

### Proton Wallet by Proton Mail

Proton, the privacy-focused Swiss technology company, is launching Proton Wallet, an open-source, E2E-encrypted, and self-custodial Bitcoin wallet.

The product is currently available to Proton Visionary and Lifetime plan users. Other users can sign up to an early waitlist or receive an invite from an active Proton Wallet user.

[Website](https://proton.me/wallet)

[Announcement](https://proton.me/blog/proton-wallet-launch)
[github](https://github.com/protonwallet/)

### HRF Bitcoin Development Fund Grants 10 BTC to 13 Bitcoin Projects

Always great to see contributions to Bitcoin Development

"HRF’s latest batch of grants focus on education for people living under authoritarian regimes, privacy and Lightning development, decentralized communications, and providing nonprofits and human rights groups with easier onramps to financial freedom tools. Areas of focus include key countries and regions in Latin America, the Middle East, Asia, and Africa," announcement reads.
These are the projects receiving financial aid from the HRF:
* Robosats
* Bitshala Internship Program
* Building Bridges to Bitcoin (BBB)
* Flash
* Bitcoin Seoul
* Margot Paez
* Validating Lightning Signer
* OpenSats
* The Core
* Terry Yiu (nostr)
* Paulo Sacramento
* Blockchain Commons
* Summer of Bitcoin

[Announcement](https://hrf.org/hrf-bitcoin-development-fund-grants-1-billion-satoshis-to-14-projects-worldwide/)

### Utreexod Beta Is Now Available for General Public Testing

utreexod is a full node bitcoin implementation with support for utreexo accumulators. It enables immediate node bootstrap by having the UTXO state hardcoded into the codebase, uses a tiny amount of memory, and has a low disk i/o.

Key features:
- Implementation of efficient Utreexo accumulators with an improved deletionn algorithm from the Utreexo paper.
- Efficient P2P transaction relay with support for caching utreexo proofs for mempool transactions.
- Quick sync to the tip of the blockchain with AssumeUtreexo.
- Built in wallet support (with BDK wallet).
- Electrum personal server support for usage with other wallets.

utreexo proponent Calvin Kim attended Taipei Bitcoin Tech Summit 2023 with Taiwan BitDevs

[announcement](https://groups.google.com/g/bitcoindev/c/5GyV9af9lv4?ref=nobsbitcoin.com)
[github](https://github.com/utreexo/utreexod/releases?ref=nobsbitcoin.com)

### A Bitaxe Has Mined Block 853742

A solo Bitcoin miner with 3 TH/s has mined block 853742, overcoming odds of 1 in 1.2 million and earning 3.192 BTC (approximately $200,000).
1 in 3,500 year odds!

[nobsbitcoin article](https://www.nobsbitcoin.com/a-bitaxe-has-found-a-block/)

### OCEAN Pool Integrates BOLT12 Lightning Payouts

“Using BOLT12 also allows us to prove to the world that a payment was made, the size of the payment, the node to which it was paid, and that it was paid by us. This means we can continue to offer fully transparent and verifiable pooled mining while no longer being restricted by the base layer.”

“Pools traditionally have held miners’ bitcoins like a bank, while on-chain Bitcoin transactions get increasingly expensive as the demand for Bitcoin rises. For small miners, the problem is exacerbated since in some cases the cost of the transaction fee is higher than the reward that they earn. This is unsustainable because it creates lock-in to custodial pools. OCEAN helps overcome this risk using Lightning,” OCEAN co-founder Luke Dashjr said.

[Announcement](https://njump.me/nevent1qqs8sz359u7ysd8hw39v99hlxl5zs7mzsrrw5rwpsctm0ufart2g0ngpp4mhxue69uhkummn9ekx7mqppamhxue69uhkummnw3ezumt0d5q3gamnwvaz7tmwdaehgu3wdau8gu3wv3jhvq3qqtvl2em0llpnnllffhat8zltugwwz97x79gfmxfz4qk52n6zpk3qn2uecg)
[Press Release](https://newsdirect.com/news/ocean-innovates-bitcoin-miners-offered-first-ever-lightning-payouts-using-bolt12-946331135)
[Documentation](https://ocean.xyz/docs/lightning?ref=nobsbitcoin.com)]

### AntPool & Bitmain Acting as 'a Pool of Pools' - Report

"Looking at the merkle branches that mining pools send to miners as part of stratum jobs, it's clear that the BTCcom pool, Binance pool, Poolin, EMCD, Rawpool, and possibly Braiins* have exactly the same template and custom transaction prioritization as AntPool," analyst 0xB10C recently shared in a post.

note: pooled mining is surprisingly something that wasn't unexpected

[full post](https://nostr.com/note1qckcs4y67eyaawad96j7mxevucgygsfwxg42cvlrs22mxptrg05qtv0jz3)

### Scam Wallets - And how to spot them

Apple's App Store continues to publish fraudulent apps that mimic popular Bitcoin wallets, leading to the theft of money from unsuspecting users.

Attack Scenarios
* Malicious Clone
* Clipboard Hijacker
* Compromised PC
* Social Engineering
* Planted Wallet File

[nobsbitcoin article](https://www.nobsbitcoin.com/scam-bitcoin-wallets-apple/  )
[Electrum Tips](https://electrum.readthedocs.io/en/latest/malware.htm)

### Cheyenne crypto mine with Chinese origins ordered to divest

In October, The New York Times published an article detailing some of the security concerns around a Cheyenne-based crypto-mining operation with Chinese origins located within one mile of F.E. Warren Air Force Base.

On Monday, The White House released a statement ordering the sale of land to the company be reversed, citing a national security risk.

The purchasers acquired the land from Cheyenne LEADS in June 2022, and then made improvements to allow for specialized cryptocurrency mining operations. The land is in close proximity to F.E. Warren, a strategic missile base and home to Minuteman III intercontinental ballistic missiles.droid

[Link](https://www.wyomingnews.com/rocketminer/news/state/cheyenne-crypto-mine-with-chinese-origins-ordered-to-divest/article_2f8613b2-13b7-11ef-ab33-9ba1a7d84a96.html)

### Mutiny Wallet to shut down

Mutiny Wallet to shut down EOY

[blog post](https://blog.mutinywallet.com/mutiny-wallet-is-shutting-down/)
[nostr post](https://primal.net/e/note1mnyfl9hjck35mw67hd659j6a2gxltmyhzq684lm99xnf6wzyeunsh33fy8)

### Robosats Mobile App

The RoboSats Federation is a set of rules that allows multiple RoboSats instances to work together under a unified client app. This federated client app enables users to seamlessly interact with any coordinator, track the coordinator reputation, verify transparently devFund donations, and more.g the current cost-less-impairment accounting model for many entities.

[nobsbitcoin article](https://www.nobsbitcoin.com/robosats-v0-6-0-pre-release/)
[Announcement](https://learn.robosats.com/robosats/update/pre-release-robosats-decentralized/)

### BitVM 8-bit PC

"It's true, you can write bitcoin smart contracts in Assembly now instead of learning boolean logic circuits," wrote @Super Testnet.
Someone also wrote a multiplication function for this virtual CPU

[Link](https://supertestnet.github.io/8bit-cpu-for-bitvm/)
[BitVM Calculator](https://x.com/super_testnet/status/1732493052185391160?s=20)

### Strike opens up for Taiwan Users!

Strike offers global remittance through the Bitcoin Network, using Lightning.
Strike allows Taiwan users to register and supports VISA debit card deposits.  Balances are only held in USD
Strike currently has no banking relationships in Taiwan

[link](https://www.nobsbitcoin.com/strike-announced-buy-bitcoin-globally-feature/)


### Discussion on CVE-2023-50428 / Vulnerability in Bitcoin Core and Bitcoin Knots (Remains Open!)

Why this is a CVE - the software which creates these OP_IF/FALSE/PUSH transactions circumvents the existing filters, and there is no such mechanism is in place to to recognize these transactions as non-standard (there are no configuration options to address this).

datacarrier and datacarrier size parameters in bitcoin.conf does not include inscription transactions

Companies and individuals maintain their own versions of Bitcoin software and should be monitoring vulnerabilities across their stack. Ultimately everyone can decide whether or not a CVE applies to them, whether or not vulnerability should be classified as such is not the issue, it is a situation to address.

There is a patch available as commit #28408, the patch does not censor ordinals, it simply subjects an expanded set of transactions which inscribe data onto the blockchain to go through the same filters as before. The miners aligned with the patch are forgoing mining fees to run this filter.

Nodes which apply the patch have the drawbacks of fee-estimations being off and slower block validation times.

Note: demonstration available on how to apply the patch (homework!)

[CVE-2023-50428](https://nvd.nist.gov/vuln/detail/CVE-2023-50428)

[Pull Request/Patch](https://github.com/bitcoin/bitcoin/pull/28408/commits)

### New on Geyser: Bitcoin Explorama, BitFables, Smart Child Kenya & More

Discover and show support to some of the latest Bitcoin grassroots projects and initiatives launched via the Geyser crowdfunding platform.

[nobsbitcoin](https://www.nobsbitcoin.com/new-on-geyser-mid-may-24/)

### Nakamoto Institute update/facelift

The Satoshi Nakamoto Institute was founded in November 2013 to advance and preserve knowledge of Bitcoin’s history, economics, and technology.

SNI is a Texas nonprofit corporation exempt from tax under Section 501(c)(3) and classified as a public charity.

[link](https://nakamotoinstitute.org/)

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
