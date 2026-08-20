# Crypto & 金融服务全平台分流规则集

本仓库提供主流加密货币交易所、数字银行、跨境汇款及 Web3 虚拟发卡平台的分流规则。所有规则独立拆分维护，内置核心 API、CDN 静态加速及 KYC 人脸识别与安全风控组件依赖。

---

## 规则订阅列表与推荐节点策略

| 规则名称 | 适用平台 | 推荐策略组 / 节点 | 核心避坑说明 | GitHub Raw 订阅链接 |
| :--- | :--- | :--- | :--- | :--- |
| **Binance** | 币安交易所 | **Taiwan** / 日本 | 无衍生品限制，避开美区/港区限制 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules` |
| **OKX** | 欧易交易所 | **Taiwan** / 日本 | 严禁美区 IP；台湾节点体验最佳 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules` |
| **Bybit** | Bybit 交易所 | **Taiwan** / 日本 | 避开美区、新加坡等受限地区 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules` |
| **Gate** | 芝麻开门 | **Taiwan** / 日本 | 避开美区与加拿大合规受限区 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules` |
| **Wise** | Wise 跨境汇款 | **Taiwan** / 注册地 | 保持固定节点，切忌频繁跳国家 IP | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules` |
| **iFAST** | 英国奕丰银行 | **United Kingdom** | 必须使用英国本地原生节点，防异地风控 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules` |
| **BiyaPay** | 跨境出入金/证券 | **Hong Kong** / 台湾 | 亚太节点延迟低，出入金流畅 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules` |
| **PokePay** | Web3 虚拟卡 | **Hong Kong** / 台湾 | 平台属地亚太，避开纯美区 IP | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules` |
| **MPChat** | 名品聊 IM 通讯 | **Hong Kong** / 台湾 | 即时通讯低延迟优先 | `https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules` |

> **国内加速镜像**：若网络环境直连拉取 GitHub 较慢，可在订阅 URL 前添加 `https://ghfast.top/` 镜像前缀（例如：`https://ghfast.top/https://raw.githubusercontent.com/...`）。

---

## Loon 配置文件一键导入代码

在 Loon 文本配置的 `[Remote Rule]` 模块下添加以下内容：

```ini
# > Crypto-Rules 分流规则集
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules), policy=Taiwan, tag=Binance, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules), policy=Taiwan, tag=ouyi, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules), policy=Taiwan, tag=Bybit, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules), policy=Taiwan, tag=Gate, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules), policy=Taiwan, tag=Wise, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules), policy=United Kingdom, tag=iFAST, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules), policy=Hong Kong, tag=BiyaPay, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules), policy=Hong Kong, tag=PokePay, enabled=true
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules), policy=Hong Kong, tag=MPChat, enabled=true
```

---

## Surge / Shadowrocket 配置文件一键导入代码

在 Surge / Shadowrocket 文本配置的 `[Rule]` 模块下添加以下内容：

```ini
# > Crypto-Rules 分流规则集
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules,Taiwan](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules,Taiwan)
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules,Taiwan](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules,Taiwan)
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules,Taiwan](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules,Taiwan)
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules,Taiwan](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules,Taiwan)
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules,Taiwan](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules,Taiwan)
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules,United](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules,United) Kingdom
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules,Hong](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules,Hong) Kong
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules,Hong](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules,Hong) Kong
RULE-SET,[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules,Hong](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules,Hong) Kong
```

---

## Clash / Mihomo 配置文件一键导入代码

在 Clash / OpenClash 文本配置中分别添加 `rule-providers` 和 `rules` 模块内容：

```yaml
# > 1. 规则集提供商 (rule-providers)
rule-providers:
  Binance:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules)"
    path: ./ruleset/Binance.list
    interval: 86400

  OKX:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules)"
    path: ./ruleset/OKX.list
    interval: 86400

  Bybit:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules)"
    path: ./ruleset/Bybit.list
    interval: 86400

  Gate:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules)"
    path: ./ruleset/Gate.list
    interval: 86400

  Wise:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules)"
    path: ./ruleset/Wise.list
    interval: 86400

  iFAST:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules)"
    path: ./ruleset/Ifast.list
    interval: 86400

  BiyaPay:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules)"
    path: ./ruleset/BiyaPay.list
    interval: 86400

  PokePay:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules)"
    path: ./ruleset/PokePay.list
    interval: 86400

  MPChat:
    type: http
    behavior: classical
    format: text
    url: "[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules)"
    path: ./ruleset/MPChat.list
    interval: 86400

# > 2. 匹配规则 (rules - 请置于通用代理规则之前)
rules:
  - RULE-SET,Binance,Taiwan
  - RULE-SET,OKX,Taiwan
  - RULE-SET,Bybit,Taiwan
  - RULE-SET,Gate,Taiwan
  - RULE-SET,Wise,Taiwan
  - RULE-SET,iFAST,United Kingdom
  - RULE-SET,BiyaPay,Hong Kong
  - RULE-SET,PokePay,Hong Kong
  - RULE-SET,MPChat,Hong Kong
```

---

## Quantumult X 配置文件一键导入代码

在 Quantumult X 文本配置的 `[filter_remote]` 模块下添加以下内容：

```ini
# > Crypto-Rules 分流规则集
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Binance-rules), tag=Binance, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/OKX-rules), tag=OKX, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Bybit-rules), tag=Bybit, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Gate-rules), tag=Gate, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Wise-rules), tag=Wise, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Ifast-rules), tag=iFAST, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Biyapay-rules), tag=BiyaPay, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/Pokepay-rules), tag=PokePay, force-remote-dns=true, opt-parser=false, update-interval=86400
[https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules](https://raw.githubusercontent.com/smllbboomm/Crypto-Rules/main/MPchat-rules), tag=MPChat, force-remote-dns=true, opt-parser=false, update-interval=86400
```
