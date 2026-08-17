# tradingbot-web

Mobile-first monitoring + control page for the Alpaca paper-trading bot.
Single static `index.html`; data via Supabase (`tb_*` tables). Deploy on
Cloudflare Pages / GitHub Pages — no build step.

- Reads: status, positions, signals (with the trader card), closed trades, watchlist.
- Writes (passcode-gated via RLS): watchlist add/pause/remove, kill switch / flatten / release commands.
- The bot polls the watchlist every ~2 min and commands every 30 s.
