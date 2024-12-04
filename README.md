## MTS - Matrix Trading System

An agentic framework for algorithmic trading on [Hyperliquid](https://app.hyperliquid.xyz/trade).

### Toolbelt

- [x] [Hyperliquid API](https://hyperliquid.gitbook.io/hyperliquid-docs) - DEX
- [x] [Python](https://www.python.org/) - Language
- [x] [Cursor](https://www.cursor.com/) - IDE
- [x] [ChatGPT](https://chatgpt.com/) - LLM
- [x] [ClaudeAI](https://claude.ai/) - LLM

### Hyperliquid Data

#### Historical data

Historical data is zipped using LZ4 compression format and uploaded to S3 in the bucket hyperliquid-archive approximately once a month

#### Market data

Format: `s3://hyperliquid-archive/market_data/[date]/[hour]/[datatype]/[coin].lz4`

If you have installed AWS CLI see [Getting Started](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) and LZ4 see [LZ4](https://github.com/lz4/lz4) or install from your package manager, then you can read the files as follows:

```
aws s3 cp s3://hyperliquid-archive/market_data/20230916/9/l2Book/SOL.lz4 /tmp/SOL.lz4 --no-sign-request
unlz4 --rm /tmp/SOL.lz4
head /tmp/SOL
```

#### Asset metadata snapshots

Format: `s3://hyperliquid-archive/asset_ctxs/[date].csv.lz4`

© Copyright 2024 Algo Traders Club - MIT License
