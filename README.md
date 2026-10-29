# Mirror

A database-backed dashboard for growth analysis: point Mirror at your MySQL /
PostgreSQL / StarRocks / Doris / ClickHouse and instantly get order tracking,
new-user metrics, user profiles and segmentation — **no SQL, no dependencies**.

**Latest release: v1.0.7** — see [What's new](#whats-new) below.

## Download & run (Windows 10 / 11)

1. Get the latest `mirror.exe` from the
   [Releases](../../releases) page — a single file, no installer, no Python.
2. Double-click it. Your browser automatically opens the connection page at
   `http://127.0.0.1:8765`.
3. Enter your database address — that is all it takes to see the dashboards
   (connect **read-only**; Mirror never writes to your database).

> Windows SmartScreen may warn about an unsigned binary:
> click **More info → Run anyway**.

## Privacy — nothing ever leaves your machine

- Mirror connects **only** to your own database, using connection strings you
  enter yourself.
- The connection is **strictly read-only** — Mirror never writes a single row
  to your business database.
- There is **no upload pipeline at all**: no telemetry, no CDN, no analytics,
  no remote server — the binary contains nothing that phones home.
- All derived metrics, session state and preferences stay in local storage on
  your own computer.

## Requirements

- Windows 10 / 11 (64-bit)
- A database: MySQL 5.7+, PostgreSQL 12+, StarRocks, Doris or ClickHouse,
  with a read-only account (recommended)

## What's new

<!-- CHANGELOG:START -->
- **[v1.0.7](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.7)** — 漏斗两期对比、诊断去年同比、日期显示星期
  - 漏斗支持两期对比：任选两个日期区间，转化率变化一眼看清
  - 诊断页尾部新增「去年同比」两卡：已支付金额 / 新增用户数对照去年同期
  - 选中日期后显示星期，如「数据截至 2026-09-19（周六）」
  - 渠道单列扩充：知乎/头条/QQ 空间/贴吧/豆瓣/即刻/脉脉/虎扑等国内二线社区 8 档
  - B 站常见叫法全收录：小破站/破站/哔哩/biliapp/b23.tv
  - 城市名归一：「北京/北京市」不再拆成两行；地名归一支持国际（日语都道府県、拉丁写法、缩写别名）
  - 渠道名支持英文/日文显示名，数据认标准名、界面按语言切换
  - 新增英文版 README
  - 修复英文系统下启动输出导致的崩溃（构建链路加固）
- **[v1.0.5](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.5)** — 一句话取数 SQL 生成增强 + 前端语法修复
- **[v1.0.4](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.4)** — AI智答升级——右下角悬浮问答、规则式画图（折线/饼图/条形）、对话历史与失败重试、本地执行日志
- **[v1.0.3](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.3)** — 业务节奏内联进经营诊断（金额结论下方）+ 同比行 + 因子树 + 异动日入口
- **[v1.0.2](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.2)** — 爆款页聚焦潜力爆款、侧栏卡片搜索、自然月口径标注、/lazy 流式补丁链路
- **[v1.0.1](https://github.com/joseygo/Mirror-Growth/releases/tag/v1.0.1)** — feat: 应用内更新检查 + 连接门双栏改版，版本 1.0.1
  - 更新检查：启动后台静默查 mirror-release 最新版（匿名 GET、3s 超时、
  - 失败无声；成功24h/失败2h冷却），/api/update_check 端点 + 两页可关闭
  - 横幅，点 × 后同版本不再提示；不做自动下载自替换。
  - 连接门：左右双栏（左特性列表 / 右表单卡），版权+版本号收进左栏底部，
  - 右侧页脚移除；修正 <script> 误插 </main> 前的既有结构错误。
- **[v0.1.1](https://github.com/joseygo/Mirror-Growth/releases/tag/v0.1.1)** — docs+ui: 「记住配置」改名「保存信息」，连接门与 README 统一口径
- **[v0.1.0](https://github.com/joseygo/Mirror-Growth/releases/tag/v0.1.0)** — ci: v* 标签改为发布 exe 到公开分发仓 mirror-release
  - 本仓即将转私有（先 exe 闭源分发、后开源），Release 改挂到独立的公开仓库，新增 release/README.md 作为分发仓主页（含版权声明），发布凭据走 secret RELEASE_TOKEN（GITHUB_TOKEN 作用域出不了本仓）。
<!-- CHANGELOG:END -->

## Feedback

The only official feedback channel is email to the author,
**joseygogogo@gmail.com** (there is also a link in the app footer).

## License

© Josey. Mirror is distributed as a free executable for personal and
internal business use; decompiling, repackaging or commercial redistribution
is not permitted.
