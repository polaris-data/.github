# Polaris

Polaris is a market data platform for emerging frontier markets, built for quantitative research, backtesting, and modelling.

We capture exchange-native data directly from venues such as Hyperliquid and Lighter, exposing normalized datasets (trades, L2 orderbook snapshots, OHLCV candles etc.) alongside raw venue payloads.

## Start here

- Docs: [polaris.supply/docs](https://polaris.supply/docs)
- CLI: [polaris-data/cli](https://github.com/polaris-data/cli)
- Python SDK: [polaris-data/polaris-py](https://github.com/polaris-data/polaris-py)

## Quickstart

Install the CLI:

```bash
curl -fsSL https://raw.githubusercontent.com/polaris-data/cli/main/install.sh | bash
```

Browse available datasets via TUI:

```bash
polaris
```

Query Polaris from Python:

```python
from polaris_data import PolarisClient

with PolarisClient() as client:
    rows = client.events(
        exchange="hyperliquid",
        asset="BTC",
        from_="2026-06-17T00:00:00Z",
        to="2026-06-18T01:00:00Z",
    )
    print(len(rows))
```

See the [docs](https://polaris.supply/docs) for API usage, authentication, and SDK guides.
