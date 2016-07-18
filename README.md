# Project of Bitcoin Data Mining

## Description
Bitcoin Data Analysis Project Proposal

_Abstract:_   
The bitcoin, or the open finance, is revolutionizing our current financial system. This decentralized currency is transparent to everyone and financially connects people all around the world. The key technology that supports bitcoin is Blockchain, which is an emerging distributed database technology and has been proved to be powerful in many other fields, such as pilot projects and copyright management system. In this project, I am going to conduct some interesting analysis on the bitcoin data and provide predictions for investment.

_Schedule_  
1. Explore the active regions where bitcoin is being used around the world. The first half of this portion has been done by monitoring the transactions’ IP addresses and bitcoin nodes’ IP addresses. Further work includes fetching social networks’ posts that contain the “bitcoin” key word and locating these posts (still collecting data on this). A comparison between the results from these two solutions would be interesting.  
2. Trace the transactions among the users and explore the topology or the most influential users of the bitcoin network. Originally, this should be a hard work since one characteristic of the bitcoin network is anonymous, which means we can only see the transactions instead of the users. Luckily, an article titled “an analysis of anonymity in the bitcoin system” has been published to solve the problem of constructing the user network from the transaction network. Based on the user network, a directed graph can be constructed and the most influential users can be found by page-rank algorithms.  
3. Analyze the price fluctuation of bitcoin. One method is to use regression analysis on the price data directly. Another is to apply NLP analysis on the social network posts to predict people’s actions. 

## Data Source and Files
- BitcoinTransactionsTrace.ipynb  
This file is for acquiring all lastest transactions of bitcoin around world and find the geolocations of these transactions.  
The transaction data is acquired by listening to the websocket service from wss://ws.blockchain.info/inv.  
The geolocation data is obtained by IP to geolocation service from http://ip-api.com/json/$IP.

- BitnodesAnalysis.ipynb  
This file is used to find all of the bitcoin's nodes around the world.  
The data of the bitcoin nodes are provided by https://bitnodes.21.co/api/v1/snapshots/$TIMESTAMP.

- BitcoinNetworkAnalysis.ipynb  
This file is used to analyze the topology and the most influencial users in the bitcoin network.  
The current data used is from http://compbio.cs.uic.edu/data/bitcoin/ and http://anonymity-in-bitcoin.blogspot.ca/2011/09/code-datasets-and-spsn11.html  
My own data set will be constructed according to http://arxiv.org/pdf/1107.4524.pdf.

