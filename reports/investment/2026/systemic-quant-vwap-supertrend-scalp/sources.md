# 来源

本目录对应报告：[README.md](README.md)。访问时间均为 2026-11-22 Asia/Shanghai。下列材料只用于研究核验，不构成交易指令。

## A. 本次打开的原帖、仓库与脚本页

| 编号 | 材料 | 地址 | 访问方式 | 用到的字段或内容 |
| --- | --- | --- | --- | --- |
| A1 | @waveking1314 时间线帖 | https://x.com/waveking1314/status/2124305028253167755 | 用户已连接的 X 接口读取主页时间线；随后用公开帖子接口复核全文 | 发布时间 2026-11-22 00:52:41 UTC（2026-11-22 08:52:41 Asia/Shanghai）；四条过关条件；每日最多 3 次；Pine Script v5；正文中的仓库短链 `https://t.co/ndq25r6xBR` |
| A2 | 短链解析后的 GitHub 仓库 | https://github.com/systemic-quant/VwapSupertrend-mtf-indicator | 打开仓库页与 README | 创建时间 2026-07-26T13:46:26Z；本轮可见 Star 7、Fork 2；License GPL-3.0；TradingView 脚本链接；默认参数与「How to Trade」；Telegram 频道引流 |
| A3 | 源码 `indicator_v1.pine` | https://raw.githubusercontent.com/systemic-quant/VwapSupertrend-mtf-indicator/main/indicator_v1.pine | 打开 raw 文件全文 | `indicator()` 声明；VWAP、Supertrend、过滤、状态机、每日上限、`barstate.isconfirmed` 只用于标签和告警、额外的 `close > open` / `close < open` 条件 |
| A4 | TradingView 公开脚本页 | https://www.tradingview.com/script/EoYskW99-Vwap-Supertrend-Intraday-Scalp/ | 打开公开页面 | 标题 *Vwap + Supertrend Intraday Scalp*；作者 `narzof88`；页面显示 Jul 26；说明文字与仓库 README 主体一致 |
| A5 | 同日相关但不同主题的帖 | https://x.com/waveking1314/status/2124350288069099847 ，引用 https://x.com/waveking1314/status/2120893892396716506 | 同一时间线窗口与公开帖子接口 | 关于 Fable 5.2 的短讯，指向已有报告 `waveking-ai-prompt-trading-desk`，不并入本指标结论 |

## B. 由 A 计算或直接对照的内容

| 编号 | 计算或对照 | 结果 | 说明 |
| --- | --- | --- | --- |
| B1 | 时间线「四条」与源码默认条件对照 | 四条均可在源码中找到对应判断；源码另有做多 `close > open`、做空 `close < open` | 属于规则对照，不是收益计算 |
| B2 | 仓库创建时间换算 | 2026-07-26 13:46:26 UTC = 2026-07-26 21:46:26 Asia/Shanghai | 由 A2 的时间戳换时区 |
| B3 | 每日信号计数是否按买卖分开 | 源码里买卖共用 `session_signal_count`，默认上限为合计 3 次 | 直接阅读 A3 |

## C. 第三方叙述，未在本轮逐项复点

| 编号 | 材料 | 说明 |
| --- | --- | --- |
| C1 | README 中的「Institutional」订单流、「high-probability momentum bursts」、「Zero-Repaint」和「historical-backtest accurate」 | 保留原文范围；其中后两项只部分对应源码里的高周期引用方式，不是已发表的绩效回测 |
| C2 | README 提示在 HUD 显示 `FULL ALIGNMENT` 时迅速执行 | 源码 HUD 并不使用这一字符串 |

## D. 本次未访问或未能核到

| 编号 | 想核验的内容 | 失败或未做的方式 |
| --- | --- | --- |
| D1 | 在 TradingView 中加载脚本、历史回放或带佣金滑点的策略回测 | 本轮只阅读公开页和源码，没有运行脚本 |
| D2 | 任何实盘、模拟盘账单或作者绩效图 | 公开材料未提供 |
| D3 | Telegram 频道 `https://t.me/+1-hIvYv_4gxiYTRl` 的内容与付费/加粉条款 | 只记录仓库中存在该链接，未加入频道 |
| D4 | `narzof88` 与 GitHub 用户 `systemic-quant` 是否为同一控制人 | 未做身份核验 |
| D5 | 脚本页的 Boost、评论区和是否有与仓库不一致的更新版本 | 打开了脚本页说明，但没有得到可可靠引用的互动计数，也未做版本逐行比对之外的页面翻查 |
| D6 | 时间线配图中的界面细节 | 未作为独立证据转写；以 A3 源码为准 |
