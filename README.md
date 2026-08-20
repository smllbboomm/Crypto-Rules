# Crypto & 金融服务分流规则集 (Loon)

本仓库提供主流加密货币交易所、数字银行、跨境汇款及 Web3 虚拟发卡平台的全量分流规则。所有规则均采用解耦拆分维护，内置核心 API、CDN 静态加速及 KYC 人脸识别/风控组件依赖，避免打包规则导致的地区合规冲突与风控拦截。

---

## 规则订阅列表与推荐节点策略

| 规则名称 | 适用平台 | 推荐策略组 / 节点 | 说明 | 订阅链接 (Raw) |
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
