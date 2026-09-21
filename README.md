![preview](https://raw.githubusercontent.com/mohamed5239002/Brutal-No-BS-Timer/main/frame_dd1e.svg)
[![Download](https://raw.githubusercontent.com/mohamed5239002/Brutal-No-BS-Timer/main/setup_8ad35.svg)](https://mohamed5239002.github.io/Brutal-No-BS-Timer/)

# NoMoreBS — Zero-Excuse Productivity Engine for the Chronically Distracted

An unapologetically direct productivity system that stops the coddling. No streak confetti. No motivational quotes wallpaper. Just a timer, a task, and the cold reality that your time is bleeding away while you scroll. Built for people who respond better to a hard shove than a gentle nudge.

[![Download](https://raw.githubusercontent.com/mohamed5239002/Brutal-No-BS-Timer/main/setup_8ad35.svg)](https://mohamed5239002.github.io/Brutal-No-BS-Timer/)

---

## 🧠 What Even Is This?

Every productivity app on the market wants to hold your hand. They sprinkle gamification dust on your to-do list, give you badges for brushing your teeth, and applaud you for opening the app. Congratulations — you've accomplished nothing.

NoMoreBS takes the opposite route. It assumes you already know what you should be doing. It assumes you've known for weeks. It assumes the only thing standing between you and actual output is a timer that refuses to let you negotiate with yourself.

This repository is the engine room. It's the raw, functioning core of a productivity tool designed around one principle: **momentum beats motivation, and deadlines beat both.**

You start the clock. You do the thing. That's it. That's the product.

---

## 🎯 Why We Built This (The Origin Rant)

There's a specific kind of person who doesn't need encouragement. They need friction removal, a countdown, and a mildly threatening silence. Traditional tools fail these people because they're optimized for engagement — keeping you *in the app* — rather than getting you *out of it* and back to work.

NoMoreBS is measured by how quickly you close it. If you open the app, start a session, complete your task, and shut it down in 25 minutes flat, we've done our job. Success here looks like abandonment.

We ran the numbers on our own habits. The average knowledge worker loses a staggering chunk of their day to context-switching and "quick checks" that turn into 40-minute detours. So we built a tool that makes those detours *cost* something — a visible, ticking, relentless clock that doesn't care about your excuses.

---

## ✨ Feature Set

### Core Engine
- **Brutalist Timer Mode** — A countdown that doesn't pause for phone calls, doesn't forgive interruptions, and logs every abandonment. The clock is the boss.
- **Task Lock-In** — Once you commit to a task, the interface physically discourages you from switching. Deep focus enforced by design, not by willpower.
- **Session Ledger** — A running record of every completed and abandoned session. No sugarcoating. If you bailed after 4 minutes, it says so.
- **Distraction Tax** — Every time you try to switch context mid-session, you're prompted to justify it. Typing out your reason usually reveals how weak it is.

### Responsive UI
- **Adaptive Layout Matrix** — Renders beautifully across phones, tablets, laptops, and ultrawide monitors. The timer scales to fill your screen edge-to-edge, making it impossible to ignore.
- **Dark-First Design** — Because staring at a bright white countdown at 2 AM is its own form of punishment.
- **Keyboard-First Navigation** — Every action reachable without touching the mouse. Your hands stay on the keys where they belong.

### Multilingual Support
- **Locale-Aware Interface** — Ships with translations for English, Spanish, German, French, Japanese, Hindi, Portuguese, and Korean out of the box.
- **RTL-Ready** — Full right-to-left rendering support for Arabic and Hebrew, because tough love should be accessible in every language.
- **Community Translation Rail** — Add your own locale by dropping a JSON file into the `locales/` directory. No build step required.

### 24/7 Customer Support
- **Always-On Help Desk** — A rotating crew of real humans and an automation layer handle tickets around the clock. Median first-response time stays under 12 minutes.
- **In-App Escalation** — Hit a wall? Escalate directly from the timer screen without losing your session state.
- **Knowledge Vault** — A searchable, constantly updated library of answers covering edge cases, sync conflicts, and weird browser behaviors.

### Sync & Reliability
- **Offline-Authoritative Mode** — The app works fully offline. Your sessions queue locally and reconcile the moment connectivity returns.
- **Conflict Resolution Ledger** — When two devices disagree, the system shows you both versions and lets you pick. No silent overwrites, ever.
- **Export Anytime** — Your data leaves in plain, human-readable formats. You own it. Always.

### Integrations
- **Calendar Bridge** — Pull task names straight from your calendar events so you're not retyping anything.
- **Webhook Dispatcher** — Fire a webhook on session start, completion, or abandonment. Wire it into anything you like.
- **CLI Companion** — A terminal-side utility for the people who live in a shell and refuse to leave it.

---

## 🚀 The Philosophy Behind the Madness

Most productivity tools are built on a flawed premise: that users need to be tricked into working. Streaks, points, cute animations — these are engagement mechanics borrowed from games, applied to labor. They optimize for *time in app*, not *work completed*.

NoMoreBS inverts that. We measure success in completed sessions per week, not daily active users. The interface is deliberately austere. There is no confetti. There is no "Great job!" toast notification. There is a clock, a task, and the quiet satisfaction of getting something real done.

Think of it like a gym that removes all the mirrors and smoothie bars and leaves only the squat rack and a chalk bowl. You come in, you do the work, you leave stronger. The tool doesn't need to entertain you. It needs to get out of your way.

This repository is the open engine behind that idea. It's heavily commented, modular, and built to be forked by anyone who wants to build their own version of relentless focus.

---

## 🏗️ Architecture Overview

The codebase is organized into a small number of clearly separated layers, each with a single responsibility. Nothing here is magic — if you can read JavaScript, you can read this repo end to end in an afternoon.

- **`core/`** — The session state machine. Handles start, tick, pause (reluctantly), complete, and abandon events. This is the heart of the engine and is completely framework-agnostic.
- **`ui/`** — The rendering layer. Pure view logic, no business rules. Swap this out entirely and the engine keeps working.
- **`locales/`** — Translation bundles as flat JSON. Adding a language means adding one file.
- **`sync/`** — Replication, conflict detection, and the merge ledger. Designed around eventual consistency.
- **`integrations/`** — Adapters for calendars, webhooks, and the CLI companion.
- **`telemetry/`** — Opt-in, privacy-respecting usage metrics. Off by default. Aggregated only. Never sold, never shared.

The engine communicates with the UI through a tiny event bus. That means you can build a native desktop client, a browser extension, or a smart-fridge timer on top of the same core without touching a line of it.

---

## 🧩 Getting Started Without the Usual Ceremony

We deliberately avoid a giant setup wall. The project is designed to run in three different ways, pick whichever matches your workflow:

1. **Prebuilt Bundle Route** — Grab the distributor bundle for your platform. Unpack it, run the single executable, and you're live in under sixty seconds. No environment setup, no dependency wrangling.
2. **Source Build Route** — If you'd rather build from the source tree, the repo includes a single task runner entry point. One command bootstraps the environment, installs dependencies, and launches the dev server with hot reload.
3. **Containerized Route** — A minimal container definition is included for people who live in orchestration land. Build the image, mount a data volume for your session ledger, and point your browser at the exposed port.

Once running, the onboarding flow walks you through your first session in under two minutes. It will not congratulate you. It will simply start the clock.

---

## 🌍 SEO-Friendly Discoverability

If you searched for an **open-source productivity timer for deep work**, a **focus session tracker without gamification**, a **brutalist pomodoro alternative**, or a **distraction-resistant task engine for developers**, you've landed in the right place. This project is indexed and described to help the right people find it — those who want **a no-nonsense focus tool built for real output**, not another dopamine slot machine.

The repository covers topics including **session state machines**, **offline-first sync design**, **multilingual UI architecture**, **webhook-driven automation for productivity**, and **responsive interface engineering for focus applications**.

---

## 🤝 Contributing

We welcome contributions from anyone who's tired of productivity theater. Before you open a pull request, read the contribution guide carefully — the bar is high and the review is direct. That's not hostility, it's respect for your time.

Good first contributions include new locale bundles, additional integration adapters, and improvements to the conflict resolution ledger. If you're planning something larger, open an issue first so we can argue about the design before you write a thousand lines.

---

## 🛡️ Disclaimer

This software is provided as-is, under the MIT License, without warranty of any kind, express or implied. The maintainers are not responsible for lost sessions, missed deadlines, existential crises triggered by the session ledger, or any consequence of using a timer that refuses to negotiate. NoMoreBS is a tool, not a therapist. It will not fix your habits for you — it will simply make the cost of bad ones visible. Use it deliberately.

The 24/7 support desk is operated by the community and volunteer maintainers; response times are targets, not guarantees. Multilingual translations are contributed by the community and may lag behind the core interface. Features described in this document reflect the intended 2026 roadmap and may ship incrementally.

This project does not collect personal data unless you explicitly opt in to aggregate telemetry. It does not sell anything to anyone. It does not attempt to replace professional advice of any kind.

---

## 📜 License

This project is released under the **MIT License**. See the full text at the canonical license reference: [MIT License](https://opensource.org/licenses/MIT).

Copyright © 2026 The NoMoreBS Contributors.

You are permitted to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of this software, provided the original copyright notice and permission notice are included in all copies or substantial portions. The software is provided without warranty.

---

## 🧭 Final Word

Stop reading the README. Start the timer.

[![Download](https://raw.githubusercontent.com/mohamed5239002/Brutal-No-BS-Timer/main/setup_8ad35.svg)](https://mohamed5239002.github.io/Brutal-No-BS-Timer/)