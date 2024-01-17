---
layout: post
type: socratic
title: "Socratic Seminar 16: Happy New Year! Post-Election Discussion"
meetup: https://www.meetup.com/taiwan-bitdevs/events/297879249/
---

## Announcements
Welcome again Bitdevs Taiwan

Our sixteenth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Bitcoin ETF launched January 10th 2024

US regulators for the first time approved exchange-traded funds that invest directly in Bitcoin, a move heralded as a landmark event for the roughly $1.7 trillion digital-asset sector that will broaden access to the largest cryptocurrency on Wall Street and beyond.

[SEC Announcement](https://www.sec.gov/news/statement/gensler-statement-spot-bitcoin-011023)
[$10 Billion in 3 days 🤯](https://x.com/JSeyff/status/1747366266166206505?s=20)

### Blackrock ETF Bitcoin Address found?

It didn't take long. Just two days after BlackRock and other bitcoin spot ETFs began trading, we can reveal at least one on-chain address that belongs to BlackRock.

The address has 227.90249795 BTC, funded on January 5th, corresponding fully to BlackRock's own prospectus that they bought that many BTC on that day.

[article](https://www.trustnodes.com/2024/01/14/revealed-the-blackrock-bitcoin-address-is-identified)

### Aqua Wallet - Lightning - Liquid Wallet

Aqua Wallet, developed by Jan3, is a non-custodial mobile Bitcoin, Lightning, Liquid and Tether USDT (on Liquid, Ethereum, and Tron) wallet. Available on Android (APK only for now) and iOS.

[Website](https://aquawallet.io/)

[Announcement](https://twitter.com/JAN3com/status/1742758563271881132)
[Blogpost](https://jan3.com/blog/surf-the-bitcoin-revolution-with-aqua/)

### Mempool filter PR (PR 28404) closed by Achow

Pull request for expanding mempool filters have been closed due to "controversy" 

For those interested in running a node with updated filters, either build Bitcoin Core directly, run Knots, or use another patched implementation
Filters will not cause forks and blocks with inscriptions are still validated correctly

note: Taiwan BitDevs also has a patched version (compiled by LeTenken) and Umbrel-compatible Docker Image

[Bitcoin Knots](https://github.com/bitcoinknots/bitcoin)

[Start9 Docker Image](https://x.com/GrassFedBitcoin/status/1746992663591792968?s=20)


### Mempool Googles - New feature on mempool.space

Mempool Goggles is a new visualization tool that lets you explore mempool transactions through 25 different filters.
> "Click on the Mempool Goggles icon at the top left of the mempool block visualization to reveal the new filter menu. There are 25 different categories to explore, or mix-and-match to narrow down your focus even further."

[mempool page](https://mempool.space)

### Stripe De-platforming Miners

Stripe is a digital payments provider.

Bitcoin consulting service and hardware store Bitsaga.be has been deplatformed by payment processor Stripe for offering Bitcoin mining equipment on its site.

"We understand that your business may be legal, but for now, due to various reasons, including requirements that apply to Stripe as a payment processor, requirements from our financial partners, and the potential risk exposure to Stripe, we're currently not able to work with certain industries."

[Full post](https://nitter.net/bitsaga_org/status/1746911320824262781?ref=nobsbitcoin.com)

### Vaneck Bitcoin ETF (BITB)  

Bitwise will be donating 10% of profits from its bitcoin ETF to OpenSats, the Human Rights Foundation, and Brink - all split evenly - for the next 10 years.

"We’ve selected @BitcoinBrink, @OpenSats, and @HRF—fantastic non-profit organizations with established track records—to receive and allocate BITB’s recurring donations. The donations have no strings attached and will be made annually for at least the next 10 years."
"Bitwise first filed for a spot bitcoin ETF 5 years ago. Today is a milestone we do not take lightly. Our vision and hope for BITB is to be the ETF this space deserves. If you support this recurring donation to bitcoin open-source development, please help spread the word about BITB!"

[Vaneck Announcement](https://www.vaneck.com/us/en/blogs/digital-assets/we-celebrate-bitcoin-builders-not-tourists/?ref=nobsbitcoin.com)
[Article](https://nitter.net/BitwiseInvest/status/1745205436708421691?ref=nobsbitcoin.com)

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

[nobsbitcoin link](https://www.nobsbitcoin.com/elizabeth-warren-wants-bank-secrecy/)

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

### Primal nostr client offers Lightning Wallet with Apple Pay Top ups (even for Taiwan!)

Primal is a nostr client that works on Web, iOS, Android.  Great explore feature.  Offers a Zap-enabled lightning wallet which can hold up to 1.5million satoshis with a $15US/day buy limit.
Apple Pay charges an additional fee to buy Bitcoin in this way

Note: Ln.bitdevs.tw now supports zaps!

[app store](https://apps.apple.com/us/app/primal/id1673134518)

### Robosats Federation

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

### BTCPayServer - LNBank Plugin Exploit (Update: LNBank is being phased out)

LNbank is a plugin for BTCPay Server to use the internal Lightning node in custodial mode: It allows server admins to open up the Lightning node and give users access via custodial layer 3 wallets. All users of BTCPay Server's LNbank plugin are urged to upgrade to to v1.8.9 as soon as possible.

Note: This is a form of hot wallet risk. Software running on lightning nodes often have full control of the node in question which means any vulnerability found in that software can be used to steal balances.  Recommend to be careful of what apps to run, and secure authentication token files properly (LND uses special cookies called macaroons)  

[Stacker News](https://stacker.news/items/347361?ref=nobsbitcoin.com)

### Discussion on CVE-2023-50428 / Vulnerability in Bitcoin Core and Bitcoin Knots (Remains Open!)

Why this is a CVE - the software which creates these OP_IF/FALSE/PUSH transactions circumvents the existing filters, and there is no such mechanism is in place to to recognize these transactions as non-standard (there are no configuration options to address this).

datacarrier and datacarrier size parameters in bitcoin.conf does not include inscription transactions

Companies and individuals maintain their own versions of Bitcoin software and should be monitoring vulnerabilities across their stack. Ultimately everyone can decide whether or not a CVE applies to them, whether or not vulnerability should be classified as such is not the issue, it is a situation to address.

There is a patch available as commit #28408, the patch does not censor ordinals, it simply subjects an expanded set of transactions which inscribe data onto the blockchain to go through the same filters as before. The miners aligned with the patch are forgoing mining fees to run this filter.

Nodes which apply the patch have the drawbacks of fee-estimations being off and slower block validation times.

Note: demonstration available on how to apply the patch (homework!)

[CVE-2023-50428](https://nvd.nist.gov/vuln/detail/CVE-2023-50428)

[Pull Request/Patch](https://github.com/bitcoin/bitcoin/pull/28408/commits)

### Sending 26.9 BTC down the Bitcoin Wishing Well

1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa is known to be the Address where the Genesis Block blockreward went. Technically there is no block reward for the Genesis Block as it cannot be spent -- because it has no utxo to reference.  Users have been sending Bitcoin to this address for a long time, for what reason one can only speculate 😂

[tx id](https://mempool.space/tx/d7db4f96a4059c8906b953677ce533493d7b9da0f854a21b99f5772910dd0a31)

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
[nip-15](https://github.com/nostr-protocol/nips/blob/master/15.md)


[github link](https://github.com/nostr-protocol/nostr)

[web client](https://snort.social)

[Amethyst android](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst&hl=en&gl=US)

[Damus iOS](https://apps.apple.com/ca/app/damus/id1628663131)
