import os
from solana.rpc.api import Client
from solana.account import Account

TELEGRAM_BOT_TOKEN = os.getenv("TELEGRAM_BOT_TOKEN")
TELEGRAM_CHAT_ID = os.getenv("TELEGRAM_CHAT_ID")
PHANTOM_KEYS = os.getenv("PHANTOM_KEYS", "").split(",")

WALLETS = []
for key in PHANTOM_KEYS:
    wallet_account = Account(bytes.fromhex(key))
    client = Client("https://api.mainnet-beta.solana.com")
    WALLETS.append({"account": wallet_account, "client": client})


