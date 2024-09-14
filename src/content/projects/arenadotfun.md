---
title: "arena.fun"
description: "A platform to make trading on-chain competitive and fun."
heroImage: "/projects/arenadotfun/hero.png"
pubDate: "July 8 2024"
badge: "BUILDING"
tags: ["Web3", "Typescript", "Firebase"]
code: ""
demo: ""
blog: ""
---
# Overview #
A platform to officiate on-chain trading competitions to provide a new and fun aspect to "degening" and trading. The competition will have a jackpot that is funded by an entry fee which will then be distributed to the winners. The winner is decided by the wallet or wallets that have the highest cumulative PNL percentage, accounting for both realized and unrealized gains. 

# Purpose #
We saw an opportunity to expand and "gamify" the game that everyone was already playing. People were quick to boast about their profits on Twitter but often lacked proof. We are here to allow the traders and private groups to prove themselves and to show the world their genuine skills. Traders wouldn't have to change their routine, they simply have to do what they have always been doing. We believe this could become an event that everyone would monitor and be excited to compete in. 

# How it was made #
For the backend, I began working on the challenge of getting accurate profit and loss (PNL) data myself. I considered some PNL APIs such as <a target="_blank" href="https://api-info.cielo.finance/">Cielo Finance</a> which would easily return the PNL for every SPL token a wallet has traded as well as their unrealized profits. This would have made the process much faster and smoother but it wasn't viable due to the price and response times of the APIs. After much research and consideration, I decided to use Helius' API to get the transaction data for a wallet. This would mean I would be able to calculate how much Solana (SOL) leaves and enters an account when they swap for a specific SPL token. This approach was also more sustainable as the number of credits used is significantly less than using Cielo's APIs. 

Using Helius' API, I'm able to keep track of each token traded and send it to the Firestore database. This proved challenging as a lot of optimizations needed to be made in order to cut down the processing time to get a wallet's PNL. Eventually, I shortened a 3 to 4 minute wait time to a few hundred milliseconds. This was necessary if we were going to get the PNL of many wallets all at the same time. 

After completing this task, I linked all the processing to the database and began testing the program. This took several days to debug as there were many edge cases to iron out and design around. An example is considering the tokens a user may already have before the game starts, which if sold, should not be counted into their profit and losses as it was beyond the scope of the game's timeframe. 

The frontend was first designed on Figma, going through several iterations of a design that we felt would match the competitive theme well. We decided to go for a futuristic theme that would style blue and orange neon accents. After designing, we then started implementing components and pages within a NextJS project. This process took several iterations as well as we ran into many troubles with file structuring and interactions with backend code.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Optimizing PNL processing
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Working with other tools/platforms
3. &nbsp;&nbsp;&nbsp;&nbsp;3\. Linking the frontend with the backend

Optimizing PNL took a lot of iterations to get right as I needed to account for all the swaps and transfers within a certain timeframe. I needed to weed out the transfers that didn't matter such as token account creation, NFT swaps, token mints, etc. I also needed to only process the transactions that fell within the game's time frame in a chronological order. This was to ensure that we kept track of all the tokens that were swapped within the timeframe and excluding those that were bought before the game started. 

Another challenge was working with the various other platforms within the Solana ecosystem. Jupiter, an aggregator that finds the best routes to swap currencies, uses a vastly different transaction system than Bonkbot, a telegram bot that thousands of users use to trade SPL tokens. Then Bonkbot's transactions varies from those using Photon or Bullx, both web app trading platforms. Then I needed to account for tokens that were not seeded on Raydium, in other words, did not have a liquidity pool for actual trading. These tokens were on pump.fun and Dexscreener's Moonshot, both platforms that easily allows anyone to launch an SPL token. The way these platforms and tools take in fees were different, all in all making the process a large mess. Much of this was resolved by keeping track of what program and address the transaction interacted with, which allowed me to accurately process the transaction based on the characteristics of the transaction. For example, Bonkbot transactions interact with the Bonkbot fee address in order to get fees, which can differentiate the transaction from a different platform's transaction.

Another problem we ran into was linking the frontend with the backend in a seamless and simple manner that we believe we could scale later in the future. We believe that we had to design it in a way so that it won't be a burden that will hinder a possible expansion of features or development. This led to a lot of restructuring, designing, and guessing in order to settle on a structure that we liked and had the best chance to scale.

# Conclusion #
Much of this project has taught me a lot about the Solana blockchain. From how accounts work to the way transactions are formatted and read. It was a lot to learn but it was a project I'm extremely passionate about. I think the idea could rapidly gain popularity within "Crypto Twitter" and I think it could distrupt the Solana ecosystem in a positive way. Only time will tell...