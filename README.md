

# OpenSCI Auto Bot

The **OpenSCI Auto Bot** is an automated tool designed to simplify interactions with OpenSCI smart contracts on the **Base Sepolia testnet**. It enables users to claim tokens from faucets and vote on OpenSCI projects effortlessly, making it ideal for testing and automation purposes.

## Features

- **Token Claiming**: Automatically claim tokens from OpenSCI faucets.
- **Project Voting**: Vote on specific OpenSCI projects with customizable token distributions.
- **Multi-Account Support**: Manage multiple accounts using private keys.
- **Proxy Support**: Rotate IP addresses with proxy integration for enhanced privacy.
- **Auto-Retry Mechanism**: Retry failed transactions automatically.
- **Token Balance Checking**: View token balances for your accounts.
- **Scheduled Operations**: Automate tasks on a daily schedule.

## Prerequisites

Before you begin, ensure you have the following:

- **[Node.js](https://nodejs.org/)** (version 14 or higher)
- **[npm](https://www.npmjs.com/)** (Node Package Manager)
- **Base Sepolia ETH** for gas fees (available via testnet faucets)

## Installation

Follow these steps to set up the OpenSCI Auto Bot:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/airdropinsiders/OpenSCI-Auto-Bot.git
   cd OpenSCI-Auto-Bot
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Set Up Configuration Files**:
   - Create a file named `pk.txt` and add your private keys (one per line).
   - (Optional) Create a file named `proxies.txt` and add your proxies (one per line).

### Configuration Files

- **`pk.txt`**:
  Add one private key per line in hexadecimal format. Example:
  ```
  0x123abc...
  0x456def...
  ```

- **`proxies.txt`** (Optional):
  Add one proxy per line in any of these supported formats:
  ```
  ip:port
  username:password@ip:port
  http://ip:port
  http://username:password@ip:port
  socks5://username:password@ip:port
  ```

## Usage

Start the bot by running:
```bash
npm start
```

This launches an interactive menu with the following options:

1. **Claim Tokens from Faucet**: Automatically request tokens from the OpenSCI faucet.
2. **Vote on Projects**: Cast votes for predefined OpenSCI projects.
3. **Both Claim Tokens and Vote**: Execute both actions sequentially.
4. **Check Balances**: Display the token balances of your accounts.
5. **Schedule Daily Operations**: Configure the bot for automated daily runs.
6. **Exit**: Shut down the bot.

## Contract Addresses

The bot interacts with the following OpenSCI contracts on the Base Sepolia testnet:

- **Voting Contract**: `0x672e69f8ED6eA070f5722d6c77940114cc901938`
- **Faucet Contract**: `0x43808E0766f88332535FF8326F52e4734de35F0e`
- **Voting Token**: `0x3E933b66904F83b6E91a9511877C99b43584adA3`

## Vote Distribution

The bot comes pre-configured to allocate tokens to the following projects:

- `0xe5d033db611ae3f5682ace7285860a6ceb1195d5f80f2721a82d4baff67daddb`: **4 tokens**
- `0xb99bb4429ce45c2cf000bc98f847741c88603e234f6099d78fe47c2b50738776`: **2 tokens**
- `0x8689005e34728a5f6027d7c12bd49ef51fa54d62971bf6e5490fbaaaf85a1e21`: **2 tokens**
- `0xf712336c9a04915c7b25b30412d0fb8613a417cd8a94f00ca0b2da73e1704949`: **2 tokens**

## Security Notice

To ensure safe usage, follow these guidelines:

- **Protect Your Private Keys**: Never share them with anyone.
- **Start Small**: Test the bot with minimal token amounts initially.
- **Use a Dedicated Wallet**: Avoid using your primary wallet for bot operations.
- **Ensure Sufficient Gas**: Keep enough Base Sepolia ETH in your wallet for transaction fees.

## License

This project is licensed under the **MIT License**.

## Disclaimer

The OpenSCI Auto Bot is provided for **educational purposes only**. Use it at your own risk. The authors are not liable for any loss of funds or damages resulting from its use.

