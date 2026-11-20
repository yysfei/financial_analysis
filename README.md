# financial_analysis
Financial Analysis

历史交易研究笔记。分类目录在 [reports/arbitrage/README.md](reports/arbitrage/README.md)，写作规则在 [docs/arbitrage-archive.md](docs/arbitrage-archive.md)。

## 最新报告（按时间倒序）

日期是报告写入或最近一次实质更新的 Asia/Shanghai 日历日。下面按这个更新顺序排列，不是按案例发生时间。

| 更新日期 | 一句话结论 | 报告 |
| --- | --- | --- |
| 2026-11-20 | 已核验的机制里没有零风险、可直接照搬的稳定套利；实盘执行若要做，只能是隔离的确定性程序，通用助手不持有私钥、不下单 | [跨策略风险与 Bot 架构评估](reports/arbitrage/2026/cross-strategy-risk-and-bot-architecture/README.md) |
| 2026-11-20 | 五分钟 BTC 宣传指向同一钱包的不同故事；抽查结算写的是 Chainlink 60 秒 TWAP，99¢ 吃单的保本胜率约 99.0693% | [五分钟 BTC](reports/arbitrage/2026/polymarket-5m-btc-microstructure/README.md) |
| 2026-11-20 | 三个天气账户经济口径为正，但高价 NO 的高胜率不是锁定收益；三段视频没有逐帧复核 | [天气市场](reports/arbitrage/2026/polymarket-weather-markets/README.md) |
| 2026-11-20 | AI V2 是方向性价值投注，不是无风险套利；没有公开钱包、源码或样本外成绩 | [AI V2 价值投注](reports/arbitrage/2026/polymarket-ai-v2-value-betting/README.md) |
| 2026-11-20 | 24 条链接收成 23 个独立帖；廉价 YES 的完整地址是 `0x6e1d5040d0ac73709b0621f620d2a60b80d2d0fa`，100 笔买入里有 31 笔 NO | [2026-11-20 去重索引](reports/arbitrage/2026/batch-2026-11-20-triage/README.md) |
| 2026-11-20 | YES+NO 小于 1 不是净利的充分条件；mo-money 与附录钱包 `0xfcda…eecc` 不合并收益 | [mo-money 完整集合](reports/arbitrage/2026/polymarket-mo-money-complete-set/README.md) |
| 2026-11-20 | 视频看板是 133.70 到 14,880.00 美元，与正文 68 到 75 万美元不一致；FOMO 未授权自动化仍是阻塞项 | [xmglia / FOMO](reports/arbitrage/2026/xmglia-fomo-ai-arbitrage-claims/README.md) |
| 2026-11-20 | 回测图按连续 5 年、无追加资金折算，复合年化约 6.56%，不是标题上的 12% | [foodloss / EA](reports/arbitrage/2026/foodloss-ai-trading-desk-ea-backtest/README.md) |
| 2026-11-20 | 67% 胜率、夏普 2.3 和 2,847 美元纸面周收益都是作者自述，没有钱包、代码或市场 ID | [强化学习择时](reports/arbitrage/2026/polymarket-rl-timing-claims/README.md) |
| 2026-11-20 | 区块 21960556 的原子多池循环历史上已成功；构建者转账远大于发起地址的净增加，没有 2026 年池状态模拟 | [以太坊区块 21960556](reports/arbitrage/2025/eth-21960556-multipool-atomic/README.md) |

分类总表、案例时间和证据状态见 [reports/arbitrage/README.md](reports/arbitrage/README.md)。

固定跟踪分支名为 `latest-reports`。它用来提供一个不随 PR 分支改名的阅读入口，路径是该分支上的 `reports/arbitrage/README.md`。规范要求新归档在 4 小时内推到这个分支。这次提交只更新当前 PR 分支，仓库里还没有安装会自己写报告的定时任务。

## 套利研究

新案例使用 [templates/arbitrage-report.md](templates/arbitrage-report.md)。这些文件只记录研究，不运行交易。
