# Alpha Vantage MCP 服务器 📈

[English](README.md) | 中文

一个模型上下文协议 (MCP) 服务器，提供与 Alpha Vantage 金融数据 API 的无缝集成，支持实时股票市场数据、加密货币价格、外汇汇率和技术指标。

## 🌟 功能特性

- **股票市场数据**: 实时报价、历史数据、公司信息
- **加密货币数据**: 实时加密货币价格和汇率
- **外汇交易**: 实时外汇汇率和货币转换
- **技术分析**: 高级指标、移动平均线、交易信号

## 🚀 快速开始

### 安装

无需安装！使用 npx 时包会自动下载并运行。

本地开发：
```bash
git clone https://github.com/jeasionr-ui/alpha-ventage-mcp.git
cd alpha-ventage-mcp
npm install
```

### 配置

在您的 MCP 设置文件中配置服务器：

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

## 🔑 API 密钥

在 [Alpha Vantage](https://www.alphavantage.co/support/#api-key) 注册获取 API 密钥。免费版包含：
- 每天 25 次 API 调用
- 实时和历史数据访问
- 全球市场覆盖

## 📝 许可证

MIT
