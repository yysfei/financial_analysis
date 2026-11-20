# 来源与证据边界：foodloss / AI 交易台 / EA 回测

案例报告：[README.md](README.md)。分级规则见 [归档规范](../../../../docs/arbitrage-archive.md)。

研究日：2026-11-20，北京时间。两帖、Article 正文和回测图来自该日的公开读取。图片曾下载并放大核读，原始图片、JSON 和页面文本不进入本仓库。本案例没有需要单独核对的动态视频。另一帖的界面视频不属于这份 EA 的业绩证据。

## 主要来源

| ID | 链接 | 已取得、可以支持 | 不支持 |
| --- | --- | --- | --- |
| X1 | [foodloss_otoko 2123446186883547391](https://x.com/foodloss_otoko/status/2123446186883547391) | 日文原文、直接引用和两张中文长提示图。主张用 AI 搭建 24 小时机器人，并让读者转发或把图交给助手。原字段 `2026-11-19T15:59:57.000Z`，北京时间 2026-11-19 23:59:57 | 不证明作者原创这些图，不证明策略有优势，也不证明机器人已经实盘 |
| X2 | [foodloss_otoko 2116376578187780173](https://x.com/foodloss_otoko/status/2116376578187780173) | 引用帖、完整 Article 和回测图。标题为「完全放置で年利12％のEAを作りました。」正文说反复做 5 年回测，并可通过 LINE 询问免费 EA。原字段 `2026-10-31T03:47:51.000Z`，北京时间 2026-10-31 11:47:51 | 不证明 12% 年化、每一年都盈利、真实成交，或该 EA 由新帖里的提示词生成 |
| X2a | [对应 Article](https://x.com/i/article/2116375410560905216) | 实体链接元数据曾 404，公开读取仍得到约 890 字符正文和图片 | 没有完整 Tester 报告、EA、参数、日志和逐笔流水 |
| M1 | [MetaTrader 5 测试报告说明](https://www.metatrader5.com/en/terminal/help/algotrading/testing_report) | History Quality、Net Profit、Profit Factor、balance / equity 回撤等口径 | History Quality 不是胜率、实盘认证或无未来函数证明 |
| M2 | [MetaTrader 5 测试说明](https://www.metatrader5.com/en/terminal/help/algotrading/testing) | 历史测试、优化、forward 和执行假设 | 不证明作者报表真实 |
| F1 | [Freqtrade 稳定版文档](https://www.freqtrade.io/en/stable/) | 回测、dry-run、live、支持的交易所和部署门槛 | 不覆盖图中每一个市场和每一种策略，也不是盈利保证 |
| F2 | [Freqtrade 止损](https://www.freqtrade.io/en/stable/stoploss/) | `stoploss_on_exchange` 支持矩阵，以及止损限价可能不成交 | 不是任意交易所或任意产品都能满足“每仓原生止损” |
| F3 | [Freqtrade 前视检查](https://www.freqtrade.io/en/stable/lookahead-analysis/) | 检查只覆盖实际执行到的信号，可能漏检或误判 | 工具通过不等于没有未来函数 |
| G1 | [Grok Bot 指南](https://x.ai/bot/guides/grok-bot-101) | 云电脑、工具和任务协调 | 不证明交易写权限、确定时延或收益 |

图中的 taker 0.10%、maker 0.05% 和单边滑点 0.05% 是规格里的例子，不是本次指定场所的现行费率。

## 条件算术

在“截图覆盖连续整 5 年、没有外部净入金、3,000 是全部初始资本、1,121.30 是该期间全部净收益”这些前提都成立时：

```text
6032.61 - 4911.31 = 1121.30
6032.61 / 4911.31 = 1.2283097585
1121.30 / 3000 = 0.3737666667
(4121.30 / 3000) ^ (1/5) - 1 = 0.0655714966
1121.30 / 3000 / 5 = 0.0747533333
1121.30 / 1626 = 0.6896063961
```

前提没有被完整报告证实，所以这是口径差异，不是欺诈裁定。0.6896 是额外未计入成本的盈亏平衡量级，不把已经含在 Net 里的佣金再扣一次。账户计价币种没有核实，不把 3,000 和 1,121.30 写成美元。

## 访问界限

- [Freqtrade dry-run 旧路径](https://www.freqtrade.io/en/stable/dry-run/) 当时返回 404。不据此否认 dry-run；当前文档首页和其他页面已经确认该功能。
- 没有联系 LINE，没有取得 `.ex5`、MQL5 源码、`.set`、完整 HTML、经纪商、品种、精确日期、tick、延迟、费用模型和实盘流水。
- 两帖线程都翻到空页。中文图没有署名，公开短语搜索没有找到更早的可核原始作者。不能断言原创，也不能断言抄袭。
- 没有证明中文提示词产生了这份 EA。
