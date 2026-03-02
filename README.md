# 🤖 handclaw

<p align="center">
  <img src="assets/logo.png" alt="handclaw" width="500" />
</p>

<p align="center">
  <strong>One Slack = Multiple AI Coding Agents</strong>
</p>

<p align="center">
  Code anywhere. From anything. Anytime.
</p>

---

## ✨ What is handclaw?

**handclaw** lets you control AI coding agents directly from Slack — no more jumping between windows, no more monitor clutter, no more being tied to a desk.

Connect to **Claude Code**, **Codex**, and **OpenCode** through a single Slack workspace. Just chat and let them build.

```
📱 Slack → "Hey, build me a React component" → 🤖 Claude Code → ✅ Done
```

> **"I can finally code from my phone while lying in bed."** — Every developer who tried it

---

## 🚀 The Difference

<p align="center">
  <strong>Without handclaw — Chaos</strong>
</p>

<p align="center">
  <img src="assets/busy.png" alt="Busy without handclaw" width="800" />
</p>

<p align="center">
  <em>Multiple monitors. Tethered to your desk. Constant context switching.</em>
</p>

---

<p align="center">
  <strong>With handclaw — Freedom</strong>
</p>

<p align="center">
  <img src="assets/HandClawSlackPhone.png" alt="HandClaw Slack Phone" width="800" />
</p>

<p align="center">
  <em>One Slack. Any device. Code from anywhere.</em>
</p>

---

## 🎯 Features

### 📱 Mobile-First Development
Work anywhere. From your phone, tablet, or any device with Slack. Your coding agents are always accessible.

### 📂 One Channel = One Agent = One Project
Each Slack channel = one project. No more tab chaos. Organize your work by channel:
- `#project-alpha` → Claude Code
- `#project-beta` → Codex
- `#hotfix` → OpenCode

### ⚡ Switch Agents Instantly
Want to try a different agent? Just rename your channel:
```
#my-project-claude → #my-project-codex
```
Done. Agent switched. Zero config.

### 🔄 Plan ↔ Build Mode
Smoothly toggle between planning and building. Discuss architecture with one agent, then hand off to another for implementation — without leaving Slack.

### 📊 Agent Observability
Monitor your coding agents in real-time:
- Success rate tracking
- Autonomous level indicators
- Performance metrics

---

## 📸 Demo

<p align="center">
  <img src="assets/HandClawSlackDesktop.png" alt="HandClaw Desktop Demo" width="800" />
</p>

**Live Demo**: _[Add your demo URL here]_

---

## 🛠️ Quick Start

```bash
# Clone and install dependencies
git clone https://github.com/deciding/handclaw.git
cd handclaw
git submodule update --init --recursive
cd openclaw

# Install and build
pnpm install
pnpm ui:build
pnpm build

# Set up Slack connection and install daemon
pnpm handclaw onboard --install-daemon
```

### Requirements
- Node.js 22+
- pnpm
- Slack workspace
- At least one AI coding agent (Claude Code, Codex, or OpenCode)

---

## 📖 Documentation

- [Getting Started](https://docs.openclaw.ai/start/getting-started)
- [Slack Setup](https://docs.openclaw.ai/channels/slack)
- [Agent Configuration](https://docs.openclaw.ai/concepts/models)
- [Channel Management](https://docs.openclaw.ai/channels)

---

## 🤝 Contributing

PRs welcome! This is a fork of [OpenClaw](https://github.com/openclaw/openclaw) — the amazing whale project that makes all this possible.

---

## 📜 License

MIT

---

## 🐋 Built on OpenClaw

handclaw is a personal fork of [OpenClaw](https://openclaw.ai) — the open-source personal AI assistant framework. OpenClaw connects to 15+ messaging channels and supports multiple AI providers.

Check out the main project: [github.com/openclaw/openclaw](https://github.com/openclaw/openclaw)

---

<p align="center">
  <strong>Try it now →</strong>
</p>
