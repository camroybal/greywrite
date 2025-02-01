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

The purpose of this function is arises from regulatory frameworks set forth by NASDAQ. In essence, market makers exist for the singular purpose of providing liquidity to the system. Doing so, however, does not come without risk. What happens if there is an adverse price move in their own inventory? What happens if they don't have the inventory to sell to a client, or enough cash to buy from a client if the prices are moving against them? Well, in short, they eat it. For taking risks like these, the market provides them with the benefit of capturing that bid ask spread as explained in the above example. They are compensated (well) for this service which is integral in a smooth functioning market. 

This used to be done by hand. Each market maker was an individual person or a company composed of persons who's sole job was to perform this function for the firm. The role is now dominated by ultra high performance algorithms with near zero latency and machines that are constantly evaluating the market to limit the risk component associated with this work. 