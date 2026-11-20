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
