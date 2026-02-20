# 🍌 TRAC Minion Clicker

> A fun P2P clicker game built on top of [Intercom](https://github.com/Trac-Systems/intercom) — the Trac Network agent communication stack.

## 🎮 What is this?

**TRAC Minion Clicker** is a browser-based idle/clicker game where players tap a Minion wearing a TRAC hat to earn TNK (simulated). It demonstrates how Intercom's peer-to-peer sidechannel infrastructure can power lightweight, interactive agent apps in-browser.

<img width="1204" height="820" alt="image" src="https://github.com/user-attachments/assets/9a24b64d-bedc-45a2-b7eb-4b75cb4d0cad" />

### Features
- 🍌 Click the Minion to earn TNK
- ⚡ Combo system — rapid clicks multiply your earnings
- 🛒 Upgrade shop (Banana Power, TRAC Goggles, Minion Army, Diamond Hat, Rocket, Mega Minion)
- 🤖 Auto-clicker unlocked via upgrades
- 🏆 Milestone achievements (10 clicks → 100K TNK)
- 👁️ Interactive Minion — eyes follow your mouse cursor
- 📦 Single file (`index.html`) — zero dependencies, runs in any browser

## 🚀 How to Run

```bash
# Clone this repo
git clone https://github.com/YOUR_USERNAME/intercom.git
cd intercom

# Just open in browser:
open index.html
# or
python3 -m http.server 8080
```

Then visit `http://localhost:8080`

## 📸 Screenshots

The app features:
- A fully custom SVG Minion character with animated TRAC hat
- A dark-themed UI with cyan/gold color palette
- Floating banana background animation
- Combo flash effects and floating TNK particles
- Upgrade cards and milestone tracker
- TRAC address input field for payout registration

## 🔗 Intercom Integration

This fork uses the Intercom P2P sidechain concept:
- **App logic** runs in the browser as a lightweight agent
- **State** is maintained locally (compatible with Intercom's replicated-state layer)
- **Agent skills** are defined in `SKILL.md` for Intercom agent coordination

## 💰 TRAC Address

```
trac14ye0c2yzg7jfv9ng2nsy80dme633t283jlqjgkxvng47tesqjpjshepqnm
```

> Replace the above with your actual Trac address to qualify for the 500 TNK payout from the Awesome Intercom list.

## 📋 Skill File

See [`SKILL.md`](./SKILL.md) for agent instructions.

## 📄 License

MIT — Fork freely, build cool stuff, earn TNK. 🚀
