# Kronos K 线基础模型：获利可行性与源码核验

- 归档日期：2026-11-24 Asia/Shanghai
- 市场与标的：开源金融 K 线基础模型 Kronos（仓库 [shiyu-coder/Kronos](https://github.com/shiyu-coder/Kronos)）。论文中的投资模拟是 A 股、沪深 300/800 的 top-K 组合，不是外汇实盘账户
- 策略类型：预测与研究工具，外加论文中的模拟回测。不是已验证可直接执行的交易系统，也不是无风险套利
- 案例时间：[@foodloss_otoko](https://x.com/foodloss_otoko/status/2124920413620711760) 发布于 2026-11-23 17:38:00 UTC（2026-11-24 01:38:00 Asia/Shanghai）
- 研究状态：源码已下载。`master` 提交 `67b630e67f6a18c9e9be918d9b4337c960db1e9a`，克隆完成于 2026-11-24 19:28:15（北京时间）。ZIP 已于 2026-11-24 北京时间成功复制到用户 Windows 电脑 `C:\Users\ThinkPad\Downloads\shiyu-coder-Kronos-67b630e-20261124.zip`。本轮没有下载权重，没有安装依赖，没有复跑模型，没有下单
- 证据等级说明：A 来源实际显示内容、官方页面与当前源码，B 条件观察（例如对随仓库发布的回测图作目视描述），C 作者自述（论文、README、推文），D 未独立验证，E 提出的验证设计。论文表中的年化超额收益是 C，不因数字写在 arXiv 上就升级为已复现实盘
- 是否复用既有报告：否。原帖引用了同一作者更早的 EA 长文，见 [foodloss / AI 交易台提示词与“完全放置年利 12%”EA](../../../arbitrage/2026/foodloss-ai-trading-desk-ea-backtest/README.md)。那一套规则未公开，与 Kronos 源码不是同一系统，成绩不合并
- 来源：[sources.md](sources.md)

本文件是人工撰写的研究笔记。它不运行交易，不连接钱包，不构成投资建议，也不会在以后自动改写自己。

## 结论

**这是一个真实、可克隆的清华大学相关开源 K 线基础模型，不是现成的自动盈利交易系统，更不应按原帖口吻当成“本周海外 AI×FX 工具、跟着就能赚钱”。公开代码可以做预测和受监督的研究回测，但不能自动下单；论文里的年化超额收益未经本轮独立复跑，且效果最好的 Kronos-large 权重并未开源。**

最关键的可执行性问题：

1. 原帖把 Kronos 写成“让 AI 预测下一根 K 线的 FX 工具”，并配上 wincy.eth 的《GitHub Finance + AI Weekly Pulse — Oct 17-23》表格。表中第一行就是 `shiyu-coder/Kronos`，本周 +2,653、累计 43,523 star。该数字来自约一个月前的周报截图，不是 11 月 23 日当天的星标增量。仓库本身是真的：2026-11-24 查询时约 48,133 star，默认分支 `master`，最新推送仍停在 2026-04-13 20:38:49（北京时间）。
2. 仓库官方定位是金融 K 线（OHLCV）基础模型，权重在 Hugging Face `NeoQuasar/*`；投资模拟走的是 Qlib、A 股、沪深 300/800 的 top-K 组合，不是外汇 EA，仓库里也没有券商/交易所下单接口。
3. 论文（[arXiv:2508.02739](https://arxiv.org/abs/2508.02739)）自述在预训练截止 2024-06、测试自 2024-07 起的投资模拟中，Kronos-large 平均年化超额收益（AER）0.2084、信息比（IR）1.6491，并称每笔交易计 0.15% 费用。这些是作者实验数字（C），本轮没有复跑。而且 README 写明 Kronos-large（499.2M）未开源，公开可用的是 mini/small/base。
4. 随仓库发布的官方回测示例图（约 2024-07 至 2025-05）目视上策略累计收益高于沪深 300，但同期大盘本身有一次陡峭反弹，绝对收益里有明显的市场贝塔；不能把这张图当成当前可复制的实盘账单。
5. `examples/` 里若干社区风格脚本质量不稳定：有的硬编码 Windows 路径，有的示例数据根本没进仓库，`examples/yuce/historical_backtest.py` 甚至用移动平均加随机波动冒充预测，却仍自称“Kronos 模型历史回测系统”。这些脚本的打印收益不能当成模型业绩。
6. 原帖引用了同一作者更早的《完全放置で年利12％のEAを作りました。》，那是已归档的另一套未公开规则 EA 宣传，与 Kronos 源码不是同一系统。作者主页链到 LINE 邀请，存在引流/利益冲突，需要单列。

**不应连接钱包、接入实盘或自动下单。** 若继续研究，只能在隔离环境里做只读复现和纸面/模拟，并自行准备数据和费用假设。

## 分析前去重

已对照历史 foodloss 案例，并只读检查 [yysfei/financial_analysis](https://github.com/yysfei/financial_analysis) 的 `latest-reports` 分支（提交 `8e1f157168f5eab71bc248d8c753c96ad5a3d02d`，提交时间 2026-11-24 16:33:15 北京时间；`truncated=false`，树中 185 个路径）。

- 已有报告：[foodloss / AI 交易台提示词与“完全放置年利 12%”EA](../../../arbitrage/2026/foodloss-ai-trading-desk-ea-backtest/README.md)，来源是 2026-11-19 的提示词帖 [2123446186883547391](https://x.com/foodloss_otoko/status/2123446186883547391) 及其引用的 EA 长文 [2116376578187780173](https://x.com/foodloss_otoko/status/2116376578187780173)。结论是提示词不是现成策略，标题 12% 与截图算术在“连续 5 年、无追加资金”假设下冲突。那份报告覆盖的不是 Kronos。
- 本案原帖再次引用同一篇 EA 长文，但正文和配图的新对象是 Kronos。去重时的 `latest-reports` 在 investment、arbitrage、research 目录下都没有 `kronos`、`shiyu-coder` 或本帖 ID 的既有详细报告。
- 同作者还在 2026-10-26、2026-11-08 发过高度相似的“本周 Kronos 涨星”帖，11-08 帖写的是 +2,846，与本帖/配图的 +2,653 不一致，说明这是重复推广而不是新的已验证系统。

因此本案是新指定链接、新仓库、新证据，不与旧 EA 报告合并成绩；但必须写明它引用了旧 EA 长文，且旧报告结论不变。

## 原帖主张、配图与仓库身份

| 来源 | 时间（API 原字段 → 北京时间） | 实际内容及限度 |
|---|---|---|
| 指定帖 2124920413620711760 | 2026-11-23T17:38:00Z → 11-24 01:38:00 | 日语称“本周海外正在增长的 AI×FX 工具”，第一条是 Kronos（+2,653 star）：让 AI 预测下一根 K 线，用大量历史图表训练，用 45 个以上交易所数据，特点是直接处理 K 线。短链只指向配图和引用的旧 EA 帖，正文没有 GitHub URL。回复 0；研究时约 218 赞、15 转、391 书签。 |
| 配图 `3_2124918258713473024` | 同上 | 表格标题 *GitHub Finance + AI Weekly Pulse — Oct 17-23*，页签还有 Oct 10-16、Oct 03-09，署名 wincy.eth。第 1 行仓库名为 **`shiyu-coder/Kronos`**，类别 Market model，本周 +2,653，累计 43,523。这是定位仓库的直接证据。 |
| 引用帖 2116376578187780173 | 2026-10-31T03:47:51Z → 10-31 11:47:51 | X Article《完全放置で年利12％のEAを作りました。》。与 Kronos 仓库不是同一套代码或规则；已在旧报告中审查。 |
| 唯一引用本帖的公开引用 | 2026-11-24T05:31:42Z → 11-24 13:31:42 | [@_____ZVCH](https://x.com/_____ZVCH/status/2125100024518652036) 只问“投资顾问是否也会被 AI 替代”，没有补充仓库或业绩证据。 |
| 作者 @foodloss_otoko | 账号创建 2025-06-18 | 简介“専業トレーダー、EA×裁量で生活してます。”；主页展开为 LINE 邀请 `https://lin.ee/yx9eCqY`。这是利益冲突，不是业绩证明。 |

GitHub 官方元数据（2026-11-24 查询，A）：完整名 `shiyu-coder/Kronos`，描述 “Kronos: A Foundation Model for the Language of Financial Markets”，**不是 fork**，默认分支 `master`，MIT 许可，语言 Python，约 48,133 star、7,974 fork、299 个未关闭 issue。创建于 2025-07-01，`pushed_at` 2026-04-13T12:38:49Z（北京时间 20:38:49）。本轮克隆到的 HEAD 与 API 一致：[`67b630e`](https://github.com/shiyu-coder/Kronos/commit/67b630e67f6a18c9e9be918d9b4337c960db1e9a)（合并 PR #243）。

推文与仓库相符的部分：README 也写“trained on data from over 45 global exchanges”，并强调直接对 K 线建模。不相符或被夸大的部分：把它称为可直接使用的 FX 交易工具、把一个月前的周星标增量说成“本周”、以及通过引用 12% EA 长文暗示“放着就能赚钱”。

## 真实代码在做什么

仓库是研究型模型代码，不是交易柜台。主干很清楚：

- `model/kronos.py`、`model/module.py`：分词器把连续 OHLCV/成交额量化成分层离散 token，再用自回归 Transformer 生成后续 token，解码回价格量。推理入口是 `KronosPredictor.predict` / `predict_batch`，以及底层的 `auto_regressive_inference`。
- 预训练权重不在 git 里（`.gitignore` 排除了 `.pth/.pt/.ckpt/.bin` 等），要通过 Hugging Face 拉取。README 模型表：

  | 模型 | 参数量 | 是否开源 |
  |---|---|---|
  | Kronos-mini | 4.1M | 是，`NeoQuasar/Kronos-mini` |
  | Kronos-small | 24.7M | 是，`NeoQuasar/Kronos-small` |
  | Kronos-base | 102.3M | 是，`NeoQuasar/Kronos-base` |
  | Kronos-large | 499.2M | **否** |

- `finetune/`：官方给出的 A 股微调 + Qlib 回测示例。README 自己写明这是演示，不是生产级量化系统，并提醒高保真回测应仔细建模交易成本、滑点和市场冲击。
- `webui/`：本地 Flask 预测界面，支持上传 K 线、出预测图，没有下单。
- `examples/`：官方预测示例与一批社区风格的数据抓取、GUI、回测脚本，质量参差（见下）。
- `tests/`：回归测试夹具，验证推理数值稳定性，不验证盈利。

官方“开始使用”脚本 [`examples/prediction_example.py`](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/prediction_example.py) 读取 `./data/XSHG_5min_600977.csv`。该 CSV **不在当前 92 个跟踪文件里**，仓库也忽略了大型数据文件。按 README 原文无法开箱即跑，需要用户自备数据。`examples/prediction_batch_example.py` 还硬编码了作者机器路径 `/home/csc/huggingface/...`。

## 数据、信号与交易执行

### 数据来源

- 论文（C）：预训练语料自称超过 120 亿条 K 线、45 家全球交易所；附录表包含 Binance、北交所、多家股票交易所等。预训练数据截止 **2024 年 6 月**，所有任务测试期从 **2024 年 7 月**开始，以保证时间隔离。
- 公开仓库 **不包含** 这份预训练语料，也没有一键下载脚本把 120 亿条数据拉下来。
- 官方微调示例假定本机已有 Qlib 日频 A 股数据，默认路径 `~/.qlib/qlib_data/cn_data`，股票池 `csi300`，总体区间 2011-01-01 至 2025-06-05。见 [`finetune/config.py`](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/config.py#L12-L38)。
- `examples/get_date_new.py`、`get_akshare_date_2024-2025_x.py` 会向外部行情接口发 HTTP 请求，并在缺依赖时用 `subprocess` 执行 `pip install`。本轮没有运行这些脚本。

### 官方回测信号（论文 vs 公开代码并不完全一致）

论文公式 (13) 把信号写成未来 H=10 日预测收盘价均值相对**当前收盘价**的百分比收益：

\[
R_{t\to t+H}=\frac{\bigl(\frac{1}{H}\sum_{i=1}^{H}\hat p_{t+i}\bigr)-p_t}{p_t}
\]

回望窗口 90 日。策略是每日对股票池按该信号排序，等权做多 top-K，每日最多调入/调出 n 只，最短持有 5 日。沪深 300：k=50、n=5；沪深 800：k=200、n=10。

公开脚本 [`finetune/qlib_test.py`](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_test.py#L275-L282) 计算的是归一化空间里的差值，而不是价格百分比：

```python
last_day_close = x[:, -1, 3].numpy()
signals = {
    'last': preds[:, -1, 3] - last_day_close,
    'mean': np.mean(preds[:, :, 3], axis=1) - last_day_close,
    'max': np.max(preds[:, :, 3], axis=1) - last_day_close,
    'min': np.min(preds[:, :, 3], axis=1) - last_day_close,
}
```

这里的 `x` 已按样本做实例归一化（[`qlib_test.py` 第 84–87 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_test.py#L84-L87)），`auto_regressive_inference` 的返回值也仍在同一归一化空间（反归一化发生在 `KronosPredictor.predict`，回测脚本没有走那一层）。因此公开演示信号更接近“以历史波动率为单位的预期变动”，与论文的百分比收益不是同一公式。排序结果可能相关，但不能把脚本输出直接当成 Table 10 的复现。

回测执行用 Qlib 的 `TopkDropoutStrategy` + `SimulatorExecutor`：`'time_per_step': 'day'`，`'delay_execution': True`，`'deal_price': 'open'`，涨跌停阈值 0.095。见 [第 120–140 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/finetune/qlib_test.py#L120-L140)。含义是：信号在当日产生后，延迟到后续开盘价成交，并考虑涨跌停，这比“用当日收盘立即成交”更接近可交易假设。账户初始资金在脚本里是 1 亿元人民币量级的模拟账户，不是个人实盘。

**整个官方管道都没有向交易所或券商提交订单的代码。** Web UI 同样只做预测展示。

### 社区回测脚本不能当作业绩

[`examples/run_backtest_kronos.py`](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py) 硬编码 `D:\lianghuajiaoyi\Kronos\...`。关键缺陷包括：

- 没有预测出未来日期时，会退回使用全部预测数据（[第 123–126 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py#L123-L126)）。
- 缺少真实价格时，用预测价充当成交价（[第 175 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py#L175)）。
- 交易循环不扣除佣金、印花税或滑点（[第 158–228 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py#L158-L228)）。
- 列名映射甚至把“收盘价”改名为 `predicted_close`，存在把真实收盘误当作预测的风险（[第 92–97 行](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/run_backtest_kronos.py#L92-L97)）。

[`examples/yuce/historical_backtest.py`](https://github.com/shiyu-coder/Kronos/blob/67b630e67f6a18c9e9be918d9b4337c960db1e9a/examples/yuce/historical_backtest.py#L71-L96) 注释写明“这里应该替换为您的实际模型预测”，实际却用移动平均加随机波动；主函数仍打印“Kronos模型历史回测系统”。同目录 JSON 报告是 2025-09/10 的宏观/行业套话模板，不是可核对的模型账单。

## 手续费、滑点、资金与部署成本

能从源码和论文直接读到的费用假设（C/A，不等于当前某券商报价）：

- 论文：为使评估更接近现实，对每笔交易采用“偏保守”的 **0.15%** 交易成本。
- 公开 Qlib 示例：`open_cost=0.001`（0.10%）、`close_cost=0.0015`（0.15%）、`min_cost=5`，成交价为开盘价，另有 9.5% 涨跌停限制。这与论文口头上的“每笔 0.15%”并不完全同一口径。
- 官方示例**没有单独建模滑点或市场冲击**；README 也承认高保真回测应当补上这些项。
- 社区脚本默认初始资金 10 万元人民币，且不计费。

部署与运行成本（没有编造电费或云账单，只列门槛）：

- 最小推理：Python 3.10+、PyTorch≥2.0、从 Hugging Face 下载 small/base 权重；CPU 可跑，GPU/MPS 更实际。Kronos-small 约 24.7M 参数，个人研究机器通常可承担，但仍需网络下载权重。本轮没有下载这些权重。
- 官方微调：README 要求 `torchrun` 多 GPU，另装 `pyqlib` 并自备 Qlib 数据。论文附录写实验环境是 3 个 Pod、合计 24 张 RTX 4090D，这是作者训练/评测规模，不是个人跟跑的必需要求，但说明完整复现论文并不便宜。
- Kronos-large 未开源，公开仓库无法复现 Table 10 中最好的那一行。
- 没有券商接口，所以不存在“填入 API 密钥就能实盘”的官方路径；若有人自行对接，那是额外的工程和合规风险，不属于本仓库提供的功能。

## 回测可信度、幸存者偏差与未来函数

**可以正面记下的设计：**

- 论文明确预训练截止 2024-06、测试从 2024-07 起，存在时间隔离声明。
- 官方 Qlib 示例使用次日开盘、延迟成交、涨跌停和成本，并同时输出“含成本超额收益”。
- 2026-04-11 的提交 [`79d6d40`](https://github.com/shiyu-coder/Kronos/commit/79d6d403d8999de4aea8b388ca10905c8bf3de33)（PR #227）修复了微调数据集的归一化泄漏：此前对整个窗口（含预测期）计算均值和标准差，等于把未来价格尺度泄漏进输入；修复后只在 lookback 段上统计。这是真实的前视风险，而且修复发生在论文（2025-08）和微调脚本发布（README 写 2025-08-17）很久之后。本轮不能断言论文数字用了有泄漏的代码，但用 2026-04-11 之前的公开微调代码复现，会踩到这个问题。

**削弱“已验证可获利”的事实：**

1. Table 10 与示例图都是作者材料，本轮未复跑，也没有逐笔成交账本。数字一律标 C/B，不升级。
2. 论文 Table 10（作者自述，测试自 2024-07 起）仅供对照，不是本轮结果：

   | 模型 | 沪深300 AER | 沪深300 IR | 沪深800 AER | 沪深800 IR | 平均 AER | 平均 IR | 公开权重 |
   |---|---:|---:|---:|---:|---:|---:|---|
   | Kronos-small | 0.1805 | 1.2394 | 0.1772 | 1.6050 | 0.1789 | 1.4222 | 有 |
   | Kronos-base | 0.1911 | 1.3782 | 0.1867 | 1.6652 | 0.1889 | 1.5217 | 有 |
   | Kronos-large | 0.2193 | 1.4177 | 0.1974 | 1.8805 | 0.2084 | 1.6491 | **无** |
   | 表中次优公开基线 Moment-large 平均 AER |  |  |  |  | 0.1681 | 1.3677 | 外部模型 |

   同表里也有明显亏损的基线（例如 iTransformer 平均 AER −0.0864）。这只能说明“在作者设定的模拟里 Kronos 排名靠前”，不能推出当前跟跑会赚到相近数字。

3. 仓库图 `figures/backtest_result_example.png` 横轴约 2024-07 至 2025-05。目视：含成本累计收益在期末大约落在 0.20–0.28（视 last/mean/max/min 信号），沪深 300 大约 0.13–0.14；含成本超额大约 0.06–0.14。2024 年 9 月末到 10 月，策略曲线与基准一起陡升，说明很大一块绝对收益来自市场反弹，不是纯粹的选股 alpha。这是对已发布图片的观察（B），不是复算后的精确报表。
4. 公开 `config.py` 的划分存在重叠：训练集到 2022-12-31，验证从 2022-09-01 起；测试从 2024-04-01 起，验证到 2024-06-30。注释说是为 lookback 预留，但 `qlib_data_preprocess.py` 是按原始 K 线日期做简单掩码，再在整段上切窗，验证/测试窗的预测目标仍可能落进更早集合。回测区间 2024-07-01 至 2025-06-05 本身在验证结束之后，相对干净，但不能消除模型选择阶段的重叠风险。
5. 论文投稿/挂网（2025-08）距测试期末（示例到 2025-06）很近；对 2025-06 之后、直至本轮的 2026-11，没有作者提供的、可核独立样本外结果。样本外是否衰减，本轮不知道（D）。
6. 论文写“不对 Qlib 数据做额外过滤”，这有利于透明，但也意味着没有剔除不可交易、停牌或流动性过差的品种；真实可成交性仍要另核。
7. 推理是随机采样（温度、top-p、`sample_count`）。同一输入多次运行不会得到完全相同的预测，因此不存在“一条确定性、可无条件复制的交易脚本”。官方回测默认 `inference_T=0.6`、`sample_count=5`。
8. 原帖和星标榜单有明显的关注度/幸存者展示偏差：列出的是当周涨星仓库，不是经过费用后的已验证收益排行。

## 依赖与安全风险

本轮只做静态审查，没有执行 `pip install`、`start.sh`、`webui/run.py` 或任何预测/回测，也没有下载模型权重。

- 主依赖见 `requirements.txt`：`torch>=2.0.0`、`huggingface_hub==0.33.1`、`pandas`、`matplotlib` 等。微调另需 `pyqlib`。运行预测会访问 Hugging Face 下载权重。
- **未发现**钱包助记词、私钥、交易所 API 密钥或自动划转资金的代码。`finetune/config.py` 里有 Comet.ml 的 `"api_key": "YOUR_COMET_API_KEY"` 占位符，注释也建议改用环境变量；不要把真实密钥写进这个文件。
- 风险点：`webui/start.sh`、`webui/run.py` 以及部分 `examples/` 脚本会在缺依赖时自动 `pip install`。对未知仓库，这属于应避免直接执行的安装路径。`pickle.load` 出现在数据集和预测缓存中，只应加载自己生成的本地文件。数据抓取脚本会访问外部 HTTP 接口。
- 许可为 MIT，可研究、修改，但许可不是投资建议，也不构成盈利保证。
- 原帖作者的 LINE 引流和旧 EA 推广，与本仓库维护者（论文作者 Yu Shi 等，单位信息为清华大学交叉信息研究院/自动化系）不是同一宣传主体。不要因为推文引用了仓库，就把作者的 12% EA 声明算到 Kronos 头上。

## 当前可复制性，以及 Bot 能做什么

| 目标 | 难度 | 本轮判断 |
|---|---|---|
| 克隆源码、阅读论文、静态复核 | 低 | 已完成。ZIP 已于 2026-11-24 北京时间复制到 `C:\Users\ThinkPad\Downloads\shiyu-coder-Kronos-67b630e-20261124.zip`。 |
| 在自备 K 线上跑官方 `KronosPredictor` 得到预测图 | 中 | 需要 Python/PyTorch、下载权重、自备 CSV；示例数据不在仓库里。本轮没有做这一步。适合有编程能力的研究用途。 |
| 按官方 `finetune/` 在 Qlib 上微调并回测 | 高 | 需要 Qlib 数据、GPU、改路径、理解训练/验证重叠和信号公式差异；结果仍是模拟。本轮未跑。 |
| 复现论文 Table 10 的 Kronos-large 行 | 目前不可行 | 权重未开源。 |
| 得到独立的、确定性的实盘交易脚本 | 仓库未提供 | 无经纪商执行层；推理本身还带随机采样。 |
| 让通用 Grok Bot 无人值守跟单或下单 | 不适合 | Bot 可以协助读代码、做研究复核、在隔离环境讨论纸面实验设计；不应连接钱包、不应自动下单、也不应代为运行来源不明的安装脚本。秒级/盘中自动交易不是这个模型或这个 Bot 的设计目标。 |

若只想研究这个模型有没有预测力，合理路径是：用公开的 small/base 权重、严格的时间切割、含费用和延迟成交的纸面回测，并自己记录未成交与失败单。这仍然不是批准实盘。

## 停止条件

出现以下任一情况，应停止向实盘升级（可继续学习或纸面研究）：没有独立复现、无法解释与论文公式的差异、未来函数未排除、费用和冲击后优势消失、只能靠未开源的 large 模型才能看到表中最好数字、必须绕过平台条款或提交高权限密钥、把原帖或社区脚本的打印收益当成实盘。

不能把“本轮无法证明可稳定获利”偷换成“已证明永远无效”。这是一个有论文和开源代码的研究项目，只是远远不够成为可自动执行的盈利系统。

## 本轮未做与未解决问题

未下载或运行模型权重，未安装依赖，未跑 Qlib 回测，未访问 LINE，未联系作者，未对 2025-06 之后的市场做样本外检验，未验证 AAAI 2026 录用的会议程序页（README 有 “accpeted” 拼写错误，录用声明暂记为作者自述）。也没有把示例回测图做像素级数值提取后当成精确报表。

仍待解决：论文 Table 10 使用的精确起止日、是否微调、是否与公开 `qlib_test.py` 同一信号公式；泄漏修复是否影响历史论文数字；2025-06 之后的真实衰减；A 股之外（包括原帖所暗示的 FX）是否存在任何经费用调整的可复核结果。

## 本地下载与复制状态

源码已下载。ZIP 已于 2026-11-24 北京时间成功复制到用户 Windows 电脑。本轮没有复跑模型。

| 项 | 值 |
|---|---|
| 仓库 | https://github.com/shiyu-coder/Kronos |
| 分支 | `master` |
| 提交 | [`67b630e67f6a18c9e9be918d9b4337c960db1e9a`](https://github.com/shiyu-coder/Kronos/commit/67b630e67f6a18c9e9be918d9b4337c960db1e9a) |
| 克隆完成 | 2026-11-24 19:28:15（北京时间，Asia/Shanghai） |
| 研究机目录 | `/workspace/research-downloads/shiyu-coder-Kronos` |
| 研究机 Zip（含 `.git`，可校验 SHA） | `/workspace/research-downloads/shiyu-coder-Kronos-67b630e-20261124.zip` |
| Zip 大小 / SHA256 | 19,280,465 字节；`a93b00198961e38a4498fdf6aab228aa4e38e4a00f3e2ea3ce986f188bbdb1ca` |
| 用户 Windows 副本 | `C:\Users\ThinkPad\Downloads\shiyu-coder-Kronos-67b630e-20261124.zip`，2026-11-24 北京时间已复制成功 |

## 复核记录

2026-11-24 北京时间：用公共 X 工具读取指定帖、引用、配图与引用该帖的讨论；用 GitHub API 确认仓库身份与提交；对照当时的 `latest-reports`（`8e1f157168f5eab71bc248d8c753c96ad5a3d02d`）与既有 foodloss EA 报告去重；静态审阅源码、README、论文 HTML 文本和示例回测图，并打包 zip。没有安装依赖，没有下载权重，没有运行预测或回测，没有下单。ZIP 已复制到 `C:\Users\ThinkPad\Downloads\shiyu-coder-Kronos-67b630e-20261124.zip`。
