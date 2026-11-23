# C5 来源与复核方法

研究读取时间：2026-11-20 10:41–10:44，北京时间。帖文正文来自该时段的公开读取，原始缓存不进入本仓库。全部为公开只读页面，没有认证账户或私钥。案例报告：[README.md](README.md)。

## 官方规则/接口

- [现行 Fees](https://docs.polymarket.com/trading/fees)：Crypto k=.07，maker0，费用5位小数。
- [费改公告](https://docs.polymarket.com/programs/fee-and-rebate-changes-november-2026.md)：北京时间2026-11-21 07:59生效，BTC5m/15m k=.05。
- [现行 Taker Rebates](https://docs.polymarket.com/programs/taker-rebates.md)：Bronze/Silver/Gold/Platinum/Diamond/Obsidian返费3/8/18/32/44/50%，对应30日加权量2k/20k/200k/1m/4m/10m；旧Crypto权重2.3；一次性升级奖金不能年化。
- 新制：<200k无taker返费；Gold10%、Platinum25%、Diamond40%、Obsidian50%、Onyx60%，阈值200k/1m/4m/10m/75m，移除类别倍数和升级奖金；同交易额可能降档。maker由每日池改30日加权量档：<200k无，200k/1m/4m/10m以上为3/7/10/15%，不是给成交额返这些比例。
- [Wallet Activity](https://docs.polymarket.com/trading/wallet-activity.md)、[Public Analytics](https://docs.polymarket.com/market-data/public-analytics)、[v2 OpenAPI](https://data-api.polymarket.com/v2/openapi.json)。`trades`、`trade_count` 和 PnL 的解释以这份 OpenAPI 为准。
- [抽查的 BTC 五分钟市场](https://gamma-api.polymarket.com/markets/slug/btc-updown-5m-1795142400)；[市场指定的 Chainlink 流](https://data.chain.link/streams/btc-usd-twap-60s-streams)。本次只核对市场写出的 URL，没有订阅或测量实时流。

## 原帖（证据为缓存正文，不代表宣传已核实）

- [AKKY 2123283773923930189](https://x.com/AKKY33157665/status/2123283773923930189)
- [Kim 2123327573337764341](https://x.com/KimSun78012382/status/2123327573337764341)
- [linda 2123265104674439213](https://x.com/linda6248130564/status/2123265104674439213)
- [crbpite8 2123249539465335203](https://x.com/crbpite8/status/2123249539465335203)
- 引用背景：[2123255265977913349](https://x.com/i/status/2123255265977913349) 提到 GoodFallen，[2123310249746759891](https://x.com/i/status/2123310249746759891) 提到 0x50f7。更深的无关 meme 链没有继续追。

## 钱包及本地原始证据

| 昵称 | Profile | 完整钱包 | 统计 | 最近 100 条活动 |
| --- | --- | --- | --- | --- |
| viniangusso | [@viniangusso](https://polymarket.com/@viniangusso) | `0x03b4c58b1bb31007cb97e2c8f2216d33c805d29c` | [user-stats](https://data-api.polymarket.com/v2/user-stats?user=0x03b4c58b1bb31007cb97e2c8f2216d33c805d29c) | [activity](https://data-api.polymarket.com/v2/activity?user=0x03b4c58b1bb31007cb97e2c8f2216d33c805d29c&limit=100) |
| gangwarharshit | [@gangwarharshit](https://polymarket.com/@gangwarharshit) | `0xaad03b403c831d0a8b484abe59ac25188b49f61d` | [user-stats](https://data-api.polymarket.com/v2/user-stats?user=0xaad03b403c831d0a8b484abe59ac25188b49f61d) | [activity](https://data-api.polymarket.com/v2/activity?user=0xaad03b403c831d0a8b484abe59ac25188b49f61d&limit=100) |
| GoodFallen | [@goodfallen](https://polymarket.com/@goodfallen) | `0x0ca4e9d27ff826a109ecbf74754fb66b93f277a6` | [user-stats](https://data-api.polymarket.com/v2/user-stats?user=0x0ca4e9d27ff826a109ecbf74754fb66b93f277a6) | [activity](https://data-api.polymarket.com/v2/activity?user=0x0ca4e9d27ff826a109ecbf74754fb66b93f277a6&limit=100) |
| 0x50f7 | [@0x50f7](https://polymarket.com/@0x50f7) | `0xee65685de42f8de9a03b4c53ee77d56a20d2cfc9` | [user-stats](https://data-api.polymarket.com/v2/user-stats?user=0xee65685de42f8de9a03b4c53ee77d56a20d2cfc9) | [activity](https://data-api.polymarket.com/v2/activity?user=0xee65685de42f8de9a03b4c53ee77d56a20d2cfc9&limit=100) |

网页把昵称映射到 proxyWallet。统计和活动使用下面两个公开接口，读取结果不另存进本仓库：

```
GET https://data-api.polymarket.com/v2/user-stats?user=<wallet>
GET https://data-api.polymarket.com/v2/activity?user=<wallet>&limit=100
```

`economic_pnl = position_pnl + wallet_income`；`fees_paid`是退款减charges披露，**不是再扣一次**；页面headline `trade_pnl`为兼容序列，不能当经济净收益。所有统计需要保留`all_time_pnl.timestamp`，不默认本次抓取时刻。

四段演示视频的时长记录约为 38.6 秒、18.8 秒、35 秒和 56 秒。本次只看预览或没有逐帧审查，视频文件不入库。画面不能替代交易和订单日志。报告里的主要结论不依赖视频。

## 2026-11-22 补充：@irongiantXBT / 0x76eca410…

研究读取约 2026-11-22 00:13–04:40 Asia/Shanghai。钱包公开数据读取时点约 2026-11-22 04:20–04:30 Asia/Shanghai。只读公开接口和公开帖文，未连接钱包、未下单。金额、持仓分类和活动计数见 [README.md](README.md) 第 3.4 节。不要把不同口径的盈亏加总成一个「真实总收益」，也不要把排行榜 `pnl` 解释成已隔离的最近 27 天收益。

### 帖文与视频

- 原帖：https://x.com/irongiantXBT/status/2124204194177356049 （2026-11-21 18:12:00 UTC）
- 回复中的钱包链接：https://x.com/irongiantXBT/status/2124208217123434690 ，指向 https://polymarket.com/profile/0x76eca4109d0dfe8649d5e3861dfccac67ae7d630
- 引用的长文帖：https://x.com/irongiantXBT/status/2122662343306059780 ，文章标题为 “Your Grok Bot Is Burning Money - Harness Fixes It”。正文是 Grok Bot / jev / harness 搭法，不是 5 分钟交易说明书；实体解析里该文章 URL 曾返回 404，但帖子对象里仍带有文章正文。
- 视频：主帖所附 24.04 秒视频，本轮已下载并观看。预渲染动画，界面写明 PAPER，损益保持 +$0。视频文件不入库。画面中没有钱包地址，也没有 5,340 或 12,640。

### 公开接口

- https://polymarket.com/profile/0x76eca4109d0dfe8649d5e3861dfccac67ae7d630
- https://data-api.polymarket.com/v2/positions?user=0x76eca4109d0dfe8649d5e3861dfccac67ae7d630
- https://data-api.polymarket.com/v2/activity?user=0x76eca4109d0dfe8649d5e3861dfccac67ae7d630
- https://data-api.polymarket.com/v2/value?user=0x76eca4109d0dfe8649d5e3861dfccac67ae7d630
- https://data-api.polymarket.com/v2/leaderboard?user=0x76eca4109d0dfe8649d5e3861dfccac67ae7d630&window=all
- Gamma 公共资料读取于本次扫描（`public-profile` 一类公开接口，创建时间 2026-05-30）

读取结果不另存进本仓库。活动翻页触及 40 页 / 4000 条上限，因此 TRADE 3812 不是全历史成交笔数。

## 2026-11-23 附录：late-to-tomorrow

- 主帖：https://x.com/linda6248130564/status/2124803436688679069 （2026-11-23 17:53:10 Asia/Shanghai）
- 跟帖：https://x.com/linda6248130564/status/2124803440090264024 （2026-11-23 17:53:11 Asia/Shanghai）
- 官方个人页（无推荐参数，账户身份以该页为准）：https://polymarket.com/@late-to-tomorrow
- 原帖中的推荐链接：https://polymarket.com/zh/@late-to-tomorrow?via=k3H86f8 。`via=k3H86f8` 只是推荐跟踪，不改变账户身份。
- 本轮记下的官方页字段：Joined Feb 2026；Total PnL +$199.1K；Total Volume 9.4M；Markets Traded 19,216。Positions Value 与 Biggest Win 的对应关系未核对，不写成精确当前持仓或单笔最大盈利。原帖视频未逐帧核验。
