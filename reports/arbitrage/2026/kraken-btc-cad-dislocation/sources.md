# 来源与证据边界

对应报告：[README.md](README.md)

## 本轮扫描窗口

- 上次成功扫描：2026-11-21 16:13:58 Asia/Shanghai（2026-11-21 08:13:58Z）。
- 本轮 `start_time`：`2026-11-21T08:00:00Z`（16:00 Asia/Shanghai），对上次成功扫描略有重叠。
- 实际覆盖：用户 `@FeiShen370926` 主页时间线两页共 148 条，最新 `2026-11-21T12:08:51Z`（20:08:51 Asia/Shanghai），最旧 `2026-11-21T08:00:08Z`（16:00:08 Asia/Shanghai）。
- 同时检查了书签前 50 条。书签接口不返回加入时间。本案例来自时间线，不是书签。
- 去重：阅读了 https://github.com/yysfei/financial_analysis 的 `latest-reports` 根索引、`reports/arbitrage/README.md`、`reports/investment/README.md` 与目录树；`main` 仍停在 `663ab8051cb08a36b566bc1a989a7b7def840bb1`，其中没有 BTC/CAD 专题。`latest-reports` 本轮开始时的最新提交是 `d0cabcb23a182fafa9659f1913118918060747be`。

## X 原帖

| 来源 | 访问方式 | 时间 | 用到的内容 | 不用它证明的事情 | 等级 |
| --- | --- | --- | --- | --- | --- |
| https://x.com/oragnes/status/2124069487549051001 ，附图 https://pbs.twimg.com/media/HXo1u5obsAAvYYQ.jpg | 用户或公共 X 只读接口，打开全文并下载附图 | 2026-11-21 09:16:43 UTC | 标题称加拿大交易对比特币打折；截图字段见主报告 | 不证明发帖人已下单，也不证明 Last Price 可按该数量成交 | A |

## 公开报道与行情页

| 来源 | 访问方式 | 用到的字段 | 计算 | 等级 |
| --- | --- | --- | --- | --- |
| https://cryptring.com/news/kraken-btc-cad-anomaly | 2026-11-21 打开。文内时间 10:39 UTC | 10:24 UTC 读取的 Kraken 公共 ticker：BTC/CAD 最低 24,250、最新成交 79,305.40；最低价位于 08:00 UTC 五分钟区间；BTC/USD 最低 55,100、最新成交 57,965.10。文内写明成因和提币主张未证实 | 用 1.43445 把 24,250 CAD 换算为约 16,905.43 美元，只作对照 | C（报道）/ B（换算） |
| 检索到的 USD/CAD 约 1.43445（2026-11-21） | 公开网页检索，不是央行官方收盘 | 用于把截图中的 CAD 价格换成美元 | 见主报告 | C |
| 检索到的 BTC/USD 第三方报价 | 流动性表与分钟价转述 | 约 58,000–58,400 美元，与指数价同一数量级 | 不采用为 Kraken 成交价 | C |
| https://pro.kraken.com/app/trade/btc-cad | 检索摘要显示 81,360.0、24h -6,640.0 CAD（-7.55%）、量 694 BTC / 56.5M CAD | 只说明稍后价格已离开截图中的 43,607 区域 | 本次没有把该页当作盘口逐档核验 | C |

## 明确没有访问或没有采用的材料

- Kraken 账户、私有订单接口、入金与提币记录。
- 08:00 UTC 五分钟窗口的原始逐笔成交文件。
- TechFlow 报道中的全部交叉交易对数字，未逐项复点。
- 未编造已实现收益、可成交数量或自动搬砖成绩。

## 利益冲突记录

原帖是市场观察截图，未见付费产品推广。本笔记与发帖人、Kraken 均无商业关系。评估不因“看起来像套利”而放宽可执行性标准。

## 2026-11-22 追加

不改写“不是可执行套利、深度极薄、价差超过 11%、不能把显示折价写成已锁定净利”。写档时 X `get_posts_by_ids` 因缺少 `developer.billing.write` 被拒，没有重拉原始 JSON。Kraken 支持帖的原文被下面两篇已打开的报道逐字引用，与本轮已经核对的原文一致。

| 来源 | 访问方式 | 时间 | 用到的内容 | 不用它证明的事情 | 等级 |
| --- | --- | --- | --- | --- | --- |
| https://x.com/krakensupport/status/2124098562443354591 | 本轮已核对全文；CryptoSlate 与 Coindaro 逐字转引 | 2026-11-21 11:12:15 UTC（2026-11-21 19:12:15 Asia/Shanghai）。账号 `@krakensupport`，显示名 Kraken Support | “Starting around 20:00 UTC on Nov 20, CAD pairs on Kraken saw heavy selling pressure that pushed prices well below other markets. Our platform processed every order correctly, and our security teams found no sign of a breach or compromised accounts. Executed trades stand.” | 不证明最低价上的可成交数量和提币，也不给出完整成因。结算方向只是：已成交的单会保留 | A（已核对的原文，并与两家引文一致） |
| https://x.com/chenke20266/status/2124395310105731125 | 本轮已读转述帖 | 2026-11-22 14:51:25 Asia/Shanghai（2026-11-22 06:51:25 UTC） | “Kraken加元盘闪崩 比特币一度报1.7万美元 市价打五折 官方说成交有效 不回滚”。附图为原报告同一张订单簿：Last 43,607.4 CAD，Index 83,515.4 CAD，24h −50.76%，价差 4,707.5 / 11.4111%，Total CAD 约等于 1 | 不是新盘口。1.7 万美元即原记录的 24,250 CAD，按约 1.43445 换算约 16,905.43 美元 | A（帖与附图身份）/ B（沿用既有换算） |
| https://cryptoslate.com/kraken-says-trades-stand-after-bitcoin-sold-at-24250-canadian/ | 2026-11-22 打开 | 文内时间 2026-11-21 13:30 GMT | 复述官方声明，并写 BTC/CAD 触及 24,250 CAD | 文中的 K 线路径和 09:40 UTC ticker 细节本轮未用 Kraken 原始响应复核 | C |
| https://www.coindaro.com/kraken-btc-cad-flash-crash-trades-stand/ | 2026-11-22 打开 | 文内时间 2026-11-21 13:20 | 同样复述官方声明，并描述公开成交里按钟点出现的市价卖单 | 本轮没有下载 Kraken 逐笔文件独立计数。不能据此声称已经找到下单人。文中约 1.4325 的汇率只是另一套换算 | C |

本轮没有登录 Kraken，没有下载逐笔成交，没有连接钱包。
