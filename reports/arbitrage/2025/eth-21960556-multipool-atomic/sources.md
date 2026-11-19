# 来源与证据边界

案例报告：[README.md](README.md)。分级规则见 [归档规范](../../../../docs/arbitrage-archive.md)。

复核日：2026-11-20 Asia/Shanghai。下表“本次访问”指这一次归档时的公开页面读取，不是持续监控。

| 编号 | 来源 | 地址 | 本次访问 | 可以支撑 | 不能支撑 |
| --- | --- | --- | --- | --- | --- |
| S1 | Etherscan 交易页 | https://etherscan.io/tx/0xcfb8d71e8e73f96c4ea215bd3a5305b4b4d93fc92e340a914e51b2aab70a5911 | 页面内容已取回 | 状态 Success、区块 21960556、时间 Mar-02-2025 05:02:47 PM +UTC、from/to、value 1 wei、gas limit 7,140,000、gas used 4,759,691、gas price 与 base fee 46.634190131 Gwei、max priority fee 0、交易费 0.221964335058809521 ETH、Ether Price 字段 2,518.51 美元/ETH、beaverbuild 转账、发起地址回款、MPL 循环的 ERC-20 数量、Logs (242)、ERC-20 Tokens Transferred: 131、概览标题和部分动作列表 | 转账旁边的美元金额。它们与页面顶部当时的 ETH 现价横幅一致，不是 Ether Price 字段。动作列表写明还有未展开部分，因此不能当作完整场所普查。未解码完整 calldata，未做账户状态差分 |
| S2 | Blockscout 交易只读接口 | https://eth.blockscout.com/api/v2/transactions/0xcfb8d71e8e73f96c4ea215bd3a5305b4b4d93fc92e340a914e51b2aab70a5911 | JSON 已取回 | 与 S1 交叉确认：result success、block 21960556、timestamp 2025-03-02T17:02:47.000000Z、相同 from/to、value 1、gas_used 4759691、gas_limit 7140000、gas_price 与 base fee 46634190131 wei、priority fee 0、fee 与 burnt fee 221964335058809521 wei、historic_exchange_rate 2518.51、区块内位置 1、nonce 55253、type 2。`to` 的 OLI 标签名为 Beanstalk3，`is_verified` 为 false | `token_transfers_overflow` 为 true，接口只返回了 10 条代币转账，不能用来点数。`exchange_rate` 1773.59 是接口当时给出的现价字段，不进入历史收入。OLI 标签不是控制人身份 |
| S3 | EigenPhi 原帖 | https://x.com/eigenphi/status/1896606664843002079 | x.com 直接打开返回 403。公开转载接口 https://api.fxtwitter.com/eigenphi/status/1896606664843002079 返回正文 | 帖文称 44 个交易场所、24 种代币，点名 Curve、MakerDAO、Balancer、Uniswap V2/V3/V4、Bitcoin.com Verse、Pancake、Fluid；收入 1.58 万美元，向 beaverbuild 支付 5.6 ETH，留下约 1,500 美元。帖文创建时间显示为 2025-03-03 17:00:40 UTC | 44 与 24 的逐场所、逐代币复点。1.58 万美元和约 1,500 美元所使用的价格时点。帖中短链 https://bit.ly/4ijw5OQ 本次返回 404，落点未知。配图未做识别 |
| S4 | Flashbots 文档，Bundle Inclusion Troubleshooting | https://docs.flashbots.net/flashbots-auction/advanced/troubleshooting | 文档页已取回 | 私有 bundle 未出现在链上的一般原因：捆绑内交易失败、激励不足、竞争报价更高、送达过晚、目标时隙的验证者未运行 mev-boost 或构建者未连到同一中继。文档说明 Flashbots 路径下失败交易通常不会出现在链上；竞争报价在上链前不可见 | 本笔使用了 Flashbots、属于某个 bundle、或私有提交已经排除竞争。文档示例里的区块号、gas 和地址属于文档自身的例子，与本笔无关 |
| S5 | 2025-03-02 ETH 日线的公开摘要 | https://coinmarketcap.com/historical/20250302/ ；检索摘要中另有 2,518.10 与 2,518.11 美元的日线收盘表述 | 检索到 CoinMarketCap 历史快照页上的 2,519.69 美元，以及其他公开摘要中的邻近收盘价 | 说明 2,518.51 附近在同一 UTC 日存在不同的日线收盘口径 | 本笔 17:02:47 UTC 的逐笔成交价。这些日线数字不替换 S1/S2 的历史汇率字段 |
| S6 | 此前研究底稿 | 本次归档任务中给出的既有结论 | 作为待复核文字，不作为链上来源 | 提供了需要复核的口径：六位小数净增加、单条 WETH 循环、费用尚未分摊、资金来源未知 | 在与 S1/S2 冲突时，以页面原始字段和由这些字段做的精确算术为准 |

## 本次页面中能对上的场所标签

以下名称出现在 S1 取回的文本里，只证明这些标签出现过，不证明场所总数：

- Uniswap V2、Uniswap V3、Uniswap V4
- Balancer，包括标签 Balancer: MPL/USDC 50/50
- Curve，包括多个 Curve 池标签
- Fluid
- MakerDAO: sDAI Token

S3 还点名 Bitcoin.com Verse 和 Pancake。这两个名字在 S1 本次取回文本中没有检索到。没有检索到名字，不能推出链上不存在相应调用。

## 明确没有取得的材料

- x.com 原始页面。
- bit.ly 短链的跳转目标。
- 原帖配图中的表格或路径图。
- 完整调用栈、状态差分和期初库存。
- 2026-11-20 当日各池的只读模拟。
- 发起地址在其他成功或失败交易上的成本。
- 研发、节点和人员成本。

未取得的材料保持空白，不从其他交易或当前报价外推。
