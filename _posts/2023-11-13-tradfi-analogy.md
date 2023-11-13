

---
title: Do Big TradFi Product Types have to be Big in Crypto too?
date: 2023-11-13 12:00:00 +0000
categories: [DeFi]
tags: [defi]
---



It is common practice in crypto discussions to analogize to traditional finance when considering potential sizes (or TAMs) of different product types and verticals. 

If options' volumes in TradFi are multiples of that of stocks while in crypto they make up an insignificant fraction of spot volumes, that must *surely* mean that options markets in crypto are heavily underexplored and poised for huge growth, right?

As someone who's fallen into this trap, I've recently been questioning myself on the value of this line of reasoning. 

Let's look at the three best examples and try to come up with a strong hypothesis as to why large TradFi verticals didn't translate to crypto (at least not yet and at least not at scale):



## Options

Option markets in traditional finance are very large when compared to spot. This isn't, however, the case in crypto, where, despite many attempts at building different options markets, both centralized and decentralized, they are still relatively small. 


**Hypothesis - Perps [(0)](https://en.wikipedia.org/wiki/Perpetual_futures) have reached ecape velocity and liquidity network effects that syphon the liquidity and interest in options that they'd need to grow.**


Derivatives markets' volumes come from a mix of speculation and hedging. An oil trader at a commodities desk buying crude oil futures to bet on some geopolitical event's outcome, or a company that produces it entering the same contract type but to hedge future price aiming for less volatile revenue (or costs).

For a derivatives market to have healthy and sustainable liquidity it is crucial to have both market participants -- the ones speculating and the ones hedging.

Perpetual swaps as an intrument were birthed in crypto and have since taken off as the most traded markets in the industry. Albeit not a replacement to everything that options can do, perps offered access to the leverage, speculation and hedging that constitute major parts of what the demand in crypto options markets would be made up of.

Importantly, they do this while asking the investor to understand the relatively simple and singular concept of funding rates instead of the plethora of partial derivatives, known as the Greeks, that options require one to grasp.

And lastly, contrary to both their TradFi counterparts (regular futures) and to options, perps don't expire. 
This design is extremely beneficial for bootstrapping and maintaining liquidity as:
1. positions don't need to rollover (and hence bootstrap) from one period to the next and 
2. there is *one*, unified perps market per asset pair versus the quadratic number of markets in options or futures as a function of pair and expiry (inevitably leading to more fragmentation).

Combined, these reasons help explain why perps have become so dominant in crypto markets, capturing the most volume and liquidity. The hypothesis is that the set of use cases that options provide and perps don't has been too small to meaningfully compete, hence leading crypto options markets to permanently have liquidity problems, that are even worse in DeFi -- and to ultimately be disproportionally smaller than in TradFi.




## Index ETFs

Passive investing into index ETFs has captured increasingly larger shares of all investing since their start around 30 years ago. They now account for a very substantial portion of all equities ownership and are well into the multiple trillions in AUM.

However, just as before in options, token indices are disproportionally much smaller in crypto than index ETFs are in traditional finance.


**Hypothesis 1 - If one is crypto-savvy enough to know about the DPI and Index coop [(1)](https://docs.indexcoop.com/index-coop-community-handbook/products/defi-pulse-index), they probably just want specific tokens, and to use them.**

One idea is that the intersection of people who know about tokenized indices and who don't want to pick their own positions but would rather have some wighted split may be very slim.

For one, there is extreme variance in quality amongst tokens, and crypto-savvy investors are probably more opinionated about what they want to hold (f.e. just SOL, not a basket of alt-L1s; or just MKR, not a basket of DeFi) than the average stock market investor that happily accepts broad exposure to, say, the US equities markets.

To exarcebate this, while in equities ETFs barely anyone cares about losing the ease or ability to vote on corporate governance votes of the underlying companies held, in tokenized indices some tokens are just economically unfeasible to hold if holding them means losing the ability to use them. Vote escrow tokens, PoS tokens, and multiple other tokenomics designs lend themselves very poorly to passive investing/indices.

**Hypothesis 2 - ETH serves as too good of an indice in itself.**

The native asset of a smart contract blockchain, in most cases, captures value from all the activity that happens on it and above it. All stablecoin transfers, token swaps, NFT purchases, contract deployments or any other type of usage on ethereum will accrue value to ETH holders and stakers in the form of deflation [(2)](https://youtu.be/MGemhK9t44Q?si=4FDEByYMhn4PsFJk) and execution layer staking yield [(3)](https://chorus.one/articles/what-is-mev-and-how-can-it-boost-your-staking-yields).

And as such, if ETH already captures value from the usage of every dapp or protocol built on it, many will perceive holding it as giving enough exposure to the broad ecosystem that exists in it (and ditto for other PoS tokens).



## Bonds & Credit


Borrowing is obviously one of the most important primitives in finance. 
However, while overcollateralized loans are large in both TradFi (mortgages, margin loans) and DeFi (MakerDAO, Aave), undercollateralized ones are large in traditional finance but not in crypto.

Companies issue debt all the time (bonds), and individuals borrow using everything from credit cards to personal loans for consumption, but the onchain equivalents don't really happen. 
The few products attempting to enable DAOs to borrow haven't picked up and individuals borrowing without collateral onchain hasn't happened at all.


**Hypothesis 1 - Raising capital with tokens is too good at the same time as bonds for volatile and often unproven business models would be too pricey.**

Buying debt issued by a DeFi DAO would be, at least for now, much more akin to investing in venture debt [(4)](https://www.svb.com/startup-insights/venture-debt/how-does-venture-debt-work#:~:text=Venture%20debt%20is%20a%20type,such%20as%20Silicon%20Valley%20Bank.) than in a Fortune 500 company's bond. 

As such: 
- anyone who believes enough in the project to consider being a lender, would probably just rather have the full upside via equity or token ownership, and 
- anyone who'd want a bond-like investment -- with relatively safe principle but higher yields than the risk-free rate [(5)](https://www.investopedia.com/articles/financial-theory/08/risk-free-rate-return.asp) -- would probably rather lend to an established, cash-flowing company than to a DAO with unproven or volatile value capture (unless they were offered a completely unreasonable yield). 

Such bonds then seem to me to be in a sort of uncanny valley [(6)](https://en.wikipedia.org/wiki/Uncanny_valley) that'd make them unattractive to every potential party involved: the upside-seeking investor, the investor looking for yield on relatively safe principle, and to the DAO itself.

The last actor there, the DAO itself, is particularly important to double click on. At the current stage of the industry's development, there is a completely one-sided cost of capital equation [(7)](https://www.investopedia.com/terms/c/costofcapital.asp) for it to raise capital:

1. On the one hand, these are imature, volatile businesses. Debt issued would thus have to be compensated with a much higher yield than what we'd expect to see in corporate bonds from established companies.
2. On the other hand, the other option available -- raising capital by selling tokens -- has, in most cases, a lower cost of capital than companies raising by issuing new equity, due to some speculative and liquidity/accessibility premiums that are commonly seen in crypto valuations. 

This scenario where the cost of capital of raising via debt is higher than its TradFi equivalents and the cost of capital of raising via token sales is lower than its TradFi equivalent is, thus, the hypothesis for why bonds as an instrument haven't worked in DeFi.




**Hypothesis 2 - personal credit onchain can't evolve before identity has been cracked.**

Moving past bonds and looking at individuals borrowing, in traditional finance, the key enabler for personal credit is identity: from credit scores to assess risk to debt collection mechanisms and legal recourses for enforcement in case of nonpayment.

Despite some attempts at building credit score equivalents based on a wallet's history and some others at bringing general identity primites onchain, at least so far, these haven't enabled robust credit and loans to happen onchain.





---

Infancy may still be the explanation as to why TradFi and crypto haven't converged when it comes to the largest product types in each. 

But it may also be the case that fundamental differences between the two dicatate that the types of financial products that find PMF and scale in each will simply be distinct.



\
\
\

(Thanks to Patrick Mayr for reading and helping me iterate earlier versions of this text.)

