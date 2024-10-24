# BETSY

## Sports Betting DApp with XMTP, Skale Network, and RedPill API Integration

## Overview

This decentralized application (DApp) enables users to create and resolve sports bets utilizing blockchain technology. The platform integrates **XMTP** for real-time messaging, allowing users to communicate and place bets via group messaging channels. The betting interactions are executed on the **Skale Network**, providing a gas-free, scalable blockchain solution for secure transactions.

The application makes use of **Phala's RedPill API** for calling large language models (LLMs) to understand user betting prompts and match them with live sports data retrieved from **RapidAPI** (NBA data). The combination of these technologies delivers a smooth betting experience that is both AI-powered and blockchain-secure.

## Technologies Used

- **XMTP**: For secure, real-time messaging, allowing users to place and discuss bets within a group messaging environment.
- **Skale Network**: A gas-free, scalable blockchain that handles all smart contract interactions related to betting, such as creating and resolving bets.
- **Phala's RedPill API**: Used to call LLMs to understand natural language betting prompts and match them with relevant sports events.
- **RapidAPI**: Provides live sports data (NBA games), which is used to validate and match user bets with actual sports events in real-time.

## Usage

1. **Initialize Coinbase Wallet**: A group wallet is created using **Coinbase SDK** and is funded using a faucet. The wallet is used to interact with the smart contracts.

2. **Create a Bet**: Users can place a bet by typing a natural language prompt. The system processes the bet using OpenAI and checks the sports API for game validity.

3. **Finalize a Bet**: Once a bet is placed, it is recorded on the Skale network using the **createGame** method from the betting contract. USDC is approved and transferred from the user's wallet for the bet.

4. **Resolve a Bet**: When a game is completed, the outcome is fetched from the sports API, and the **resolveAndDistribute** method of the betting contract is called to distribute winnings based on the bet outcome.

## License

This project is licensed under the MIT License.
