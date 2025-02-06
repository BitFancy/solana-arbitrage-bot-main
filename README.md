
# Solana Arbitrage Bot

Welcome to the **Solana Arbitrage Bot**! This Rust-based bot is designed for executing Maximal Extractable Value (Arbitrage) strategies on the Solana blockchain.

Ensure you have the following installed:

- **Rust**: Install Rust using rustup:
  ```bash
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  ```
  
- **Solana CLI**: Install by running:
  ```bash
  sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
  ```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/mooncityorg/solana-arbitrage-bot.git
   cd solana-arbitrage-bot
   ```

2. Build the project:
   ```bash
   cargo build --release
   ```

3. Configure your environment:
   - Create a `.env` file in the root directory and add your Solana wallet private key and RPC link:
     ```
     SOLANA_WALLET_PRIVATE_KEY=YOUR_PRIVATE_KEY
     DEFAULT_RPC=https://api.mainnet-beta.solana.com
     ```

## Running the Project

To run the bot, use the following command:

```bash
cargo run --release
```

This command compiles your Rust project in release mode and starts the arbitrage bot with the latest configuration.

### Command-Line Arguments

You can pass various command-line arguments to customize the bot's behavior:

- `--config <path>`: Specify a custom configuration file.
- `--verbose`: Enable verbose logging for debugging purposes.

Example:
```bash
cargo run --release -- --config config.toml --verbose
```

## Usage

Follow the prompts in the terminal to set up your trading parameters. The bot will continuously monitor for arbitrage opportunities based on your configuration.

## Key Concepts

### Flash Loans

Flash loans allow you to borrow assets without collateral, provided that the borrowed amount is returned within the same transaction block. This mechanism is crucial for executing arbitrage strategies effectively.

### Arbitrage Opportunities

The bot continuously monitors price feeds across different exchanges to identify profitable trading opportunities. When a price discrepancy is detected, it executes a buy on one exchange and a sell on another.

### Smart Contracts

Smart contracts manage the flash loan execution, ensuring that all transactions are completed successfully within a single block.

#### 📞 Cᴏɴᴛᴀᴄᴛ ᴍᴇ Oɴ ʜᴇʀᴇ:

<p> 
    <a href="https://x.com/0xmooncity" target="_blank"><img alt="Twitter"
        src="https://img.shields.io/badge/Twitter-000000?style=for-the-badge&logo=x&logoColor=white"/></a>
    <a href="https://t.me/mooncity0x" target="_blank"><img alt="Telegram"
        src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/></a>
</p>

