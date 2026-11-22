# 来源与核验记录

核验时间：2026-11-23 01:10 至约 01:20（北京时间，UTC+8）。只做公开只读核验，未下单、未连接钱包、未联系作者，也未按帖文交易或执行任何代码。原帖没有配图或视频。FOMC 新闻发布会另有官方录像，本核验没有观看视频，只使用官方 PDF 实录和官方讲话网页。

## 原帖与账户

| 项目 | 记录 |
| --- | --- |
| 原帖 | https://x.com/leelee19950701/status/2124321065342210339 |
| 帖 ID / 对话 ID | 2124321065342210339 |
| 作者 | @leelee19950701 / Clannad17，用户 ID 1665730586424795136 |
| 发布时间 | 2026-11-22T01:56:24.000Z = 2026-11-22 09:56（北京时间，UTC+8） |
| 类型 | 加长帖（`note_tweet`），不是 X Article；无媒体、无引用、无正文外链、无投票 |
| 账户创建 | 2023-06-05T14:41:52.000Z = 2023-06-05 22:41（北京时间，UTC+8） |
| 核验时公开指标 | 约 999 赞、116 转帖、56 回复、14 引用、642 书签、约 297,177 次展示；跟随者约 4,722，帖文约 11,123 |
| 认证 | 蓝标 |
| 资料页 | 所在地 Austin, TX；YouTube https://youtube.com/@ethereum2017?si=xgr2YUl5idpHyVua ；VPN 注册页 https://www.vmssr.net/#/register?code=6CiRo4Qz |
| 读取方式 | 公开读取原帖，并核对话和引用 |

完整加长正文见同目录 [README.md](README.md)。展示摘要在「他们是真的打算继续加息。」处截断。

## 引用与回复（仅作传播记录，不是主要证据）

- 公开读取到的引用里，日文圈转发较集中。例如 https://x.com/ToyamaKingyo/status/2124539910690611568 称之为「ありがちな陰謀論」（常见阴谋论）；https://x.com/ulk_sasakero/status/2124539118961271283 翻译了「泡沫必须刺破后再降息收割」一段。返回结果里还夹杂了对另一条日文转帖的转发，不能把所有返回行都当成直接引用本帖。
- 原串回复里，有人区分财政部与美联储，例如 https://x.com/YouXiainvest/status/2124528384348975490 、https://x.com/XingPony/status/2124526335615983749。这些是评论，不是官方来源。
- 按原帖对话检索，未见作者补充原始演讲或声明链接。

## 美国债务与利息（官方）

| 来源 | URL | 核验方式与要点 |
| --- | --- | --- |
| Treasury Fiscal Data：Debt to the Penny 数据集页 | https://fiscaldata.treasury.gov/datasets/debt-to-the-penny/ | 本轮打开页面。数据集区间至 2026-11-19，上次更新 2026-11-20，下一次预期 2026-11-23 |
| Debt to the Penny API | https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v2/accounting/od/debt_to_penny?sort=-record_date&page[size]=3 | 打开页面得到官方 JSON。2026-11-19：总额 40,709,780,700,317.02 美元；公众持有 32,901,459,975,089.26 美元；政府内部持有 7,808,320,725,227.76 美元。直接请求该 API 的本地解析失败，以页面取得的官方 JSON 为准 |
| 第三方转载（只作交叉，不以之为权威） | https://fedgazette.com/debt-to-the-penny/ 、https://everydebtclock.com/how-much-is-the-national-debt/ | 数字与官方 API 一致，用于确认不是页面抓取错误 |
| Monthly Treasury Statement Table 9 API | https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_9?filter=record_date:eq:2026-09-30&page[size]=100 | 打开页面得到官方 JSON。`classification_desc=Net Interest`，`line_code_nbr=320`：2026 财年至今（即全年）净利息 1,051,753,969,311.11 美元；上一财年同期 970,358,886,994.32 美元；9 月当月 34,787,531,902.86 美元（9 月会因信贷融资账户年终利息收入而偏低，单月不宜外推）。总支出（line 340 Total）7,395,799,983,313.23 美元。由此计算净利息约占支出 14.2% |
| 最终月报 PDF | https://fiscaldata.treasury.gov/static-data/published-reports/mts/MonthlyTreasuryStatement_202609.pdf | 检索与 HTTP 头确认文件存在（约 2.3 MB，Last-Modified 2026-10-17）。净利息主证以 Table 9 API 为准 |
| 2026 年 10 月净利息（下一财年首月，仅作背景） | 第三方整理如 https://www.tftc.io/federal-interest-expense/net-interest | 称 10 月约 1,030.76 亿美元。本报告不以该第三方为 2026 财年主证 |

## 美联储官方文本

| 来源 | URL | 要点 |
| --- | --- | --- |
| 2026-09-16 FOMC 声明 | https://www.federalreserve.gov/newsevents/pressreleases/monetary20260916a.htm | 本轮打开页面。12 比 0，加息 25 个基点至 3.75%–4.00% |
| 2026-09-16 实施说明 | https://www.federalreserve.gov/newsevents/pressreleases/monetary20260916a1.htm | 检索确认存在，未作为主引 |
| 2026-10-28 FOMC 声明 | https://www.federalreserve.gov/newsevents/pressreleases/monetary20261028a.htm | 本轮打开页面。10 比 2，维持 3.75%–4.00%。反对票：Cook、Hammack，主张当场加 25 个基点。声明称经济活动强劲扩张，通胀仍然偏高 |
| 2026-10-28 实施说明 | https://www.federalreserve.gov/newsevents/pressreleases/monetary20261028a1.htm | 准备金利率维持 3.90%，自 2026-10-29 生效；隔夜逆回购 3.75%，正回购 4.0% |
| 2026-10-27 至 10-28 会议纪要 | https://www.federalreserve.gov/monetarypolicy/fomcminutes20261028.htm | 本轮打开页面。2026-11-18 14:00 ET 公布。几乎所有与会者认为，在其基线下，进一步上调目标区间可能合适；也讨论了 AI 投资回报若令人失望时的资产重估风险，同时提到银行和家庭资产负债表仍是缓冲 |
| 2026-10-28 主席新闻发布会实录 PDF | https://www.federalreserve.gov/mediacenter/files/FOMCpresconf20261028.pdf | 已打开官方 PDF 并转文本核验。主席为 Kevin Warsh。关键原话见 README。全文无 bubble / harvest / valuation；crisis 仅出现在 2008 年语境。没有观看 https://www.youtube.com/watch?v=hs8YWtNQQ40 |
| 实录网页转写（交叉） | https://www.whenthefedspeaks.com/doc/press_conference_20261028 | 与官方 PDF 一致，不作独立权威 |
| 2026-11-16 沃什在旧金山生产力与就业工作会议的开幕讲话 | https://www.federalreserve.gov/newsevents/speech/warsh20261116a.htm | 本轮打开全文。明确写 illustrative scenarios, not forecasts。较差情景包括：超级智能令人失望后，预期回报下降、股市估值下跌，进而经济放缓、失业率更明显上升。这是原帖「最新表态」最接近的公开文本，但被改写成了既定方针 |
| Axios 对 11-16 讲话的概括 | https://www.axios.com/2026/11/16/fed-warsh-ai-boom-stocks | 检索到标题将之概括为「若 AI 繁荣令人失望，存在股市受挫风险」。只说明媒体已发生压缩，证据仍以官方讲话为准 |

未把较早、且与官方路径冲突的转写当作证据。例如有页面将 2026 年 10 月的主席写成鲍威尔、把利率写成 4.25%–4.50%，与联邦储备官网不符，已弃用。

## 市场定价（非官方承诺）

| 来源 | URL | 用法 |
| --- | --- | --- |
| CME FedWatch 工具页 | https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool | 确认工具存在；本核验没有抓到带具体概率的官方即时页面 |
| 第三方 FedWatch 计算 | https://altinla.com/en/fed-faiz-izleme | 称截至约 2026-11-20 21:59 UTC，12 月 9 日会议加息概率约 93%，目标区间 4.00%–4.25%；当前目标 3.75%–4.00% |
| Quartz 转述路透 / 摩根大通 | https://qz.com/jp-morgan-forecasts-fed-rate-hikes-december-january-march-112126 | 2026-11-21：市场将 12 月加 25 个基点视为近乎确定，另有约 8% 的 50 个基点可能性；纪要强化了「几乎所有人认为还需要再加」的读法 |
| 其他二次报道 | https://discernmentai.de/community/1736-update-fed-rate-hike-odds-reach-94-following-inflation-data 、https://sembr.live/en/digests/fed-macro-20261121/ | 数字并不完全一致，只用来说明「12 月加 25 个基点被广泛定价」，不采用单一精确概率 |

## 方法边界

- 只读公开帖文、官方网页和官方 API。
- 没有观看视频。官方录像是 https://www.youtube.com/watch?v=hs8YWtNQQ40 ，文本以 https://www.federalreserve.gov/mediacenter/files/FOMCpresconf20261028.pdf 为准。现场口头表述是否与最终实录有实质性出入，本核验未核对。
- 没有对利率期货或债市做实盘下单，也没有在 CME 官方页面保存即时概率截图。
- 没有完整复盘 2025 年市场对降息的定价路径。
