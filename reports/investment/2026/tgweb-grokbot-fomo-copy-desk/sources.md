# 来源

本目录对应报告：[README.md](README.md)。扫描覆盖 2026-11-24 12:12 至 16:13 Asia/Shanghai（UTC 04:12:00 至 08:13:24），账号 @FeiShen370926。本帖的发帖时间早于该窗口，本轮因新书签首次详细评估。下列材料只用于研究核验，不构成交易指令，也不包含会话令牌或绕过条款的实现。

## A. 本次扫描读到的帖子

| 编号 | 材料 | 地址 | 用到的字段或内容 |
| --- | --- | --- | --- |
| A1 | @TGweb3333 原帖 | https://x.com/TGweb3333/status/2125031652699029721 | 2026-11-24 09:00 Asia/Shanghai（UTC 01:00）。书签列表第 2 位，位于此前顶部书签 miles_mazy AGY 之前。宣传十页提示词和通宵盯盘 |

新书签第 1 位是 @AIExplorerTim，https://x.com/AIExplorerTim/status/2124692670534865392 。本轮不单开报告。该帖第 7 项的短链接未能解析，不把未打开的仓库名写成已核对原链。

## C. OCR 与未核来源

十张图使用 Tesseract 识别。下面是扫描记录中的主线，等级 C，个别词可能错误。

| 编号 | 内容 | 限制 |
| --- | --- | --- |
| C1 | 五个角色：Watcher、Vetter、Sizer、Executor、Guard；iPhone 网页和推送；用户自己登录；通过屏幕上的 Chrome 点击 FOMO 网页的 Buy / Sell | 不提供点击脚本 |
| C2 | 提示词写明不要密码、助记词、私钥或 2FA，不要点 Withdraw。默认 PAPER。LIVE 需用户输入确认。提现只按用户命令，由用户确认和 2FA | 这些是材料里的边界，不是已经审计的实现 |
| C3 | 材料称 FOMO 没有公开交易 API，并提到非官方主机 https://prod-api.fomo.family ，以及从 Chrome 调试端口读取 Bearer 会话令牌、约 69 分钟过期，只用于 READ / VERIFY | 过期时间来自 OCR，未对照官方文档。本目录不写读取令牌或调用接口的步骤 |
| C4 | 鲸名单：24h / 7d / 30d 至少出现在两个窗口；胜率不低于 55%；7 日至少 20 笔；持仓中位数不低于 15 分钟；单一币种不超过 7 日盈亏的 40%；按 7 日盈亏乘胜率排序，取前 25 | 无样本。OCR 可能认错阈值 |
| C5 | Whale proof：三个鲸最近五笔要在 60 秒内对上链上签名；匹配率低于 80% 则停止，不得进入 PAPER 夜盘 | 无日志 |
| C6 | 现金示例 100 美元 | E。不是实盘成绩 |
| C7 | 技术栈被写成 Python 3.12、asyncio、Playwright、SQLite | 只记录材料中的名词，不提供工程实现 |
| C8 | 油管课程 4,000 美元；「一手内部信号」 | C/D。本轮未找到来源页 |

## 利益冲突

| 编号 | 材料 | 地址 | 处理 |
| --- | --- | --- | --- |
| R1 | FOMO 推荐入口 | https://fomo.family/r/Quickscout | 引流。不打开账户，不连接钱包 |

## 明确不记录的实现

- 不记录如何打开浏览器调试端口，如何复制 Bearer 令牌，或如何刷新约 69 分钟的会话。
- 不记录如何调用 `prod-api.fomo.family`。
- 不记录 Playwright 或屏幕点击 Buy / Sell / Withdraw 的步骤。
- 不记录任何助记词、私钥、密码或 2FA 的存放方式。

## 相邻但不合并

- [Grok Bot 全天自动交易 Meme 币](../linda-grokbot-meme-intraday/README.md)
- [Grok Bot 八代理加密交易台](../bober-smart-grokbot-eight-agent-desk/README.md)
- [0xboan Solana meme 币筛查台](../oxboan-solana-rug-filter-desk/README.md)

评估过程中没有连接钱包，没有调用 FOMO 的网页或接口，没有下单。
