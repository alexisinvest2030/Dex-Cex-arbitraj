# CEX·DEX ARB SCANNER v4.4

**Live:** https://alexisinvest2030.github.io/Dex-Cex-arbitraj/

## Fix v4.4
| Bug | Cauza | Fix |
|-----|-------|-----|
| `price.jup.ag ERR_NAME_NOT_RESOLVED` | DNS instabil | Eliminat complet — DeFiLlama Solana mint primar |
| `POL = $0.20` aberant | CC `MATIC` simbol deprecated | CC_SYM fix + validare ratio vs Binance WS |
| Favicon 404 | Lipsea | Adăugat inline SVG favicon |

## Surse prețuri (toate cu CORS open)
| Sursa | Acoperire |
|-------|-----------|
| Binance WebSocket bookTicker | CEX bid/ask real-time |
| DeFiLlama `solana:MINT` | Solana DEX prices |
| DeFiLlama `chain:address` batch 8 | EVM DEX prices |
| Pyth Hermes | SUI oracle |
| CryptoCompare | Fallback universal + validare |
