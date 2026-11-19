# 来源与证据边界：mo-money 完整集合

案例报告：[README.md](README.md)。分级规则见 [归档规范](../../../../docs/arbitrage-archive.md)。

研究记录的取证窗口是北京时间 2026-11-20 02:17—02:23。本次归档在同一上海日历日重新打开了官方费率页、结算说明和四笔 Polygon 交易。账户统计接口没有重拉，因此不使用更晚的盈亏或成交量替换 02:00:01 的记录。采集过程中曾保存帖文、统计和浏览器文本，那些原始快照不进入本仓库。

## 帖文与媒体

| 材料 | 链接 | 本次边界 |
| --- | --- | --- |
| 原帖 | [x.com/Twiggynberries/status/2123351737004142760](https://x.com/Twiggynberries/status/2123351737004142760) | 公开读取记录给出 `created_at` = `2026-11-19T09:44:38.000Z`，即北京时间 2026-11-19 17:44:38。完整长文包含 560,370 美元、107,973 次、2,880 万美元交易量、单笔最高 2,719 美元，以及 48¢+49¢ 的例子。帖文自己写明收益数据有待完整交易记录验证。线程续页没有返回实质讨论 |
| 账户链接 | [polymarket.com/@mo-money?via=ace-cq9c](https://polymarket.com/@mo-money?via=ace-cq9c) | 这是带推荐参数的主页，不是裸链上地址。去参数主页为 [polymarket.com/@mo-money](https://polymarket.com/@mo-money) |
| 视频 | [video.twimg.com 的公开 MP4](https://video.twimg.com/amplify_video/2123351594439675904/vid/avc1/720x820/J268Zawt8PNsuEKJ.mp4) | 时长记录为 49.9 秒。复核结论见报告的媒体证据：主要是自定义面板，没有足够完整的可独立验证账本 |
| 预览图 | [pbs.twimg.com 预览图](https://pbs.twimg.com/amplify_video_thumb/2123351594439675904/img/TAs7jijU7qJOJ_DH.jpg) | 预览图含有截断地址。不能据此写成视频中绝无地址 |

## 研究记录中的官方账户字段

下列数字来自该时点的公开接口，本次归档没有重拉。

| 材料 | 链接 | 记录中的字段 |
| --- | --- | --- |
| 公开搜索 | [gamma-api public-search](https://gamma-api.polymarket.com/public-search?q=mo-money&search_profiles=true&limit_per_type=5) | 精确名称 mo-money，pseudonym Amazing-Mail，proxyWallet `0x32ed2e546b187ca15e2841edc82b22c713cf8ec3`。结果中的近似名称未采用 |
| 公开档案 | [gamma-api public-profile](https://gamma-api.polymarket.com/public-profile?address=0x32ed2e546b187ca15e2841edc82b22c713cf8ec3) | 同一名称与 proxy。记录为 takerTier=2、Silver、weightedVolume=173702.631924。`createdAt` 记录为 `2025-08-07T17:56:13.986357Z` |
| 统计 | [data-api v2 user-stats](https://data-api.polymarket.com/v2/user-stats?user=0x32ed2e546b187ca15e2841edc82b22c713cf8ec3) | 记录 timestamp=1795111201，即北京时间 2026-11-20 02:00:01，source_block=97603821。各盈亏与成交量字段见报告，口径不相加。deposits、withdrawals、cashflow_net 为 null |
| 活动抽样 | [data-api v2 activity](https://data-api.polymarket.com/v2/activity?user=0x32ed2e546b187ca15e2841edc82b22c713cf8ec3&limit=20) | 最新 20 项，`has_more=true`。不是全历史 |

主页显示记录为 Total PnL 约 +601.5K、Biggest Win 2719.58、Markets Traded 114,319、Total Volume 32.6M。页面简写不自动当成美元成交额。

## 本次重新打开的链上交易

四笔都属于页面标题 [Bitcoin Up or Down - November 19, 1:15PM-1:20PM ET](https://polygonscan.com/tx/0xe0b7953e1c2c0a107d91599f1d812e62910e99ea04ebc860cb52139f93d7d496) 这一五分钟市场，conditionId 为 `0xe9672a35fc7c41bb10a001f707b076d0beb1d219a9b7d75dad881f5532f95fba`。浏览器顶部动作有时概括的是同一批次里的其他交易者。下表只采用 mo-money 自己的转账和订单事件。

| 标识 | 链接 | 本次读到的 mo-money 流量 | 不采用的页面元素 |
| --- | --- | --- | --- |
| C1 | [0x58a02190…](https://polygonscan.com/tx/0x58a0219048eba8e26446e34c705b4c30c6b26e519e656fba597d1819d2732c45) | 北京时间 2026-11-20 02:15:04。mo-money 付出 240 pUSD，收到互补结果 token 500 份。对应 OrderFilled 里 mo-money 是 maker，fee 为 0 | 顶部动作写的是另一名交易者买入 Up。外层 gas 不记成该账户自付 |
| C2 | [0xb71277a5…](https://polygonscan.com/tx/0xb71277a50268076697ef3516db8d7cc8231dccde243e738b8926044afc183ce0) | 北京时间 2026-11-20 02:15:44。mo-money 付出 5.7936 pUSD，收到同一互补 token 36.21 份 | 顶部动作写的是另一名交易者买入 45 份 Up。批次中的其他费用不记到 mo-money |
| C3 | [0x07e8d427…](https://polygonscan.com/tx/0x07e8d427a187334bbf7f9186829f7409b684cd13b8e93eacb3674d0e2e67cdf8) | 北京时间 2026-11-20 02:18:22。mo-money 收到 536.21 份 Up，付出 498.6753 pUSD，另有 2.4435 pUSD 费用。合计付出 501.1188 pUSD。mo-money 在该笔中是 taker | 外层发送者是 `0x46C47B4C9532AD62bA92Fb849A9270E8474c08A2`，交易费 0.094196561651808504 POL 记在该地址 |
| C4 | [0xe0b7953e…](https://polygonscan.com/tx/0xe0b7953e1c2c0a107d91599f1d812e62910e99ea04ebc860cb52139f93d7d496) | 北京时间 2026-11-20 02:18:46。两枚互补 token 各销毁 536.21 份，mo-money 收到 536.21 USDC.e。抵押品合约是 `0x2791Bca1f2de4661ED88A30C99A7a9449Aa84174` | 转账旁的美元是页面现价换算。外层发送者是 `0xF8C16afDe13F60Fa86554A6e250BfF564A737F8F`，交易费 0.060417081439806919 POL 记在该地址 |

pUSD 合约记录为 `0xc011a7e12a19f7b1f670d46f03b03f3342e82dfb`。它和 USDC.e 不是同一个合约。

## 本次重新打开的规则页

| ID | 链接 | 支持 | 限制 |
| --- | --- | --- | --- |
| D1 | [价格与订单簿](https://docs.polymarket.com/concepts/prices-orderbook) | 研究记录采用的规则：中间价或末笔成交价不是可成交价；CLOB 在链下撮合、链上结算 | 单笔结算的原子性不证明两腿订单同时成功。本次归档没有重读该页全文 |
| D2 | [持仓管理](https://docs.polymarket.com/trading/positions/manage) | 完整集合可以 split、merge、redeem；CTF 与 Protocol V2 路由不同 | 具体市场的抵押品和版本要逐个看 |
| D3 | [Fees](https://docs.polymarket.com/trading/fees) | 本次读到：生效前公式 `fee = C × feeRate × p × (1 − p)`，C 为份数。Crypto 系数 0.07，Weather 0.05，Geopolitics 0。Maker 平台交易费为 0。费用四舍五入到小数点后 5 位，最小收费 0.00001。当前规则维持到 2026-11-20 23:59 UTC | 市场自身参数优先于类别表。Crypto 行的 20% 是 maker rebate 栏目，不是 Silver 的 8% taker 返佣 |
| D4 | [2026 年 11 月费改公告](https://docs.polymarket.com/programs/fee-and-rebate-changes-november-2026) | 本次读到：2026-11-20 23:59 UTC 生效，即北京时间 2026-11-21 07:59。此前旧规则继续有效。BTC 5 分钟和 15 分钟涨跌系数改为 0.05，其他 Crypto 改为 0.01，Weather 改为 0.01，Geopolitics 仍为 0。Silver 档取消；30 日 taker 加权量低于 20 万美元则 taker 返佣为 0；Gold 改为 10% | 新的加权定义去掉类别乘数。研究时点的 weightedVolume 不能直接套进新门槛 |
| D5 | [Taker Rebate Program](https://docs.polymarket.com/programs/taker-rebates) | 本次读到：当前 Silver 为 30 日加权量 20,000 美元档、返佣 8%；Gold 为 18%。返佣向后适用、按日以 pUSD 支付、最低支付额 1 pUSD，规则可改 | 档案上的当前档位不是每一笔历史成交的档位。返佣不保证到账，也不能在未查明口径时再次加进平台 PnL |
| D6 | [Resolution](https://docs.polymarket.com/concepts/resolution) | 本次读到：胜方通常每份赎回 1 美元，负方为 0。UMA 的 Unknown/50-50 情形下每份赎回 0.50 美元。涨跌市场使用 Chainlink TWAP | 不把通用规则未经核对地套到帖文未命名的旧市场 |
| D7 | [钱包活动说明](https://docs.polymarket.com/trading/wallet-activity) | 研究记录采用的字段区分：份数成交量、美元成交量、不同市场数、累计 PnL 不能再求和 | 一次 20 项读取不是全量会计 |
| D8 | [市场详情](https://docs.polymarket.com/market-data/market-details) | condition、market、token、版本和费率需要具体市场 ID | 帖文例子没有给出可复核的市场 ID |
| D9 | [公开搜索接口](https://docs.polymarket.com/api-reference/search/search-markets-events-and-profiles) | 官方搜索参数 | 只采用精确账户名 |
| D10 | [按钱包读取公开档案](https://docs.polymarket.com/api-reference/profiles/get-public-profile-by-wallet-address) | 地址与用户名可以对照 | 不能证明背后的自然人身份 |
| D11 | [活动接口迁移说明](https://docs.polymarket.com/api-reference/core/get-user-activity) | 研究记录写明 v1 已退役，实际使用的是 v2 活动地址 | 文档路径曾有 404，不把失效路径当成数据 |

## 条件算术

Q=100、价格 0.48 与 0.49、两腿都按 taker 计费，是假设例子，不是订单簿快照。公式和结果写在报告里。抽样四笔的脸面差额也只说明可见流量，不是账户总利润。

## 明确没有取得

原帖发布当时的账户快照、税务对话、107,973 的统计单位、全量成交与资金转移、每笔历史费率和 maker 比例、完整库存批次、初始或峰值资本、现金流，以及 pUSD 与 USDC.e 的兑换对账。第三方网站上的旧统计没有当作作者策略或全历史业绩。
