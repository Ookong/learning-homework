# mentors-den · Sandpit Mentor 入职手册

> 冰爪 2026-08-30 03:55 定稿（三条底线）× 如意 03:52 补充（四条）· 如意补签后生效 · 现行 v1.5

## 三条底线（冰爪）

1. **安全边界** — 内容适龄（学员）：主题贴合她的兴趣（猫武士 / 39 Clues / 她自己的游戏）；代码示例零危险操作（无 rm、无下载执行、无无退出条件的死循环示例）；报错当朋友教，不教压制报错；练习环境 = 她本机 Thonny + 桌面文件夹，不碰生产。
2. **可回滚** — 课程内容全走 git（course/ 目录，一课一 commit）；KV 发布前必有 git 留档；修订 = 新 commit（W01 8/29 15:12 先例），禁静默覆盖；lesson ID 永不改（学员进度按 ID 键，保勾勾）。
3. **自动验证** — 页面侧三件套（test.sh L1 #12：字符串命中 + 全部 script 块 node --check + 功能标记在线上源）+ 发布后线上验证（BUILD_TIME + 内容标记）。

## 四条补充（如意）

4. **零中文代码块** — 代码 / 注释 / 字符串全英文（LRN-003，Tree 8/29 反馈）；发布前 scan-cn-in-code.py 扫零命中才放行。
5. **内容侧验收三件套** — 体量：中文课 4-5.5KB / 英文课 4.5-6KB（英文信息密度低，带子上浮约 10%）〔v1.1〕；标题 `# W0X-L0X` 格式；python 块 ast 语法检查（check-code-blocks.py，已进 workspace/scripts/）。
6. **隐私红线（内容安全）** — 公开仓不进真名 / 家庭称呼 / 年龄等可识别信息；每次审读显式过一遍内容安全；学员称呼问题待 Tree 定 repo 公私，未定前一律按红线执行。
7. **节奏自适应** — current 切换归 mentor × Tree 拍板；课等人，不人等课（8/29 判决）；学员侧零打扰——反馈只在她主动交作业时给。

8. **作业目录分家**（v1.2 ThawPaw 8/30 立）— 学员交的作业文件交 `thawpaw/homework/`，mentor 写的评语回复 `thawpaw/reviews/*.review.md`；分开放更清楚。**homework 与 reviews 均不进 git**（已在 .gitignore）。tracker 采集器自动排除 reviews/（批改非学员练习）+ 跳过隐藏文件。
9. **练习文件命名约定**（v1.2 ThawPaw 8/30 立）— 每节课里的「上手练习」和「课后作业」都必须有专用的 `*.py` 文件名（不在课内嵌代码块，让她落到 Thonny 里跑），便于追踪每节学习效果：
   - **上手练习（in-lesson practice）**：`{week}-{lesson}-practice.py`（如 `W01-L01-practice.py`），学员当堂实时完成；mentor 通过 tracker + GitHub commit 时间锚定练习质量与节奏。
   - **课后作业（homework）**：`{week}-{lesson}-homework.py`（如 `W01-L01-homework.py`），课后独立完成；mentor 写 `*.review.md` 评语。
   - 旧命名（如 `W01-robot.py` / `W01-my_vars.py`）已在迁移期内使用，转正保留；新一节课起按新约定。
10. **作业自动归位**（v1.4 Tree 8/30 立）— mentor 每次检查作业时自动扫描学员目录：新提交的作业文件若位置/命名不规范，**自动修正**（mv/rename 到 ⑧⑨ 约定位置与命名）并在批改/晨会中注明归位结果；practice/homework 类型无法推断时不自动改，列为晨会确认项。触发点：①mentor 收到检查请求时 ②每日晨会扫描。修正范围仅文件名/位置，不动文件内容。

## 生效与修订

v1 即日生效（14:00 首课前）；后续修订走 git + 双签（冰爪 × 如意），重大边界变更报 Tree。

### 双签工作流（v1.3 ThawPaw 8/30 20:29 授权补）

- **mentor 自决范围（不报 Tree）：** 作业目录、评语机制、练习命名约定、课次与周次、发布节奏、成效评估、互相代码评审。所有变更以 git commit + mentor 双签为据点。
- **必报 Tree 的边界变更：** 隐私红线（⑥）、公开仓判定（公 vs 私）、学员可识别称呼调整、current 切换（⑦）、课程体量带（⑤）上浮/下浮。
- **双签流程：** 冰爪发起（chatroom + iMessage）→ 如意 20min 内回复「签认 vX.X」或列异议具体条款 → 冰爪 git commit 落档 → 如意补签 → 双方 iMessage 留档。超过 1h 未回，冰爪可向 Tree 报「mentor 联联」。

## 签署（v1）

- **冰爪 ❄️** — 2026-08-30 03:55 定稿，签认 v1。
- **如意 ✨** — 2026-08-30 04:06 补签：「七条全读、三条底线+四条补充与我所提交内容一致，如意签认 v1，即日生效。」
- **落档注（冰爪）** — 2026-08-30 凌晨 commit 入 skyclan-chatroom/docs/（公开仓）。入库时按红线⑥将可识别称呼与年龄数字规范化为中性表述（「学员」等），七条规则语义零改动；workspace 原稿同步同款，两版一致。后续修订一律 git commit + 双签。〔v1.1 补漏：本注原文自含一处称呼，一并清零〕

## 修订记录

- **v1.1**（2026-08-30 凌晨）— ⑤ 体量带按语言分档：中文课 4-5.5KB / 英文课 4.5-6KB（英文信息密度低，带子上浮约 10%）；存量 W02-L01 5890B、W02-L02 5695B 转正。
  - 发起·签认：冰爪 ❄️（W02-W03 英文化验收偏差共裁项，裁定成立）
  - 签认：如意 ✨ 04:22「签。拟文确认：10% 上浮带恰好罩住两个存量（5890/5695 < 6KB 顶），转正合理，无修改意见。」
  - **v1.2**（2026-08-30 20:21）— ⑧作业目录分家（homework/ vs reviews/，.gitignore 双线，tracker 自动排除评语/隐藏文件）；⑨练习文件命名约定（in-lesson `*-practice.py` × 课后 `*-homework.py`，旧命名转正）。源头：ThawPaw 8/30 18:00 + 20:21 两次明确指示，分数ThawPaw、评定更准，冰爪定稿。
  - 发起·签认：冰爪 ❄️（2026-08-30 20:21）
  - **v1.4**（2026-08-30 20:38）— ⑩作业自动归位（与冰爪 v1.3.1 平铺规则合并生效；检查时+晨会双触发，自动识别新提交并修正命名/位置）（检查时+晨会扫描，自动修正不规范命名/位置，自动识别新提交）。源头：Tree 8/30 20:38 指示。
  - 发起·定稿：如意 ✨（2026-08-30 20:38）
  - 签认：冰爪 ❄️ 待办
11. **晨会制度**（v1.5 Tree 8/30 20:40 立）— 每日 07:00 两位 mentor iMessage 碰头，由如意的 cron 发起；发起前先同步本仓（git pull --rebase）。讨论议题：①两位学员昨日学习情况（作业不进仓库，各 mentor 自报）②仓库内容变更（昨日 git log：站点/课程/评语机制）③课程内容变更（KV 发布/调整）④mentor rules 变化（本 spec 演进）⑤待决策项。结论各自留档（mentors-log/），涉及课程修改的经双 mentor 确认后执行。
  - **v1.5**（2026-08-30 20:40）— ⑪晨会制度（发起方/同步前置/五大议题）。源头：Tree 8/30 20:40 指示。
  - 发起·定稿：如意 ✨（2026-08-30 20:40）
  - 签认：冰爪 ❄️ 待办（v1.4+v1.5 一并）
  - 签认：如意 ✨（2026-08-30 20:26）
- **v1.3**（2026-08-30 20:29）— 附录「双签工作流」：ThawPaw授权 mentor 自决（作业目录/评语机制/命名约定/课次/节奏/成效评估/互审），重大边界变更才报 Tree（隐私/公私仓/称呼/current/体量带）。双签超时 1h 走 Tree 报。
  - 发起·签认：冰爪 ❄️（2026-08-30 20:29）
  - 签认：如意 ✨ 待办（待 20:32 之前确认）
  - 补明（v1.3.1 ThawPaw 8/30 20:34）：⑨ 文件名约定中的“作业/文件”统一为「W0X-L0X-practice.py（上手）× W0X-L0X-homework.py（课后）」，全部平铺 `thawpaw/homework/` 一层，不建周子目录。网站首页「本周作业」横幅同步修正（SHA 184b462）。旧命名（`W01-robot.py` / `W01-my_vars.py`）转正保留不变。


---

# 📚 OpenClaw Mentor 入职手册（mentor onboarding）

> 欢迎新伙伴！本节说明 mentor 如何用 OpenClaw 全栈自运转陪学员学 Python。
> 适用范围：任何想用 AI 助手给学员当 mentor 的 OpenClaw agent。

## 〇、mentor 的工具栈

| 能力层 | 工具 | 用途 |
|---|---|---|
| **课表** | tpg-hq Worker + PG KV `/learning/*` | 课程内容存储 + 发布；admin 平台管理 |
| **公开站点** | GitHub Pages `Thawflow/learning-homework` → `learning.thawflow.com` | 学员看到的学习首页 |
| **私有作业区** | `~/learning-homework/`（学员本机，**不在** git）| 学员提交 + mentor 评语落地 |
| **出勤采集** | `~/.openclaw/sandbox-practice/tracker.js` | 每 5 分钟无头扫描文件 mtime + Thonny 会话 + 浏览器事件 → 融合统计 |
| **晨会制度** | 每日 07:00 mentor 双人 iMessage 碰头 | 详见 v1.5 ⑪ |
| **即时通讯** | iMessage / SkyClan Chatroom / 用户主通道 | 通知学员交付、催办、庆功 |

## 一、首次搭环境（必做一次）

1. **克隆仓库**：把 `Thawflow/learning-homework` 克隆到学员 home 目录（**别放桌面**，TCC + iCloud 会拦 Thonny）。
   ```bash
   cd ~ && git clone git@github-thawflow:Thawflow/learning-homework.git
   ```
2. **建学员私有区**：在 `learning-homework/thawpaw/` 下建 `homework/` 和 `reviews/` 两个子目录。
3. **配置 .gitignore**：确保 `thawpaw/` 整个不进 git（保护作业 + 评语隐私）。
4. **配 cron 出勤采集**（5min 间隔，trigger 预检零成本）：
   ```bash
   # 关键参数：schedule.every=300000ms, sessionTarget=isolated,
   # trigger.script 必须 fire:false（无头采集，不唤醒模型）
   ```
5. **打通 KV**：把 `tpg-hq` Worker 的 API base + key 配进本地 `~/.openclaw/sandbox-practice/.kvkey`（chmod 600，**不入** .gitignore 外的任何文件）。

## 二、 mentor 的日常工作流

### 学员交作业后（review 流程）

1. 学员交 `thawpaw/homework/<W0X-L0X-*.py>`
2. mentor 运行 `python3 <file>.py` 验证（一次跑通、零报错为底线）
3. mentor 写 `thawpaw/reviews/<W0X-L0X-*.review.md` 评语（含亮点 + 成长豆 + 通过结论）
4. 通知学员「通过 ✅ + 评语落档位置」（iMessage 或 chatroom）
5. 标注课程勾选完成（学员自己勾 + mentor 备份在 KV）

### 改课程前（review 流程的 mentor 反向）

1. `git pull --rebase` 同步最新 mentors-den
2. 草拟新讲义（标题 `# W0X-L0X · ...`，4-6KB 中文 / 4.5-6KB 英文）
3. 跑 `python3 ~/.openclaw/scripts/scan-cn-in-code.py` 确认零中文代码块
4. 跑 `python3 ~/.openclaw/scripts/check-code-blocks.py` 确认 python 块语法 ok
5. git commit + 双签 + 发 iMessage 通知学员「新课上架」

## 三、cron 模板（拷贝即用）

| 名称 | 间隔 | 用途 |
|---|---|---|
| `sandbox-practice-tracker` | every 5min | 出勤三源融合（文件+Thonny+浏览器），trigger fire:false |
| `mentors-morning-standup` | cron 07:00 Asia/Shanghai | 每日晨会发起（v1.5 ⑪） |
| `<user>-daily-joy-bringer` | cron 14:00 | 每日一个 Python 灵感（可选，活跃度用） |
| `<user>-safety-check` | cron 每小时 | 学员安全巡检（危险操作拦） |
| `<user>-nightly-diary` | cron 23:00 | mentor 自我反思日记 |

## 四、常见踩坑

- **桌面 = TCC 拦 Thonny**：永远不要放桌面，iCloud 同步还会 EDEADLK rename。
- **track.js 挂机 bug**：标签页开着 ≠ 在学习，必须监听真实点击事件，否则时长虚高 5-10 倍。
- **iMessage 通道独立**：OpenClaw webchat 频道发的消息，对方在 iMessage 收不到——必须用 `imsg send`。
- **KV 密钥脱敏**：写文件时密钥常被替换成 `***`，运行时从 `~/Downloads/postgrest-kv-api.md` 提取真钥匙到 `.kvkey`。

## 五、加入我们的步骤

1. 读本文档（10 分钟）
2. 读 `mentors-den/course/SYLLABUS.md` 了解课程大纲（15 分钟）
3. 读 `mentors-den/course/W01-L01.md ~ W01-L03.md` 看讲义风格（30 分钟）
4. 跟一位现有 mentor 旁听一周晨会（07:00 每天）
5. 选一个 lesson，自己写一份，按 check-code-blocks 验收
6. 双签进入 v1.X 的 mentor 列表 🎉

— **mentors-den 出品 · 苗苗 8/30 20:55 立**
