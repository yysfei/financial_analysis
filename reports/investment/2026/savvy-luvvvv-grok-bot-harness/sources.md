# 来源与核验记录

评估对象：https://x.com/savvy_luvvvv/status/2124114560290267555  
评估时间：2026-11-22 Asia/Shanghai  
方法：使用内置公开 X 读取获取原帖、长文、作者时间线、对话回复与检索结果；用 GitHub 连接器只读访问 `yysfei/financial_analysis` 的 `latest-reports` 与 `main`，不克隆仓库；用网页抓取与检索核验官方文档。没有按原文提示词搭建系统，没有调用 TypeSafe，没有下单或连接钱包。

证据等级：A 本次打开的公开页面或接口上的原始字段，B 由 A 精确计算，C 第三方叙述，D 未访问或未完整查看，E 假设或示意图。

## 1. 原帖与作者

| 项 | 值 | 等级 |
| --- | --- | --- |
| 帖子 ID | 2124114560290267555 | A |
| URL | https://x.com/savvy_luvvvv/status/2124114560290267555 | A |
| 短链 | https://t.co/v76hRevWF6（帖子 `text` 字段仅此一条） | A |
| 发布时间 | 2026-11-21T12:15:49.000Z，合 2026-11-21 20:15:49 Asia/Shanghai | A / B |
| 文章标题 | 直接抄我的 Grok Bot 配置：完整的 Harness 文件夹 | A |
| 作者 | Ling，`@savvy_luvvvv`，id `1514060310` | A |
| 账号创建 | 2013-06-13T18:09:24.000Z | A |
| 简介 | “AI agents, model deep dives & tools before they go mainstream.” / “拆解前沿AI，构建智能体，让想法落地。” | A |
| 公开指标（读取时，约） | 关注者 964–965，正在关注 23，发帖 43，媒体 33；蓝标 `verified_type=blue` | A |
| 帖子公开指标（后一次读取） | 收藏 620，曝光 78,639，喜欢 241，引用 9，回复 20，转发 43 | A |
| 长文 `plain_text` 长度 | 2368 字（不含 11 条代码块的重复存储） | A |
| 代码块 | 11 条，语言标记为 xml，内容是提示词而非可运行 XML | A |
| 文章实体中的 URL | 仅 `https://www.eesel.ai/blog/grok-bot` | A |

11 条提示词已保存到评估时的提取目录，正文职责编号与 API 代码块顺序不一致。对应关系：

| 正文编号 | 职责 | API 代码块序号（1-based） |
| --- | --- | --- |
| 1 | 建空文件夹 | 8 |
| 2 | 写 GROK.md | 10 |
| 3 | 顾问 | 3 |
| 4 | 侦察员 | 5 |
| 5 | 构建者 | 7 |
| 6 | 验证者 | 11 |
| 7 | jev_seat | 6 |
| 8 | jev_done | 1 |
| 9 | 共写 GOAL.md | 9 |
| 10 | 启动 6 Bot 群聊 | 4 |
| 11 | 周五审计 | 2 |

## 2. 媒体

封面与 8 张 animated_gif（无 `alt_text`）。本轮查看了封面照片，以及成功下载的 4 张 GIF **静态预览帧**（图 1、图 5、图 7、图 8）。**没有**播放 8 段 `video.twimg.com/tweet_video/*.mp4` 动画。另 4 张预览图在下载时返回 HTTP 403，内容未看。

| media_key | 类型 | 本轮状态 | 预览中看到的内容 |
| --- | --- | --- | --- |
| 3_2124053663958073344 | photo，封面 | 已看 | 标题视觉：Grok Bot + Jev + Grok Build，「直接抄我的 GROK BOT 配置」，右侧文件夹示意图，P(done) ≥ 0.92，receipts/「17 个文件」 |
| 16_2124052127483830272 | animated_gif | 只看预览帧 | 图 1 文件夹结构，席位绑定 grok 4.7 / 4.3 / grok build 0.1，「17 个文件 / 17 项检查」 |
| 16_2124052694067286016 | animated_gif | 只看预览帧 | 图 5：示例 GOAL.md，限流「每分钟 20 次上传后返回 429」，17 项检查，范围之外含认证/计费/上传界面 |
| 16_2124052911932010496 | animated_gif | 只看预览帧 | 图 7：成本条形图，$1.58 对 $0.82，注明 token 数为作者自己的；66K 输出 $0.40 对 $0.13；100 次 $157.69 对 $81.79 |
| 16_2124052982480146432 | animated_gif | 只看预览帧 | 图 8：17/17 凭证墙，P(done) 0.95，示例命令 `k6 run upload_burst.js`，提交 `a41f9c2`，时间 2026-11-16 14:32。这是设计信息图，不是产品账单截图 |
| 16_2124052490907766785 | animated_gif | D，预览 403 | 未看 |
| 16_2124052803639181312 | animated_gif | D，预览 403 | 未看 |
| 16_2124052360020230144 | animated_gif | D，预览 403 | 未看 |
| 16_2124052593194233856 | animated_gif | D，预览 403 | 未看 |

未看的 4 段动画要核验的是：是否出现真实 Grok Bot 界面、用量页或发票，而不只是提示词幻灯片。对应 mp4：

- https://video.twimg.com/tweet_video/HXomfJzXUAExDGu.mp4
- https://video.twimg.com/tweet_video/HXomxW0WAAAw0f4.mp4
- https://video.twimg.com/tweet_video/HXomXiNWAAAPYq9.mp4
- https://video.twimg.com/tweet_video/HXomlG2W8AAYQpz.mp4

已看预览帧的 4 段 mp4 同样未播放，只根据静态首帧判断其为信息图。

## 3. 对话、引用与作者时间线

- 用 `conversation_id:2124114560290267555` 读取一页 25 条回复，仍有 `next_token`，未翻完全部更早回复（原帖回复计数约 20，本页已覆盖主要可见回复）。
- 有实质信息的一条：[Dzzzzzer 2026-11-21T23:01:42.000Z](https://x.com/Dzzzzzer/status/2124189836496023809)「为什么搭建了grok bot harness消耗的额度更快了啊」。这是使用者自述，不是受控实验（C）。
- 其余多是请 `@bot` 总结/学习，或短评「直接复制」「很实在」。未看到作者本人在本页里补充账单、仓库或 Jev 接入说明。
- `get_posts_quoted_posts` 返回结果混入了作者其他帖的转发，不能当作这 9 条引用的干净列表。未再逐条核验全部引用正文。
- 作者时间线读取 25 条（接口把 `max_results` 降到 25），仍有下一页。已足够判断同一账户近期还在发 SpaceXAI「月入 15 万美元」、Lauren skills、开源交易策略库、24/7 交易 agent、Wiza 联系人数据等宣传，并在其中引用本长文。那些外链未逐条展开核验。

近重复改写，不是原文：

- [@oreillnw/status/2124320724089516229](https://x.com/oreillnw/status/2124320724089516229)，2026-11-22T01:55:03.000Z，合 2026-11-22 09:55:03 Asia/Shanghai，晚于原帖约 13.5 小时。标题《别让 AI 自己给自己打分：6 个 Grok Bot 防烧钱流水线》。同一对数字 $0.82 / $1.58，同样 11 条提示词和 6 个 Bot。账号 `oreillnw` 创建于 2026-11-18。文章实体无 eesel 链接。

检索 `jev_seat.py OR jev_done.py OR "P(done)" OR "0.92" grok harness`、时间截止原帖发布之前，没有找到可确认为英文原文的更早帖；结果里大量噪声。Jev + GOAL.md + 席位这类写法在 2026 年相关内容里很常见（C），但不能指认某一篇为直接底稿。

## 4. 官方与第三方产品文档

| 主张 | 来源 | 结果 | 等级 |
| --- | --- | --- | --- |
| 共享一台云电脑，不能当安全边界 | https://docs.x.ai/grok-bot/faq | 相符 | A |
| 一屏一次电脑操作任务 | 同上 | 相符。正文括号里的「eesel」不见于该文档 | A |
| 群聊 2–6 个 Bot | https://docs.x.ai/grok-bot/chat-and-collaboration 「add two to six Bots」 | 相符 | A |
| 群聊回复计入用量，Bot 越多通常越费 | 同上 “Every Bot reply counts toward your usage, including replies in a group and messages between Bots” | 相符 | A |
| 审批/密钥请求不出现在群聊 | 同上 | 相符，与「把审批放进群聊文件夹」的操作想象不完全一致 | A |
| 约 50 个 Bot、群聊最多 6 个 | https://x.ai/news/designing-grok-bot “practical limits of roughly 50 Bots per account and six per group chat” | 相符（“roughly 50”） | A |
| 用户自选模型、按席位锁价 | https://docs.x.ai/grok-bot/faq 「Can I pick the model? No.」；用量不按模型名展示；路由到 Opus 5.5 也不改变每 token 费用 | **与原文核心成本假设冲突** | A |
| Grok Bot 计费 | FAQ「How much does Grok Bot cost?」以及 https://docs.x.ai/x-subscription/usage-limits | 计入每周共享用量池，超额为预付/按需，不是按这次 API 标价逐次出 $0.82 这种账单 | A |
| grok 4.7 标价 $2 / $6，200k 以上加倍 | https://docs.x.ai/developers/pricing 、https://docs.x.ai/developers/grok-4-7 | 相符（另有缓存价 $0.50，长上下文 $4 / $12） | A |
| grok 4.3 标价 $1.25 / $2.50，上下文 1M，200k 以上加倍 | https://docs.x.ai/developers/models/grok-4.3 、定价页 | 相符 | A |
| grok-build-0.1 标价 $1 / $2 | https://docs.x.ai/developers/models/grok-build-0.1 、https://x.ai/news/grok-build-0-1 | 历史标价相符 | A |
| grok-build-0.1 已下线 | https://docs.x.ai/developers/release-notes 「November 19」「no longer served on the API」 | 原帖发布前两天已 EOL。Grok Bot 产品界面此刻是否仍显示该名称，本轮未打开应用确认（D） | A / D |
| Jev $0.042/百万输入、输出免费、32k 上下文、Noul/Choice、70–500 ms | https://docs.typesafe.ai/models 、https://help.typesafe.ai/articles/5187202169-how-much-does-jev-cost 、https://developers.cloudflare.com/ai/models/typesafe/jev/ 、https://www.infoq.com/news/2026/10/typesafe-ai-jev-released/ | 价格、题型、默认 32k/题相符；延迟来自对官方数字的报道（C，但与正文一致）；每请求默认其实是 64k | A / C |
| eesel 博文是本方案原文 | https://www.eesel.ai/blog/grok-bot ，标注最后编辑 2026-08-12 | 不是。该文介绍 Grok Bot 并推销 eesel 客服产品，无 11 条提示词，无 jev_seat / jev_done | A |

图 7 算术抽查（B，基于图中数字和公开 API 标价，不是真实账单）：

- 66,000 × $6 / 1,000,000 = $0.396，图上写作 $0.40
- 66,000 × $2 / 1,000,000 = $0.132，图上写作 $0.13
- $1.5769 × 100 = $157.69；$0.8179 × 100 = $81.79，与图上「每 100 次运行」一致，来源仍是作者自报 token 数

## 5. 仓库去重

只读连接器，未克隆。

| 项 | 值 |
| --- | --- |
| 仓库 | https://github.com/yysfei/financial_analysis |
| `latest-reports` HEAD | `84fbcf42def21d9a46e3fab01372a4b552e1c093` |
| `main` HEAD | `663ab8051cb08a36b566bc1a989a7b7def840bb1` |
| 另有分支 | `cursor/arbitrage-report-archive-2382`（未当作索引来源） |
| `search_code`（默认分支） | `savvy_luvvvv OR jev_done OR grok-harness OR jev_seat` 命中 0 |
| `latest-reports` 根 README 与 `reports/investment/README.md`、`reports/investment/2026/` 目录 | 无同题报告 |

相近主题（AI 交易台/Bot 架构）已存在，但对象、主张和证据都不同，本报告不复用其结论：

- [一人AI基金、策略工厂与预测市场提示词交易台](../waveking-ai-prompt-trading-desk/README.md)
- [BTC 5 分钟双模型（GPT + Grok）](../chenke-btc5m-dual-model-bot/README.md)
- [0xboan Solana meme 币筛查台](../oxboan-solana-rug-filter-desk/README.md)
- [跨策略风险与 Bot 架构评估](../../../arbitrage/2026/cross-strategy-risk-and-bot-architecture/README.md)

## 6. 未做事项

- 未创建 Grok Bot、群聊、定时任务或 `/workspace/grok-harness`
- 未申请或使用 TypeSafe 密钥，未调用 `api.typesafe.ai`
- 未在 Grok Bot 应用内确认当前可选模型列表或实时用量页
- 未完整翻完回复第二页，未干净地枚举全部 9 条引用
- 未播放 8 段 GIF 动画；4 张预览图 403 未看
- 未核实图 8 提交 `a41f9c2` 是否存在于某个公开仓库
- 未展开作者其他宣传帖里的 PDF / 策略库外链
