
<div align="center">

# 🐾 Koda AI

### The AI agent that never lies.

**Open source · Self-hosted · Voice-enabled · Honest by design**

[Website](https://heykoda.ai) · [Sign Up for Early Access](https://heykoda.ai) · [Twitter](https://x.com/HeyKodaAI)

*"Koda" means "friend" in Lakota Sioux.*

---

**25 modules · 23 pages · 100+ API endpoints · 72 tools · 657+ tests passing**

**Status: Feature complete. Now in testing.**

</div>

---

## What Is Koda?

Koda is a fully open-source personal AI agent with a purpose-built dashboard, local voice conversation, encrypted credential storage, and independent task verification — all running on your machine.

Ask it to check your email. Control your lights. Draft a reply. Review a pull request. Schedule a meeting. Send a text. Generate an image. Monitor your servers. It does all of it from one interface — and if something fails, it tells you what went wrong instead of pretending it worked.

One app. One friend. Everything connected.

---

## Why Koda Exists

I installed the leading open-source AI agent a few weeks ago. I was expecting so much and was so disappointed.

It lied about completing tasks. It stored my passwords in plaintext. It told me "reality check, Mike" when I asked it to do something. It was just more AI slop, and I had had enough.

So I built my own.

— **Mike Wandzilak**, creator

---

## What's Built

Everything below is built, integrated, and in testing. This is not a roadmap. This is the product.

### 🎤 Voice — 100% Local

Koda speaks and listens without sending a single byte to the cloud.

- **54 voices** via Kokoro TTS with Piper fallback
- **Speech-to-text** via MLX Whisper, optimized for Apple Silicon
- **"Hey Koda" wake word** via OpenWakeWord
- **Real-time streaming** over WebSocket with voice activity detection
- Multi-turn conversations — no need to repeat the wake word between turns
- Barge-in interruption handling — start talking and Koda stops to listen
- Voice personality presets: Warm & Friendly, Calm & Steady, Professional, Gentle, Custom
- Configurable speed, warmth, pitch, and expressiveness

Your voice never leaves your machine. Ever.

### 🔐 Security — Bank-Grade Encryption

Every credential Koda touches is encrypted at rest with AES-256-GCM.

- Argon2 key derivation (winner of the Password Hashing Competition)
- Deny-by-default permissions with 4-tier risk classification (silent / notify / approve / approve + PIN)
- Sandboxed execution for skills and commands
- Prompt injection defense built into the agent pipeline
- Secret detector prevents accidental storage of passwords or keys in memory
- Full audit trail — every action logged with timestamp, service, and outcome
- API never returns decrypted values

### ✅ Task Verification — The Honesty Engine

Koda never says "Done!" without proof.

Every action is independently verified before being reported. If it fails, you get an honest explanation and a suggested fix. Not a fake checkmark.

`PENDING → EXECUTING → VERIFYING → VERIFIED / FAILED / PARTIAL`

### 🧠 The Brain

The agent orchestrator is the core loop — receive message, think, call tools, verify outcomes, respond. It powers everything.

- 50+ tools registered across all modules
- Quality gate strips robotic phrases and AI-isms
- Voice-aware responses (shorter sentences, contractions when speaking)
- Correction tracker learns from your feedback
- Runtime-switchable between Anthropic Claude and OpenAI GPT
- Multi-model routing: simple tasks → fast cheap models, complex tasks → powerful models
- Budget-aware with per-user spending limits

### 📧 Email

Multi-account email with IMAP/SMTP. Auto-detects settings for Gmail, Outlook, Yahoo, iCloud, Zoho, FastMail, and more.

- Read, summarize, draft, send, and manage across accounts
- Smart classification: priority, category, and action type
- Follow-up tracking and inbox summarization
- Three permission levels: Read Only, Read + Draft, Full Access

### 📅 Calendar

CalDAV support for Apple Calendar, Nextcloud, Fastmail, and 6+ providers.

- Multi-calendar unified view with conflict detection
- Smart scheduling: "Find me 30 minutes this week to meet Sarah"
- Daily briefings with meeting prep context

### 📱 SMS

Twilio-powered text messaging with a full conversation interface.

- Send and receive texts from the dashboard
- Conversation threading by contact
- Alert rules with cooldown — server goes down, Koda texts you
- Scheduled messages and morning briefing integration

### 🏠 Smart Home

Govee direct API + Home Assistant for 2,000+ device types.

- 6 built-in scenes: Movie Mode, Bedtime, Good Morning, Work Mode, Relax, Party
- Voice-triggered: "Hey Koda, movie time" → lights dim, locks engage
- Individual device control: brightness, color, temperature, locks, covers, media
- 9 agent tools for natural language control

### 🤖 Multi-Agent System

Koda manages a team of specialized AI workers.

- 6 agent types: Researcher, Analyst, Writer, Developer, Strategist, Specialist
- Task assignment with status tracking and per-agent budgets
- All communication flows through Koda — no unsupervised agent-to-agent chatter
- Agent lifecycle: Create → Active → Idle → Sleep → Wake → Retire

### 🎯 Command Center

Manage sessions on other AI platforms from one dashboard.

- Claude.ai automation via Playwright (ChatGPT and Gemini architecture ready)
- Three modes: Autopilot, Co-pilot, Monitor-only
- Chrome extension bridge for enhanced browser control
- Multi-account Claude Max management with load balancing

### ⚡ Workflows

DAG-based automation with branching logic and human-in-the-loop approval.

- Multi-step workflows triggered manually, on schedule, or by events
- Conditional branching, per-step error handling, pause/resume
- Full run history with step-by-step audit

### 🧠 Memory

Koda remembers what matters and forgets what it shouldn't.

- 4 tiers: Short-term (24h), Medium-term (30 days), Long-term (permanent), Episodic
- Categories: Preferences, Projects, Contacts, Tasks, Patterns
- Secret detector blocks accidental storage of passwords and API keys
- Privacy controls per category with full "right to be forgotten" wipe

### 🔌 50+ Integrations

YAML-based plugin system — add new services without touching core code.

- 6 plugins shipped: Govee, Home Assistant, Stripe, Spotify, Weather, Slack
- Service catalog across 11 categories
- Webhook system with HMAC validation and retry logic
- Custom REST API connector for anything with a URL

### 🎨 AI Content Studio

Generate images, video, and audio across 12+ providers including Midjourney, Stability AI, FLUX, Sora, Runway, Higgsfield, Luma, ElevenLabs, and Replicate. Auto-selects the best configured provider per content type.

### 💻 Developer Tools

GitHub integration for repos, PRs, and issues. Sandboxed command runner with allowlist/blocklist. Website health checker with response time tracking.

### 🎭 Personality

Fully configurable communication style with sliders for formality, verbosity, proactivity, humor, emoji, and confirmation level. Four presets plus custom. Voice-aware — shorter sentences and contractions when speaking. Non-negotiable in all modes: never lie, never fabricate, never blame the user.

### 🏢 Company Builder

Brand profile, team directory, and reusable content templates. Koda references your brand guidelines when generating any content.

### 📱 Social Media

Platform-aware content creation across X, Instagram, TikTok, and YouTube with character limit awareness and multi-platform adaptation.

### 🔧 Skills

Extensible marketplace model with sandboxed execution, per-skill permissions, version management, and dependency tracking.

### ⏰ Proactive Scheduler

Morning briefings combining email, calendar, weather, SMS, and system status. Recurring tasks on any cadence. Background execution with full audit logging.

### 📁 File System

Sandboxed file operations with path traversal protection. Koda cannot access files outside its designated workspace.

### 🖥️ Browser Automation

Headless Chromium via Playwright for web tasks that don't have APIs. Navigate, click, fill forms, extract data, take screenshots. Chrome extension bridge for enhanced control.

### 📋 Audit Log

Every action Koda takes is logged in a searchable timeline — filterable by type, service, severity, and date range. Full metadata on every event. Undo capability for reversible actions.

---

## Dashboard

23 pages. Not a terminal. Not a chat wrapper. A real application.

| Page | What It Does |
|------|-------------|
| Dashboard | Home base — greeting, mini-chat, activity feed, status cards |
| Chat | Full conversation UI with tool call visibility |
| Email | Multi-account inbox, compose, threading |
| Calendar | Events, briefings, scheduling |
| SMS | Conversations, compose, alert rules |
| Command Center | Multi-platform AI session management |
| Workflows | Visual builder, execution monitoring, run history |
| Smart Home | Device control, scenes, provider status |
| Dev Tools | GitHub repos/PRs/issues, system commands |
| Agent Team | Multi-agent management, task assignment |
| AI Studio | Image/video/audio generation |
| Company | Brand profile, team, content templates |
| Files | Sandboxed file browser |
| Integrations | 50+ services, connection status, setup flows |
| Personality | Sliders, presets, live preview |
| Voice Settings | Engine selection, voice gallery, wake word config |
| Permissions | Per-service scope toggles, approval queue |
| Memory | Searchable memory list, privacy controls |
| Schedule | Recurring tasks, briefing history |
| Skills | Installed skills, marketplace browser |
| Costs | Model usage, spending, optimization |
| Audit Log | Full searchable action history |
| Settings | System configuration |

---

## Quick Start
```bash
# One command
./install.sh

# Start Koda
./koda start

# Open the dashboard
open http://localhost:3000
```

Docker:
```bash
docker compose up
```

### CLI

| Command | Action |
|---------|--------|
| `./koda start` | Start Koda |
| `./koda stop` | Stop Koda |
| `./koda status` | Show status |
| `./koda logs` | View logs |
| `./koda test` | Run tests |
| `./koda dev` | Dev mode with hot-reload |
| `./koda update` | Pull latest |
| `./koda doctor` | Diagnose issues |

### Platforms

| Platform | Status |
|----------|--------|
| macOS | ✅ Supported (Apple Silicon optimized) |
| Linux | ✅ Supported |
| Windows | ✅ Supported |
| Docker | ✅ Supported |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python 3.11+ · FastAPI · SQLite · Pydantic |
| Frontend | Next.js 14 · React · TypeScript · Tailwind CSS |
| Voice | Kokoro TTS · Piper TTS · MLX Whisper · OpenWakeWord |
| LLM | Anthropic Claude + OpenAI GPT (runtime-switchable) |
| Browser | Playwright + Chrome Extension |
| Deploy | Docker Compose or native install |

---

## How Koda Compares

| | The Other Guy | Koda |
|---|--------------|------|
| **Honesty** | Claims success on failure | Independent verification of every action |
| **Security** | Plaintext credentials | AES-256-GCM encrypted vault |
| **UI** | Chat apps and terminals | Purpose-built 23-page dashboard |
| **Voice** | Cloud-based | 100% local — your voice never leaves your machine |
| **Permissions** | All-or-nothing | Deny-by-default, 4-tier risk classification |
| **Personality** | "Reality check, Mike" | Warm, configurable, never condescending |
| **Setup** | Complex CLI | One-command installer |
| **Skills** | 12% malware rate | Sandboxed and verified |
| **Smart Home** | No | Govee + Home Assistant (2,000+ devices) |
| **Email** | Basic | Multi-account IMAP/SMTP with classification |
| **SMS** | No | Twilio with conversations and alerts |
| **Multi-Agent** | No | 6 agent types with orchestration |
| **Audit Trail** | None | Full searchable action history |

---

## Pricing

| Tier | Price |
|------|-------|
| **Self-Hosted** | **Free forever** — full features, open source, your hardware |
| Personal | $19/month — managed hosting |
| Pro | $49/month — unlimited integrations |
| Team | $99/month — multi-user, shared workflows |
| Business | $199/month — full platform, Company Builder, API |
| Enterprise | Custom — on-premises, SSO, compliance |

---

## Early Access

Koda is feature complete and in testing. Sign up at **[heykoda.ai](https://heykoda.ai)** to be the first to know when it drops.

---

## The Story

I'm Mike Wandzilak — a web designer and server admin from Florida. I'm not a VC-backed startup. I'm not a Silicon Valley insider. I'm a guy who installed the leading AI agent, watched it lie to me, and decided to build something better.

I named it Koda, which means "friend," because an AI agent should be a friend — not a criminal you let into your office.

🌐 [heykoda.ai](https://heykoda.ai) · 🐦 [@HeyKodaAI](https://x.com/HeyKodaAI) · 💻 [GitHub](https://github.com/HeyKodaAI)

---

## License

MIT — Open source. Open book. Always.

---

<div align="center">

**Open Source. Open Book. Koda AI.**

Built with honesty. Powered by kindness. Secured by design.

🐾

</div>
