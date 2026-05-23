# Sortie

> Every AI agent. One mission control. Run Claude, Codex, Gemini, Hermes, Pi, Amp, Claw, Kilo, and SoulFire from a single iOS app.

**Website:** https://sortie.fly.dev
**TestFlight:** https://testflight.apple.com/join/1jB6HJ9m
**Install (Mac CLI):** `brew tap thebasedcapital/sortie && brew install sortie`

---

## What is this repo for?

This is the **public issue tracker** for Sortie. Use it to:

- Report bugs you hit during the TestFlight beta
- Request features
- Ask questions about install, pairing, or agent behavior

The Sortie codebase is currently private during beta. This repo is issues-only.

## How to report a bug

1. Run `sortie doctor` in your terminal and paste the output
2. Open a new issue: https://github.com/thebasedcapital/sortie/issues/new/choose
3. Include: what you did, what you expected, what actually happened

## How Sortie works

```
┌─────────────────────┐         ┌─────────────────────┐
│   iPhone (Sortie)   │  E2E    │   Mac (sortie CLI)  │
│   mission control   │ ◄─────► │   runs the agents   │
└─────────────────────┘ libsodium└─────────────────────┘
                                          │
                                          ▼
                              claude / codex / gemini / ...
```

The Mac CLI runs the actual agent. The iOS app is the remote-control surface. The relay server (Fly.io) can't read message content — keys live on your devices.

## Requirements

- macOS (Apple Silicon or Intel) with Homebrew
- iOS 17 or newer
- At least one of: `claude`, `codex`, or `gemini` CLI installed

## Links

| | |
|---|---|
| **Landing** | https://sortie.fly.dev |
| **TestFlight** | https://testflight.apple.com/join/1jB6HJ9m |
| **Brew tap** | https://github.com/thebasedcapital/homebrew-sortie |
| **Privacy** | https://sortie.fly.dev/privacy.html |

## License

The CLI is MIT-licensed (see the brew tap). The iOS app source will be opened after v1.0.
