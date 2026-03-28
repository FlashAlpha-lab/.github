# FlashAlpha

**Real-time options exposure analytics**

The FlashAlpha API delivers institutional-grade options analytics over a simple REST interface. Compute dealer positioning, Black-Scholes greeks, implied volatility, and vol surfaces for US equities — in milliseconds.

[![PyPI](https://img.shields.io/pypi/v/flashalpha)](https://pypi.org/project/flashalpha/)
[![Python](https://img.shields.io/pypi/pyversions/flashalpha)](https://pypi.org/project/flashalpha/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## What the API provides

| Category | Endpoints |
|---|---|
| Exposure analytics | GEX, DEX, VEX, CHEX by strike; key levels (gamma flip, call/put walls, max pain); exposure summary |
| Market data | Stock quotes, option quotes with greeks, vol surface, option chains |
| Pricing | Black-Scholes greeks (first, second, third order), implied volatility |
| Volatility | ATM IV, skew, term structure, realized vol, IV/RV spread |
| Sizing | Kelly criterion position sizing |
| Narrative | AI-generated regime and outlook analysis |
| Historical | Minute-level stock and option quotes from ClickHouse |

---

## Quick start

```bash
pip install flashalpha
```

```python
from flashalpha import FlashAlpha

fa = FlashAlpha("YOUR_API_KEY")

gex = fa.gex("SPY")
print(f"Net GEX: ${gex['net_gex']:,.0f}")
print(f"Gamma flip: {gex['gamma_flip']}")
```

---

## Free tier

10 requests/day — no credit card required. Includes GEX, DEX, VEX, CHEX, key levels, greeks, IV, and stock quotes.

Get your API key at **[flashalpha.com](https://flashalpha.com)**.

---

## Links

- [flashalpha.com](https://flashalpha.com) — API keys, docs, pricing
- [flashalpha.com/docs](https://flashalpha.com/docs) — API documentation
- [PyPI: flashalpha](https://pypi.org/project/flashalpha/) — Python SDK
