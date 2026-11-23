# financial_analysis
Financial Analysis

历史交易研究笔记。套利笔记在 [reports/arbitrage/README.md](reports/arbitrage/README.md)，投资、配置、期权、择时与收益策略笔记在 [reports/investment/README.md](reports/investment/README.md)，金融传闻核验在 [reports/research/README.md](reports/research/README.md)，三者并列。套利写作规则在 [docs/arbitrage-archive.md](docs/arbitrage-archive.md)。

## 最新报告（按时间倒序）

日期是报告写入或最近一次实质更新的 Asia/Shanghai 日历日。下面按这个更新顺序排列，不是按案例发生时间。

| 更新日期 | 一句话结论 | 报告 |
| --- | --- | --- |
| 2026-11-23 | 仓库是 MIT 许可的 TradingView 指标，规则公开，并声明不下单、没有回测成绩。这是开盘首小时的方向性框架，不是已验证交易系统，也不应让 Grok Bot 自动下单 | [开盘首小时「两根K线定方向」回踩指标](reports/investment/2026/waveking-coil-reclaim-opening-hour/README.md) |
| 2026-11-23 | 2026-11-22 桥接铸币和随后的跨市场搬砖有公开报道交叉核对；The Block 追查到的例子是约 40 美元买入、约 17,670 美元卖出，不是「60 美元本金」的精确账本。桥储备当日已被搬空，存在回滚和合规风险，这不是可重复套利，不应参与或自动下单 | [Fusionist ACE 跨链桥 relabel 后的跨市场价差](reports/arbitrage/2026/fusionist-ace-bridge-dislocation/README.md) |
| 2026-11-23 | 摩根大通 11 月 20 日把行业生产成本中枢估在约 8.6 万美元，周五价格跌破 6 万美元、MARA 卖出 13,597 枚（约占 9 月 30 日持仓 40%）可核对。生产成本不是自动底部，「等最后一批矿机关机」只是推论，不能自动抄底 | [比特币「生产成本 8.6 万美元、市价约 6 万美元」与矿工卖币](reports/investment/2026/kkawsb-btc-miner-cost-gap/README.md) |
| 2026-11-23 | 纳斯达克与 NYSE Arca 计划于 2026-12-06 增加美东 21:00–04:00 夜盘、以限价单为主，使交易日接近 23 小时。这是市场结构变化，不是交易策略；原帖所引浑水「赌场」原话本轮未独立核到 | [纳斯达克与 NYSE Arca 的 23/5 夜盘（2026-12-06）](reports/research/2026/nasdaq-nyse-arca-23-5-trading/README.md) |
| 2026-11-23 | 对多数没有信息优势的个人，用低费率宽基指数、短期国债或现金、黄金或商品做分散配置并再平衡，是说得通的长期思路，但原文没有权重和产品，不能写成唯一数学最优解，也不能自动下单。牛顿「亏损两万英镑」和文中个股亏损案例本轮均未核成确定事实 | [跨资产低费率被动配置的“哑铃”思路](reports/investment/2026/python-xxt-barbell-passive-allocation/README.md) |
| 2026-11-23 | 官方仓库是 Apache 2.0 回测引擎和 51 个教学示例，自己写明不是实盘系统、不是投资建议、不保证样本外有效。托管页 2026-07-11 批次中，45 份绩效表有 7 个总收益为负、19 个夏普≤0、没有夏普≥1；原帖「全部盈利、用 Grok Bot 几分钟接入实盘」与官方说明和演示视频不符。这是投研工具，不能自动下单 | [QuantJourney 开源回测库](reports/investment/2026/irongiant-quantjourney-bt-library/README.md) |
| 2026-11-23 | 特朗普 11 月 20 日公开催降息有多家媒体引述，但未直接观看发布会录像；美联储公开文件未支持中国即将爆雷或高利率意在逼中国承压。公开文件无证据不等于证明内部绝无讨论。与美元潮汐报告交叉链接，不合并。这是宏观叙事核验，不是交易策略 | [白宫催降息与逼中国承压](reports/research/2026/wangyun-whitehouse-fed-china/README.md) |
| 2026-11-23 | 格力滚动税前股息率 7.32% 和本金算术基本成立，但年度现金分红折算不等于每月实际派息，历史股息率不保证未来，税后与持有期有关，新预案未实施。这是高股息本金测算，不是套利，也不是完整交易系统 | [格力 7.32% 股息率躺平测算](reports/investment/2026/kongyigc-gree-dividend-yield/README.md) |
| 2026-11-23 | 美债总额和付息压力可核对，但加息路径被夸大，主席讲话的情景分析被改写为刺泡承诺，全球收割没有证据。这是宏观叙事核验，不是交易策略 | [美联储加息与美元潮汐叙事](reports/research/2026/leelee-fed-dollar-tide/README.md) |
| 2026-11-23 | 部分交易所欧元 SEPA 充值确实暂停，但 KuCoin 明确提现及其他支付方式仍可用；没有银行名、文件或监管通报证明欧洲主流银行无差别封杀或全球出入金关闭。谨慎保留的限制：其他平台帮助页不是实际到账测试；机构托管上线也不直接证明零售出入金可用，不能拿其夸大反证。这是金融传闻核验，不是套利，也不是可执行策略 | [小电欧洲银行法币通道传闻](reports/research/2026/xiaodian-eu-bank-fiat-rails/README.md) |
| 2026-11-23 | 官方文档确认 Grok Bot 可接 Bitget 云端 MCP，独立账户且下单前确认；这只是执行层，不创造交易优势。原文与 Bitget 合作并带邀请码，标的是代币化美股而非股票直连。本研究未授权、未下单，不应无人值守交易 | [Bitget Agenthub MCP](reports/investment/2026/waveking-bitget-agenthub-mcp/README.md) |
| 2026-11-23 | 周五 NVDA 收盘 125.53 美元可核对，但「近两年任意买入几乎全亏」不成立，也不能证明 125 美元是安全抄底。黄仁勋辞职与董事会不拟恢复其职务的既有结论不变。贝森特 11 月 22 日 CBS 采访原话是 “Jensen is on the outside now”，并称要看责任止于何处，不能把这句改写成「回归已成定局」或财富密码。没有退出规则，不能自动下单 | [NVDA 125 美元抄底与 ARK 减持](reports/investment/2026/komereji-mmoptions-nvda-125-dip-ark/README.md) |
| 2026-11-23 | VRT / CEG / VST 的多项官方财报、合同和周五跌幅可核对；亚马逊 20 年协议含 690MW（其中约 190MW 为新增），谷歌协议支持 890MW 新增核电。这是方向性板块观点，没有进出场规则，不能视为已验证机会 | [AI 电力与基础设施：VRT / CEG / VST](reports/investment/2026/python-xxt-ai-power-infra/README.md) |
| 2026-11-23 | 作者称 VIX 多空 +22.32%、A 股增强 +9.77% 为实盘，但规则未公开、成绩无法独立核对；所列标普 +5.61% 与 11 月 20 日收盘后约 +0.8% 至 +0.9% 的公开口径不一致。这是带俱乐部推广的绩效展示，不是可执行交易系统 | [VIX 多空与 A 股指数增强周报](reports/investment/2026/amy6tina-vix-ls-index-enhance/README.md) |
| 2026-11-23 | 中国融资保证金 100% 降至 80% 由上交所公告确认，但 11 月 30 日才生效，周一开盘并不适用。台湾金管会限空措施 11 月 23 日起生效，财政部称国安基金已进场但未公布金额。韩国是约 10.76 万亿韩元稳定基金准备启动、并非已经买入。「黑色星期一能躲过」只是推论 | [周末亚洲稳市措施](reports/investment/2026/oragnes-asia-weekend-stabilization/README.md) |
| 2026-11-22 | 多 Bot 分工可用于受监督编程，但原帖的模型锁定和 API 标价省费假设不适用于 Grok Bot；Jev 脚本未实现，尚无可核验账单。这是投研/工程工具方法，不是交易策略 | [Grok Bot Harness 文件夹](reports/investment/2026/savvy-luvvvv-grok-bot-harness/README.md) |
| 2026-11-22 | 既有结论不变：黄金金字塔是方向性摊低成本规则，不是已验证交易系统。新增：作者晒出 BTCUSDT 永续 3 倍做多截图，开仓均价 58,344、标记价 61,247.8、未实现约 +14.90%，与价格变动乘 3 倍大体相符，但不是已实现收益，也没有仓位和交易所；杠杆与清算风险未出现在原黄金表中，不应自动下单 | [黄金金字塔式越跌越买](reports/investment/2026/yijiangren-gold-btc-pyramid-dca/README.md) |
| 2026-11-22 | 期权坤哥讨论周五 VIX 盘中触及 40 后的结构与日历价差。部分极值可核对，但绩效未复现，2022 年标普跌幅口径错误，规则不完整，不能当成已验证机会，不应自动下单 | [周五 VIX 盘中触及 40 与日历价差](reports/investment/2026/sober-vix40-structural-calendar/README.md) |
| 2026-11-22 | 既有结论不变：VIX 收盘阈值按 11-20 收盘尚未触发，QQQ 截图 +1.57% 是相对成本不是日历年收益，规则仍不完整。新增：公开的 TQQQ 长期收益宣传高于官方 2026-10-31 月末年化，400 倍与官方年化折算倍数不一致，不能自动下单 | [VIX>40 逆向加仓与 QQQ/TQQQ 长期配置](reports/investment/2026/vix-contrarian-qqq-tqqq/README.md) |
| 2026-11-22 | 既有结论不变：不是可执行套利，深度极薄，价差超过 11%，不能把显示折价写成已锁定净利。新增：Kraken 官方称成交保留、未发现入侵；转述帖仍是同一张订单簿，「1.7 万美元」不是新的更低价 | [Kraken BTC/CAD 盘口折价](reports/arbitrage/2026/kraken-btc-cad-dislocation/README.md) |
| 2026-11-22 | 源码与公开规则可核对：这是 VWAP 与 15 分钟 Supertrend 加成交量、实体过滤的方向性日内信号，默认每天最多 3 次；仓库与脚本页没有可核验的收益或完整进出场规则，不能视为已验证交易系统，不应自动下单 | [VWAP + 多周期 Supertrend 限次日内短线指标](reports/investment/2026/systemic-quant-vwap-supertrend-scalp/README.md) |
| 2026-11-22 | Kobeissi 图把周五标普标在 50 日均线下方 4.1 个标准差；周五收盘 6,910.39、约低于 50 日均线 9.4% 可核对，但 4.1 的公式未复算，「均值回归是大概率」只是推论，不是可执行交易系统 | [标普低于 50 日均线 4.1 个标准差](reports/investment/2026/kkawsb-spx-4sigma-mean-reversion/README.md) |
| 2026-11-22 | 既有结论不变：不是无风险套利，不能把钱包收益归因到所宣传规则。新增 @irongiantXBT 宣传的钱包真实，但公开持仓是月度方向性价位盘而非 5 分钟涨跌，配视频为 PAPER 动画，不能作为该规则的业绩证明 | [五分钟 BTC](reports/arbitrage/2026/polymarket-5m-btc-microstructure/README.md) |
| 2026-11-22 | 文章给出了 BTC 5 分钟永续的双模型规则，但正文与交易舱截图规则不一致；展示的 +18.70% 写明是模拟盘且无回测，不能视为已验证交易系统，50 倍杠杆下不应自动下单 | [BTC 5 分钟双模型（GPT + Grok）](reports/investment/2026/chenke-btc5m-dual-model-bot/README.md) |
| 2026-11-22 | 0xboan 给出先用公开规则过滤、再让 Grok 读 X、最后由人签字的 Solana meme 币流程；文中成绩图标明不是真实运行，公开 GitHub 仓库为 0，且带有 FOMO 推荐链接，不能视为已验证交易系统 | [0xboan Solana meme 币筛查台](reports/investment/2026/oxboan-solana-rug-filter-desk/README.md) |
| 2026-11-21 | 作者黄金框架把黄金视为储值资产，并写明当前价位偏高、个人不会参与；文中 9 月 1 日 4434 美元更接近盘中价而非收盘，不能当成买入信号 | [黄金宏观周期框架](reports/investment/2026/jonylin-gold-macro-framework/README.md) |
| 2026-11-21 | 财报后 IV 回落可让方向正确的 Call 仍亏损；文中约 40% 亏损与 90%→50% 的 IV 没有交割单核验，这是风险教育不是已验证交易系统 | [财报 IV 回落与 VIX/IV/HV](reports/investment/2026/soberoption-earnings-iv-crush/README.md) |
| 2026-11-21 | Kobeissi 认为这是正常调整而不是 AI 泡沫破裂，并明确说不认为已经见底；文中多项数字未逐项复核，且作者推广付费订阅，不能自动执行 | [AI 调整还是泡沫破裂](reports/investment/2026/kobeissi-ai-correction-not-bubble/README.md) |
| 2026-11-21 | 官方债务表支持 2027-09-15 约 10.1 亿美元和 2028 年合计约 49 亿美元的可转债回售窗口；跌破成本不会自动强平，但储备和现金须以官方更新为准，不能排除更远期压力 | [微策略回售窗口与卖压](reports/investment/2026/mstr-convertible-put-reserve/README.md) |
| 2026-11-21 | 作者承认公开 AI 实盘测试中亏钱的模型更多；提示词给出研究闸门和风控清单，但没有可独立核验的收益，不能视为已验证交易系统；通用助手不应按提示词自动下单 | [一人AI基金、策略工厂与预测市场提示词交易台](reports/investment/2026/waveking-ai-prompt-trading-desk/README.md) |
| 2026-11-20 | 已核验的机制里没有零风险、可直接照搬的稳定套利；实盘执行若要做，只能是隔离的确定性程序，通用助手不持有私钥、不下单 | [跨策略风险与 Bot 架构评估](reports/arbitrage/2026/cross-strategy-risk-and-bot-architecture/README.md) |
| 2026-11-20 | 三个天气账户经济口径为正，但高价 NO 的高胜率不是锁定收益；三段视频没有逐帧复核 | [天气市场](reports/arbitrage/2026/polymarket-weather-markets/README.md) |
| 2026-11-20 | AI V2 是方向性价值投注，不是无风险套利；没有公开钱包、源码或样本外成绩 | [AI V2 价值投注](reports/arbitrage/2026/polymarket-ai-v2-value-betting/README.md) |
| 2026-11-20 | 24 条链接收成 23 个独立帖；廉价 YES 的完整地址是 `0x6e1d5040d0ac73709b0621f620d2a60b80d2d0fa`，100 笔买入里有 31 笔 NO | [2026-11-20 去重索引](reports/arbitrage/2026/batch-2026-11-20-triage/README.md) |
| 2026-11-20 | YES+NO 小于 1 不是净利的充分条件；mo-money 与附录钱包 `0xfcda…eecc` 不合并收益 | [mo-money 完整集合](reports/arbitrage/2026/polymarket-mo-money-complete-set/README.md) |
| 2026-11-20 | 视频看板是 133.70 到 14,880.00 美元，与正文 68 到 75 万美元不一致；FOMO 未授权自动化仍是阻塞项 | [xmglia / FOMO](reports/arbitrage/2026/xmglia-fomo-ai-arbitrage-claims/README.md) |
| 2026-11-20 | 回测图按连续 5 年、无追加资金折算，复合年化约 6.56%，不是标题上的 12% | [foodloss / EA](reports/arbitrage/2026/foodloss-ai-trading-desk-ea-backtest/README.md) |
| 2026-11-20 | 67% 胜率、夏普 2.3 和 2,847 美元纸面周收益都是作者自述，没有钱包、代码或市场 ID | [强化学习择时](reports/arbitrage/2026/polymarket-rl-timing-claims/README.md) |
| 2026-11-20 | 区块 21960556 的原子多池循环历史上已成功；构建者转账远大于发起地址的净增加，没有 2026 年池状态模拟 | [以太坊区块 21960556](reports/arbitrage/2025/eth-21960556-multipool-atomic/README.md) |

套利分类总表、案例时间和证据状态见 [reports/arbitrage/README.md](reports/arbitrage/README.md)。投资类报告见 [reports/investment/README.md](reports/investment/README.md)。金融传闻核验见 [reports/research/README.md](reports/research/README.md)。

固定跟踪分支 `latest-reports` 已存在。它提供不随 PR 分支改名的阅读入口：套利索引是该分支上的 `reports/arbitrage/README.md`，投资索引是该分支上的 `reports/investment/README.md`，传闻核验索引是该分支上的 `reports/research/README.md`。本提交只更新 `latest-reports`，不合并 `main`。仓库里没有会自己写报告的定时任务，也没有自动监控或自动交易。

## 套利研究

新案例使用 [templates/arbitrage-report.md](templates/arbitrage-report.md)。这些文件只记录研究，不运行交易。

## 投资研究

方向性投资、配置、期权、择时、收益策略和投研方法放在 [reports/investment/README.md](reports/investment/README.md)，与 `reports/arbitrage/` 并列。这些笔记记录研究，不构成交易指令。

## 传闻核验

金融传闻与公开事实核验放在 [reports/research/README.md](reports/research/README.md)，与 `reports/arbitrage/`、`reports/investment/` 并列。这些笔记记录核验，不是套利，也不是可执行策略，不构成交易指令。
