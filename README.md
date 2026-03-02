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

### ⚡ Thinking Process
The thinking process is streamed to the user.

### ⚡ Self-Evolution
We add self evolution skills to each agent.

### 📂 One Channel = One Agent = One Project

Each Slack channel = one project with built-in autonomous level control:

<p align="center">
  <img src="assets/HandClawSlack.png" alt="Channel Naming Convention" width="800" />
</p>

```
#l0-claude-repo1    → Level 0 (lowest, 80% need user agreement)
#l1-opencode-repo2  → Level 1 (moderate autonomy)
#l2-codex-prod      → Level 2 (high autonomy)
```

- **l0**: 80% of actions need your approval
- **l1**: 50% autonomous  
- **l2**: Fully autonomous (trust the agent)

### 🔀 Migration

Just rename the channel to switch agent and autonomous level!

<p align="center">
  <img src="assets/Migration.png" alt="Migration Demo" width="600" />
</p>

```
#l1-opencode-repo1 → #l0-claude-repo1
```

### 🔄 Plan ↔ Build Mode

Smoothly toggle between planning and building:

- `!code switch plan/build` — Switch persistently between plan/build mode
- `!plan` — One-time plan request (stays in current agent)
- `!build` — One-time build request (stays in current agent)

### 📊 Agent Observability & Status

Monitor your coding agents in real-time:

<p align="center">
  <img src="assets/Status.png" alt="Status Demo" width="600" />
</p>

- `!rate` — Check autonomous level and your acceptance rate
- `@OpenClawApp status` — Summarize all channels' progress

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
