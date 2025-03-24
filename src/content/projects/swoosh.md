---
title: "Swoosh - ETHDenver 2024"
description: "Swoosh is a decentralized payment and bill splitting application built on Ethereum. It allows users to easily send payments, request money from others, and split expenses using crypto. Made during ETHDenver's BUIDL Hackathon."
heroImage: "/projects/swoosh/hero.png"
pubDate: "Mar 1 2024"
badge: ""
tags: ["Web3", "Solidity"]
code: "https://github.com/sreeduggirala/swoosh"
demo: "https://swoosh-eth-denver.vercel.app/"
blog: "https://devfolio.co/projects/swoosh-d164"
---
# Background #
ETH Denver is one of, if not the largest crypto and web3 convention in North America. This is where many web3 companies come to showcase and present their projects to investors, developers, and enthusiasts. They also host a hackathon to allow developers to build on specific platforms or chains and to learn more about new technologies. As part of the Labs Division of Texas Blockchain, we came out to Denver to participate in the hackathon to win some bounties and meet different teams and companies.

# Purpose #
The purpose of Swoosh is to make it easier for friends, coworkers, or family to split bills without needing to calculate how much each person owes. It quickly simplifies a common problem that many of us have. On top of that, Swoosh allows direct and instant payment on the blockchain with little fees.

# Challenges #
1. &nbsp;&nbsp;&nbsp;&nbsp;1\. Connecting to SDKs
2. &nbsp;&nbsp;&nbsp;&nbsp;2\. Web3 Documentation

A challenge we faced when building Swoosh was connecting to the different APIs and SDKs required for the app to work. An example was connecting to the thirdweb account abstraction SDK and having the buttons to open a modal made by thirdweb work properly. As we were working on our project, the button to allow the user to sign up with Google, Apple, or Facebook started erroring out when it was pressed, ultimately crashing the application for that user. This was nearing the end of the BUIDL hackathon which was rather upsetting to see as we weren't able to find a solution before submissions were closed. Despite this, we were still able to showcase the main funcitonality of our app to different companies and panels with no problem.

Another challenge we faced was the lack of clear and concise documentation for developers that were completely new to the ecosystem or its tools. We found this to be a common problem among most SDKs as naturally, these products are constantly changing and documentation often lags far behind to match the current state of the product. This made it hard to use some new tools that we were using to build our app and led to constant trial and error in order to get adequate integration.  

# Prizes #
1. &nbsp;&nbsp;&nbsp;&nbsp;- Best Solana DeFi/Payments Integration (<a target="_blank" href="https://twitter.com/solana_devs/status/1769766724411232680?t=9CzhNLP6RssQFRWgDHxRdg">Twitter Post</a>)
2. &nbsp;&nbsp;&nbsp;&nbsp;- Most creative BUIDL using XDC network  
<br>

# Full Tech Stack #  
| Languages    | Libraries      | Tools     | Chains              |
| :----------- | :------------- | :-------- | :------------------ | 
| - TypeScript | - TailwindCSS  | - Foundry | - Solana (Neon EVM) |
| - Solidity   | - React.js     | - VSCode  | - Base              |
| - JavaScript | - thirdWeb SDK | - Vercel  | - XDC               |
| - CSS        |                |           | - Injective (inEVM) |
|              |                |           | - Linea             |
|              |                |           | - Arbitrum          |
|              |                |           | - Hedera            |