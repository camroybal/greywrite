---
title: VWAP
date: 2025-02-08
tags:
  - seed
  - tradedesk
---
## Volume Weighted Average Price

A [[Passive Trading Algorithm]] used to execute orders in a non-linear fashion across a time frame in relation to the average price traded on a security throughout the day. Large orders may have an impact on market price if sold immediately by wiping out large portions of current bid/ask spreads all at once. 

$$VWAP = ∑(Price × Volume)​ / ∑Volume$$

#### Features
- Set and forget
- Large order execution 
- Easily reportable as Average Price
- Equal time Interval execution