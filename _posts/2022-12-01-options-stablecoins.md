---
title: An Options Protocol for Stablecoins
date: 2022-12-01 12:00:00 +0000
categories: [DeFi]
tags: [defi]
---

### Context

Option markets in traditional finance are a much larger than the equivalent spot markets. However, in DeFi (and in crypto in general) options are still at the very early stages of their development.

### The product

1. Current options to speculate or hedge depeging events in crypto are limited.
2. Depeging events are one of the largest (systemic) risks in crypto and DeFi in particular, as evidenced by the UST/Luna crash this year.

From 1. and 2. a product that would allow market participants to make or take risk on depeging seems yet another piece needed in the DeFi stack and would allow two new views to be taken in a capital efficient manner by the market: betting on a depeging event or hedging one’s position against one.

We propose a protocol that allows users to issue and/or purchase put options on pegged assets, starting with USD stablecoins.

1. Users could deposit their stablecoins in option-selling vaults at different risk ranges (think puts at .99 or puts at .75). 
2. Users could purchase puts previously minted by the vault depositors, gaining positive exposure to eventual depeg events.

 

It would be important to have these puts be american options, since speculating on a depeg event at a specific date (the counterfactual that european options would allow) intuitively seems a much much smaller market.

### Use cases

1. Betting on a Depeg Event
    1. As evidenced from the UST depeg and subsequent Luna crash in May ‘22, depegging events can be extremely impactful economic events in crypto markets.
        1. Between UST (~18B) and LUNA (-40B), about the same market value was wiped as in the Lehman collapse in 2008 (~60B).
    2. Trading risk around these infrequent but large economic events is an important part of functioning markets.
    3. Market participants who could purchase these puts, without holding the underlying stablecoins to get cheap upside to a possible depeg. 
        1. Again, in the Luna scenario, there were multiple investors and funds that were outspoken against UST’s risks. They had a contrarian, and ultimately correct, view — the best combination for having a large win in the market.
        2. However, in our opinion, no existing product for expressing that view was perfect:
            1. Shorting LUNA has quite limited upside (2x) and unlimited downside as LUNA kept rising (and as the famous aphorism goes: the market can remain irrational longer than you can stay solvent).
            2. Borrowing UST to short it has even more limited upside (still 2x in theory but Luna falls faster in practice due to the minting mechanism) albeit much more limited downside too (UST would in all likelihood never go substantially above $1 and make this short position lose money).
            However, UST had access to an anchor yield of 20%, and as such, we would expect market forces to make borrowing rates for UST very high as well, thus making holding this borrowed/short UST position expensive to carry.
        3. On the other hand betting on UST’s depeg by buying deep out of the money puts (for example at .80 or .60 while UST is still firmly pegged to $1) should be relatively cheap (you’re buying the right to sell what is supposed to be one dollar at 60 cents) and hence pay off many multiples on the capital invested if they become in the money. The downside is 1x and most expiries should end out of the money, but this strategy would pay much more than the previous short strategies we’ve covered if what we’re trying to bet on happens.
    
2. Depeg Insurance/hedging on held Stablecoin position
    1. An investor that holds a percentage of their portfolio in stablecoins (for yield farming, for dry powder, etc) may want to insure against one of the risks that position carries — a possible depegging. For this use case, investors would buy puts to insure either all or a portion of their stablecoin position. Guaranteeing a max limit to the loss they’d take if a depeg happens (this max loss can be smaller or higher depending on how much they are willing to pay for the puts).
    2. This depeg insurance via puts strategy envolves continuously repurchasing these options as the previous ones expire to assure perpetual protection. In practice it would be a negative yield on the stablecoins insured.

1. Yield on Stablecoins 
    1. Stablecoin depositors sell puts on a rolling basis (as soon as one out of the money put sold expires, a new put is immediately sold by the vault).
    2. Put strike prices would obviously be <1 but could be:
        1. All at a number like .98 to concentrate liquidity and allow at least some size to purchase (hopefully leading to fairer pricing)
        2. Distributed over a few fixed prices (for example .99, .975, .9, .75, .5) with puts sold proportionately over them (still is an automatic allocation reducing decision fatigue and gives put buyers more choices to express their views)
        3. Decided by the user, by selection on a slider scale where some users would be very confident in a stablecoin’s peg and hence comfortable selling all in .99 strike puts and other users, less confident in the peg, could sell .98 or .95, generating a lower yield but incurring less risk of having to pay up since only a deeper depeg would hit them

### Further Considerations

It is probably even better for this product to be implemented in a synthetic way instead of actually needing to deposit stablecoins. There is considerable opportunity cost to locking up stablecoins and it.

Most examples given here were on the stablecoin use case, but this concept/intrument would apply equally well to any pegged asset where depegging is a possibility (even if remote). Liquid staking derivatives, especially before ETH can be withdrawn from PoS validators, are another prime candidate for a put options market to form around (and potentially could be even bigger).