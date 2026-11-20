# 来源与证据边界：强化学习择时自述

案例报告：[README.md](README.md)。分级规则见 [归档规范](../../../../docs/arbitrage-archive.md)。

研究记录的取证窗口是北京时间 2026-11-20 02:17—02:23。本次归档重新打开了费率、返佣和结算文档。帖文长文沿用该次公开读取，没有另造业绩数字。采集时保存的帖文原文和媒体文件不进入本仓库。

## 帖文与媒体

| 材料 | 链接 | 本次边界 |
| --- | --- | --- |
| 原帖 | [x.com/PolRaviraj/status/2123315135192146050](https://x.com/PolRaviraj/status/2123315135192146050) | 公开读取记录给出 `created_at` = `2026-11-19T07:19:12.000Z`，即北京时间 2026-11-19 15:19:12。完整长文包含 18 个月、200 万次迭代、四类输入、四类动作、样本外 67% 胜率、夏普 2.3、一周纸面 2,847 美元、14 个市场胜出 11 次，以及伊朗例子的 48¢、96¢ 和 1,200 美元。这些都是作者自述 |
| 推荐入口 | [polymarket.com/zh/?via=Poly666](https://polymarket.com/zh/?via=Poly666) | 带推荐参数的平台入口，不是模型仓库或成绩证明。本次没有注册、下单或提交表单 |
| 视频 | [video.twimg.com 的公开 MP4](https://video.twimg.com/amplify_video/2123315026580627456/vid/avc1/1920x1060/_wHbPcbygGFK9RNU.mp4) | 时长记录为 19.202 秒。复核结论见报告：主要是自定义面板，没有可复现训练过程或独立业绩账本 |
| 预览图 | [pbs.twimg.com 预览图](https://pbs.twimg.com/amplify_video_thumb/2123315026580627456/img/IAZKNZFIdA8Y3izc.jpg) | 预览图是演示界面。自动识别出的每个标题或数字不升为事实 |

线程记录为原帖加 8 条简短回复，下一页为空。回复没有补充实验、成交或代码。没有引用帖、文章对象、模型仓库、钱包或结算哈希。

## 规则页

与完整集合案例共用的官方页面，在本次归档中重新打开了 D3、D4、D5、D6。其余沿用研究记录，不把失效的文档路径当成数据。

| ID | 链接 | 用于本案例的内容 | 限制 |
| --- | --- | --- | --- |
| D1 | [价格与订单簿](https://docs.polymarket.com/concepts/prices-orderbook) | 显示价可以是中间价或末笔成交价；买入要看卖盘，卖出要看买盘 | 纸面触价不等于成交 |
| D3 | [Fees](https://docs.polymarket.com/trading/fees) | 当前 `fee = C × feeRate × p × (1 − p)`。Weather 系数 0.05，Geopolitics 为 0，Maker 平台交易费为 0 | 作者没有给出市场 ID，不能先认定伊朗例子或天气例子的类别 |
| D4 | [2026 年 11 月费改公告](https://docs.polymarket.com/programs/fee-and-rebate-changes-november-2026) | 2026-11-20 23:59 UTC，即北京时间 2026-11-21 07:59 生效。Weather 拟改为 0.01，Geopolitics 仍为 0 | 18 个月历史必须用当时费制。公告不是当前已生效的成交价 |
| D5 | [Taker Rebate Program](https://docs.polymarket.com/programs/taker-rebates) | 返佣向后适用、按日支付、规则可改 | 没有账户，就不能套用任何档位 |
| D6 | [Resolution](https://docs.polymarket.com/concepts/resolution) | 普通胜方通常每份赎回 1 美元，负方为 0；罕见的 UMA Unknown/50-50 为每份 0.50 美元 | 96¢ 因此不能直接称作常规最终兑付价，也不能直接判为虚假 |

## 条件算术与缺失

0.48 买到 0.96、利润 1,200 美元时，未计费用的名义规模是 2,500 份。这是由作者数字反推的算术，不是成交量。同样 2,500 份若按 1 美元兑付，毛利润是 1,300 美元。差额可能来自费用、数量或提前卖出，需要原始记录。

没有钱包、市场 ID、逐笔纸面订单、实盘记录、代码、数据版本、训练日志、实验种子、样本外区间、初始本金和回撤。没有用一个看起来相似的市场代替伦敦天气或伊朗制裁例子。
