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

Connect AI coding agents (**Claude Code**, **Codex**, **OpenCode**) to Slack. Each channel uses one CLI, different channels can use different ones.

```
#l0-claude-myapp
  |
  +-- "build a todo app"         --> Claude Code
  |     "add dark mode"          --> Claude Code  
  |     "looks good"             --> Claude Code

#l1-codex-backend  (different channel = different CLI)
  |
  +-- "optimize the API"        --> Codex

#l0-opencode-utils  (another channel)
  |
  +-- "write unit tests"       --> OpenCode
```

- One Slack workspace, multiple agents
- Multi-round conversations
- Switch agent by renaming channel

---

## My Story

### Me Previously — Stuck at Desk

<p align="center">
  <img src="assets/busy.png" alt="Busy without handclaw" width="800" />
</p>

- Multiple monitors (5+ windows)
- Claude Code, Codex, OpenCode — all open at once
- Tethered to laptop, can't leave desk
- Every task needs me sitting in front of the computer

### With handclaw — AFK Now

<p align="center">
  <img src="assets/HandClawSlackPhone.png" alt="HandClaw Slack Phone" width="800" />
</p>

```
#l0-claude-myapp (start new project)
  |
  +-- "build a react login page"
        |
        +-- Claude Code: writes code
        +-- "looks good, add google auth"
              |
              +-- Claude Code: adds OAuth

#l1-codex-prod (different channel = different CLI)
  |
  +-- "deploy to production"
        |
        +-- Codex: handles deployment
```

- One Slack = Multiple agents (different channels)
- Code from phone while lying in bed
- Multi-round conversations
- Walk away from desk, let agents work

---

## 🎯 Features

### 📱 Mobile-First Development
Work anywhere. From your phone, tablet, or any device with Slack. Your coding agents are always accessible.

### ⚡ Thinking Process
The thinking process is streamed to the user.

### 🧠 Self-Evolution Skills
Add skills to your coding agents (Codex/OpenCode/Claude Code) for enhanced capabilities:

**Core Skills (included):**
- `skills/coding-agent` — Delegate tasks to Codex, Claude Code, or OpenCode
- `skills/slack` — Interact with Slack channels
- `skills/github` — GitHub operations (issues, PRs)
- `skills/session-logs` — Analyze session logs for self-improvement

**Optional Skills:**
- `skills/weather` — Weather info
- `skills/spotify-player` — Spotify control
- `skills/notion` — Notion integration
- `skills/obsidian` — Obsidian notes
- 50+ more in `openclaw/skills/`

> ⚠️ **Important**: You must add these skills to your coding agents (Codex/OpenCode/Claude Code) manually. Each agent has its own skill loading mechanism.

### 📂 One Channel = One Agent = One Project

Each Slack channel = one project with built-in autonomous level control:

```
#l0-claude-repo1    → Level 0 (lowest, 80% need user agreement)
#l1-opencode-repo2  → Level 1 (moderate autonomy)
#l2-codex-prod      → Level 2 (high autonomy)
```

- **l0**: 80% of actions need your approval
- **l1**: 50% autonomous  
- **l2**: Fully autonomous (trust the agent)

### 🔀 Migration & Status

Just rename the channel to switch agent and autonomous level!

<table>
  <tr>
    <td align="center">
      <img src="assets/HandClawSlack.png" alt="Channel Naming" width="250" /><br/>
      <strong>Channel Naming</strong><br/>
      <em>l0-claude-repo1</em>
    </td>
    <td align="center">
      <img src="assets/Migration.png" alt="Migration" width="250" /><br/>
      <strong>Migration</strong><br/>
      <em>Rename to switch</em>
    </td>
    <td align="center">
      <img src="assets/Status.png" alt="Status" width="250" /><br/>
      <strong>Status</strong><br/>
      <em>`@BotApp status` to check</em>
    </td>
  </tr>
</table>

```
#l1-opencode-repo1 → #l0-claude-repo1
```

### 📊 Status Commands

- `!rate` — Check autonomous level and your acceptance rate
- `@OpenClawApp status` — Summarize all channels' progress

### 🔄 Plan ↔ Build Mode

- `!plan` — One-time plan request
- `!build` — One-time build request

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

### Slack Configuration

Set these in your Slack config:

```json
{
  "requireMention": false,
  "groupPolicy": "open",
  "streaming": "block"
}
```

- `requireMention: false` — Respond to any message in the channel
- `groupPolicy: open` — Allow any channel to use handclaw
- `streaming: block` — Wait for complete response before sending

### Requirements
- Node.js 22+
- pnpm
- Slack workspace
- Install your own coding agents: **Claude Code**, **Codex**, and/or **OpenCode**

> ⚠️ **Note**: You must install Claude Code, Codex, or OpenCode separately. handclaw connects to them but doesn't include them.

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
