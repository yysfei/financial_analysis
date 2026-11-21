# 套利研究索引

这里归档人工撰写的历史套利研究。目录规则在 [docs/arbitrage-archive.md](../../docs/arbitrage-archive.md)，新报告从 [templates/arbitrage-report.md](../../templates/arbitrage-report.md) 复制。

没有程序读取链上数据，也没有程序向本目录自动添加文件。表中每一行都对应一次人工归档。

## 最新报告（按时间倒序）

这一节按写入或最近一次实质更新的 Asia/Shanghai 日期排列。下面的分类表仍按案例发生时间排列，两套顺序不要混用。

| 更新日期 | 一句话结论 | 报告 |
| --- | --- | --- |
| 2026-11-22 | 既有结论不变：不是无风险套利，不能把钱包收益归因到所宣传规则。新增 @irongiantXBT 宣传的钱包真实，但公开持仓是月度方向性价位盘而非 5 分钟涨跌，配视频为 PAPER 动画，不能作为该规则的业绩证明 | [五分钟 BTC](2026/polymarket-5m-btc-microstructure/README.md) |
| 2026-11-21 | Kraken BTC/CAD 在 2026-11-21 出现过相对指数约五成的显示折价，但盘口价差超过 11% 且深度极薄，原因未证实，不能视为可执行套利 | [Kraken BTC/CAD 盘口折价](2026/kraken-btc-cad-dislocation/README.md) |
| 2026-11-20 | 已核验机制里没有可直接照搬的零风险套利；实盘执行边界是隔离的确定性程序，通用助手不持有私钥 | [跨策略风险与 Bot 架构评估](2026/cross-strategy-risk-and-bot-architecture/README.md) |
| 2026-11-20 | 天气账户经济口径为正，高价 NO 的胜率不是锁定收益；三段视频没有逐帧复核 | [天气市场](2026/polymarket-weather-markets/README.md) |
| 2026-11-20 | AI V2 是方向性价值投注；没有公开钱包、源码或样本外成绩 | [AI V2 价值投注](2026/polymarket-ai-v2-value-betting/README.md) |
| 2026-11-20 | 24 条链接收成 23 个独立帖；廉价 YES 完整地址已映射，100 笔买入中有 31 笔 NO | [2026-11-20 去重索引](2026/batch-2026-11-20-triage/README.md) |
| 2026-11-20 | YES+NO 小于 1 不是净利充分条件；附录钱包不与 mo-money 合并收益 | [mo-money 完整集合](2026/polymarket-mo-money-complete-set/README.md) |
| 2026-11-20 | 视频金额是 133.70 到 14,880.00 美元，与正文 68 到 75 万美元不一致 | [xmglia / FOMO](2026/xmglia-fomo-ai-arbitrage-claims/README.md) |
| 2026-11-20 | 回测图按 5 年无追加资金折算约 6.56%，不是标题 12% | [foodloss / EA](2026/foodloss-ai-trading-desk-ea-backtest/README.md) |
| 2026-11-20 | 胜率、夏普和纸面周收益均为作者自述，没有可复现账本 | [强化学习择时](2026/polymarket-rl-timing-claims/README.md) |
| 2026-11-20 | 历史原子多池交易已成功；没有当前池状态模拟，不构成持续收益 | [以太坊区块 21960556](2025/eth-21960556-multipool-atomic/README.md) |

固定跟踪分支名为 `latest-reports`，用来用固定路径阅读最新归档。新归档应在 4 小时内推到该分支。这次改动只在当前 PR 分支上，仓库没有已安装的定时写入任务。

## 分类目录

| 案例时间（UTC） | 链 | 策略类型 | 研究状态 | 报告 |
| --- | --- | --- | --- | --- |
| 2025-03-02 17:02:47 | Ethereum mainnet | 同链单笔原子多池循环 | 历史执行已复核。场所数、币种数和原帖美元估值未独立复点。没有 2026 年池状态模拟 | [区块 21960556](2025/eth-21960556-multipool-atomic/README.md) |
| 2026-11-19 09:44:38 | Polygon 上的 Polymarket 账户；完整集合结算不限于单笔 | 二元完整集合。价差不是净利的充分条件 | 机制与四笔链上样本已复核。文末附录另有钱包 `0xfcda…eecc`，不与 mo-money 合并收益 | [mo-money 完整集合](2026/polymarket-mo-money-complete-set/README.md) |
| 2026-11-19 07:19:12 | 未给出结算链上的单笔 | 方向性强化学习择时。不是已证明的无风险套利 | 业绩数字均为作者自述。无钱包、代码、市场 ID 或可复现训练记录 | [强化学习择时自述](2026/polymarket-rl-timing-claims/README.md) |
| 2026-11-19 08:51:45 | 未给出可核验的链、钱包或交易 | 宣传为价差套利。可读材料混合信号、方向性交易和开发提示词 | 两段动态视频已对照。画面金额与正文 68 / 75 万不一致。没有可核验账本。FOMO 自动化授权仍是阻塞项 | [xmglia / FOMO](2026/xmglia-fomo-ai-arbitrage-claims/README.md) |
| 2026-11-19 15:59:57 | 未给出链上交易。回测图来自 MetaTrader | 量化系统需求提示词，加上未公开规则的 EA 历史回测宣传 | 截图字段已复核。按 5 年无追加资金的条件算术约为 6.56%，不是标题 12% | [foodloss / EA](2026/foodloss-ai-trading-desk-ea-backtest/README.md) |
| 2026-11-15 15:21:41 | 未给出钱包或成交。样本规则指向 Binance BTC 日线收盘 | 事件价值投注和尾部彩票。不是无风险套利 | 文章可读。没有公开源码、钱包和样本外成绩。没有附带视频 | [AI V2 价值投注](2026/polymarket-ai-v2-value-betting/README.md) |
| 报告未单列原帖 UTC。统计观察在 2026-11-19 至 2026-11-20 | Polygon 上的三个 Polymarket 天气账户 | 按站点规则买天气结果。高胜率不是锁定收益 | 三个账户的经济口径为正。宣传的胜率、周收益和“只买高价 NO”没有被样本证实。三段视频未逐帧复核 | [天气市场](2026/polymarket-weather-markets/README.md) |
| 公开读取 2026-11-20 02:41–02:44；2026-11-22 补充读取约 00:13–04:40 | Polygon 上的 BTC 五分钟和近到期市场 | 延迟、弱势侧、动量和尾盘微观结构。不是无风险套利 | 两个宣传指向同一钱包。结算样本写的是 Chainlink TWAP，不是 Binance 现货。视频未逐帧审查。2026-11-22 补充：@irongiantXBT 宣传的钱包真实，但公开持仓是月度方向性价位盘而非 5 分钟涨跌，配视频为 PAPER 动画，不能作为该规则的业绩证明，也不能把该钱包收益归因到所宣传规则 | [五分钟 BTC](2026/polymarket-5m-btc-microstructure/README.md) |
| 2026-11-21 09:16:43（Asia/Shanghai 17:16:43） | Kraken 现货（BTC/CAD，对照 BTC/USD） | 中心化交易所跨计价货币的盘口错位 | 显示折价可核验但价差和深度不支持可执行套利、成因未证实 | [Kraken BTC/CAD 盘口折价](2026/kraken-btc-cad-dislocation/README.md) |

上表前八行仍是此前的八篇深度报告。第九行是 [Kraken BTC/CAD 盘口折价](2026/kraken-btc-cad-dislocation/README.md)。跨策略对照和自动化边界在 [跨策略风险与 Bot 架构评估](2026/cross-strategy-risk-and-bot-architecture/README.md)。它不新增行情或回测，只转述这八篇和下面的分拣记录。

2026-11-20 的 24 条链接、23 个独立帖的去重索引在 [batch-2026-11-20-triage](2026/batch-2026-11-20-triage/README.md)。其中的 [廉价 YES 钱包核验](2026/batch-2026-11-20-triage/c7-cheap-yes-wallet-check.md) 使用完整地址 `0x6e1d5040d0ac73709b0621f620d2a60b80d2d0fa`。CasaVerilla 提到的另一个完整集合钱包写在 mo-money 报告末尾，不单独开案。

当前归档日：2026-11-22 Asia/Shanghai。本索引只在人工提交时改写。

后两案与上面的 Polymarket 笔记不是同一平台、同一业绩。xmglia 讨论的是 FOMO 宣传和一段重复使用的控制台视频；foodloss 讨论的是开发规格和一份未公开规则的回测图。两案都没有被证明为无风险套利。

## 2026 年两则帖文的对比

两帖都带推荐参数，也都配有视频。推荐参数只说明存在推广背景，不能据此推断帖文造假。两段视频都主要是自定义数据面板和交互界面。

| 问题 | [mo-money 完整集合](2026/polymarket-mo-money-complete-set/README.md) | [强化学习择时](2026/polymarket-rl-timing-claims/README.md) |
| --- | --- | --- |
| 收益从哪里来 | 同一条件的互补结果可以合并或赎回。YES+NO 低于 1 只是毛价差 | 买入后价格或结算是否朝持仓方向变化。帖文没有锁定差价的结构 |
| 已有的公开原始记录 | 官方档案接口记录，以及四笔可打开的 Polygon 交易 | 帖文长文本身。没有钱包、市场 ID、代码或训练日志 |
| 视频能证明什么 | 约 550,045.93 美元的累计展示，以及流动的单边成交。不能独立复核双腿同时成交、真实成交价和全成本收益 | 展示胜率、夏普和对比次数的界面。没有可复现训练过程，也没有独立业绩账本 |
| 和另一套数字为何不同 | 视频约 550,045.93、原帖 560,370、研究时点平台 `trade_pnl` 601,539.115804 可以来自不同时点或口径 | 67% 胜率、2.3 夏普、2,847 美元纸面周收益都还只有作者自述 |
| 这次没有做的事 | 没有重拉更晚的账户行情，没有把 pUSD 和 USDC.e 当成同一记账资产轧平 | 没有训练模型，没有回测，没有挑选一个“看起来相似”的市场代替原例 |
