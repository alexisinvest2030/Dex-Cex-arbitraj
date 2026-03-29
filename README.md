# CEX·DEX ARB SCANNER v4.3

**Live:** https://alexisinvest2030.github.io/Dex-Cex-arbitraj/

## Fix v4.3 — rezolvat CORS GitHub Pages
| API | Status | Motiv |
|-----|--------|-------|
| Binance WebSocket | ✅ OK | WS nu are CORS |
| CryptoCompare | ✅ OK | CORS `*`, înlocuiește CoinGecko |
| DeFiLlama | ✅ OK | CORS `*` |
| Jupiter price.jup.ag | ✅ OK | CORS `*` |
| Pyth Hermes | ✅ OK | CORS `*` |
| ~~CoinGecko free~~ | ❌ BLOCAT | CORS blocat din 2024 |

## Arhitectura
- **CEX prices**: Binance WebSocket bookTicker (bid/ask real)
- **SOL**: price.jup.ag → DeFiLlama Solana mint → CryptoCompare
- **EVM**: DeFiLlama on-chain (batch 8) → CryptoCompare  
- **SUI**: Pyth Hermes oracle → CryptoCompare
- **Fallback**: CryptoCompare (250k calls/luna gratuit, CORS open)
