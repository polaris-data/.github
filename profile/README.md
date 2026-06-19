# Polaris

Polaris is a market data platform for emerging frontier markets, built for quantitative research, backtesting, and modelling.

We capture exchange-native data directly from venues such as Hyperliquid and Lighter, exposing normalized datasets alongside raw venue payloads.

### For terminal users

Install the [CLI](https://github.com/polaris-data/cli):

```bash
curl -fsSL https://raw.githubusercontent.com/polaris-data/cli/main/install.sh | bash
```

Browse and download available datasets via TUI:

```bash
polaris
```

### For Python users

Query the last 7 days of events with the [Python SDK](https://github.com/polaris-data/polaris-py):

```python
from polaris_data import PolarisClient

with PolarisClient() as client:
    rows = client.events(exchange="hyperliquid", asset="BTC")
    print(len(rows))
```

See the [docs](https://polaris.supply/docs) for API usage, authentication, and SDK guides, or read [llms.txt](https://polaris.supply/llms.txt) for the compact LLM-facing version.
