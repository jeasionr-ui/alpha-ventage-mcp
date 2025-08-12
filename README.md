# Alpha Vantage MCP Server 📈

English | [中文](README.zh.md)

A Model Context Protocol (MCP) server that provides seamless integration with Alpha Vantage's financial data API, enabling real-time stock market data, cryptocurrency prices, forex rates, and technical indicators.

## 🌟 Features

- **Stock Market Data**: Real-time quotes, historical data, company information
- **Cryptocurrency Data**: Real-time crypto prices and exchange rates
- **Forex Trading**: Live foreign exchange rates and currency conversions
- **Technical Analysis**: Advanced indicators, moving averages, trading signals

## 🚀 Quick Start

### Installation

#### Installing via Smithery

To install Alpha Vantage Financial Data Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@deepsuthar496/alpha-ventage-mcp):

```bash
npx -y @smithery/cli install @deepsuthar496/alpha-ventage-mcp --client claude
```

### Manual Installation

1. Clone the repository:
```bash
git clone https://github.com/jeasionr-ui/alpha-ventage-mcp
cd alpha-ventage-mcp
```

2. Install dependencies:
```bash
npm install
```

3. Build the server:
```bash
npm run build
```

### Configuration

Configure the server in your MCP settings file:

#### Option 1: Using npx (Recommended)
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

#### Option 2: Local Installation
```bash
# Clone and build locally
git clone https://github.com/jeasionr-ui/alpha-ventage-mcp.git
cd alpha-ventage-mcp
npm install
npm run build
```

Then configure with local path:
```json
{
  "mcpServers": {
    "alpha-vantage": {
      "command": "node",
      "args": ["/path/to/alpha-ventage-mcp/build/index.js"],
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

Sign up for an API key at [Alpha Vantage](https://www.alphavantage.co/support/#api-key). Free tier includes:
- 25 API calls per day
- Real-time and historical data access
- Global market coverage

## 📝 License

MIT
