# Synthelix Auto Bot

**Automated tool for managing Synthelix nodes across multiple wallets**

## 🌟 Features

- 👛 Manage multiple Ethereum wallets from a single script
- 🚀 Auto-start nodes for maximum uptime
- 💎 Auto-claim daily rewards
- 📊 Monitor node status, uptime, and points
- 🔄 Auto-restart nodes when needed
- 🌐 Proxy support for better stability and multiple accounts
- 🏃‍♂️ Run & forget with automatic monitoring

## 📋 Prerequisites

- Node.js (v14+)
- NPM or Yarn
- Ethereum wallet private key(s)
- Optional: Proxy list for managing multiple accounts

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/airdropinsiders/Synthelix-Auto-Bot.git
cd Synthelix-Auto-Bot
```

2. Install dependencies:
```bash
npm install
```

3. Set up your environment:
```bash
cp .env.example .env
```

4. Edit the `.env` file with your private key(s):
```
# Single wallet
PRIVATE_KEY=your_private_key_here

# Multiple wallets (comma separated)
PRIVATE_KEY=key1,key2,key3

# OR multiple wallets (numbered)
PRIVATE_KEY_1=key1
PRIVATE_KEY_2=key2
PRIVATE_KEY_3=key3
```

5. (Optional) Set up proxies:
   - Create a file named `proxies.txt`
   - Add one proxy per line in any of these formats:
     ```
     http://username:password@host:port
     socks5://username:password@host:port
     host:port
     ```

## 🏃‍♂️ Usage

Start the bot:
```bash
npm start
```

The bot will:
1. Log in to each wallet in sequence
2. Start nodes if they're not running
3. Claim daily rewards if available
4. Monitor and restart nodes as needed
5. Display status information and points earned

## ⚙️ Configuration

Edit the following constants in `index.js` to adjust behavior:

```javascript
const DELAY_BETWEEN_WALLETS = 2000; // Delay between wallet operations (ms)
const MAX_RETRIES = 3;              // Max login retry attempts
const CHECK_INTERVAL = 60 * 1000;   // Status check interval (ms)
```

## 📝 Logs

The bot provides colored console output showing:
- Wallet connection status
- Node operations (start/stop)
- Points earned
- Error messages
- Summary statistics

## 🔒 Security

- Your private keys are stored locally in the `.env` file
- Never share your `.env` file or private keys
- Consider using a dedicated wallet with limited funds for added security

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## ⚠️ Disclaimer

This tool is provided for educational purposes only. Use at your own risk. The creators of this tool are not responsible for any potential losses or issues that may arise from its use.

## 💬 Support

Join our community:
- [Discord](https://discord.gg/tmrBhAxU)
- [Telegram](https://t.me/AirdropInsiderID)