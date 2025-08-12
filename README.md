# Alpha Vantage MCP Server

[English](README.md) | [中文](README.zh.md)

A Model Context Protocol (MCP) server that provides access to Alpha Vantage financial data APIs. This server enables AI assistants to fetch real-time and historical financial market data including stock prices, forex rates, cryptocurrency data, and various technical indicators.

## ✨ Features

- **Real-time Stock Data**: Get current stock prices, quotes, and market information
- **Historical Data**: Access historical stock prices and trading volumes
- **Technical Indicators**: Calculate various technical analysis indicators (SMA, EMA, RSI, MACD, etc.)
- **Forex Data**: Real-time and historical foreign exchange rates
- **Cryptocurrency**: Digital currency prices and market data
- **Company Information**: Fundamental data, earnings, and company overviews
- **Market News**: Latest financial news and market sentiment

## 🚀 Quick Start

### Prerequisites

- Node.js 16+ installed
- Alpha Vantage API key (get one free at [Alpha Vantage](https://www.alphavantage.co/support/#api-key))

### Installation

No installation required! The package will be downloaded and run automatically using npx.

For local development:
```bash
git clone https://github.com/jeasionr-ui/alpha-ventage-mcp.git
cd alpha-ventage-mcp
npm install
```

## ⚙️ Configuration

### Configuration

Configure the server in your MCP settings file:

```json
{
  "mcpServers": {
    "alpha-vantage": {
      "command": "npx",
      "args": ["alpha-ventage-mcp"],
      "env": {
        "ALPHA_VANTAGE_API_KEY": "your-api-key-here"
      },
      "disabled": false,
      "alwaysAllow": []
    }
  }
}
```

## 🔑 API Key

Get your free Alpha Vantage API key:
1. Visit [Alpha Vantage](https://www.alphavantage.co/support/#api-key)
2. Sign up for a free account
3. Copy your API key
4. Add it to your environment variables or MCP configuration

## 📊 Available Tools

### Stock Data
- `get_stock_quote` - Get real-time stock quote
- `get_stock_intraday` - Get intraday stock data
- `get_stock_daily` - Get daily stock prices
- `get_stock_weekly` - Get weekly stock prices
- `get_stock_monthly` - Get monthly stock prices

### Technical Indicators
- `get_sma` - Simple Moving Average
- `get_ema` - Exponential Moving Average
- `get_rsi` - Relative Strength Index
- `get_macd` - Moving Average Convergence Divergence
- `get_bollinger_bands` - Bollinger Bands
- `get_stochastic` - Stochastic Oscillator

### Forex & Crypto
- `get_forex_rate` - Real-time forex exchange rates
- `get_crypto_rating` - Cryptocurrency ratings
- `get_crypto_intraday` - Intraday crypto data

### Company Information
- `get_company_overview` - Company fundamental data
- `get_earnings` - Quarterly and annual earnings
- `search_symbol` - Search for stock symbols

### Market News
- `get_news_sentiment` - Market news and sentiment analysis

## 🛠️ Development

### Building
```bash
npm run build
```

### Testing
```bash
# Test with environment variable
ALPHA_VANTAGE_API_KEY=your_key_here node build/index.js
```

## 📝 Example Usage

Once configured, you can ask your AI assistant questions like:

- "What's the current stock price of AAPL?"
- "Show me the RSI for Tesla stock"
- "Get the latest earnings for Microsoft"
- "What's the EUR/USD exchange rate?"
- "Show me Bitcoin's price trend today"

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - see LICENSE file for details.

## 🔗 Links

- [Alpha Vantage API Documentation](https://www.alphavantage.co/documentation/)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [MCP Specification](https://spec.modelcontextprotocol.io/)
