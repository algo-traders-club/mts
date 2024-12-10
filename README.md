[![MTS - Matrix Trading System](./mts-logo.png)](./mts-logo.png)

# MTS - Matrix Trading System

An agentic crypto trading system for Hyperliquid.

## Overview

MTS uses a Matrix-inspired architecture with specialized agents:

- **Morpheus**: Risk Management Agent

  - Manages position sizing
  - Validates risk parameters
  - Protects your capital

- **Neo**: Pattern Recognition Agent

  - Detects market patterns
  - Processes market data
  - Makes trading decisions

- **Trinity**: Trade Execution Agent

  - Places orders
  - Manages positions
  - Handles trade lifecycle

- **Oracle**: Price Discovery Agent

  - Provides market prices
  - Calculates indicators
  - Predicts price movements

- **Tank**: System Operations Agent
  - Coordinates all agents
  - Monitors system health
  - Manages overall operations

## Installation

1. Clone the repository:

```bash
git clone https://github.com/algotraders/mts.git
cd mts
```

2. Install dependencies with Poetry:

```bash
poetry install
```

3. Configure your environment:

```bash
cp .env.example .env
# Edit .env with your credentials
```

4. Run the system:

```bash
poetry run python main.py
```

## Contributing Guidelines for ATC Learners

### 1. Start Small

- Begin with small improvements or bug fixes
- Comment your code clearly
- Test your changes before submitting

### 2. Development Flow

- Fork the repository
- Create a feature branch: `feature/your-feature-name`
- Write clear commit messages
- Submit a pull request with a description of your changes

### 3. Code Style

- Use single quotes for strings
- Follow PEP 8 guidelines
- Keep functions short and focused
- Add docstrings to functions and classes

### 4. Testing

- Always test your changes locally first
- Use small amounts when testing trading logic
- Start with paper trading before live trading

### 5. Learning Path

- Study existing agent implementations
- Start by improving documentation
- Move on to adding features to existing agents
- Finally, try creating new agents or strategies

## Project Structure

```
mts/
├── .env
├── pyproject.toml
├── README.md
├── main.py           # Main entry point
├── mts/
│   ├── __init__.py
│   ├── config.py
│   ├── agents/
│   │   ├── __init__.py
│   │   ├── morpheus.py  # Risk Management
│   │   ├── neo.py      # Pattern Recognition
│   │   ├── trinity.py  # Trade Execution
│   │   ├── oracle.py   # Price Prediction
│   │   └── tank.py     # System Operations
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── logger.py
│   │   └── validators.py
│   └── data/
│       ├── __init__.py
│       └── market_data.py
└── tests/
    └── __init__.py
```

## Configuration

Create a `.env` file with the following variables:

```
HYPERLIQUID_PRIVATE_KEY='your-private-key'
EXCHANGE_URL='https://api.hyperliquid.xyz'
RISK_PERCENTAGE=0.02
MAX_POSITIONS=3
DEFAULT_LEVERAGE=3
```

## ⚠️ Risk Disclaimer

THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. BY USING THIS SOFTWARE, YOU ACKNOWLEDGE AND ACCEPT THE FOLLOWING RISKS:

1. Trading cryptocurrency involves substantial risk of loss and is not suitable for all investors.

2. This software is for educational purposes only and should not be used as financial advice.

3. Software bugs, network issues, or other technical problems could lead to trading losses.

4. Market conditions can change rapidly and past performance does not guarantee future results.

5. Users are solely responsible for:
   - Validating the code
   - Testing strategies thoroughly
   - Managing their risk
   - Securing their API keys
   - Any financial losses incurred

USE THIS SOFTWARE AT YOUR OWN RISK. THE AUTHORS AND CONTRIBUTORS OF THIS PROJECT ACCEPT NO RESPONSIBILITY FOR ANY FINANCIAL LOSSES.

## Support

For help and discussions:

- Join our Discord server
- Check the [Wiki](https://github.com/algotraders/mts/wiki)
- Raise issues on GitHub

## License

© Copyright Algo Traders Club 2024 - MIT License
