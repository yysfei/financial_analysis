# QuantJourney 开源回测库与「全部盈利、一键实盘」宣传

- 归档日期：2026-11-23 Asia/Shanghai
- 市场与标的：示例覆盖股票/行业 ETF、外汇现货与连续期货等；这是回测研究工具和教学策略模板，不是单一可交易组合
- 策略类型：开源组合/订单回测引擎，附带趋势、动量、均值回归、突破、市场中性配对、风险平价和波动目标等示例。是投研工具方法，不是套利，也不是已验证的实盘交易系统
- 案例时间：[@irongiantXBT](https://x.com/irongiantXBT/status/2124582184376029638) 发布于 2026-11-23 03:14:00 Asia/Shanghai（UTC 19:14:00，2026-11-22）；同一对话的[回复](https://x.com/irongiantXBT/status/2124585314438299742)发布于 03:26:26，给出 GitHub 策略目录。官方仓库 `QuantJourneyOrg/quantjourney-bt` 创建于 2026-06-25，本轮读取时最近一次推送为 2026-11-04 19:46 Asia/Shanghai，托管策略目录页标注 Generated 2026-07-11
- 研究状态：已读取原帖全文（含超过 280 字的 `note_tweet`）、回复中的仓库链接、官方 README 与 `strategies/README.md`、GitHub 仓库元数据、团队页、Substack 更新文、托管策略目录和 W01 证据包，并观看了原帖 24 秒配视频。官方仓库确实存在且可运行示例；但「全部盈利」「SpaceX AI 工程师」「几分钟用 Grok Bot 接到券商做 24/7 实盘」与官方说明、托管绩效表和视频内容不符。本轮没有独立复跑回测，也没有下单或连接券商
- 证据等级说明：A 本次打开的公开页面、接口或原帖/视频上的原始字段，B 由 A 精确计算或计数，C 第三方叙述，D 未访问或未完整查看，E 假设、演示或示意数据
- 是否复用既有报告：否。`latest-reports` 的投资与套利目录中没有以本帖、QuantJourney 回测库或「开源策略库一键实盘」为对象的既有报告。相邻但不合并的材料：[Grok Bot Harness 文件夹](../savvy-luvvvv-grok-bot-harness/README.md)（原帖引用了作者 11 月 17 日的 Harness 长文，但正文谈的是策略库，不是同一套方法）、[Bitget Agenthub MCP](../waveking-bitget-agenthub-mcp/README.md)、以及同一作者此前的五分钟盘宣传（见既有 irongiant 相关核验，不在本目录重复展开）

本文件是研究笔记。评估过程中没有下单，没有连接券商、交易所或钱包，也没有把示例回测数字当成应当跟随的实盘成绩。

## 结论

[@irongiantXBT](https://x.com/irongiantXBT/status/2124582184376029638) 的核心宣传是：一名「SpaceXAI engineer」做了一个开源库，「every single one」都是已经用多年真实行情回测过的盈利策略，免费提供完整代码、仪表盘指标，并且「you can turn any strategy into a live 24/7 trading bot with grok bot in minutes」，可连接 Alpaca、Interactive Brokers 或 Oanda，从模拟盘起步，还带风险限额和 kill switch。文末是「steal this before everyone starts using it」。回复里给出的地址是 [QuantJourneyOrg/quantjourney-bt 的 strategies 目录](https://github.com/QuantJourneyOrg/quantjourney-bt/tree/main/strategies)。

**官方对象和原帖包装不是一回事。** 打开后的仓库是 Apache 2.0 的 Python 回测引擎，主页为 [backtester.quantjourney.cloud](https://backtester.quantjourney.cloud)。GitHub 接口在本轮读取时给出 685 星、263 次 fork，默认分支 `main`，语言 Python。官方 README 的「What It Is Not」写明：这不是券商、不是实盘交易系统、不是投资建议，也不保证策略在样本外有效；部分示例有意简化了融券、融资、流动性和冲击成本，并要求这些假设被写明而不是藏起来。`strategies/README.md` 把 51 个文件称作「runnable example strategies」和「self-contained template」：复制最接近的例子、改规则，就能测试自己的策略。托管 W01 证据包也写明目标是教学，展示的是可运行研究代码在既定设置下的观察结果，「it is not presented as optimized alpha or an investment recommendation」。

**「全部盈利」与官方已公布的绩效表冲突。** 托管目录页写明 50/50 runs passed、45 份绩效仪表盘，生成日期 2026-07-11；短周期日内例子故意不给年化头条指标，以免误导。本轮按该页表格计数：45 个给出总收益的例子中，有 7 个总收益为负（O10、O16、O19、W08、W16、W23、W24）；40 个给出夏普的例子中，有 19 个夏普小于或等于 0；没有任何一个公布夏普大于或等于 1；夏普不低于 0.5 的只有 O17（0.53）、W18（0.57）、W25（0.62）。这些数字全部来自官方托管页，本轮没有用自有数据或官方 API 复跑，因此只用来反驳「每一个都是已验证盈利策略」，不能当成新的可投资成绩。

**实盘与 Grok Bot 通道在官方回测仓库里没有对应说明。** 本轮打开的 README 全文检索没有出现 Live、Alpaca 或 Grok。原帖 24 秒视频是黑暗主题的「Grok Bot / OPEN SOURCE LIBRARY」界面，标题为 Trading bot library，标称「120+ BOTS」，版本文字为 `v1 x 2026.11.23`；画面没有出现 QuantJourney、Alpaca、Interactive Brokers 或 Oanda 字样，也没有实际下单或 kill switch 面板。视频只展示 6 个机器人；点击 Run 后指标会在几乎没有等待的情况下跳到另一组数字，且「Trend pullback bot」跳变后的 Return / CAGR / Sharpe / Max DD / Win rate / Profit factor 与「SMA crossover bot」的初始数字完全相同。更合理的判断是演示界面和占位数据，而不是一次可复核的回测或实盘。视频里的指标也与官方托管目录中对应规则的数字对不上，例如画面中 SMA crossover 初始总收益 +79.6%、CAGR +2.57%、夏普 0.24，而官方 O01 Market SMA Cross 为总收益 126.66%、CAGR 3.33%、夏普 0.21。

**「SpaceX AI 工程师」未能核实。** 官方团队页只列出四个名字：Jakub（研究与架构）、Alexander（策略与 live systems）、Tomasz（优化与绩效）、Patryk（机器学习与数据工程），没有姓氏，也没有 SpaceX 或 SpaceX AI 的任职信息。对 Patryk Kozak 与 SpaceX 的公开检索没有找到与 QuantJourney 对应的任职证据。这一声称目前只能记为原帖用语，不能当成已核验的作者身份。

把材料放在一起，只能得到一个更弱、也更有用的结论：QuantJourney Backtester 可以作为受监督的量化研究工具，用来阅读经典规则的实现、查看官方示例包、并在自有数据或官方工作流上复现回测；它不是一条已经验证过的盈利流水线，也不能根据原帖把示例「一键」交给 Grok Bot 做无人值守交易。不应自动下单。

## 机制与主张

原帖给出的盈利逻辑，是把「开源 + 全样本回测 + 完整代码」直接等同于可挪用的实盘优势，再用 Grok Bot 和三家券商接口把研究包变成 24 小时交易机器人。成立条件至少包括：示例策略在扣除完整成本后仍有稳健的样本外期望、执行路径确实存在并且经过验证、以及推广者没有把教学回测包装成保证收益。就本轮证据看，这三项都没有成立。

官方引擎的实际机制更接近标准研究流水线：数据 → 特征 → 信号 → 目标权重或订单 → 模拟成交 → 持仓与现金 → NAV、指标和报告包。它区分两种研究模式。权重模式面向组合、轮动、多空和风险覆盖；订单模式面向市价、限价、止损、移动止损、括号单和 OCO，并模拟佣金、滑点、成交和持仓。仓库还提供 walk-forward、Optuna 优化，以及给编程助手用的 `skills/` 说明包。官方 Substack 更新文把对象写成「50 ready-to-run Python strategies」和可自带 CSV / Parquet / DataFrame / yfinance 数据的研究框架，并指向与 VectorBT、Backtrader 等引擎的对比，而不是「保证盈利的策略工厂」。

示例本身多为公开、可讨论的经典规则，例如日频 SMA(50/200) 趋势、RSI 回归、双动量、反向波动率加权、配对交易、截面动量/反转、风险平价、布林带、MACD、外汇动量和期货 Donchian / 连续合约趋势。策略类型可以讨论，但不因为它们是公开指标或教学模板就没有研究价值；同样，它们也不因为被放进同一个仓库，就变成已经验证的赚钱系统。

原帖引用了作者 2026-11-17 的长文 [Your Grok Bot Is Burning Money - Harness Fixes It](https://x.com/i/article/2122340667510960129)。那篇文章谈的是多 Bot 编排与成本，已经单独归档，不能用来补上本帖缺失的实盘接口证据。

## 公开证据和可信度

| 主张 | 核验 | 等级 |
| --- | --- | --- |
| 存在公开仓库 `QuantJourneyOrg/quantjourney-bt`，Apache 2.0，主页为 backtester.quantjourney.cloud | GitHub 仓库接口与 README、LICENSE | A |
| 本轮读取时 685 星、263 fork；创建于 2026-06-25T11:28:39Z，最近推送 2026-11-04T11:46:57Z | GitHub 仓库接口字段 | A |
| 仓库提供 51 个可运行示例（26 个权重、20 个订单、5 个 walk-forward / 优化）；W26 在目录中标注为 Empty sample or own archive | 官方 README 与 `strategies/README.md` | A |
| 托管目录写 50/50 通过、45 份绩效仪表盘，Generated 2026-07-11 | [策略目录页](https://backtester.quantjourney.cloud/strategies) | A |
| 官方写明这不是券商、不是实盘系统、不是投资建议，也不保证样本外有效；部分示例简化融券、融资、流动性和冲击成本 | README「What It Is Not」 | A |
| 原帖称每一个策略都已用多年真实数据回测且盈利 | 与官方「example / template / not optimized alpha」表述冲突；也与托管表中的负收益和大量非正夏普冲突 | A（官方表述）+ B（对官方表计数） |
| 托管表：45 个总收益里 7 个为负；40 个夏普里 19 个 ≤ 0；0 个夏普 ≥ 1；夏普 ≥ 0.5 的只有 O17、W18、W25 | 对 2026-07-11 目录表逐行计数 | B |
| W01 Daily SMA Trend：行业 ETF 宇宙 XLB–XLY，配置期 2000-01-03 至 2026-01-01，基准 SPY，初始资金 10 万美元，数据源 yfinance，引擎快照 0.10.0 · a35f582c47dcd036；CAGR 7.38%，夏普 0.45，最大回撤 -34.68%，总收益 536.96%，波动率 14.75% | [W01 证据包](https://backtester.quantjourney.cloud/strategies/example-weights-01-sma-daily) | A |
| W01 模拟佣金合计 2,799.38 美元，约占成交金额 27,786,585 美元的 0.01%；佣金模型 fixed_bps、费率 1.01 bps；滑点模型为 none；无风险利率 2.00% | 同上证据包 Operational / 模型字段 | A |
| 可用自有数据运行，不必绑定 QuantJourney API；真实目录回测也可使用 `QJ_API_KEY`，托管产品需要 `product:backtester` 权限 | README Quick Start | A |
| 原帖称可在几分钟内用 Grok Bot 变成 24/7 实盘，并连接 Alpaca / IB / Oanda，含模拟盘、风险限额和 kill switch | 官方回测仓库 README 未出现这些字段；视频中也未出现券商名称或该设置界面 | A（缺失） |
| 视频是真实回测或实盘仪表盘 | 视觉复核：标称 120+ 却只展示 6 个；Run 后指标立即跳变，且不同机器人出现完全相同的小数；未出现 QuantJourney 或券商名称 | A（屏幕内容）+ 对「真实回测」为否定 |
| 作者是 SpaceX AI 工程师 | 团队页无该任职信息；公开检索未找到对应证据 | D（未证实） |
| 网上另有 Jakub Polec 关于跨 Interactive Brokers 与 OANDA 的 OMS 陈述，以及 IBKR 官方与 ChatGPT/Grok 的代理交易集成 | 检索到第三方或不相干产品页面，本轮未打开 OMS 源码，也未把 IBKR 官方功能算成 QuantJourney 回测库的一部分 | C / D |

## 收益口径与成本

本轮不把任何示例数字写成「已验证收益」。需要标明的口径如下：

- 托管目录和 W01 证据包中的 CAGR、夏普、最大回撤和总收益，是官方在既定宇宙、区间、基准和成本假设下的模拟结果，生成批次标注为 2026-07-11。W01 的配置期到 2026-01-01，并不覆盖此后的行情。
- 本轮没有重新下载行情、没有复跑 `./strategy.sh`，因此这些数字的等级是「官方页面上的字段」，不是本仓库独立回测。
- W01 已计入约 1.01 bps 的固定佣金，但滑点模型为 none。官方自己也提醒部分示例简化了融资融券、流动性和冲击成本。把「已计入佣金」理解成「完整交易成本」并不成立，尤其是日内、外汇、期货和配对交易。
- 短周期日内例子在目录中不给年化 CAGR / 夏普，这是官方为了避免误导做出的限制，不能用很短窗口的总收益去外推年化。
- 视频里出现的 Return、CAGR、Sharpe、Max DD、Win rate、Profit factor 只能作为画面内容记录，不能进入收益表。页脚甚至出现过 Total Return -12.4%、Max DD -41.2% 这类与「全部盈利」直接相反的滚动数字。
- 税费、资金占用、借款费率、期货保证金和展期、外汇点差，以及 yfinance 作为研究数据源的已知限制，本轮都没有从官方示例包里看到完整、统一的建模，一律视为未知。

## 风险

- 方向与模型风险：示例多数是有方向暴露的公开规则。即便某个历史路径看起来为正，也不构成对拥挤交易、制度变化或样本外失效的保护。walk-forward 页明确写了「not independent OOS evidence」，优化流程给出的 Sharpe 也不能直接当成实盘期望。
- 成本与流动性风险：滑点为 none、冲击成本被简化时，回测会高估高频、限价和窄价差策略。期货与外汇还涉及合约规格、保证金和点差，本轮未逐项复核。
- 数据风险：W01 使用 yfinance。复现结果取决于数据修正、停牌、分红调整和接口可用性；官方也提供自带数据的路径。
- 平台与产品边界：开源引擎之上还有托管平台、API 密钥和 `product:backtester` 权限。研究工具可以使用开源部分；不能把托管仪表盘或「Pro」图表理解成已经开通的交易通道。
- 宣传与利益冲突：原帖使用 FOMO 措辞，并把策略库与作者自己的 Grok Bot Harness 文章绑在一起。QuantJourney 同时维护开源仓库和带权限的托管产品。引流本身不否定仓库的研究价值，但独立核验必须把宣传主张和官方文本分开。
- 合规与杠杆：即便日后出现真实的券商接口，自动下单仍涉及账户资质、市场准入和当地规则。本轮没有验证任何券商连接，也没有评估杠杆或清算路径。
- 身份与来源风险：「SpaceX AI 工程师」未证实。不能据此提高对回测质量的信任。

## 可执行性与自动化部署评估

作为研究工具，可执行性中等偏好。仓库是公开 Python 项目，有 `strategy.sh` / `strategy.bat`、`--check`、`--sample-data` 和文档；不设置 API 密钥也能做导入检查和示例数据演示。把某个示例改成自己的规则、用自有数据复现，对熟悉 Python 和量化研究流程的人是可行的。这需要一定的专业知识，但并不要求先接受原帖的盈利主张。所需本金和期限取决于研究者自己选择的市场和频率，官方 W01 只用 10 万美元作为模拟起始资金，不是实盘门槛。

作为交易系统，可执行性低，也不适合自动化下单。官方回测仓库明确把自身排除在实盘系统之外。原帖所说的 Grok Bot 分钟级接入、三家券商和 kill switch，在本轮打开的官方文档和视频里都没有得到证实。Grok Bot 可以在人工监督下帮助阅读代码、检查是否存在前视偏差、以及组织回测报告；它可以做只读研究助理，但不应该被授权根据这些示例直接下单。AI 辅助的边界是：帮助理解与复核，而不是替代风控、成交和合规判断。

若只做研究复现，合理的停止条件是：能在本地或自有数据上跑通一个示例，读懂宇宙、成本、成交假设和样本区间，并拒绝把官方或视频中的绩效数字当成实盘预期。若目标是自动交易，在出现可核验的官方实盘文档、可审计的券商接口和独立样本外证据之前，不应继续把该宣传当作可部署方案。

## 来源

详细访问记录见 [sources.md](sources.md)。

## 未解决问题和复核记录

- 本轮没有独立复跑 45 个绩效包，也没有核验托管页与本地 `docs/strategy-results` 预览是否逐项一致。
- 没有打开 QuantJourney 可能存在的独立 OMS 或 live 仓库源码；检索到的 Jakub Polec OMS 陈述仍待直接核验。
- 没有验证 Alpaca、Interactive Brokers、Oanda 或任何 Grok Bot 实盘/模拟盘连接。
- 没有核实团队成员的完整身份或 SpaceX 任职。
- 原帖视频中「Source code」按钮和 Discord 图标指向的具体地址，画面里没有展开，本轮未能打开。
- 仓库在 11 月 4 日之后是否还有未推送的私有改动，本轮只看到公开 `main`。
