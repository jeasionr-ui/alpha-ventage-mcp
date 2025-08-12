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

#### 通过 Smithery 安装

通过 [Smithery](https://smithery.ai/server/@deepsuthar496/alpha-ventage-mcp) 自动为 Claude Desktop 安装 Alpha Vantage 金融数据服务器：

```bash
npx -y @smithery/cli install @deepsuthar496/alpha-ventage-mcp --client claude
```

### 手动安装

1. 克隆仓库：
```bash
git clone https://github.com/jeasionr-ui/alpha-ventage-mcp
cd alpha-ventage-mcp
```

2. 安装依赖：
```bash
npm install
```

3. 构建服务器：
```bash
npm run build
```

### 配置

在您的 MCP 设置文件中配置服务器：

```json
{
  "mcpServers": {
    "alpha-vantage": {
      "command": "node",
      "args": ["https://github.com/jeasionr-ui/alpha-ventage-mcp/blob/main/build/index.js"],
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
