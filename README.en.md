# Know Your Owner 🧠

**Your AI assistant understands you from day one.**

Just set up your AI assistant / [OpenClaw](https://github.com/openclaw/openclaw)? It doesn't know who you are. Run Know Your Owner once, and it'll feel like it's known you for years — automatically collecting data from your social platforms, cross-analyzing to build a precise personal profile, writing USER.md and MEMORY.md for you.

🌐 [中文](./README.md) | **English**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT) [![GitHub stars](https://img.shields.io/github/stars/ClawCap/Know-Your-Owner.svg)](https://github.com/ClawCap/Know-Your-Owner)

---

## 💡 Why Know Your Owner?

The biggest pain point of AI assistants: **they don't know you.**

| | Without Know Your Owner | With Know Your Owner |
|---|---|---|
| **How well it knows you** | Starts from zero, you explain preferences every time | Knows your interests, follows, and personality from day one |
| **Personalization** | Generic answers, same for everyone | Precise: "You bookmarked 34 pasta recipes on Xiaohongshu, so here's a pasta restaurant" |
| **Profile building** | Manual questionnaires, tedious and incomplete | Auto-collects from 5 platforms, done in 10-20 minutes |
| **Data safety** | — | Data stays local, inferences clearly labeled, no conclusions on sensitive topics |

> **TL;DR: Run this Skill once, and your AI assistant goes from "stranger" to "old friend".**

---

## 🚀 Quick Start

### Option 1: Let your AI agent install it (Recommended 🦞)

If you're using [OpenClaw](https://github.com/openclaw/openclaw), just send this to your agent:

```text
Please install Know Your Owner Skill by downloading the entire project:
https://github.com/ClawCap/Know-Your-Owner
```

Your agent will automatically: download the Skill → detect and install [ManoBrowser](https://github.com/ClawCap/ManoBrowser) (browser tool dependency) → guide you through setup → start profile collection.

### Option 2: Manual installation (2 minutes)

**① Download the Skill**

```bash
git clone https://github.com/ClawCap/Know-Your-Owner.git
```

Place the directory in your AI client's skills folder (e.g. OpenClaw's `~/.openclaw/skills/know-your-owner/`).

**② Let your AI assistant read SKILL.md**

It will auto-detect the environment, install dependencies (ManoBrowser), guide configuration, and start profile collection.

---

## 📋 Features

### 🎯 Deep Collection from 5 Social Platforms

| Platform | What it collects | Example |
|----------|-----------------|---------|
| 🎵 **Douyin (TikTok CN)** | Profile, posts, likes, favorites, following list | "Following 214 dance-related accounts" |
| 📕 **Xiaohongshu (RED)** | Profile, notes, bookmarks, liked posts | "Bookmarked 34 pasta recipes" |
| 🐦 **Weibo** | Profile, posts, following, favorites | "Recent posts mainly about AI and coding" |
| 📖 **Douban** | Profile, movies watched/wanted, books, broadcasts | "213 books rated, 69% rating rate, hard sci-fi fan" |
| 📺 **Bilibili** | Profile, uploads, favorite folders, following list | "93 tutorial bookmarks in 4 folders" |

Also supports **generic mode** — tell your AI assistant about other platforms you use, and it'll explore and collect using ManoBrowser.

### 🔍 Six-Dimensional Cross Analysis

Not just labels — precise insights backed by data:

| Dimension | How | Example |
|-----------|-----|---------|
| **Creator identity** | Cross-platform content consistency | "Posts pixel game tutorials on both Douyin and Bilibili" |
| **Bookmark breakdown** | Fine-grained categorization | "93 Bilibili bookmarks split into coding/design/music folders" |
| **Following clusters** | Type distribution analysis | "60% of follows are indie game developers" |
| **Rating behavior** | Rating patterns and strictness | "69% rating rate on Douban, strict type, only 1-star was a self-help book" |
| **Career/education** | Inferred from bookmarks and follows | "Systematically bookmarked 10 grad school prep posts (inferred)" |
| **Hidden patterns** | Cross-platform contradictions | "200+ anime on Bilibili but only 30 marked on Douban" |

### 📊 Generates Precise Personal Profile

Auto-writes two files:
- **USER.md**: Name, background, core identity, interest map, personality clues, social accounts
- **MEMORY.md**: Detailed profile with evidence chains, hidden discoveries, one-line summary

### 🔄 Continuous Updates

- **Full refresh**: "Refresh my profile" → re-collect all platforms, compare changes
- **Single platform**: "Refresh my Bilibili data" → re-run Bilibili only
- **Data reuse**: Raw data stored as JSON per platform, queryable anytime

---

## 🎯 Use Cases

### 🦞 New User Onboarding for OpenClaw
First thing after setting up OpenClaw: run Know Your Owner. Your agent goes from "knowing nothing" to "feels like an old friend".

### 🤖 Personalization for Any AI Assistant
Not limited to OpenClaw — any AI assistant that needs to understand its user can benefit. Collect data → build profile → write to memory files.

### 📱 Personal Data Management
Raw data is stored locally. You can:
- Export Douban movie/book lists as spreadsheets
- Organize Bilibili favorites (deduplicate/categorize)
- Generate annual viewing reports
- Cross-platform interest analysis

---

## 🔐 Privacy & Security

- **Fully local data**: Collected data stays in `know-your-owner-data/` on your machine, never uploaded
- **Your data only**: Only accesses your own logged-in profile pages, never others'
- **Facts vs inferences**: Sensitive topics (relationships/health/income) only state data facts, never draw conclusions
- **User confirmation**: Profile is shown for your approval before saving — you can edit or remove anything
- **Easy deletion**: Delete the `know-your-owner-data/` directory to remove all collected data

---

## 📁 Project Structure

```
Know-Your-Owner/
├── SKILL.md                              ← Main skill file (AI assistant reads this)
├── douyin-deep-profile-collect/          ← 🎵 Douyin collection module
├── xiaohongshu-deep-profile-collect/     ← 📕 Xiaohongshu collection module
├── weibo-deep-profile-collect/           ← 🐦 Weibo collection module
├── douban-deep-profile-collect/          ← 📖 Douban collection module
├── bilibili-deep-profile-collect/        ← 📺 Bilibili collection module
├── workflows/                            ← Collection workflows
└── examples/                             ← Profile examples (fictional user)
    ├── USER.md
    └── MEMORY.md
```

**Dependency**: [ManoBrowser](https://github.com/ClawCap/ManoBrowser) (auto-downloaded from GitHub on first use)

---

## 📄 License

[MIT](LICENSE) — free to use, modify, and distribute.

---

**⭐ Star this repo if Know Your Owner helps you!**
