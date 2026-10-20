# ⚔️ ENDLESS HORDE: SURVIVE

A fast, neon sci-fi **endless survival shooter** that runs entirely in your browser. Move, auto-fire, collect XP, pick an upgrade every level-up, build something absurd, and survive the horde for as long as you can. There are no stages and no final boss. You fight until you die, then try to beat your own best score.

### 🎮 [Play it now](https://a4x-coder.github.io/Endless-Horde/)

Works on Android phones (portrait) and desktop browsers. No install, no login, no ads.

---

## ✨ Features

- **Pure endless gameplay.** Difficulty rises continuously with survival time: more enemies, tougher enemies, faster enemies, and periodic horde surges.
- **Auto-targeting combat.** You only worry about movement and positioning. Your weapons find targets themselves.
- **Level-up upgrade picks.** The game pauses and offers 3 random upgrades each level. Builds change every run.
- **Weapon synergies.** Piercing + multishot, missiles + damage boosts, blades + shields, and more.
- **6 distinct enemy types** with different shapes and behaviours, including a periodic Elite mini-boss.
- **Temporary pickups** that drop from enemies: repair, magnet, invincibility, overcharge, blast wave.
- **Combo scoring** that rewards fast kill streaks.
- **Permanent Armory.** Spend coins earned in runs on small, capped permanent upgrades.
- **Local save.** Best score, best time, and coins persist between sessions in your browser.
- **Fully procedural.** All graphics are drawn on Canvas and all sounds are synthesized with the Web Audio API. There are no image or audio files.

---

## 🕹️ Controls

| Platform | Move | Pause | Pick upgrade |
|---|---|---|---|
| **Mobile / Touch** | Touch and drag anywhere on the screen to spawn a floating joystick | Pause button (top-right) | Tap a card |
| **Desktop** | `W` `A` `S` `D` or Arrow keys (or click-and-drag with the mouse) | `P` or `Esc` | Click a card or press `1` `2` `3` |

Attacks are automatic. The game also auto-pauses if you switch tabs or the window loses focus.

---

## 👾 Enemies

| Enemy | Behaviour |
|---|---|
| **Grunt** | Basic chaser with low health. |
| **Runner** | Fast and fragile. Forces constant movement. |
| **Brute** | Large, slow, and very tanky. Hits hard. |
| **Ranged** | Keeps its distance and fires projectiles at you. |
| **Exploder** | Rushes you, arms a short fuse, then detonates in an area blast. |
| **Elite** | Gold spiked mini-boss with lots of health that appears periodically. Guaranteed coin drop and a high chance of a pickup. |

Enemies spawn just outside the screen and never on top of you. Every ~55 seconds a **horde surge** rolls in from one direction.

---

## 🧬 Upgrades (picked during a run)

| Upgrade | Effect | Max rank |
|---|---|---|
| Rapid Reloader | +20% fire rate | 5 |
| Multishot Matrix | +1 bullet per volley | 4 |
| Depleted Energy Core | +1 bullet pierce | 3 |
| Plasma Orbital Blade | +1 orbiting blade that shreds nearby enemies | 4 |
| Tesla Discharger | Chain lightning that zaps groups of enemies | 4 |
| Seeker Rockets | Homing missiles with splash damage | 4 |
| Support Drone | +1 autonomous drone that shoots enemies | 3 |
| Overcharged Rounds | +18% damage on all weapons | 5 |
| Rail Accelerator | +20% bullet speed | 3 |
| Aegis Shield | Absorbs one hit, recharges every 12 seconds | 3 |
| Servo Overdrive | +15% movement speed | 5 |
| Graviton Siphon | +35% pickup radius | 5 |
| Nano Reinforced Hull | +30 max HP and an instant heal | 5 |
| Bio-Regen Nanites | +1.2 HP per second | 4 |
| Targeting Matrix | +12% critical hit chance | 4 |

Every upgrade has a rank cap so builds stay powerful without becoming broken.

---

## 🎁 Pickups

| Pickup | Effect |
|---|---|
| **Repair** | Restores 35% of max health. |
| **Ultra Magnet** | Pulls every gem on the map to you. |
| **Invincibility** | 6 seconds of full damage immunity. |
| **Overcharge** | 8 seconds of doubled attack speed. |
| **Blast Wave** | Large explosion that damages every enemy around you. |

---

## 🏆 Scoring

Score comes from actual play, not just time:

- Points for every kill, with higher values for tougher enemies (Elites are worth 200 base)
- A **combo multiplier** that grows while you keep killing within a short window
- Bonus points at every 25-kill combo milestone
- A small passive score for surviving

Your **best score is saved the moment you beat it**, not only at Game Over.

After each run you earn **coins** from the ones you collect, plus a performance bonus for survival time and kills.

---

## 🛡️ Armory (permanent upgrades)

Spend banked coins on small permanent bonuses. All have 5 ranks with rising costs, so they help without destroying balance.

| Upgrade | Bonus per rank |
|---|---|
| Reinforced Plating | +18 starting max HP |
| Overclocked Emitters | +10% base weapon damage |
| Attractor Coils | +22 px pickup radius |
| Ion Thrusters | +8% movement speed |

---

## 🧱 Tech

- Single self-contained `index.html` using plain **HTML, CSS, JavaScript, and Canvas 2D**
- No libraries, frameworks, build tools, backend, or external assets
- `requestAnimationFrame` loop with delta-time movement and clamped frame deltas
- Object pooling for bullets, capped particle, gem, and text counts, and a limit on live enemies
- Pointer Events for multi-touch safe controls
- Web Audio API sound effects with a mute toggle (audio only starts after the first interaction)
- `localStorage` persistence with safe fallbacks if storage is unavailable
- Safe-area insets and dynamic canvas scaling for phones with notches and different screen ratios

---

## 🚀 Run locally

No setup is required.

```bash
git clone https://github.com/A4X-Coder/Endless-Horde.git
cd Endless-Horde
```

Then open `index.html` in any modern browser. To serve it locally instead:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## 🌐 Deploy your own copy

1. Fork or clone the [repository](https://github.com/A4X-Coder/Endless-Horde).
2. Keep `index.html` at the repository root.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, select your main branch and the `/ (root)` folder, then save.
4. After a minute or two the game is live at `https://<your-username>.github.io/<repo-name>/`.

---

## 👤 Author

Created by **A4X-Coder** · [GitHub profile](https://github.com/A4X-Coder)

---

## 📄 License

No license is specified in this repository unless a LICENSE file is added. Until then, reuse and redistribution permissions should not be assumed.
