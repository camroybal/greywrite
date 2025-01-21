---
title: SDTC Project
date: 2025-01-19
tags:
  - seed
---
I was able to get access to the schwab developer portal on an individual-api license. I have begun work on a project called the SDCT or Schwab Depth Charge Terminal. The idea is to create a companion software for ThinkorSwim, that individuals can use to quickly look a their account information, evaluate equities and efts and even fire off quick trades if they want.

One of the biggest gripes that[[thoughts/Dumb Money| retail clients]] have expressed with with their overall trading experience, appeared when Schwab removed access to their legacy trading platform Street Smart Edge. Clients got used to simple workflow for viewing their account data and history. I will admit, that information is about 6/10 in terms of difficulty to easily access with TOS. 

This project is supposed to be a simple tool where all the information can be quickly viewed. Even though the application relies heavily on Schwab api performance, the app itself will be designed to have an incredibly fast front end with the bulk of the data being queried and manipulated by the backend. 

I am aiming for small package sizes, simple user interface, server side rendering. 

## Tools

#### Languages
- Python
- Javascript
#### Frameworks
- FastAPI
- Svelte
- Pocketbase
#### Libraries
- Pandas
- numpy
- poetry 
- pydantic

## System Design

![[thoughts/images/SDCT-Mock.png]]
## Features List

- Fast - Ultra light weight
- Comprehensive account info
	- All orders - 30 days
	- Simple Profit and Loss
	- Position Tracking
	- Account Status
		- Numbers
		- Status - PDT, SCUF, MARGIN EQ, ETC
		- Cash
		- Buying power
		- Settled cash 
- Equities & ETFs
	- Fundamentals
	- Numbers only technicals
	- Calculations
	- Transformations
	- Alerts

