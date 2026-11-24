# 来源

本目录对应报告：[README.md](README.md)。扫描覆盖 2026-11-24 12:12 至 16:13 Asia/Shanghai（UTC 04:12:00 至 08:13:24），账号 @FeiShen370926。下列材料只用于研究核验，不构成交易指令。

## A. 本次打开的公开页与原帖

| 编号 | 材料 | 地址 | 用到的字段或内容 |
| --- | --- | --- | --- |
| A1 | 宣传主帖 | https://x.com/linda6248130564/status/2125107587582775525 | 2026-11-24 14:01 Asia/Shanghai。深圳 22 岁大学生、900 元红米、月赚 1.47 万美元、PhoneDriver、Claude、像素识别、国内新闻相对海外盘滞后 20–50 分钟。这些句子是宣传，成绩见 C |
| A2 | 钱包回复 | https://x.com/linda6248130564/status/2125107590023860403 | 指向下面的 Polymarket 页 |
| A3 | 邀请链回复 | https://x.com/linda6248130564/status/2125107592297062773 | 邀请参数、跟单机器人，以及官方/永续邀请链 |
| A4 | Polymarket 公开页 | https://polymarket.com/zh/@432614799197 | 去掉 `?via=k3H86f8` 不改变身份。Joined Jan 2026。320.2K views。Positions Value $0.00。Biggest Win $1.5M。Markets Traded 4,549。Total PnL +$4.5M。Total Volume 185.5M。可见市场名称主要是 NBA、NHL、足球等体育盘 |
| A5 | PVNGL 公开页（同日另一则，不单开） | https://polymarket.com/ja/profile/0x5eda5ce195168b746f1c4cc10b05a663f8cd3136 | Total PnL +$14.7K。Biggest Win $3,573.32。Markets Traded 1,838。可见仓位多为比特币短时段涨跌 |

A4 的 1 周和 1 个月区间在抓取里显示 $0.00。扫描记录把它视为可能未渲染，不解释成月收益为零，分时段记为未完整查看。185.5M 不换算单位。Positions Value $0.00 与列表中的体育市场名称同时出现，不合并成一种未说明的口径。

## B. 由页面字段不能做的归因

没有把 +$4.5M、Biggest Win $1.5M 或 4,549 个市场除成「月赚 1.47 万美元」。没有把 185.5M 写成 1.855 亿美元。没有把 +$14.7K 写成 13.9 万。

## C. 宣传文本

| 编号 | 材料 | 内容 | 限制 |
| --- | --- | --- | --- |
| C1 | A1 的人物和工具故事 | 22 岁、900 元红米、月赚 1.47 万美元、PhoneDriver 截图、Claude、像素识别、滞后 20–50 分钟 | 未核账单和时戳。不提供像素识别或绕过限制的步骤 |
| C2 | edzachary 体育盘宣传 | 总盈利 24.5 万美元、单日 9 万美元 | 扫描记录的公开页 Total PnL 为 +$40.7K，与 24.5 万不符。简报未给出该主页 URL，本目录不补地址。无执行规则 |
| C3 | PVNGL 宣传 | 30 天 400U 到 628U、本月盈利 13.9 万、胜率 50.8% | 与 A5 的 +$14.7K 和可见的比特币短时段仓位冲突 |

## 利益冲突

| 编号 | 材料 | 地址 | 处理 |
| --- | --- | --- | --- |
| R1 | Polymarket 邀请参数 | 页面和帖中的 `via=k3H86f8` | 引流。不改变 A4 的身份 |
| R2 | Telegram 跟单 | https://t.me/KreoPolyBot?start=ref-tx1688 | 只记录链接。不访问、不启动、不连接 |
| R3 | 官方注册与永续邀请链 | 见 A3 | 扫描记录确认该回复是邀请链。未单列的落地 URL 不补造 |

## D. 未访问或未做成的事

- 没有测量国内新闻与任何 Polymarket 市场的到达时差。
- 没有打开新闻 App，没有实现或描述像素识别、截图自动化或绕过条款的步骤。
- 没有连接钱包，没有调用交易接口。
- 没有把 1 周 / 1 个月的 $0.00 当成完整的区间盈亏。

## 相邻但不合并

- [0DTE 新闻时差与 ApeWire](../mm-options-nvda-0dte-newswire-latency/README.md)：美股新闻线路，不是这个钱包
- [Polymarket 小时级自相关与方差比](../linda-polymarket-hourly-acf-vr/README.md)：同一发帖人的另一套规则
- [neo7777 天气钱包](../linda-polymarket-neo7777-weather/README.md)：同日另一钱包，标的是气温档
