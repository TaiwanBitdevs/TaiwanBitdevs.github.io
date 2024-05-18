---
layout: post
type: socratic
title: "Socratic Seminar 19: everybody wanna be demon 'til they get chipped by a throwaway"
meetup: https://www.meetup.com/taiwan-bitdevs/events/299203425/
---

## Announcements
Welcome again Bitdevs Taiwan

Our nineteenth Socratic Seminar event will be held at our typical location 9 LiShui St. Da'An Dist. Taipei.

We will start the socratic seminar discussion with general introductions and follow with discussion on the latest bitcoin developents and news.

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Samourai Wallet Founders Arrested & Charged with Money Laundering, Unlicensed Money Transmitting Offenses

The charges include conspiracy to commit money laundering and conspiracy to run an unlicensed money transmitting business. These charges could lead to a maximum sentence of 20 years and five years, respectively.

Samourai’s web servers and domain (https://samourai.io/) have been seized and a seizure warrant for Samourai’s mobile application was served on the Google Play Store.  Per DOJ, the application will no longer be available to be downloaded from the Google Play Store in the United States.

“As alleged, Keonne Rodriguez and William Lonergan Hill are responsible for developing, marketing, and operating Samourai, a cryptocurrency mixing service that executed over $2 billion in unlawful transactions and served as a haven for criminals to engage in large-scale money laundering.  Rodriguez and Hill allegedly knowingly facilitated the laundering of over $100 million of criminal proceeds from the Silk Road, Hydra Market, and a host of other computer hacking and fraud campaigns.  Together with our law enforcement partners, we will continue to relentlessly pursue and dismantle criminal organizations that use cryptocurrency to hide illicit conduct,” U.S. Attorney Damian Williams said.
[Press Release](https://www.justice.gov/usao-sdny/pr/founders-and-ceo-cryptocurrency-mixing-service-arrested-and-charged-money-laundering?ref=nobsbitcoin.com)
[Full Indictment](https://www.justice.gov/media/1349321/dl?ref=nobsbitcoin.com)


### FBI Issues Warning Against Using 'No-KYC Cryptocurrency Money Transmitting Services'

In a move against what's deemed the best practices in Bitcoin security, the Federal Bureau of Investigations issued a warning to Americans against using 'cryptocurrency' services that are not registered as money services businesses (MSB) or do not perform KYC surveillance on their users.
Delivering these same capabilities on the Bitcoin blockchain without smart contracts and stablecoins was challenging & we therefore made the difficult decision to remove native Bitcoin & other UTXO support," she added.

Events like this cause a chilling-effect

[Announcement](https://www.ic3.gov/Media/Y2024/PSA240425?ref=nobsbitcoin.com)

### zkSNACKs Coinjoin Coordinator is Now Blocking US Residents and Citizens

update: zkSNACKs to Suspend Its Coinjoin Coordination Service on June 1st

Wasabi Wallet also offers coinjoins similar to Samourai (Wasabi allows for many coordinators)

"Effective immediately and until further notice, zkSNACKs is now blocking U.S. citizens and residents from visiting its websites, downloading and using Wasabi Wallet and any related products and services, including APIs and RPC interfaces," announced the company.

"zkSNACKs is now blocking U.S. citizens and residents from visiting its websites, downloading and using Wasabi Wallet and any related products and services, including APIs and RPC interfaces," announced the developers of Wasabi Wallet.

zkSNACKs is the company behind the default coinjoin coordinator of Wasabi Wallet. Since March 2022, the company has been proactively filtering certain UXTOs from registering to coinjoins by partnership with a chain surveillance partner since March 2022.

[blogpost](https://blog.wasabiwallet.io/zksnacks-now-blocking-u-s-residents-and-citizens/?ref=nobsbitcoin.com)


### Phoenix Wallet to Stop Serving US Customers on May 3rd

"On May 3rd, 2024, Phoenix Wallet will be removed from US app stores," announced the project.
"Recent announcements from US authorities cast a doubt on whether self-custodial wallet providers, Lightning service providers, or even Lightning nodes could be considered Money Services Businesses and be regulated as such. We are removing Phoenix Wallet from US app stores and will be assessing other potential impacts to our operations," said ACINQ, the developer behind Phoenix Wallet.
The project developer added that users from the US should empty their wallet by going to:

Settings > Close channels (Android)
Settings > Drain wallet (iOS)
"We highly recommend *not force-closing* channels, as on-chain fees could be significant," added the developer.

Phoenix wallet users in the United States are encouraged to close their channels and empty their wallets prior to May 3, 2024.

[ACINQ statement](https://twitter.com/acinq_co?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1783878732865740940%7Ctwgr%5Eeb23899225e0c1ca09fe9914be7c96ff62bc4060%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fprotos.com%2Fphoenix-wallet-to-be-removed-from-us-app-store-after-samourai-crackdown%2F&ref=nobsbitcoin.com)
[Announcement](https://twitter.com/PhoenixWallet/status/1783878658014249027?ref=nobsbitcoin.com)

### Alexey Pertsev - Tornado Cash case (REVIEW)

Dutch court found Tornado Cash developer Alexey Pertsev guilty of money laundering and sentenced him to 64 months in prison. Pertsev's legal team has 14 days to appeal the decision.

Tornado Cash Developer Alexey Pertsev Sentenced to 64 Months in Prison in the Netherlands

A Dutch court convicted 31-year-old Alexey Pertsev of laundering $2.3 billion in cryptocurrency through the Tornado Cash mixer.
Dutch prosecutors have alleged that Pertsev designed Tornado Cash to be the ideal money laundering tool through the use of "smart contracts." Conversely, Pertsev's defenders argued that these same attributes made Tornado Cash such an effective privacy tool.

The judges rejected Pertsev's argument that it was wrong to hold him accountable for Tornado Cash's users, who are, by design, anonymous and independent.

[Case Documents (Dutch)](https://uitspraken.rechtspraak.nl/details?id=ECLI%3ANL%3ARBOBR%3A2024%3A2069&ref=nobsbitcoin.com)
[News Article](https://www.dlnews.com/articles/regulation/tornado-cash-dev-alexey-pertsev-guilty-of-money-laundering/?ref=nobsbitcoin.com)

### Aqua Wallet - Lightning - Liquid Wallet

Aqua Wallet, developed by Jan3, is a non-custodial mobile Bitcoin, Lightning, Liquid and Tether USDT (on Liquid, Ethereum, and Tron) wallet. Available on Android (APK only for now) and iOS.

[Website](https://aquawallet.io/)

[Announcement](https://twitter.com/JAN3com/status/1742758563271881132)
[Blogpost](https://jan3.com/blog/surf-the-bitcoin-revolution-with-aqua/)

### Roger Ver Charged with Mail Fraud, Tax Evasion & Filing False Tax Returns

Roger was an early bitcoin advocate turned fork proponent

Ver is accused of neglecting to file tax returns on asset sales and failing to pay a "United States exit tax" on capital gains after he gave up U.S. citizenship and set up businesses and secured citizenship in St. Kitts and Nevis.
The indictment claims that by June 2017, Ver’s two U.S. registered companies, MemoryDealers and Agilestar, owned approximately 70,000 BTC. In November 2017, Ver allegedly sold tens of thousands of them on cryptocurrency exchanges for approximately $240 million in cash.
"Even though Ver was not then a U.S. citizen, he was still legally required to report to the IRS and pay tax on certain distributions such as dividends from MemoryDealers and Agilestar, which were U.S. corporations. Ver allegedly concealed from his accountant that he had received and sold MemoryDealers’ and Agilestar’s bitcoins that year. As a result, Ver’s 2017 individual income tax return did not report any gain or pay any tax related to the distribution of MemoryDealers’ and Agilestar’s bitcoins to him," was stated in the press release.
"In total, Ver is alleged to have caused a loss to the IRS of at least $48 million," was stated in the indicment.

[Indictment](https://www.justice.gov/opa/pr/early-bitcoin-investor-charged-tax-fraud?ref=nobsbitcoin.com)
[Press Release](https://www.justice.gov/opa/pr/early-bitcoin-investor-charged-tax-fraud?ref=nobsbitcoin.com)

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

### How to Make Use of BOLT12 in LDK

Jeff Czyz from Lightning Dev Kit wrote a walkthrough on BOLT12, explaining what it is and how one can make use of it in LDK.

"BOLT12 is a new payment protocol for Lightning that offers enhanced privacy, reusable payment codes, refunds, and much more, all natively over the Lightning Network."
No additional servers are required. This is all possible using new technologies like onion messages and route blinding.
BOLT12 specification defines "an offer that can be considered a precursor to an invoice. It contains less data than an invoice and is smaller to display as a QR code. Optionally, it may contain blinded paths—more on that in a moment. Someone scanning an offer sends an invoice request to the intended recipient, who replies with an invoice containing a unique payment hash."

[Guide](https://lightningdevkit.org/blog/bolt12-has-arrived)

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

### Blitz Wallet Beta available for testing

Self-custodial Lightning Wallet built off of Blockstream Greenlight and Breez SDK, 100 spots for iOS and APK available for Android

[Link](https://blitz-wallet.com/)

### El Salvador's Chivo Wallet Source Code & VPN Access Leaked

According to The Block, the hackers released the stolen information to the public to punish the Salvadoran government for refusing to engage with them. It's unclear what the hackers want to discuss with El Salvador officials.
"This time I am bringing you the code that is inside the Bitcoin Chivo Wallet ATMs in El Salvador, remember that it is a government wallet, and as you know, we do not sell, we publish everything for free for you,” CiberInteligenciaSV said in a post.
The files reportedly contain snippets of the wallet's code and VPN credentials associated with the Chivo Wallet's ATM network.
The group recently disclosed the personal data of approximately 5.1 million Salvadorans in a separate exploit. This is part of a series of extensive database leaks containing various records from the country.

Note: stakes are high

[Article](https://www.tftc.io/el-salvador-chivo-wallet-hack-source-code-leak/)

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
