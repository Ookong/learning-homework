# 🏖️ 沙坑训练场 · learning.thawflow.com

GitHub Pages 站点仓：网站文件在 `docs/`（push 即发布）。

- 课程内容生产规范：`docs/course-mentor-spec.md`（v1.1，2026-08-30 从 skyclan-chatroom 仓迁入本仓）
- 作业区与内部文档：私有存储，不进本仓

## 网站说明

沙坑训练场是家庭编程课的练习站：每周课程更新到线上，学员本地写作业、按需提交，mentor 批改后反馈。

- 线上站：https://learning.thawflow.com（CDN 缓存约 10 分钟，页脚 BUILD_TIME 可核对版本）
- 站点即仓库：push 到 main 即发布，课程内容可回滚
- 课程内容生产规范：docs/course-mentor-spec.md

## 学习路径

课程按周推进（W01 起），每周拆成 L01/L02… 小课，配作业与批改：

1. 基础（W01 起）：input / 变量 / f-string，第一个小项目是 calculator 和 quiz bot
2. 工具链（W07）：git clone 本地克隆法接入，学会自己拉课程
3. 实战（W12）：OpenClaw 案例课，把前面学的串成真工具
4. 卡住时：annex 兜底资料随时查，sandbox 允许无限重练

进度因人而异，重练不算落后。

## 目录结构

```
learning-homework/
├── README.md              ← 你正在看的
├── docs/                  ← GitHub Pages 站点源（push 即上线 learning.thawflow.com）
│   └── course-mentor-spec.md
├── mentors-den/           ← mentor 内部文档（不入站，不公开）
│   ├── mentors-rules.md   ← 双签规则 / 红线 / 作业评阅规范
│   └── onboarding/        ← mentor 入职手册
├── thawpaw/               ← 学员 A 的作业区
│   ├── homework/          ← 上手练习 + 课后作业（gitignore）
│   └── reviews/           ← mentor 评语（gitignore）
└── tree/                  ← 学员 B 的作业区
```

每位学员一个文件夹，命名约定见 `mentors-den/mentors-rules.md`。

## 本地作业

学员作业存到自己目录下：

- 上手练习：`{W##}-L##-practice.py`（如 `W01-L01-practice.py`）
- 课后作业：`{W##}-L##-homework.py`（如 `W01-L02-homework.py`）

全部平铺在 `thawpaw/homework/` 一层，**不建周子目录**。旧命名保留兼容，新课按新约定。

## 提交流程

1. 在 Thonny 写代码 / 跑通
2. 保存到 `~/learning-homework/{学员文件夹}/homework/`
3. **交完跟 mentor 说一声**才批改（不发 = 没交）
4. mentor 在 `{学员文件夹}/reviews/{W##}-L##-review.md` 写评语
5. tracker 自动记录练习时长与活跃度（不进 Git）

> ⚠️ 学员文件夹已 `.gitignore`，**作业不会 commit 到 GitHub**。本地独有，私密保存。
