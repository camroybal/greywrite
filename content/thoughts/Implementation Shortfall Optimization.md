---
title: Implementation Shortfall Optimization
date: 2025-02-08
tags:
  - seed
  - tradedesk
---
> *Implementation Shortfall is the difference between the decision price and the final execution price (including fees or commissions) during a trade; also known as **Slippage**. 
> The concept is of particular concern when dealing with large institutional level orders where liquidity is a primary concern.

$$ \ IS = [ (N * (PriceAtEnd - PriceAtDecision))$$
$$ - Σ (NumActual * (PriceActual - PriceAtDecision)) ] $$
$$ / (N * PriceAtDecision)$$
