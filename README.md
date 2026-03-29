# CEX·DEX ARB SCANNER v4.2

Scanner de arbitraj CEX-DEX în timp real — 8 chains, 44 tokeni.

**Live:** https://alexisinvest2030.github.io/Dex-Cex-arbitraj/

## Surse prețuri
| Sursă | Ce acoperă | Endpoint |
|-------|-----------|----------|
| Binance WebSocket | Toate perechile | `wss://stream.binance.com` bookTicker |
| Jupiter Price API | Solana tokens | `price.jup.ag/v4` → `api.jup.ag/price/v2` |
| DeFiLlama (batch) | EVM chains | `coins.llama.fi` în batch de 10 |
| Pyth Hermes | SUI | `hermes.pyth.network/v2` |
| CoinGecko | Fallback universal | `api.coingecko.com` |

## Fix v4.2
- Jupiter: `quote-api.jup.ag` → `price.jup.ag` (DNS mai stabil)
- DeFiLlama: batch de 10 tokens (evită 414 URI Too Long)
- Waterfall complet pentru Solana: Jupiter → DeFiLlama Solana → CoinGecko
