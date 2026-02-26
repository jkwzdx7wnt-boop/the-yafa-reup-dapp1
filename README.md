<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>THE YAFA REUP • $YAFAREUP</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body { background: linear-gradient(135deg, #0a001f, #1a0033); color: #e0e0ff; font-family: system-ui, sans-serif; }
    .hero { background: linear-gradient(90deg, #ff00aa, #00ffff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    .neon { text-shadow: 0 0 20px #00ffff, 0 0 40px #ff00aa; }
    .card { background: rgba(255,255,255,0.05); backdrop-filter: blur(12px); border: 1px solid rgba(100,150,255,0.2); }
  </style>
</head>
<body class="min-h-screen">
  <div class="max-w-4xl mx-auto px-6 py-16 text-center">
    <h1 class="text-6xl md:text-7xl font-bold hero neon mb-4">THE YAFA REUP</h1>
    <p class="text-3xl text-cyan-300">IT’S ALL ABOUT THE YAFA 🤴🏾</p>

    <div class="card rounded-3xl p-10 my-12">
      <h2 class="text-4xl font-bold mb-6">Buy $YAFAREUP</h2>
      <div class="bg-black/60 rounded-2xl p-5 font-mono text-sm break-all mb-8">
        HNvFVYzN5eqBacybyzkEVwEnqZxUozexvjgLjdAJ6iki
      </div>
      <button onclick="window.open('https://jupiter.ag','_blank')" class="bg-gradient-to-r from-pink-500 to-cyan-500 px-10 py-5 rounded-full text-xl font-semibold mx-2">BUY ON JUPITER</button>
      <button onclick="window.open('https://raydium.io/swap/','_blank')" class="bg-gradient-to-r from-purple-500 to-pink-500 px-10 py-5 rounded-full text-xl font-semibold mx-2">TRADE ON RAYDIUM</button>
    </div>

    <div class="card rounded-3xl p-10 my-12">
      <h2 class="text-4xl font-bold mb-6">Backend & Strategy</h2>
      <p class="text-xl">Full technical backend strategy and private bot setup documented here</p>
      <a href="BACKEND-STRATEGY.md" class="text-cyan-400 underline text-lg mt-4 inline-block">View Full Backend Strategy →</a>
    </div>

    <footer class="mt-16 text-sm text-gray-500">
      Fair launch • No presale • Real dev • Additional wallets added later
    </footer>
  </div>
</body>
</html>
# $YAFAREUP Backend Strategy

**Overview**
The backend is 100% private (never in public GitHub). It handles:
- Treasury fee collection & auto-buy $GODSKING
- 14 hot wallet management
- Annual 7% burn execution
- Admin dashboard communication

**Architecture**
- Flask Python API (lightweight, easy to host)
- Environment variables only for private keys (never committed)
- Jupiter API for swaps (Treasury → $GODSKING)
- Cron/scheduler for July 26 burn

**Core Components**
1. **Treasury Flow**
   - 7% tax lands in Master Treasury wallet automatically (Token-2022 fee)
   - Bot checks balance every 30 min
   - 50% swapped to $GODSKING via Jupiter (one-click or automated)

2. **Hot Wallet Management**
   - 14 wallets loaded from .env
   - Used for trading, liquidity adds, giveaways
   - Keys stored only on private server / Render secrets

3. **Annual Burn**
   - Separate script runs on July 26 (cron job)
   - 7% of current supply burned from main holding wallet
   - Liquidity safety check before burn

4. **Admin Dashboard Connection**
   - Frontend admin.html sends POST to /update_params
   - Updates trade amount, AI mode, etc. in real time

**Deployment (Recommended – Free Tier)**
1. Go to render.com → New Web Service
2. Connect your private GitHub repo (or upload files manually)
3. Set environment variables (all 14 PRIVATE_KEY_1 to PRIVATE_KEY_14 + RPC URL)
4. Add Cron job for annual burn (July 26 every year)
5. Use Helius or QuickNode RPC for production speed

**Security Rules**
- Keys NEVER in public repo
- All keys in Render secrets / .env (gitignore)
- Admin password protected
- Bot runs with minimal permissions

**Future Upgrades**
- Full claim site for holders rewards
- Telegram bot notifications
- P2E game treasury integration
- Multi-sig for large burns

This backend keeps everything transparent on-chain while giving you full private control.
# THE YAFA REUP – $YAFAREUP

Official public landing page.

Live: https://yourusername.github.io/the-yafa-reup-dapp

Full backend strategy (private bot, treasury buys, annual burn) → see BACKEND-STRATEGY.md
.env
.env.*
*.key
*.secret
.DS_Store

