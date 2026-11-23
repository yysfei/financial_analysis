# 来源

本目录对应报告：[README.md](README.md)。时间线扫描覆盖北京时间 2026-11-23 12:09:08–16:17:04。仓库字段来自同日下午打开的公开页面。下列材料只用于研究核验，不构成交易指令。

## A. 本次打开的帖文与仓库

| 编号 | 材料 | 地址 | 用到的字段或内容 |
| --- | --- | --- | --- |
| A1 | `@0xcherry` 原帖 | https://x.com/0xcherry/status/2124774608670998543 | 北京时间 2026-11-23 15:58:37。称用刚发布的 GLM-5.4 跑了 AutoQuant bench，思考更长，执行前会先探索，请人自己跑完再点评。没有个人收益，也没有称这是已验证实盘 |
| A2 | 仓库 | https://github.com/TraderAlice/Auto-Quant | 公开。默认分支 `master`。`main` 上的 README 会 404。created 2026-04-22。pushed_at 2026-11-23T07:10:50Z（北京时间 15:10:50）。stargazers_count 396。forks_count 51 |
| A3 | 官方 README | 同仓库 `master` 分支 | 把 Karpathy autoresearch 模式用到 FreqTrade。宇宙 BTC/ETH/SOL/BNB/AVAX。周期 1h/4h/1d。成功标准是循环能跑出可解释的 results.tsv，不是找到可盈利策略。原句：Nothing in this repo is a recommendation to trade real capital。v0.1.0 把 Sharpe 18 的簇当作 oracle-gaming 丢掉，保留线停在 Sharpe 1.44，并称真实边缘更低。后续版本自述有 clean Sharpe、portfolio_robust_sharpe 等指标 |

## B. 由 A 做的换算

| 编号 | 换算 | 结果 |
| --- | --- | --- |
| B1 | 原帖北京时间 2026-11-23 15:58:37 减去 8 小时 | UTC 2026-11-23 07:58:37 |
| B2 | pushed_at 2026-11-23T07:10:50Z 加 8 小时 | 北京时间 2026-11-23 15:10:50 |

没有把 Sharpe 18 或 1.44 换成收益、回撤或本金。后续指标的数值没有进入本表。

## C. 作者叙述

| 编号 | 材料 | 说明 |
| --- | --- | --- |
| C1 | GLM-5.4、思考更长、执行前先探索 | 只存在于 A1。本轮没有运行日志 |
| C2 | README 中的 Sharpe 筛选过程 | 原文等级见 A3。分数本身是项目自述，本轮未复跑，不能写成样本外或实盘 |

## D. 未访问或未完整查看

| 编号 | 内容 | 处理 |
| --- | --- | --- |
| D1 | 克隆仓库并复跑 bench，打开 results.tsv | 未做 |
| D2 | 后续版本 clean Sharpe、portfolio_robust_sharpe 的具体数值 | 本次记录只确认名称存在，不补造数字 |
| D3 | 许可证全文、依赖锁定文件、默认配置里的手续费和滑点 | 不在本次可引用摘录中 |
| D4 | 作者或仓库维护者的实盘账户 | 原帖没有给出，本轮不寻找替代账单 |
| D5 | `main` 分支除 README 404 之外的其他文件 | 只记录 README 会 404，不把整个分支描述成空仓库 |

## 相邻但不合并

[QuantJourney 开源回测库](../irongiant-quantjourney-bt-library/README.md) 也是公开的研究工具，官方同样声明不是实盘建议。仓库、绩效表和宣传帖都不同，数字不混用。
