---
layout: post
type: socratic
title: "Socratic Seminar 4"
meetup: https://www.meetup.com/taiwan-bitdevs/events/286459306/
---

## Announcements

Our fourth Socratic Seminar event will be held at a new location:

IMBIBE Taipei
誠安里 Section 3, Civic Blvd, 304號 · Da’an District

Learn about bitcoin development. Share, debate, and discuss trade offs in progress. Skim the [discussion topics](https://github.com/TaiwanBitdevs/TaiwanBitdevs.github.io/pull/9) on GitHub. We discuss a variety of developments, from industry updates and press releases, pull requests in popular git repositories (e.g. Bitcoin Core, lnd, c-lightning, rust-bitcoin, Joinmarket, WasabiWallet), research papers, technical blog posts, IRC logs, network monitors and more. Please add to the discussion topics on GitHub. We'd love to hear from you. After the event the we socialize over food and drinks. New location at the excellent Imbibe Taipei, 5 minutes from Zhongxiao Fuxing Station. Taiwanese food, homemade soft drinks, and cocktails available.

This event is free but everyone must order at least one drink.

我們每月舉辦的蘇格拉底式的研討會活動旨在促進辯論、信息共享和開放討論。在活動前幾週,聚會成員會從各種來源去整理討論主題：流行git倉儲（例如 Bitcoin Core、lnd、c-lightning、rust-bitcoin, Joinmarket、WasabiWallet）中的pull requests、研究論文、技術博客帖文、IRC 日誌、網絡監測等。經過一段時間的討論，一些活動會有來自開源項目、公司、研究和其他相關內容的介紹。隨後是反饋和問答部分。活動結束後，我們會在活動場地進行社交。

---
---

## Discussion Topics

### Taiwan deports Chinese-American Crypto-robbery suspect back to USA

Allegedly stole $3m in girls cryptocurrency and put it in Taiwanese made CoolBit wallets. He entered intto her house. Wallets were siezed.

[新聞] 華裔男在美搶9千萬躲台2個月全靠「冷錢包」

source: [English](https://focustaiwan.tw/society/202206060014), [中文](https://moptt.tw/p/DigiCurrency.M.1654492918.A.A8D)

---

### The History of Lightning Dev Kit

LDK is a growing lightning implementation written in Rust.  It's used in server side software even though that was not its goal.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">A history of LDK:<br><br>1. rust-lightning is created with the goal of being embedded in existing Bitcoin wallets, like Electrum<br>2. Electrum makes its own LN Implementation<br>3. rust-lightning changes its name to LDK and pivots to being a kit for implementing LN in Bitcoin mobile wallets</p>&mdash; fiatjaf (@fiatjaf) <a href="https://twitter.com/fiatjaf/status/1534584538994819072?ref_src=twsrc%5Etfw">June 8, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

---

## Celsius Network "Pauses" Customer Withdrawals

- Celsius offered enormous yields to customers by allegedly rehypothicating funds
- Celsius allegedly holds 150k btc, Luna LFG held 80k
- Funds might get held in litigation for years if MtGox is any clue
- Canada's 2nd largest pension fund invested in a $400m equity round of financing for celsius in oct 2021

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">.<a href="https://twitter.com/CelsiusNetwork?ref_src=twsrc%5Etfw">@CelsiusNetwork</a> is pausing all withdrawals, Swap, and transfers between accounts. Acting in the interest of our community is our top priority. Our operations continue and we will continue to share information with the community. More here: <a href="https://t.co/CvjORUICs2">https://t.co/CvjORUICs2</a></p>&mdash; Celsius (@CelsiusNetwork) <a href="https://twitter.com/CelsiusNetwork/status/1536169010877739009?ref_src=twsrc%5Etfw">June 13, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

---

## BIP 47 Payment Code Upgrades (v5?)

[BIP47 @PizzaDayPrague discussion](https://gist.github.com/RubenSomsen/21c477c90c942acf45f8e8f5c1ad4fae?permalink_comment_id=4197284#gistcomment-4197284)

- reducing space requirements
- outsourcing notification tx
- allowing collisions

Participants: @afilini, @kixunil, @SomsenRuben, as well as @danielabrozzoni, @EricSirion, @pavolrusnak, @salvatoshi, and others.

> As per this gist, this version of BIP47 (v5?) adds one or two points of complexity and removes a big one:
>
> - Outsourcing requires private interaction over (presumably) the Lightning Network
> - Detecting new notifications requires custom infrastructure (optional, only if recipient address outputs are avoided to save space)
> - Notification transaction no longer leaks privacy (big)

---

### [Fuji](https://fuji.money): Borow bitcoin-backed stablecoins, synthetic stocks and bonds on Liquid

- Liquid (Blockstream led Federated Sidechain) based

---

### KYC Free Visa MasterCard Debit Cards are Gaining Steam

get a digital or physical debit card for sats. No KYC requirment because the cards are low (&lt; $1000?) value

- [The Bitcoin Company](thebitcoincompany.com) Visa
- [Edge Wallet](edge.app) MasterCard

---

### Bolt.fun [Shock the Web Hackathon 2](https://bolt.fun/hackathons/shock-the-web-2/)

4 day hackathon. Thousands of USD in prizes.

> build and design web applications that can interact with lightning & [WebLN](https://www.webln.guide/).

Let's put a Team Taiwan together. Good opportunity for us to set up a space

> Shock the Web 2 ⚡️will be starting on Thursday (June 16th) with a day of discussions and workshops. We'll then let you get on with hacking for the whole weekend until the submission deadline (17th-19th). Of-course, we’re going to have mentors to help you along the way.

---

## El Salvador Introduced 44 Countries to Bitcoin

[Bitcoin Magazine coverage](https://bitcoinmagazine.com/culture/el-salvador-brought-44-countries-to-bitcoin)

> - El Salvador hosted central bankers and financial authorities from 44 countries for a financial inclusion event this week.
> - All participating members were able to download their own Bitcoin wallets and make purchases with BTC.
> - In July 1944, 44 countries met to determine the Bretton Woods financial system. Once again, 44 countries came together to learn a new system.

---

### Oslo Freedom Forum

> The main themes of the conference were human rights and the struggle against despotism in all its forms. This year, however, the activists were presented with a powerful aid: Bitcoin and its permissionless payments, its individual empowerment, its ability to help raise funds for any cause, anywhere in the world.

[Bitcoin Magazine coverage](https://bitcoinmagazine.com/culture/bitcoin-purpose-at-oslo-freedom-forum)

---

### 0-conf BOLT [PR](https://github.com/lightning/bolts/pull/910)

Blue Matt [Says](https://twitter.com/thebluematt/status/1531509811866529792?s=21&t=cWK88c6Hn54_Jj9BY6DwLQ):
> This allows for interoperability between various lightning implementations in how they negotiate and allow 0-conf channel use, allowing more flexible client/LSP relationships.
--
> This PR does three things:
>
> - Add support for channel aliases: a made up alias (can be independent for each side) unconnected to the real funding UTXO, by adding a TLV to funding_locked.
> - Allow a peer to insist that the alias always be used, never the real SCID, for privacy, using a new channel_type.
> - Allow a peer to indicate that it trusts the opener, and will allow zeroconf, using a new channel_type.

---

### Rust [cln_plugin](https://docs.rs/cln-plugin/latest/cln_plugin/) crate

- Core Lightning plugin Let's [fedimint's minimint](https://github.com/fedimint/minimint/pull/101) intercept HTLC contracts to allow someone to buy the preimage of the contract from the federation to complete incoming lightning payments. I think.

---

### Umbrel [v0.5 CLN release](https://twitter.com/umbrel/status/1534164270459473921)

- made over UI
- includes Core Lightning

<img src="https://i.imgur.com/b8IeGru.jpeg" alt="Screenshot of Umbrel v0.5 dashboard looking like MacOS" width="800">

---

### [*Un*brel](https://github.com/dsbaars/unbrel) removes Umbrel's proprietary cruft to revert back to lnd

- Umbrel don't use a free software license
- their apple-looking front end is getting heavy
- people don't like that so much infrastructure is built on unreliable Raspberry Pi single-board computers either

> Ah I missed this was posted here as well, probably needs a bit of context 😅
>
> I created this because there was an accumulation of bad decisions and a lack of action and taking responsibility regarding these decisions regarding Umbrel.
> Although I do like how accessible Umbrel makes running LN node for everyone, I don't like the recklessness they seem to have when it comes to releasing and the lack of priority they seem to have regarding the security of critical components.
>
> Although I'm honestly impressed by how Umbrel 0.5.0 looks, this actually reconfirms the feeling they prioritize this over security.
> They broke quite a lot of useful applications like lightning-shell, haven't updated the most used tooling (like Thunderhub) in a while.
> The last drop for me was that they accidentily downgraded the LND container from 0.14.2 to 0.14.1 (while 0.14.3 is out for a while).
> I know making mistakes is human, but this is only the fraction of the things I noticed which is really reckless.
>
> I know they state their software is beta and experimental, but that is really no excuse for this reckless behaviour which can be easily avoided simply by adding tests and simple checks (e.g. LND version should be greater than or equal than current version).
>
> Since the Umbrel dashboard doesn't add any functionality, only makes it look nice I didn't want to be dependent on the Umbrel development team and therefore I created un-brel.
> With the default settings (configurable through the .env file) it uses the same docker images as Umbrel does, but with a newer version without the need to move the data.
>
> I also added the lines to easily enable RTL, Thunderhub, LNDg and Lightning shell, so the only thing you would miss is the Umbrel dashboard.
> I have been running it with portainer as stack myself, this really makes updates very easy since projects like RTL and Thunderhub provide up-to-date multi-arch docker images as well.
> The stack runs stable for two days now, with far less resources than Umbrel.
>
> I'm also thinking of creating a simple status dashboard, but first I want to make sure the bare minimum is working correctly and without problems.
>
> — Djuri, the author, in Shadowy Super Coders telegram

---

### [Lightning Muxer](https://github.com/bottlepay/lnmux)

> fail-over for incoming Lightning payments. BOLT11 invoices are bound to a single node. If that node goes down, the invoice is no longer payable. The same is true for the node or its peers running out of inbound liquidity.
>
> What lnmux allows you to do is set up a cluster of nodes where each of these nodes can settle any invoice. If a node is unable to accept payments for one of the reasons above, senders will still be able to pay the invoice via one of the other nodes.
>
> Even with all nodes in the cluster available, it can be advantageous for the sender to have multiple routing options to better utilize liquidity and minimise fees. If needed, multi-part payments can be completed through more than one cluster node.

---

### Lightning withdraw Point of Sale via an embedded URL in a NFC card

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Announcing “The Bolt Card” 🧵<br><br>Visa? No<br>Mastercard? No<br>Lightning? Yes<br><br>The Bolt Card is an offline Lightning contactless card, powered by NFC, <a href="https://twitter.com/hashtag/Bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#Bitcoin</a> Lightning and LNURL.<br><br>A global, open, permissionless, decentralised monetary network. <a href="https://t.co/Wzv7mJQN6g">https://t.co/Wzv7mJQN6g</a></p>&mdash; Danny Scott ⚡ (@CoinCornerDanny) <a href="https://twitter.com/CoinCornerDanny/status/1526573313962680321?ref_src=twsrc%5Etfw">May 17, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

- [BLIP](https://github.com/theDavidCoen/blips/blob/84b00ea0802afca9c3a2c4e89b9891be3efe4333/blip-0015.md) for standardizing LNURL-withdraw for use at point-of-sale, e.g. over NFC
- Definitely has [security concerns](https://github.com/theDavidCoen/blips/blob/84b00ea0802afca9c3a2c4e89b9891be3efe4333/blip-0015.md#rationale)

---

### New York State To Place Moratorium On Non-Renewable Bitcoin Mining

> New York’s Senate just voted to place a two-year moratorium on the bitcoin mining industry preventing new applications for carbon-based mining.

[source](https://bitcoinmagazine.com/business/new-york-to-place-moratorium-on-carbon-based-bitcoin-mining)

---
---

## DEMO: [Rare Japanese NFTs](https://rarejapanesenfts.com)

*by [Koji Higashi](https://twitter.com/Coin_and_Peace)*

Japan's early vintage NFTs issued in 2016 and 2017 on Bitcoin with Counterparty
