---
title: "TrenchTown.fun"
description: "A platform to make trading on-chain competitive and fun. Pivoted to 
portfolio tracking on Solana."
heroImage: "/projects/trenchtown/hero.png"
pubDate: "July 8 2024"
badge: ""
tags: ["Web3", "Typescript", "Firebase"]
code: "https://github.com/trenchtowndotfun"
demo: "https://www.trenchtown.fun/"
socials: "https://x.com/playtrenchtown"
---
# Overview #
Originally a platform to officiate on-chain trading competitions to provide a new and fun aspect to "degening" and trading. The competition will have a jackpot that is funded by an entry fee which will then be distributed to the winners. The winner is decided by the wallet or wallets that have the highest cumulative PNL percentage, accounting for both realized and unrealized gains. We then pivoted to a portfolio tracking platform that allows users to track their positions and PNL across all tokens traded.

<center>
  <Image
    src="/projects/trenchtown/preview.png"
    width="400"
    height="200"
    format="png"
    alt="Portfolio Preview"
    class="image"
  />
  <p class="caption">Portfolio Preview</p>
</center>

# Purpose #
We saw an opportunity to expand and "gamify" the game that everyone was already playing. People were quick to boast about their profits on Twitter but often lacked proof. We are here to allow the traders and private groups to prove themselves and to show the world their genuine skills. Traders wouldn't have to change their routine, they simply have to do what they have always been doing. We believe this could become an event that everyone would monitor and be excited to compete in.

Then this idea became hard to sustain as we found it hard to have players come back every week to compete and the platform was heavily dependent on the market conditions. So we pivoted to be a portfolio tracking platform that aimed to be more accurate than other existing solutions in the Solana ecosystem. We saw that the PNL data that was provided other platforms were incredibly inaccurate often due to multiple reasons: fees, incorrect transaction parsing, unsupported platforms, liquidity trades, unintuitive UI, and denominating in only SOL or only USD.

# How it was made #
To get accurate PNL data, we used Helius to fetch a wallet's signatures. These signatures are then converted to readable transactions and parsed to extract the necessary data (input token, output token, amounts, etc.) which are then combined together to get the PNL over a certain timeframe. Combined PNL data is then stored in Firebase which is then fetched and displayed on the frontend.

The frontend was built using NextJS, TailwindCSS, and express APIs. The design was kept minimalistic and modern with a focus on usability and intuitiveness. 

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Optimizing PNL processing
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Data storage and efficiency
3. &nbsp;&nbsp;&nbsp;&nbsp;3\. Unreliable archival data retrieval

Optimizing PNL took a lot of iterations to get right as we needed to parse every Solana protocol to get the accurate information. This involved a parsing algorithm that would need to check every transaction element (swap data, account addresses, transaction type, etc.) to figure out what kind of transaction it was and what protocol it was coming from. Transaction types involved: swaps, transfers, mints, burns, and liquidity add/remove. Some protocols included Jupiter, Raydium, Bonkbot, Photon, Bullx, pump.fun, DAOs.fun, LMAO.fun, and Dexscreener's Moonshot. Then we needed to process as many transactions in parallel as possible given the Helius API's rate limits.

Given the amount of data, reads, and writes required for TrenchTown.fun, we designed a database schema that would make querying easier. All transactions and combined PNL data is stored in documents in a subcollection for a user. Each document is separated to hold data from 00:00:00 UTC to 23:59:59 UTC of a certain day. Documents in firebase have constraints as well so document ids were named to be in the format of (UTC day)_(index) where index is the ith document of that day. To fetch the cumulative portfolio data for a timeframe, we would fetch all documents that contained relevant data and then recombined such data to display on the frontend.
<center>
  <Image
    src="/projects/trenchtown/portfolioFetching.png"
    width="400"
    height="200"
    format="png"
    alt="Portfolio Fetching"
    class="image"
  />
  <p class="caption">Design of fetching portfolio data from Firebase</p>
</center>

Another unforseen challenge was Solana's incapability to retrieve archival data. The RPC getSignaturesForAddress() is unreliable and may return 0 signatures, skip over some signatures, or time out. This is because of Google BigTable query timing out but fetching older transactions also become longer to query as well. We solved this by implementing a Google Cloud Function to continously refetch data for a wallet until we were sure there were no more signatures to fetch.

# Prizes #
1. &nbsp;&nbsp;&nbsp;&nbsp;- Honorable Mention in Colosseum's Radar Hackathon (<a target="_blank" href="https://blog.colosseum.org/announcing-the-winners-of-the-solana-radar-hackathon/">Blog Post</a>)
2. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 13,671 participants, 156 countries, 1,359 final projects
3. &nbsp;&nbsp;&nbsp;&nbsp;- Awarded $7,500 in grant funding from Solana Foundation and Texas Blockchain Incubator Program
<br>

# Conclusion #
Much of this project has taught me a lot about the Solana blockchain and ecosystem. I've grown in my technical ability in both web2 and web3 aspects but I've also met a lot of new people because of this project. 

# Full Tech Stack #  
| Languages    | Libraries     | Tools     | Chains   |
| :----------- | :------------ | :-------- | :------- | 
| - TypeScript | - TailwindCSS | - Cursor  | - Solana |
| - HTML       | - React.js    | - Birdeye |          |
| - CSS        | - Helius SDK  | - Vercel  |          |
|              | - Raydium SDK |           |          |
|              | - Solana SDK  |           |          |
|              | - Web3js      |           |          |
|              | - Firebase    |           |          |