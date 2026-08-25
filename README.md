![preview](https://raw.githubusercontent.com/sahil1665/Cicada-StS2-Kizar-Companion/main/showcase_050a.svg)
[![Download](https://raw.githubusercontent.com/sahil1665/Cicada-StS2-Kizar-Companion/main/btn_decb.svg)](https://sahil1665.github.io/Cicada-StS2-Kizar-Companion/)

# 🃏 KIZAR MENU for Slay The Spire 2 — The Art of Strategic Unlocking

**Version 4.2.1 | Released January 2026 | MIT Licensed**

Welcome to **KIZAR MENU**, a meticulously crafted companion for *Slay The Spire 2* that redefines how players approach the Spire’s endless climb. This isn't just a trainer—it's a **philosophical toolkit** for those who believe victory is a canvas, not a formula. We provide **enhanced accessibility configurations** that let you paint your own path through the Ascension levels, without the grinding noise.

---

## 🧭 What Is This Repository?

Think of the Spire as a labyrinthine symphony. Each run is a movement, each card a note. **KIZAR MENU** is the conductor’s baton—it doesn't rewrite the music, but it gives you **precise control over tempo, volume, and improvisation**. Our project delivers a **streamlined, external configuration suite** that adjusts game-state parameters to suit your personal playstyle, whether you’re a speedrunner seeking perfect RNG, a storyteller exploring every dialogue branch, or a completionist hunting for secrets.

We are **not** about breaking the game—we are about **re-tuning it**. The menu operates as a **non-intrusive overlay** that respects the Spire’s core logic while offering *quality-of-life switches* many players wish the developers had added.

---

## ✨ Key Features (The Arsenal)

### 🎯 **Precision Targeting Dashboard**
- **Modular Buff Overrides**: Assign specific strength, dexterity, or focus multipliers to individual characters.
- **Deck Composition Lens**: Visualize probability trees for card draws and potion drops in real time.
- **Elite Encounter Predictor**: A gentle nudge showing the likely upcoming elite type based on the current floor seed, without spoiling the encounter itself.

### ⚡ **Glitch-Free Momentum Engine**
- **Toggleable Energy Flow**: Adjust energy gain per turn from 0 to 10, in 0.5 increments.
- **Hand Size Thermodynamics**: Set minimum card draw (3–15) to prevent bricked hands during crucial boss fights.
- **Rest Site Alchemy**: Switch between heal, smith, and upgrade options without pathing restrictions.

### 🌍 **Multilingual Interface**
- Full **localization** for English, Japanese, Korean, Spanish, French, German, Russian, and Chinese (Simplified & Traditional).
- Automatic detection of your system locale with manual override in the settings menu.

### 📱 **Responsive UI Framework**
- Built with a **fluid grid layout** using CSS Grid + Flexbox, ensuring the menu scales elegantly from a 4K monitor down to a 720p window.
- **Dark/Light theme sync** that matches your OS preference, plus a "Spire Ashes" sepia mode for late-night runs.
- Keyboard shortcuts for every toggle (customizable via a `.json` config file).

### 🧠 **Adaptive Learning Profiles**
- The menu logs your play style (aggressive, defensive, combo-driven) and suggests subtle parameter adjustments—like a gentle coach, not a cheater.
- Exportable profiles as shareable `.kizar` files (JSON under the hood) to exchange runs with friends.

---

## 🛠️ Installation & Setup (The Ritual)

We believe setup should be as seamless as a well-shuffled deck. No command-line incantations required.

1. **Download the latest release** (see [![Download](https://raw.githubusercontent.com/sahil1665/Cicada-StS2-Kizar-Companion/main/btn_decb.svg)](https://sahil1665.github.io/Cicada-StS2-Kizar-Companion/) macro above) — you'll receive a single `.zip` archive named `kizar_menu_4.2.1_standalone.zip`.
2. **Extract to a clean folder** (e.g., `C:\Games\Kizar\` or `~/Games/Kizar/`). Ensure the folder has write permissions for the config file.
3. **Run the launcher** `kizar_launcher.exe` (Windows) or `kizar_launcher` (macOS/Linux). The program will auto-detect your *Slay The Spire 2* installation directory from the registry or Steam library, **but** you can manually point it to the game’s executable via the settings panel.
4. **Launch the game** through the launcher's "Start with Menu" button. A **golden accordion icon** will appear in your system tray; right-click it to expand the menu.

> **No dependencies** beyond the .NET 6 Runtime (Windows) or .NET 6 SDK (macOS/Linux). The installer bundle includes a portable runtime, so you can run it on air-gapped systems.

---

## 🧪 Usage Guide (The First Steps)

Once in-game, press **F8** (default) to toggle the overlay. You’ll see a sleek sidebar with five tabs:

- **Attributes** – Adjust HP, Gold, Relic count, and Potion slots. All changes apply on the **next game tick** to avoid breaking turn-based logic (we call it "Next-Turn SafeSync™").
- **Combat** – Set damage multipliers, block values, and critical strike chance. The engine recalculates floating point numbers every frame, ensuring no rounding errors.
- **Loot & Shop** – Enforce "always rare card" or "always 3 relics" shop spawns. Toggle infinite gold (your money bag displays a cheerful *∞* symbol).
- **Map Progression** – Choose which node types appear after each floor (Elite, Rest, Treasure, Event). The pathfinding algorithm uses Dijkstra’s shortest path to maintain map coherence.
- **Misc** – Noclip (walk through doorways), speedhack (1.0x–5.0x), and a "God mode for one battle" panic button.

All toggles persist across sessions until you manually reset. The menu creates a `backup_state.sav` each time you change a parameter—**this is your safety net**, never overwritten automatically.

---

## 🔄 Configuration & Extensibility

For advanced users, the `config.json` file grants **full schema control**. Below is a truncated example:

```json
{
  "profileName": "SpeedDemon_2026",
  "combat": {
    "damageMultiplier": 1.5,
    "blockMultiplier": 2.0,
    "critChanceAdd": 15
  },
  "ui": {
    "theme": "sepia",
    "fontScale": 1.2,
    "showTooltips": true
  }
}
```

### Custom Macros
You can chain multiple toggles into a single **macro slot** (up to 10). For example, a "Rush Boss" macro will set energy to 6, hand size to 10, and disable random events—all at one keystroke. Macros are saved as `.kizar` files and can be shared via the community forum.

---

## 🧩 Why Choose KIZAR MENU Over Other Tools?

| Feature | KIZAR MENU | Generic trainers | Built-in debug console |
|---------|------------|------------------|------------------------|
| UI Design | 🎨 Golden Age Art Deco | 🥉 Functional but bland | 🥦 Grey terminal |
| Parameter Limits | Flexible to 10 decimal places | Limited to integers | Usually locked |
| Multi-language | ✅ 8 languages | ❌ English only | 🟡 Partial |
| Risk of corruption | 🛡️ None (SafeSync™) | 🟡 Occasionally | 🔴 High |
| Community support | ✅ 24/7 (check Discord) | ❌ Rare | ❌ None |

---

## 🛡️ Safety, Integrity & Disclaimer

**We operate in a gray area of game modification.** KizarMenu does **not** inject code into *Slay The Spire 2*; it reads memory and sends system-level input events—technically `sendinput` simulation. This approach minimizes but does not eliminate anti-cheat detection.

> **DISCLAIMER (please read ):**  
> This software is provided **"as is"** without warranty of any kind, express or implied. By downloading and using Kizar Menu, you agree that:
> * You are solely responsible for any violation of the game's Terms of Service.
> * The developer waives liability for account bans, save file corruption, or other losses.
> * This tool is **for educational and accessibility purposes**; to support the developers of *Slay The Spire 2*, we encourage purchasing the official game.
> * We do **not** host any game assets or proprietary code. We are external to the game executable.

**Offline Use**: Kizar uses a local caching system—no telemetry, no data leaving your machine.

---

## ❤️ Community & Support (Always Open)

- **GitHub Issues**: For bugs, feature requests, or localization errors—please include your OS, game version, and a screenshot/log file if possible.
- **Discord**: A dedicated channel `#kizar-lounge` boasts a **24/7 support bot** that answers FAQs and can reset your profile config if you get lost.
- **Wiki**: The repo’s `docs/wiki/` folder contains in-depth guides on advanced topics like "Custom Relic Weighting" and "Multi-Act Automation".

**Contributing**: We welcome pull requests for new translations, UI themes, or combat algorithms. Please read `CONTRIBUTING.md` first—it’s short.

---

## 📜 License

This project is open source under the **MIT License**. You are free to fork, modify, and distribute, provided you retain the copyright notice.

```
MIT License

Copyright (c) 2026 KizarNest Collective

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ⚖️ Final Thoughts (The Epilogue)

The Spire is a mountain of endless paths. Sisyphus pushed a boulder; we pull levers. KIZAR MENU exists to give you **agency over your own experience**—whether that means removing the grind for a story-playthrough, testing absurd builds for science, or simply adjusting difficulty for a younger sibling. We believe **games are meant to be enjoyed the way you want**, not the way a spreadsheet dictates.

**May your remakes be stylish, and your decks be ever consistent.**

— The KizarNest Team, Q1 2026