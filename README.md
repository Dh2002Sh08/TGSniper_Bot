# Sniper Bot - Multi-Chain Telegram Trading Bot

## 🚀 Overview

Sniper Bot is a multi-chain trading bot with a Telegram interface, supporting Ethereum (ETH), Binance Smart Chain (BSC), and Solana (SOL). It automatically detects and snipes new tokens using advanced filtering, honeypot detection, and customizable trading strategies. All interactions are managed via Telegram for ease of use.

---

## 🛠️ Features
- **Multi-chain support:** ETH, BSC, SOL
- **Telegram interface:** Manage wallets, configure trading, and monitor snipes via Telegram
- **Automatic token detection:** Filters out stablecoins, suspicious tokens, and honeypots
- **Customizable trading config:** Set slippage, stop loss, take profit, and more
- **Paper trading mode:** Test strategies risk-free
- **Wallet management:** Create, import, and manage wallets for all supported chains

---

## ⚡ Quick Start

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd tgbot
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Up Environment Variables
Create a `.env` file in the root directory with the following content:

```env
# Telegram Bot Token (from @BotFather)
TELEGRAM_BOT_TOKEN=your_telegram_bot_token

# QuickNode API Key (for ETH/BSC WebSocket & RPC)
QUICKNODE_KEY=your_quicknode_api_key

# Shyft API Key (for Solana)
SHYFT_KEY=your_shyft_api_key

BSC_RPC_URL=your_bsc_rpc
ETH_RPC_URL=your_eth_rpc
SOL_RPC_URL=your_sol_rpc
OWNER_CHAT_ID=your_chat_id

# Optional: GoPlus API Key (for enhanced honeypot detection)
GOPLUS_API_KEY=your_goplus_api_key
```

- Get your Telegram bot token from [@BotFather](https://t.me/BotFather)
- Get QuickNode and Shyft API keys from their respective services

### 4. Build the Project (if using TypeScript)
```bash
npm run build
```

### 5. Start the Bot
```bash
npm start
```
Or for development with auto-reload:
```bash
npm run dev
```

---

## 🤖 Using the Sniper Bot via Telegram

1. **Start the Bot:**
   - Open Telegram and search for your bot (the username you set with BotFather)
   - Send `/start` to begin

2. **Create or Import Wallets:**
   - Use the menu or commands to create wallets for ETH, BSC, and SOL
   - You can also import existing wallets using private keys (keep them secure!)

3. **Configure Trading Settings:**
   - Set your buy amount, slippage, stop loss, and take profit via the Telegram interface
   - Example: Use `/config` or the settings menu

4. **Start Sniping:**
   - Use the inline button or menu to start the Sniper Bot
   - The bot will monitor for new tokens and attempt to snipe based on your config

5. **Monitor and Manage:**
   - View sniped tokens, wallet balances, and trading history
   - Stop the bot anytime with the menu or `/stop`

6. **Paper Trading:**
   - Test your strategies risk-free using the paper trading mode

---

## 🧩 Advanced Configuration

- **Validation Criteria:**
  - Minimum liquidity, volume, token age, and honeypot detection can be customized
  - Use the settings menu in Telegram to adjust these

- **Trade Limits:**
  - Set daily trade limits to manage risk

- **Token Filtering:**
  - The bot automatically excludes stablecoins and suspicious tokens

---

## 🔒 Security & Best Practices
- **Never share your private keys** with anyone
- Use a dedicated wallet for trading (not your main wallet)
- Store your `.env` file securely and never commit it to version control
- Be aware of API rate limits and network fees

---

## 🐞 Troubleshooting
- **Bot not responding?**
  - Check your `.env` file for correct API keys and bot token
  - Ensure all dependencies are installed (`npm install`)
  - Make sure your Telegram bot is started and not blocked
- **Wallet issues?**
  - Double-check private keys when importing
  - Ensure you have enough funds for gas/fees
- **API errors?**
  - Verify your QuickNode and Shyft API keys are valid and not rate-limited

---

## 📝 Example .env File
```env
TELEGRAM_BOT_TOKEN=123456789:ABCdefGHIjklMNOpqrSTUvwxYZ
QUICKNODE_KEY=your_quicknode_key
SHYFT_KEY=your_shyft_key
GOPLUS_API_KEY=your_goplus_key
BSC_RPC_URL=your_bsc_rpc
ETH_RPC_URL=your_eth_rpc
SOL_RPC_URL=your_sol_rpc
OWNER_CHAT_ID=your_chat_id
```

---

## 📚 More Information
- **Dependencies:** See `package.json` for all required packages
- **Customization:** Explore the `lib/` and `utils/` directories for advanced features
- **Enhanced Token Scanner:** See `ENHANCED_SCANNER_README.md` for details on token filtering and honeypot detection

---

## 🏆 Credits
- Built with [Telegraf](https://telegraf.js.org/), [ethers.js](https://docs.ethers.org/), [web3.js](https://web3js.readthedocs.io/), [Solana Web3](https://solana-labs.github.io/solana-web3.js/), and more

---

## ⚠️ Disclaimer
This software is for educational and research purposes only. Use at your own risk. The authors are not responsible for any financial losses or damages.
