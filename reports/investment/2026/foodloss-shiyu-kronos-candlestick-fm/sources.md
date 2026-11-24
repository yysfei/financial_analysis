# 来源与核验记录：foodloss 指定帖与 shiyu-coder/Kronos

研究日：2026-11-24，北京时间（Asia/Shanghai）。X 公开读取通过命名空间 `x` 的公共工具完成，没有使用用户 X 账户发帖或登录。仓库只读克隆。不联系 LINE、不安装依赖、不下载模型权重、不输入密钥、不交易。本轮没有复跑模型。

## 主要来源

| ID | URL | 已取得/可支持 | 不支持/仍缺失 |
|---|---|---|---|
| X1 | https://x.com/foodloss_otoko/status/2124920413620711760 | 日文原文、配图、直接引用旧 EA 帖；主张 Kronos +2,653 star、用 45+ 交易所数据预测下一根 K 线 | 正文无 GitHub URL；不证明本周星标增量、FX 可交易系统或实盘收益 |
| X1img | 配图 `https://pbs.twimg.com/media/HX055eNbsAAdEvg.png`（本地副本 `post-image-github-finance-oct17-23.png`） | 表格写明仓库 `shiyu-coder/Kronos`，类别 Market model，本周 +2,653，累计 43,523；标题为 Oct 17-23 周报，署名 wincy.eth | 不是 2026-11-23 的实时星标；累计 43,523 已被当日 API 的约 48,133 超过 |
| X2 | https://x.com/foodloss_otoko/status/2116376578187780173 | 被 X1 引用；Article 标题《完全放置で年利12％のEAを作りました。》 | 与 Kronos 源码不是同一系统；12% 已在旧报告中审查，本案不重算为新业绩 |
| X3 | https://x.com/foodloss_otoko/status/2119455388945047967 | 2026-11-08 23:41:56（北京时间）同类“本周 Kronos”帖，写的是 +2,846 | 与 X1/配图的 +2,653 冲突，说明数字会被重复或改写使用 |
| X4 | https://x.com/foodloss_otoko/status/2114583090496749962 | 2026-10-26 13:01:10（北京时间）已出现几乎相同的 Kronos +2,653 文案 | 证明本帖不是首次披露 |
| X5 | https://x.com/_____ZVCH/status/2125100024518652036 | 本帖唯一公开引用，无新证据 | 不提供仓库或业绩 |
| G1 | https://github.com/shiyu-coder/Kronos | 官方仓库；本轮克隆 `master` @ `67b630e67f6a18c9e9be918d9b4337c960db1e9a`（2026-04-13 20:38:49 北京时间）；约 48,133 star，MIT，非 fork | 不含预训练语料、不含 Kronos-large 权重、不含示例 CSV `XSHG_5min_600977.csv` |
| G1b | https://github.com/shiyu-coder/Kronos/commit/67b630e67f6a18c9e9be918d9b4337c960db1e9a | 当前 HEAD，合并 PR #243 | — |
| G1c | https://github.com/shiyu-coder/Kronos/commit/79d6d403d8999de4aea8b388ca10905c8bf3de33 | 2026-04-11 修复微调归一化窗口的未来函数泄漏（PR #227） | 不能自动证明论文实验是否使用过泄漏代码 |
| HF | https://huggingface.co/NeoQuasar | README 指向的权重命名空间（mini/small/base 与对应 tokenizer） | 本轮未下载权重，未核对其校验和 |
| P1 | https://arxiv.org/abs/2508.02739 | 论文 HTML/摘要：45 所交易所、约 120 亿条 K 线；预训练至 2024-06，测试自 2024-07；相对 RankIC 提升自称 93%/87%；投资模拟与 Table 10 的 AER/IR | 未独立复跑；Kronos-large 最好数字对应未开源权重；论文“每笔 0.15%”与公开脚本 open 0.10%/close 0.15% 口径不完全相同 |
| Q1 | https://github.com/microsoft/qlib | 官方微调/回测所依赖的框架，文档与代码引用属实 | 不为本案回测数字背书 |
| FA | https://github.com/yysfei/financial_analysis/tree/latest-reports | 去重时 `latest-reports` 尖端 `8e1f157168f5eab71bc248d8c753c96ad5a3d02d`（2026-11-24 16:33:15 北京时间）；已有 foodloss EA 报告，无 Kronos 专篇 | 该提交不能代替本篇的源码核验 |
| FA-old | https://github.com/yysfei/financial_analysis/blob/latest-reports/reports/arbitrage/2026/foodloss-ai-trading-desk-ea-backtest/README.md | 旧 foodloss 提示词/EA 12% 案，去重对照 | 不覆盖本仓库 |

作者主页短链 `https://t.co/JUDQKM4Puc` 展开为 `https://lin.ee/yx9eCqY`。这是引流/利益冲突记录，不是业绩来源。本轮没有打开 LINE 或索取资料。

## 时间、线程与去重

- X1：`2026-11-23T17:38:00.000Z`，北京时间 2026-11-24 01:38:00。`conversation_id` 等于帖 ID，`reply_count=0`，没有补充代码的线程回复。
- X2：`2026-10-31T03:47:51.000Z`，北京时间 2026-10-31 11:47:51。
- 用 `from:foodloss_otoko Kronos` 检索到更早的 X3、X4，属于同一推广模板。
- 去重时的 `latest-reports` 树（185 个路径，未截断）只命中既有 `reports/arbitrage/2026/foodloss-ai-trading-desk-ea-backtest`，没有 Kronos 专篇。本地历史有 2026-11-20 的 foodloss EA 研究稿，同样不覆盖本仓库。

## 关键源码证据（均固定到提交 67b630e）

| 主题 | 固定链接 |
|---|---|
| 官方“演示而非生产系统”与费用提醒 | [README.md#L217-L306](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/README.md#L217-L306) |
| 模型是否开源（large 为否） | [README.md#L77-L82](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/README.md#L77-L82) |
| 预测反归一化（公开回测脚本未走这一层） | [model/kronos.py#L544-L558](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/model/kronos.py#L544-L558) |
| 自回归推理返回归一化空间 | [model/kronos.py#L389-L469](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/model/kronos.py#L389-L469) |
| 公开回测信号（归一化差值，非论文百分比） | [finetune/qlib_test.py#L275-L282](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_test.py#L275-L282) |
| Qlib 费用、开盘价、延迟成交、涨跌停 | [finetune/qlib_test.py#L120-L140](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_test.py#L120-L140) |
| 训练/验证/测试/回测时间与持仓参数 | [finetune/config.py#L12-L38](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/config.py#L12-L38)、[L110-L120](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/config.py#L110-L120) |
| 按日期掩码切分（重叠风险） | [finetune/qlib_data_preprocess.py#L102-L110](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_data_preprocess.py#L102-L110) |
| 泄漏修复后的归一化 | [finetune/dataset.py#L107-L117](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/dataset.py#L107-L117) |
| 社区回测不计费、预测价填真实价 | [examples/run_backtest_kronos.py#L123-L228](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py#L123-L228) |
| 非 Kronos 的“历史回测”占位预测 | [examples/yuce/historical_backtest.py#L71-L96](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/yuce/historical_backtest.py#L71-L96) |
| Web UI 自动 pip 安装 | [webui/start.sh](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/webui/start.sh)、[webui/run.py](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/webui/run.py) |

论文投资模拟与 Table 10 摘自 arXiv HTML 附录（约第 1133–1248 段）。预训练截止与测试起点见约第 1049 段。本轮没有声称已复现这些表格。

随仓库发布的 `figures/backtest_result_example.png` 仅作目视描述，未做像素标定后的精确读数。

## 本地下载记录

| 项 | 值 |
|---|---|
| 克隆目录 | `/workspace/research-downloads/shiyu-coder-Kronos` |
| 远程 | `https://github.com/shiyu-coder/Kronos.git` |
| 分支 | `master` |
| SHA | `67b630e67f6a18c9e9be918d9b4337c960db1e9a` |
| 跟踪文件数 | 92 |
| 克隆完成 | 2026-11-24 19:28:15（北京时间） |
| Zip | `/workspace/research-downloads/shiyu-coder-Kronos-67b630e-20261124.zip`（含 `.git`） |
| Zip SHA256 | `a93b00198961e38a4498fdf6aab228aa4e38e4a00f3e2ea3ce986f188bbdb1ca` |
| Zip 大小 | 19,280,465 字节，创建于 2026-11-24 19:28:43（北京时间） |
| 用户 Windows 副本 | `C:\Users\ThinkPad\Downloads\shiyu-coder-Kronos-67b630e-20261124.zip`，2026-11-24 北京时间已复制成功 |
| 元数据文件 | `/workspace/research-downloads/CLONE_METADATA.txt` |

克隆时未执行仓库内任何安装或启动脚本，也未下载权重、未复跑模型。

## 访问范围与未核验

- 未运行 `pip`、`start.sh`、`webui/run.py`、预测或回测，因此没有生成新的收益率。
- 未下载 Hugging Face 权重，未安装 Qlib 数据，未打开 LINE。
- 未独立复算 Table 10，未对 2025-06 之后做样本外检验，未核验 AAAI 2026 程序页。
