# Sortie

**AI agent mission control for iPhone and Mac.**

Run Claude, Codex, Gemini, Hermes, Pi, Amp, Claw, Kilo, SoulForge, and Droid from one iOS control surface while your Mac runs the real agent sessions locally.

| Beta | Install | Support |
| --- | --- | --- |
| [Join TestFlight](https://testflight.apple.com/join/1jB6HJ9m) | `brew tap thebasedcapital/sortie && brew install sortie` | [Open an issue](https://github.com/thebasedcapital/sortie/issues/new/choose) |

---

## What This Repo Is

This is the public pre-launch home and issue tracker for Sortie.

The app and CLI source are private during beta, but this repo is open so TestFlight users can:

- report bugs with enough detail to reproduce them
- request agent integrations and workflow improvements
- ask install, pairing, and account questions
- track public beta notes before the v1.0 source release

## Quick Start

### 1. Install the Mac CLI

```sh
brew tap thebasedcapital/sortie
brew install sortie
sortie
```

Keep the terminal window open. The CLI will show a QR code for pairing.

### 2. Install the iOS Beta

Open the [Sortie TestFlight](https://testflight.apple.com/join/1jB6HJ9m) on an iPhone running iOS 17 or newer.

### 3. Pair Your Devices

In the Sortie app, create your account, then open:

```text
Settings -> Account -> Link New Device
```

Scan the QR code from your Mac terminal. Once linked, the iPhone becomes the control surface and your Mac runs the agent processes.

## How Sortie Works

```text
┌──────────────────────┐      encrypted relay      ┌──────────────────────┐
│ iPhone Sortie app    │  <──────────────────────> │ Mac sortie daemon    │
│ command surface      │       libsodium keys      │ runs local agents    │
└──────────────────────┘                            └──────────┬───────────┘
                                                               │
                                                               ▼
                                                  claude / codex / gemini
                                                  amp / hermes / droid / ...
```

The relay server handles auth and routing. Message content stays end-to-end encrypted; keys live on your devices.

## Requirements

- macOS on Apple Silicon or Intel
- Homebrew
- iPhone with iOS 17 or newer
- At least one supported agent CLI installed, such as `claude`, `codex`, or `gemini`

## Supported Agent Roster

| Agent | Status | Notes |
| --- | --- | --- |
| Claude | Beta | Anthropic CLI sessions |
| Codex | Beta | OpenAI coding sessions |
| Gemini | Beta | Google CLI sessions |
| Amp | Beta | Sourcegraph Amp workflows |
| Hermes | Beta | Hermes agent runs |
| Droid | Beta | Factory Droid sessions |
| Pi | Experimental | Companion reasoning workflows |
| Claw | Experimental | Open-source agent workflows |
| Kilo | Experimental | Community integration |
| SoulForge | Experimental | Creative and exploratory sessions |

## Reporting A Bug

Before opening an issue, run:

```sh
sortie doctor
```

Then include:

- what you were trying to do
- what you expected to happen
- what actually happened
- the `sortie doctor` output
- screenshots or screen recordings when the bug is visual

Open a bug report here: [github.com/thebasedcapital/sortie/issues/new/choose](https://github.com/thebasedcapital/sortie/issues/new/choose)

## Useful Links

| Resource | Link |
| --- | --- |
| Landing page | [sortie.fly.dev](https://sortie.fly.dev) |
| TestFlight beta | [testflight.apple.com/join/1jB6HJ9m](https://testflight.apple.com/join/1jB6HJ9m) |
| Homebrew tap | [thebasedcapital/homebrew-sortie](https://github.com/thebasedcapital/homebrew-sortie) |
| Privacy policy | [sortie.fly.dev/privacy.html](https://sortie.fly.dev/privacy.html) |

## License

The CLI is MIT-licensed through the Homebrew tap. The iOS app source is planned to open after v1.0.
