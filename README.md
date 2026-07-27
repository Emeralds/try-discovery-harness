# Discovery Harness

For founders stuck after `/office-hours`: the thesis is sharp, but
validating it means talking to real people, and that's usually where it
stalls.

Import your discovery-handoff YAML (or type a hypothesis in by hand) and
Discovery Harness finds real people who might feel the pain, states
specifically why each one is worth contacting, and drafts outreach that's
ready to send. Nothing goes out automatically — you approve everything.

**[Download for Windows](https://github.com/Emeralds/try-discovery-harness/releases/download/v0.10.1/Discovery.Harness.Setup.0.10.1.exe)** ·
**[Download for Mac (Apple Silicon)](https://github.com/Emeralds/try-discovery-harness/releases/download/v0.10.1/Discovery.Harness-0.10.1-arm64.dmg)** ·
**[Intel Mac / all releases](https://github.com/Emeralds/try-discovery-harness/releases/tag/v0.10.1)**

## Requirements

- **Windows 10/11** or **macOS 12+** (Apple Silicon or Intel).
- Your own **OpenAI** or **Anthropic API key** ([get one from OpenAI](https://platform.openai.com/api-keys)
  or [Anthropic](https://console.anthropic.com/settings/keys)) — the app is
  local-first and bring-your-own-key: research and drafting calls go
  straight from your machine to your own provider account, never through a
  server I run. You paste the key into Settings on first run; it's
  encrypted at rest.
- Optional: [Claude Code](https://claude.com/claude-code) with the `gstack`
  skill and the [`discovery-harness-skill`](https://github.com/Emeralds/discovery-harness-skill)
  (`discovery-handoff`) skill, if you want to import a structured targeting
  YAML instead of typing a hypothesis in by hand. Not required — every
  field works either way.

## Install

Both builds are **unsigned** — this is a solo project without a
code-signing budget yet. It's safe, just unfamiliar to your OS:

### Windows

1. Download the `.exe` above and run it.
2. Windows SmartScreen will say *"Windows protected your PC."* Click
   **More info**, then **Run anyway**.
3. Follow the installer.

### Mac

1. Download the `.dmg` above and open it, then drag the app to
   Applications.
2. On first launch, Gatekeeper will block it. **Right-click** (or
   Control-click) the app in Applications → **Open** → confirm **Open** in
   the dialog that appears.
3. After that first launch, it opens normally like any other app.

## First run

1. Open the app. A **Getting Started** guide walks you through the basics
   the first time — reopen it anytime from the header.
2. Click the **Settings** icon and paste in your OpenAI and/or Anthropic
   API key, then pick which provider/model handles **research** (web
   search) vs. **drafting** (chat).
3. Add your first product hypothesis — either **Import from
   discovery-handoff** (if you have a YAML from the gstack skill) or fill
   in the form by hand: name, one-sentence thesis, target customer,
   problem hypothesis, and what you most need to learn.
4. From there: find companies or prospects, review why each one is
   relevant, generate an outreach draft, and approve it before it's ever
   marked sent. A daily send cap and human approval are hard-coded —
   nothing sends on its own.

## FAQ

**Why isn't this open source?**
It's early. I want to see how it holds up outside my own use before
opening the source — might revisit that later.

**Why do I need my own API key?**
Local-first and BYOK means your research and drafting calls go straight
from your machine to your own OpenAI/Anthropic account, so there's no
server in between reading your hypothesis, prospects, or drafts.

**Do I need Claude Code / gstack to use this?**
No. It's richer with a discovery-handoff YAML import (see Requirements
above), but every field can be filled in by hand and the app works fully
without either installed.

**Where does my data live?**
On your own machine, in a local database in your OS's per-user app-data
folder. Nothing is uploaded anywhere except your own research/drafting
calls to your own configured OpenAI/Anthropic account.

## Feedback

Found a bug, or something confusing? Use the in-app **Give feedback**
button (bottom-right on every page), or open an issue on this repo.
