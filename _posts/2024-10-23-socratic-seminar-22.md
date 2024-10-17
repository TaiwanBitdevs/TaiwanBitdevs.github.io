---
layout: post
type: socratic
title: "Socratic Seminar 22: Trade-offs and Catch 22s"
meetup: https://www.meetup.com/taiwan-bitdevs/events/304061485

## Announcements

Our 22nd Socratic Seminar will be co-hosted with TempoX! Thank you to TempoX for offering the space, food, and their willingness to promote Bitcoin development and awareness. Hopefully, we will be able to showcase the importance of Bitcoin, and the problems it solves, to a wider audience.

Location : [Tempo House](https://maps.app.goo.gl/yXMwGAFzV3cUsT1j9)

We will start the Socratic Seminar with general introductions and follow with discussion on the latest bitcoin developments and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Bitcoin Mempool Upgrades

Recently, there has been some really cool mempool P2P upgrades to Bitcoin that are worth talking about.
* Package relay for 1P1C (one parent one child).
* TRUC (topologically restricted until confirmation) transaction relay.
* Package RBF.
* Sibling eviction.
* A standard P2A (pay-to-anchor) output script type.

> Gregory Sanders has written a [guide](https://bitcoinops.org/en/bitcoin-core-28-wallet-integration-guide/) for Optech aimed at developers of wallets and other software that uses Bitcoin Core to create or broadcast transactions. The guide walks through the use of several of the features and describes how the features can be useful for multiple protocols, including simple payments and RBF fee bumping, LN commitments and [HTLCs](https://bitcoinops.org/en/topics/htlc/), [Ark](https://bitcoinops.org/en/topics/ark/), and [LN splicing](https://bitcoinops.org/en/topics/splicing/).

[Optech Newsletter](https://bitcoinops.org/en/newsletters/2024/10/11/#guide-for-wallets-employing-bitcoin-core-28-0)

### Bitcoin Core v28.0: Testnet4, Full RBF by Default & More

* Bitcoin Core v28 supports testnet4 and introduces a variety of P2P/mempool policy changes, including opportunistic 1-parent-1-child (1p1c) package relay, default relay of opt-in TRUC and pay-to-anchor transactions, limited package RBF relay, and full-RBF is now on by default.
* It also adds default parameters for assumeUTXO, enabling the loadtxoutset RPC to use a UTXO set downloaded outside the Bitcoin network (etc. via torrents).
* The update also packages many other new features, updated RPCs, fixes, stability and performance improvements, as well as updated translations.
* AssumeUTXO available on mainnet. AssumeUTXO mainnet parameters have been added for height 840,000. The loadtxoutset RPC can now be used on mainnet with the matching UTXO set from that height.
* New Windows Data Directory. The default Windows data directory has been moved to C:\Users\Username\AppData\Local\Bitcoin. If old directory is present, the client will continue to use it for backwards compatibility.
* JSON-RPC 2.0 Support. The JSON-RPC server now recognizes JSON-RPC 2.0 requests and responds with strict adherence to the specification.
    "JSON-RPC clients may need to be updated to be compatible with the JSON-RPC server. Please open an issue on GitHub if any compatibility issues are found."
* libbitcoinconsensus Removal. The libbitcoin-consensus library was deprecated in 27.0 and is now completely removed.
* Easier to migrate legacy wallets to descriptor wallet format.
    The "Migrate Wallet" menu allows users to migrate any legacy wallet in their wallet directory, regardless of the wallets loaded.
* A new createwalletdescriptor RPC allows users to add new automatically generated descriptors to their wallet. This can be used to upgrade wallets created prior to the introduction of a new standard descriptor, such as taproot.
* Blockstorage improvements. Block files are now XOR'd by default with a key stored in the blocksdir.
* Maximum mempool size along with the mempool usage are now displayed in the "Information" window.

CVE-2023-50428 remains at large

[release](https://bitcoincore.org/en/2024/10/02/release-28.0/)


### OCEAN Unveils Decentralized Alternative Templates for Universal Mining (DATUM)

Similar to Stratum V2, DATUM is designed to decentralize block construction by empowering miners to create their own block templates via their own Bitcoin node. Users can mine on pools that offer Datum support or solo mine without needing a third party to set up a server for them.

* The launch of datum is motivated by concerns of large mining pools controlling over 50% of Bitcoin’s hash rate, thus increasing the risk of miner centralization and potential transaction censorship. DATUM aims to decentralize block construction, prevent 51% attacks and keep Bitcoin network free and open.

[Press Release](https://newsdirect.com/news/ocean-restoring-bitcoin-mining-decentralization-177177279)

### Bitcoin Core Discloses Three Vulnerabilities Affecting Versions Before v25.0

Disclosed vulnerabilities include a blocktxn remote node crash (CVE-2024-35202), an issue with mutated blocks hindering block propagation, and a node communication issue due to inv-to-send sets growing too large.

Disclosed vulnerabilities include:

* CVE-2024-35202. This is a high severity issue that allows attackers to crash Bitcoin Core nodes remotely by triggering an assertion in the blocktxn message handling logic. The vulnerability was discovered by Niklas Gögge and fixed in Bitcoin Core v25.0.
* Hindered block propagation due to mutated blocks. This is a medium severity issue that allows a peer to clear the block download state of other peers by sending unrequested, mutated blocks. It was fixed in #27608 by ensuring that a peer can only affect its own block download state, not the download states of other peers.
* DoS due to inv-to-send sets growing too large. It's a medium severity issue where excessively large m_tx_inventory_to_send sets could disrupt node communication by slowing inventory message construction.

[Announcement](https://groups.google.com/g/bitcoindev/c/WeSDeV8YOSA)

### Bitmain Launches the ANTMINER S21+ Series

At the Bitcoin Amsterdam 2024 conference, Bitcoin miner manufacturer Bitmain announced two new machines: the Antminer S21+ Hyd and the Antminer S21+.

* The Antminer S21+ Hyd. is said to deliver a hashrate of 319 TH/s and an efficiency of 15 J/TH.
* The S21+ model promises 216 TH/s with a power efficiency of 16.5 J/TH.
* Shipping of the new products is expected to begin in Q1/Q2 of 2025.

[Press Release](https://www.bitmain.com/news-detail/bitmain-launches-the-antminer-s21-series-358)

### Italy Plans to Raise Bitcoin Capital Gains Tax from 26% to 42%

Italy intends to increase the capital gains tax on Bitcoin from 26% to 42% as part of a strategy to fund costly election commitments while reducing the budget deficit.

* On Wednesday, Italy unveiled its draft budgetary plan (DBP), which outlined new revenue-raising strategies.
* The proposal to hike bitcoin taxes accompanies the country's aim to generate 0.2% of its gross domestic product (GDP), translating to approximately 4 billion euros ($4.35 billion) by 2025.
* The plan also includes raising funds through new tax regulations targeting banks, insurance products, gaming business licenses, and adjustments to the web tax.

[Reuters](https://www.reuters.com/markets/europe/italy-stiffens-terms-digital-services-tax-2025-budget-2024-10-16/#:~:text=Italy%20will%20also%20raise%20a,from%2026%25%2C%20Leo%20added)

### Electrum Plugin for Joinstr Tutorial

In this tutorial I will share the steps to use electrum plugin for joinstr on Ubuntu. First step is to get the latest version of electrum. Run the below commands so that electrum can be used:

[tutorial](https://uncensoredtech.substack.com/p/tutorial-electrum-plugin-for-joinstr?ref=nobsbitcoin.com)
[article](https://www.nobsbitcoin.com/how-to-use-electrum-plugin-for-joinstr/)

### BDK `v1.0.0-beta.5` Released

Here is the summary of the latest and previous beta releases.

* `beta.1`: This release includes the first beta version of `bdk_wallet` with a stable 1.0.0 API. The changes in this version include reworked wallet persistence, changeset, and construction, optional user provided RNG, custom tx sorting, and use of merkle proofs in bdk_electrum.
* `beta.2`: The primary user facing changes are re-enabling single descriptor wallets and renaming LoadParams methods to be more explict. Wallet persistence was also simplified and blockchain clients no longer depend on bdk_chain.
* `beta.{3|4}`: Fixed transaction creation to not skip unused addresses, added function for sorting wallet transactions and option to change default BNB fallback coin selection. We moved the bdk_hwi crate functionality to the rust-hwi repo.
* `beta.5`: This release changes bdk_wallet transaction creation to enable RBF by default, it also updates the bdk_esplora client to retry server requests that fail due to rate limiting. The bdk_electrum crate now also offers a use-openssl feature.

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

### RFK Speech at Bicoin Conference 2024

Robert F. Kennedy Jr. delivers a groundbreaking speech Bitcoin 2024, outlining his vision for integrating Bitcoin into America's economic and national security strategies. As an independent presidential candidate, RFK Jr. proposes bold initiatives including making the US government a major Bitcoin holder, eliminating taxes on Bitcoin transactions, and using Bitcoin mining to incentivize green energy production.

[youtube](https://www.youtube.com/watch?v=ssYCRVpzcxc)
[中文翻譯](https://btczh.tw/posts/a8961609)

### Bitcoin Optech #306: Disclosure of Vulnerabilities Affecting Older Versions of Bitcoin Core

This issue announces an upcoming disclosure of Bitcoin Core vulnerabilities, and describes: a draft BIP for testnet4, functional encryption covenants, proposed updates to 64-bit arithmetic in Bitcoin Script, looks at OP_CAT script to validate proof of work, as well as proposed update to BIP21.

"Several members of the Bitcoin Core project discussed on IRC a proposed policy for disclosing vulnerabilities that affected older versions of Bitcoin Core..."
"After this policy has a chance to be further discussed, it is the intention of the project to begin disclosing vulnerabilities affecting Bitcoin Core 24.x and below. It is strongly recommended that all users and administrators upgrade to Bitcoin Core 25.0 or above within the next two weeks."

[Ava Chow post](https://x.com/achow101/status/1799972733092294814)
[Newsletter](https://bitcoinops.org/en/newsletters/2024/06/07/)


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
