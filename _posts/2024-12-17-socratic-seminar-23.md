---
layout: post
type: socratic
title: "Socratic Seminar 23: 2024 Year-end Review"
meetup: https://www.meetup.com/taiwan-bitdevs/events/304855459
---

## Announcements

Our 23rd Socratic Seminar event will be held at 9 LiShui St. Da’An Dist. Taipei.

For the last event of 2024, a year-end review of all technical discussions will also be had

We will start the Socratic Seminar with general introductions and follow with discussion on the latest bitcoin developments and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Czech Republic Eliminates Bitcoin Capital Gains Tax for Long-term Holdings

The Czech Republic has enacted a law that exempts Bitcoin holdings held for more than three years from capital gains tax. This legislation received unanimous approval from the nation's parliament on December 6 and is scheduled to take effect on January 1, 2025.

[article](https://www.theblock.co/post/329788/czech-republic-scraps-capital-gains-tax-on-crypto-held-for-over-3-years)

### WabiSabi Vulnerability Allows Malicious Coordinators to Deanonymize Coinjoin Users

A vulnerability in the WabiSabi protocol allows malicious coordinators to deanonymize users' coins and link inputs to outputs, compromising the privacy of coinjoin participants. Users are urged to update their instances immediately.

The affected versions of the WabiSabi protocol have a vulnerability due to inadequate client-side validation of credential issuers. It allows malicious coordinators to use multiple issuers to differentiate inputs from outputs, trace input ownership, and break the anonymity set of Bitcoin's coinjoin process, compromising user privacy.

[disclosure](https://github.com/GingerPrivacy/GingerWallet/discussions/116)
[artcile](https://www.therage.co/vulnerability-wabisabi-coinjoin/)

### Vulnerability allowing theft from LN channels with miner assistance

David Harding announced to Delving Bitcoin a vulnerability he had responsibly disclosed earlier in the year. Old versions of Eclair, LDK, and LND with default settings allowed the party who opened a channel to steal up to 98% of channel value. Core Lightning remains affected if the non-default --ignore-fee-limits configuration option is used; this option’s documentation already indicates it is dangerous.

The announcement also described two less severe variants of the vulnerability. All LN implementations listed above attempt to mitigate those additional risks, but a complete solution awaits additional work on package relay, channel upgrades, and related projects.

The vulnerability takes advantage of the LN protocol allowing an old channel state to commit to more onchain fees than the fee-paying party controls in the latest state. For example, in a state where Mallory controls 99% of the channel balance, she dedicates 98% of the overall balance to endogenous fees. She then creates a new state that pays only minimal fees and forwards 99% of the channel balance to Bob’s side. By personally mining the old state that pays 98% to fees, she can capture those fees for herself—reducing the maximum value Bob can receive onchain from his expected 99% to an actual 2%. Mallory can use this method to simultaneously steal from about 3,000 channels per block (with each channel potentially controlled by a different victim), allowing theft of about $3 million USD per block if the average channel value is about $1,000 USD.

note: from version Eclair v0.10.0 (29 Feb 2024), LDK 0.0.123 (8 May 2024), LND 0.18.3-beta 1 (11 Sept 2024)

[disclosure](https://delvingbitcoin.org/t/disclosure-irrevocable-fees-stealing-from-ln-using-revoked-commitment-transactions/1314)


### Eclair v0.11.0: Official Bolt 12 Support, Splicing, Liquidity Ads & On-The-Fly Funding Prototypes

Eclair (French for Lightning) is a Scala implementation of the Lightning Network developed by ACINQ.

* Official support for Bolt 12. This release contains full support for Bolt 12 payments.
* Splicing prototype for private channels. Improved ACINQ implementation of splicing by relying on the official quiescence feature and adding RBF support.
* Liquidity ads prototype. Liquidity ads empower nodes to sell their liquidity in a trustless and decentralized way. Each node advertises the rates at which they are willing to sell their liquidity, allowing buyers to connect with sellers offering favorable rates.
* Updated minimal version of Bitcoin Core to v27.2. The latest version of Eclair requires Bitcoin Core 27.2, which introduces CoinGrinder, a new coin selection algorithm that reduces on-chain transaction costs when feerates are high. Newer Bitcoin Core versions may be used but haven't been thoroughly tested.

[announcement](https://xcancel.com/acinq_co/status/1864242997396644034)

### Bitcoin ATM Operator Byte Federal Reports Data Breach Affecting 58,000 Users
U.S.-based Bitcoin ATM operator Byte Federal has reported a data breach that may have compromised the personal information of approximately 58,000 customers.

"Customer personal information that was subject to the attempt at unauthorized access includes name, birthdate, address, phone number, email address, government-issued ID, social security number, transaction activity, and photographs of users," said the company.

[breach announcement](https://www.bytefederal.com/files/Consumer%20Breach%20Notification%20Letter.pdf)

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

### Ashigaru v1.1.0: Removed DNS Dependencies & UI Improvements

Ashigaru is a self-custodial, open-source and secure mobile Bitcoin wallet that is private by design. It has been forked and build upon Samourai Wallet Source Code. Available on Android.

"The Ashigaru Open Source Project is pleased to announce the update of Ashigaru mobile to v1.1.0. Thank you to those who have used the wallet and provided valuable feedback, some of which has been addressed within this update," announced the project.
This release implements automatic updates of Tor onion services, removing all dependencies and reliance on DNS from the app, overhauls Settings screen user interface, introduces new transaction alerts, and more

note: although ashigaru is open source from the remains of the last version of Samourai wallet, ashigaru uses a pre-compilied bitcoinj library

[blogpost](https://ashigaru.rs/news/mobile-wallet-v1-1-0/)
[repo](http://ashicodepbnpvslzsl2bz7l2pwrjvajgumgac423pp3y2deprbnzz7id.onion/Ashigaru/Ashigaru-Mobile/releases/tag/v1.1.0)

### Samourai Wallet & Tornado Cash Prosecutor Damian Williams to Step Down in December

Damian Williams, the United States Attorney for the Southern District of New York and the district's chief federal law enforcement officer, announced his resignation. He will step down from his position effective at 11:59 p.m. on December 13, 2024.

Damian Williams assumed office on October 10, 2021, appointed by President Joe Biden. During his three-year tenure, Williams has overseen many high-profile cases, including the convictions of FTX's Sam Bankman-Fried and Jeffrey Epstein's accomplice Ghislaine Maxwell, the prosecutions of New York City Mayor Eric Adams and rap artist Sean "Diddy" Combs, as well as the developers of Tornado Cash and Samourai Wallet privacy tools.
Edward Y. Kim, the current Deputy United States Attorney, will take over as Acting United States Attorney when he departs. Additionally, President-elect Trump has announced his intention to nominate Jay Clayton, former head of the Securities and Exchange Commission, to lead the office.

[press release](https://www.justice.gov/usao-sdny/pr/us-attorney-damian-williams-announces-anticipated-resignation-southern-district-new)

### Bitmain Launches the ANTMINER S21+ Series

At the Bitcoin Amsterdam 2024 conference, Bitcoin miner manufacturer Bitmain announced two new machines: the Antminer S21+ Hyd and the Antminer S21+.

* The Antminer S21+ Hyd. is said to deliver a hashrate of 319 TH/s and an efficiency of 15 J/TH.
* The S21+ model promises 216 TH/s with a power efficiency of 16.5 J/TH.
* Shipping of the new products is expected to begin in Q1/Q2 of 2025.

[Press Release](https://www.bitmain.com/news-detail/bitmain-launches-the-antminer-s21-series-358)

### RoboSats v0.7.3-alpha: LNP2PBot Orders & Nostr Order Books on Android

RoboSats is a simple and private way to exchange bitcoin. It simplifies the peer-to-peer user experience and uses lightning hold invoices to minimize custody and trust requirements while helping users stick to best privacy practices. Available on the web, Android, Windows, MacOS, and Linux.

RoboSats v0.7.3 is now available! This release introduces the ability to fetch orders from the LNP2PBot platform when the user enables Nostr orders in settings, thanks to shared Nostr order books.
"Robosats and LNP2PBot are two separate platforms for P2P Bitcoin exchange. Both are now publishing their public orders to Nostr, so we can now display their orders in our client. This brings a lot of benefits. One of the most direct is that Robosats users will now have more info when comparing premiums, which will reduce the arbitrage between platforms and increase the general liquidity," said KoalaSat.
Additionally, Android app users now have the option to enable Nostr orders in settings, along with a few other fixes.

[announcement](https://njump.me/nevent1qqsfd8gf7c7mnta8s7pdre8ar3rmkdj7qgz3l7suetszmheq7l2cwtcpzemhxue69uhhyetvv9ujumn0wd68ytnzv9hxgqgdwaehxw309ahx7uewd3hkcq3qv3tgrwwsv7c6xckyhm5dmluc05jxd4yeqhpxew87chn0kua0tjzqeqvasa)
[repo](https://github.com/RoboSats/robosats/releases/tag/v0.7.3-alpha)

### Electrum Plugin for Joinstr Tutorial

In this tutorial I will share the steps to use electrum plugin for joinstr on Ubuntu. First step is to get the latest version of electrum. Run the below commands so that electrum can be used:

[tutorial](https://uncensoredtech.substack.com/p/tutorial-electrum-plugin-for-joinstr?ref=nobsbitcoin.com)
[article](https://www.nobsbitcoin.com/how-to-use-electrum-plugin-for-joinstr/)

## Discussion of softfork proposals

(placeholder for discussion over drama regarding opcodes)

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


### Strike opens up for Taiwan Users!

Strike offers global remittance through the Bitcoin Network, using Lightning.
Strike allows Taiwan users to register and supports VISA debit card deposits.  Balances are only held in USD
Strike currently has no banking relationships in Taiwan

[link](https://www.nobsbitcoin.com/strike-announced-buy-bitcoin-globally-feature/)


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
