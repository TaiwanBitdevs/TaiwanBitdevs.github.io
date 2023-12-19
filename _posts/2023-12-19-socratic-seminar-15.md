---
layout: post
type: socratic
title: "Socratic Seminar 15: Merry Christmas~ You want the Moon? Just say the word and I'll throw a lasso around it and pull it down"
meetup: https://www.meetup.com/taiwan-bitdevs/events/297879249/
---

## Announcements
Welcome again Bitdevs Taiwan

Our fifteen Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Bitcoin v26.0

Bitcoin Core version 26.0 is now available for download. It includes experimental support for the version 2 transport protocol, support for taproot in miniscript, enhanced connection strategies against eclipse attacks and many other improvements and bug fixes.

BIP-324 will allow Bitcoin nodes to communicate with each other over encrypted connections, while AssumeUXTO option is set to allow instant UTXO set bootstrapping for Bitcoin nodes.

[link]([https://github.com/bitcoin/bitcoin/pull/28331])

[bip-324]([https://github.com/bitcoin/bips/blob/master/bip-0324.mediawiki])

[release notes]([https://bitcoincore.org/en/releases/26.0/])

[annoucement]([https://lists.linuxfoundation.org/pipermail/bitcoin-core-dev/2023-December/000131.html])

[article]([https://bitcoinmagazine.com/technical/the-big-deal-with-bitvm-arbitrary-computation-now-possible-on-bitcoin-without-a-fork])

### F2Pool reverses course on censoring OFAC transactions

Last month 0xB10C from miningpool.observer detected F2Pool censoring transactions.
After a series of posts, F2Pool's co-founder, Chun, admitted that F2Pool had been involved in transaction censoring and stated that the filtering patch has been disabled for now.

Note: this is censorship as OFAC lists have nothing to do with enforcing Bitcoin transactions, transactions are still free to relay on other nodes and mined elsewhere

[OxB10c Report]([https://b10c.me/observations/08-missing-sanctioned-transactions])

[F2Pool walkback]([https://nitter.net/satofishi/status/1727194584231662042])

### Ocean Mining Pool launch - filtering of transactions enforcing -datacarriersize

"Mummolin, Inc., announced today that it has raised $6.2million in seed funding, led by Jack Dorsey, Accomplice, Barefoot Bitcoin Fund, MoonKite, NewLayer Capital, the Bitcoin Opportunity Fund, and other strategic partners"
Restart of Eligius mining pool from Luke Dashjr, incorporating Stratum V2 and Lightning Payouts.

OCEAN uses Bitcoin Knots, which is another implementation of Bitcoin, it currently filters out transactions exceeding the "OP_RETURN limit" set in Bitcoin Core. Leading to inscriptions (transactions which bypass restriction by using OP_FALSE in tapscript) and Samourai Wallet tx0 for whirlpool (using >40 bytes of OP_RETURN) 

Note: this is filteriing as the criteria is set within Bitcoin itself, transactions are still free to relay on other nodes and mined elsewhere

[blog post]([https://b10c.me/observations/07-invalid-block-809478/])

[annnouncement]([https://www.prnewswire.com/news-releases/jack-dorsey-leads-seed-round-in-support-of-oceans-mission-to-decentralize-bitcoin-mining-globally---announces-launch-at-future-of-bitcoin-mining-conference-301999073.html])

[explanation on why these transactions should be filtered]([https://primal.net/e/note1xakyurzpw8hdgrv7sgf7adwldsywxfp5njn3k4jhcsck2afuryfshax4rl])

### Mempool Googles - New feature on mempool.space

Mempool Goggles is a new visualization tool that lets you explore mempool transactions through 25 different filters.
> "Click on the Mempool Goggles icon at the top left of the mempool block visualization to reveal the new filter menu. There are 25 different categories to explore, or mix-and-match to narrow down your focus even further."

[mempool page]([https://mempool.space])

### Ledger Live Tracks and Sends ALL User Information to Outsourced Data Harvesting Service

"Ledger Live is phoning out data on assets you hold in your hardware wallet the moment you access Ledger Live. It's also sending out tons of other info about your computer and device," wrote @rektbuildr
Channel splicing allows for flexible channel capacities without increasing on-chain footprint
Note that existing swap addresses should no longer be used!

[Full post]([https://crypto.bi/forum/threads/ledger-live-data-collection-is-more-than-a-little-concerning.5/?ref=nobsbitcoin.com])

### Zeus Wallet - remote control lightning node now also has option to run a node on the app

Zeus offers a node-on-the-phone (LND) which opens channels with Zeus, invoices generated from Zeus use HODL invoices to help with offline receiving
Zeus is a self-custodial mobile Lightning wallet with an embedded node, Lightning service provider, and self-custodial lightning addresses. It can also be used as mobile Bitcoin/Lightning node manager and wallet app for LND, CLN, and Eclair.


[blog post]([https://lightning.engineering/posts/2023-10-03-lnd-0.17-launch/])

### Elizabeth Warren Wants to Extend Bank Secrecy Act Regulations to Free & Open Source Software

The bill aims to extend Bank Secrecy Act (BSA) requirements including know-your-customer (KYC) rules to miners, validators, wallet providers and others.

The Digital Asset Anti-Money Laundering Act would: 

* Extend Bank Secrecy Act (BSA) responsibilities, including Know-Your-Customer requirements, to digital asset wallet providers, miners, validators, and other network participants that may act to validate, secure, or facilitate digital asset transactions.
* Address a major gap with respect to “unhosted” digital wallets – which allow individuals to bypass AML and sanctions checks – by directing FinCEN to finalize and implement its December 2020 proposed rule, which would require banks and money service businesses (MSBs) to verify customer and counterparty identities, keep records, and file reports in relation to certain digital asset transactions involving unhosted wallets or wallets hosted in non-BSA compliant jurisdictions.
* Direct FinCEN to issue guidance to financial institutions on mitigating the risks of handling, using, or transacting with digital assets that have been anonymized using digital asset mixers and other anonymity-enhancing technologies. 
* Strengthen enforcement of BSA compliance by directing the Treasury Department to establish an AML/CFT compliance examination and review process for MSBs and other digital asset entities with BSA obligations and directing the Securities and Exchange Commission and Commodity Futures Trading Commission to establish AML/CFT compliance examination and review processes for the entities they regulate. 
* Extend BSA rules regarding reporting of foreign bank accounts to include digital assets by requiring United States persons engaged in a transaction with a value greater than $10,000 in digital assets through one or more offshore accounts to file a Report of Foreign Bank and Financial Accounts (FBAR) with the Internal Revenue Service. 
* Mitigate the illicit finance risks of digital asset ATMs by directing FinCEN to ensure that digital asset ATM owners and administrators regularly submit and update the physical addresses of the kiosks they own or operate and verify customer and counterparty identity.

Note: Often Republic of China/Taiwan policy follows suit with the US, so best to keep alert on what is happening with the KYC/AML side -- however generally everyone is already KYC'ed

[nobsbitcoin link]([https://www.nobsbitcoin.com/elizabeth-warren-wants-bank-secrecy/])

### Blackrock iShares Bitcoin Trust submits S-1 Amendment

Investment manager Blackrock had on Monday, December 18, 2023 submitted an amendment to the form S-1 for its iShares Bitcoin Trust as part of its spot Bitcoin ETF filing with the U.S. Securities and Exchange Commission (SEC).

[link to amendment] ([https://www.sec.gov/Archives/edgar/data/1980994/000143774923034772/bit20231215_s1a.htm])

### Primal nostr client offers Lightning Wallet with Apple Pay Top ups (even for Taiwan!)

Primal is a nostr client that works on Web, iOS, Android.  Great explore feature.  Offers a Zap-enabled lightning wallet which can hold up to 1.5million satoshis with a $15US/day buy limit.
Apple Pay charges an additional fee to buy Bitcoin in this way

Note: Ln.bitdevs.tw now supports zaps!

[app store]([https://apps.apple.com/us/app/primal/id1673134518])

### FASB Officially Adopts Fair Value Accounting Rules for Bitcoin Starting December 2024

"FASB has officially adopted Fair Value Accounting for Bitcoin for fiscal years beginning after December 15, 2024. This upgrade to accounting standards will facilitate the adoption of BTC as a treasury reserve asset by corporations worldwide," said MicroStrategy's Chairman Michael Saylor on X.
Stakeholders stated that the current accounting—except as provided in generally accepted accounting principles (GAAP) for certain specialized industries—for holdings of crypto assets as indefinite-lived intangible assets, which is a cost-less-impairment accounting model, does not provide investors, lenders, creditors, and other allocators of capital (collectively, “investors”) with decision-useful information.

Specifically, accounting for only the decreases, but not the increases, in the value of crypto assets in the financial statements until they are sold does not provide relevant information that reflects (1) the underlying economics of those assets and (2) an entity’s financial position. Investors also requested additional disclosures about the types of crypto assets held by entities and the changes in those holdings.

In addition to better reflecting the economics of crypto assets, measuring those assets at fair value will likely reduce cost and complexity associated with applying the current cost-less-impairment accounting model for many entities.
  
[Press Release]([https://www.fasb.org/page/getarticle?uid=fasb_Media_Advisory_12-13-23])


### Diamond Hands announces partnership with Boltz to provide lightning liquidity swap services for Bitcoin and Liquid

Diamond Hands released a new and improved DH Swap service for better Lightning liquidity management in partnership with Boltz.

Note: Liquid is a great solution during high fee environments

[article]([https://www.nobsbitcoin.com/diamond-hands-partners-with-boltz-to-improve-dh-swap-service/])

### Strike opens up for Taiwan Users!

Strike offers global remittance through the Bitcoin Network, using Lightning.
Strike allows Taiwan users to register and supports VISA debit card deposits.  Balances are only held in USD
Strike currently has no banking relationships in Taiwan

[link]([https://www.nobsbitcoin.com/strike-announced-buy-bitcoin-globally-feature/])

### BTCPayServer - LNBank Plugin Exploit

LNbank is a plugin for BTCPay Server to use the internal Lightning node in custodial mode: It allows server admins to open up the Lightning node and give users access via custodial layer 3 wallets. All users of BTCPay Server's LNbank plugin are urged to upgrade to to v1.8.9 as soon as possible.

Note: This is a form of hot wallet risk. Software running on lightning nodes often have full control of the node in question which means any vulnerability found in that software can be used to steal balances.  Recommend to be careful of what apps to run, and secure authentication token files properly (LND uses special cookies called macaroons)  

[Stacker News]([https://stacker.news/items/347361?ref=nobsbitcoin.com])

### Discussion on CVE-2023-50428 / Vulnerability in Bitcoin Core and Bitcoin Knots

Why this is a CVE - the software which creates these OP_IF/FALSE/PUSH transactions circumvents the existing filters, and there is no such mechanism is in place to to recognize these transactions as non-standard (there are no configuration options to address this).

datacarrier and datacarrier size parameters in bitcoin.conf does not include inscription transactions

Companies and individuals maintain their own versions of Bitcoin software and should be monitoring vulnerabilities across their stack. Ultimately everyone can decide whether or not a CVE applies to them, whether or not vulnerability should be classified as such is not the issue, it is a situation to address.

There is a patch available as commit #28408, the patch does not censor ordinals, it simply subjects an expanded set of transactions which inscribe data onto the blockchain to go through the same filters as before. The miners aligned with the patch are forgoing mining fees to run this filter.

Nodes which apply the patch have the drawbacks of fee-estimations being off and slower block validation times.

Note: demonstration available on how to apply the patch (homework!)

[CVE-2023-50428]([https://nvd.nist.gov/vuln/detail/CVE-2023-50428])
[Pull Request/Patch]([https://github.com/bitcoin/bitcoin/pull/28408/commits])

### Lightning HTLCs, in detail!

A very nice explanation on the HTLCs that traverse the lightning network
This post will walk through the different operations of a Lightning channel by following a long-running example with plenty of explanatory diagrams. First, we explore how Hash Time Locked Contracts (HTLCs) are added to a channel and how channel peers commit to a new state including these HTLCs. Next, we discuss how a channel’s normal flow is re-established after a disconnection. And finally, we finish with how a cooperative channel closure happens. These topics are all covered in Bolt 2 for those interested in learning more. Note that some of these operations will change with Taproot channels, which will be detailed in a future post.

[link](https://lightning.engineering/posts/2023-06-28-channel-normal-op/?ref=nobsbitcoin.com)

### Nostr, zaps and stuff (always)

Taiwan BitDevs would like to explore Nostr with the audience by generating an npub with the audience present to follow along.
Nostr stands for "notes and other stuff transmitted over relays" it is a protocol designed around censorship resistance which can be used for social media. Nostr is a lot of fun and a great way to use Lightning Network (NIP-57 / zaps / LNURL)

#### NIP update - nostr marketplace (NIP-15)
Theres an LNBits extension that allows you to list and shop for goods using nostr relays and get paid through Bitcoin/Lightning

[tutorial](https://github.com/lnbits/lnbits/wiki/LNbits-Extensions)
[nip-15]([https://github.com/nostr-protocol/nips/blob/master/15.md])


[github link](https://github.com/nostr-protocol/nostr)

[web client](https://snort.social)

[Amethyst android](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst&hl=en&gl=US)

[Damus iOS](https://apps.apple.com/ca/app/damus/id1628663131)
