# Batch 3 全量去重索引与低噪音归档备忘

- 研究日：2026-11-20，北京时间（Asia/Shanghai）。24 条提交 URL、23 个独立帖子 ID。查询参数不影响帖子身份。
- 帖文正文来自当天的公开读取。原始缓存不进入本仓库。
- “#编号”是独立帖序号。“提交序号”是用户原 24 条列表的位置，避免重复项之后全部错位。
- 本目录是分拣索引。C4 追加到 [mo-money 完整集合](../polymarket-mo-money-complete-set/README.md)。C1、C3 指向已经归档的报告，不另开新案。归档规则见 [docs/arbitrage-archive.md](../../../../docs/arbitrage-archive.md)。

## 1. 每一条用户链接的归属

| 提交序号 | triage编号 | 独立帖子 | 家族 | 处理结论 |
|---:|---|---|---|---|
| 1 | #1 | [bkdgiffug / 2123269535033627130](https://x.com/bkdgiffug/status/2123269535033627130) | C11 | 数据接口工具，非套利；见C11简评 |
| 2 | #2 | [Cora64189920179 / 2123471729213509841](https://x.com/Cora64189920179/status/2123471729213509841) | C12 | 追原帖EMA20/15分钟外汇Article；LINE引流，未有套利闭环 |
| 3 | #3 | [AKKY33157665 / 2123283773923930189](https://x.com/AKKY33157665/status/2123283773923930189) | C5b | C5家族深研；与#20同钱包不同归因 |
| 4 | #4 | [CDanielleD1997 / 2123352319437783165](https://x.com/CDanielleD1997/status/2123352319437783165) | C7 | [廉价 YES 钱包核验](c7-cheap-yes-wallet-check.md)。公开主页已映射完整地址 `0x6e1d5040d0ac73709b0621f620d2a60b80d2d0fa` |
| 5 | #5 | [linda6248130564 / 2123265104674439213](https://x.com/linda6248130564/status/2123265104674439213) | C5c | C5家族深研；无钱包/代码，动量自述 |
| 6 | #6 | [crbpite8 / 2123249539465335203](https://x.com/crbpite8/status/2123249539465335203) | C5d | C5家族深研；钱包不只做98–99¢尾盘 |
| 7 | #7 | [PapiSleepy_RF / 2123322399265280427](https://x.com/PapiSleepy_RF/status/2123322399265280427) | C2 | C2模板备忘；与#21同QKL2058 |
| 8 | #8 | [chenke20266 / 2121987007333441920](https://x.com/chenke20266/status/2121987007333441920) | C9 | [AI V2 价值投注](../polymarket-ai-v2-value-betting/README.md) |
| 9 | #9 | [ElianeAmar83560 / 2123246982290719126](https://x.com/ElianeAmar83560/status/2123246982290719126) | C6 | [天气市场](../polymarket-weather-markets/README.md) |
| 10 | #10 | [rgk_degen / 2123504330992939014](https://x.com/rgk_degen/status/2123504330992939014) | C2 | C2英文对照；同一ID重复提交两次，未验证收益 |
| 11 | #10（重复提交） | [rgk_degen / 2123504330992939014](https://x.com/rgk_degen/status/2123504330992939014) | C2 | 重复上一条，同ID，参数不同；不再研究 |
| 12 | #11 | [Huahuazo / 2123443934638506025](https://x.com/Huahuazo/status/2123443934638506025) | C11 | 投研工具，非套利；见C11 |
| 13 | #12 | [linda6248130564 / 2123313309143400562](https://x.com/linda6248130564/status/2123313309143400562) | C2 | C2 GTA meme；Pumpner，与QKL2058非同账户证据 |
| 14 | #13 | [CasaVerilla / 2123238871290769847](https://x.com/CasaVerilla/status/2123238871290769847) | C4 | C4追加既有mo-money附录，不新开策略 |
| 15 | #14 | [Web3Yjy / 2123439672106058051](https://x.com/Web3Yjy/status/2123439672106058051) | C2 | C2开源库/GMGN引流；链接截断、无收益账本 |
| 16 | #15 | [ElianeAmar83560 / 2123299666636976144](https://x.com/ElianeAmar83560/status/2123299666636976144) | C8 | C8学生/iPad模板；无钱包/代码 |
| 17 | #16 | [yumekawii_s2 / 2123243840928641312](https://x.com/yumekawii_s2/status/2123243840928641312) | C6 | [天气市场](../polymarket-weather-markets/README.md) 的站点口端子类型。不是 #9 的同一个钱包 |
| 18 | #17 | [cryptoxxw / 2123464396588687377](https://x.com/cryptoxxw/status/2123464396588687377) | C8 | C8无具体钱包；天气自述仅供C6背景 |
| 19 | #18 | [LabSpeculation / 2123219518201938300](https://x.com/LabSpeculation/status/2123219518201938300) | C10 | C10 RSI(2)简评；规则可编程，非套利 |
| 20 | #19 | [Twiggynberries / 2123237674723037248](https://x.com/Twiggynberries/status/2123237674723037248) | C3 | C3已分析RL故事改写，跳过重复深研 |
| 21 | #20 | [KimSun78012382 / 2123327573337764341](https://x.com/KimSun78012382/status/2123327573337764341) | C5a | C5家族深研；追引用@0x50f7作背景，别混为同算法 |
| 22 | #21 | [crbpite8 / 2123567750526456170](https://x.com/crbpite8/status/2123567750526456170) | C2 | C2模板，与#7同QKL2058；非BTC尾盘案 |
| 23 | #22 | [xmglia / 2122935538659524736](https://x.com/xmglia/status/2122935538659524736) | C1 | 并入已归档的 [xmglia / FOMO](../xmglia-fomo-ai-arbitrage-claims/README.md)，这是其直接原帖 |
| 24 | #23 | [xmglia / 2123428583054221566](https://x.com/xmglia/status/2123428583054221566) | C1 | 引用 #22，同一原帖和推荐码。69.67 到 13,370 与已归档数字不是同一条净值 |

## 2. 新深研与附录的交接

- **C5**：[#3、#5、#6、#20](../polymarket-5m-btc-microstructure/README.md)。两个 viniangusso 叙事合并，不当成两次独立成功。
- **C4**：追加到 [mo-money 完整集合](../polymarket-mo-money-complete-set/README.md) 的钱包附录。地址 `0xfcda969d818f49fb945b889275405f929221eecc`。页面 headline 48,849.52 美元，economic_pnl 34,493.84 美元。最近样本是 BTC 五分钟盘，不只是 15 分钟。67 秒视频没有逐帧审查。
- **C7**：[廉价 YES 钱包核验](c7-cheap-yes-wallet-check.md)。完整地址 `0x6e1d5040d0ac73709b0621f620d2a60b80d2d0fa`。headline 926,637.06 美元，economic_pnl 765,829.29 美元。样本里有 NO 和高价 YES，不是“只买 1–15¢ YES”。约 33.8 秒视频没有逐帧审查。
- **C9**：[AI V2 价值投注](../polymarket-ai-v2-value-betting/README.md)。
- **C6**：[天气市场](../polymarket-weather-markets/README.md)。三段视频只看了封面和约 5 秒抽帧，没有逐帧复核。

## 3. 为什么不重复深研

### C3：已分析RL，不是又一个独立算法

#19 Twiggynberries 没有直接引用原帖，但 18 个月、200 万轮强化学习、67% 胜率、2.3 夏普、纸面一周 2,847 美元和天气/伊朗例子，与已归档的 [强化学习择时](../polymarket-rl-timing-claims/README.md)（原帖 [2123315135192146050](https://x.com/polraviraj/status/2123315135192146050)）是同一故事。按内容指纹去重，不只按 URL 去重。换语言或换作者，不使这些自述获得独立验证。

### C1：并入已归档的 xmglia 原帖链

#22 [2122935538659524736](https://x.com/xmglia/status/2122935538659524736) 是已归档 [xmglia / FOMO](../xmglia-fomo-ai-arbitrage-claims/README.md) 所分析用户帖 [2123338427840270444](https://x.com/xmglia/status/2123338427840270444) 的直接原帖。#23 [2123428583054221566](https://x.com/xmglia/status/2123428583054221566) 引用 #22，使用同一提示词工具链和 FOMO 推荐码 `qkl2058`。#23 称 69.67 到 13,370。已归档报告里的正文是 68 到 750,000，已核对视频是 133.70 到 14,880.00。这些是不同快照或口径，不能连成同一条净值，也不另开新案。

### C2：隔夜meme/多代理/推荐码矩阵

范围 #7、#10、#12、#14、#21。共同点是小本金、极短周期、多个助手分工、精准倍数和几笔例子，但没有可复现的完整收益账本。#7 与 #21 共享 [pump.fun/u/QKL2058](https://pump.fun/u/QKL2058)。#23 和已归档的 xmglia 帖使用推荐码 `qkl2058`。这能证明推广标识重复，不能证明同一个钱包、同一个操作者，也不能据此判定诈骗。#12 用 Pumpner，#14 用另一个 GMGN 推荐码，不能写成所有链接同一个码。

#10 RGK是英文、声称自己研发、1小时1257笔，引用的长文却是“18 browser routines / seat成本优化”，不是业绩来源。可作为独立自述对照，但重复链接不等于两个样本；目前同样未给独立交易审计。

**逻辑/执行简评**：meme狙击是方向性和流动性竞争，不存在两个现金流事前锁定；LP销毁、开发者持仓比例、KOL与止盈规则不能排除rug、可卖性限制或MEV。专业程序能自动化数据/风控/发单，开发生产系统很难，通用聊天AI不能保证0.4秒执行或隔夜持续收益。库名列表只说明组件存在，不证明连接、部署、安全和策略alpha。只建共享高噪音备忘，不值得为每个换本金故事开长篇。

### C8：学生+iPad、AI+隔夜暴利模板

#15“21 岁交大学生 + iPad 副屏 + Claude Code/OpenClaw + 2 天搭系统”，和已归档 [xmglia / FOMO](../xmglia-fomo-ai-arbitrage-claims/README.md) 里“19 岁日本学生 + iPad”的结构相似。没有钱包和代码，叙事相似不等于抄袭已经证实。#17“50 到 5,273、先亏到 11 再转天气”所链的页面是 [polymarket.com/zh?via=Tgweb3](https://polymarket.com/zh?via=Tgweb3)，没有地址。“扫描 500–1,000 个盘、8% 优势、凯利 6%”不证明真实概率、成交或净值。只保留为模板对照。天气句子交给 [天气市场](../polymarket-weather-markets/README.md) 作背景，不把没有地址的自述当成另一个已核验钱包。

### C12：日文Grok Bot→LINE引流，而不是可验套利

#2 引用自己的 [2121641443798487540](https://x.com/i/status/2121641443798487540)，Article 讨论 EMA20 与 15 分钟外汇，并含 [lin.ee/VbjBtuH](https://lin.ee/VbjBtuH)。它和已归档的 [foodloss / EA](../foodloss-ai-trading-desk-ea-backtest/README.md) 体裁相似，但不是同一原帖，也不是同一份资料。多个助手、否决权和先做 demo 是工程建议，不是收益证据。EMA20 外汇方向交易不是套利。分工不会凭空产生正期望。本次没有点击 LINE，没有联系作者，没有领取或安装资料。资料未公开就不能审计。

## 4. C10：经典RSI(2)规则简评与自动化

#18 [LabSpeculation](https://x.com/LabSpeculation/status/2123219518201938300)给出规则：收盘>200日均线；RSI(2)<10收盘买；收盘回到5日均线上方卖；不设价格止损。它是趋势过滤的均值回归，不是双边锁定收益套利；规则明确，日频专用bot开发难度低至中，通用AI适合辅助编码和复盘而不是承诺收益。所谓33年胜率77%、年化5.2% vs持有10.7%、最大回撤15% vs55%、BTC单笔亏22%均为帖主/配图自述，本轮未复算，不标已验证。回测必须指定ETF/复权/分红、RSI平滑算法、交易时间和费用；用当天最终收盘价生成信号又无摩擦买在同一收盘会有前视/成交假设问题，应预先定义MOC或次日执行。无止损不能推出风险低，跨股票/BTC参数迁移、隔夜跳空和趋势转换仍可大亏；先做样本外含费用重放，不能用胜率比较替代资金占用/回撤评估。无需为公开指标规则另立“新套利”深研。

## 5. C11：开源数据/投研工具，不是套利方法

- #1：[a-stock-data](https://github.com/simonlin1212/a-stock-data)、[global-stock-data](https://github.com/simonlin1212/global-stock-data)，自称聚合 A 股和美港股数据。
- #11：[augur](https://github.com/BruceLanLan/augur)，多流派的投资研究工具。
- 本次只根据帖文里的链接识别用途。没有审查仓库源代码、许可证、数据质量或安全性，不声称宣传功能已经实测。
- 专用程序可以抓数和写投研摘要。这是研究基础设施，还没有入场、出场、对冲、可执行价差、资金和成本组成的策略闭环。免费封装不等于底层数据可以商用或高频使用。授权、延迟、复权、限流、源站变更、模型幻觉和依赖都要另核。能接模型，不等于能套利。

## 6. 归档纪律与下一轮去重键

1. 首要键：post ID（忽略`s=46`、`a=`、`via`等）；其次引用/转发原帖ID；再用完整钱包地址、策略机制和内容数字指纹。
2. 同钱包不同宣传规则先合并核验归因；同策略新钱包做附录，不把每个地址都新开机制报告；不同钱包不擅自合并所有权。
3. 名称像地址不一定真是完整钱包：C7应读公开profile映射；不能随意补位或把用户名当合约地址。
4. 账本字段统一：trades=不同市场数，trade_count=canonical fills，volume=份额，volume_usdc=美元；headline与economic_pnl分列；记录统计观察时间而不仅抓取时间。
5. 每条链接都有明确归属：已深研、附录、重复、非套利，或证据不足的短评。本批 23 条原帖都可读。引用链极深处的无关 meme [2123241925176385805](https://x.com/i/status/2123241925176385805) 没有继续追，不影响用户提交清单的覆盖。
6. 视频边界：C6 三段视频只看了封面和约 5 秒抽帧，没有逐帧复核。C5、C4、C7 的视频只看了预览，或没有逐帧审查。核心结论建立在公开账本、官方规则和算术上。有视频不等于收益已被证明。

本次没有交易，也没有把原始缓存、图片或视频放进仓库。公开 URL 已写在各案例的 `sources.md` 和本索引的表格里。
