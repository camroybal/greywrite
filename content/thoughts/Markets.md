---
title: Markets
date: 2025-01-06
tags:
  - seed
---
## The Stock Market

What began as an interconnected web of human beings speculating on future earnings of corporations in the United States, has now evolved into the *erectus spinea* supporting the U.S. economy. The average American relies on the stock market to give a representative temperature reading of the over all financial health of the nation. 

As a professional participant in the U.S. capital markets, I routinely have close brushes with the intestines of this system. Like many other complex [[Systems Ontology |systems]], the shape of the U.S. stock market tends to take on fractal like properties; exploding into subsystems and interwoven segments that work together; functionally, in large part primarily out of sheer luck and of course from build in strict regulatory frameworks. 

> "I am but a loose collection of parts, flying in formation - My grandfather"

### Layers of abstraction

##### Observation points 1 & 2
From a high enough observation point, the U.S. stock market has a simple form. Human and corporate participants exchanging dollars for participation in growth patterns of corporations and their businesses. As you *zoom in*, you notice that despite the fact that nearly half of the U.S. population has exposure to the market, the core exchange partners **actually** participating are[[#Market Makers| machines]]. Very seldom are retail human participants actually exchanging shares amongst themselves. So instead of "web" of market participants, you have a wheel and spoke design with only the spokes (in this case the market makers) being networked to each other. What appeared on the surface as a latticed system with many nodes connecting to each other, in fact have much fewer edges than initially expected and larger but fewer nodes. The *body* of each node however, contains **lots** of sub nodes. 

These sub nodes are comprised of actual speculators, traders, and investors that are placing orders into the system at this level (there are sub levels where greater *volumes* of stock are traded but in this case we are talking surface market activity). 

#### Market Makers

Here is how the process of market making works - A investor or trader places an order with their broker dealer, for this example we can consider this as nothing more than an aggregator function in this system. That order flows from participant node (our investor/trader) along the interconnect to the broker dealer. That aggregator node then either sends that order, along with all the others, through to a market maker. Upon receipt of the order, the market maker evaluates the price - "does this client need a specific price or have the designated the order at market price, meaning they will take whatever is available at the the best price available. If the client as designated a price, the market maker compares it to their own inventory of stock or makes a purchase along their own connection on the exchanges (often NASDAQ or an Electronic Trading Network called an ECN or more often, Dark pools) - "are we willing to sell or buy at X price, or can this be bought among our networks for Y price and then given to the client at X price?".

The high level of this logic looks like this

``` logic
## Buy order

client_price = x
current_bid = b    #market makers buy at the bid. Participants sell at the bid.
current_ask = a    #market makers sell at the ask. Participants buy at the ask.

if current_inventory_cost ==< client_price;
	then sell_shares_to_client;
	else buy_shares_at == b;    #Buy shares from networked node at bid
		sell_shares(client, a);
	return difference_between a-b && calculate_profit

```

The purpose of this function is actually regulatory required by NASDAQ. In essence, market makers exist for the singular purpose of providing liquidity to the system. Doing so, however, does not come without risk. What happens if there is an adverse price move in their own inventory? What happens if they don't have the inventory to sell to a client, or enough cash to buy from a client if the prices are moving against them? Well, in short, they eat it. For taking risks like these, the market provides them with the benefit of capturing that bid ask spread as explained in the above example. They are compensated (well) for this service which is integral in a smooth functioning market. 

This used to be done by hand. Each market maker was an individual person or a company composed of persons who's sole job was to perform this function for the firm. The role is now dominated by ultra high performance algorithms with near zero latency and machines that are constantly evaluating the market to limit the risk component associated with this work. 
