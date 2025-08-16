
# Telegram-Controlled Solana Trading Bot

## Setup Instructions

1. Deploy this repo to Railway (https://railway.app) or any Python cloud platform.
2. Set environment variables:
   - TELEGRAM_BOT_TOKEN=<Your Telegram Bot Token>
   - TELEGRAM_CHAT_ID=<Your Telegram Chat ID>
   - PHANTOM_KEYS=<Comma-separated Phantom wallet private keys>

3. Deploy and start the project. You should receive a Telegram alert:
   "🚀 Telegram-controlled Solana Trading Bot Started - Mainnet Ready"

## Commands via Telegram
- /start → Start trading
- /stop → Stop trading
- /status → Check wallet balances
- /portfolio → Check total portfolio value

## Notes
- Max simultaneous trades: 3
- Daily CU limit: 50,000
- Conditional holding: portfolio > $1,000,000
- Minimum balance to trade: $0.1
