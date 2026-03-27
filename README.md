# Know Your Owner 🧠

**让 AI 助手第一天就懂你**

新装好 AI 助手 / [OpenClaw](https://github.com/openclaw/openclaw)，它不知道你是谁。跑一遍 Know Your Owner，它就像认识你很久了——自动从你的社交平台采集数据，交叉分析生成精准的个人画像，直接写好 USER.md 和 MEMORY.md。

🌐 **中文** | [English](./README.en.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT) [![GitHub stars](https://img.shields.io/github/stars/ClawCap/Know-Your-Owner.svg)](https://github.com/ClawCap/Know-Your-Owner)

---

## 💡 为什么需要 Know Your Owner？

AI 助手的最大痛点：**它不了解你**。

| | 没有 Know Your Owner | 用了 Know Your Owner |
|---|---|---|
| **助手对你的了解** | 从零开始，每次都要解释自己的喜好 | 第一天就知道你喜欢什么、关注什么、是什么样的人 |
| **个性化程度** | 通用回答，和对所有人一样 | 精准到"你小红书收藏了34条面食做法，所以推荐面食餐厅" |
| **建档方式** | 手动填写问卷，费时且不全面 | 自动从5个平台采集，10-20分钟完成 |
| **数据安全** | — | 数据存本地，推断和事实严格区分，敏感信息不下结论 |

> **一句话总结：跑一遍这个 Skill，你的 AI 助手就从"陌生人"变成"老朋友"。**

---

## 🚀 快速体验

### 方式一：让龙虾帮你安装（推荐 🦞）

如果你正在使用 [OpenClaw](https://github.com/openclaw/openclaw)，直接把下面这句话发给你的龙虾：

```text
请帮我安装 Know Your Owner Skill，从这个 GitHub 仓库下载整个项目：
https://github.com/ClawCap/Know-Your-Owner
```

龙虾会自动完成：下载 Skill → 检测并安装 [ManoBrowser](https://github.com/ClawCap/ManoBrowser)（依赖的浏览器工具） → 引导你完成配置 → 开始画像采集。

### 方式二：手动安装（2 分钟）

**① 下载 Skill 包**

```bash
git clone https://github.com/ClawCap/Know-Your-Owner.git
```

将整个目录放到你的 AI 客户端的 skills 目录下（如 OpenClaw 的 `~/.openclaw/skills/know-your-owner/`）。

**② 让 AI 助手读 SKILL.md 开始**

AI 助手读取 SKILL.md 后会自动检测环境、安装依赖（ManoBrowser）、引导配置，然后开始画像采集。

---

## 📋 功能一览

### 🎯 支持 5 大社交平台深度采集

| 平台 | 采集内容 | 示例 |
|------|---------|------|
| 🎵 **抖音** | 个人资料、作品、喜欢、收藏、关注列表 | "关注了214个舞蹈类账号" |
| 📕 **小红书** | 个人资料、笔记、收藏、点赞 | "收藏了34条面食做法" |
| 🐦 **微博** | 个人资料、微博、关注、收藏 | "近期微博主要讨论AI和编程" |
| 📖 **豆瓣** | 个人资料、看过/想看电影、读过/想读书、广播 | "213本书打分率69%，硬科幻信徒" |
| 📺 **B站** | 个人资料、投稿、收藏夹内容、关注列表 | "93条教程收藏分4个夹子" |

还支持**通用模式**——告诉 AI 助手你用的其他平台（知乎、即刻、快手等），它会通过 ManoBrowser 实时探索采集。

### 🔍 六维度交叉分析

不是贴标签，是用数据做精准洞察：

| 维度 | 分析方式 | 示例 |
|------|---------|------|
| **创作者身份** | 跨平台作品主题一致性分析 | "抖音和B站都在做像素风游戏教程" |
| **收藏内容细分** | 细粒度分类，不停留在大类 | "B站93条教程收藏分编程/设计/音乐3个夹子" |
| **关注列表聚类** | 按类型统计创作者/知识/电竞/美食等 | "关注列表60%是独立游戏开发者" |
| **评分行为解码** | 打分率/一星率/补标行为识别 | "豆瓣打分率69%，严格型，唯一一星给了鸡汤书" |
| **职业学业推断** | 从收藏/关注内容推断当前阶段 | "系统性收藏了10条考研备考资料（推断）" |
| **隐藏信息挖掘** | 跨平台矛盾点和意外模式 | "B站追番200+但豆瓣只标了30部动画" |

### 📊 生成精准个人画像

自动写好两个文件：

- **USER.md**：姓名、背景、核心身份、兴趣图谱、性格线索、社交平台
- **MEMORY.md**：详细画像（证据链+结论）、隐藏发现、一句话画像、平台活跃度排序

**画像示例**（虚构用户）：
> "像素风独立游戏开发者，B站93条教程收藏分4个夹子，小红书收藏34条面食做法——一个会做饭的码农。"

### 🔄 持续更新

- **全量刷新**："刷新画像" → 重新采集所有平台，对比变化
- **单平台刷新**："刷新我的B站数据" → 只重跑B站
- **原始数据复用**：采集的数据按平台存为 JSON，后续可以直接查询（"我豆瓣看过的科幻电影有哪些？"）

---

## 🎯 适用场景

### 🦞 OpenClaw 新用户 Onboarding
装好 OpenClaw 后第一件事：跑 Know Your Owner。龙虾从"啥都不知道"变成"像认识你很久了"。

### 🤖 任何 AI 助手的个性化
不限于 OpenClaw——任何需要了解用户的 AI 助手都能用。采集数据 → 生成画像 → 写入记忆文件。

### 📱 个人数据管理
采集的原始数据存本地，可以随时：
- 导出豆瓣电影/书单为表格
- 整理B站收藏夹（去重/分类）
- 生成年度观影报告
- 跨平台兴趣分析

---

## 🔐 隐私与安全

- **数据完全本地**：采集的数据存在你电脑上的 `know-your-owner-data/` 目录，不上传任何服务器
- **只采集你自己的数据**：只访问你已登录的个人主页，不采集他人信息
- **事实与推断严格区分**：敏感信息（感情/健康/收入）只陈述数据事实，不下结论
- **用户确认后才写入**：画像生成后展示给你确认，不准的可以修改或删除
- **随时可删**：删除 `know-your-owner-data/` 目录即清除所有采集数据

---

## 📁 项目结构

```
Know-Your-Owner/
├── SKILL.md                              ← 主 Skill 文件（AI 助手读这个）
├── douyin-deep-profile-collect/          ← 🎵 抖音采集模块
├── xiaohongshu-deep-profile-collect/     ← 📕 小红书采集模块
├── weibo-deep-profile-collect/           ← 🐦 微博采集模块
├── douban-deep-profile-collect/          ← 📖 豆瓣采集模块
├── bilibili-deep-profile-collect/        ← 📺 B站采集模块
├── workflows/                            ← 采集工作流
└── examples/                             ← 画像示例（虚构用户）
    ├── USER.md
    └── MEMORY.md
```

**依赖**：[ManoBrowser](https://github.com/ClawCap/ManoBrowser)（首次使用自动从 GitHub 下载安装）

---

## 📄 License

[MIT](LICENSE) — 自由使用、修改、分发。

---

**⭐ 如果 Know Your Owner 对你有帮助，给个 Star 支持一下！**
