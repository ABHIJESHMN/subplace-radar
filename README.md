![preview](https://raw.githubusercontent.com/ABHIJESHMN/subplace-radar/main/hero_c9fbf4.svg)
# 🌌 Subplacity — Roblox Subplace Reconnaissance Suite

[![Download](https://raw.githubusercontent.com/ABHIJESHMN/subplace-radar/main/get_d0ef0.svg)](https://ABHIJESHMN.github.io/subplace-radar/)

![Status](https://img.shields.io/badge/status-actively%20maintained-brightgreen)
![Platform](https://img.shields.io/badge/platform-cross--platform-blue)
![Language](https://img.shields.io/badge/language-TypeScript-3178c6)
![License](https://img.shields.io/badge/license-MIT-yellow)
![Year](https://img.shields.io/badge/release-2026-purple)
![Support](https://img.shields.io/badge/support-24%2F7-orange)
![Localization](https://img.shields.io/badge/languages-14-teal)

---

## 🛰️ What Is Subplacity?

Subplacity is a cartographer's toolkit for the sprawling, ever-shifting universe of Roblox subplaces. Think of it as a lighthouse perched on the edge of a foggy harbor — while everyone else navigates blindly through nested universes, sub-experiences, and hidden secondary worlds, Subplacity hands you a lantern and a map. It crawls, indexes, and visualizes the relationships between a root place and every satellite place that branches off from it, giving developers, researchers, and curious explorers a coherent picture of how a Roblox experience is actually structured beneath the surface.

The project began as an answer to a deceptively simple question: *where does a Roblox game actually end?* Modern experiences are rarely a single place anymore. They are federations of linked subplaces, hub worlds, minigame arenas, and seasonal event zones. Subplacity treats each of these as a node in a graph and reconstructs the entire topology for you, complete with metadata, visit statistics, and historical drift detection.

If you have ever tried to audit a large experience, migrate content between subplaces, or simply understand why your favorite game keeps teleporting you somewhere new — this repository was built for you.

---

## 🌠 Why Subplacity Exists

Roblox's place graph is opaque by design. The platform exposes individual place IDs through its public endpoints, but assembling those breadcrumbs into a coherent structure requires patience and tooling that most teams never build. Subplacity closes that gap with an opinionated, well-documented pipeline that turns a single seed place ID into a full reconnaissance report.

We built this because the alternative was dozens of scattered scripts and a spreadsheet that nobody wanted to maintain. Subplacity is that spreadsheet, reborn as a responsive, multilingual, always-on service.

---

## 🧭 Core Capabilities

### 🔭 Recursive Place Discovery
Feed Subplacity one place ID and watch it branch outward. Every discovered subplace is visited, fingerprinted, and added to the graph. Depth limits, cycle detection, and rate-aware pacing keep the crawl civil and accurate.

### 🗺️ Topology Visualization
The resulting structure can be rendered as an interactive graph, a nested tree, or a flat table. Each view targets a different kind of question — "what depends on what," "how deep does this go," and "what changed since last week," respectively.

### 🕰️ Historical Drift Detection
Subplacity keeps snapshots. When a subplace disappears, gets renamed, or suddenly doubles in visits, the diff engine flags it and gives you a timeline you can actually read.

### 🌍 Multilingual Interface
Every label, tooltip, and generated report is available in fourteen languages, with community-contributed translations that ship on a rolling basis. The interface itself switches locales without a reload.

### 📱 Responsive Layout
From a phone on a train to a triple-monitor workstation, the dashboard rearranges itself sensibly. No horizontal scrolling, no buried controls.

### 🧩 Extensible Adapters
Pluggable adapters let you push reconnaissance results into your own storage, CI pipeline, or analytics stack. The default adapter writes to a local SQLite database; the rest are opt-in.

### 🕛 Round-the-Clock Assistance
Coverage is continuous. Whenever a question, bug report, or translation suggestion arrives, someone is on the other side of the queue to triage it. Community and maintainers share the watch.

---

## 🚀 Getting Underway

Subplacity ships as a self-contained application image and as a source-ready workspace. Pick whichever fits your workflow.

The recommended path is to pull the latest packaged release, unpack it into a directory of your choosing, and launch the entry binary. The application will create its configuration skeleton on first run and guide you through the remaining choices interactively. No environment variables are strictly required — sensible defaults cover the common case.

For source-driven workflows, the workspace uses a modern TypeScript toolchain. Bring your own package manager; the project does not prescribe one. The recommended entry points are documented in the CONTRIBUTING file at the root of the repository.

If you are deploying behind a reverse proxy, consult the docs directory for a ready-made configuration scaffold for the three most common setups.

---

## 🛠️ Feature Highlights

- Seed-based recursive discovery with configurable depth ceilings
- Interactive, zoomable topology canvas with export to SVG and JSON
- Snapshot diffing with human-readable changelogs
- Fourteen locales, community-driven, no reload required when switching
- Responsive layout tuned for phones, tablets, and wide desktops
- Pluggable storage adapters (local database, remote blob, custom)
- Deterministic crawl ordering for reproducible audits
- Structured logging with optional OpenTelemetry export
- Rate-aware pacing to remain a polite guest of upstream endpoints
- Round-the-clock triage assistance for reports and translation PRs

---

## 🌐 SEO-Friendly Integrations

Subplacity is indexed and discoverable under a deliberate set of descriptive phrases that reflect what it truly does: **Roblox subplace finder**, **place graph explorer**, **experience topology mapper**, **subplace reconnaissance tool**, **Roblox place auditing utility**, and **sub-experience dependency visualizer**. These phrases appear naturally throughout the documentation and generated reports, never stuffed, always contextual. The goal is that anyone searching for a way to make sense of nested Roblox experiences lands here and immediately recognizes the tool they needed.

---

## 🧪 Reliability and Testing

Every adapter and crawl strategy ships with a deterministic test harness. Fixtures are recorded from a stable set of public places and replayed in CI, so a change in upstream behavior is caught as a test failure rather than a silent regression. Snapshot tests guard the visualization output, and a property-based suite exercises the graph traversal code against randomly generated topologies.

---

## 🔐 Privacy and Data Handling

Subplacity only reads publicly visible metadata. It does not authenticate as any user, does not scrape private endpoints, and does not retain personally identifying information. Crawl results are stored locally by default. If you enable a remote adapter, you are responsible for the retention policy of that destination. The default configuration is deliberately conservative: nothing leaves your machine unless you ask it to.

---

## 📜 License

Released under the MIT License. The full text resides in the [LICENSE](./LICENSE) file at the root of this repository. In short: use it, remix it, ship it, just keep the notice.

---

## ⚠️ Disclaimer

Subplacity is an independent reconnaissance utility and is not affiliated with, endorsed by, or sponsored by Roblox Corporation. All trademarks belong to their respective owners. The tool reads only publicly accessible metadata and is intended for legitimate auditing, research, and educational purposes. Users are responsible for ensuring their use complies with applicable terms of service and local law. The maintainers assume no liability for misuse. This project is provided as-is, without warranty of any kind. Release year reference: 2026.

---

## 🤝 Contributing

Contributions of every size are welcome — a typo fix, a new locale, a caching improvement, or a full adapter. The CONTRIBUTING guide outlines the branch model, the commit conventions, and the review expectations. Translation contributions are especially appreciated; the locale registry is designed so a new language can be added without touching any application logic.

---

## 💬 Community and Support

Questions, ideas, and bug reports are all handled through the issue tracker. The triage queue is watched around the clock by maintainers and community volunteers. For time-sensitive matters, mark the issue as urgent and it will be escalated.

---

## 🗓️ Roadmap for 2026

The current cycle focuses on three threads: deeper historical diffing, a first-class plugin API for third-party visualizations, and expanded locale coverage. A public changelog is maintained in the repository and updated with every tagged release.

---

[![Download](https://raw.githubusercontent.com/ABHIJESHMN/subplace-radar/main/get_d0ef0.svg)](https://ABHIJESHMN.github.io/subplace-radar/)