# 来源

本目录对应报告：[README.md](README.md)。访问时间均为 2026-11-23 Asia/Shanghai。下列材料只用于研究核验，不构成交易指令。

## A. 本次打开的原帖、仓库、官方页与视频

| 编号 | 材料 | 地址 | 访问方式 | 用到的字段或内容 |
| --- | --- | --- | --- | --- |
| A1 | `@irongiantXBT` 策略库宣传帖 | https://x.com/irongiantXBT/status/2124582184376029638 | 用户已连接的 X 主页时间线，以及公开 X 接口的全文（`note_tweet`）和媒体信息 | 发布时间 2026-11-22T19:14:00.000Z（北京时间 2026-11-23 03:14:00）；声称 SpaceXAI engineer、全部盈利且经多年真实数据回测、可用 Grok Bot 在几分钟内做 24/7 实盘，并连接 Alpaca / Interactive Brokers / Oanda；引用 2122662343306059780；配 24 秒视频 |
| A2 | 同一对话的回复，给出 GitHub 目录 | https://x.com/irongiantXBT/status/2124585314438299742 | 同上 | 发布时间 2026-11-22T19:26:26.000Z（北京时间 03:26:26）；链接 https://github.com/QuantJourneyOrg/quantjourney-bt/tree/main/strategies |
| A3 | 原帖引用的作者长文 | https://x.com/irongiantXBT/status/2122662343306059780 、 https://x.com/i/article/2122340667510960129 | 公开 X 接口返回的 `article.title` 与 `article.plain_text` 开头 | 标题《Your Grok Bot Is Burning Money - Harness Fixes It》。已有独立报告，本轮只确认引用关系，不合并结论 |
| A4 | 原帖配视频 | 媒体 ID 13_2124451290482958336；MP4 保存于研究时的工作目录，不写入本仓库 | 下载官方 MP4 后做视觉复核 | 无对白；界面品牌为 Grok Bot OPEN SOURCE LIBRARY，标题 Trading bot library，标称 120+ BOTS，版本文字 `v1 x 2026.11.23`；展示 6 个机器人；未出现 QuantJourney 或券商名称；点击 Run 后指标跳变，且 Trend pullback bot 与 SMA crossover bot 初始指标完全相同 |
| A5 | GitHub 仓库 `QuantJourneyOrg/quantjourney-bt` | https://github.com/QuantJourneyOrg/quantjourney-bt | 打开仓库页，并读取 https://api.github.com/repos/QuantJourneyOrg/quantjourney-bt | 描述 QuantJourney Backtester；homepage https://backtester.quantjourney.cloud；created_at 2026-06-25T11:28:39Z；pushed_at 2026-11-04T11:46:57Z；stargazers_count 685；forks_count 263；license Apache License 2.0；language Python；默认分支 main |
| A6 | 官方 README | https://raw.githubusercontent.com/QuantJourneyOrg/quantjourney-bt/main/README.md | 原始文件全文 | 「What It Is Not」：不是券商、不是实盘系统、不是投资建议、不保证样本外有效；51 个示例的分类；Quick Start 与 API / 自有数据说明；检索未出现 Live、Alpaca、Grok |
| A7 | 官方策略目录说明 | https://raw.githubusercontent.com/QuantJourneyOrg/quantjourney-bt/main/strategies/README.md | 原始文件全文 | 51 个可运行示例的完整表；称为 template；W26 为 Empty sample or own archive |
| A8 | 官方团队页 | https://backtester.quantjourney.cloud/team | 公开网页 | 四人：Jakub、Alexander、Tomasz、Patryk；Alexander 的职责文案含 live systems；无姓氏，无 SpaceX 任职信息；许可证 Apache 2.0 |
| A9 | 官方托管策略目录 | https://backtester.quantjourney.cloud/strategies | 公开网页表格 | 「50/50 runs passed」「45 performance dashboards」「Generated 2026-07-11」；各示例的 CAGR、Sharpe、Max DD、Return；日内短窗口例子的年化指标为 — |
| A10 | W01 证据包 | https://backtester.quantjourney.cloud/strategies/example-weights-01-sma-daily | 公开网页 | 教学声明；宇宙 XLB–XLY；配置期 2000-01-03 → 2026-01-01；基准 SPY；初始资金 100,000 美元；数据源 yfinance；引擎 0.10.0 · a35f582c47dcd036；CAGR 7.38%；Sharpe 0.45；Max DD -34.68%；Total return 536.96%；Volatility 14.75%；Total Commission 2,799.38 美元；Total Volume 27,786,585 美元；Commission Rate 1.01 bps；Slippage Model none；Risk-Free Rate 2.00% |
| A11 | QuantJourney Substack 更新文 | https://quantjourney.substack.com/p/quantjourney-update-open-source-backtester | 公开网页 | 作者署名 Cheers, Jakub；强调开源回测器、约 50 个可运行策略、可自带数据、walk-forward 与 Optuna；指向 GitHub 与托管站 |
| A12 | LICENSE | https://raw.githubusercontent.com/QuantJourneyOrg/quantjourney-bt/main/LICENSE | 原始文件开头 | Apache License 2.0 |

## B. 由 A 计算的数字

| 编号 | 计算 | 结果 | 依据 |
| --- | --- | --- | --- |
| B1 | 对 A9 表格中给出总收益的 45 行，统计总收益以 `-` 开头的行 | 7 个：O10、O16、O19、W08、W16、W23、W24 | A9 |
| B2 | 对 A9 表格中给出数值夏普的 40 行，统计夏普 ≤ 0 的行 | 19 个 | A9 |
| B3 | 同上 40 行中，夏普 ≥ 1 的行数 | 0 | A9 |
| B4 | 同上 40 行中，夏普 ≥ 0.5 的行 | 3 个：O17 0.53、W18 0.57、W25 0.62 | A9 |
| B5 | W01 页面「Commission (% Vol) 0.01%」与 2,799.38 / 27,786,585 的对照 | 2,799.38 / 27,786,585 ≈ 0.0101%，与页面 0.01% 和 1.01 bps 一致 | A10 |

视频中的绩效数字只作为 A4 的屏幕记录，不进入本表，也不作为回测成绩。

## C. 第三方叙述，未在本轮逐项复点

| 编号 | 材料 | 说明 |
| --- | --- | --- |
| C1 | 网络检索中的 Jakub Polec LinkedIn 陈述：曾编写可连接 Interactive Brokers 与 OANDA 的 OMS | 与回测仓库「不是实盘系统」的官方说明不是同一份文件。本轮没有打开该 OMS 的源码或文档，不能用来证实原帖的 Grok Bot 实盘通道 |
| C2 | 检索到的 Interactive Brokers 与 ChatGPT / Grok 代理交易集成报道 | 这是券商自己的产品消息，不能记成 QuantJourney 回测库或原帖视频已经提供的功能 |
| C3 | 官方团队页提到 Alexander「Owns … live trading systems」 | 只是职责描述。本轮没有在 `quantjourney-bt` 中打开对应 live 代码 |

## D. 本次未访问或未能核到

| 编号 | 想核验的内容 | 失败或未做的方式 |
| --- | --- | --- |
| D1 | 独立复跑 45 个官方绩效包，以及 `docs/strategy-results` 本地预览是否与托管页一致 | 未运行 `./strategy.sh`，未下载完整结果包 |
| D2 | Alpaca、Interactive Brokers、Oanda 的真实或模拟盘连接，以及原帖所称 kill switch | 官方回测 README 无对应字段；视频未展示；未做任何登录或下单测试 |
| D3 | 团队成员完整姓名、任职经历，以及「SpaceX AI 工程师」是否属实 | 团队页无姓氏；对 Patryk Kozak 与 SpaceX 的检索没有找到与本项目对应的证据 |
| D4 | 视频中 Source code 按钮和 Discord 图标的实际链接 | 画面未展开目标地址 |
| D5 | QuantJourney 托管账户权限、收费和 `product:backtester` 的完整条款 | 只在 README 中见到权限名称，未打开账户计费页 |
| D6 | 原帖之后仓库是否还有未推送到 `main` 的私有更新 | 公开接口的 pushed_at 为 2026-11-04T11:46:57Z |

## E. 假设或示意，不进入案例结论

| 编号 | 内容 | 出处 |
| --- | --- | --- |
| E1 | 原帖视频在点击 Run 后跳变出的第二组指标，以及不同机器人之间完全相同的复制数字 | A4，视为演示或占位数据 |
| E2 | 原帖「几分钟接入 24/7 实盘」的操作工期 | 未被官方文档证实，不得当作可执行工期估计 |
